# Лабораторная работа №1: Настройка Nginx в Docker

## Описание
Создание и настройка простого веб-сервера на основе Nginx в Docker-контейнере.

## Цель
Получить знания и опыт о том, как устроен хостинг.

## Технологии
- Docker
- Nginx
- HTML

## Структура проекта
- `website/` — папка с файлами сайта (подключается к контейнеру как том)
- `nginx/default.conf` — конфигурация Nginx

## Как запустить

### Требования
- Установленный и запущенный Docker Desktop

### Инструкции
1. Откройте терминал в папке `lab-01`.
2. Выполните команду:
   ```bash
   docker run -d --name my-nginx-lab -p 5143:80 -v ${PWD}/website:/usr/share/nginx/html:ro -v ${PWD}/nginx/default.conf:/etc/nginx/conf.d/default.conf:ro nginx:latest