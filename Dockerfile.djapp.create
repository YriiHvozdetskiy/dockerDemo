FROM python:3.11-slim

# зберігати в корновій папці не безпечно
WORKDIR /usr/src/app

RUN pip install --no-cache-dir --upgrade pip

RUN pip install django

CMD ["django-admin", "startproject", "djapp"]