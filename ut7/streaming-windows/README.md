# **Instalación de un servicio de Streaming en Windows 2016 Server**

***Nombre:*** Diego Peraza Cabo
<br>
***Curso:*** 2º ASIR

## **Índice** <a id="0"></a>

  + [1. Instalación de Unreal Media Server](#1)
  + [2. Comprobación en el servidor](#2)
  + [3. Comprobación en el cliente](#3)

### **1. Instalación de Unreal Media Server** <a id="1"></a>

- Descargamos el programa `Unreal Media Server` en la siguiente página web.

  ![](img/1.png)

  ![](img/2.png)

- Seleccionamos el destino que queramos para extraer los archivos. En mi caso puse `C:\UMediaServer`.

  ![](img/3.png)

- Vamos a la carpeta donde se ha descomprimido todos los archivos y daremos click al ejecutable.

  ![](img/4.png)

- Le daremos a ejecutar y pasaremos con la instalación de `Unreal Media Server`. Seguiremos los pasos indicados en las fotos.

  ![](img/5.png)

- Le damos a `Next`.

  ![](img/6.png)

- Aceptamos los términos y condiciones.

  ![](img/7.png)

- Dejamos la ubicación que hay por defecto.

  ![](img/8.png)

- Le damos a `Next`.

  ![](img/9.png)

- Esperamos a que se instale.

  ![](img/10.png)

  ![](img/12.png)

- Una vez hemos instalado el programa, daremos click al símbolo de Windows y buscamos el programa para iniciarlo.

    ![](img/13.png)

- Una vez dentro del programa, vemos que en la carpeta `File resources -> MediaRoot` tenemos dos archivos de prueba. En esta carpeta podremos poner los videos que queramos pero solo se mostrarán los videos que tengan de formato `.avi`.

    ![](img/14.png)

[Volver](#0)

### **2. Comprobación en el servidor** <a id="2"></a>

- Entramos en la siguiente URL: `mms://IP-DEL-SERVIDOR/MediaRoot/test.avi`, y elegimos el `Reproductor de Windows Media`.

  ![](img/15.png)

  ![](img/16.png)

- Comprobamos.

  ![](img/17.png)

[Volver](#0)

### **3. Comprobación en el cliente** <a id="3"></a>

- Para hacer la comprobación desde el cliente, primero tenemos que descargarnos `VLC` o algún programa parecido.

- Una vez realizado el paso anterior, vamos al navegador web `Firefox` y pondremos la siguiente URL `mms://IP-DEL-SERVIDOR/MediaRoot/test.avi`.

    ![](img/22.png)

- Elegimos `VLC` como aplicación para abrir el vídeo.

    ![](img/20.png)

- Comprobamos.

    ![](img/21.png)

[Volver](#0)
