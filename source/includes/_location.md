# Location

## Near Locations
> To get the list of nearby locations, use this code:

```python
import requests
url = 'https://dev.spotskim.com/api/phone/2_5/locations/'
parameters = {
    'near_latitude': '41.9803581', 
    'near_longitude': '-87.6647797',
    'distance' : '200'
}
headers = {'Authorization': 'ApiKey user@spotksim.com:204db7bcfafb2deb7506b89eb3b9b715b09905c8'}
response = request.get(url, parameters, headers)
```

> The above command returns JSON structured like this:

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
`GET https://dev.spotskim.com/api/phone/2_5/locations/`

### Query Parameters
Parameter | Required | Value
--------  | -------- | -----
near_latitude | Yes    | latitude for the reference point
near_longitude| Yes    | longitude for the reference point
distance      | No    | radius in which to search for locations

### Headers
Header | Value
------ | -----
Authorization | ApiKey info@inspectpos.com:50f69f0..

### Notes
1. Results are always ordered by distance from the reference point, if `near_longitude`, and `near_longitude` are present and valid 
2. Results are always limited to 20 per page with the reference to the next page provided in `meta`
3. If `distance` is not specified the default radius assumed is 10.00 miles 
4. If `near_latitude` and `near_longitude` are not valid types, then the error is `HTTP 400`
5. If `near_latitude` and `near_longitude` are valid values, but nothing is found within 10 miles around those values, blank array is returned


## Location by Coordinates
> To get the closest location using coordinates, use this code:

```python
import requests
url = 'https://dev.spotskim.com/api/phone/2_5/locations/get_by_coordinates/?latitude=0.0&longitude=0.0'
headers = {'Authorization': 'ApiKey user@spotksim.com:204db7bcfafb2deb7506b89eb3b9b715b09905c8'}
response = request.get(url, headers)
```

> The above command returns JSON structured like this:

```json
{
  "address_line1": "19 Stenholm",
  "asset_count": 2,
  "assets": [
    {
      "asset_type": {
        "description": "Card processing kiosks such as ones used for ticket vending machines, food kiosks, receipt lookup kiosks, etc.,",
        "id": 46,
        "image": "https://spotskim-dev-thumbnails.s3.amazonaws.com/asset_primary_angles/Bus_Ticket_Machine.png?Signature=nlDc2yRC0h%2FdLphWRIUnmxcy76w%3D&Expires=1433271680&AWSAccessKeyId=AKIAIWXP3QT3ECK4SGFQ",
        "name": "Kiosk",
        "order": 2
      },
      "device_status": "not_in_use",
      "id": 178,
      "is_compliant": true,
      "is_compromised": false,
      "is_due": false,
      "last_inspected": "2015-03-16T13:48:45",
      "last_inspector": {
        "id": 52,
        "name": "Vasu  Nagendra",
        "username": "vasu@safecard.io"
      },
      "risk_rating": "high",
      "sublocation": null,
      "tag": "NEWA4",
      "thumbnail": "https://spotskim-dev-images.s3.amazonaws.com/vasu%40safecard.io/2015_02_17_17/rtmgbbpmszhw/NEWA4/IMG_142.jpg_thumb.jpg?Signature=M%2FJKu37AhBFEHGo5zh7tFm9sEWw%3D&Expires=1433271680&AWSAccessKeyId=AKIAIWXP3QT3ECK4SGFQ"
    },
    {
      "asset_type": {
        "description": "A Credit card terminal, also known as a Payment Terminal or EFTPOS Terminal. Terminals allow for swipe, dip, of credit cards. This includes dial-up terminals as well as Multi-Lane terminals, such as the ones connected to Cash Register via a cable.",
        "id": 44,
        "image": "https://spotskim-dev-thumbnails.s3.amazonaws.com/asset_primary_angles/cardterminal2.png?Signature=RyujN8gxi96X5IaYW%2FSk5qq2ATE%3D&Expires=1433271680&AWSAccessKeyId=AKIAIWXP3QT3ECK4SGFQ",
        "name": "Terminal",
        "order": 0
      },
      "device_status": "not_in_use",
      "id": 169,
      "is_compliant": true,
      "is_compromised": false,
      "is_due": false,
      "last_inspected": "2015-03-16T14:20:03",
      "last_inspector": {
        "id": 52,
        "name": "Vasu  Nagendra",
        "username": "vasu@safecard.io"
      },
      "risk_rating": "high",
      "sublocation": null,
      "tag": "newbysimon",
      "thumbnail": "https://spotskim-dev-images.s3.amazonaws.com/info%40inspectpos.com/2015-02-10-19/mgjjavqxdtos/newbysimon/IMG_135.jpg_thumb.jpg?Signature=vUvaV%2FZ8tv0Csu51fX1ZZvjWEEo%3D&Expires=1433271680&AWSAccessKeyId=AKIAIWXP3QT3ECK4SGFQ"
    }
  ],
  "city": "Aalborg",
  "distance": 3981.25,
  "id": 34,
  "latitude": 57.0723,
  "longitude": 9.8829403,
  "name": "North Operations",
  "organization": 9,
  "state": "Nordjylland",
  "zipcode": "9400"
}
```

