## REQUISITS PREVIS ABANS DE LA INSTAL·LACIO DEL MYSQL 8.0

- Tenir una maquina CentOS 7 minimal amb 2 interfícies de xarxa: 

- *1 NAT* per accés a internet per descarregar lo necessari per fer la practica i actualitzar el sistema 

- *1 Adaptador nomes amfitrió* per tenir connexió des de el Putty del nostre ordinador a la Maquina CentOS 7 minimal de forma segura.

***




## INSTAL.LACIÓ MYSQL 8.0

- Abans d’instal·lar el MySQL 8.0, hem de fer un Update del sistema 

*yum update -y*

![imagen](https://user-images.githubusercontent.com/61557739/154850647-69443c21-21ea-4365-b3a7-2e19c8ab8540.png)

- La centos no ve per defecte amb el “wget” per tant utilitzarem la seguent comanda per instalarlo:

*yum install wget*

![imagen](https://user-images.githubusercontent.com/61557739/154850671-555c6cf6-9192-4e07-9e8f-eaa4c0893d29.png)

- Despres d’actualitzar el sistema i instal·lar el wget. 

- Eliminarem mariadb ja que centos7 la porta per defecte. Comprovem si el tenim instal·lat:

*rpm -qa | grep mariadb*

![imagen](https://user-images.githubusercontent.com/61557739/154850693-15197c1d-bae6-472a-b9f1-66adc2df613c.png)

- Finalment eliminem mariadb:

*rpm -e --nodeps mariadb-libs-5.5.64-1.el7.x86_64*

![imagen](https://user-images.githubusercontent.com/61557739/154850715-dc5355e7-42ba-4d2e-bf95-1f9b77e22d36.png)

***

- A continuacio, hem de descarregar els repositoris per poder instal·lar el MySQL a la ultima versió, amb la següent comanda:

*sudo wget https://dev.mysql.com/get/mysql80-community-release-el7-5.noarch.rpm*

![imagen](https://user-images.githubusercontent.com/61557739/154850746-dc5123fd-7cc4-4936-bbd0-5c7c5e732d42.png)


- Una vegada descarregat el repositori hem de utilitzar la següent comanda per instal·lar-ho:

*yum localinstall mysql80-community-release-el7-5.noarch.rpm*

![imagen](https://user-images.githubusercontent.com/61557739/154850752-69f690f2-3872-4a11-aa52-3e4f1658fe78.png)


- A continuació comprovarem que el Repositori YUM MySQL ha sigut afegit correctament amb la següent comanda:

*yum repolist enabled | grep "mysql.*-community.*"*

![imagen](https://user-images.githubusercontent.com/61557739/154850773-4316c3d6-6e11-45ae-826f-c3c32d803709.png)


 - Finalment utilitzarem la següent comanda per instal·lar a la ultima versió el MySQL:

*yum install mysql-community-server*

![imagen](https://user-images.githubusercontent.com/61557739/154850788-af9da49f-1707-4a58-a2bc-4d269cc17bc5.png)

***

- Iniciarem el MySQL amb la següent comanda:

*service mysqld start*

![imagen](https://user-images.githubusercontent.com/61557739/154850795-905f0559-8d7d-4990-9fe4-27ed94378442.png)

- Finalment comprovem el seu estatus i versió:

*systemctl status mysqld*

*mysql -V*

![imagen](https://user-images.githubusercontent.com/61557739/154850813-7d97b3a0-8f4a-44df-8477-bad6b0bfe9ee.png)

*Finalment ja estaria*
