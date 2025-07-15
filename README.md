# k8s_ingress2
# Настройка по аналогии как в k8s_ingress

allower@MacBookAir k8s_for_yandex % curl -v https://allower.online/app2/
* Host allower.online:443 was resolved.
* IPv6: (none)
* IPv4: 51.250.47.179
*   Trying 51.250.47.179:443...
* Connected to allower.online (51.250.47.179) port 443
* ALPN: curl offers h2,http/1.1
* (304) (OUT), TLS handshake, Client hello (1):
*  CAfile: /etc/ssl/cert.pem
*  CApath: none
* (304) (IN), TLS handshake, Server hello (2):
* (304) (IN), TLS handshake, Unknown (8):
* (304) (IN), TLS handshake, Certificate (11):
* (304) (IN), TLS handshake, CERT verify (15):
* (304) (IN), TLS handshake, Finished (20):
* (304) (OUT), TLS handshake, Finished (20):
* SSL connection using TLSv1.3 / AEAD-CHACHA20-POLY1305-SHA256 / [blank] / UNDEF
* ALPN: server accepted h2
* Server certificate:
*  subject: CN=allower.online
*  start date: Jul 13 19:39:17 2025 GMT
*  expire date: Oct 11 19:39:16 2025 GMT
*  subjectAltName: host "allower.online" matched cert's "allower.online"
*  issuer: C=US; O=Let's Encrypt; CN=R11
*  SSL certificate verify ok.
* using HTTP/2
* [HTTP/2] [1] OPENED stream for https://allower.online/app2/
* [HTTP/2] [1] [:method: GET]
* [HTTP/2] [1] [:scheme: https]
* [HTTP/2] [1] [:authority: allower.online]
* [HTTP/2] [1] [:path: /app2/]
* [HTTP/2] [1] [user-agent: curl/8.7.1]
* [HTTP/2] [1] [accept: */*]
> GET /app2/ HTTP/2
> Host: allower.online
> User-Agent: curl/8.7.1
> Accept: */*
> 
* Request completely sent off
< HTTP/2 200 
< server: ycalb
< date: Tue, 15 Jul 2025 01:41:47 GMT
< content-type: text/html,text/html
< 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Welcome to Nginx</title>
</head>
<body>
    <h1>Welcome to Nginx!</h1>
    <p>If you see this page, the Nginx web server is successfully configured.</p>
    <p>Learn more about deploying and managing applications with Kubernetes in our comprehensive Kubernetes course.</p>
    <p>THIS IS APP-2! Pod Name: alb-demo-2-665fcb5f48-b626f</p>
</body>
</html>
* Connection #0 to host allower.online left intact
allower@MacBookAir k8s_for_yandex % curl -v https://allower.online/app1/
* Host allower.online:443 was resolved.
* IPv6: (none)
* IPv4: 51.250.47.179
*   Trying 51.250.47.179:443...
* Connected to allower.online (51.250.47.179) port 443
* ALPN: curl offers h2,http/1.1
* (304) (OUT), TLS handshake, Client hello (1):
*  CAfile: /etc/ssl/cert.pem
*  CApath: none
* (304) (IN), TLS handshake, Server hello (2):
* (304) (IN), TLS handshake, Unknown (8):
* (304) (IN), TLS handshake, Certificate (11):
* (304) (IN), TLS handshake, CERT verify (15):
* (304) (IN), TLS handshake, Finished (20):
* (304) (OUT), TLS handshake, Finished (20):
* SSL connection using TLSv1.3 / AEAD-CHACHA20-POLY1305-SHA256 / [blank] / UNDEF
* ALPN: server accepted h2
* Server certificate:
*  subject: CN=allower.online
*  start date: Jul 13 19:39:17 2025 GMT
*  expire date: Oct 11 19:39:16 2025 GMT
*  subjectAltName: host "allower.online" matched cert's "allower.online"
*  issuer: C=US; O=Let's Encrypt; CN=R11
*  SSL certificate verify ok.
* using HTTP/2
* [HTTP/2] [1] OPENED stream for https://allower.online/app1/
* [HTTP/2] [1] [:method: GET]
* [HTTP/2] [1] [:scheme: https]
* [HTTP/2] [1] [:authority: allower.online]
* [HTTP/2] [1] [:path: /app1/]
* [HTTP/2] [1] [user-agent: curl/8.7.1]
* [HTTP/2] [1] [accept: */*]
> GET /app1/ HTTP/2
> Host: allower.online
> User-Agent: curl/8.7.1
> Accept: */*
> 
* Request completely sent off
< HTTP/2 200 
< server: ycalb
< date: Tue, 15 Jul 2025 01:41:54 GMT
< content-type: text/html,text/html
< 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Welcome to Nginx</title>
</head>
<body>
    <h1>Welcome to Nginx!</h1>
    <p>If you see this page, the Nginx web server is successfully configured.</p>
    <p>Learn more about deploying and managing applications with Kubernetes in our comprehensive Kubernetes course.</p>
    <p>THIS IS APP-1! Pod Name: alb-demo-1-5fdcc9b7bd-9s67z</p>
</body>
</html>
* Connection #0 to host allower.online left intact
allower@MacBookAir k8s_for_yandex % curl -v https://allower.online/     
* Host allower.online:443 was resolved.
* IPv6: (none)
* IPv4: 51.250.47.179
*   Trying 51.250.47.179:443...
* Connected to allower.online (51.250.47.179) port 443
* ALPN: curl offers h2,http/1.1
* (304) (OUT), TLS handshake, Client hello (1):
*  CAfile: /etc/ssl/cert.pem
*  CApath: none
* (304) (IN), TLS handshake, Server hello (2):
* (304) (IN), TLS handshake, Unknown (8):
* (304) (IN), TLS handshake, Certificate (11):
* (304) (IN), TLS handshake, CERT verify (15):
* (304) (IN), TLS handshake, Finished (20):
* (304) (OUT), TLS handshake, Finished (20):
* SSL connection using TLSv1.3 / AEAD-CHACHA20-POLY1305-SHA256 / [blank] / UNDEF
* ALPN: server accepted h2
* Server certificate:
*  subject: CN=allower.online
*  start date: Jul 13 19:39:17 2025 GMT
*  expire date: Oct 11 19:39:16 2025 GMT
*  subjectAltName: host "allower.online" matched cert's "allower.online"
*  issuer: C=US; O=Let's Encrypt; CN=R11
*  SSL certificate verify ok.
* using HTTP/2
* [HTTP/2] [1] OPENED stream for https://allower.online/
* [HTTP/2] [1] [:method: GET]
* [HTTP/2] [1] [:scheme: https]
* [HTTP/2] [1] [:authority: allower.online]
* [HTTP/2] [1] [:path: /]
* [HTTP/2] [1] [user-agent: curl/8.7.1]
* [HTTP/2] [1] [accept: */*]
> GET / HTTP/2
> Host: allower.online
> User-Agent: curl/8.7.1
> Accept: */*
> 
* Request completely sent off
< HTTP/2 200 
< server: ycalb
< date: Tue, 15 Jul 2025 01:41:57 GMT
< content-type: application/octet-stream,text/plain
< content-length: 22
< 
Add app# to URL path 
* Connection #0 to host allower.online left intact
allower@MacBookAir k8s_for_yandex %  
я могу что-то тут спалить, если в гит закину?
