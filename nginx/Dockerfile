FROM nginx:1.23.4-alpine as nginx

WORKDIR /var/www/html/

RUN apk add --no-cache \
    curl \
    && rm -rf /var/cache/apk/*

LABEL org.opencontainers.image.authors="Wojciech Dziedzic"

COPY default.conf /etc/nginx/conf.d/

EXPOSE 6005

HEALTHCHECK --interval=30s --timeout=30s --start-period=5s --retries=3 \
    CMD [ "curl localhost:6005" ]

CMD ["nginx", "-g", "daemon off;"]