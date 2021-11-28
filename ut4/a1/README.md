# **Práctica Servidor Web Apache - Linux**

### **Configurar MV Ubuntu o similar en adaptador Puente**

![](img/049.png)

![](img/050.png)

### **Apache**

- **Instalar Apache:**

![](img/002.png)

![](img/001.png)

- **Comprobar la carpeta raíz sitio web.**

![](img/003.png)

- **Comprobar acceso a localhost o 127.0.0.1:**

![](img/004.png)

![](img/005.png)

- **Editar el fichero `/etc/hosts` y añadir la siguiente línea.**

![](img/007.png)

- **Reiniciamos Apache.**

![](img/008.png)

- **Comprobar acceso.**

![](img/009.png)

- **Error + Access logs:**

![](img/010.png)

### **PHP**

- **Instalar PHP 7.4 y el paquete `libapache2-mod-php7.4`:**

![](img/011.png)

![](img/012.png)

![](img/014.png)

- **Comprobar acceso a index.php:**

![](img/069.png)

![](img/070.png)

### **Crear Hosts Virtuales**

- **En este punto asociaremos carpetas con sitios web y modifciaremos el archivo `/etc/apache2/sites-available/000-default.conf`.**

![](img/016.png)

![](img/017.png)

- **Pondremos el ``ServerName`` que acabamos de poner en el fichero de configuración , en el archivo de ``/etc/hosts``.**

![](img/018.png)

- **Comprobamos de que hay un index.html creado en la carpeta ``/var/www/empleados``.**

![](img/019.png)

- **Comprobamos en el navegador web poniendo ``empleados.miempresa.com``.**

![](img/020.png)

### **Configurar sitio web seguro `pagos`**

- **Generamos certificado autofirmado y creamos una carpteta `/etc/apache2/ssl` y dentro de esta carpeta meteremos los siguientes ficheros generados:**

![](img/035.png)

![](img/036.png)

![](img/072.png)

- **Crearemos un archivo de configuración nuevo que solo estará el Host Virtual ``pagos``.**

![](img/071.png)

- **Habilitamos el módulo SSL Apache y el sitio ``pagos``.**

![](img/037.png)

- **Comprobamos que hay contenido en la carpeta `/var/www/empleados/pagos`**

![](img/031.png)

- **Reiniciamos Apache:**

![](img/038.png)

- **Comprobamos en el navegador web.**

![](img/034.png)

### **Acceso a carpetas privadas**

- **Autenticación mediante ``.htaccess``:**

![](img/066.png)

![](img/067.png)

- **Carpeta Claves:**

![](img/065.png)

- **Archivo de configuración de empleados:**

![](img/068.png)

- **Comprobación en el navegador web.**

 - **Empleado 1**

![](img/062.png)

![](img/042.png)

 -**Empleado 2**

![](img/063.png)

![](img/064.png)

 - **Empleado 3**

![](img/082.png)

![](img/083.png)

### **MySQL**

- **Instalamos MySQL:**

![](img/043.png)

**- Instalar soporte php para MySQL:**

![](img/044.png)

### **phpMyAdmin**

- **Descargar la última versión (tar.gz) , descomprimiremos en `/var/www/phpMyAdmin`, asociada a un Host Virtual y comprobaremos el acceso.**

![](img/073.png)

![](img/074.png)

![](img/075.png)

![](img/076.png)

![](img/046.png)

![](img/079.png)

- **Si nos sale como un error o que nos falta algo por instalar, seguramente sea que no tenemos instalado algunos de los paquetes siguientes:**

  - `sudo apt-get install php7.4-mysqli`
  - `sudo apt-get install php7.4-xml`

### **Plataforma WordPress / Drupal / Joomla / Moodle / etc**

- **Creación de base de datos y usuarios necesarios.**

![](img/080.png)

![](img/081.png)

- **Instalación y configuración de SSH para acceso remoto desde cliente.**

![](img/051.png)

![](img/052.png)

![](img/054.png)

![](img/053.png)

- **Descarga, instalación y configuración plataforma WordPress.**

![](img/055.png)

![](img/078.png)

![](img/077.png)

![](img/056.png)

![](img/057.png)

![](img/059.png)

![](img/060.png)

![](img/061.png)
