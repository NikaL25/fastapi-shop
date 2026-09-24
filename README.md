🛒 FastAPI Shop

Full-stack интернет-магазин на FastAPI и Vue 3.

Проект состоит из двух частей: серверного API и клиентского веб-приложения.

📁 Структура проекта
fastapi-shop/
├── backend/
│   ├── ...
│   └── requirements.txt
│
├── frontend/
│   ├── src/
│   ├── public/
│   ├── package.json
│   └── ...
│
└── README.md

🛠️ Стек технологий
Backend

Python

FastAPI — REST API

SQLAlchemy — работа с базой данных

Pydantic — валидация данных

Pydantic Settings — конфигурация приложения

Uvicorn — ASGI-сервер

python-dotenv — переменные окружения

Frontend

Vue 3 — пользовательский интерфейс

Vue Router — маршрутизация

Pinia — управление состоянием

Vite — сборка и development server

ESLint — статический анализ

Oxlint — быстрый линтер

Prettier — форматирование кода

⚙️ Требования

Перед запуском проекта необходимо установить:

Python 3

Node.js 20.19+ или 22.12+

pnpm

🚀 Запуск Backend

Перейдите в директорию backend:

cd backend


Создайте виртуальное окружение:

python -m venv .venv


Активируйте его.

Linux / macOS
source .venv/bin/activate

Windows
.venv\Scripts\activate


Установите зависимости:

pip install -r requirements.txt


Запустите сервер:

uvicorn main:app --reload


После запуска API будет доступно по адресу:

http://127.0.0.1:8000


Swagger UI:

http://127.0.0.1:8000/docs


ReDoc:

http://127.0.0.1:8000/redoc

🎨 Запуск Frontend

Перейдите в директорию frontend:

cd frontend


Установите зависимости:

pnpm install


Запустите development server:

pnpm dev


Для production-сборки:

pnpm build


Для локального просмотра production-сборки:

pnpm preview

🧹 Code Quality

Проверка и автоматическое исправление проблем:

pnpm lint


Форматирование проекта:

pnpm format

🔐 Environment Variables

Конфиденциальные настройки приложения должны храниться в .env.

Пример файла:

DATABASE_URL=...


Файлы с секретными значениями не должны добавляться в Git.

🏗️ Архитектура

Приложение разделено на клиентскую и серверную части:

                    ┌──────────────────┐
                    │     Vue 3        │
                    │                  │
                    │ Router + Pinia   │
                    └────────┬─────────┘
                             │
                             │ HTTP / API
                             ▼
                    ┌──────────────────┐
                    │     FastAPI      │
                    │                  │
                    │ REST API         │
                    └────────┬─────────┘
                             │
                             ▼
                    ┌──────────────────┐
                    │    SQLAlchemy    │
                    │                  │
                    │    Database      │
                    └──────────────────┘


Frontend отвечает за пользовательский интерфейс, маршрутизацию и состояние приложения.

Backend предоставляет API, выполняет бизнес-логику и взаимодействует с базой данных.

📦 Основные команды
Backend
uvicorn main:app --reload

Frontend
pnpm dev
pnpm build
pnpm preview
pnpm lint
pnpm format

📄 License

Лицензия проекта пока не указана.
