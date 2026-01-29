FROM node:18-alpine

WORKDIR /app

# Install dependencies
COPY frontend/package*.json ./
RUN npm install

# Copy application code
COPY frontend/ .

# Build the app
RUN npm run build

# Expose port
EXPOSE 8080

# Start the application
CMD ["npm", "run", "serve"]
