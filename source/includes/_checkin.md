# Inspection Check in
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