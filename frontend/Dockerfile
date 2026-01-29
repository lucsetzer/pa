FROM node:18-alpine

WORKDIR /app

# First copy only package files for better caching
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application
COPY . .

# Build the app
RUN npm run build

# Expose port
EXPOSE 8080

# Start the application
CMD ["npm", "run", "serve"]
