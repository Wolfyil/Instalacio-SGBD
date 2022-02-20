5.	Crea un usuari anomenat asix en el sistema operatiu i en SGBD de tal manera que aquest usuari del sistema operatiu no hagi d'introduir l'usuari i password cada vegada que cridem al client mysql? 
Usuari SO-→ asix / patata . Usuari MySQL → asix / patata 


Modificarem el següent arxiu per despres poder crear correctament la contrasenya “patata” en el SO. Hem de modificar la política de contrasenya de la Centos, en la següent ruta:

Nano /etc/pam.d/system-auth

Els canvis que farem seran els següents:
Comentarem la linea que hi havia originalment i afegirem una linea de sufficient en el password i editarem les 2 dues sufficient.

![imagen](https://user-images.githubusercontent.com/61557739/154850289-fc7099e9-9b8d-4145-968d-783a0ff66a03.png)

Despres guardem, sortim del fitxer i crearem l’usuari asix al SO. Posarem la contrasenya “patata”

![imagen](https://user-images.githubusercontent.com/61557739/154850302-a5d5cd47-02b0-4ece-b027-4826aee7d0d6.png)


A continuació crearem l’usuari asix en el MySQL Percona, primer entrarem al MySQL:

![imagen](https://user-images.githubusercontent.com/61557739/154850333-76a21380-380a-4402-bd93-677610f36e32.png)

Crearem l’usuari asix i la contrasenya patata

![imagen](https://user-images.githubusercontent.com/61557739/154850343-cb8e219d-40cb-4ff5-9dd6-4cb37aaec52b.png)

A continuació li donarem tots els permisos al usuari asix en el MySQL

![imagen](https://user-images.githubusercontent.com/61557739/154850355-ea9d9eeb-356f-44b0-8be4-ae952ba08376.png)

Despres sortirem del mysql i iniciarem sessió en el usuari asix en el SO

A continuació posarem la següent comanda perque quan l’usuari asix en el SO cridi el mysql, inicii automàticament sessió en el client MySQL sense posar contrasenya ni usuari

mysql_config_editor set --login-path=mysql --host=localhost --port=3306 --user=asix --password


![imagen](https://user-images.githubusercontent.com/61557739/154850373-4c2b6a85-0172-4916-aa46-357c3cbcb5c2.png)


Farem una comprovació amb la següent comanda i ja estaria:

![imagen](https://user-images.githubusercontent.com/61557739/154850386-d0f220ad-24f6-4aa1-83ea-17f9bcf9e39c.png)

Comprovacio login 

![imagen](https://user-images.githubusercontent.com/61557739/154850430-8bf5d2fc-fbaf-4279-9642-d6885e392b84.png)
