FROM node:12.0.0-alpine as builder
WORKDIR /usr/src/app
COPY package*.json ./
RUN npm ci 
RUN npm install sass
COPY . .
RUN npm run build:prod

FROM nginx:latest
COPY --from=builder /usr/src/app/dist/questionnaire-frontend/ /usr/share/nginx/html
COPY ./nginx.conf /etc/nginx/conf.d/default.conf

EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
