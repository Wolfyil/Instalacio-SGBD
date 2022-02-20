REQUISITS PREVIS ABANS DE LA INSTAL·LACIO DEL PERCONA SERVER FOR MYSQL

- Tenir una maquina CentOS 7 minimal amb 2 interfícies de xarxa: 

1 NAT per accés a internet per descarregar lo necessari per fer la practica i actualitzar el sistema 

1 Adaptador nomes amfitrió per tenir connexió des de el Putty del nostre ordinador a la Maquina CentOS 7 minimal de forma segura.






INSTAL.LACIÓ PERCONA SERVER FOR MYSQL

Abans d’ instal·lar el Percona Server for MySQL, hem de fer un Update del sistema 

yum Update -y

![imagen](https://user-images.githubusercontent.com/61557739/154849384-d14e7fc0-86c4-4dba-9e7b-d6c6e88189c4.png)
 

Despres d’actualitzar el sistema, hem de instal·lar els repositoris de percona amb la següent comanda:

yum install https://repo.percona.com/yum/percona-release-latest.noarch.rpm

![imagen](https://user-images.githubusercontent.com/61557739/154849720-7a5946c1-0b2c-4ab3-bc70-5bcbb6a7aabf.png)

Despres activarem els respositoris per el Percona versió 8
sudo percona-release setup ps80

![imagen](https://user-images.githubusercontent.com/61557739/154849758-fbefe943-cdb2-4c03-a2d0-63f9b2089591.png)

Finalment instal·larem els paquets i el percona server for MySQL
sudo yum install percona-server-server
![imagen](https://user-images.githubusercontent.com/61557739/154849786-b497006a-5ef1-4ff3-adc7-332bf4fff731.png)

Comprovem la versió del percona MySQL sigui la 8

![imagen](https://user-images.githubusercontent.com/61557739/154849806-7dc950c3-8675-41a5-bdad-910dd35594ff.png)

Important iniciar el servei MySQL
service mysqld start

![imagen](https://user-images.githubusercontent.com/61557739/154849825-afdc1425-724e-441f-a456-19e02547e473.png)
