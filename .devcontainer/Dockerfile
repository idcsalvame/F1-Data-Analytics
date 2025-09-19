FROM python:3.12-slim

RUN apt-get update && apt-get install -y git \
    build-essential \
    postgresql-client \
    pkg-config \
    libpq-dev \
    curl \
    && rm -rf /var/lib/apt/lists/*
    

WORKDIR /workspace

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt