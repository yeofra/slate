# Get User Policy
```python
import requests
url = 'https://dev.spotskim.com/api/phone/2_5/accounts/users/1/'
headers = {'Authorization': '204db7bcfafb2deb7506b89eb3b9b715b09905c8'}
response = request.get(url, headers)
```
> The above command returns JSON structured like this 

```json
{
    "content": "Policy HTML Content"
}

```

### HTTP Method
`GET https://dev.spotskim.com/api/phone/2_1/accounts/users/1/policy/`

### Parameters
None

### Notes
1. HTML content sent by the server should be generally safe as we don't allow HTML content on the server (only markdown allowed)
