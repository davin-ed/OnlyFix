# Use the official Node.js image
FROM node:18

# Set the working directory inside the container
WORKDIR /usr/src/app

# Copy package.json and package-lock.json from the root directory
COPY ./package*.json ./

# Install Node.js dependencies
RUN npm install

# Copy the React source code into the container
COPY ./resources/js ./resources/js

# Set working directory to the React folder where package.json exists
WORKDIR /usr/src/app/resources/js

# Build the React app
RUN npm run build

# Expose the port (for development, typically 3000; adjust if necessary for production)
EXPOSE 3000

# Start the React app (usually you want to use 'npm run start' for development, 
# but if you want to serve the build, you'd need something like `serve` or Nginx)
CMD ["npm", "start"]
