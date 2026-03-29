FROM node:20-alpine

# Set working directory
WORKDIR /app

# Copy package files
COPY package.json package-lock.json ./

# Install dependencies
RUN npm install

# Copy app code
COPY . .

# Build app code
RUN npm run build

# Expose frontend port
EXPOSE 3000

# Serve with npx serve
CMD ["npx", "serve", "-s", "build", "-l", "3000"]
# CMD ["npm", "run", "dev"]
