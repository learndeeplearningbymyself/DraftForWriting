Docker Course

**Docker client** = **Docker CLI** 
----> **Docker server** 
-----> Image cache (will be checked by docker server before pull images from the **Docker hub**)

Our OS's model:

<img src="https://user-images.githubusercontent.com/43769314/78319510-49b56d80-75a2-11ea-83a8-6376e25cb7f9.png" width="720" />

Use the feature that is called **Name spacing** to segment your hard disk

<img src="https://user-images.githubusercontent.com/43769314/78319757-c8aaa600-75a2-11ea-9f68-2735decc324d.png" width="720" />

A container can be thinked like a process or a group of processes that have a grouping of resources specifically assigned to it

<img src="https://user-images.githubusercontent.com/43769314/78320743-23450180-75a5-11ea-824a-c00436cbdba6.png" width="720" />

FS: File system, Startup command will be executed immediately after container is created

<img src="https://user-images.githubusercontent.com/43769314/78320915-9b132c00-75a5-11ea-8dda-fde134ef6f0f.png" width="720" />

<img src="https://user-images.githubusercontent.com/43769314/78321321-98650680-75a6-11ea-8d78-f795a474ae28.png" width="720" />

> docker run <image> <command - override default Startup command of container>

### Container life cycle

> docker run = docker create + docker start

When we talk about **create container**, it's just a copy FS snapshot to "Hard drive segment for container" process. To **start container** we have to execute **Startup Command**

> docker start -a container_id

-a: to make docker watches for output from the container and print it out to your terminal

**build cache** is all images that you have pulled from docker hub

> docker system prune

> docker logs <container id>

> docker on Mac or Windows will be ran in the Virtual Linux environment

**Stop docker container**

- In case of **docker stop container_id**: we send a **SIGTERM** (Terminate signal) signal or message to the process (container), the running process inside of the container will receive **SIGTERM** message telling it essentially to shut down on its own time

**SIGTERM** is used any time that you want to stop a process inside of your container and shut the container down and you want to give that process inside there a little bit of time to shut itself down and do a litte bit of clean up

<img src="https://user-images.githubusercontent.com/43769314/78331887-e76c6500-75c1-11ea-973b-72c6256bcd8c.png" width="720" />

- In case of **docker kill container_id**: we issue a **SIGKILL** signal means **YOU HAVE To SHUT DOWN RIGHT NOW**, you do not get to do any additional work

Tips: 

> 10 seconds after you send **SIGTERM** signal if the container do not stop, Docker is going to automatically fall back to issue docker kill command

Every process that we create in the Linux environment has three communication channels attach to it:
- STDIN
- STDOUT
- STDERR

<img src="https://user-images.githubusercontent.com/43769314/78344543-7f287e00-75d7-11ea-9fae-e70b144b8d43.png" width="720" />

-i: attach our terminal's stuff to **CMD_LINE STDIN**
-t: show up result in pretty format

### Build our own docker-image

- **Docker Client (CLI)** will send your **dockerfile** to **Docker Server**, **Docker Server** will read it (line by line), after that publish your image

<img src="https://user-images.githubusercontent.com/43769314/78526995-bcc71a00-7816-11ea-88aa-6385b5e74262.png" width="720" />

With docker build command:

> docker build .
> docker build -f dockerfile_name . // -f: specify dockerfile

[.] symbol is the context (includes folders and files that you want to import into your image)

The build process in detail

1. Pulling base image
2. If we have **RUN** instruction in our Dockerfile, a **temporary container** is going to be created
3. The command of **RUN** will be executed as **temporary container**'s main process
4. After command stop, **temporary container** will be removed but before that happens, all FS snapshot of **temporary container** will be copied and be stored at **temporary image**
5. With **CMD**, we will look at previous created **temporary image**, create a very temporary container out of this and the command in **CMD** will be a primary process of new container. After that, remove temp container and create finally image

> Successfully built IMAGE_ID

**Using cache**

Docker build uses cache to build an image, but if we **change instructions's order**in Dockerfile, **cache is not going to be used**.

**Tagging an image**

tag convention: [DockerID]/[Repo/Project_Name]:[Version]

**Create　image from container**

With the following command

> docker commit -c "CMD"

**COPY** instruction

> COPY PATH_IN_YOUR_MACHINE/ PATH_IN_CONTAINER/

**PORT mapping**

Our docker container can by default make requests on its own behalf to the outside world

Docker run with port mapping

> docker run -p [LOCAL_HOST_PORT]:[CONTAINER_PORT] <image_name>

**WORKDIR instructions**

> WORKDIR /path/

Any following commands will be executed relative to this path in the container

**/usr/app** folder is the best place to put your application into it.

### Docker Compose

The containers that are created by **docker-compose** are automatically have the same networking

> docker run <image_name> === docker-compose up

> docker build . + docker run <image_name> === docker-compose up --build

> docker-compose up -d // detach mode

> docker-compose down

<img src="https://user-images.githubusercontent.com/43769314/78973546-1dbe5d00-7b4b-11ea-84be-41b3f05ecd58.png" width="720" />

> restart: value // in docker-compose.yml file
