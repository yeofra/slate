# Asset Details
> To Get asset details, use this code:

```python
import requests
url = 'https://dev.spotskim.com/api/phone/2_5/assets/102345678/'
headers = {'Authorization': 'ApiKey user@spotksim.com:204db7bcfafb2deb7506b89eb3b9b715b09905c8'}
response = request.get(url, headers)
```

> The above command returns a JSON structure like this:

```json
{
  "added_datetime": "2015-06-02T18:24:16",
  "asset_type": {
    "description": "Card processing kiosks such as ones used for ticket vending machines, food kiosks, receipt lookup kiosks, etc.,",
    "id": 46,
    "image": "https://spotskim-dev-thumbnails.s3.amazonaws.com/asset_primary_angles/Bus_Ticket_Machine.png?Signature=FJzFp5RibvtOStro7WChdxhnl8g%3D&Expires=1433274598&AWSAccessKeyId=AKIAIWXP3QT3ECK4SGFQ",
    "name": "Kiosk",
    "order": 2
  },
  "device_status": "in_use",
  "due_angles": [
    {
      "id": 142,
      "image": "https://spotskim-dev-images.s3.amazonaws.com/uploads/9/328/2015-06-02T184910-67096542/142.jpg?Signature=T0eUuFcQtCrb56DthYSKsCS9ePg%3D&Expires=1433274598&AWSAccessKeyId=AKIAIWXP3QT3ECK4SGFQ",
      "name": "Swipe slot",
      "upload_url": "https://spotskim-dev-images.s3-us-west-2.amazonaws.com/uploads/9/328/2015-06-02T184958-5064e35a/142.jpg?Signature=ihMjOnemqq95U06h2pA1MY16fyA%3D&Expires=1434480598&AWSAccessKeyId=AKIAIWXP3QT3ECK4SGFQ&x-amz-acl=private"
    },
    {
      "id": 143,
      "image": "https://spotskim-dev-images.s3.amazonaws.com/uploads/9/328/2015-06-02T184910-67096542/143.jpg?Signature=h%2BDv2s9ZqEzToGJbMBdOqQ66sEM%3D&Expires=1433274598&AWSAccessKeyId=AKIAIWXP3QT3ECK4SGFQ",
      "name": "Keypad",
      "upload_url": "https://spotskim-dev-images.s3-us-west-2.amazonaws.com/uploads/9/328/2015-06-02T184958-5064e35a/143.jpg?Signature=EfQwj3aBYZmT3bx0JKxnKm3gxSc%3D&Expires=1434480598&AWSAccessKeyId=AKIAIWXP3QT3ECK4SGFQ&x-amz-acl=private"
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
  "last_check_in": {
    "datetime_inspected": "2015-06-02T18:49:39",
    "flag_as_compromised": false,
    "flag_as_compromised_comments": "",
    "id": 1069,
    "latitude": 42.00431710709071,
    "longitude": -87.66261517311584,
    "submitted_by": {
      "id": 52,
      "name": "Vasu  Nagendra",
      "username": "vasu@safecard.io"
    }
  },
  "location": {
    "id": 50,
    "latitude": 42.0012081,
    "longitude": -87.66074,
    "name": "Rogers Park"
  },
  "maintenance": null,
  "risk_rating": "low",
  "sublocation": {
    "id": 206,
    "latitude": 42.00431710709071,
    "longitude": -87.66261517311584,
    "name": "lane 10"
  },
  "tag": "102345678",
  "thumbnail": "https://spotskim-dev-images.s3.amazonaws.com/uploads/9/328/2015-06-02T184910-67096542/142.jpg_thumb.jpg?Signature=6%2FRN%2B%2Bt9SvFH6aiGcYpwl1LLkRE%3D&Expires=1433274598&AWSAccessKeyId=AKIAIWXP3QT3ECK4SGFQ"
}
```

### HTTP Request
`GET https://dev.spotskim.com/api/phone/2_5/assets/102345678/`

<aside class="success">
Make sure to replace the corresponding asset tag in the url (.../assets/{tag here}/)
</aside>


### Return Values
Return Value | Meaning 
------------ | --------
200          | No error, call successful.
404          | Asset not found.

### Headers
Header | Value
------ | -----
Authorization | ApiKey info@inspectpos.com:50f69f0..