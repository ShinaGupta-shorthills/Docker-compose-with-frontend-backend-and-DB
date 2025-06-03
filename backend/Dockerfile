FROM python:3.9-slim

WORKDIR /app

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY app.py .
COPY wait-for-db.sh .
RUN chmod +x wait-for-db.sh

CMD ["python", "app.py"]
