---
draft: "true"
---
//------Filter for selecting posts by semester------//

// Register ?semester= as a recognised URL param
add_filter( 'query_vars', function( $vars ) {
    $vars[] = 'semester';
    return $vars;
});

// Inject semester dropdown inline with the archive title
add_filter( 'render_block', function( $block_content, $block ) {
    if ( $block['blockName'] !== 'core/query-title' ) return $block_content;
    if ( ! is_category( 'capstone-test' ) ) return $block_content;

    $category = get_queried_object();

    $posts = get_posts([
        'category'    => $category->term_id,
        'numberposts' => -1,
        'fields'      => 'ids',
    ]);

    if ( empty( $posts ) ) return $block_content;

    $semesters = [];
    foreach ( $posts as $post_id ) {
        $month = (int) get_the_date( 'n', $post_id );
        $year  = (int) get_the_date( 'Y', $post_id );

        if ( $month >= 1 && $month <= 5 )     $term = 'Spring';
        elseif ( $month >= 6 && $month <= 8 ) $term = 'Summer';
        else                                   $term = 'Fall';

        $key = strtolower( $term ) . '-' . $year;
        $semesters[ $key ] = $term . ' ' . $year;
    }
	
	//sort by year first, then semester
	uksort( $semesters, function( $a, $b ) {
		$order = [ 'spring' => 1, 'summer' => 2, 'fall' => 3 ];
		list( $a_term, $a_year ) = explode( '-', $a );
		list( $b_term, $b_year ) = explode( '-', $b );
		if ( $a_year !== $b_year ) return (int) $b_year - (int) $a_year;
		return $order[ $b_term ] - $order[ $a_term ];
	});

    $current  = get_query_var( 'semester', '' );
    $base_url = get_term_link( $category );

    $dropdown  = '<select onchange="window.location=this.value">';
    $dropdown .= '<option value="' . esc_url( $base_url ) . '"' . ( ! $current ? ' selected' : '' ) . '>All Semesters</option>';

    foreach ( $semesters as $slug => $label ) {
        $url      = esc_url( add_query_arg( 'semester', $slug, $base_url ) );
        $selected = ( $current === $slug ) ? ' selected' : '';
        $dropdown .= '<option value="' . $url . '"' . $selected . '>' . esc_html( $label ) . '</option>';
    }

    $dropdown .= '</select>';

    return '<div style="display:flex; align-items:center; justify-content:space-between; margin-bottom:1em;">'
        . $block_content
        . '<div>' . $dropdown . '</div>'
        . '</div>';

}, 10, 2 );

// Filter the Query Loop block's query when ?semester= is in the URL
add_filter( 'query_loop_block_query_vars', function( $query, $block ) {
    if ( ! is_category( [ 'news', 'events' ] ) ) return $query;

    $semester = get_query_var( 'semester', '' );
    if ( ! $semester ) return $query;

    $parts = explode( '-', $semester );
    $year  = (int) end( $parts );
    $term  = strtolower( $parts[0] );

    $ranges = [
        'spring' => [ 'month_start' => 1, 'month_end' => 5  ],
        'summer' => [ 'month_start' => 6, 'month_end' => 8  ],
        'fall'   => [ 'month_start' => 9, 'month_end' => 12 ],
    ];

    if ( ! isset( $ranges[ $term ] ) ) return $query;

    $query['date_query'] = [[
        'after'     => [ 'year' => $year, 'month' => $ranges[ $term ]['month_start'], 'day' => 1  ],
        'before'    => [ 'year' => $year, 'month' => $ranges[ $term ]['month_end'],   'day' => 31 ],
        'inclusive' => true,
    ]];

    return $query;

}, 10, 2 );


//------End filter for selecting posts by semester------//

