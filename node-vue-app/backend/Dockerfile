# Use Node.js LTS image
FROM node:20

# Set the working directory
WORKDIR /usr/src/app

# Copy package.json and install dependencies
COPY package.json ./
RUN npm install

# Copy the application code
COPY . .

# Expose the backend port
EXPOSE 3000

# Start the backend server
CMD ["npm", "start"]
