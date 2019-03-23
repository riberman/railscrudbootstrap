# README

# Rails and Bootstrap Simple CRUD  
Hi, In this project we have a simple crud of articles, using containner **docker, rails, bootstrap and postgreSQL.**
## Requirements
Install Docker and Docker Compose
[https://docs.docker.com/compose/install/](https://docs.docker.com/compose/install/) 
## Config Container
Generate your container
````
docker-compose build
````
If the project package have a permission problem you need execute this command line
````
chown -R youruser:youruser .
````
If you need add gem install add in **Gemfile** like this
````
gem 'pack', '~> 1.0'
````
Or no especific version
````
gem 'pack'
````
## Up Container
````
docker-compose up
````
## Data base 
If the docker is up, now you need create the data base in **postgreSQL**
````
docker-compose run web rake db:create
````

## Localhost Server Start
If the server is down is since in last command, **re run this.**
````
docker-compose up
````
In terminal you need see like this.
````
db_1   | 2019-03-23 06:54:53.358 UTC [1] LOG:  listening on IPv4 address "0.0.0.0", port 5432
db_1   | 2019-03-23 06:54:53.359 UTC [1] LOG:  listening on IPv6 address "::", port 5432
db_1   | 2019-03-23 06:54:53.382 UTC [1] LOG:  listening on Unix socket "/var/run/postgresql/.s.PGSQL.5432"
db_1   | 2019-03-23 06:54:53.443 UTC [23] LOG:  database system was shut down at 2019-03-23 06:09:46 UTC
db_1   | 2019-03-23 06:54:53.474 UTC [1] LOG:  database system is ready to accept connections
````
**Now the page is on in localhost**
````
localhost:3000/articles
````

## I need Help
The tutorial is on in this link.
[https://docs.docker.com/compose/rails/](https://docs.docker.com/compose/rails/)

![alt text](data:image/png;base64,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)
![alt text](https://www.mundodocker.com.br/wp-content/uploads/2015/06/docker_facebook_share.png)
![alt text](http://micreiros.com/wp-content/uploads/bootstrap-logo.png)
![alt text](https://d1.awsstatic.com/rdsImages/postgresql_logo.6de4615badd99412268bc6aa8fc958a0f403dd41.png)
