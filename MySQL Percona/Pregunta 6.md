## 6.	El servei de MySQL (mysqld) escolta al port 3306. Quina modificació/passos caldrien fer per canviar aquest port a 33306 per exemple?  
### Important: No realitzis els canvis. Només indica els passos que faries. 
***

- Per canviar el port que escolta el MySQL, hem d’anar a la ruta: 

*nano /etc/my.cnf*

- Dins del fitxer *my.cnf*, en el apartat de “mysqld” afegirem la linea: 

*port=33306* 

- Així es canviaria el port a un que nosaltres especifiquem.

![imagen](https://user-images.githubusercontent.com/61557739/154850478-155aaa2b-0d3c-4c30-a0d4-5ec41dcb538e.png)
