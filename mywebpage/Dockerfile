# Imagen base
FROM node:lts-alpine3.13 as build

# Directorio de trabajo
WORKDIR /usr/local/app

# Copia de codigo fuente
COPY ./ /usr/local/app/

# Instalando dependencias
RUN npm install

# Construccion de la aplicacion
RUN npm run build

# Imagen base final
FROM nginx:alpine

# Copiamos la construccion de la aplicacion
COPY --from=build /usr/local/app/dist/mywebpage /usr/share/nginx/html

# Exponemos nuestro puerto
EXPOSE 80