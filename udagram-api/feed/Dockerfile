# Use NodeJS base image
FROM node:13

# Create app directory in Docker
WORKDIR /usr/src/app

# Install app dependencies by copying
# package.json and package-lock.json
COPY package*.json ./

# Install dependencies in Docker
RUN npm install

COPY ./ ./

# Bind the port that the image will run on
RUN export PORT=8080
EXPOSE $PORT

# Define the Docker image's behavior at runtime
CMD ["node", "./www/server.js"]
