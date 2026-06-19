FROM node:18-alpine

WORKDIR /app

COPY package*.json ./
RUN npm install

COPY vite.config.js ./
COPY src/ ./src/
COPY public/ ./public/
COPY .eslintrc.cjs ./

RUN npm run build

EXPOSE 5173

CMD ["npx", "vite", "preview", "--host", "--port", "5173"]