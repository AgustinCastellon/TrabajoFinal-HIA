# Usa la imagen oficial de Node.js como base para compilar
FROM node:18 AS builder
WORKDIR /app

# Copia los archivos de la aplicación e instala dependencias
COPY package*.json ./
RUN npm install
COPY . .

# Construye la aplicación Angular para producción
RUN npm run build --prod

# Usa una imagen ligera de Nginx para servir los archivos
FROM nginx:alpine
COPY --from=builder /app/dist/final-project /usr/share/nginx/html

# Expon el puerto que usa Nginx
EXPOSE 80

# Comando para iniciar Nginx
CMD ["nginx", "-g", "daemon off;"]

