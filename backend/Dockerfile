FROM node:20
#if the /opt/backend is not availble WORKDIR will creates that
WORKDIR /opt/backend
COPY package.json .
COPY *.js .
RUN npm install
ENV MY_HOST="mysql"
CMD [ "node", "index.js" ]