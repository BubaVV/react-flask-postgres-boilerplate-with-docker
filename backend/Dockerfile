FROM python:3.10-slim

COPY requirements.txt /app/requirements.txt

RUN apt-get update && \
    pip install --upgrade pip && \
    pip install --no-cache-dir -r /app/requirements.txt && \
    rm -rf /var/lib/apt/lists

COPY . /app

CMD ["python", "/app/app.py"]