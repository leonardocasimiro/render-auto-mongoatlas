# Bootcamp Backend III - [Documental] Módulo 5 - Cloud – Laboratorio
## _render-auto-mongoatlas_
## Introducción

> Para esta práctica se sube a render la rest API de la practica anterior, la 4. Pero en un contenedor de docker
Para ello hemos hecho un repositorio "render-auto-mongoatlas". A pesar del nombre, modificando una variable de entorno podemos pasar de datos mock a datos en mongo Atlas
![Alt text](./img/mongoAtlas.jpg)

Repo:
- https://github.com/leonardocasimiro/render-auto-mongoatlas

El enlace de render 
- https://render-auto-mongoatlas.onrender.com

Si se chequea el enlace de render, este tirará de los datos subidos en Mongo Atlas.
https://render-auto-mongoatlas.onrender.com/api/houses

![Alt text](./img/render1.JPG)


Si deseas ver datos mock, debes cambiar la variable de entorno en render
![Alt text](./img/variables_entorno.jpg)

## Acciones

> Se crea en render un WEB SERVICE. Basado en Docker. A este render se le indica el repo, region de alojamiento. Repositorio y rama de este.

> Importante, en los settings hay que indicar el Dockerfile

> Dockerfile. Es aqui donde indicamos que se baje el node determinado para funcionar y los comandos 
#### Hacemos el install y el build según se indica en el Dockerfile
RUN npm ci

RUN npm run build

> Al subir el repo a gitHub y como está sincronizado con este, render lo hará de forma automatica (se lo hemos indicado así) un Deploy.
Este deploy consiste en:
- Sincronizarse, de hecho es lo que activa el deploy
- Ejecuta los pasos de Dockerfile.


## end Points
Tiene los siguientes end points:

Get para consultar todos las casas

https://render-manual-mock.onrender.com/api/houses

Get para consultar por id

https://render-manual-mock.onrender.com/api/houses/65624450bec208d2830a55dc

Post para añadir una casa. Se puede usar postman agregando la casa en el body con   formatoJSON

http://localhost:3000/api/houses/

son los end points del modulo 4. Los no GET necesitamos postman …..

Ejemplo PATCH
![Alt text](./img/patch.JPG)

Ejemplo POST
![Alt text](./img/post.JPG)
