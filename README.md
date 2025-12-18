# Assignment 2 – Container Communication

## Containers
- Web container: Nginx static site
- API container: hashicorp/http-echo

## Network
Custom Docker network: webnet

## Commands Used
docker network create webnet

docker run -d --name api --network webnet \
hashicorp/http-echo -text="Hello from API"

docker build -t web-app .

docker run -d --name web --network webnet \
-p 8080:80 web-app

docker exec -it web curl http://api:5678

## Explanation
here we require .conf file because we need add a api which cannot be done by 
standard configuration and in docker file we placed are configuratin file where nginx 
checks for any configurational changes 

## images
<img width="1918" height="1078" alt="docker_2" src="https://github.com/user-attachments/assets/33ec8771-0075-48f2-8c28-ce9583af9046" />

