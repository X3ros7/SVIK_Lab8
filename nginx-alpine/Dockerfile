FROM alpine

ARG NGINX_VERSION=1.26.2

RUN apk update

RUN apk add nginx~=${NGINX_VERSION}

RUN apk add supervisor

COPY nginx.conf /etc/nginx/nginx.conf

COPY index.html /usr/share/nginx/html/

COPY supervisord.conf /etc/supervisord.conf

CMD [ "supervisord", "-c", "etc/supervisord.conf" ]