### HTTP Request
`GET https://dev.spotskim.com/api/phone/2_5/locations/get_by_coordinates/?latitude=0.0&longitude=0.0`

### URL Parameters
Parameter | Required | Value
--------  | -------- | -----
latitude | Yes    | latitude for the reference point
longitude| Yes    | longitude for the reference point

### Headers
Header | Value
------ | -----
Authorization | ApiKey info@inspectpos.com:50f69f0..

### Return Values
Return Value | Meaning 
------------ | --------
200          | No error, call successful.
500 | latitude or longitude url parameter is missing.


## Location Details
> To get the Location details, use this code:

```python
import requests
url = 'https://dev.spotskim.com/api/phone/2_5/locations/1/'
headers = {'Authorization': 'ApiKey user@spotksim.com:204db7bcfafb2deb7506b89eb3b9b715b09905c8'}
response = request.get(url, headers)
```

> The above command returns JSON structured like this (same object as "current_location" in User Details request):

```json
{
  "address_line1": "555 N Michigan Ave",
  "asset_count": 2,
  "assets": [
    {
      "asset_type": {
        "description": "Unattended Fuel Dispenser with an integrated card reader.",
        "id": 47,
        "image": "https://spotskim-dev-thumbnails.s3.amazonaws.com/asset_primary_angles/SpotSkim_Refueling_Pump.png?Signature=CPh%2BezV208iLbh0b8%2FAelmNCOac%3D&Expires=1433270607&AWSAccessKeyId=AKIAIWXP3QT3ECK4SGFQ",
        "name": "Gas Pump",
        "order": 3
      },
      "device_status": "not_in_use",
      "id": 111,
      "is_compliant": false,
      "is_compromised": false,
      "is_due": false,
      "last_inspected": null,
      "last_inspector": null,
      "risk_rating": "low",
      "sublocation": null,
      "tag": "p",
      "thumbnail": "https://spotskim-dev-thumbnails.s3.amazonaws.com/asset_primary_angles/SpotSkim_Refueling_Pump.png?Signature=CPh%2BezV208iLbh0b8%2FAelmNCOac%3D&Expires=1433270607&AWSAccessKeyId=AKIAIWXP3QT3ECK4SGFQ"
    },
    {
      "asset_type": {
        "description": "Card processing kiosks such as ones used for ticket vending machines, food kiosks, receipt lookup kiosks, etc.,",
        "id": 46,
        "image": "https://spotskim-dev-thumbnails.s3.amazonaws.com/asset_primary_angles/Bus_Ticket_Machine.png?Signature=eYjWcycmBHZ27Aasv5%2BoKYWtMNU%3D&Expires=1433270607&AWSAccessKeyId=AKIAIWXP3QT3ECK4SGFQ",
        "name": "Kiosk",
        "order": 2
      },
      "device_status": "not_in_use",
      "id": 113,
      "is_compliant": false,
      "is_compromised": false,
      "is_due": false,
      "last_inspected": null,
      "last_inspector": null,
      "risk_rating": "low",
      "sublocation": null,
      "tag": "jjsjs",
      "thumbnail": "https://spotskim-dev-thumbnails.s3.amazonaws.com/asset_primary_angles/Bus_Ticket_Machine.png?Signature=eYjWcycmBHZ27Aasv5%2BoKYWtMNU%3D&Expires=1433270607&AWSAccessKeyId=AKIAIWXP3QT3ECK4SGFQ"
    }
  ],
  "city": "Chicago",
  "id": 26,
  "latitude": 41.8921805,
  "longitude": -87.62416,
  "name": "North Michigan",
  "organization": 9,
  "state": "IL",
  "zipcode": "60611"
}
```

