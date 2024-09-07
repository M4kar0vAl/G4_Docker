FROM python:slim

ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

WORKDIR /app

COPY requirements.txt requirements.txt

RUN pip install --no-cache-dir --no-warn-script-location -r requirements.txt

COPY . .

EXPOSE 8000

CMD python manage.py migrate && \
    python manage.py collectstatic --noinput && \
    gunicorn django_project.wsgi:application -b 0.0.0.0:8000 --timeout 90