### Where  to look for web-cache poisioning
Look the response header of request.If there is any header like
#### Cache-Control: max-age=35
#### Age: 7
#### X-Cache: hit
then this request can be vulnerable.
### How find endpoints
Use param miner extension to look for any header that can be inject into the request.If found than add the header into  the request and look carefully where the
header value is reflected.Than manipulate the header value with malicious payloads as required.
### Note
Use Cache-bluster not to harm other users.
