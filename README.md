## Crear imaen
docker build -t render-auto:1 .
## Crear contenedor
docker run --name render-auto-container --rm -d -p 3001:3000 render-auto:1