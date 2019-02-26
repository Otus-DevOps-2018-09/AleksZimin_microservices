# AleksZimin_microservices
AleksZimin microservices repository

## HW-14
[![Build Status](https://travis-ci.com/Otus-DevOps-2018-09/AleksZimin_microservices.svg?branch=docker-3)](https://travis-ci.com/Otus-DevOps-2018-09/AleksZimin_microservices)

### Основное задание:
* Установил hadolint в своей ОС и интегрировал его с VScode с помощью расширения vscode-hadolint.
* Загрузил новые исходники нашего приложения, разделённые на модули.
* Написал докерфайлы для каждого сервиса.
* Скачал образ mongodb, сбилдил образы с сервисами, создал сеть (bridge) для приложения.
* Запустил контейнеры.
* Перезапустил контейнеры с новыми сетевыми алиасами без пересборки образов.
* Добавил volume для mongodb. Теперь при перезапуске приложения посты не удаляются.

## HW-13
[![Build Status](https://travis-ci.com/Otus-DevOps-2018-09/AleksZimin_microservices.svg?branch=docker-2)](https://travis-ci.com/Otus-DevOps-2018-09/AleksZimin_microservices)

### Основное задание:
* Создал новый проект в GCP.
* Сконфигурировал gcloud на новый проект.
* Установил docker-machine. Средство для управления несколькими докер-хостами.
* Создал docker-host через gcloud.
* Повторил практику из лекции, посмотрел на изоляцию неймспейсов (PID, network).
* Запустил докер-в-докере.
* Создал Dockerfile с установкой и настройкой всех необходимых пакетов для приложения reddit.
* Собрал образ, запустил его на docker-host, опубликовал в docker-registry, запустил локально.
* Посмотрел логи, проверил, что kill pid 1 уничтожает контейнер.
* Вывел инфу о контейнере.
* Посоздавал папки и файлы, удалил контейнер, создал, проверил, что папки отсутствуют.

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
