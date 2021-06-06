# Урок 4. Докер на практике

В этом уроке решаятся задача по развертыванию веб-сервера, который отдает веб страницу и является обратным прокси, и сервиса, выполняющего функцию генератора цитат из фильмов "Брат" и "Брат 2".

В ходе урока были выполнены следующие команды:

Сборка *quota-service*:
`docker build -t quote-service ./service`

Создание docker network:
`docker network create -d bridge quota-infra`

Запуск *quota-service*:
`docker run --hostname=quotaservice --network=quota-infra -d quote-service`

Запуск nginx
`docker run -v $(pwd)/nginx/www:/usr/share/nginx/html -v $(pwd)/nginx/conf:/etc/nginx -p 80:80 -d --network=quota-infra nginx`