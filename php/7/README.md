# Webserver with Apache/2.4.29 and PHP 7.2.3 on Ubuntu 18.04

The default virtualhost has default params:
- display_errors **on**
- error_reporting **22527**
  - You can get the number of error_reporting on [PHP Error Reporting Wizard](http://www.bx.com.au/tools/ultimate-php-error-reporting-wizard)
- date.timezone **America/Sao_Paulo**
- max_execution_time **60**
- max_input_time **120**
- memory_limit **512**
- post_max_size **30M**
- upload_max_filesize **30M**

The port 80 is expose

# How to use
###### Using docker in command line
```
docker run -d -v [host_path]:/var/www/html -p [host_port]:80 higgorm/apachephp7
```

###### Using docker-compose
```
version: '3'
services:
  webphp:
    image: higgorm/apachephp7
    ports:
      - "[host_port]:80"
    volumes:
      - [host_path]:/var/www/html

```

This image has a environment variable called WEB_DOCUMENT_ROOT if you need to point DocumentRoot to another folder. For exemple the framework Laravel, the DocumentRoot needs to point to public folder.

###### Using docker in command line
```
docker run -d -v [host_path]:/var/www/html -p [host_port]:80 -e WEB_DOCUMENT_ROOT=public higgorm/apachephp7
```

###### Using docker-compose
```
version: '3'
services:
  webphp:
    image: higgorm/apachephp7
    ports:
      - "[host_port]:80"
    volumes:
      - [host_path]:/var/www/html
    environment:
      WEB_DOCUMENT_ROOT: public
```
