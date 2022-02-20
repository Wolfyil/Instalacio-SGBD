## 1.	Un cop realitzada la instal·lació realitza una securització de la mateixa. Quin programa realitza aquesta tasca? Realitza una securització de la instal·lació indicant que la contrasenya de root sigui patata. 

- El programa que realitza aquesta tasca es el “mysql_secure_installation”. 
- Aquest programa lo que fa es millorar la seguretat del nostre Percona MySQL.
***

- Abans de fer la securitzacio anirem a cambiar els requeriments i política de la contrasenya per el SQL, per poder posar “patata” com a contrasenya. 

- Anirem a la següent ruta:

*nano /etc/my.cnf*

- Al modificar la política de la contrasenya en aquest fitxer sempre es guardaran els canvis. 

- Afegirem les següents linees com es mostra en l’imatge

![imagen](https://user-images.githubusercontent.com/61557739/154850026-15d80606-bdbd-4adb-96be-45fdc057b5e8.png)

- Despres reiniciarem el Percona MySQL

*systemctl restart mysql*

![imagen](https://user-images.githubusercontent.com/61557739/154850043-98748d46-ff9e-4863-8d9f-55dbbd873363.png)

***
- Ara mirarem quina es nostre contrasenya temporal del Percona MySQL, per accedir al MySQL amb la següent comanda:

*sudo grep "temporary password" /var/log/mysqld.log*

![imagen](https://user-images.githubusercontent.com/61557739/154850059-db0b519c-9509-482c-a15e-1dfd91065a5b.png)


- Copiarem aquesta contrasenya temporal. A continuació realitzarem una securitzacio al nostre Percona for MySQL, utilitzant la següent comanda:

*mysql_secure_installation*

![imagen](https://user-images.githubusercontent.com/61557739/154850067-08666ae9-602b-43aa-b889-fc3b90a76338.png)

![imagen](https://user-images.githubusercontent.com/61557739/154850076-dd8e34dd-69f3-434c-b886-ead50b993bee.png)

*Finalment ja estaria.*
