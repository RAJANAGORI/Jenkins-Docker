# Jenkins with Docker
## To run the jenkins on docker, copy the below content and run. 

sudo docker container run --name jenkins-blueocean --detach --volume jenkins-data:/var/jenkins_home  --volume jenkins-docker-certs:/certs/client:ro  --publish 8080:8080 --publish 50000:50000 --restart=unless-stopped jenkinsci/blueocean
