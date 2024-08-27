FROM python:3.12

WORKDIR /app

COPY main.py .
COPY database.py .
COPY .env .


RUN pip install fastapi sqlalchemy geopy pydantic python-dotenv gunicorn pymysql


CMD ["gunicorn", "main:app", "--bind", "0.0.0.0:8729", "--workers", "4"]

EXPOSE 8729

