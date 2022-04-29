# Dockerfile
FROM node:16.15.0-alpine

# create & set working directory
RUN mkdir -p /src
WORKDIR /src

COPY package*.json ./

# ARG NPM_ACCESS_TOKEN

# RUN echo "//registry.npmjs.org/:_authToken=${NPM_ACCESS_TOKEN}" >> ~/.npmrc

# install dependencies
RUN npm install

# copy source files
COPY . /src

# start app
RUN npm run build
EXPOSE 3105
CMD npm run start