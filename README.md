# AleksZimin_microservices
AleksZimin microservices repository

## HW-13
[![Build Status](https://travis-ci.com/Otus-DevOps-2018-09/AleksZimin_microservices.svg?branch=docker-2)](https://travis-ci.com/Otus-DevOps-2018-09/AleksZimin_microservices)

### Основное задание:
Создал новый проект в GCP.
Сконфигурировал gcloud на новый проект.
Установил docker-machine.
Создал docker-host через gcloud.
Повторил практику из лекции, посмотрел на изоляцию неймспейсов (PID, network).
Запустил докер-в-докере.
Создал Dockerfile с установкой и настройкой всех необходимых пакетов для приложения reddit.
Собрал образ, запустил его на docker-host, опубликовал в docker-registry, запустил локально.
Посмотрел логи, проверил, что kill pid 1 уничтожает контейнер.
Вывел инфу о контейнере.
Посоздавал папки и файлы, удалил контейнер, создал, проверил, что папки отсутствуют.

## HW-12
[![Build Status](https://travis-ci.com/Otus-DevOps-2018-09/AleksZimin_microservices.svg?branch=docker-1)](https://travis-ci.com/Otus-DevOps-2018-09/AleksZimin_microservices)

### Основное задание:
* Добавлен файл шаблона PR .github/PULL_REQUEST_TEMPLATE
* Скопирован файл .travis.yml
* Выполнена интеграция со Slack
* Установил docker-ce и docker-compose
* Запустил первый контейнер hello-world
* Поработал с простыми командами для работы с контейнерами и образами
* Остановил все контейнеры, удалил все остановленные контейнеры, удалил все образы.
