#User

## User Details
> To get the user details, use this code:

```python
import requests
url = 'https://dev.spotskim.com/api/phone/2_5/accounts/users/1/'
headers = {'Authorization': 'ApiKey user@spotksim.com:204db7bcfafb2deb7506b89eb3b9b715b09905c8'}
response = request.get(url, headers)
```

> The above command returns JSON structured like this (exactly the same as a login call), typically used in a token caching scenario:
 
```json
{
    "asset_types": [
        {
            "description": "A Credit card terminal, also known as a Payment Terminal or EFTPOS Terminal. Terminals allow for swipe, dip, of credit cards. This includes dial-up terminals as well as Multi-Lane terminals, such as the ones connected to Cash Register via a cable.",
            "id": 44,
            "image": "https://spotskim-dev-thumbnails.s3.amazonaws.com/asset_primary_angles/terminal.png?Signature=QCg%2FayL8kLiQ3eNCD%2BwLFqGuYWs%3D&Expires=1431473724&AWSAccessKeyId=AKIAIWXP3QT3ECK4SGFQ",
            "name": "Terminal",
            "order": 0
        },
        {
            "description": "An externally attached card reader, such as the ones on a keyboard, externally mounted to Point-Of-Sale systems, or readers that are plugged in on an as-needed basis to PCs.",
            "id": 45,
            "image": "https://spotskim-dev-thumbnails.s3.amazonaws.com/asset_primary_angles/keyboard.png?Signature=Te%2BxrGFf4ZLrVxejdperxTu%2B214%3D&Expires=1431473724&AWSAccessKeyId=AKIAIWXP3QT3ECK4SGFQ",
            "name": "External Card Reader",
            "order": 1
        },
        {
            "description": "Card processing kiosks such as ones used for ticket vending machines, food kiosks, receipt lookup kiosks, etc.,",
            "id": 46,
            "image": "https://spotskim-dev-thumbnails.s3.amazonaws.com/asset_primary_angles/kiosk.png?Signature=loySLj2u%2F6jEXDP6GgVtEC9FH%2Bw%3D&Expires=1431473724&AWSAccessKeyId=AKIAIWXP3QT3ECK4SGFQ",
            "name": "Kiosk",
            "order": 2
        },
        {
            "description": "Unattended Fuel Dispenser with an integrated card reader.",
            "id": 47,
            "image": "https://spotskim-dev-thumbnails.s3.amazonaws.com/asset_primary_angles/gas_pump.png?Signature=DVPAJsmoXvCHQdi8IKqREyke%2Fn0%3D&Expires=1431473724&AWSAccessKeyId=AKIAIWXP3QT3ECK4SGFQ",
            "name": "Gas Pump",
            "order": 3
        },
        {
            "description": "ATM (Automated Teller Machine) allows customers access basic bank services, such as making deposits and cash withdrawals from remote locations, twenty-four hours a day.",
            "id": 89,
            "image": "https://spotskim-dev-thumbnails.s3.amazonaws.com/asset_primary_angles/atm_final2.png?Signature=TQn851wpoBZ1W0RAcuwp1Q4gad0%3D&Expires=1431473724&AWSAccessKeyId=AKIAIWXP3QT3ECK4SGFQ",
            "name": "ATM",
            "order": 4
        },
        {
            "description": "A Clover POS system terminal. The integrated physical security on the device simplifies the inspection process to one view and question.",
            "id": 68,
            "image": "https://spotskim-dev-thumbnails.s3.amazonaws.com/asset_primary_angles/Screen_Shot_2015-03-02_at_10.53.22_PM.png?Signature=Ly7%2BC0q49NKK9ZXGoP6dxbjZzKk%3D&Expires=1431473724&AWSAccessKeyId=AKIAIWXP3QT3ECK4SGFQ",
            "name": "Clover Terminal",
            "order": 5
        }
    ],
    "current_location": {
        "address_line1": "5413 N Glenwood Ave",
        "asset_count": 31,
        "assets": [
            {
                "asset_type": {
                    "description": "A Clover POS system terminal. The integrated physical security on the device simplifies the inspection process to one view and question.",
                    "id": 68,
                    "image": "https://spotskim-dev-thumbnails.s3.amazonaws.com/asset_primary_angles/Screen_Shot_2015-03-02_at_10.53.22_PM.png?Signature=F70Mxlsgjlkiyu4pA2LhKpb8ZHE%3D&Expires=1431473723&AWSAccessKeyId=AKIAIWXP3QT3ECK4SGFQ",
                    "name": "Clover Terminal",
                    "order": 5
                },
                "device_status": "not_in_use",
                "id": 205,
                "is_compliant": true,
                "is_compromised": false,
                "is_due": false,
                "last_inspected": "2015-03-03T05:16:28",
                "last_inspector": {
                    "id": 33,
                    "name": "Edward Moore",
                    "username": "info@inspectpos.com"
                },
                "risk_rating": "low",
                "sublocation": null,
                "tag": "c010uc40450528",
                "thumbnail": "https://spotskim-dev-images.s3.amazonaws.com/info%40inspectpos.com/2015-03-02-23/c010uc40450528/447052529vvcct.jpg_thumb.jpg?Signature=sNqUN8g3X4VTds5hYfATU2fV%2FCI%3D&Expires=1431473723&AWSAccessKeyId=AKIAIWXP3QT3ECK4SGFQ"
            },
            {
                "asset_type": {
                    "description": "Card processing kiosks such as ones used for ticket vending machines, food kiosks, receipt lookup kiosks, etc.,",
                    "id": 46,
                    "image": "https://spotskim-dev-thumbnails.s3.amazonaws.com/asset_primary_angles/kiosk.png?Signature=eYthX0CnvbIABVRj0Vb9t7taXDE%3D&Expires=1431473723&AWSAccessKeyId=AKIAIWXP3QT3ECK4SGFQ",
                    "name": "Kiosk",
                    "order": 2
                },
                "device_status": "in_use",
                "id": 156,
                "is_compliant": false,
                "is_compromised": false,
                "is_due": true,
                "last_inspected": "2015-04-24T20:41:33",
                "last_inspector": {
                    "id": 52,
                    "name": "Vasu  Nagendra",
                    "username": "vasu@safecard.io"
                },
                "risk_rating": "low",
                "sublocation": {
                    "id": 98,
                    "latitude": 41.96120351235184,
                    "longitude": -87.64905941450937,
                    "name": "lane 12"
                },
                "tag": "QAZ12345",
                "thumbnail": "https://spotskim-dev-images.s3.amazonaws.com/vasu%40safecard.io/2015-02-04-15/nztmltvoyawj/QAZ12345/IMG_142.jpg_thumb.jpg?Signature=SDIDWGcG2eJ8PcJwKyDWqOpadSY%3D&Expires=1431473723&AWSAccessKeyId=AKIAIWXP3QT3ECK4SGFQ"
            }
        ],
        "city": "Chicago",
        "id": 28,
        "latitude": 41.9803581,
        "longitude": -87.6647797,
        "name": "Andersonville",
        "organization": 9,
        "state": "IL",
        "zipcode": "60640"
    },
    "id": 33,
    "name": "Edward Moore",
    "organizations": [
        {
            "has_policy": true,
            "has_training": true,
            "id": 9,
            "name": "Inspectpos"
        }
    ],
    "policy_complete": true,
    "token": "50f69f00f6ae37aa5a0d825de8bbda0956d21a66",
    "training_complete": true,
    "username": "info@inspectpos.com"
}

```

