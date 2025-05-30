#FROM node:20
FROM node:20.18.3-alpine3.21
#if the /opt/backend is not availble WORKDIR will creates that
WORKDIR /opt/backend
COPY package.json .
COPY *.js .
RUN npm install
ENV DB_HOST="mysql"
#ENV DB_HOST="localhost"
CMD [ "node", "index.js" ]