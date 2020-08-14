# primera capa:  base en centos
FROM centos

# segunda capa: instalamos apache (el -y es como decir 'si a todo')
RUN yum install httpd -y

#Tercera capa: Levanta el servidor apache y lo deje FOREGROUND
CMD apachectl -DFOREGROUND
