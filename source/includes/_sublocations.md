# Get sublocations
> To get the sublocations of a specific location, use this code:

```python
import requests
url = 'https://dev.spotskim.com/api/phone/2_5/locations/50/sublocation/'
headers = {'Authorization': 'ApiKey user@spotksim.com:204db7bcfafb2deb7506b89eb3b9b715b09905c8'}
response = request.get(url, headers)
```

> The above command returns JSON structured like this:

```json
{
  "meta": {
    "limit": 20,
    "next": null,
    "offset": 0,
    "previous": null,
    "total_count": 3
  },
  "objects": [
    {
      "id": 135,
      "latitude": 42.0042953,
      "longitude": -87.6626017,
      "name": "lane 1"
    },
    {
      "id": 198,
      "latitude": 42.0042566,
      "longitude": -87.6625714,
      "name": "lane 8a"
    },
    {
      "id": 206,
      "latitude": 42.00431710709071,
      "longitude": -87.66261517311584,
      "name": "lane 10"
    }
  ]
}
```

### HTTP Request
`GET https://dev.spotskim.com/api/phone/2_5/locations/50/sublocation/`

<aside class="success">
Make sure to replace the corresponding parameter in the url (.../locations/{location_id here}/sublocation/)
</aside>

### Query Parameters
None

### Return Values
Return Value | Meaning
------------ | --------
200          | No error, call successful.

### Headers
Header | Value
------ | -----
Authorization | ApiKey info@inspectpos.com:50f69f0..
