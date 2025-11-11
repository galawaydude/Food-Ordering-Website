# Use Node.js LTS
FROM node:18-slim

# Set working directory
WORKDIR /usr/src/app

# Copy dependency definitions
COPY package*.json ./

# Install dependencies (production only)
RUN npm ci --only=production

# Copy app source
COPY . .

# Expose port
EXPOSE 4000

# Start the app
CMD ["node", "server.js"]
