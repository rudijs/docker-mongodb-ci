meanr-docker-mongodb-ci
=======================

MongoDB Docker container for use in Jenkins CI [MEANR Full Stack](https://github.com/rudijs/meanr-full-stack) builds.

## Some Docker Utility Commands

List docker images

    sudo docker images

List all running containers

    sudo docker ps

List all containers ever created

    sudo docker ps -a

Clean up all non-running containers (free's up disk space)

    sudo docker ps -a -q | xargs sudo docker rm
