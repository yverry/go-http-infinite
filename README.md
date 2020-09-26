# Go HTTP Infinite

This project was created to generate an infinite file with "0"

# Usage

This program open an http server on port 8090 and generate the file on any path

## Nginx

Just `proxy_pass` as usual:

```nginx
server {
    location /infinite.file {
        proxy_ignore_client_abort off;
        proxy_pass http://go-http-infinite:8090;
    }
}
```