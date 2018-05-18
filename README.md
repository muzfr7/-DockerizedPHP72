# Dockerized PHP 7.2
Docker containers configured and ready to develop PHP7 applications..

### What's included?
* PHP:7.2-fpm
* MySQL
* Nginx
* Composer
* Git
* Nano

### How to install?
**Step 1.** Having [Git](https://git-scm.com) installed, clone this repository somewhere in your computer, for this example I'm going to clone it in `~/Developer/` directory:
```
$ cd ~/Developer
$ git clone https://github.com/muzfr7/-DockerizedPHP72.git
```

**Step 2.** You may want to update timezone settings in following files:
```
$ nano DockerizedPHP72/nginx/Dockerfile
$ nano DockerizedPHP72/php-fpm/Dockerfile
$ nano DockerizedPHP72/php-fpm/php.ini
```

**Step 3.** Having [Docker](https://www.docker.com) natively installed on your computer, build and run containers:
```
$ cd ~/Developer/DockerizedSymfony4
$ docker-compose build
$ docker-compose up -d
```