### HTTP Request
`GET https://dev.spotskim.com/api/phone/2_5/locations/1/`

<aside class="success">
Make sure to replace the corresponding location id in the url (.../locations/{location_id here}/)
</aside>


### Query Parameters
None

### Return Values
Return Value | Meaning
------------ | --------
200          | No error, call successful.
401          | Token used in the header has expired.
404          | Location not found.

### Headers
Header | Value
------ | -----
Authorization | ApiKey info@inspectpos.com:50f69f0..


## Get sublocations
> To get the sublocations of a specific location, use this code:

```python
import requests
url = 'https://dev.spotskim.com/api/phone/2_5/locations/50/sublocation/'
headers = {'Authorization': 'ApiKey user@spotksim.com:204db7bcfafb2deb7506b89eb3b9b715b09905c8'}
response = request.get(url, headers)
```

> The above command returns JSON structured like this:

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
      "id": 135,
      "latitude": 42.0042953,
      "longitude": -87.6626017,
      "name": "lane 1"
    },
    {
      "id": 198,
      "latitude": 42.0042566,
      "longitude": -87.6625714,
      "name": "lane 8a"
    },
    {
      "id": 206,
      "latitude": 42.00431710709071,
      "longitude": -87.66261517311584,
      "name": "lane 10"
    }
  ]
}
```

### HTTP Request
`GET https://dev.spotskim.com/api/phone/2_5/locations/50/sublocation/`

<aside class="success">
Make sure to replace the corresponding parameter in the url (.../locations/{location_id here}/sublocation/)
</aside>

### Query Parameters
None

### Return Values
Return Value | Meaning
------------ | --------
200          | No error, call successful.

### Headers
Header | Value
------ | -----
Authorization | ApiKey info@inspectpos.com:50f69f0..


## Sublocation Details
> To get the sublocation details, use this code:

```python
import requests
url = 'https://dev.spotskim.com/api/phone/2_5/locations/50/sublocation/178/'
headers = {'Authorization': 'ApiKey user@spotksim.com:204db7bcfafb2deb7506b89eb3b9b715b09905c8'}
response = request.get(url, headers)
```

> The above command returns JSON structured like this (same object as "sublocation" in Asset Details request):

```json
{
  "id": 178,
  "latitude": 41.8921805,
  "longitude": -87.62416,
  "name": "lane 5"
}
```

### HTTP Request
`GET https://dev.spotskim.com/api/phone/2_5/locations/50/sublocation/178/`

<aside class="success">
Make sure to replace the corresponding parameters in the url (.../locations/{location_id here}/sublocation/{sublocation_id here}/)
</aside>


### Query Parameters
None

### Return Values
Return Value | Meaning
------------ | --------
200          | No error, call successful.
404          | Sublocation not found.

### Note
1. `latitude` and `longitude` can be `null`.

### Headers
Header | Value
------ | -----
Authorization | ApiKey info@inspectpos.com:50f69f0..


## Modify Sublocation
> To patch the sublocation coordinates, use this code:

```python
import requests
url = 'https://dev.spotskim.com/api/phone/2_5/locations/50/sublocation/178/'
headers = {'Authorization': 'ApiKey user@spotksim.com:204db7bcfafb2deb7506b89eb3b9b715b09905c8'}
parameters = {
  "latitude": 41.8921805,
  "longitude": -87.62416
}
response = request.patch(url, parameters, headers)
```

> The above command returns JSON structured like this:

```json
{
  "id": 178,
  "latitude": 41.8921805,
  "longitude": -87.62416,
  "name": "lane 5"
}
```

### HTTP Request
`PATCH https://dev.spotskim.com/api/phone/2_5/locations/50/sublocation/178/`

<aside class="success">
Make sure to replace the corresponding parameters in the url (.../locations/{location_id here}/sublocation/{sublocation_id here}/)
</aside>


### Query Parameters
Parameter | Required | Description
--------- | -------- | -----------
latitude | No | The latitude to set on this sub-location.
longitude | No | See latitude

### Return Values
Return Value | Meaning
------------ | --------
202          | No error, call successful.
404          | Sublocation not found.

### Note
1. `latitude` and `longitude` CANNOT be `null`.
2. At least one of the two parameters has to be in the body.

### Headers
Header | Value
------ | -----
Authorization | ApiKey info@inspectpos.com:50f69f0..
