# User History
```python
import requests
url = 'https://dev.spotskim.com/api/phone/2_5/accounts/users/1/history/'
headers = {'Authorization': '204db7bcfafb2deb7506b89eb3b9b715b09905c8'}
response = request.get(url, headers)
```

> The above command returns JSON structured like this 

```json
[
    {
        "asset_tag": "00124E16A6BD",
        "checkin_thumbnail": "https://spotskim-dev-images.s3.amazonaws.com/info%40inspectpos.com/2015-05-12-09/00124E16A6BD/453133038jdwkl.jpg_thumb.jpg?Signature=w7KzhcG7ojFPGRp53AFlvg7nh%2Bk%3D&Expires=1431474805&AWSAccessKeyId=AKIAIWXP3QT3ECK4SGFQ",
        "current_device_status": "in_use",
        "datetime_inspected": "2015-05-12T14:18:41",
        "id": 906
    },
    {
        "asset_tag": "jsatm22",
        "checkin_thumbnail": "https://spotskim-dev-images.s3.amazonaws.com/info%40inspectpos.com/2015-05-12-08/jsatm22/453130024uprht.jpg_thumb.jpg?Signature=OXDu6aJdcn8YvXAK9fwY8zdKHho%3D&Expires=1431474805&AWSAccessKeyId=AKIAIWXP3QT3ECK4SGFQ",
        "current_device_status": "in_use",
        "datetime_inspected": "2015-05-12T13:28:05",
        "id": 905
    },
    {
        "asset_tag": "0123456d",
        "checkin_thumbnail": null,
        "current_device_status": "not_in_use",
        "datetime_inspected": "2015-04-22T00:43:05",
        "id": 820
    },
    {
        "asset_tag": "012345678",
        "checkin_thumbnail": null,
        "current_device_status": "in_use",
        "datetime_inspected": "2015-04-21T15:46:12",
        "id": 814
    },
    {
        "asset_tag": "00124E16A6BD",
        "checkin_thumbnail": "https://spotskim-dev-images.s3.amazonaws.com/info%40inspectpos.com/2015-04-16-13/00124E16A6BD/450903140vumvd.jpg_thumb.jpg?Signature=iLSr7bxe%2Fgc4DF2aHzM6dm%2BFZkY%3D&Expires=1431474805&AWSAccessKeyId=AKIAIWXP3QT3ECK4SGFQ",
        "current_device_status": "in_use",
        "datetime_inspected": "2015-04-16T18:52:28",
        "id": 777
    }
]
```

### HTTP Request
`GET https://dev.spotskim.com/2_5/accounts/users/33/history/`

### Query Parameters
None

### Headers
Header | Value
------ | -----
authorization | ApiKey info@inspectpos.com:50f69f0..

### Notes
1. This returns both Web-Inspection and App-Inspection history for the user. 
2. If the user performed Web-Inspection or didn't upload any pictures as part of their App-Inspection, then `thumbnail` is null
