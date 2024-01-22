FROM node:alpine

# Environment variables
ARG SERVER_PORT=8080

RUN mkdir -p /home/node/app/node_modules

WORKDIR /home/node/app

# Copy packages
COPY ./package*.json ./

# Inst
RUN npm install

COPY . .

RUN npm run build

EXPOSE ${SERVER_PORT}

CMD [ "node", "server.js" ]
