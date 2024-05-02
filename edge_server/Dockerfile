FROM alpine:latest
LABEL org.opencontainers.image.authors="Luis M. Barrera"
LABEL org.opencontainers.image.source="https://github.com/lubauss/container-fundamentals"
LABEL org.opencontainers.image.description="Container Fundamentals - Static Website Image on Alpine"
LABEL org.opencontainers.image.licenses="APACHE2"
LABEL server_type="edge_server"

RUN apk add --no-cache nginx
RUN mkdir -p /run/nginx

COPY config/nginx.conf /etc/nginx/nginx.conf
COPY web_content/ /var/www/html

EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
