# **Instalación y Configuración de un Servidor Multimedia (Audio) en Linux**

***Nombre:*** Diego Peraza Cabo
<br>
***Curso:*** 2º ASIR

  ![](img/42.png)

## **Índice** <a id="0"></a>

  + [1. Instalación y configuración de IceCast](#1)
  + [2. Instalación y configuración de Vorbis Ices2](#2)
  + [3. Comrpobamos su funcionamiento desde el servidor](#3)
  + [4. Comprobamos su funcionamiento desde el cliente](#4)
  + [5. Investigación de Gerbera](#5)
    + [5. 1 Instalación y configuración de Gerbera en el servidor.](#5.1)
    + [5.2 Comprobamos su funcionamiento.](#5.2)

### **1. Instalación y configuración de IceCast** <a id="1"></a>

- Descargamos e instalamos y configuramos el paquete `Icecast`.

  ![](img/6.png)

- Durante la instalación nos saldrá un menu de sí queremos configurar ahora el paquete. En mi caso le di a que sí pero puedes configurarlo más tarde perfectamente.

  ![](img/1.png)

  ![](img/2.png)

  ![](img/3.png)

  ![](img/4.png)

  ![](img/5.png)

- No nos hará falta editar el fichero `/etc/icecast2/icecast.xml` si realizamos la configuración anterior.

- Podemos ver que si hacemos el paso anterior se guardan los datos que introducimos.

  ![](img/7.png)

- Editamos el fichero ``/etc/default/icecast2``.

  ![](img/8.png)

- Iniciamos el servicio correspondiente a IceCast y comprobamos su estado.

  ![](img/9.png)

[Volver](#0)

### **2. Instalación y configuración de Vorbis Ices2** <a id="2"></a>

- Descargamos e instalamos el paquete `Vorbis Ices2`.

  ![](img/10.png)

- Creamos el directorio `/etc/ices2` para el codificador y copiamos el fichero de configuración por defecto.

  ![](img/11.png)

- Editamos el fichero de configuración del codificador que acabamos de copiar y establecemos los parámetros de nuestra emisora mediante las siguientes etiquetas:

  ![](img/12.png)

  ![](img/13.png)

- Ahora tendremos que recopilar ficheros de audio en formato .ogg y copiarlos en el directorio `/tmp/musica` que vamos a crear.

  ![](img/14.png)

- Generamos la lista de reproducción.

  ![](img/15.png)

- Creamos el directorio log de ices2 y ejecutamos el codificador en background.

  ![](img/16.png)

- Si vemos que nos sale `unable to open log /var/log/ices/ices.log`, solo tendremos que cambiar la siguiente línea del fichero de configuración.

  ![](img/27.png)

- Comprobamos.

  ![](img/28.png)

[Volver](#0)

### **3. Comrpobamos su funcionamiento desde el servidor** <a id="3"></a>

- Procedemos a acceder al navegador web con la siguiente URL `miempresa.com:8000/admin/`.

  ![](img/29.png)

- Comprobamos las opciones globales del servidor.

  ![](img/20.png)

- Comprobamos el punto de montaje.

  ![](img/22.png)

- Accedemos vía web a la lista de reproducción desde el propio servidor.

  ![](img/26.png)

[Volver](#0)

### **4. Comprobamos su funcionamiento desde el cliente** <a id="4"></a>

  ![](img/24.png)

  ![](img/25.png)

[Volver](#0)

### **5. Investigación de Gerbera** <a id="5"></a>

- En principio busqué información sobre el programa `GMedia Server`, pero era muy antiguo y no me funcionaba. Entonces descubrí otro programa que es parecido.

  ![](img/30.png)

  ![](img/43.png)

- **Gerbera** es un potente servidor de medios **UPnP** (Universal Plug and Play) rico en características con una interfaz de usuario web agradable e intuitiva.

  ![](img/41.png)

- Nos va permitir transmitir medios digitales (vídeos, imágenes, audio, etc.) a través de una red doméstica y reproducirlo en diferentes tipos de dispositivos compatibles con **UPnP**, desde teléfonos móviles a tabletas y muchos más.

#### **5. 1 Instalación y configuración de Gerbera en el servidor.** <a id="5.1"></a>

- Instalamos el programa.

  ![](img/32.png)

- Iniciamos y habilitamos Gerbera. Además comprobamos el estado.

  ![](img/33.png)

- Editamos el fichero de configuración que se encuentra en `/etc/gerbera/config.xml`.

  ![](img/35.png)

  ![](img/34.png)

- Reiniciamos el servicio.

  ![](img/36.png)

#### **5.2 Comprobamos su funcionamiento.** <a id="5.2"></a>

- Entramos al navegador web y nos dirigimos a la siguiente URL: `IP-DEL-SERVIDOR:49152`(También puede ser un nombre DNS).

  ![](img/37.png)

- Añadimos algún archivo.

  ![](img/39.png)

- Comprobamos.

  ![](img/38.png)

[Volver](#0)
