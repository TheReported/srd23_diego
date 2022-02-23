# **Instalación y configuración del Servicio VoIP en Linux**

***Nombre:*** Diego Peraza Cabo
<br>
***Curso:*** 2º ASIR

  ![](img/0.png)

## **Índice** <a id="0"></a>

+ [1. Instalación de ``Asterisk``](#1)
+ [2. Configuración de ``Asterisk``](#2)
+ [3. Instalación de ``MicroSIP`` en Cliente Windows](#3)
+ [4. Instalación y configuración de ``MizuDroid SIP VOIP Softphone`` en el teléfono móvil](#4)
+ [5. Comprobación del funcionamiento de Asterisk con los clientes](#5)


### **1. Instalación de Asterisk** <a id="1"></a>

- Instalamos el programa.

  ![](img/1.png)

  ![](img/2.png)

- Comprobamos que podemos entrar al programa.

  ![](img/3.png)

- Comprobamos los archivos de configuración en el directorio `/etc/asterisk`.

  ![](img/4.png)

[Volver](#0)

### **2. Configuración de Asterisk** <a id="2"></a>

- Una vez hemos realizado los pasos anteriores, pasaremos con la configuración. Para ello cambiamos el nombre de los archivos siguientes con la terminación `.backup` y creamos unos nuevos con el nombre que tenían antes.

  - Fichero `sip.conf`

    ![](img/5.png)

    - Contenido

      ![](img/6.png)

  - Fichero `extensions.conf`

    ![](img/7.png)

    - Contenido

      ![](img/8.png)

  - Fichero `voicemail.conf`

    ![](img/9.png)

    - Contenido

      ![](img/10.png)

- Cunado hayamos terminado de configurar todo, entramos al programa y hacemos un `reload` para que cargue los ficheros de configuración que hemos creado.

  ![](img/11.png)

- Salimos y volvemos a entrar al programa, y comprobamos los clientes con el siguiente comando: `sip show peers`.

  ![](img/12.png)

[Volver](#0)

### **3. Instalación de MicroSIP en Cliente Windows** <a id="3"></a>

- Vamos a la máquina cliente y descargamos e instalamos el programa.

  ![](img/13.png)

- Una vez dentro del programa pondremos una cuenta con los siguientes datos. Una vez hemos puesto todos los datos necesarios le damos a `Guardar`.

  ![](img/14.png)

- Comprobamos de que nos hemos conectado correctamente.

  ![](img/15.png)

[Volver](#0)

### **4. Instalación y configuración de ``MizuDroid SIP VOIP Softphone`` en el teléfono móvil** <a id="4"></a>

- Vamos a la ``Play Store`` , buscamos e instalamos el programa.

  ![](img/19.jpeg)

- Entramos a la aplicación.

  ![](img/20.jpeg)

- Ponemos los datos necesarios, como la dirección IP del servidor, el usuario y la contraseña.

  ![](img/21.jpeg)

- Una vez puesto todos los datos, nos saldrá que estamos logeados correctamente, ya que pone `Registered` en la parte superior izquierda.

  ![](img/24.jpeg)

[Volver](#0)

### **5. Comprobación del funcionamiento de Asterisk con los clientes** <a id="5"></a>

- Ahora llamamos al cliente Windows con el cliente del móvil, indicando el número de la extensión.

  ![](img/22.jpeg)

  ![](img/23.jpeg)

- Comprobamos en el cliente Windows y en el servidor Linux de que está recibiendo la llamada.

  ![](img/16.png)

- Aceptamos la llamada y vemos que cuando hablamos emite sonido.

  ![](img/17.png)

- Por último, iremos al programa de `Asterisk` en el Servidor y comprobamos que en los clientes (peers), se nos ha puesto la dirreción IP de los dispositivos.

  ![](img/18.png)

[Volver](#0)
