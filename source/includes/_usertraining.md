# Get User Training
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


