FROM node:14.5.0-alpine

EXPOSE 8080
ENV REDIS_HOST=redis \
    CATALOGUE_HOST=catalogue
WORKDIR /opt/server

COPY package.json /opt/server/

RUN npm install

COPY server.js /opt/server/

CMD ["node", "server.js"]

