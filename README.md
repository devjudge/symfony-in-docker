# symfony-in-docker

PROJECT START STEPS:

    Pre-requisites:
    1. php must be installed
    2. Composer must be installed (https://getcomposer.org/download/)

    Steps:
    1. To run this application, do the following:
        1.a. Go to the project root directory.
        1.b. Run the following commands in the terminal/command line to build the app:
            - composer install
        1.c. Run the following command(s) in the terminal/command line to run the app:
            - php -S 127.0.0.1:8000 -t public

    2. Go to http://127.0.0.1:8000/ in your browser to view it.


DOCKER START STEPS:

    Pre-requisites:
    1. Docker is installed (http://console.codejudge.io/setup)

    Steps:
    1. Build the docker image:
        1.a. Go to the project root directory.
        1.b. Run the following command(s) in the terminal/command line:
            - docker build -t symfony-app .

    2. Run the image in a container (Make sure port 8080 is available):
        2.a. Run the following command(s) in the terminal/command line:
            - docker run -i -p 8000:8000 symfony-app
        2.b. Check the logs for any errors.

    3. Go to http://127.0.0.1:8000/ in your browser to view it.

DOCKER STOP STEPS:

    Steps:
    1. Run the following commands:
        - docker ps
    2. Copy the container id and run the below command:
        - docker stop <container_id>
        - docker system prune

DOCKER LOGS:

    Steps:
    1. Run the following commands(s):
        - docker ps
    2. Copy the container id and run the below command:
        - docker logs <container_id>

DOCKER REMOVE CONTAINER:

    Steps:
    1. Run the following command(s):
        - docker ps
    2. Copy the container id and run the below command:
        - docker rm <container_id>
        - docker system prune

DOCKER REMOVE IMAGE:

    Steps:
    1. Run the following command(s):
        - docker ps
    2. Copy the image id and run the below command:
        - docker rmi <image_id>
        - docker system prune
