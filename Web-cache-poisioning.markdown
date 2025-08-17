### Where  to look for web-cache poisioning
Look the response header of request.If there is any header like
##### Cache-Control: max-age=35
##### Age: 7
##### X-Cache: hit
then this request can be vulnerable.
### How find endpoints
Use param miner extension to look for any header that can be injected into the request.If found then add the header into  the request and look carefully where the
header value is reflected.Then manipulate the header value with malicious payloads as required.
### Note
Use Cache-bluster not to harm other users
### Termology
##### cache-key 
This is the header value or query parameter value which is stored in cache server and if any users send the same request which match with that key the cached response is send.
##### uncache-key
This can be header value of query parameter which value is not store in cache.We use it  to check if the cache key is stored or not.
##### cache-bluster
It is extra parameter that is used to make the request unique.This is used for safety purposes as it makes the request unique so no other user
won't visit that specific endpoints so they will not affected.
