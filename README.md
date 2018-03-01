# nginx-proxy-resolver-example
Example implementation of Nginx reverse proxy with DNS resolver inside Docker with multiple locations and multiple backends. Configuration will work with any DNS CNAME/ALIAS records like AWS ELB/ALB endpoints.
This example shows rewrites from hypothetical API /v1 endpoints to /v2 in backend2 and /v3 endpoint to /v4 on backend1.
Please see *default.conf* Nginx configuration for details.

# Usage

```
docker-compose build
docker-compose up -d
```

In Browser navigate to
 - http://localhost Navigates to sitea
 - http://localhost/v1/ Navigates to siteb /v2
 - http://localhost/v3/ Navigates to sitea /v4