### HTTP Request

`GET http://dev.spotskim.com/api/phone/2_5/accounts/users/1/`

### Query Parameters
None

### Headers
Header | Value
------ | -----
Authorization | ApiKey info@inspectpos.com:50f69f0..

### Notes
1. The response is exactly the same as the login call, however this call is authenticated

### Changes in 2.5
1. Bucket Credentials have been removed. The upload URLS (presigned) are provided as part of the Asset Detail Call
2. Asset Types are now part of the Assets in the Location
3. User's Organization has been added in `organizations`. This is all the Organizations that the user has access to. It is an Array. In 2.5 the system does not support having one user tied to multiple Organizations
4. If the organization that the user is logging into has policy setup, then `has_policy`  will be true. Same for `has_training`


## User History
> To get the user history, use this code:

```python
import requests
url = 'https://dev.spotskim.com/api/phone/2_5/accounts/users/1/history/'
headers = {'Authorization': 'ApiKey user@spotksim.com:204db7bcfafb2deb7506b89eb3b9b715b09905c8'}
response = request.get(url, headers)
```

> The above command returns JSON structured like this:

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
Authorization | ApiKey info@inspectpos.com:50f69f0..

### Notes
1. This returns both Web-Inspection and App-Inspection history for the user. 
2. If the user performed Web-Inspection or didn't upload any pictures as part of their App-Inspection, then `thumbnail` is null


