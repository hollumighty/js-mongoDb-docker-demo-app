## demo app - developing with Docker

This demo app shows a simple user profile app set up using 
- index.html with pure js and css styles
- nodejs backend with express module
- mongodb for data storage


#### To start the application using docker compose

START BY CONFIGURING THE DATABASE

- pull the mongodb official image from dockerhub
- pull the mongodb official image from dockerhub

- Run mongodb and mongo express container to make the  mongodb database available for our application and to connect the mongo express with the mongodb container
- connect both containers using docker compose from a docker-compose file

- start mongodb and mongo-express

    docker-compose -f docker-compose.yaml up
    
_You can access the mongo-express under localhost:8080 from your browser_
    
= in mongo-express UI - create a new database "my-db"

- in mongo-express UI - create a new collection "users" in the database "my-db"       



-START THE NODEJS APP
    
start node server 

    npm install
    node server.js
    
- access the nodejs application from browser 

    http://localhost:3000


- create a dockerfile for the app
- build the nodejs app image from the dockerfile
- run the container and push it to docker repository



- TO START THE THREE CONTAINERS AT ONCE
add the nodeJs container to the docker-compose.yaml file
- docker-compose -f docker-compose.yaml up


- DOCKER VOLUME
- For data persistency, to avoid loss of data after restarting the containers
- use docker volume in the docker compose file.