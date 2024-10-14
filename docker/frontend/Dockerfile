FROM node:22-alpine3.19

RUN mkdir -p /var/www/dailycrm/frontend
WORKDIR /var/www/dailycrm/frontend

COPY ./frontend/package*.json ./
RUN npm install

COPY . .

RUN npm run build

EXPOSE 3000

ENV NUXT_HOST=frontend

ENV NUXT_PORT=3000

CMD [ "npm", "run", "dev" ]