# Curl

## Usage

- `$ curl https://example.com` or `$ curl "https://example.com"`: GET request
- `$ curl http://example.com --verbose -w "\nTotal time: %{time_total}s\n"`: GET request with time taken to complete the request
- `$ curl -X POST https://example.com`: POST request
- `$ curl --verbose "127.0.0.1:3000"`: verbose mode i.e. shows the request and response headers and body

> Just use `-v` instead of `--verbose`.

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

- `$ curl https://example.com | json_pp`: prettify the JSON output in terminal. Also, it shows the download, upload and total bytes transferred.

```sh
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100    61  100    33  100    28  45205  38356 --:--:-- --:--:-- --:--:-- 61000
{
   "id" : 1337,
   "username" : "abhi3700"
}
```

- Post request with JSON body in 2 ways:
  - `$ curl localhost:3000/users -X POST -H "Content-Type: application/json" -d '{"username":"abhi3700"}' | json_pp`, where `body.json` is defined at current directory. `{"username":"abhi3700"}`
  - `$ curl localhost:3000/users -X POST -H "Content-Type: application/json" -d @body.json | json_pp`, where `body.json` is defined at current directory. `body.json` is really helpful in cases where JSON content is very big and might look clumsy to write in terminal.
