# 1era capa:  base en centos
FROM centos

# 2da capa: instalamos apache (el -y es como decir 'si a todo')
RUN yum install httpd -y

# 3era capa
WORKDIR /var/www/html

# 4ta capa: Copiamos el folder en el document root de apache
# COPY beryllium /var/www/html
COPY startbootstrap-freelancer-master .

# 5ta capa: Seteamos una variable de entorno
ENV contenido test

# 6ta capa: Escribimos la variable en un archivo
RUN echo "$contenido" > /var/www/html/prueba.html

# 7ma capa: Levanta el servidor apache y lo deje FOREGROUND
CMD apachectl -DFOREGROUND
