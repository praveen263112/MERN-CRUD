# Use an official Node runtime as a parent image
FROM node:14

# Set the working directory in the container
WORKDIR /usr/src/app

# Install app dependencies by copying
# package.json and package-lock.json only
COPY package*.json ./

# Install dependencies
RUN npm install

# Bundle app source inside Docker image
COPY . .

# Make port 8080 available for the app
EXPOSE 8080

# Define the command to run the app
CMD ["npm", "start"]
