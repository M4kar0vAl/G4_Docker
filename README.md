## Переменные окружения

- Создать в корне проекта файл `.env`
- Заполнить его по подобию `example.env`

## Запуск

- При первом запуске выполнить команды:
  ```
  docker compose up -d --build
  docker exec django python manage.py createsuperuser --noinput
  ```
- При последующих создавать суперпользователя уже не нужно, поэтому просто:
  ```
  docker compose up -d --build
  ```
  
## Остановка

- ```
  docker compose down
  ```
  
## Админ панель

http://127.0.0.1:8000/admin/
