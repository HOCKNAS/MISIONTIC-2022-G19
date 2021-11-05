
# MISIONTIC-2022-G19 ====================

    Mision TIC 2022 Grupo Habilitación
    
    - Santiago Chacón Sora santiago.chacon99@gmail.com de Boyacá, Rol / Developer
    - Lissette Sierra Bonilla lizzethe19@gmail.com de Bogota, Rol / Scrum Master
    - Alejandro Granada Ospina collerx100pre@gmail.com de Medellin, Rol / Produect Owner



## TRELLO ===============================

 [FLUJO DE TRABAJO SPRINT 6 SCRUM](https://trello.com/b/y92EmE5m)



## BACKEND ==============================

El backend se desarrolló utilizando un patrón de diseño MVC (Modelo - Vista - Controlador)

Se realizó utilizando ExpressJS

Se requiere configurar las siguientes variables:

`PORT` El puerto de escucha para las conexiones.

`DATABASE_URL` URL de la base de datos de MONGO.

`DATABASE_NAME` Nombre de la base de datos.



## AUTENTICACIÓN ========================

El proceso de autenticación se hizo con AUTH0 y requiere configurar una regla, la cual relacionamos a continuación:

```
function (user, context, callback) {
  const namespace = 'http://localhost';
  
  let idTokenClaims = context.idToken || {};
  let accessTokenClaims = context.accessToken || {};
  
  accessTokenClaims[`${namespace}/userData`] = user;
  
  context.idToken = idTokenClaims;
  context.accessToken = accessTokenClaims;
  
  callback(null, user, context);
}

```


## API =================================

Se utilizan los métodos GET, POST, DELETE y PATCH para interactuar con el API.



## SCRIPTS =============================


Para correr el proyecto es necesario seguir los siguientes pasos:

`git clone git@github.com:HOCKNAS/MISIONTIC-2022-G19.git`

`cd MISIONTIC-2022-G19`

`cd backend`

`yarn`

`yarn start`



## FRONTEND =============================

Este proyecto fue realizado utilizando React JS. Se crearon diferentes componentes según las necesidades de diseño de la página.

Hay diferentes páginas, entre las cuales están:

- VENTAS
- PRODUCTOS
- USUARIOS

Y sus respectivas funciones de CRUD.



## SCRIPTS ===============================

`git clone git@github.com:HOCKNAS/MISIONTIC-2022-G19.git`

`cd MISIONTIC-2022-G19`

`cd frontend`

`yarn`

`yarn start`


