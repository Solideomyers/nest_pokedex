<p align="center">
  <a href="http://nestjs.com/" target="blank"><img src="https://nestjs.com/img/logo-small.svg" width="200" alt="Nest Logo" /></a>
</p>

[circleci-image]: https://img.shields.io/circleci/build/github/nestjs/nest/master?token=abc123def456
[circleci-url]: https://circleci.com/gh/nestjs/nest

# Ejecutar en desarrollo

1. Clonar el repositorio
2. Ejecutar

```
npm install
```

3. Tener Nest CLI instalado

```
npm i -g @nestjs/cli
```

4. Levantar la base de datos

```
docker-compose up -d
```

5. Clonar el archivo **.env.template** y renombrar la copia a `.env`

6. Llenar las variables de entorno definidas en el `.env`

7. Ejecutar la aplicacion en dev:

```
npm run start:dev
```

8. Reconstruir la base de datos con la semilla

```
http://localhost:3000/api/v2/seed
```

### Stack usado

- MongoDB
- Nest

# Production Build

1. Crear el archivo `.env.prod`
2. Llenar las variables de entorno para produccion
3. Crear la nueva imagen

```
docker-compose -f docker-compose.prod.yaml --env-file .env.prod up --build
```

## Despliegue en Railway

![Deployed with Railway](https://img.shields.io/badge/Deployed%20with-Railway-black?style=for-the-badge&logo=railway)


La aplicación está actualmente desplegada en Railway.

### Pruebas con Postman

Bien puedes seguir los pasos de ```Production Build``` y tendras la aplicacion totalmente funcional.

Pero, tambien puedes probar el funcionamiento de la aplicación utilizando Postman. Simplemente agrega `/api/v2` al final del enlace del despliegue. 

Por ejemplo, para obtener todos los Pokémon, puedes usar el siguiente enlace:

```
https://nestpokedex-production-9614.up.railway.app/api/v2/pokemon
```