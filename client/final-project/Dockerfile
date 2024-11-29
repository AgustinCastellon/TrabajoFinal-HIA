FROM node:18

# Establecer el directorio de trabajo
WORKDIR /app

# Copiar los archivos necesarios
COPY package*.json ./

# Instalar dependencias
RUN npm install

# Copiar el código fuente
COPY . .

# Exponer el puerto del servidor de desarrollo Angular
EXPOSE 4200

# Iniciar Angular en modo desarrollo
CMD ["npm", "start"]


