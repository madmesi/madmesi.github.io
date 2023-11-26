---
title:  "What is Docker?"
categories: 
  - docker
  - code
last_modified_at: 2023-11-11T16:48:34-05:00
---

Docker is an open platform for developing, shipping, and running applications. It allows developers to build, package, and distribute their applications in a format called a container. This approach has gained popularity in recent years due to its portability, efficiency, and flexibility.

The technology works by creating a container image that contains all the dependencies needed for the application to run. This container can then be deployed on any system that has Docker installed, ensuring consistent behavior across different environments.

<figure class="align-center">
  <img src="{{ site.url }}{{ site.baseurl }}/assets/images/what-is-docker-blog-1.jpeg" alt="">
  <figcaption>Docker Containers desgined with hotpot.ai </figcaption>
</figure> 


# Some key features of Docker include:

Isolation: Docker containers are isolated from each other and from the host system, which enhances security and stability.
Lightweight: Containers consume fewer resources compared to virtual machines, which allows for efficient utilization of hardware resources.
Portability: Docker containers can be easily moved between different systems, simplifying application deployment and scaling.
Scalability: Docker makes it easy to create multiple containers from a single image, enabling applications to scale horizontally as needed.
Version Control: Docker allows for easy management of different versions of an application and its dependencies, improving development efficiency and stability.



# What happens after running docker run?

The Docker Engine will try to pull the image if it is not already available locally. If it can't find the image, it will raise an error and exit.

The Docker Engine will then create a new container using the specified image. It will also set up the container's environment according to the instructions provided in the Dockerfile.

If the Dockerfile contains a CMD instruction, the Docker Engine will execute the command specified in the CMD instruction. This command typically starts the application that the container is running.

The Docker Engine will also map any exposed ports of the container to the host machine's ports, as specified by the -p flag in the docker run command. This allows the container to communicate with the outside world.

The Docker Engine will keep the container running until the application running inside the container exits or the container is manually stopped using the docker stop command.

After the Docker Engine starts the container, it will monitor the container's state and take appropriate action based on the container's status. For example, if the container crashes or stops, the Docker Engine will automatically remove the container to free up system resources. Additionally, if the Docker Engine itself is stopped, it will stop all running containers as well.


```graph
    Docker looks for the image on this computer. --> Is it installed? --> if not, Docker searches Docker Hub for the image. --> Is it on Docker Hub? --> If Yes, Docker downloads the image. --> The image layers are installed on this computer. --> Docker creates a new container and starts the program. --> The container is running!
     id1([docker run]) --> Docker looks for the image on this computer.
```