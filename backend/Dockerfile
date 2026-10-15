#use Node.js base image for backend
FROM node:18-alpine

#Setting working directory inside container
WORKDIR /app

#Copying package.json and package-lock.json to working directory
COPY package*.json ./

#Installing dependencies
RUN npm install

COPY . .

# Create directory for SQLite data files
RUN mkdir -p /app/data

# Expose the port that the backend will run on
EXPOSE 5000

# Start the application
CMD ["npm", "start"]