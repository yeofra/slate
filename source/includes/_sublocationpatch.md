# Sublocation Patch
> To patch the sublocation coordinates, use this code:

```python
import requests
url = 'https://dev.spotskim.com/api/phone/2_5/locations/50/sublocation/178/'
headers = {'Authorization': 'ApiKey user@spotksim.com:204db7bcfafb2deb7506b89eb3b9b715b09905c8'}
parameters = {
  "latitude": 41.8921805,
  "longitude": -87.62416
}
response = request.patch(url, parameters, headers)
```

> The above command returns JSON structured like this:

```json
{
  "id": 178,
  "latitude": 41.8921805,
  "longitude": -87.62416,
  "name": "lane 5"
}
```

### HTTP Request
`PATCH https://dev.spotskim.com/api/phone/2_5/locations/50/sublocation/178/`

<aside class="success">
Make sure to replace the corresponding parameters in the url (.../locations/{location_id here}/sublocation/{sublocation_id here}/)
</aside>


### Query Parameters
Parameter | Required | Description
--------- | -------- | -----------
latitude | No | The latitude to set on this sub-location.
longitude | No | See latitude

### Return Values
Return Value | Meaning
------------ | --------
202          | No error, call successful.
404          | Sublocation not found.

### Note
1. `latitude` and `longitude` CANNOT be `null`.
2. At least one of the two parameters has to be in the body.

### Headers
Header | Value
------ | -----
Authorization | ApiKey info@inspectpos.com:50f69f0..
