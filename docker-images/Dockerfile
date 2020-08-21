# Primera capa:  base en centos
FROM centos

# Segunda capa: instalamos apache (el -y es como decir 'si a todo')
RUN yum install httpd -y

# Tercera capa: Copiamos el folder en el document root de apache
# COPY beryllium /var/www/html
COPY startbootstrap-freelancer-master /var/www/html

# Cuarta capa: Seteamos una variable de entorno
ENV contenido test

# Quinta capa: Escribimos la variable en un archivo
RUN echo "$contenido" > /var/www/html/prueba.html

# Sexta capa: Levanta el servidor apache y lo deje FOREGROUND
CMD apachectl -DFOREGROUND
