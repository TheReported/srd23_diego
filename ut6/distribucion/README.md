# **Listas de distribución**

***Nombre:*** Diego Peraza Cabo
<br>
***Curso:*** 2º ASIR

## **Índice** <a id="0"></a>

+ [1. Instalación de la aplicación phpList en un entorno Ubuntu Server con Apache, php y MySQL.](#1)
+ [2. Investigar sobre las principales opciones de configuración y mantenimiento.](#2)
+ [3. Buscar información sobre los usos y potenciales de phpList. ¿Para que sirve? ¿Qué le ofrece a una empresa la utilización de esta aplicación?](#3)
+ [4. Realizar acciones](#4)
  + [4.1 Incluir nuevos usuarios](#4.1)
  + [4.2 Crear una lista e incluir miembros en ella](#4.2)
  + [4.3 Crear una página home de suscripción a una lista](#4.3)
  + [4.4 Crear una campaña](#4.4)

### **1. Instalación de la aplicación phpList en un entorno Ubuntu Server con Apache, php y MySQL.** <a id="1"></a>

- Primero que nada comprobamos que nuestro entorno de Ubuntu Server tiene instalado correctamente: Apache, php y MySQL.

  ![](img/1.png)

- Una vez hecho el paso anterior, nos descargaremos la aplicación phpList.

  ![](img/2.png)

  ![](img/4.png)

  ![](img/3.png)

- Descomprimimos el archivo comprimido de phpList.

  ![](img/6.png)

- Movemos la carpeta `phplist-3.6.6` al directorio `/var/www`con el nombre `phplist`.

  ![](img/7.png)

- Cambiamos los permisos de la carpeta.

  ![](img/8.png)

- Ahora creamos la base de datos que vamos a utilizar y modificamos el fichero `config.php`.

  ![](img/9.png)

  ![](img/10.png)

- Además le pondremos el idioma en Español.

  ![](img/11.png)

- Ahora crearemos un virtualhost para phpList con la siguiente ruta: `/var/www/html/lists/admin`

  ![](img/17.png)

- Habilitamos el sitio y reiniciamos el servicio de `apache2`.

  ![](img/15.png)

- Comprobamos de que el sitio web ha sido habilitado.

    ![](img/16.png)

- Añadimos en el fichero `/etc/hosts` el virtualhost.

  ![](img/12.png)

- Entramos al navegador web y pondremos lo siguiente: `localhost/lists/admin` y pasaremos con la instalación.

  ![](img/18.png)

  ![](img/19.png)

  ![](img/20.png)

- Ya terminada la instalación, iniciaremos sesión y entramos a phpList para realizar las acciones que queremos hacer.

  ![](img/22.png)

### **2. Investigar sobre las principales opciones de configuración y mantenimiento.** <a id="2"></a>



### **3. Buscar información sobre los usos y potenciales de phpList. ¿Para que sirve? ¿Qué le ofrece a una empresa la utilización de esta aplicación?** <a id="3"></a>

### **4. Realizar acciones dentro del phpList.** <a id="4"></a>

##### **4.1 Incluir nuevos usuarios** <a id="4.1"></a>

##### **4.2 Crear una lista e incluir miembros en ella** <a id="4.2"></a>

##### **4.3 Crear una página home de suscripción a una lista** <a id="4.3"></a>

##### **4.4 Crear una campaña** <a id="4.4"></a>
