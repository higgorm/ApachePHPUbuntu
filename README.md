# Webserver's with Apache and PHP on Ubuntu

Versions of PHP:
- PHP 7
- PHP 5.6.*


# How to use PHP 7
docker run -d -v [host_path]:/var/www/html -p [host_port]:80 higgorm/apachephp7

# How to use PHP 5.6.*

docker run -d -v [host_path]:/var/www/html -p [host_port]:80 higgorm/apachephp5.6
