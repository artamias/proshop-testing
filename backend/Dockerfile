FROM node:20-alpine

# Set working directory
WORKDIR /app

# Copy root package files into container
COPY package.json package-lock.json ./

# Install production dependencies
RUN npm install --production

# Copy backend source code
COPY backend/ /app/backend

# Expose backend port
EXPOSE 5000

# Start backend server
CMD ["node", "backend/server.js"]
