# Launch instructions
This brief readme file contains brief instructions on how to launch and test Enhancify locally.

## With docker
Make sure to install docker engine, and run the following command from the root folder of the project (where this file is located)

docker compose up --build

## Without docker

This option is preferrable if you want to test the components (redis, backend, frontend) separately. 
Below are the commands you need to run to make it work.

### Backend

Navigate to the directory with "main.py" file (/backend/app)
Open the terminal from there

#### Requirements
(One-time only)
Make sure to setup all neccessary dependencies from requirements.txt file by running
------------
pip install -r requirements.txt
------------

#### Launching the server

Run the following command:
-------------
uvicorn main:app --reload --port 3000
-------------

### Frontend

Navigate to the "frontend" directory and open the terminal from there

### Installing necessary dependencies

To make sure you have all packages installed run:

---------------
npm run build
-------------

#### Launching frontend

To start the frontend run the following command:

-------------
npm run dev
-------------

### Redis

You'll have to run redis as a separate docker container. So to set it up you'll have to configure a Redis image inside of docker, following this tutorial:
https://redis.io/docs/latest/operate/oss_and_stack/install/install-stack/docker/


