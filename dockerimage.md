create dockerFile in project and code

FROM nginx:alpine
COPY /dist  /usr/share/nginx/html
EXPOSE 80


make sure you have docker desktop version installed

run following commands

docker build -t resturant-listing .     //it is going to create new image in docker
docker run -it --rm -p 9000:80 image_name_from_docker  //it is going to run the image

to see the content deployed go to docker desktop -> container -> select running container -> click terminal - add cd /usr/share/nginx/html ls
it will list the all contents uploaded to docker image
