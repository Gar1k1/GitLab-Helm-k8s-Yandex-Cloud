FROM node:16-alpine3.16

WORKDIR /usr/src/app

# Копируем package.json и package-lock.json
COPY package.json package-lock.json ./

# Устанавливаем зависимости
RUN npm install

# Копируем остальной код
COPY . .

# Запускаем приложение
CMD ["npm", "start"]