ARG NODE_VERSION=20

FROM node:${NODE_VERSION}-alpine

ENV NODE_ENV=production

WORKDIR /usr/src/app

COPY package.json package.json
COPY package-lock.json package-lock.json

RUN npm ci --omit=dev

COPY . .

EXPOSE 3000

CMD node src/index.js