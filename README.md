# docker-postfix-dovecot-postfixadmin-redmine-mariadb
+ Простой почтовый сервер для локальной сети с авторизацией почтовых ящиков с помощью нешифрованных паролей.

# Предварительные условия
* Запущенный Docker на хостовой машине.
* Запущенный Docker compose на хостовой машине.
* Базовые знания по работе с Docker 

# Описание и структура проекта:
* cfg - каталог с неизменяемыми конфигурационными файлами
* data - каталог базы данных почтовых ящиков
* dockerfile - содержит настраиваемый образ в зависимости от переменных окружения заданных в файле .env
*  - dovecot - конф.файлы программ dovecot и postfix, которые настраиваются в зависимости от файла .env при сборке образа.
*  - postfix - ...
* .env.example - файл с используемыми переменными окружения. Данный файл следует переименовать в файл .env
* docker-compose.yml - основной файл с используемыми сервисами.

# Установка
+ Clone the repo.
+ Запустите `docker-compose up -d` для запуска контейнеров.

# Используемы images:
+ redis:alpine
+ postgres:9.5-alpine
+ rabbitmq:3-management-alpine
+ nginx:alpine
+ php:8.2-fpm


