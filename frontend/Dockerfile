FROM node:18-alpine

WORKDIR /app

COPY package.json package-lock.json ./
RUN npm install --production

COPY public ./public
COPY src ./src
COPY index.html ./
COPY vite.config.js ./

RUN npm run build

EXPOSE 5173

CMD ["npx", "vite", "preview", "--host", "--port", "5173"]