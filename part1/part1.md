

* 1.1 

CONTAINER ID        IMAGE               COMMAND                  CREATED              STATUS                     PORTS               NAMES
174f48231409        nginx               "/docker-entrypoint.…"   38 seconds ago       Exited (0) 9 seconds ago                       zen_hoover
aede47d32901        nginx               "/docker-entrypoint.…"   About a minute ago   Exited (0) 4 seconds ago                       nice_bohr
bf857f9508fc        nginx               "/docker-entrypoint.…"   About a minute ago   Up About a minute          80/tcp              cranky_blackwell

* 1.2

 jaakkogummerus@Jaakko-MacBook-Air  ~/Desktop/devops-docker  docker ps -a
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES

 jaakkogummerus@Jaakko-MacBook-Air  ~/Desktop/devops-docker  docker images
REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE

* 1.3

Digest: sha256:7c0635934049afb9ca0481fb6a58b16100f990a0d62c8665b9cfb5c9ada8a99f
Status: Downloaded newer image for devopsdockeruh/pull_exercise:latest
Give me the password: basics
You found the correct password. Secret message is:
"This is the secret message"

* 1.4

 ✘ jaakkogummerus@Jaakko-MacBook-Air  ~  docker run -d --rm -it --name testing devopsdockeruh/exec_bash_exercise

jaakkogummerus@Jaakko-MacBook-Air  ~  docker exec -it testing bash

root@5608d2f1a3b3:/usr/app# tail -f ./logs.txt

Thu, 13 Aug 2020 15:50:28 GMT
Secret message is:
"Docker is easy"

* 1.5

jaakkogummerus@Jaakko-MacBook-Air  ~  docker run -d --rm -it --name helsinki ubuntu:16.04 sh -c 'echo "Input website:"; read website; echo "Searching.."; sleep 1; curl http://$website;'

jaakkogummerus@Jaakko-MacBook-Air  ~  docker exec -it helsinki bash

root@a44eea6220db:/# apt-get update

root@a44eea6220db:/# apt-get install curl

root@a44eea6220db:/# curl helsinki.fi

* 1.6.

✘ jaakkogummerus@Jaakko-MacBook-Air  ~/desktop/devops-docker/part1  docker build -t docker-clock .

jaakkogummerus@Jaakko-MacBook-Air  ~/desktop/devops-docker/part1  docker run docker-clock -c 20

* 1.7.

 ✘ jaakkogummerus@Jaakko-MacBook-Air  ~/desktop/devops-docker/part1/1.7.  docker build -t curler .

 jaakkogummerus@Jaakko-MacBook-Air  ~/desktop/devops-docker/part1/1.7.  docker run -it curler
root@a1c3ba5af450:/mydir# curl helsinki.fi

* 1.8.

✘ jaakkogummerus@Jaakko-MacBook-Air  ~/desktop/devops-docker/part1/1.7.  docker run -v $(pwd)/logs.txt devopsdockeruh/first_volume_exercise

* 1.9.

jaakkogummerus@Jaakko-MacBook-Air  ~/desktop/devops-docker/part1/1.7.  docker run -p 1234:80 devopsdockeruh/ports_exercise

- > go to page: http://127.0.0.1:1234

* 1.11.

jaakkogummerus@Jaakko-MacBook-Air  ~/desktop/devops-docker/part1/1.11.  docker build -t backendex .

 ✘ jaakkogummerus@Jaakko-MacBook-Air  ~/desktop/devops-docker/part1/1.11.  docker run -v $(pwd):/logs.txt -p 8000:8000 backendex

 * 1.12.

 docker run -p 8000:8000 backendex

 docker run -p 5000:5000 frontendex

 * 1.15.

 https://hub.docker.com/repository/docker/jagummer/wineapp


* 1.16.

https://dockerexample16.herokuapp.com/presses/new

* 1.17.

