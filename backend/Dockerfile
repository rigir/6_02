FROM node:latest AS build

WORKDIR /app
COPY package.json .
RUN npm install
COPY ./src ./src

FROM node:latest
WORKDIR /app
COPY --from=build ./app . 
EXPOSE 9000
CMD node ./src/index.js 