## Nginx exporter requirements

Expose the built-in metrics in NGINX/NGINX Plus

```
...

http {
    ...

    include /etc/nginx/conf.d/*.conf;

    server {
        listen 0.0.0.0:9300;
        location /status {
            stub_status;
            allow all;
        }
    }
}

```

Restart nginx after config

## Trafik exporter requirements

Expose metrics on port 9400

Add option to run command
```
"--metrics.prometheus=true"
```

port mapping:
```
"<internal_ip>:9400:8080"
```