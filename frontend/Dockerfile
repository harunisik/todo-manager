FROM node:14
#FROM registry.access.redhat.com/ubi8/nodejs-12

# Create app directory
WORKDIR /usr/src/app

# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied
# where available (npm@5+)
#COPY package*.json ./

#RUN npm install
# If you are building your code for production
# RUN npm ci --only=production

COPY . /usr/src/app

#RUN npm install
RUN npm install --global http-server
RUN npm install json-server
RUN npm ci --only=production

EXPOSE 8080

CMD sh /usr/src/app/start.sh
