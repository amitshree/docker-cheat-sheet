
#### Pull a docker image
    
###### To pull an un-official image
````
docker pull user/repository:tag

````
Example: amitshree/hello-world:my_custom_tag
###### To pull an official image
````
docker pull official_image:tag
````

#### Run a container

````
docker container run --name="name_of_the_container" official_image:tag
docker container run --name="name_of_the_container" user/repository:tag
````
Example: docker container run --name hello_world amitshree/hello-world:my_custom_tag

#### Remove docker container
````
docker container rm name_of_the_container // remove a stopped container
docker container rm -f name_of_the_container // forcfully remove a running or stopped container
````

#### Remove all docker containers
````
docker container rm $(docker container ls -qa) // remove all stopped containers
docker container rm -f $(docker container ls -qa) // forcefully remove all running and stopped containers
````

#### Remove docker image
````
docker rmi amitshree/hello-world:my_custom_tag // Remove a docker image which has no running containers from it
docker rmi -f amitshree/hello-world:my_custom_tag // Forcefully remove a docker image

````

#### Push an image to hub.docker.com 

Login to your docker repository first using command
````
docker login // To login to hub.docker.com
````

Then push your image
````
docker push amitshree/hello-world:my_custom_tag
````