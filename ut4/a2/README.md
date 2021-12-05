# **Informe FTP - Prácticas Windows y Linux**

- ##  **Instalación y Configuración de un Servidor FTP - Windows**

#### **1. Instalar Servicio FTP en Windows 2016 Server, a través de Agregar roles y características (IIS)**

![](img/windows/001.png)

![](img/windows/002.png)

![](img/windows/003.png)

![](img/windows/004.png)

![](img/windows/005.png)

#### **2. Acceder a la creación y configuración de Sitios FTP por medio de la Administración de IIS.**

![](img/windows/054.png)

![](img/windows/055.png)

- **Aislamiento de usuario FTP:** a fin de definir el modo de aislamiento de usuario para el sitio FTP. El aislamiento de usuario FTP es una solución que permite a los proveedores de acceso a Internet (ISP) ofrecer a sus clientes directorios FTP individuales para cargar contenido.

- **Autenticación FTP:** configurar los métodos de autenticación que los clientes FTP pueden utilizar para obtener acceso al contenido. Puede ordenar esta lista por nombre, estado o tipo haciendo clic en el encabezado de columna adecuado.

- **Compatibilidad con el firewall de FTP:** a fin de modificar la configuración de las conexiones pasivas cuando los clientes FTP se conecten a un servidor FTP ubicado detrás de un firewall.

- **Configuración SSL de FTP:** a fin de administrar el cifrado para las transmisiones de canal de control y canal de datos entre el servidor FTP y los clientes.

- **Examen de directorios FTP:** a fin de modificar la configuración de contenido para examinar un directorio en el servidor FTP. Cuando se configura el examen de directorios, todos los directorios usan la misma configuración.

- **Filtrado de solicitudes de FTP:** definir la configuración del filtrado de solicitudes para su sitio FTP. El filtrado de solicitudes de FTP es una característica de seguridad que permite a los proveedores de acceso a Internet (ISP) y a los proveedores de servicios de aplicaciones restringir el comportamiento de los protocolos y del contenido.

- **Mensajes de FTP:** modificar la configuración de los mensajes que se envían cuando un usuario se conecta a su sitio FTP.

- **Registro FTP:** para configurar las características de registro en el nivel de sitio o servidor, y para configurar los valores de registro.

- **Reglas de autorización:** configurar reglas para autorizar a los usuarios a obtener acceso a sitios FTP.

- **Restricciones de direcciones IPv4 y dominios de FTP:** definir y administrar reglas que permitan o denieguen el acceso al contenido de una dirección IPv4, un intervalo de direcciones IPv4 o un nombre o nombres de dominio específicos.

- **Restricciones de intento de inicio de sesión de FTP:** característica para proteger el servidor FTP frente ataques basados en red.

#### **3. Crear tres nuevos sitios FTP (en todos ellos se debe poder acceder a través de las IPs del servidor y, en algún caso, de un nombre DNS ftp.tudominio.ext)**

- **Sitio Web 1 - FTP**

Creamos y configuramos el sitio web 1 - FTP:

![](img/windows/006.png)

![](img/windows/007.png)

![](img/windows/009.png)

Tratamos de acceder al sitio web:

  - Consola

![](img/windows/010.png)

  - Explorador de archivos

![](img/windows/011.png)

![](img/windows/012.png)

  - Navegador Web

![](img/windows/013.png)

![](img/windows/014.png)

  - Navegador Web - Cliente

![](img/windows/015.png)

  - Explorador de archivos - Cliente

![](img/windows/021.png)

![](img/windows/020.png)

  - WinSCP - Cliente

Instalación del software WinSCP

![](img/windows/016.png)

![](img/windows/017.png)

![](img/windows/018.png)

![](img/windows/019.png)

Establecemos la conexión

![](img/windows/022.png)

![](img/windows/023.png)

****
**OJO!! DETENDREMOS EL SITIO WEB 1 PARA QUE EL SIGUIENTE SITO WEB FUNCIONE CORRECTAMENTE**
****

- **Sitio Web 2 - FTP**

Creamos y configuramos el sitio web 2 - FTP:

![](img/windows/024.png)

![](img/windows/025.png)

![](img/windows/026.png)

Creamos un usario que pertenezca al dominio

![](img/windows/027.png)

Tratamos de acceder al sitio web:

  - Explorador de archivos

![](img/windows/030.png)

  - Navegador web

![](img/windows/031.png)

![](img/windows/032.png)

  - Explorador de archivos - Cliente

![](img/windows/029.png)

![](img/windows/028.png)

  - Navegador web - Cliente

![](img/windows/033.png)

![](img/windows/034.png)

  - Conexión SSL desde WinSCP - Cliente

![](img/windows/035.png)

![](img/windows/036.png)

![](img/windows/037.png)

****
**OJO!! DETENDREMOS EL SITIO WEB 2 PARA QUE EL SIGUIENTE SITO WEB FUNCIONE CORRECTAMENTE**
****

- **Sitio Web 3 - FTP**

Creamos y configuramos el sitio web 3 - FTP:

![](img/windows/038.png)

![](img/windows/039.png)

![](img/windows/040.png)

Cambiamos el nombre de host:

![](img/windows/041.png)

- Creamos un nuevo host en nuestro dominio `miEmpresa.com`.

![](img/windows/042.png)

- Comprobamos desde cliente:

![](img/windows/043.png)

![](img/windows/044.png)

No podremos escribir ni borrar nada, pero si leer.

![](img/windows/046.png)

![](img/windows/045.png)

![](img/windows/048.png)

- Comprobamos desde servidor:

