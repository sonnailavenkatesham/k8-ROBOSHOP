FROM node:14.18.2-alpine
RUN addgroup -S roboshop && adduser -S catalogue roboshop
WORKDIR /app
RUN chown -R roboshop:catalogue /app
USER catalogue
COPY package.json /app/
COPY server.js /app/
RUN npm install
CMD [ "node", "server.js" ]