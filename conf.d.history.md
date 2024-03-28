# Workspace: ./conf.d/[domain].conf

Use for websocket on my domain nexlelive-stream.[mycompanydomain.com]

- certbot use key-size 2048

```
certbot --nginx certonly --rsa-key-size 2048 -d nexlelive-stream.demo.nexlesoft.com
```

- add new line on `location / {...}`

```
#allow websocket ws, wss
                proxy_http_version 1.1;
                proxy_set_header Connection "upgrade";
                proxy_set_header Upgrade $http_upgrade;
```

- Set custom error page on `location / {...}`

```
        include /etc/nginx/nginx_error.conf;
```
