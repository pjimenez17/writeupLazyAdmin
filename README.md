Hago un nmap a la ip y descubro que los puertos 22 y 80 estan abiertos

Ahora entrare a la pagina de la IP en mi caso 10.10.17.193 que es la default de apache

Con Postman hago una peticion GET para obtener el codigo fuente de la pagina de la IP pero no descubro nada interesante

Hago un dirb para ver los directorios ocultos en la web con **dirb http://10.10.17.193 /usr/share/wordlist/common.txt**

Me da varios directorios ocultos

me da el /content per dice This site is building now pero hay mas alla de content como content/as que es un login y en content/as/lib donde hay archivos php y sql

Hay un archivo mysqlBackup en /content/inc/ que me lo descargo con una contraseña encriptada y varios nombres como el usuario **manager**

La desencriptamos poniendo la contraseña MD5 en un desencriptador **md5hashing.net** pasamos el md5 hash y nos da un md5 value y del valor MD5 la convertimos a texto con https://iotools.cloud/es/tool/md5-decrypt/ la contraseña es Password123

Una vez dentro intente buscar metasploits y vulnerabilidades en la pagina de SweetRice version 1.5.1 pero me quede sin tiempo