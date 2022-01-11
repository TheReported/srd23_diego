<center>

# **Instalación y Configuración de Servicios de Correo Electrónico en Windows 2016 Server**

</center>

***Nombre:*** Diego Peraza Cabo
<br>
***Curso:*** 2º ASIR

## **Índice** <a id="0"></a>

  + [Instalación y Configuración de un Servidor de Correo SMTP](#1)
  + [Instalación y Configuración de hMailServer](#2)

### **Instalación y Configuración de un Servidor de Correo SMTP** <a id="1"></a>

#### **1. Instalación Servicio SMTP en Windows 2016 Server**

![](img/001.png)

![](img/002.png)

![](img/003.png)

![](img/004.png)

![](img/005.png)

![](img/006.png)

![](img/007.png)

![](img/008.png)

![](img/009.png)

#### **2. Configuración del Servicio SMTP**

- Una vez instalado el servicio SMTP, realizaremos las siguientes acciones para realizar la configuración del mismo.

![](img/010.png)

![](img/011.png)

![](img/012.png)

- Establecer como IP todas las asignadas.
- Limitar el número de conexiones a 50.
- Habilitar el registro en formato W3C, diario y en una carpeta determinada.

![](img/013.png)

![](img/014.png)

- Configurar envío de mensajes dentro de nuestra red local.

![](img/017.png)

![](img/016.png)

![](img/019.png)

- Establecer autenticación anónima.

![](img/020.png)

- Aplicamos los cambios.

![](img/021.png)

- Crea un dominio de tipo alias para disponer de cuentas en otro dominio.

![](img/023.png)

![](img/022.png)

![](img/024.png)

![](img/026.png)

- Comprobamos las carpetas de correo creados en ``C:\Inetpub\mailroot``.

![](img/114.png)

#### **3. Creamos una nueva zona de búsqueda directa.**

![](img/028.png)

#### **3.1. Comprobamos desde el cliente el acceso al nuevo nombre DNS creado en el servidor.**

![](img/030.png)

#### **4. Agregamos dos usuarios AD**

![](img/031.png)

![](img/032.png)

#### **5. Enviamos varios correos desde / hacia las diferentes cuentas y comprobar envío**

![](img/033.png)

#### **6. Establecemos autenticación básica de Windows.**

![](img/034.png)

![](img/035.png)

#### **7. Enviamos varios correos a cuenta personal de correo y a un usuario que no existe**

![](img/036.png)

![](img/037.png)

![](img/038.png)

![](img/039.png)

![](img/040.png)

[Volver](#0)

### **Instalación y Configuración de hMailServer**

#### **1. En primer lugar, hay que desinstalar el servicio SMTP de Windows 2016 Server.**

![](img/041.png)

![](img/042.png)

![](img/043.png)

![](img/044.png)

![](img/045.png)

![](img/046.png)

#### **2. Debes descargar e instalar en el servidor Windows 2016 server el servidor de correo hMailServer.**

![](img/047.png)

![](img/048.png)

![](img/049.png)

![](img/050.png)

![](img/051.png)

![](img/052.png)

![](img/053.png)

![](img/054.png)

![](img/055.png)

- Vemos que nos da un error al instalar el hMailServer asociado a la característica de .NET Framework 2.0. Para solucionar este problema instalaremos está característica en el servidor.

![](img/056.png)

![](img/057.png)

![](img/058.png)

![](img/059.png)

- Ahora ya podremos instalar el hMailServer.

![](img/060.png)

![](img/061.png)

- Pondremos una contraseña y finalizamos la instalación.

![](img/062.png)

![](img/063.png)

#### **3. Crea dos dominios denominados srd.edu y asir.edu.**

![](img/065.png)

![](img/066.png)

![](img/067.png)

![](img/068.png)

#### **4. Ejecuta los diagnósticos para ambos dominios y soluciona el error de backup asignando una carpeta para tal fin. Establece copia de seguridad de los mensajes.**

![](img/069.png)

![](img/070.png)

#### **5. Crea dos cuentas para dos usuarios ficticios en cada uno de los dos dominios. Investiga y configura las cuentas con diferentes opciones (cuota de disco, auto-reply, forwarding, signature, etc.)**

![](img/074.png)

- Yoda

![](img/075.png)

- Maul

![](img/076.png)

- Vader

![](img/077.png)

#### **6. Configura el servicio DNS para crear las entradas mail.srd.edu y mail.asir.edu que apunten a la dirección ip del servidor windows 2016.**

![](img/078.png)

#### **7. Realiza todas las opciones de configuración que consideres necesarias y/o convenientes. Consulta para ello los tutoriales cuyos enlaces se proporcionan (opciones de protocolos SMTP, POP e IMAP, rangos de IP, bloqueo de correo entrante, nombre de host, reenvío dominios remotos, blacklists, opciones de logging, etc.)**

- Configuraremos las opciones del servidor más convenientes.

- Creamos un rango de Ip's.

![](img/079.png)

![](img/080.png)

- Ponemos mensajes de bienvenida a los protocolos.

- **SMTP**

![](img/081.png)

- **IMAP**

![](img/082.png)

- Cambiamos el puerto del protocolo POP3.

![](img/083.png)

- Añadimos los logs de los protocolos.

![](img/084.png)

- Para hacer la comprobación necesitaremos instalarnos la característica `Cliente Telnet`.

![](img/085.png)

![](img/086.png)

- Comprobamos.

SMTP

![](img/087.png)

![](img/088.png)

POP3

![](img/089.png)

![](img/090.png)

IMAP

![](img/091.png)

![](img/092.png)


Logs

![](img/093.png)

- Ponemos el local hostname.

![](img/095.png)

#### **8. Configura en el cliente Windows un cliente de correo como thunderbird o Live Mail (en los ordenadores clientes) para acceder al servidor de correo instalado en Windows 2016.**

- Iniciamos sesión con todos los usuarios.

![](img/097.png)

![](img/098.png)

- Nos saldrá siempre el siguiente aviso pero le damos a que Aceptamos los riesgos y confirmamos.

![](img/099.png)

- Comprobamos de que están todas las cuentas.

![](img/100.png)

#### **9. Realiza prueba de envío y recepción de correos entre los diferentes usuarios, comprobando, además de envío y recepción correctas, el efecto de las opciones configuradas en las cuentas.**

Obiwan

![](img/101.png)

![](img/103.png)

Maul

![](img/104.png)

![](img/105.png)

Vader

![](img/106.png)

![](img/107.png)

- Esperamos un poco para la autorespuesta.

![](img/108.png)

#### **10. Crea una lista de distribución empleados asociada al dominio y añade a los dos usuarios de miempresa.com a ella.**

![](img/110.png)

![](img/116.png)

#### **11. Realiza prueba de envío y recepción de correos por medio de la lista de distribución.**

![](img/117.png)

![](img/118.png)

![](img/119.png)

Hasta aquí queda por concluida la actividad.

[Volver](#0)
