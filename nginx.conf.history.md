# Workspace: ./nginx.conf

## Disable Timeouts
- Set on: `http {...}`
  ```
# Disable common NGINX Timeouts
        keepalive_timeout 1d;
        send_timeout 1d;
        client_body_timeout 1d;
        client_header_timeout 1d;
        proxy_connect_timeout 1d;
        proxy_read_timeout 1d;
        proxy_send_timeout 1d;
        fastcgi_connect_timeout 1d;
        fastcgi_read_timeout 1d;
        fastcgi_send_timeout 1d;
        memcached_connect_timeout 1d;
        memcached_read_timeout 1d;
        memcached_send_timeout 1d;
  ```