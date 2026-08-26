FROM ubuntu

WORKDIR /app

RUN apt update -y

RUN apt install apache2 -y

COPY . /var/www/html

EXPOSE 80

ENTRYPOINT ["apachectl", "-D", "FOREGROUND"]

# Dockcerfile for NodeJs application

FROM node:latest

WORKDIR /usr/src/app

COPY package*.json ./

RUN npm install

COPY . .

EXPOSE 3000

CMD ["node", "app.js"]