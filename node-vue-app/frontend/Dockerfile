# Use Node.js LTS image for building Vue app
FROM node:20 AS build

# Set the working directory
WORKDIR /usr/src/app

# Copy package.json and install dependencies
COPY package.json ./
RUN npm install

# Copy the application code
COPY . .

# Build the frontend for production
RUN npm run build

# Use Nginx to serve the static files
FROM nginx:alpine
COPY --from=build /usr/src/app/dist /usr/share/nginx/html

# Expose the frontend port
EXPOSE 8080
