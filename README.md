After making directory "php" open a terminal and make image with name my-php-app by command "docker build -t my-hph-app ."

To check all our available images use command docker images

Now use command docker run -t 8001:80 -d my-php-app

-t 8001:80 we r using to set the port. 8001 - our random port. And 80 - port after word EXPOSE in Dockerfile

After that we should create in root directory yaml file: docker-compose.yml

After that w r goidn to dockerhub and search phpmyadmin. Then we look for topic about usage with docker-compose and copy it in our project in file docker-compose and use command docker-compose build

If u discovered a mistake " the attribute `version` is obsolete" u shoul delete version from ur file

After successful building use command docker-compose up

Now we have localhost with port 8080 with phpmyadmin

To add another one port with some files, in file docker-compose in services we add php: build: ./php ports: -8081:80.

8080 and 8081 - different ports. And we use different ports to avoid mistakes

Now we can open 2 and more defferent projects in browser with docker-compose
