FROM node:14.5.0-alpine
RUN addgroup -S cart && adduser -S cart -G cart
EXPOSE 8080
ENV REDIS_HOST=redis \
    CATALOGUE_HOST=catalogue
WORKDIR /opt/server
RUN chown -R cart:cart /opt/server
USER cart
COPY package.json /opt/server/
RUN npm install
COPY server.js /opt/server/
CMD ["node", "server.js"]

