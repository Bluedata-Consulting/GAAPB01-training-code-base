FROM python:3.12-slim

WORKDIR /app

COPY . .
RUN pip install --no-cache-dir -r requirements.txt

EXPOSE 8080
ENV FLASK_APP=app:create_app
CMD ["gunicorn","-b","0.0.0.0:8080","app:create_app()"]
