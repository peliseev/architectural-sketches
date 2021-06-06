FROM nginx

RUN rm /etc/nginx/conf.d/default.conf

COPY conf/nginx.conf /etc/nginx/nginx.conf
COPY www/index.html /usr/share/nginx/html