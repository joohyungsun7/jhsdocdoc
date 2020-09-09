FROM node:current-slim

WORKDIR /usr/src/app
COPY package.json .
RUN npm install

EXPOSE 7070
CMD [ "npm", "start" ]

COPY . .
