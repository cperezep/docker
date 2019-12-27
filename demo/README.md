# Curso de Docker en Platzi

Ésta es una aplicación de ejemplo para el curso de Docker de Platzi por Guido
Vilariño.

Encuentra más información en https://platzi.com, suscríbete al curso y aprende
a usar Docker de manera profesional.

### App
docker build -t platziapp .
docker run -d --name app -p 3000:3000 --env MONGO_URL=mongodb://mongo-db:27017/test platziapp

### DB
docker run -d --name mongo-db mongo

### Network
docker network create --attachable mern-net

### Connect Apps
docker network connect mern-net mongo-db
docker network connect mern-net platziapp
