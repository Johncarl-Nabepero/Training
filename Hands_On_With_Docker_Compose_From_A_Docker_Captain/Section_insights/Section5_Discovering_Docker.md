## Section Insights

**Docker run hello-world**

- The Docker client contacted the docker daemon.

**Docker Images and Docker Container**

Echo command - Utility that comes with any linux like operating system.

`docker run -it alpine sh` This command very similar to the one docker recommends.

Alpine - Is very light weight in the next distribution.

**Difference between Docker Image and Docker Container**

- Docker images is a combination of a file system and parameters.

- Docker images doesn't have any state attach to it and once it is build it never change.

- Docker Container are immunable it means any changes that you made of running will be lost forever when you stop that container.

**Explaining the docker build process**

**2 ways to build docker Image**

1. Docker Commit - To run a docker container just like what i did in a previous lesson and once i am inside in my container i can commit changes.

2. Docker File - Is to use a thing of dockerfile as a blueprint recipe book for creating docker images.

`Notes:Docker Hub is Docker Registry`