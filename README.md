nginx version: nginx/1.24.0


- Set Error custom page:

  - On: conf.d/[domain] -> check on conf.d.history
  - On: nginx.conf -> check on nginx.conf.history
  - Add new page error path: nginx_error.conf
    ```
    error_page  403  /403.html;
    location = /403.html{
    }

    error_page  404  /404.html;
    location = /404.html{
    }

    error_page  500  /500.html;
    location = /500.html{
    }

    error_page  502  /502.html;
    location = /502.html{
    }
    ```
- Disable nginx timeout

  - Set on: nginx.conf -> check on nginx.conf.history
