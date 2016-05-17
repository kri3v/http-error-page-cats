# http-error-page-cats
Custom error pages with funny cat images taken from https://http.cat/
## How to use:
### Nginx
Upload html and jpg files and configure like this on your server block:
```
	error_page 404 /error/404.html;
	error_page 500 /error/500.html;
	error_page 502 /error/502.html;
	error_page 503 /error/503.html;

	location ^~ /error/(404|500|502|503).html {
	   internal;
	   alias /usr/share/nginx/html;
       }
```
### Apache
