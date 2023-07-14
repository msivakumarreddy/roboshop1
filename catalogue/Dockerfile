FROM node:14.5.0-alpine
RUN addgroup -S catalogue && adduser -S catalogue -G catalogue
EXPOSE 8080
ENV MONGO_URL="mongodb://mongodb:27017/catalogue"
WORKDIR /opt/server
RUN chown -R catalogue:catalogue /opt/server
USER catalogue
COPY package.json /opt/server/

RUN npm install

COPY server.js /opt/server/

ENTRYPOINT ["node", "server.js"]

