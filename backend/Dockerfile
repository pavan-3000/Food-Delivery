FROM node:18-alpine

WORKDIR /usr/src/app

COPY package*.json ./
RUN npm install --production

COPY config/db.js ./config/
COPY controllers/ ./controllers/
COPY middleware/auth.js ./middleware/
COPY models/ ./models/
COPY routes/ ./routes/
COPY server.js ./
COPY uploads/ ./uploads/

EXPOSE 4000

CMD ["node", "server.js"]