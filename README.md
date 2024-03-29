# REST API
Реализация REST API без использования фреймворков.

## Системные требования
- PHP 8.2
- MariaDB 10.6.7 + или альтернативная версия MySQL 
- Apache 2.4.53 +
- Postman (для тестирования)

## Установка
- Создаем локальный домен
- Спуливаемся в корневую директорию локального домена
- Создаем базу данных. Например, такую:
  - name = 'data'
  - collation = 'utf8mb4_general_ci'
- Настраиваем подключение к БД в конфиг. файле ```/src/config.php```
- Открываем Postman:
- Производим однократный GET запрос к ```{ваш домен}/api/seeder``` для того, чтобы 
создать таблицу ```records``` и наполнить её демо-данными.
- Вы восхитительны!

## Поддерживаемые запросы
- GET ```/records:``` возвращает список всех записей.
- GET ```/records/:id:``` возвращает детали указанной записи.
- POST ```/records:``` добавляет новую запись. Новые данные передаются в теле запроса в формате JSON.
- PUT ```/records/:id:``` обновляет существующую запись. Данные для обновления передаются в теле запроса в формате JSON.
- DELETE ```/records/:id:``` удаляет существующую запись.

