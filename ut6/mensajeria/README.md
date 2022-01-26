# **Instalación y Configuración de un Servidor de Mensajería Instantánea en Windows 2016 Server**

***Nombre:*** Diego Peraza Cabo
<br>
***Curso:*** 2º ASIR

## **Índice** <a id="0"></a>

  + [1. Comprobar que en tu servidor Windows 2016 están instalados y funcionan correctamente: IIS, PHP, MySQL y phpMyAdmin.](#1)
  + [2. Descargar e instalar el servidor de mensajería instantánea OpenFire para Windows.](#2)
  + [3. Crear una base de datos en blanco en MySqQL a través de phpMyAdmin y recordar nombre de la BD, así como usuario y contraseña con privilegios.](#3)
  + [4. Ejecutar el script de instalación de Openfire desde un navegador web del servidor, mediante la url ``http://127.0.0.1:9090``. (openfire trabaja con los puertos 9090 y 9091 –https-).](#4)
  + [5. Instalación y Configuración de OpenFire.](#5)
  + [6. Comprobamos desde el servidor el acceso con el usuario admin.](#6)
  + [7. Una vez instalado el servidor OpenFire, vamos a descargar e instalar un cliente de Mensajería, en este caso Spark.](#7)
  + [8. Ahora vamos a crear dos nuevos usuarios en OpenFire (además del administrador) para poder mantener una conversación entre cliente y servidor](#8)
  + [9. Comprobamos el funcionamiento de Spark](#9)

### **1. Comprobar que en tu servidor Windows 2016 están instalados y funcionan correctamente: IIS, PHP, MySQL y phpMyAdmin.** <a id="1"></a>

- Comprobamos que tenemos instalado IIS, yendo a `Administración del servidor -> Herramientas`, y nos saldrá la herramienta `Administador de IIS`. En los pasos siguientes se comprobará su funcionamiento.

  ![](img/1.png)

- Comprobamos que tenemos instalado PHP, creando un sitio web, que de carpeta raíz tenga una cualquiera, pero que contenga un archivo con el siguiente contenido: `<?php phpinfo();?>`

  ![](img/2.png)

- Para comprobar que tenemos instalado MySQL, entramos por línea de comandos y vemos la versión que tenemos.

  ![](img/4.png)

- Entramos a `phpmyadmin.miempresa.com` para comprobar tres cosas, el funcionamiento de ISS, el de MYSQL y el de phpMyAdmin.

  ![](img/5.png)

  ![](img/6.png)

[Volver](#0)

### **2. Descargar e instalar el servidor de mensajería instantánea OpenFire para Windows.** <a id="2"></a>

  ![](img/7.png)

  ![](img/8.png)

  ![](img/9.png)

  ![](img/10.png)

- Vemos que necesitamos descargarnos un programa para seguir con la instalación

  ![](img/11.png)

- Para la instalación de OpenFire nos tendremos que instalar el programa `install4j`.

  ![](img/12.png)

  ![](img/13.png)

  ![](img/14.png)

  ![](img/15.png)

  ![](img/16.png)

  ![](img/17.png)

  ![](img/18.png)

  ![](img/19.png)

  ![](img/20.png)

- Una vez instalado el programa `install4j`, seguiremos con la instalación de OpenFire y le daremos a `Ubicación`. Tendremos que buscar en la carpeta del programa, el ejecutable `java.exe`.

  ![](img/21.png)

  ![](img/22.png)

- Seleccionamos el idioma `Español`.

  ![](img/23.png)

  ![](img/24.png)

- Aceptamos los términos de licencia.

  ![](img/25.png)

  ![](img/26.png)

  ![](img/27.png)

- Esperamos a que se instale.

  ![](img/28.png)

- Iniciamos el servicio y pasaremos después con la configuración de OpenFire mediante el URL `http://localhost:9090`.

    ![](img/29.png)

[Volver](#0)

### **3. Crear una base de datos en blanco en MySqQL a través de phpMyAdmin y recordar nombre de la BD, así como usuario y contraseña con privilegios.** <a id="3"></a>

  ![](img/46.png)

  ![](img/33.png)

  ![](img/77.png)

  ![](img/78.png)

[Volver](#0)

### **4. Ejecutar el script de instalación de Openfire desde un navegador web del servidor, mediante la url ``http://127.0.0.1:9090``. (openfire trabaja con los puertos 9090 y 9091 –https-).** <a id="4"></a>

  ![](img/75.png)

  ![](img/76.png)  

[Volver](#0)

### **5. Instalación y Configuración de OpenFire.** <a id="5"></a>

- Elegimos el idioma `Español`

  ![](img/30.png)

- El dominio y los puertos se pondrán automáticamente, asi que le daremos a `Continuar` sin cambiar nada.

  ![](img/31.png)

- Seleccionamos `Conexión Estándard` y continuar.

  ![](img/32.png)

- En el paso siguiente que es la `Configuración de la fuente de datos`, tendremos que tener puesto en `Drivers Predefinidos -> MySQL`, en la URL de la base de datos , pondremos lo siguiente: `jdbc:mysql://localhost:3306/openfire`, y en el usuario tiene que ser el user con privilegios, en este caso pondremos `root` con su respectiva contraseña.

- En la configuración de perfil, la pondremos por defecto.

  ![](img/36.png)

- Pondremos la cuenta del administrador que vamos a utlizar para iniciar sesión en `Openfire`.

  ![](img/42.png)

- Veremos en la base de datos de openfire que hemos creado nosotros, que el usuario que se ha guardado es el ``admin``, en vez de ``admin_diego``.

  ![](img/44.png)

- La verdad que nose el porque pero inicaremos sesión con el nombre de usuario ``admin`` y la contraseña que pusimos en el paso final de la cuenta del administrador.

  ![](img/47.png)

  ![](img/43.png)

[Volver](#0)

### **6. Comprobamos desde el servidor el acceso con el usuario admin.** <a id="6"></a>

  ![](img/47.png)

  ![](img/43.png)

[Volver](#0)

### **7. Una vez instalado el servidor OpenFire, vamos a descargar e instalar un cliente de Mensajería, en este caso Spark.** <a id="7"></a>

  ![](img/49.png)

  ![](img/51.png)

  ![](img/52.png)

  ![](img/53.png)

  ![](img/54.png)

  ![](img/55.png)

  ![](img/56.png)

[Volver](#0)

### **8. Ahora vamos a crear dos nuevos usuarios en OpenFire (además del administrador) para poder mantener una conversación entre cliente y servidor** <a id="8"></a>

  ![](img/57.png)

  ![](img/58.png)

  ![](img/59.png)

  ![](img/60.png)

  ![](img/61.png)

[Volver](#0)

### **9. Comprobamos el funcionamiento de Spark** <a id="9"></a>

- Antes de nada tenemos que hacer lo siguiente:

  - Iniciamos sesión con el usuario pepe en el servidor y nos saldrá lo siguiente:

    ![](img/62.png)

    ![](img/63.png)

  - Vemos que nos sale el siguiente error:

    ![](img/64.png)

  - Para solucionarlo, tedremos que ir a la parte de abajo y seleccionar `Avanzado`, una vez hecho esto, se nos abrirá una ventana de la Configuración Avanzada de Spark.

    ![](img/65.png)

  - Iremos a la parte de seguridad, `Security` y activamos la siguiente opción:

    ![](img/66.png)

- Este paso lo realice con un compañero de clase , Salvador Gónzalez , él me ayudo a establecer una conversación con el usuario benito, con lo cuál él actuaba como cliente y yo como servidor.

  ![](img/67.png)

- Le envió la solicitud de amistad.

  ![](img/68.png)

  ![](img/73.png)

  ![](img/74.png)

- Una vez hemos aceptado los dos la solicitud de amistad, los usuarios saldrán en línea.

  ![](img/69.png)

  ![](img/70.png)

- Establecemos una conversación con lo usuarios creados anteriormente.

  ![](img/71.png)

  ![](img/72.png)

[Volver](#0)
