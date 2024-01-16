# Laravel-PHP-Dokcerized-Project
A simple setup to learn Multi-Container Orchestration

## Target Setup
Create laravel applications without installing anything on our host machine, except for Docker.\\

### Idea
Three Application Containers:
- host machine contains the Laravel source code 
- source code will then be exposed to the PHP interpreter container 
- PHP interpreter container generates and response to incoming requests
- Nginx Web Server container takes incoming requests then to the PHP interpreter
- MySQL Database for storing data 
- PHP interpreter container communicate with MySQL database

Utility Containers:
- Composer container used by Laravel to install dependencies
- Laravel Artisan is used by Laravel to run migrations against our database and write initial starting data to the database
- Npm Container for some of its front and logic