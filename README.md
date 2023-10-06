# Dockerized-React-Node-Mongo-Simple-Application

First of all, you have to install docker into your local machine

Create a docker network [hint: use network goals-net as the network name]
Then run
docker create network goals-net

Database
Pull the MongoDB image from the Docker Hub.
Then run
docker run --name mongodb --rm --network goals-net -v goals:/data/db -d mongo

Backend
Go inside the backend folder
Then run
Docker build -t <any-tag-name-you-like>
docker run --name <name-for-container> -v <local-machine-absolute-path-for-backend-folder>:/app -v node_modules:/app/node_modules -v logs:/app/logs --rm --network goals-net -p 81:80 <tag-name-you-used-on-pervious-command>

Frontend
Go inside the frontend folder
Open Dockerfile
if you change the port of the backend bind to your local machine, then you have to change the value of LOCAL_DOMAIN variable
Then run
Docker build -t <any-tag-name-you-like>
docker run --name <name-for-container> -v <local-machine-absolute-path-for-frontend-src-folder>:/app/src -v node_modules:/app/node_modules --rm --network goals-net -p 3000:3000 -it <tag-name-you-used-on-pervious-command>

