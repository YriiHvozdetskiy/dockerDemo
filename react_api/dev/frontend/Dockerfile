FROM node:20.16.0-slim AS build

WORKDIR /usr/src/myapp

COPY package*.json ./

RUN npm install

COPY . .

RUN npm run build

FROM nginx:alpine-slim

# берем з першого етапу зборки build файли з /usr/src/myapp/build
# розміщуємо всі файли в папку /usr/share/nginx/html
COPY --from=build /usr/src/myapp/build /usr/share/nginx/html

RUN rm /etc/nginx/conf.d/default.conf
COPY nginx.conf /etc/nginx/conf.d

EXPOSE 3000