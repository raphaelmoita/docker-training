# DOCKER

### 1st day

> docker info
> docker inspect <image-name>
  
  https://docs.google.com/document/d/1O2YDR0RIGpcgjqJyUxk4NgxP7WAzfBP4V0hnyaFTlLM/edit
  
  TASK-1
  
1. docker run -d -p 80:80 docker/getting-started
When started go to http://localhost and follow instructions

2. docker run docker/whalesay cowsay boo
Analyze the source code of the docker image. Check what is cowsay in Unix and what steps were necessary to replace it with whalesay. 

3. docker run -it --rm docker/doodle:halloween2019
Play the game and discover all possibilities. Analyze its source code line by line and try to understand everything. 

4. Watch Docker in 100 seconds: https://www.youtube.com/watch?v=Gjnup-PuquQ 


### 2nd day

> docker ps
> docker kill <hash>
  
 sudo docker run -d --name jenkins-instance --publish-all jenkins/jenkins:lts
 
 # Exec & Run
 
 Docker run is for creating containers. It is important to differentiate it from exec , which is used to interact with containers that are already running. The -it runs Docker interactively (so you get a pseudo-TTY with STDIN). The --rm causes Docker to automatically remove the container when it exits.
 
 # Exec & attach
 
 docker exec executes a new command / create a new process in the container's environment, while docker attach just connects the standard input/output/error of the main process(with PID 1) inside the container to corresponding standard input/output/error of current terminal(the terminal you are using to run the command)