## User Policy
> To get the policy html content, use this code:

```python
import requests
url = 'https://dev.spotskim.com/api/phone/2_5/accounts/users/1/'
headers = {'Authorization': 'ApiKey user@spotksim.com:204db7bcfafb2deb7506b89eb3b9b715b09905c8'}
response = request.get(url, headers)
```
> The above command returns JSON structured like this:

```json
{
    "content":"Policy HTML Content"
}
```

### HTTP Request
`GET https://dev.spotskim.com/api/phone/2_5/accounts/users/1/policy/`

<aside class="success">
Make sure to replace the corresponding user id in the url (.../users/{user_id here}/policy/)
</aside>

### Parameters
None

### Headers
Header | Value
------ | -----
Authorization | ApiKey info@inspectpos.com:50f69f0..

<aside class="warning">
If the authorization value does not match with the user id, the API will return code 401
</aside>


### Notes
1. HTML content sent by the server should be generally safe as we don't allow HTML content on the server (only markdown allowed)


## User Training
> To get training video url, use this code:

```python
import requests
url = 'https://dev.spotskim.com/api/phone/2_5/accounts/users/1/'
headers = {'Authorization': 'ApiKey user@spotksim.com:204db7bcfafb2deb7506b89eb3b9b715b09905c8'}
response = request.get(url, headers)
```

> The above command returns JSON structured like this:

```json
{
    "training_url": "pre_signed_S3_url.mp4"
}
```

### HTTP Request
`GET https://dev.spotskim.com/api/phone/2_5/accounts/users/1/training/`

<aside class="success">
Make sure to replace the corresponding user id in the url (.../users/{user_id here}/training/)
</aside>

### Parameters
None

### Headers
Header | Value
------ | -----
Authorization | ApiKey info@inspectpos.com:50f69f0..

<aside class="warning">
If the authorization value does not match with the user id, the API will return code 401
</aside>

### Notes
1. S3 URL that the server has where the training video is hosted
2. This URL should be valid for 1 hour
3. Subsequent calls to the server, change the expiration of the URL, thus change the URL string that is returned


## Modify User
> To modify the user details, use this code:

```python
import requests
url = 'https://dev.spotskim.com/api/phone/2_5/accounts/users/1/'
headers = {'Authorization': 'ApiKey user@spotksim.com:204db7bcfafb2deb7506b89eb3b9b715b09905c8'}
parameters = {
    "training_complete": "True", 
    "policy_complete": "True", 
    "current_location": "10", 
    "latitude": "37.7262924",
    "longitude": "-89.2281921"
}
response = request.patch(url, parameters, headers)
```
> The above command returns JSON structured like this:
> 

