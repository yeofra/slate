# Request maintenance for Asset
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