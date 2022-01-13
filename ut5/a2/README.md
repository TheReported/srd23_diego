<center>

# **<font color="#F06F69">Instalación y Configuración de un Servidor de Correo en Ubuntu </font>**

</center>

***Nombre:*** Diego Peraza Cabo
<br>
***Curso:*** 2º ASIR



## **Índice** <a id="0"></a>

  + [1. Instalar servicio SMTP en Linux, utilizando el servidor Postfix.](#1)
    + [1.1 Descargar, instalar y configurar Postfix.](#1.1)
    + [1.2 Comprobar servicio (y puerto) SMTP activo y a la escucha.](#1.2)
    + [1.3 Realizar una prueba de envío de mensaje entre dos usuarios del sistema mediante telnet.](#1.3)
    + [1.4 Comprobar de que el usuario ha recibido el mensaje, para ello debemos mirar en la carpeta `/var/spool/mail`.](#1.4)
    + [1.5 Instalar un cliente de correo, en este caso el programa Evolution, en una MV que actué como cliente.](#1.5)
    + [1.6 Crear dos nuevas entradas en /etc/hosts: `smtp.miempresa.com` y `pop.miempresa.com`](#1.6)
    + [1.7 Realizar envió de correos. Comprobar la recepción de correos en la carpeta `/var/mail`.](#1.7)
  + [2. Instalar servicio IMAP y servidor Correo Web SquirrelMail.](#2)
    + [2.1 Instalar servicio IMAP.](#2.1)
    + [2.2 Comprobar servicio (y puerto) IMAP activo y a la escucha.](#2.2)
    + [2.3 Instalación de la aplicación de correo web SquirrelMail.](#2.3)
    + [2.4 Configuración de SquirrelMail.](#2.4)
    + [2.5 Acceder desde el servidor y cliente al gestor de correo SquirrelMail vía HTTP.](#2.5)
    + [2.6 Comprobamos que los mensajes enviados desde ambas cuentas se siguen encontrando en los respectivos buzones de los usuarios en la carpeta `/var/mail`.](#2.6)
  + [3. Instalar servicio POP3](#3)

### **<font color="#F06F69"> 1. Instalar servicio SMTP en Linux, utilizando el servidor Postfix. </font>** <a id="1"></a>

- **1.1 Descargar, instalar y configurar Postfix.** <a id="1.1"></a>

  ![](img/3.png)

  ![](img/1.png)

  ![](img/2.png)

  ![](img/4.png)

- **1.2 Comprobar servicio (y puerto) SMTP activo y a la escucha.** <a id="1.2"></a>

  ![](img/6.png)

  ![](img/7.png)

  ![](img/8.png)

- **1.3 Realizar una prueba de envío de mensaje entre dos usuarios del sistema mediante telnet.** <a id="1.3"></a>

  ![](img/9.png)

- **1.4 Comprobar de que el usuario ha recibido el mensaje, para ello debemos mirar en la carpeta `/var/spool/mail`.** <a id="1.4"></a>

  ![](img/10.png)

- **1.5 Instalar un cliente de correo, en este caso el programa Evolution, en una MV que actué como cliente.** <a id="1.5"></a>

  ![](img/11.png)

- Comprobamos de que se ha instalado correctamente.

  ![](img/12.png)

- **1.6 Crear dos nuevas entradas en /etc/hosts: `smtp.miempresa.com` y `pop.miempresa.com`** <a id="1.6"></a>

  ![](img/13.png)

- **1.7 Realizar envió de correos. Comprobar la recepción de correos en la carpeta `/var/mail`.** <a id="1.7"></a>

  ![](img/16.png)

  ![](img/18.png)

[Volver](#0)

### **<font color="#F06F69"> 2. Instalar servicio IMAP y servidor Correo Web SquirrelMail. </font>** <a id="2"></a>

- **2.1 Instalar servicio IMAP.** <a id="2.1"></a>

  ![](img/19.png)

- **2.2 Comprobar servicio (y puerto) IMAP activo y a la escucha.** <a id="2.2"></a>

  ![](img/20.png)

  ![](img/21.png)

  ![](img/22.png)

- **2.3 Instalación de la aplicación de correo web SquirrelMail.** <a id="2.3"></a>

- Descargaremos la aplicación desde su web, ya que SquirrelMail no está en el repositorio de Ubuntu.

  ![](img/23.png)

- Descomprimimos el paquete.

  ![](img/24.png)

- Ahora moveremos la carpeta de la aplicación hacia `/var/www/html`, cambiaremos el propietario y los permisos de la carpeta y a de las subcarpetas, además le cambiaremos el nombre de la carpeta.

  ![](img/25.png)

- **2.4 Configuración de SquirrelMail.** <a id="2.4"></a>

- Con el siguiente comando empezaremos la configuración: `sudo perl /var/www/html/squirrelmail/config/conf.pl`.

  ![](img/27.png)

- Seleccionaremos la opción `2. Server Settings`, seguidamente la opción `1. Domain` e introducimos el dominio de `miempresa.com`.

  ![](img/26.png)

- Después le damos a guardar y por último vamos a configurar las opciones generales.

  ![](img/28.png)

- Una vez terminado de configurar el programa SquirrelMail, saldremos de la configuración.

  ![](img/29.png)

- **2.5 Acceder desde el servidor y cliente al gestor de correo SquirrelMail vía HTTP.** <a id="2.5"></a>

- Ahora accedemos al servidor a través del navegador introduciendo la URL `localhost/squirrelmail`

  ![](img/30.png)

- También podremos acceder por el dominio de `miempresa.com`.

  ![](img/65.png)

- Accedemos desde una MV cliente, vía HTTP, al gestor de correo SquirrelMail instalado en el servidor.

  ![](img/31.png)

- Enviamos y recibimos correos entre las dos cuentas creadas.

  - Cliente

    ![](img/32.png)

  - Servidor

    ![](img/34.png)

  ![](img/61.png)

- **2.6 Comprobamos que los mensajes enviados desde ambas cuentas se siguen encontrando en los respectivos buzones de los usuarios en la carpeta `/var/mail`.**  <a id="2.6"></a>

  ![](img/64.png)

  ![](img/63.png)

  [Volver](#0)

### **<font color="#F06F69"> 3. Instalar servicio POP3 </font>** <a id="3"></a>



[Volver](#0)
