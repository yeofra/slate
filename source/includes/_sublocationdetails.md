# Sublocation Details
> To get the sublocation details, use this code:

```python
import requests
url = 'https://dev.spotskim.com/api/phone/2_5/locations/50/sublocation/178/'
headers = {'Authorization': 'ApiKey user@spotksim.com:204db7bcfafb2deb7506b89eb3b9b715b09905c8'}
response = request.get(url, headers)
```

> The above command returns JSON structured like this (same object as "sublocation" in Asset Details request):

```json
{
  "id": 178,
  "latitude": 41.8921805,
  "longitude": -87.62416,
  "name": "lane 5"
}
```

### HTTP Request
`GET https://dev.spotskim.com/api/phone/2_5/locations/50/sublocation/178/`

<aside class="success">
Make sure to replace the corresponding parameters in the url (.../locations/{location_id here}/sublocation/{sublocation_id here}/)
</aside>


### Query Parameters
None

### Return Values
Return Value | Meaning
------------ | --------
200          | No error, call successful.
404          | Sublocation not found.

### Note
1. `latitude` and `longitude` can be `null`.

### Headers
Header | Value
------ | -----
Authorization | ApiKey info@inspectpos.com:50f69f0..
