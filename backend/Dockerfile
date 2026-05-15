FROM node:18-alpine

WORKDIR /app

# Copiamos dependencias
COPY package*.json ./
RUN npm install

# Copiamos todo el proyecto
COPY . .

# Exponemos el puerto de tu API
EXPOSE 3000

# EJECUTAMOS EL PUNTO DE ENTRADA CORRECTO
CMD ["node", "src/server.js"]
