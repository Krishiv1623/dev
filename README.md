# Assignment 1 – Dockerized Static Website

## Files
- index.html: Static webpage
- Dockerfile: Builds the Nginx-based image

## Commands Used
docker build -t krishiv-site .
docker run -d --name mysite -p 7070:80 krishiv-site
curl http://localhost:7070
docker stop mysite
docker rm mysite

## explanation
made a basic html file with heading <!DOCTYPE html> which tells nginx the file is in html 5 code
 in docker file first wrote 'from' which provides the base image, then we copy index.html file with the 
  file location of the default file location in nginx