<p align="center">
  <a href="http://nestjs.com/" target="blank"><img src="https://nestjs.com/img/logo-small.svg" width="200" alt="Nest Logo" /></a>
</p>


# Teslo API

1. Clonar proyecto
2. ```yarn install```
3. Clonar el archivo ```.env.template``` y renombrarlo a ```.env```
4. Cambiar las variables de entorno
5. Levantar la base de datos
```
docker-compose up -d
```

6. Levantar: ```yarn start:dev```

7. Ejecutar SEED 
```
http://localhost:3000/api/seed
```



# Production notes:
1. Comentar de la línea **20** a la **25** de ```app.module.ts```

2. Ejecutar
```
docker compose -f docker-compose.prod.yml build
docker compose -f docker-compose.prod.yml up
```
Al hacer cambios en un ```Dockerfile``` o levantar otro ```docker-compose```
También se recomienda hacer un build y un up.
En caso de tener errores se recomienda limpiar los volúmenes con ```docker compose down --volumes```

***IMPORTANTE:*** ```docker compose down --volumes``` Limpia toda la db.

Si es necesario se pueden limpiar las imágenes con ```docker image prune -a``` o ```docker image rm <id>``` según lo amerite

Este es un repo de prueba tomado del curso [Docker - Guía práctica de uso para desarrolladores](https://www.udemy.com/course/docker-guia-practica/) de Fernando Herrera.
[Repo original](https://github.com/Klerith/docker-teslo-shop)