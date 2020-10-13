The Maven build lifecycle is composed of Maven phases. Each phase is a sequense of goals, and each goal is responsible for a specific task.
When we run a phase – all goals bound to that phase are executed in order.

Here are some of the phases and default goals bound to them:
	compiler:compile – the compile goal from the compiler plugin is bound to the compile phase
	compiler:testCompile is bound to the test-compile phase
	surefire:test is bound to test phase
	install:install is bound to install phase
	jar:jar and war:war is bound to package phase


Create docker group:
$ groupadd docker

Add your user to the docker group:
$ usermod -aG docker $USER

Activate changes to groups:
$ newgrp docker

Check the docker version:
$ docker --version

Run hello-world Docker Image (usually used to test that the docker is working properly):
$ docker run [OPTIONS] hello-world
Options:
 --rm 			Automatically remove the container when it exits
 -P, --publish		Publish all exposed ports to random ports
 -d, --detach		Run container in background and print container ID (run in mode deamon)
 --name		Specifies a name with which you can refer to your container in subsequent commands.

List the images that were downloaded into the machine:
$ docker image ls

List the containers (active containers included) spawned by the images:
$ docker ps -a

Stop one or more running containers:
$ docker stop CONTAINER ID | IMAGE

$ docker rm --force CONTAINER
The --force option stops a running container, so it can be removed. If you stop the container running with docker stop CONTAINER first, then you do not need to use --force to remove it.

Dockerfiles describe how to assemble a private filesystem for a container, and can also contain some metadata describing how to run a container based on this image.
