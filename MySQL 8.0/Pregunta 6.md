6.	Ensenya al professor que us podeu connectar al SGBD. 

Com no es demana crear cap usuari específic com l’exercici anterior. Crearé un usuari SO i SQL, ja que tampoc es demana que aquest usuari, inicii automàticament sessió en el client MySQL sense posar contrasenya ni usuari.  

Nom d’usuari SO: daniel_asix / patata
Nom d’usuari SQL: daniel_asix / patata


Per crear la contrasenya patata en el SO he modificat el següent fitxer:
Nano /etc/pam.d/system-auth

Els canvis que farem seran els següents:
Comentarem la linea que hi havia originalment i afegirem una linea de sufficient en el password i editarem les 2 dues sufficient.

![imagen](https://user-images.githubusercontent.com/61557739/154851116-41e6f4d5-475b-4d81-ab93-adbc2a3f6e37.png)

crearem l’usuari daniel_asix al SO. Posarem la contrasenya “patata”

![imagen](https://user-images.githubusercontent.com/61557739/154851140-b728d8b7-0a74-45b6-8d4c-ba96792a980b.png)

Per posarli la contrasenya “patata” al root MySQL he anat al següent arxiu i l’he modificat:

nano /etc/my.cnf

Al modificar la política de la contrasenya en aquest fitxer sempre es guardaran els canvis. 
Afegirem les següents linees com es mostra en l’imatge

![imagen](https://user-images.githubusercontent.com/61557739/154851171-430f6892-393b-49ad-93cb-1ff19a71fe6c.png)

Despres reiniciarem el MySQL
systemctl restart mysqld

![imagen](https://user-images.githubusercontent.com/61557739/154851196-cb10c23a-1e96-4359-9098-f0b36cff6584.png)


A continuació crearem l’usuari daniel_asix en el MySQL, primer entrarem al MySQL root:

![imagen](https://user-images.githubusercontent.com/61557739/154851214-aa66f063-897c-46c7-a337-19048e60eb21.png)


Crearem l’usuari daniel_asix i la contrasenya patata

![imagen](https://user-images.githubusercontent.com/61557739/154851237-a6968a36-1e4c-4d4a-9fe3-b9260f493746.png)

A continuació li donarem tots els permisos al usuari daniel_asix en el MySQL

![imagen](https://user-images.githubusercontent.com/61557739/154851252-c1a32bc4-1d25-4c73-8392-9e7ff60ca5e2.png)

Ja el tindríem, hara faríem les connexions:


Per connectarnos hi ha 2 formes, per la CentOS i per el MySQL Workbench
CONNEXIO AMB LA CENTOS

Primer iniciarem sesio al SO amb l’usuari daniel_asix que vam crear, despres simplement utilitzarem la següent comanda per connectarnos al SGBD:
mysql -udaniel_asix-p

Despres quan ens demani la contrasenya al SQL, posarem la contrasenya patata del usuari SQL daniel_asix 
Ja tenim la connexió de daniel_asix al SGBD

![imagen](https://user-images.githubusercontent.com/61557739/154857277-28d645e8-e2c6-48e1-9414-a6331e6cdbc9.png)



CONNEXIO AMB EL MySQL WORKBENCH
Desde el nostre ordinador, hem de tindre instal·lat el MySQL Workbench o per exemple el Toad for MySQL. En el meu cas utilitzo el MySQL Workbench

Iniciem el MySQL Workbench i li donarem al boto +, per fer una nova connexió 


![imagen](https://user-images.githubusercontent.com/61557739/154857291-7ba50e67-b959-4502-a775-f7f5d4c44676.png)

Posarem un nom a la connexió, despres posarem el tipus de conexio TCP/IP over SSH i posarem la IP  de la nostre centos, l’usuari daniel_asix del SO, el hostname MySQL el deixarem per defecte ja que es localhost i l’usuari daniel_asix del MySQL

Finalment li donarem a test connection

![imagen](https://user-images.githubusercontent.com/61557739/154857306-4538f678-afd8-491b-819c-67ca5989553e.png)

La contrasenya del usuari daniel_asix del SO es patata

![imagen](https://user-images.githubusercontent.com/61557739/154857321-06214f1a-4f73-4522-957a-227102d02084.png)


La contrasenya del usuari daniel_asix del MySQL es patata

![imagen](https://user-images.githubusercontent.com/61557739/154857332-ad2cb48e-6994-45ea-9be2-1211f7ee6492.png)

Finalment el test de la connexió funciona

![imagen](https://user-images.githubusercontent.com/61557739/154857351-86cf7883-ece5-4b88-a2e3-93219cc46f3c.png)

Per ultim li donarem a OK

![imagen](https://user-images.githubusercontent.com/61557739/154857362-713d3c0c-0515-4701-a840-c9579e991f7c.png)

Ja estaria tot

![imagen](https://user-images.githubusercontent.com/61557739/154857369-13afdb72-48ad-4355-9a2b-687eb1f4147c.png)

![imagen](https://user-images.githubusercontent.com/61557739/154857372-d1f8cdce-fec7-4906-acb5-53babf51ab02.png)





