# Flag asset as compromised
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