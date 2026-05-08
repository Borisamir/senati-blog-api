# SENATI Blog API
API REST para gestión de blog personal (autores y artículos).

## Tecnologías
- Node.js + Express
- MongoDB + Mongoose
- REST API

## Instalación
npm install
npm run dev
Variables de entorno (.env)
text
PORT=3000
MONGODB_URI=mongodb://127.0.0.1:27017/senati_blog
Endpoints
Autores (/api/authors)
Método
Endpoint
Descripción
GET
/api/authors
Listar autores
GET
/api/authors/:id
Obtener autor
POST
/api/authors
Crear autor
PUT
/api/authors/:id
Actualizar autor
DELETE
/api/authors/:id
Eliminar autor

Artículos (/api/posts)
Método
Endpoint
Descripción
GET
/api/posts
Listar artículos
GET
/api/posts/:id
Obtener artículo
GET
/api/posts/author/:authorId
Artículos por autor
POST
/api/posts
Crear artículo
PUT
/api/posts/:id
Actualizar artículo
DELETE
/api/posts/:id
Eliminar artículo

Ejemplos de peticiones
Crear autor
curl -X POST http://localhost:3000/api/authors \
  -H "Content-Type: application/json" \
  -d '{"name":"Gabriel García Márquez","email":"gabo@email.com","bio":"Escritor colombiano"}'
Crear artículo
curl -X POST http://localhost:3000/api/posts \
  -H "Content-Type: application/json" \
  -d '{"title":"Cien años de soledad","content":"Análisis de la obra...","author":"ID_DEL_AUTOR","tags":["literatura","realismo"]}'
Autor
Estudiante SENATI - Desarrollo Fullstack
