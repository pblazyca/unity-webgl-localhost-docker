FROM nginx:alpine

WORKDIR /etc/nginx/conf.d
COPY webgl.conf default.conf

WORKDIR /srv/www/webgl
COPY app/ .