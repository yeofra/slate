# Locations List
```python
import requests
url = 'https://dev.spotskim.com/api/phone/2_5/locations/'
parameters = {
    'near_latitude': '41.9803581', 
    'near_longitude': '-87.6647797',
    'distance' : '200'
}
headers = {'Authorization': '204db7bcfafb2deb7506b89eb3b9b715b09905c8'}
response = request.get(url, parameters, headers)
```

> The above command returns JSON structured like this 

```json
{
    "meta": {
        "limit": 20,
        "next": null,
        "offset": 0,
        "previous": null,
        "total_count": 3
    },
    "objects": [
        {
            "address_line1": "5413 N Glenwood Ave",
            "asset_count": 31,
            "city": "Chicago",
            "distance": 0,
            "id": 28,
            "latitude": 41.9803581,
            "longitude": -87.6647797,
            "name": "Andersonville",
            "organization": 9,
            "state": "IL",
            "zipcode": "60640"
        },
        {
            "address_line1": "6538 N Sheridan Rd",
            "asset_count": 5,
            "city": "Chicago",
            "distance": 1.46,
            "id": 50,
            "latitude": 42.0012081,
            "longitude": -87.66074,
            "name": "Rogers Park",
            "organization": 9,
            "state": "IL",
            "zipcode": "60626"
        },
        {
            "address_line1": "869 W Buena Ave",
            "asset_count": 16,
            "city": "Chicago",
            "distance": 1.64,
            "id": 43,
            "latitude": 41.9584503,
            "longitude": -87.6525574,
            "name": "UpTown",
            "organization": 9,
            "state": "IL",
            "zipcode": "60613"
        }
    ]
}
```

### HTTP Request
`GET https://dev.spotskim.com/2_5/locations/`

### Query Parameters
Parameter | Required | Value
--------  | -------- | -----
near_latitude | Y    | latitude for the reference point
near_longitude| Y    | longitude for the reference point
distance      | N    | radius in which to search for locations

### Headers
Header | Value
------ | -----
authorization | ApiKey info@inspectpos.com:50f69f0..

### Notes
1. Results are always ordered by distance from the reference point, if `near_longitude`, and `near_longitude` are present and valid 
2. Results are always limited to 20 per page with the reference to the next page provided in `meta`
3. If `distance` is not specified the default radius assumed is 10.00 miles 
4. If `near_latitude` and `near_longitude` are not valid types, then the error is `HTTP 400`
5. If `near_latitude` and `near_longitude` are valid values, but nothing is found within 10 miles around those values, blank array is returned
6. 
