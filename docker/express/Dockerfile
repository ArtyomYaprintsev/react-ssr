# Fetching the minified node image on apline linux
FROM node:slim

# Installing dependencies
COPY ./package.json /package.json
COPY ./package-lock.json /package-lock.json
RUN npm install

COPY ./docker/express/start /start
RUN sed -i 's/\r$//g' /start
RUN chmod +x /start

# Setting up the work directory
WORKDIR /app
