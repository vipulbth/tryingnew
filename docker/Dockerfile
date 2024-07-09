# Use an official Node.js runtime as a parent image
FROM node:14

# Set the working directory
WORKDIR /app

# Copy package.json and package-lock.json (if present)
COPY package*.json ./

# Install any needed packages
RUN npm install

# Copy the rest of the application code
COPY . .

# Build the application (if needed)
RUN npm run build

# Serve the application using a static server (e.g., serve)
# First, install serve globally
RUN npm install -g serve

# Expose port 5000 to the outside world
EXPOSE 5000

# Command to run the app
CMD ["serve", "-s", "build", "-l", "5000"]
