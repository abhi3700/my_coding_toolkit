# Curl

## Usage

- `$ curl https://example.com` or `$ curl "https://example.com"`: GET request
- `$ curl -X POST https://example.com`: POST request
- `$ curl --verbose "127.0.0.1:3000"`: verbose mode i.e. shows the request and response headers and body

```sh
❯ curl --verbose "127.0.0.1:3000"
*   Trying 127.0.0.1:3000...
* Connected to 127.0.0.1 (127.0.0.1) port 3000
> GET / HTTP/1.1
> Host: 127.0.0.1:3000
> User-Agent: curl/8.4.0
> Accept: */*
> 
< HTTP/1.1 200 OK
< content-type: text/plain; charset=utf-8
< content-length: 12
< date: Tue, 19 Dec 2023 18:05:38 GMT
< 
* Connection #0 to host 127.0.0.1 left intact
Hello World!% 
```

- `$ curl https://example.com | json_pp`: prettify the JSON output in terminal
