# 1. Imagen base de Node
FROM node:18-alpine

# 2. Directorio de trabajo
WORKDIR /app

# 3. Copiar archivos de dependencias
COPY package*.json ./

# 4. Instalar librerías
RUN npm install

# 5. Copiar todo el código (incluyendo la carpeta src)
COPY . .

# 6. Exponer el puerto del backend
EXPOSE 3000

# 7. EJECUTAR EL ARCHIVO CORRECTO (src/server.js)
CMD ["node", "src/app.js"]
