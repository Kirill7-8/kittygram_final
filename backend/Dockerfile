# Используем официальный образ Python 
FROM python:3.10

# Устанавливаем рабочую директорию внутри контейнера
WORKDIR /app

# Копируем файл с зависимостями
COPY requirements.txt .

# Устанавливаем зависимости
RUN pip install --no-cache-dir -r requirements.txt

# Копируем весь код бэкенда в контейнер
COPY . .

# Команда для запуска Gunicorn (сервер для Django)
CMD ["gunicorn", "--bind", "0.0.0.0:8000", "kittygram_backend.wsgi"]