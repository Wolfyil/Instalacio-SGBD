## 7.	Ensenya al professor que us podeu connectar al SGBD. 

- Per connectarnos hi ha 2 formes, per la CentOS i per el MySQL Workbench

***

## CONNEXIO AMB LA CENTOS

- Primer iniciarem sesio al SO amb l’usuari "asix", despres simplement cridarem al mysql amb la següent comanda:

*mysql*

- Ja tenim la connexió de "asix" al SGBD, ja que el vam configurar perque s’iniciï automàticament sense posar usuari i contrasenya al cridar el mysql.

![imagen](https://user-images.githubusercontent.com/61557739/154857104-5112bc1e-9cf4-4656-a95b-52c30bb94357.png)

***

## CONNEXIO AMB EL MySQL WORKBENCH

- Desde el nostre ordinador, hem de tindre instal·lat el MySQL Workbench o per exemple el Toad for MySQL. 
- En el meu cas utilitzo el MySQL Workbench

- Iniciem el MySQL Workbench i li donarem al boto +, per fer una nova connexió 


![imagen](https://user-images.githubusercontent.com/61557739/154857111-2c9a0424-a741-40ca-9aff-2b14601dd6cd.png)

- Posarem un nom a la connexió, despres posarem el tipus de conexio TCP/IP over SSH. 
- Posarem la IP de la nostre centos, l’usuari "asix" del SO, el hostname MySQL el deixarem per defecte ja que es localhost i l’usuari "asix" del MySQL

- Finalment li donarem a test connection


![imagen](https://user-images.githubusercontent.com/61557739/154857123-2131548a-dd2a-40a1-b74d-82374ee0baa3.png)

- La contrasenya del usuari "asix" del SO es "patata"

![imagen](https://user-images.githubusercontent.com/61557739/154857138-efd550c0-980e-42bb-9ded-6f8821f3e8d4.png)

- La contrasenya del usuari "asix" del MySQL es "patata"

![imagen](https://user-images.githubusercontent.com/61557739/154857157-cd68a51f-4684-41ea-b4b6-466ef57bf17b.png)


- Finalment el test de la connexió funciona

![imagen](https://user-images.githubusercontent.com/61557739/154857174-9c4b0ff8-8233-46f5-b8e7-0b9f01419eb2.png)

- Per ultim li donarem a OK

![imagen](https://user-images.githubusercontent.com/61557739/154857188-3017b3c9-5ce9-4875-ad2a-3f694b9ae645.png)


*Ja estaria tot*

![imagen](https://user-images.githubusercontent.com/61557739/154857207-fe90ea13-cebc-4e02-a587-b0943204e529.png)

![imagen](https://user-images.githubusercontent.com/61557739/154857216-486dbb51-a089-4343-ab80-b2966d77305e.png)
