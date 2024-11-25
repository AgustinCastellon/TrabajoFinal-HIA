# Usa una imagen de Node.js
FROM node:18

# Establece el directorio de trabajo
WORKDIR /app

# Copia los archivos de configuración del proyecto Angular
COPY package*.json ./

# Instala Angular CLI globalmente y las dependencias del proyecto
RUN npm install -g @angular/cli
RUN npm install

# Copia el código fuente
COPY . .

# Exponer el puerto en el que el servidor de Angular funciona (4200 por defecto)
EXPOSE 4200

# Comando para iniciar el servidor
CMD ["npm", "start"]