```json
{
    "asset_types": [
        {
            "description": "A Credit card terminal, also known as a Payment Terminal or EFTPOS Terminal. Terminals allow for swipe, dip, of credit cards. This includes dial-up terminals as well as Multi-Lane terminals, such as the ones connected to Cash Register via a cable.",
            "id": 44,
            "image": "https://spotskim-dev-thumbnails.s3.amazonaws.com/asset_primary_angles/terminal.png?Signature=QCg%2FayL8kLiQ3eNCD%2BwLFqGuYWs%3D&Expires=1431473724&AWSAccessKeyId=AKIAIWXP3QT3ECK4SGFQ",
            "name": "Terminal",
            "order": 0
        },
        {
            "description": "An externally attached card reader, such as the ones on a keyboard, externally mounted to Point-Of-Sale systems, or readers that are plugged in on an as-needed basis to PCs.",
            "id": 45,
            "image": "https://spotskim-dev-thumbnails.s3.amazonaws.com/asset_primary_angles/keyboard.png?Signature=Te%2BxrGFf4ZLrVxejdperxTu%2B214%3D&Expires=1431473724&AWSAccessKeyId=AKIAIWXP3QT3ECK4SGFQ",
            "name": "External Card Reader",
            "order": 1
        },
        {
            "description": "Card processing kiosks such as ones used for ticket vending machines, food kiosks, receipt lookup kiosks, etc.,",
            "id": 46,
            "image": "https://spotskim-dev-thumbnails.s3.amazonaws.com/asset_primary_angles/kiosk.png?Signature=loySLj2u%2F6jEXDP6GgVtEC9FH%2Bw%3D&Expires=1431473724&AWSAccessKeyId=AKIAIWXP3QT3ECK4SGFQ",
            "name": "Kiosk",
            "order": 2
        },
        {
            "description": "Unattended Fuel Dispenser with an integrated card reader.",
            "id": 47,
            "image": "https://spotskim-dev-thumbnails.s3.amazonaws.com/asset_primary_angles/gas_pump.png?Signature=DVPAJsmoXvCHQdi8IKqREyke%2Fn0%3D&Expires=1431473724&AWSAccessKeyId=AKIAIWXP3QT3ECK4SGFQ",
            "name": "Gas Pump",
            "order": 3
        },
        {
            "description": "ATM (Automated Teller Machine) allows customers access basic bank services, such as making deposits and cash withdrawals from remote locations, twenty-four hours a day.",
            "id": 89,
            "image": "https://spotskim-dev-thumbnails.s3.amazonaws.com/asset_primary_angles/atm_final2.png?Signature=TQn851wpoBZ1W0RAcuwp1Q4gad0%3D&Expires=1431473724&AWSAccessKeyId=AKIAIWXP3QT3ECK4SGFQ",
            "name": "ATM",
            "order": 4
        },
        {
            "description": "A Clover POS system terminal. The integrated physical security on the device simplifies the inspection process to one view and question.",
            "id": 68,
            "image": "https://spotskim-dev-thumbnails.s3.amazonaws.com/asset_primary_angles/Screen_Shot_2015-03-02_at_10.53.22_PM.png?Signature=Ly7%2BC0q49NKK9ZXGoP6dxbjZzKk%3D&Expires=1431473724&AWSAccessKeyId=AKIAIWXP3QT3ECK4SGFQ",
            "name": "Clover Terminal",
            "order": 5
        }
    ],
    "current_location": {
        "address_line1": "5413 N Glenwood Ave",
        "asset_count": 31,
        "assets": [
            {
                "asset_type": {
                    "description": "A Clover POS system terminal. The integrated physical security on the device simplifies the inspection process to one view and question.",
                    "id": 68,
                    "image": "https://spotskim-dev-thumbnails.s3.amazonaws.com/asset_primary_angles/Screen_Shot_2015-03-02_at_10.53.22_PM.png?Signature=F70Mxlsgjlkiyu4pA2LhKpb8ZHE%3D&Expires=1431473723&AWSAccessKeyId=AKIAIWXP3QT3ECK4SGFQ",
                    "name": "Clover Terminal",
                    "order": 5
                },
                "device_status": "not_in_use",
                "id": 205,
                "is_compliant": true,
                "is_compromised": false,
                "is_due": false,
                "last_inspected": "2015-03-03T05:16:28",
                "last_inspector": {
                    "id": 33,
                    "name": "Edward Moore",
                    "username": "info@inspectpos.com"
                },
                "risk_rating": "low",
                "sublocation": null,
                "tag": "c010uc40450528",
                "thumbnail": "https://spotskim-dev-images.s3.amazonaws.com/info%40inspectpos.com/2015-03-02-23/c010uc40450528/447052529vvcct.jpg_thumb.jpg?Signature=sNqUN8g3X4VTds5hYfATU2fV%2FCI%3D&Expires=1431473723&AWSAccessKeyId=AKIAIWXP3QT3ECK4SGFQ"
            },
            {
                "asset_type": {
                    "description": "Card processing kiosks such as ones used for ticket vending machines, food kiosks, receipt lookup kiosks, etc.,",
                    "id": 46,
                    "image": "https://spotskim-dev-thumbnails.s3.amazonaws.com/asset_primary_angles/kiosk.png?Signature=eYthX0CnvbIABVRj0Vb9t7taXDE%3D&Expires=1431473723&AWSAccessKeyId=AKIAIWXP3QT3ECK4SGFQ",
                    "name": "Kiosk",
                    "order": 2
                },
                "device_status": "in_use",
                "id": 156,
                "is_compliant": false,
                "is_compromised": false,
                "is_due": true,
                "last_inspected": "2015-04-24T20:41:33",
                "last_inspector": {
                    "id": 52,
                    "name": "Vasu  Nagendra",
                    "username": "vasu@safecard.io"
                },
                "risk_rating": "low",
                "sublocation": {
                    "id": 98,
                    "latitude": 41.96120351235184,
                    "longitude": -87.64905941450937,
                    "name": "lane 12"
                },
                "tag": "QAZ12345",
                "thumbnail": "https://spotskim-dev-images.s3.amazonaws.com/vasu%40safecard.io/2015-02-04-15/nztmltvoyawj/QAZ12345/IMG_142.jpg_thumb.jpg?Signature=SDIDWGcG2eJ8PcJwKyDWqOpadSY%3D&Expires=1431473723&AWSAccessKeyId=AKIAIWXP3QT3ECK4SGFQ"
            }
        ],
        "city": "Chicago",
        "id": 28,
        "latitude": 41.9803581,
        "longitude": -87.6647797,
        "name": "Andersonville",
        "organization": 9,
        "state": "IL",
        "zipcode": "60640"
    },
    "id": 33,
    "name": "Edward Moore",
    "organizations": [
        {
            "has_policy": true,
            "has_training": true,
            "id": 9,
            "name": "Inspectpos"
        }
    ],
    "policy_complete": true,
    "token": "50f69f00f6ae37aa5a0d825de8bbda0956d21a66",
    "training_complete": true,
    "username": "info@inspectpos.com"
}

```

### HTTP Request
`PATCH https://dev.spotskim.com/api/phone/2_5/accounts/users/1/`

### Parameters
Parameter | Required | Description
--------- | -------- | -----------
training_complete | No | modifies the user to now have the required training marked as complete. Has no effect if the organization does not have training enabled 
policy_complete | No | same as above, for policy
current_location | No | Unique ID of the location that is part of the organization. 
latitude | No | When present, longitude must also be present
longitude | No | When present, longitude must also be present

#### Notes
1. If the current_location is not part of the organization, the error code is 402
2. You don't have to specify user's current location directly. Providing a latitude/longitude combination (valid) will change the user's current location to the closest location to that latitude/longitude
3. If you send both latitude/longitude, and current_location; current location takes precedence 
4. If you'd like to refresh user's training/policy status, you can pass in False and make the user take the training again 

### Return Values
Return Value | Meaning 
------------ | --------
202          | No error, call successful
401          | `current_location` not part of the user's organization

### Headers
Header | Value
------ | -----
Authorization | ApiKey info@inspectpos.com:50f69f0..
<aside class="warning">
If the authorization value does not match with the user id, the API will return code 401
</aside>