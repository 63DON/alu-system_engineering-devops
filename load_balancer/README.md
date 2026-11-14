# Load balancer

Scripts that add redundancy to the web stack: two Nginx web servers
(web-01 and web-02) behind an HAProxy load balancer (lb-01).

| File | Description |
|------|-------------|
| `0-custom_http_response_header` | Configures Nginx with an `X-Served-By` header set to the server's hostname |
| `1-install_load_balancer` | Installs HAProxy on lb-01, sending traffic to web-01 and web-02 with roundrobin |
