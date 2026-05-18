FROM python:3.11-slim

WORKDIR /app

# Устанавливаем все необходимые системные зависимости
RUN apt-get update && apt-get install -y \
    libpq-dev \
    gcc \
    zlib1g-dev \
    libjpeg-dev \
    && rm -rf /var/lib/apt/lists/*

COPY requirements.txt .

RUN pip install -r requirements.txt --no-cache-dir

COPY . .

CMD ["gunicorn", "--bind", "0.0.0.0:8000", "kittygram_backend.wsgi"]
