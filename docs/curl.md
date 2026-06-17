# cURL

**Usage: curl [options...] {url}**  

## Flags  

- **-X**:  Specifies the HTTP method (GET, POST, PUT, DELETE).
- **-H**:  Adds a custom header to the request
- **-o**:  Writes the output to a specific file. -O to save the original filename.
- **-i**:  Includes the headers in the saved response, -I only includes the headers
- **-L**:  Follow redirects
- **-f**:  fail fast
- **-v**:  verbose mode
- **-s**:  Silent mode, -S to atleast show errors
- **-#**:  For Progress bar  
- **-b**: Specify a filename that contains cookies to be sent to the url
- **-c**: Specify a filename to save the incoming cookies from the url

- **-d**:  Sends data in a POST request. (in the body section)
- **-u**:  Provides credentials for basic authentication (user:password).
- **-k**:  Allows "insecure" SSL connections (handy for local testing).
- **-C -**: continue from where a previous download stopped
- **-F**: Tell curl to upload a file. -F "profile_pic=@file.jpg"
- **--connect-timeout**: Specify the number of seconds to wait for connection before cancelling
- **-m**: Specify the max number of seconds the connection will persist before terminating
- **--http**: Specify http version. --http1.0, --http1.1, --http2, --http3
- **-A**: Pretend to be browser. -A "Mozilla/5.0 (Windows NT 10.0; Win64; x64) Chrome/120.0.0.0"
- **-e**: Fake a referrer. -e "://google.com" ://example.com/secret-file Sends: Referer: ://google.com header
- **-x**: Specify a proxy. It will request the proxy instead of the actual target and the proxy is supposed to forward the request at an application layer level
