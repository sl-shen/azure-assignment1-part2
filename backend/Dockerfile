FROM node:18-alpine

# Create app directory
WORKDIR /app

# Copy package.json and package-lock.json
COPY package*.json ./

# Install npm dependencies
ENV NODE_ENV=production
RUN npm ci --only=production

# Bundle app source
COPY . .

# Expose port
EXPOSE 8080

# Start application
CMD [ "node", "index.js" ]