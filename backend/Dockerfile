# 1. Usamos una imagen ligera de Node.js
FROM node:18-alpine

# 2. Creamos el directorio de trabajo
WORKDIR /app

# 3. Copiamos solo los archivos de dependencias para aprovechar la caché
COPY package*.json ./

# 4. Instalamos las dependencias
RUN npm install

# 5. Copiamos el resto del código (incluyendo index.js)
COPY . .

# 6. Exponemos el puerto que usa tu API (verifica si es el 3000 o 5000)
EXPOSE 3000

# 7. Comando para arrancar la aplicación
CMD ["node", "index.js"]
