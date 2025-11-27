# backend/Dockerfile
FROM node:18-alpine

WORKDIR /app

# Install production dependencies only
COPY backend/package*.json ./
RUN npm ci --only=production

# Copy rest of the backend code
COPY backend/ .

ENV PORT=5000
EXPOSE 5000

# If your entrypoint is server.js or index.js change below accordingly
CMD ["node", "index.js"]
