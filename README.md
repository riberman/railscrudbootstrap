# Rails and Bootstrap Simple CRUD
# [![Build Status](https://travis-ci.org/riberman/railscrudbootstrap.svg?branch=master)](https://travis-ci.org/riberman/railscrudbootstrap)[![GitHub contributors](https://img.shields.io/github/contributors/Naereen/StrapDown.js.svg)](https://GitHub.com/Naereen/StrapDown.js/graphs/contributors/)[![GitHub version](https://badge.fury.io/gh/Naereen%2FStrapDown.js.svg)](https://github.com/Naereen/StrapDown.js)[![Package Control total downloads](https://img.shields.io/packagecontrol/dt/SwitchDictionary.svg)](https://packagecontrol.io/packages/SwitchDictionary)[![Open Source Love svg2](https://badges.frapsoft.com/os/v2/open-source.svg?v=103)](https://github.com/ellerbrock/open-source-badges/)
<br />
Hi, In this project we have a simple crud of articles, using containner **docker, rails, bootstrap and postgreSQL.**
[HEROKU_Link](https://pacific-citadel-82967.herokuapp.com/articles)
<br />
![alt text](https://d1yjjnpx0p53s8.cloudfront.net/styles/logo-thumbnail/s3/112012/rails.png?itok=UeYwdITD)
![alt text](https://www.mundodocker.com.br/wp-content/uploads/2015/06/docker_facebook_share.png)
![alt text](http://micreiros.com/wp-content/uploads/bootstrap-logo.png)
![alt text](https://d1.awsstatic.com/rdsImages/postgresql_logo.6de4615badd99412268bc6aa8fc958a0f403dd41.png)
## Requirements and Link Tutorial
Install Docker and Docker Compose
[https://docs.docker.com/compose/install/](https://docs.docker.com/compose/install/) 
How to make this project from scratch
<br />
[https://guides.rubyonrails.org/getting_started.html](https://guides.rubyonrails.org/getting_started.html)
<br />
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
