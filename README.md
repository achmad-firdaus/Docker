# Docker <img src="https://raw.githubusercontent.com/MartinHeinz/MartinHeinz/master/wave.gif" width="30px">
All Abound Docker

#### LIST
- [Help 👻](#introduction-)
- [Mysql 👻](#mysql-)
- [OS 👻](#os-)
- [Log 👻](#log-)
- [Dockerfile 👻](#dockerfile-)
- [Delete 👻](#delete-)

#### INTRODUCTION 👻

    docker images   // check images installed
    docker images -a   // check history images installed
    
    docker ps   // check run container
    docker ps -a    //check hostory run container stoped
    
    docker [stop/start/restart] [container image/ container name]   // stop run container
    
    -d  // run in background

#### MYSQL 👻

    sudo docker run --name=[name container] -p [local port]:[docker port] [option] [image]
    sudo docker run --name=MySql -p 33061:3306 -e MYSQL_ROOT_PASSWORD=1  mysql
    
    sudo docker exec -it MySql2 mysql -uroot -p // enter in mysql

#### OS 👻

    sudo docker exec -it [container name] bash

#### LOG 👻

    sudo docker logs [option] [name container]
    sudo docker logs -f apache-php56

#### DOCKERFILE 👻
### Build My Dockerfile

    sudo docker build -t [repo name]:[tag name] -f [filename] [directory filename]
    sudo docker build -t bionic_php56:v1 -f dockerfileBionicPhp56 /var/www/html/php56/
    
### RUN My DockerFile

    sudo docker run -it --name [container name] -v [local folder:docker folder] [image]
    sudo docker run -it --name bionicphp56 -v /var/www/html/php56:/var/www/html 99918e1d6e64

#### DELETE 👻
- Delete Image:

      sudo docker image rm [image]
      sudo docker image rm 2f938b337df3

- Delete Container:
  
    - Delete All Container    

          docker container prune  // remove old container
          OR
          docker system prune // remove all stoped container

    - Delete Spesific Container   

          docker rm [Container ID]

