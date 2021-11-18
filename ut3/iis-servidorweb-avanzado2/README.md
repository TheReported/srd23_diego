# **Informe IIS - Servidor Web avanzad - Instalación de PHP, MySQL y PHPMyAdmin**

### **0. Preparativos**

| Programas       | Versiones      |
| :------------- | :------------- |
| PHP      | 5.3.18       |
| MySQL    | 5.5.2        |
| PHPMyAdmin  | 4.4.15.10         |
| Drupal      | 6.38 |

### **1. Instalación de PHP**

![](img/009.png)

![](img/010.png)

![](img/011.png)

![](img/012.png)

![](img/013.png)

- Para seguir con la instalación debemos agregar el rol de ``CGI`` que esta dentro de nuestro Servidor Web (IIS).

![](img/014.png)

![](img/015.png)

![](img/016.png)

- Volvemos con la instalación de PHP.

![](img/017.png)

![](img/018.png)

- Una vez tengamos PHP instalado, configuraremos nuestro IIS para que admita el fichero index.php por defecto .

![](img/064.png)

![](img/019.png)

### **2. Comprobamos que la instalación de PHP es correcta**

![](img/020.png)

![](img/021.png)

### **3. Instalación de MYSQL**

![](img/039.png)

![](img/040.png)

![](img/041.png)

![](img/042.png)

![](img/043.png)

![](img/044.png)

![](img/045.png)

![](img/046.png)

![](img/047.png)

![](img/048.png)

### **4. Instalación de PHPMyAdmin**

![](img/065.png)

- Descomprimiremos los ficheros de PHPMyAdmin en la carpeta correspondiente. Además crearemos un nuevo sitio web asociado a `phpmyadmin.miEmpresa.com`.

![](img/037.png)

![](img/036.png)

![](img/051.png)

![](img/050.png)

- Comprobación

![](img/052.png)

![](img/053.png)

- Crearemos una base de datos y un usuario denominados `cms` con todos los privilegios para la mísma base de datos:

![](img/069.png)

![](img/070.png)

![](img/075.png)

### **5. Instalación del Servidor FTP FileZilla**

![](img/054.png)

![](img/055.png)

![](img/056.png)

![](img/057.png)

![](img/058.png)

![](img/066.png)

![](img/060.png)

![](img/067.png)

### **6. Crear usuario `ftpuser` en el Servidor FTP y crear nuevo  registro DNS que permita acceder a nuestro sitio FTP a través de la dirección ``ftp.miEmpresa.com``**

![](img/063.png)

![](img/068.png)

![](img/062.png)

- **¡¡ERROR EN EL SERVIDOR FTP FILEZILLA!!**

![](img/102.png)

### **7. Instalación CMS Drupal**

- Descargamos y descomprimimos los archivos:

![](img/076.png)

![](img/077.png)

- Configurar idioma a español:

![](img/082.png)

![](img/083.png)

- Copiamos el archivo `default.setting.php` y lo pegamos en el mismo sitio pero con el nombre de  `settings.php`.

![](img/103.png)

- Vamos al navegador para comenzar con la instalación:

![](img/084.png)

![](img/085.png)

![](img/086.png)

![](img/087.png)

![](img/088.png)

![](img/089.png)

### **8. Configuración y creación del sitio Drupal**

- Instalar módulo `gtranslate`:

![](img/079.png)

![](img/081.png)

![](img/091.png)

![](img/092.png)

![](img/093.png)

![](img/104.png)

- Instalar y configurar temas Marinelli, Zen y Fusion:

![](img/094.png)

![](img/095.png)

![](img/097.png)

- Crear dos páginas de contenido:

![](img/098.png)

![](img/099.png)

![](img/100.png)

![](img/101.png)

![](img/105.png)
