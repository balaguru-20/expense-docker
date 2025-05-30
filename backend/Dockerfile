#FROM node:20
#for reducing the image size
FROM node:20.18.3-alpine3.21
#if the /opt/backend is not availble WORKDIR will creates that
RUN addgroup -S expense && adduser -S expense -G expense && \
    mkdir /opt/backend && \
    chown -R expense:expense /opt/backend
WORKDIR /opt/backend
ENV DB_HOST="mysql"
#ENV DB_HOST="localhost"
USER expense
COPY package.json .
COPY *.js ./
RUN npm install
CMD [ "node", "index.js" ]