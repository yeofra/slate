# Asset

## Create a new Asset
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

## Asset Details
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


## Request maintenance
> To request maintenance for an asset, use this code:

```python
import requests
url = 'https://dev.spotskim.com/api/phone/2_5/assets/102345678/request_maintenance/'
headers = {'Authorization': 'ApiKey user@spotksim.com:204db7bcfafb2deb7506b89eb3b9b715b09905c8'}
parameters = {
  "comment": "Here is the comment that justify the inspector request"
}
response = request.post(url, parameters, headers)
```

> The above command returns a JSON structure like this:

```json
{
  "comment": "Here is the comment that justify the inspector request",
  "id": 136,
  "request_by": {
    "id": 33,
    "name": "Edward Moore",
    "username": "info@inspectpos.com"
  },
  "request_comment": "Here is the comment that justify the inspector request",
  "request_datetime": "2015-06-02T20:15:44"
}
```

### HTTP Request
`POST https://dev.spotskim.com/api/phone/2_5/assets/102345678/request_maintenance/`

<aside class="success">
Make sure to replace the corresponding asset tag in the url (.../assets/{tag here}/request_maintenance/)
</aside>

### Parameters
Parameter | Required | Description
--------- | -------- | -----------
comment | Yes | Comment to attach to the maintenance request. 

### Return Values
Return Value | Meaning 
------------ | --------
201          | No error, maintenance requested.
400          | {"errors": "Can not request maintenance on an asset that is under maintenance."}


### Headers
Header | Value
------ | -----
Authorization | ApiKey info@inspectpos.com:50f69f0..


## Complete maintenance
> To complete maintenance for an asset, use this code:

```python
import requests
url = 'https://dev.spotskim.com/api/phone/2_5/assets/102345678/maintenance_complete/'
headers = {'Authorization': 'ApiKey user@spotksim.com:204db7bcfafb2deb7506b89eb3b9b715b09905c8'}
parameters = {
  "comment":"A comment to justify that the maintenance has been done",
  "activate":true
}
response = request.post(url, parameters, headers)
```

> The above command returns a JSON structure like this:

```json
{
  "activate": true,
  "comment": "A comment to justify that the maintenance has been done",
  "complete_activate": true,
  "complete_by": {
    "id": 33,
    "name": "Edward Moore",
    "username": "info@inspectpos.com"
  },
  "complete_comment": "A comment to justify that the maintenance has been done",
  "complete_datetime": "2015-06-02T20:22:54",
  "id": 136
}
```

### HTTP Request
`POST https://dev.spotskim.com/api/phone/2_5/assets/102345678/maintenance_complete/`

<aside class="success">
Make sure to replace the corresponding asset tag in the url (.../assets/{tag here}/maintenance_complete/)
</aside>

### Parameters
Parameter | Required | Description
--------- | -------- | -----------
comment | Yes | Comment to attach to the maintenance completion. 
activate | No | Determines whether asset will be marked as active now. Default: true

### Return Values
Return Value | Meaning 
------------ | --------
201          | No error, maintenance requested.
400          | "errors": "Can not complete maintenance on an asset that is not under maintenance."


### Headers
Header | Value
------ | -----
Authorization | ApiKey info@inspectpos.com:50f69f0..


## Flag asset as compromised
> To flag an asset as compromised, use this code:

```python
import requests
url = 'https://dev.spotskim.com/api/phone/2_5/assets/102345678/flag_compromised/'
headers = {'Authorization': 'ApiKey user@spotksim.com:204db7bcfafb2deb7506b89eb3b9b715b09905c8'}
parameters = {
  "comment":"A comment to justify that the asset looks compromised."
}
response = request.post(url, parameters, headers)
```

> The above command returns a JSON structure like this:

```json
{
  "id": 1073
}
```

### HTTP Request
`POST https://dev.spotskim.com/api/phone/2_5/assets/102345678/flag_compromised/`

<aside class="success">
Make sure to replace the corresponding asset tag in the url (.../assets/{tag here}/flag_compromised/)
</aside>

### Parameters
Parameter | Required | Description
--------- | -------- | -----------
comment | Yes | Explanation of the compromise.

### Return Values
Return Value | Meaning 
------------ | --------
201          | No error, asset has been flagged as compromised.
400          | "errors": "No recent check-in."
400          | "errors": "Asset already flagged compromised."


