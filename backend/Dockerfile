FROM node:20-alpine AS build
WORKDIR /app
COPY package*.json ./
RUN npm install --only=production

FROM node:20-alpine
WORKDIR /app
RUN addgroup -S appgroup && adduser -S appuser -G appgroup
COPY --from=build /app/node_modules ./node_modules
COPY . .
USER appuser
EXPOSE 3001
CMD ["node", "src/server.js"]