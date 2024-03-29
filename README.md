# Red social :busts_in_silhouette:

![Diagrama](./src/img/red-social.jpg)


Bienvenido a la documentación de la API de mi red social. Es mi quinto proyecto desarrollado en GeeksHubs Academy en el cual se ponen en práctica habilidades de desarrollo backend con JavaScript y MongoDB Compass.

## Tabla de contenido :page_with_curl:

- [Tecnologías.](#tecnologías-star2)
- [Diagrama.](#diagrama-bd-book)
- [Instalación en local.](#instalación-en-local-gear)
- [Implementación en vivo. ](#implementación-en-vivo)
- [Usuarios modelo](#usuarios-modelo-pouting_face)
- [Endpoint.](#endpoints-dart)
- [Autor.](#autor-curly_haired_man)
- [Agradecimientos.](#agradecimientos)

### Tecnologías :star2:

<img src="https://img.shields.io/badge/JAVASCRIPT-000000?style=for-the-badge&logo=javascript&logoColor=yelow" alt="JS" /> <img src="https://img.shields.io/badge/MongoDB-229954?style=for-the-badge&logo=mongodb&logoColor=white" alt="MongoDB" /> <img src="https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white" alt="Express.js" /> <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker" /> <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white" alt="Node.js" /> <img src="https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=jsonwebtokens&logoColor=white" alt="JWT" /> <img src="https://img.shields.io/badge/{/}  fl0-0B615E?style=for-the-badge&logo=postma&logoColor=white" alt="FL0" />


### Diagrama BD :book:

![Diagrama](./src/img/diagrama.jpg)

### Instalación en local :gear:

**1. Clona el repositorio.**
````
git clone https://github.com/VictorBlasco5/Proyect-backend-2
````
**2. Instalar las dependencias.**
````
$ npm install
````
**3. Poner en marcha el servidor.**
````
$ npm run dev
````

**4. Ejecutar los seeders.**
````
$ npm run seed
````
### Implementación en vivo

https://proyect-backend-2-dev-hbfk.2.us-1.fl0.io


### Usuarios modelo :pouting_face:
#### User
````
Nombre: user
Email: user@user.com
Contraseña: 123456
````
#### Admin
````
Nombre: admin
Email: admin@admin.com
Contraseña: 123456
````
#### Superadmin
````
Nombre: super_admin
Email: super_admin@super_admin.com
Contraseña: 123456
````

### Endpoints :dart:
##### Autenticación
- `POST /api/auth/register` - **Registrar nuevo usuario.**
Pasamos los siguientes datos por el body. Ejemplo:
````
{
   "name": "nombre",
   "email": "email@email.com",
   "password": "contraseña"
}
````
![Body](./src/img/body.jpg)

- `POST /api/auth/login` - **Inicio de sesión.**
Pasamos los siguientes datos por el body. Ejemplo:
````
{
  "email": "email@email.com",
  "password": "contraseña"
}
````
##### Usuarios

- `GET /api/users` - **Ver todos los usuarios.** Pasamos el token del propio usuario. 

![Token](./src/img/token.jpg)

- `GET /api/users/profile` - **Ver perfil de usuario.**
Pasamos el token del propio usuario.

- `PUT /api/users/profile` - **Modificar datos del perfil.**
Pasamos el token del propio usuario y los datos que queramos modificar por el body. Ejemplo:
````
{
  "name": "Nombre",
  "email": "email@email.com"
}
````


- `DELETE /api/users/{id}` - **Eliminar usuario. (Solo el superadmin)**
Pasamos el token del superadmin y el id del usuario a eliminar por parámetro.


![Parámetro](./src//img/parámetro.jpg)

- `PUT /api/users/{id}/role` - **Modificar el role del usuario. (Solo el superadmin)**
Pasamos el token del superadmin y el id del usuario a modificar por parámetro.


##### Posts
- `POST /api/posts` - **Crear post.**
Pasamos el token del usuario y los siguientes datos por el body. Ejemplo:
````
{
  "description": "texto"
}
````

- `DELETE /api/posts/{id}` - **Eliminar un post.**
Pasamos el token del creador del post y el id del post a eliminar por parámetro.

- `PUT /api/posts` - **Actualizar mi post.**
Pasamos el token del creador del post y por el body los datos que deseemos actualizar. Ejemplo:
````
{
  "description": "texto 2"
}
````
- `GET /api/posts/own` - **Ver todos mis posts.**
Pasamos el token del usuario para ver sus posts.

- `GET /api/posts` - **Ver todos los posts.**
Pasamos el token del usuario para todos los posts.

- `GET /api/posts/{id}` - **Ver un post.**
Pasamos el token del usuario y el id del post por parámetro.

- `GET /api/posts/users/{user-id}` - **Ver todos los posts de un usuario.**
Pasamos el token del usuario y el id del usuario que queremos ver por parámetro.


##### Likes
- `PUT /api/posts/like/{id}` - **Dar y quitar like a un post**

Pasamos el token del usuario y el id del post por parámetro.



### Autor :curly_haired_man:
- **Víctor Blasco** - Project Developer.
   - [GitHub](https://github.com/VictorBlasco5)

### Agradecimientos 
- Agradecimiento a GeeksHubs Academy por su implicación en mi aprendizaje.