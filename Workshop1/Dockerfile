FROM node:latest

ENV DB_HOST=mydb 
ENV DB_PORT=3306
ENV DB_USER=root
ENV DB_PASSWORD=changeit
ENV APP_DIR=/APP_DIR
ENV APP_PORT=3000

WORKDIR ${APP_DIR}

ADD config config
ADD public public
ADD views views

ADD main.js .
ADD package.json .
ADD package-lock.json .

RUN npm install

EXPOSE ${APP_PORT}

ENTRYPOINT ["node", "main.js"]
