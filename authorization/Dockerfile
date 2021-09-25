# Imagen base
FROM node:lts-alpine3.13

# Directorio de trabajo
WORKDIR /usr/src/app

# Instalacion de modulos (dependencias)
COPY package*.json ./
RUN npm install

# Copia de codigo fuente
COPY . .

# Exposicion de puertos
EXPOSE 3000

CMD [ "npm", "start" ]