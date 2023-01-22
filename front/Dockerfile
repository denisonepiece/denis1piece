FROM node:16-alpine
WORKDIR /app
COPY package*.json ./
RUN npm i
COPY tsconfig*.json ./
COPY index.html ./
COPY public public
COPY src src
RUN npm run build

RUN npm i --global serve
CMD serve -s dist