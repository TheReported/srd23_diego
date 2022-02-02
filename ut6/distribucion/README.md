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

- Cambiaremos el nombre de la carpeta `public_html` a `html`, además la movemos a `/var/www` y le pondremos de propietario `root` y a sus subcarpetas.

  ![](img/55.png)

- Ahora creamos la base de datos que vamos a utilizar y modificamos el fichero `config.php`.

  ![](img/9.png)

  ![](img/10.png)

- Además le pondremos el idioma en Español. Aunque también se puede hacer añadiendo la siguiente línea: `$language_module = "spanish.inc";`.

  ![](img/11.png)

- Si queremos acceder a phpList hay dos maneras por localhost o creando un virtualhost, yo lo hice por localhost pero si lo quieres hacer de la otra manera, tendremos que crear el virtual host en `/etc/apache2/sites-available`, con el siguiente contenido:

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

- Vemos que también podemos entrar poniendo la siguiente URL `phplist.miempresa.com`.

  ![](img/56.png)

  ![](img/57.png)

[Volver](#0)

### **2. Investigar sobre las principales opciones de configuración y mantenimiento.** <a id="2"></a>

- **Las principales opciones de configuración y mantenimiento son:**

  - **Configuraciones principales para la base de datos:**

    - *$database_name*
    - *$database_user*
    - *$database_password*

  - **Configurar idioma:**
    - *$language_module*

  - **Configurar los rebotes:**
    - *$message_envelope*
    - *$bounce_mailbox_host*
    - *$bounce_mailbox_user*
    - *$bounce_mailbox_password*

  - **Configurar para evitar ser considerado spammer:**

    - *define(«MAILQUEUE_BATCH_SIZE»,0); //Número de emails por periodo*
    - *define(«MAILQUEUE_BATCH_PERIOD»,3600); //El periodo en segundos aqui 1 hora*
    - *define(‘MAILQUEUE_THROTTLE’,15);//Pausa entre emails en segundos (240 emails por hora)*

  - **Configurar si no queremos que aparezca el ``powered by`` en nuestros emails:**

    - *define («REGISTER»,0);*

[Volver](#0)

### **3. Buscar información sobre los usos y potenciales de phpList. ¿Para que sirve? ¿Qué le ofrece a una empresa la utilización de esta aplicación?** <a id="3"></a>

- **phpList** es un software de código abierto que nos permite crear listas de distribución de correo para efectuar envíos masivos de email.

- Se emplea principalmente para la divulgación de información mediante envío de boletines, novedades o simplemente publicidad.


[Volver](#0)

### **4. Realizar acciones dentro del phpList.** <a id="4"></a>

##### **4.1 Incluir nuevos usuarios** <a id="4.1"></a>

- Para incluir nuevos usuarios, tendremos que ir al Inicio y darle click a `Import Subscribers`.

  ![](img/23.png)

- Incluimos los usuarios que queramos y le daremos a `Import emails`.

  ![](img/24.png)

- Vemos que se han incluido los usuarios correctamente.

  ![](img/25.png)

##### **4.2 Crear una lista e incluir miembros en ella** <a id="4.2"></a>

  ![](img/26.png)

  ![](img/27.png)

- Comprobamos que se ha creado correctamente.

  ![](img/28.png)

- Ahora vamos a incluir miembros en ella.

  ![](img/29.png)

  ![](img/30.png)

  ![](img/31.png)

- Incluimos los emails que queramos.

  ![](img/32.png)

- Comprobamos que se han agregado correctamente los miembros a la lista.

  ![](img/33.png)

##### **4.3 Crear una página home de suscripción a una lista** <a id="4.3"></a>

- Nos dirigimos al menú de la parte izquierda y vamos a `Opciones de configuración` y le daremos click a `Crear una nueva página de suscripción`.

  ![](img/34.png)

  ![](img/35.png)

- La modificamos como queramos y le damos a guardar.

  ![](img/36.png)

  ![](img/37.png)

- Comprobamos que se ha creado bien la página.

  ![](img/38.png)

  ![](img/39.png)

- Para solucionar el error anterior, tendremos que eliminar el archivo``index.html`` o cambiarle el nombre. También se puede arreglar dandole prioridad al fichero ``index.php``.

  ![](img/40.png)

  ![](img/41.png)

- Nos suscribimos a nuestra página y comprobamos.

  ![](img/42.png)

  ![](img/43.png)

##### **4.4 Crear una campaña** <a id="4.4"></a>

  ![](img/44.png)

  ![](img/45.png)

  ![](img/46.png)

  ![](img/47.png)

  ![](img/48.png)

  ![](img/49.png)

  ![](img/50.png)

  ![](img/51.png)

  ![](img/52.png)

  ![](img/53.png)

  ![](img/54.png)

[Volver](#0)
