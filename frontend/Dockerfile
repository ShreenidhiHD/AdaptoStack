# Use the official Node image.
FROM node:14

# Set the working directory in Docker
WORKDIR /usr/src/app

# Copy package.json and package-lock.json before other files
# Utilize Docker cache to save re-installing dependencies if unchanged
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy local code to the container
COPY . .

# Specify port
EXPOSE 3000

# Command to run the application
CMD ["npm", "start"]
