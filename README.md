# Maven image with Docker-in-Docker

Image for use in ci/cd environments.


## Usage
bind socket mode

* Docker  
```
docker run --rm -v /var/run/docker.sock:/var/run/docker.sock -v ~/.m2:/root/.m2 fobbyal/maven-dind docker ps
```

* Maven  
```
docker run --rm -v /var/run/docker.sock:/var/run/docker.sock -v ~/.m2:/root/.m2 fobbyal/maven-dind mvn -v
```

* Maven  
```
docker run --rm -v /var/run/docker.sock:/var/run/docker.sock -v ~/.m2:/root/.m2 fobbyal/maven-dind java -version
```
