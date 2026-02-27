# Dockerfile for React Application

# Step 1: Build the React application
FROM node:16 AS build
WORKDIR /app
COPY package.json .
COPY package-lock.json .
RUN npm install
COPY . .
RUN npm run build

# Step 2: Serve the application using NGINX
FROM nginx:alpine
COPY --from=build /app/build /usr/share/nginx/html

# Expose the port NGINX is running on
EXPOSE 80

# Command to run NGINX
CMD ["nginx", "-g", "daemon off;"]