### Headers
Header | Value
------ | -----
Authorization | ApiKey info@inspectpos.com:50f69f0..


## Inspect an asset
> To post an inspection, use this code:

```python
import requests
url = 'https://dev.spotskim.com/api/phone/2_5/assets/706CB90528/check_in/'
headers = {'Authorization': 'ApiKey user@spotksim.com:204db7bcfafb2deb7506b89eb3b9b715b09905c8'}
parameters = {
  "responses": [
    {
      "question_id": 421,
      "answer_id": 841,
      "comments": "Found a camera in the ceiling."
    },
    {
      "question_id": 423,
      "answer_id": 845
    }
  ],
  "images": [
    {
      "angle_id": 24,
      "image": "https://s3bucket.s3-us-west-2.amazonaws.com/checkin123/image001.jpg"
    },
    {
      "angle_id": 25,
      "image": "https://s3bucket.s3-us-west-2.amazonaws.com/checkin123/image002.jpg"
    },
    {
      "angle_id": 26,
      "image": "https://s3bucket.s3-us-west-2.amazonaws.com/checkin123/image003.jpg"
    }
  ],
  "latitude": 40.32435,
  "longitude": -80.1234,
  "flag_as_compromised": true,
  "flag_as_compromised_comments": "Something looks bad!"
}
response = request.post(url, parameters, headers)
```

> The above command returns a JSON structure like this:

```json
{
  "id": 65
}
```

### HTTP Request
`POST https://dev.spotskim.com/api/phone/2_5/assets/706CB90528/check_in/`

### Parameters
Parameter | Required | Description
--------- | -------- | -----------
responses | Yes | Answers to questions. Provided as an array of objects composed of: question_id, answer_id, and comments.
images | No | Angle pictures of the inspected asset. Provided as an array of objects composed of: angle_id and image (url pointing to aws s3 bucket).
datetime_inspected | No | The date and time of the inspection, in ISO 8601. If left blank, the server will use the current time.
latitude | No | When present, latitude must also be present.
longitude | No | When present, longitude must also be present.
flag_as_compromised | No | Flag the asset as compromised using a boolean.
flag_as_compromised_comments | No | Provide a comment, to justify the flag.

#### Notes
1. Latitude and Longitude are major keys to the inspection since it determines the position of the inspected asset, it helps track and verify its location.
2. Flag an asset as compromised does not mean it is compromised yet. The reviewer decides if it is or not (using the portal).

### Return Values
Return Value | Meaning 
------------ | --------
201          | No error, post successful.

### Headers
Header | Value
------ | -----
Authorization | ApiKey info@inspectpos.com:50f69f0..


## Modify Asset
> To patch an asset sublocation, use this code:

```python
import requests
url = 'https://dev.spotskim.com/api/phone/2_5/assets/102345678/'
headers = {'Authorization': 'ApiKey user@spotksim.com:204db7bcfafb2deb7506b89eb3b9b715b09905c8'}
parameters = {
  "sublocation":"a name for the sublocation"
}
response = request.patch(url, parameters, headers)
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
  "sublocation": {
    "id": 34, 
    "latitude": null,
    "longitude": null,
    "name": "a name for the sublocation"
  },
  "tag": "102345678",
  "thumbnail": "https://spotskim-dev-thumbnails.s3.amazonaws.com/asset_primary_angles/Bus_Ticket_Machine.png?Signature=%2BdggJ6PyxxjO9BrhgJkoqixHnok%3D&Expires=1433273056&AWSAccessKeyId=AKIAIWXP3QT3ECK4SGFQ"
}
```

### HTTP Request
`PATCH https://dev.spotskim.com/api/phone/2_5/assets/102345678/`

<aside class="success">
Make sure to replace the corresponding asset tag in the url (.../assets/{tag here}/)
</aside>

### Parameters
Parameter | Required | Description
--------- | -------- | -----------
sublocation | No | The name of the sublocation that this asset belongs to.

### Return Values
Return Value | Meaning 
------------ | --------
202          | No error, call successful.
404          | Asset not found.

### Headers
Header | Value
------ | -----
Authorization | ApiKey info@inspectpos.com:50f69f0..

