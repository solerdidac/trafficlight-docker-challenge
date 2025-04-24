# 1.1.1 | Usar la imagen base "node:17.0-alpine3.14"
FROM node:17.0-alpine3.14

# 1.1.2 | Establecer el directorio de trabajo en "/app"
WORKDIR /app

# 1.1.3 | Copiar los archivos package.json y package-lock.json (si existe) al directorio de trabajo
COPY package*.json ./

# 1.1.4 | Instalar las dependencias
RUN npm install

# 1.1.5 | Copiar el archivo app.js al directorio de trabajo
COPY app.js ./

# 1.1.6 | Copiar el archivo index.pug a la carpeta views
RUN mkdir -p /app/views
COPY index.pug /app/views/

# 1.1.6 (actualizado) | Copiar el favicon.ico, que se encuentra en la raíz de la aplicación
COPY favicon.ico ./

# 1.1.7 | Exponer el puerto "80" (la app escucha en ese puerto)
EXPOSE 80

# 1.1.8 | Ejecutar el comando "node app.js" en tiempo de ejecución
CMD ["node", "app.js"]
