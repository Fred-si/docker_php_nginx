FROM nginx:alpine as nginx

COPY nginx.conf /etc/nginx/conf.d/default.conf
COPY /public /app

RUN chown -R nginx:nginx /app && \
    chmod -R 755 /app

FROM php:fpm-alpine as php

COPY /public /app
RUN chmod -R 755 /app

