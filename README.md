## Crear imaen
docker build -t render-auto:1 .
## Crear contenedor
docker run --name book-container --rm -d -p 3001:3000 book-store-app:1