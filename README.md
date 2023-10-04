# Dockerized-React-Node-Mongo-Simple-Application

Backend
Go inside the backend folder
Then run
Docker build -t <any-tag-name-you-like>
docker run --name <name-for-container> -v <absolute-path-for-backend-folder>:/app -v node_modules:/app/node_modules -v logs:/app/logs --rm --network goals-net -p 81:80 -it <tag-name-you-used-on-pervious-command>

Frontend
Go inside the frontend folder
Open Dockerfile

Then
Docker build -t <any-name-you-like>

Then run
docker run --name goals-frontend -v <absolute-path-for-frontend-src-folder>:/app/src --rm --network goals-net -p 3000:3000 -it goals-react

Then your 

