FROM node:18
EXPOSE 8080
#default server aneedi opt/server
WORKDIR /opt/server
ENV MONGO=true
COPY package.json /opt/server/
COPY server.js /opt/server/
#dependences ni install chestundhi
RUN npm install
CMD ["node", "server.js"]