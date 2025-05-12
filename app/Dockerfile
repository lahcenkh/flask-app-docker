FROM python:3.11-slim-bullseye

WORKDIR /flask-todo-app

COPY requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt

COPY . .

EXPOSE 5000

CMD ["gunicorn", "--bind", "0.0.0.0:5000", "wsgi:app", "--log-level=debug", "--workers=3"]