![](img/windows/049.png)

#### **4. En un principio es posible que debas detener un sitio ftp para que pueda iniciarse otro. Tras comprobar el funcionamiento por separado de los sitios, encontrar una solución para que nuestro servidor ofrezca varios sitios FTP simultáneamente.**

- Para ello pondremos un puerto diferente a casa sitio web.

![](img/windows/053.png)

- ##  **Instalación y Configuración de un Servidor FTP - Linux**

#### **0. Preparativos**

- Ip del servidor:

![](img/linux/011.png)

- Editamos el fichero `/etc/hosts` del cliente.

![](img/linux/014.png)

#### **1. Instalamos el servicio SSH en el servidor de Linux**

![](img/linux/001.png)

#### **2. Creamos dos usuarios en el sistema, con diferentes privilegios y niveles de acceso al filesystem.**

![](img/linux/005.png)

![](img/linux/006.png)

![](img/linux/007.png)

![](img/linux/008.png)

#### **3. Comprobamos, desde una máquina cliente, acceso de los usuarios mediante ssh.**

![](img/linux/009.png)

![](img/linux/010.png)

#### **4. Tratar de ejecutar una aplicación gráfica del servidor de forma remota, desde el cliente, mediante ssh.**

![](img/linux/012.png)

![](img/linux/016.png)

![](img/linux/013.png)

![](img/linux/015.png)

#### **5. Acceder, también desde el cliente, mediante sftp (ftp seguro, incluido en el paquete ssh) al sistema de ficheros del servidor y probar acceso, carga y descarga de archivos con ambos usuarios.**

![](img/linux/017.png)

![](img/linux/018.png)

![](img/linux/019.png)

#### **6. Realizar varias copias de archivos hacia / desde el servidor mediante scp, utilizando también los dos usuarios creados anteriormente.**

![](img/linux/020.png)

![](img/linux/021.png)

![](img/linux/022.png)

#### **7. Instalar el paquete proftpd.**

![](img/linux/023.png)

#### **8. Investigar y editar el fichero de configuración /etc/proftpd/proftpd.conf buscando información en Internet.**

![](img/linux/024.png)

![](img/linux/025.png)

#### **9. Tratar de conectar al servicio ftp gestionado por proftpd tanto desde el servidor como desde un cliente.**

- Cliente

![](img/linux/026.png)

- Servidor

![](img/linux/027.png)

#### **10. Desde la máquina cliente, probar el acceso al ftp mediante los usuarios creados y realizando diferentes operaciones de listado, subida y descarga de archivos.**

![](img/linux/028.png)

![](img/linux/029.png)

#### **11. Informar sobre la configuración, uso y funcionamiento de proftpd.**

- ProFTPd es un popular servidor FTP para Linux. ProFTPd es un programa que fue escrito para ser un software poderoso y configurable, por lo que no es necesariamente el servidor de FTP más liviano disponible, pero si el más conocido y el más usado. en servidores.

- El archivo de configuración principal de proFTPd se encuentra en ``/etc/proftpd/proftpd.conf``. Desde aquí deberemos configurar la mayoría de los aspectos de nuestro servidor FTP.

  - **AuthPAM off:** Para deshabilitar la autentificacion PAM, es decir para que no ´
autentifique a los usuarios reales.

  - **RequireValidShell off:** Requiere una Shell valida para iniciar secci ´ on. Las shell ´
validas son las que estan en /etc/shells.

  - **DefaultRoot ˜:** Para que cuando un usuario entra en el servidor ftp, no pueda
salir de su home a drectorios superiores.

  - **SQLBackend:** Con esta directiva indicamos el servidor de base de datos que
vamos a utilizar. En nuestro caso mysql.

  - **SQLAuthTypes:** En tipos de identificacion tenemos (entre otras) PlainText
(texto plano), Crypt (como en el /etc/shadow) o Backend (utiliza el sistema
propio de la base de datos). Aqu´ı depende de con que vayamos a cifrar las ´
contrasenas en la base de datos. Si lo haces con CRYPT() usa Crypt, si usas ˜
PASSWORD() usa Backend.

  - **SQLAuthenticate:** Con esta directiva decimos quien tiene que identificarse
en MySQL. Podemos seleccionar grupos o usuarios, yo me limito a decirque todos: on.

  - **SQLConnectInfo:** Se indica los datos de la conexion a la base de datos.

  - **SQLDefaultGID y SQLDefaultUID:** Indican, respectivamente, los GID y UID
que se usan por defecto en caso de no poner nada en la tabla.

  - **SQLMinUserGID y SQLMinUserUID:** Indican el UID y el GID m´ınimo que
han de tener los usuarios para poder loguear

  - **SQLGroupInfo:** Se indica el nombre de la tabla que posee la informacion de ´
los grupos, as´ı como los nombres de los campos.

  - **SQLUserInfo:** Se indica el nombre de la tabla que posse la informacion de los ´
usuarios, as´ı como los nombres de los campos.

  - **SQLUserWhereClause:** Indica una condicion a la hora de seleccionar los cam- ´
pos. Nosotros la usamos para controlar si una cuenta esta activa o no.

  - **SQLLogFile:** Se indica el archivo de log donde se guarda la informacion ge- ´
nerada por el servidor al acceder a la base de datos.

- Una vez allí, buscaremos la línea comentada «DefaultRoot» y la descomentamos borrando la almohadilla #. Esto nos va a permitir que cuando cada usuario acceda a su cuenta del FTP, estos accederán directamente a su carpeta «home» y no podrán salir de ese directorio.
