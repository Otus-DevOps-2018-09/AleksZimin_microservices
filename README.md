# AleksZimin_microservices
AleksZimin microservices repository

## HW-18
[![Build Status](https://travis-ci.com/Otus-DevOps-2018-09/AleksZimin_microservices.svg?branch=monitoring-1)](https://travis-ci.com/Otus-DevOps-2018-09/AleksZimin_microservices)

### Основное задание:
* Запустил Prometheus в докере из официального образа.
* Создал докерфайл, который на основе официального образа Prometheus собирает кастомный образ с нашим конфигом. При каждом изменении конфига Prometheus необходимо пересобрать образ.
* Собрал образы приложения и Prometheus.
* Добавил в docker-compose prometheus и убрал оттуда все инструкции build, т.к. образы собираем баш скриптами.
* Поднял контейнеры, проверил добавление новых targets.
* Поднял node-exporter (софт для предоставления метрик о работе ОС Linux). Проверил его работу

### Сылка на докер хаб с моими образами:
* https://hub.docker.com/u/zav19

## HW-17
[![Build Status](https://travis-ci.com/Otus-DevOps-2018-09/AleksZimin_microservices.svg?branch=gitlab-ci-2)](https://travis-ci.com/Otus-DevOps-2018-09/AleksZimin_microservices)

### Основное задание:
* Запустил созданный в прошлом занятии инстанс в GCP с помощью docker-machine. У инстанса сменился ip.
* Из за смены ip необходимо было выполнить следующее:
```
-Сгенерировать новые сертификаты для инстанса в docker-machine (docker-machine regenerate-certs docker-host)
-Заменить ip адрес сервера в docker-compose.yml для контейнера gitlab-ci.
-Пересоздать контейнер gitlab-ci.
-Зарегистрировать в gitlab runner новый адрес сервера и токен.
```
* Создал новый проект example2 в gitlab
* Добавил проект в git
* Добавил окружения dev, stage и production в .gitlab-ci.yml
* Добавил ограничения для окружений stage и production (when: manual и only)
* Добавил переменные в .gitlab-ci.yml, которые определяют динамические окружения для каждой ветки в репозитории, кроме ветки master

## HW-16
[![Build Status](https://travis-ci.com/Otus-DevOps-2018-09/AleksZimin_microservices.svg?branch=gitlab-ci-1)](https://travis-ci.com/Otus-DevOps-2018-09/AleksZimin_microservices)

### Основное задание:
* Развернул инстанс в GCP с помощью docker-machine
* Запустил gitlab в контейнере. Отключил решистрацию, создал группу и проект в веб-интерфейсе.
* Запушил исходники в репозиторий проекта на gitlab.
* Создал pipeline .gitlab-ci.yml
* Создал контейнер gitlab-runner и в интерктивном режиме его зарегистрировал.
* Запустил pipeline, runner запустил контейнер, сбилдил приложение и прогнал простейшие тесты

## HW-15
[![Build Status](https://travis-ci.com/Otus-DevOps-2018-09/AleksZimin_microservices.svg?branch=docker-4)](https://travis-ci.com/Otus-DevOps-2018-09/AleksZimin_microservices)

### Основное задание:
* Запустил контейнеры с разными встроенными драйверами: none, host, bridge.
* Создал две сети front_net и back_net.
* Установил docker-compose. Написал конфиг для него
* Изменил docker-compose.yml под кейс с множеством сетей.
* Параметризировал с помощью переменных окружений: 
```
-внешний и внутренний порты сервиса ui
-версии сервисов
-имя пользователя
-название проекта
```
* Добавил файл .env в .gitignore.
* Базовое имя создается по имени папки, в которой происходит запуск docker-compose.

Для задания базового имени проекта необходимо добавить переменную COMPOSE_PROJECT_NAME=reddit_app.

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
