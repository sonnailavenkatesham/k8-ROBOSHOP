FROM node:14.18.2-alpine
EXPOSE 8080
RUN addgroup -S roboshop && adduser -S catalogue roboshop
WORKDIR /app
RUN chown -R catalogue:roboshop /app
USER catalogue
COPY package.json /app/
COPY server.js /app/
RUN npm install
ENV MONGO=true
CMD [ "node", "server.js" ]