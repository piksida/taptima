FROM node:12.0.0-alpine
WORKDIR /usr/src/app
COPY package*.json ./
RUN npm ci
COPY . .
RUN cp src/environments/environment.prod.ts src/environments/environment.ts
RUN npm run build

EXPOSE 3000
CMD [ "node", "./dist/index.js" ]
