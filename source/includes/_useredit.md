# Modify User
```python
import requests
url = 'https://dev.spotskim.com/api/phone/2_5/accounts/users/1/'
headers = {'Authorization': '204db7bcfafb2deb7506b89eb3b9b715b09905c8'}
parameters = {
    "training_complete": "True", 
    "policy_complete": "True", 
    "current_location": "10", 
    "latitude": "37.7262924",
    "longitude": "-89.2281921"
}
response = request.patch(url, parameters, headers)
```
> The above command returns JSON structured like this 
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

### HTTP Method
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
authorization | ApiKey info@inspectpos.com:50f69f0..
