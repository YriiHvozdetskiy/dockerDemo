FROM node:20.16.0-slim

WORKDIR /usr/src/app

EXPOSE 5173

# Встановлюємо pnpm
RUN npm install -g pnpm

# Копіюємо pnpm-lock.yaml (якщо є) та package.json
COPY pnpm-lock.yaml package.json ./

# Встановлюємо залежності
RUN pnpm install --frozen-lockfile

# Копіюємо решту файлів проекту
COPY ../.. .
