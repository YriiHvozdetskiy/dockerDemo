FROM nginx

# видаляємо стандартний конфіг
RUN rm /etc/nginx/conf.d/default.conf

# підміняємо стандартний конфіг на свій
COPY nginx.conf /etc/nginx/conf.d
