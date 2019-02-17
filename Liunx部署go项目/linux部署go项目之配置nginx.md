#### linux部署go项目之配置nginx

1.配置nginx.conf

```nginx
 server{
        listen 80;
        server_name www.a.com a.com;
        location /{
            try_files /_not_exists @backend;
         }

         location @backend{
               proxy_set_header X-Forwarded-For $remote_addr;
               proxy_set_header Host            $http_host;
               proxy_pass  http://localhost:8080;
         }
    }
```

