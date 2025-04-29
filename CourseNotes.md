# Image VS Container
1. An image is the application we want to run.
2. A container is an instance of that image running as a process.
3. You can have many containers running off the same image.
4. Docker's default image "registry" is called _Docker Hub_.

```docker container run --publish 80:80 nginx```
1. Downlaoded image 'nginx' from Docker hub.
2. Started a new container from that image.
3. Opened port 80 on the host IP.
4. Routes that traffic to the container IP, port 80.  

**NOTE:** You'll get a _bind_ error if teh left number (host port) is being used by anything else, even another container. You can use any port you want on the left, like 8080:80 or 8888:80, then use localhost:8888 when testing.