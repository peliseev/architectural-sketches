# Урок 5. Почему OpenShift

В этом уроке в кластере OpenShift развертывается qute-service из предыдущего урока. 

В ходе урока были выполнены следующие команды:

Запуск CRC с явным указанием DNS 1.1.1.1:
`crc start -n 1.1.1.1`

Создание проекта в OpenShift:
`oc new-project architectural-sketches`

Создание configMap с конфигурацией nginx:
`oc create configmap nginx-conf --from-file=$(pwd)\nginx-cm\nginx.conf`

Создание configMap с html
`oc create configmap nginx-html --from-file=$(pwd)\nginx-cm\index.html`

Создание остальных ресурсов 
`oc apply -f .\quote-app.yaml`