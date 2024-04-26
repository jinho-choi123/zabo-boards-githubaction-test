# Dockerfile for production build
FROM node:18-alpine

WORKDIR /app

COPY . .

RUN npm install -g yarn

RUN yarn

RUN yarn build

RUN yarn install --global serve

EXPOSE 80

ENTRYPOINT ["serve", "-l", "80", "/app/dist"]
