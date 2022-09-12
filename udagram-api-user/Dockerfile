# Use NodeJS base image
FROM node:16-alpine

# Create app working directory
WORKDIR /usr/src/app

# Install app dependencies by copying
# package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm ci

# Bundle app source
COPY . .

EXPOSE 8080
CMD [ "npm", "run", "prod" ]