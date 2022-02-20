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
