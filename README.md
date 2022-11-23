# Libreta de Contactos

---
LibretaContactos es una aplicación web que permite gestionar una Libreta de Contactos en un sistema. Esta gestión está relacionada con permitir, eliminar, crear, consultar y editar (CRUD) de la Libreta.

#Tecnologias 

---
-Lenguaje javascript
-Backend node.js
-Frontend con vue.js 
-ORM a cargo es Sequelize con una base de datos mysql.
-Postman 


## Instalación
---
-Descarga e instala node js
-Librería Express (para crear servidor)
-Librería Body-parser (para trabajar con las peticiones POST)
-Librería Sequelize ( trabaja con MySql, Maria DB, PostgreSQL)
-Librería mysql2 
-Librería Nodemon (Para tener iniciada la aplicación y observar los cambios)





## Ejecución
---
Una vez instalado Node js y las librarías correspondientes, para la correcta ejecución del sistema se debe abrir la terminal de comandos con permisos de administrador, especificar la ruta del proyecto y aplicar el comando:

    ```bash
    node index.js 
    ```

ó 

  ```bash
    nodemon index.js 
    ```

se utiliza el metodo Listen para iniciar el servidor el cual por defecto utiliza el puerto 3000 (servidor local) para escuchar la conexión cifrada (http://localhost/).



## Configuración
---
Se requiere crear una base de datos en mysql para posteriormente llenarla con los datos de contactos.

**SERVIDOR y BASE DE DATOS**
El sistema utiliza por defecto el puerto 3000, este a su vez puede ser modificado en el archivo  [/index.js](https://github.com/LuzKntillo/Lib_Contactos/blob/main/back/index.js) del proyecto

> Fragmento de código: 

 ```js
 app.listen(3000,()=>{
        console.log('Server start');
    });
});

  modificar  3000 por el puerto deseado
```

>La configuración  de la conexion con la base de datos se encuentra en el  archivo [db.js](https://github.com/LuzKntillo/Lib_Contactos/blob/main/back/db.js) del proyecto, en la cual se debe seguir la siguiente estructura:

```js
 const sequelize = new Sequelize('base de datos','usuario','contraseña',{
    host:'host',
    dialect: 'mysql'
});

```

---
>En caso de configurar el puerto y el servidor dirigirse al archivo [/main.js](https://github.com/LuzKntillo/Lib_Contactos/blob/main/front/front/main.js) y cambiar la url con las respectivas modificaciones

```js

    url='http://localhost:3000/api/contactos/';

```