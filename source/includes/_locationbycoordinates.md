# Location by Coordinates
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
