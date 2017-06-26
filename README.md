If we certify this API for public consumption, with parameters q, limit & api_key?


/*200 OK
400 	Bad Request. Method request is incorrectly formatted.
401 	Unauthorized. Authentication failed.
404 	Method Not Allowed. Request contains an HTTP method type that is not supported for that API function.*/



-->The Certify API uses standard RESTful API calls via HTTP web requests with methods like GET, POST, and DELETE. All calls must be made using HTTPS.
-->The Certify API accepts requests and returns responses in either JSON or XML. Please set the Content-Type header to either “application/json” or “application/xml” in the requests to define which format you would like. The default format is JSON.
-->All API calls to the Certify API must include authentication information to verify the identity of the caller. Authentication is comprised of two tokens called the API Key and the API Secret. 
-->The API Key is a hashed code for your company; it tells us who you are. The API Secret is a generated token that grants you access to your Certify data. Both tokens can be found in the Configuration section of your company’s administrator users inside Certify. 
-->These tokens should NOT be freely given out, they should only be given to parties trusted with access to your company’s data.
-->Successful responses returned from the Certify API will be formatted according to the specific API method.


Request without paramters:-

GET /planetary/sounds HTTP/1.1

GData-Version:
    1.4
Host:
    api.nasa.gov
X-Target-URI:
    https://api.nasa.gov
Connection:
    Keep-Alive

-------------------------------------------------------------------------------------------------------------------------------
Response without parameters:-

HTTP/1.1 403 Forbidden

Strict-Transport-Security:
    max-age=31536000
Vary:
    Accept-Encoding
Access-Control-Allow-Origin:
    *
Date:
    Mon, 26 Jun 2017 15:21:12 GMT
Content-Length:
    125
Connection:
    keep-alive
Content-Type:
    application/json
X-Cache:
    MISS
Server:
    openresty


{
  "error": {
    "code": "API_KEY_MISSING",
    "message": "No api_key was supplied. Get one at https://api.nasa.gov"
  }
}

----------------------------------------------------------------------------------------------------

Request with parameters:-

GET /planetary/sounds?q=nasa&max-results=10&api_key=DEMO_KEY HTTP/1.1

GData-Version:
    1.4
Host:
    api.nasa.gov
X-Target-URI:
    https://api.nasa.gov
Connection:
    Keep-Alive

-----------------------------------------------------------------------------------------------------------------------------
Response with parameters:-


HTTP/1.1 200 OK
Age:
    0
X-RateLimit-Remaining:
    33
X-RateLimit-Limit:
    40
Content-Length:
    3535
Connection:
    keep-alive
Server:
    openresty
X-Cache:
    MISS
Cache-Control:
    no-cache
X-Cloud-Trace-Context:
    744897c68fbf000dfe401c599c254aad;o=1
Strict-Transport-Security:
    max-age=31536000
Date:
    Mon, 26 Jun 2017 15:17:00 GMT
Vary:
    Accept-Encoding
Vary:
    Accept-Encoding
Via:
    http/1.1 api-umbrella (ApacheTrafficServer [cMsSf ])
Content-Type:
    application/json


{"count": 10, "results": [{"description": "The Voyager 1 spacecraft has experienced three \"tsunami waves\" in interstellar space. Listen to how these waves cause surrounding ionized matter to ring. More details on this sound can be found here: http://www.nasa.gov/jpl/nasa-voyager-tsunami-wave-still-flies-through-interstellar-space/", "license": "cc-by-nc-sa", "title": "Voyager 1: Three \"Tsunami Waves\" in Interstellar Space", "download_url": "https://api.soundcloud.com/tracks/181835738/download", "duration": 18365, "last_modified": "2014/12/16 22:34:23 +0000", "stream_url": "https://api.soundcloud.com/tracks/181835738/stream", "tag_list": "Space", "id": 181835738}, {"description": "Courtesy of United Launch Alliance", "license": "cc-by-nc", "title": "Delta IV: Launch", "download_url": "https://api.soundcloud.com/tracks/173578614/download", "duration": 30095, "last_modified": "2014/10/24 02:16:33 +0000", "stream_url": "https://api.soundcloud.com/tracks/173578614/stream", "tag_list": "space", "id": 173578614}, {"description": null, "license": "cc-by-nc", "title": "Wheel Stop", "download_url": "https://api.soundcloud.com/tracks/172463130/download", "duration": 5903, "last_modified": "2014/10/16 19:29:13 +0000", "stream_url": "https://api.soundcloud.com/tracks/172463130/stream", "tag_list": "space", "id": 172463130}, {"description": null, "license": "cc-by-nc", "title": "Vector Transfer", "download_url": "https://api.soundcloud.com/tracks/172463129/download", "duration": 3760, "last_modified": "2014/10/16 19:29:12 +0000", "stream_url": "https://api.soundcloud.com/tracks/172463129/stream", "tag_list": "space", "id": 172463129}, {"description": null, "license": "cc-by-nc", "title": "Roger Roll", "download_url": "https://api.soundcloud.com/tracks/172463128/download", "duration": 1515, "last_modified": "2014/10/16 19:29:12 +0000", "stream_url": "https://api.soundcloud.com/tracks/172463128/stream", "tag_list": "space", "id": 172463128}, {"description": null, "license": "cc-by-nc", "title": "On its way to Orbit", "download_url": "https://api.soundcloud.com/tracks/172463126/download", "duration": 7497, "last_modified": "2014/10/16 19:29:12 +0000", "stream_url": "https://api.soundcloud.com/tracks/172463126/stream", "tag_list": "space", "id": 172463126}, {"description": null, "license": "cc-by-nc", "title": "Press to ATO", "download_url": "https://api.soundcloud.com/tracks/172463124/download", "duration": 2560, "last_modified": "2014/10/16 19:29:12 +0000", "stream_url": "https://api.soundcloud.com/tracks/172463124/stream", "tag_list": "space", "id": 172463124}, {"description": null, "license": "cc-by-nc", "title": "Nice to be in Orbit", "download_url": "https://api.soundcloud.com/tracks/172463122/download", "duration": 5641, "last_modified": "2014/10/16 19:29:11 +0000", "stream_url": "https://api.soundcloud.com/tracks/172463122/stream", "tag_list": "space", "id": 172463122}, {"description": null, "license": "cc-by-nc", "title": "MECO", "download_url": "https://api.soundcloud.com/tracks/172463117/download", "duration": 3187, "last_modified": "2014/10/16 19:29:11 +0000", "stream_url": "https://api.soundcloud.com/tracks/172463117/stream", "tag_list": "space", "id": 172463117}, {"description": null, "license": "cc-by-nc", "title": "Lookin At It", "download_url": "https://api.soundcloud.com/tracks/172463116/download", "duration": 2429, "last_modified": "2014/10/16 19:29:10 +0000", "stream_url": "https://api.soundcloud.com/tracks/172463116/stream", "tag_list": "space", "id": 172463116}]}



