# Webserver's with Apache and PHP on Ubuntu

Versions of PHP:
- PHP 7
- PHP 5.6.*

This dockerfiles are for development, below you can see the default params:
- display_errors **on**
- error_reporting **22527**
  - You can get the number of error_reporting on [PHP Error Reporting Wizard](http://www.bx.com.au/tools/ultimate-php-error-reporting-wizard)
- date.timezone **America/Sao_Paulo**
- max_execution_time **60**
- max_input_time **120**
- memory_limit **512**
- post_max_size **30M**
- upload_max_filesize **30M**

The port 80 is expose.

# How to use PHP 7
docker run -d -v [host_path]:/var/www/html -p [host_port]:80 higgorm/apachephp7

# How to use PHP 5.6.*

docker run -d -v [host_path]:/var/www/html -p [host_port]:80 higgorm/apachephp5.6
