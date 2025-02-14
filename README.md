<p align="center">
  <a href="http://nestjs.com/" target="blank"><img src="https://nestjs.com/img/logo-small.svg" width="120" alt="Nest Logo" /></a>
</p>

# Ejecutar en desarrollo

1. Clonar el repositorio
2. Ejecutar

```
npm i
```
3. Tener instalado Nest CLI instalado
```
npm i -g @nestjs/cli
```
4. Levantar la base de datos
```
docker-compose up -d
```
5. Clonar el archivo __.env.example__
```
cp .env .env.example
```
6. Llenar las variables de entorno en el __.env__
7. Ejecutar la aplicación en dev
```
npm run start:dev
```
8. Reconstruir la base de datos con el seed
```
GET: http://127.0.0.1:3000/api/v2/seed
```

## Stack utilizado
* MongoDB
* Nestjs

# Production build
1. Crear el archivo ```.env.prod```
2. Llenar las variables de entorno de prod
3. Crear la nueva imagen
```
docker-compose -f docker-compose.prod.yaml --env-file .env.prod up --build
```