# Errors


SpotSkim API uses the following error codes:


Error Code | Meaning
---------- | -------
400 | Bad Request 
401 | Unauthorized -- Your API key is wrong, or userID/password is wrong
403 | Forbidden -- The resource requested is hidden for administrators only
404 | Not Found -- The specified Asset/Location could not be found
405 | Method Not Allowed -- You tried to access a resource with an invalid method
406 | Not Acceptable -- You requested a format that isn't json
500 | Internal Server Error -- We had a problem with our server. Try again later.
503 | Service Unavailable -- We're temporarially offline for maintanance. Please try again later.
