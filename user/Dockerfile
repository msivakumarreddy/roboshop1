FROM node:14.5.0-alpine

EXPOSE 8080
RUN addgroup -S user && adduser -S user -G user

ENV MONGO_URL="mongodb://mongodb:27017/users"
USER user
WORKDIR /opt/server

COPY package.json /opt/server/

RUN npm install

COPY server.js /opt/server/

CMD ["node", "server.js"]

