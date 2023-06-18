FROM nginx:1.23.4-alpine as nginx

WORKDIR /var/www/html/

COPY default.conf /etc/nginx/conf.d/

EXPOSE 6005

CMD ["nginx", "-g", "daemon off;"]