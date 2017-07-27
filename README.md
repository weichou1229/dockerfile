# dockerfile
my docker file


## run jenkins 

```
JENKINS_DATA=/path/to/jenkins-data
MAVEN_HOME=/path/to/maven-repos
           
docker rm -f jenkins

docker run --restart=always -d --name jenkins -p 8080:8080 -p 50000:50000 -u root \
    -v $JENKINS_DATA:/var/jenkins_home -v $MAVEN_HOME:/root/.m2 \
    -v /var/run/docker.sock:/var/run/docker.sock \
    weichou/jenkins

```