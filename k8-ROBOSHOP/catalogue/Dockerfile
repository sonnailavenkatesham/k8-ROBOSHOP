FROM node:14.21.3-alphine3.17
RUN addgroup -S roboshop && adduser -S catalogue roboshop
WORKDIR /app
RUN chown -R roboshop:catalogue /app
USER catalogue
COPY package.json /app/
COPY server.js /app/
RUN npm install
CMD [ "node", "server.js" ]