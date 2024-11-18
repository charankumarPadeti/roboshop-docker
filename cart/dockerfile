# #FROM node:18
# FROM node:18.19.1-alpine3.19
# EXPOSE 8080
# #default server aneedi opt/server
# WORKDIR /opt/server
# ENV MONGO=true
# COPY package.json /opt/server/
# COPY server.js /opt/server/
# #dependences ni install chestundhi
# RUN npm install
# CMD ["node", "server.js"]


FROM node:18.19.1-alpine3.19
EXPOSE 8080
RUN addgroup -S roboshop && adduser -S roboshop -G roboshop
WORKDIR /opt/server
ENV MONGO=true
RUN chown roboshop:roboshop /opt/server
USER roboshop
COPY package.json /opt/server/
COPY server.js /opt/server/
RUN npm install
CMD ["node", "server.js"]