meanr-docker-mongodb-ci
=======================

MongoDB Docker image with no database persistance, used in continuous integration builds

## Pull the image (if you prefer to build your own see next step)

    sudo docker pull rudijs/docker-mongodb-ci
    
## Build Image

If you prefer to build the image instead of pulling from the public docker registry

    cd docker-mongodb-ci/
    sudo docker build -t <your-name>/docker-mongodb-ci .

Review the new image

    sudo docker images

## Using the MongoDB image

Run a mongodb-ci container (replace rudijs with <your-name> if you built your own docker image)

    sudo docker run -d -p 27017:27017 -name mongodb-ci rudijs/docker-mongodb-ci

Check the status

    sudo docker ps -a
    sudo docker logs mongodb-ci

## Some Docker Utility Commands

List all containers ever created

    sudo docker ps -a

Clean up all non-running containers (free's up disk space)

    sudo docker ps -a -q | xargs sudo docker rm
