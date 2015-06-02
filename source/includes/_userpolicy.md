# Get User Policy
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
