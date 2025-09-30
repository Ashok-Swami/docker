# Use lightweight Node.js base image
FROM node:22-alpine

# Set working directory
WORKDIR /app

# Copy only package files first (better caching)
COPY package*.json ./

# Install dependencies (full set for development)
RUN npm install --legacy-peer-deps

# Copy rest of the code
COPY . .



# Expose React dev server port
EXPOSE 3000

# Start React app in development mode
CMD ["npm", "start"]
