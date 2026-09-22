when we were talking about how the router assigns IP addresses when users connect, i noted my IP address in class: 10.20.54.237, and then i wrote down IP my address at school a couple days later: 10.20.54.237. turns out they were the same, although i don't remember if that's expected behavior or not.

at first, i found the traceroute to be a bit disappointing. either it stopped getting responses after a couple hops at home or after leaving the nyu networks while at school, or it turned out to be a pretty short number of hops. then i started looking through it was interesting to see whose networks my packets were being routed through. i got a bunch of cloudflare ip addresses in my routes as well as my ISP, optimum. it was also interesting to see which traceroutes made it to their destination quickly and which ones stopped getting responses before they reached their destination. youtube, facebook, and my email host proton mail all responded pretty quickly, but wikipedia timed out after only 6 hops, all within my isp's network. 

one interesting terminal command i learned while doing this process that was sort of unrelated to the assignment was `tee`, which i used to send the output of traceroute to both the terminal's stdout as well as a text file i used to save the output. i used it like this:

```
traceroute wikipedia.org | tee output.txt
```

i found it to be quite useful in order to save the output automatically to a file but also see it in the terminal in realtime, which can't be done with something like `>>` 

when i looked at some geolocations, i didn't see too much that was surprising, although there were some discrepancies between the different services i tried out. i found the traceroute mapper site to be useful and interesting, but it didn't seem to be very accurate and it was a little hard to understand the maps display of the route. ip2location.io worked quite well, although the amount of information provided was a bit overwhelming, as seen in the example below

Here's a map from traceroute mapper of my traceroute to youtube.com:

![[class 2-1790051857791.webp]]

as far as i can tell, the only points on the map are from nodes in my isp's network, and it left out the last hop which ended at google's servers. this particular server seems to be registered in california, as seen below, but doesn't show up on the map. i began to question traceroute mapper's accuracy after seeing this discrepancy.

```powershell
curl "https://api.ip2location.io/?ip=142.251.200.104"

{
    "ip": "142.251.200.104",
    "country_code": "US",
    "country_name": "United States of America",
    "region_name": "California",
    "district": "Santa Clara County",
    "city_name": "Mountain View",
    "latitude": 37.38605,
    "longitude": -122.08385,
    "zip_code": "94043",
    "time_zone": "-07:00",
    "asn": "15169",
    "as": "Google LLC",
    "as_info": {
        "as_number": "15169",
        "as_name": "Google LLC",
        "as_domain": "google.com",
        "as_usage_type": "DCH",
        "as_cidr": "142.251.192.0/20"
    },
    "isp": "Google LLC",
    "domain": "google.com",
    "net_speed": "T1",
    "idd_code": "1",
    "area_code": "650",
    "weather_station_code": "USCA0746",
    "weather_station_name": "Mountain View",
    "mcc": "-",
    "mnc": "-",
    "mobile_brand": "-",
    "elevation": 32,
    "usage_type": "DCH",
    "address_type": "Unicast",
    "ads_category": "622",
    "ads_category_name": "Web Hosting",
    "continent": {
        "name": "North America",
        "code": "NA",
        "hemisphere": [
            "north",
            "west"
        ],
        "translation": {
            "lang": "en",
            "value": "North America"
        }
    },
    "country": {
        "name": "United States of America",
        "alpha3_code": "USA",
        "numeric_code": 840,
        "demonym": "Americans",
        "flag": "https://cdn.ip2location.io/assets/img/flags/us.png",
        "capital": "Washington, D.C.",
        "total_area": 9826675,
        "population": 339665118,
        "currency": {
            "code": "USD",
            "name": "United States Dollar",
            "symbol": "$"
        },
        "language": {
            "code": "EN",
            "name": "English"
        },
        "tld": "us",
        "translation": {
            "lang": "en",
            "value": "United States of America"
        }
    },
    "region": {
        "name": "California",
        "code": "US-CA",
        "translation": {
            "lang": "en",
            "value": "California"
        }
    },
    "city": {
        "name": "Mountain View",
        "translation": {
            "lang": "en",
            "value": "Mountain View"
        }
    },
    "time_zone_info": {
        "olson": "America/Los_Angeles",
        "current_time": "2026-09-21T21:39:39-07:00",
        "gmt_offset": -25200,
        "is_dst": true,
        "abbreviation": "PST",
        "dst_start_date": "2026-03-08",
        "dst_end_date": "2026-11-01",
        "sunrise": "06:56",
        "sunset": "19:08"
    },
    "geotargeting": {
        "metro": "807"
    },
    "is_proxy": false,
    "fraud_score": 3,
    "proxy": {
        "last_seen": 1,
        "proxy_type": "DCH",
        "threat": "-",
        "provider": "-",
        "is_vpn": false,
        "is_tor": false,
        "is_data_center": true,
        "is_public_proxy": false,
        "is_web_proxy": false,
        "is_web_crawler": false,
        "is_ai_crawler": false,
        "is_residential_proxy": false,
        "is_consumer_privacy_network": false,
        "is_enterprise_private_network": false,
        "is_spammer": false,
        "is_scanner": false,
        "is_botnet": false,
        "is_bogon": false
    }
}
```

Here's a very zoomed out map of a traceroute to my email host in switzerland. this was as far as my traceroute traveled as far as i could tell

![[class 2-1790052175389.webp]]