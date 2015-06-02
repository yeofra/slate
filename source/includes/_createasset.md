# Create a new Asset
> To create an asset, use this code:

```python
import requests
url = 'https://dev.spotskim.com/api/phone/2_5/assets/'
headers = {'Authorization': 'ApiKey user@spotksim.com:204db7bcfafb2deb7506b89eb3b9b715b09905c8'}
parameters = {
  "tag":"102345678",
  "asset_type":46,
  "latitude":42.0106749,
  "longitude":-87.6659234,
  "sublocation_name":"lane 10",
  "unexpected":false 
}
response = request.post(url, parameters, headers)
```

> The above command returns a JSON structure like this:

```json
{
  "added_datetime": "2015-06-02T18:24:16",
  "asset_type": {
    "description": "Card processing kiosks such as ones used for ticket vending machines, food kiosks, receipt lookup kiosks, etc.,",
    "id": 46,
    "image": "https://spotskim-dev-thumbnails.s3.amazonaws.com/asset_primary_angles/Bus_Ticket_Machine.png?Signature=%2BdggJ6PyxxjO9BrhgJkoqixHnok%3D&Expires=1433273056&AWSAccessKeyId=AKIAIWXP3QT3ECK4SGFQ",
    "name": "Kiosk",
    "order": 2
  },
  "device_status": "not_in_use",
  "due_angles": [
    {
      "id": 142,
      "image": null,
      "name": "Swipe slot",
      "upload_url": "https://spotskim-dev-images.s3-us-west-2.amazonaws.com/uploads/9/328/2015-06-02T182416-f806056e/142.jpg?Signature=tYgFtT1wgpx8MepieL8HIrJgnog%3D&Expires=1434479056&AWSAccessKeyId=AKIAIWXP3QT3ECK4SGFQ&x-amz-acl=private"
    },
    {
      "id": 143,
      "image": null,
      "name": "Keypad",
      "upload_url": "https://spotskim-dev-images.s3-us-west-2.amazonaws.com/uploads/9/328/2015-06-02T182416-f806056e/143.jpg?Signature=xOl8Ddwj7CFwRionnOBujmb72rs%3D&Expires=1434479056&AWSAccessKeyId=AKIAIWXP3QT3ECK4SGFQ&x-amz-acl=private"
    }
  ],
  "due_questions": [
    {
      "answers": [
        {"id": 615, "text": "No"},
        {"id": 616, "text": "Yes"}
      ],
      "frequency": "always",
      "id": 308,
      "long_text": "Are the color and general condition of the terminal as described, with no additional marks or scratches?",
      "short_text": "Condition correct?"
    },
    {
      "answers": [
        {"id": 613, "text": "No"},
        {"id": 614, "text": "Yes"}
      ],
      "frequency": "always",
      "id": 307,
      "long_text": "Are the manufacturer's security seals and labels present, with no signs of peeling or tampering?",
      "short_text": "Seals present?"
    }
  ],
  "id": 328,
  "is_compliant": true,
  "is_compromised": false,
  "is_due": false,
  "last_check_in": null,
  "latitude": 42.0106749,
  "location": {
    "id": 50,
    "latitude": 42.0012081,
    "longitude": -87.66074,
    "name": "Rogers Park"
  },
  "longitude": -87.6659234,
  "maintenance": null,
  "risk_rating": "low",
  "sublocation": null,
  "sublocation_name": "lane 10",
  "tag": "102345678",
  "thumbnail": "https://spotskim-dev-thumbnails.s3.amazonaws.com/asset_primary_angles/Bus_Ticket_Machine.png?Signature=%2BdggJ6PyxxjO9BrhgJkoqixHnok%3D&Expires=1433273056&AWSAccessKeyId=AKIAIWXP3QT3ECK4SGFQ"
}
```

### HTTP Request
`POST https://dev.spotskim.com/api/phone/2_5/assets/`

### Parameters
Parameter | Required | Description
--------- | -------- | -----------
tag | Yes | Barcode present on the asset
asset_type | Yes | Asset type id, determines the kind of asset it is.
latitude | No | The latitude of the user at time of asset creation. This should be pulled from the device's GPS. If not provided, the system will default to the user's current_location.
longitude | No | See latitude.
sublocation_name | No | The name of the sublocation that this asset belongs to.
unexpected | No | Indicates whether or not the device was 'expected', for purposes of internal security. Default: false

### Return Values
Return Value | Meaning 
------------ | --------
201          | No error, asset created.
400          | Asset_type not valid.

### Headers
Header | Value
------ | -----
Authorization | ApiKey info@inspectpos.com:50f69f0..