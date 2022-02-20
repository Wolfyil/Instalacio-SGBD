## 3. El procés de mysqld escolta al port 3306. Quina modificació/passos caldrien fer per canviar aquest port a 33306 per exemple? 
### *Important: No realitzis els canvis. Només indica els passos que faries.* 

***

- Aniriem al arxiu de configuració *my.cnf* (nano /etc/my.cnf) i afegirem la linea: port=33306 en el apartat “mysqld”.
- El MySQL es canviaria al port que nosaltres li hem especificat

![imagen](https://user-images.githubusercontent.com/61557739/154850968-c6ad0e19-e530-4d54-ae74-3b767e6cc932.png)
