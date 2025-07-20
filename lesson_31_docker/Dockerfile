# Dockerfile
FROM python:3.12-slim

# Робоча директорія в контейнері
WORKDIR /app

# Копіюємо всі файли
COPY . .

# Встановлюємо залежності
RUN pip install --no-cache-dir -r requirements.txt

# Порт для FastAPI
EXPOSE 8000

# Значення за замовчуванням (можна змінити через CMD)
ENTRYPOINT ["python"]

# Якщо не вказано іншого, запускається FastAPI
CMD ["-m", "uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "8000"]
