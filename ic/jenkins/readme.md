# Jenkins 

## Info:

[See official repo](https://github.com/jenkinsci/jenkins)


## Build:

Basic build: 

```
docker build -t dperezcabrera/jenkins .
```

Custom jenkins version:

```
docker build -t dperezcabrera/jenkins --build-arg JENKINS_VERSION=alpine .
```

Create a shared network to run this container with others:

```
docker network create --driver bridge my_ci_network_test
```


## Usage:

```
docker run -v /var/run/docker.sock:/var/run/docker.sock -ti --name jenkins-alpine-alonsoir --publish 8080:8080 --publish 50000:50000 --network my_ci_network_test dperezcabrera/jenkins
```

# Disclaimer:
I will use this container to learn more about DevOps, so i will have to install another software, like openssh, ansible. Thank you @dperezcabrera for the starting point.

