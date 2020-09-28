# Jenkins with Docker
## To run the jenkins on docker, copy the below content and run. 

sudo docker container run 
--name jenkins-blueocean \
--detach \
--network jenkins \
--env DOCKER_HOST=tcp://docker:2376 \
--env DOCKER_CERT_PATH=/certs/client \
--env DOCKER_TLS_VERIFY=1 \
--volume jenkins-data:/var/jenkins_home  --volume jenkins-docker-certs:/certs/client:ro 
--publish 8080:8080 \
--publish 50000:50000 \
--cap-add NET_ADMIN \
--device /dev/net/tun \
--user root \
--restart=unless-stopped 
jenkinsci/blueocean
