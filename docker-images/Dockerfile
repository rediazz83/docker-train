# Primera capa:  base en centos
FROM centos

# Segunda capa: instalamos apache (el -y es como decir 'si a todo')
RUN yum install httpd -y

# Tercera capa: Copiamos el folder en el document root de apache
COPY beryllium /var/www/html

# Cuarta capa: Levanta el servidor apache y lo deje FOREGROUND
CMD apachectl -DFOREGROUND
