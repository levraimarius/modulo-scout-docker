FROM node:16.3.0-alpine

WORKDIR /app

COPY /sources/node /sources/node

RUN yarn install

EXPOSE 3000

CMD ["yarn", "start"]