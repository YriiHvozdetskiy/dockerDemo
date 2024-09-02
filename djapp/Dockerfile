FROM python:3.11-slim

# зберігати в корновій папці не безпечно
WORKDIR /usr/src/myapp

# щоб не було буферизації
ENV PYTHONUNBUFFERED=1

COPY requirements.txt .

# --no-cache-dir при оновленні pip запобігає зберіганню непотрібного кешу
RUN pip install --no-cache-dir --upgrade pip && \
    pip install -r requirements.txt

# Це дозволяє максимально використовувати кешування шарів Docker
COPY . .