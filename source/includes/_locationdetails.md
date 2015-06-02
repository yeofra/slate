# Location Details
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
