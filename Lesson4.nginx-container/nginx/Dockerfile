# ПЛОХОЙ ПРИМЕР
# 
# Хорошей практикой является создание образа только с теми файлами, 
# которые не должны быть изменены все время жизни контейнера.
# Если требуется подложить в образ конфигурационные файлы или контент,
# который может быть изменен во время жизни контейнера, лучше это делать
# через docker volume.

FROM nginx

RUN rm /etc/nginx/conf.d/default.conf

COPY conf/nginx.conf /etc/nginx/nginx.conf
COPY www/index.html /usr/share/nginx/index.html
