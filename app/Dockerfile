# pull the base image
FROM node:16.15.0-alpine3.14

# set the working direction
WORKDIR /app

# add `/node_modules/.bin` to $PATH
ENV PATH /node_modules/.bin:$PATH

# install app dependencies
COPY /package.json ./

COPY /yarn.lock ./

RUN yarn

# add app
COPY . ./

# start app
CMD ["yarn", "start"]
