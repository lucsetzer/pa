FROM node:18-alpine

WORKDIR /app

# Install dependencies
COPY package*.json ./
RUN npm install

# Copy application code
COPY . .

# Build the app
RUN npm run build

# Expose port
EXPOSE 8080

# Start the application
CMD ["npm", "run", "serve"]
