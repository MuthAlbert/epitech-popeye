FROM node:12-alpine

WORKDIR /result

COPY package*.json ./

RUN npm install

COPY . .

EXPOSE 80

CMD npm start