# Step 1: Use an official Node.js image as the base
FROM node:20-alpine

# Step 2: Set the working directory inside the container
WORKDIR /app

# Step 3: Copy package.json and package-lock.json
COPY package*.json ./

# Step 4: Install dependencies
RUN npm install

# Step 5: Copy the rest of the application code
COPY . .

# Step 6: Build the app for production
RUN npm run build

# Step 7: Serve the build using a simple HTTP server
RUN npm install -g serve
CMD ["serve", "-s", "dist"]

# Expose the port the app will run on
EXPOSE 3000