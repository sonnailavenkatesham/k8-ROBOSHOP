FROM node:14
RUN addgroup -S roboshop && adduser -S catalogue roboshop
WORKDIR /app
RUN chown -R roboshop:catalogue /app
USER /app
COPY package.json /app/
COPY server.js /app/
RUN npm install
CMD [ "node", "server.js" ]