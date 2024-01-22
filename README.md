# Javvy
## Javvy repository for Issue tracking, Instructions, and Releases


Javvy is a self-hosted media web app designed for JAV collectors.


The application leverages the following technologies:
* FFmpeg - to generating thumbnail
* MongoDB - database for storing all movie data
* Flask server - facilitating communication between the front-end and back-end
* Next.js app - serving as the front-end user interface
* Docker - for deploying the app

### Installation:
Given that the installation and setup of the aforementioned technologies can be challenging, Javvy can currently be installed as a Docker container. Docker, similar to a "virtual machine," enables users to install apps in containers managed by Docker, separate from their local machines. Containers can be easily removed and installed.

1. Download and Install [docker](https://www.docker.com/products/docker-desktop/) in your machine. [systems supported mac,win,linux](https://docs.docker.com/get-docker/#supported-platforms)
2. Download Javyy.zip
3. Unzip Javyy.zip and edit the compose.yaml file to set your configurations (instructions inside file)
4. Open terminal inside Javvy folder and run the folowing commands  <br/>
  `docker load < javvyserver.tar && docker load < javvyapp.tar` <br/>
  `docker compose up -d`
8. Done! Open up your browser and enter [http://localhost:3000](http://localhost:3000)
