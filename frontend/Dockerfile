# Use the official Node.js image as a base image
FROM node:18.14.2 as build

# Set the working directory to /app
WORKDIR /app

# Copy the package.json and package-lock.json files to the working directory
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy all files from the current directory to the working directory
COPY . .

# Build the frontend application
RUN npm run build

# Use a lightweight Nginx image as the final image
FROM nginx:latest

# Copy the build files from the build stage to the default Nginx public folder
COPY --from=build /app/build /usr/share/nginx/html

# Expose the port on which the Nginx server will run
EXPOSE 80

# Command to run the Nginx server
CMD ["nginx", "-g", "daemon off;"]
