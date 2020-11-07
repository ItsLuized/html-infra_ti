# HTML-INFRA_TI

Final project for the class IT Infrastructure

### What we did

In the Dockerfile make a custom image of a nginx docker image, replacing the default html with this repo

### To build the custom image use the following command:

`docker build -t webserver .`\
Where "webserver" is the name of the image (Can be changed to the desired name)

### Steps to use this docker as intended

The goal was to have a NFS that could change images in this html...

So, at the time of running the docker, the following command was used:

`sudo docker run -it --rm -d -p 8080:80 --name web -v ~/images:/usr/share/nginx/html/images webserver`\

-p binds port 80 of the container to TCP port 8080 of the host machine, and can be changed as desired \
_{host machine port}:{port of the container}_
