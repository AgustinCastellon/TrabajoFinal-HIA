# backend/Dockerfile
FROM node:18

# Configura el directorio de trabajo
WORKDIR /app

# Copia los archivos y dependencias
COPY package*.json ./

RUN npm install

# Copia el código fuente
COPY . .

# Exponer el puerto del backend
EXPOSE 3000

# Comando de inicio
CMD ["npm", "start"]
