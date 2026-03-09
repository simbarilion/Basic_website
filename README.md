## Basic_website

Минимальный HTTP-сервер на Python, реализованный с использованием стандартного модуля http.server.

Проект демонстрирует:

- обработку GET- и POST-запросов

- отдачу HTML и CSS

- базовую маршрутизацию

- работу с переменными окружения

- организацию сервера в ООП-стиле

### Архитектура

Сервер реализован через наследование от BaseHTTPRequestHandler.

**Обработка запросов:**

- do_GET() — возвращает HTML-страницу или CSS-файл

- do_POST() — принимает данные запроса и выводит их в консоль

- read_content() — читает файл из директории dist/ и отправляет клиенту

Поддерживается:

- определение Content-Type

- чтение Content-Length

- возврат 404 при отсутствии файла

### Структура проекта

    Basic_website/
    │
    ├── src/
    │   └── class_server.py
    ├── dist/
    │   ├── page_contacts.html
    │   └── *.css
    ├── main.py
    ├── pyproject.toml
    └── README.md

### Технологии

Python 3.x

http.server (стандартная библиотека)

dotenv

Poetry

Bootstrap (для HTML-шаблонов)

### Установка:

````
git clone https://github.com/simbarilion/Basic_website.git
cd Basic_website
poetry install
poetry shell
````

Создайте файл .env:
```
HOST_NAME=127.0.0.1
SERVER_PORT=your_server_port_here
```

### Запуск
```
python main.py
```
После запуска сервер будет доступен по адресу:

```
http://127.0.0.1:8080
```

### Использование

**GET-запрос**

- Возвращает HTML-страницу из директории dist/.

**POST-запрос**

- Сервер:

  - считывает Content-Length

  - принимает данные запроса

  - выводит тело запроса в консоль

- Тестирование можно выполнить через:

    - браузер
    
    - Postman
    
    - curl

### Особенности

- Реализация сервера без использования фреймворков

- ООП-подход

- Работа с HTTP-заголовками

- Обработка ошибок (404)

- Конфигурация через переменные окружения

### Лицензия:

Проект распространяется под [лицензией MIT](LICENSE)

### Автор

Надежда Попова

Python Developer

📧 nadezhdapopova13@yandex.ru

🔗 GitHub: simbarilion