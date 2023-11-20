# Use the official Node.js image as a base image
FROM node:18.14.2

# Set the working directory to /app
WORKDIR /app

# Copy the package.json and package-lock.json files to the working directory
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy all files from the current directory to the working directory
COPY . .

# Expose the port on which the application will run
EXPOSE 3000

# Command to run the application
CMD ["node", "server.js"]
