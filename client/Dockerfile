# Use an official Node runtime as a parent image
FROM node:14

# Set the working directory in the container
WORKDIR /usr/src/app

# Install app dependencies by copying
# package.json and package-lock.json only
COPY package*.json ./

# Install dependencies
RUN npm install
RUN npx browserslist@latest --update-db

# Bundle app source inside Docker image
COPY . .

# Build the application for production
RUN npm run build

CMD ["npm", "run", "start"]