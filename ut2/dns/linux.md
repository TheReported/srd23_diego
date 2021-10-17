# **Práctica Servidor DNS Linux bind9**

### **0. Configuración de red de la MV Servidor DNS**

![](img-linux/029.png)

- Reiniciamos la MV y comrpobamos que se han guardado los cambios.

![](img-linux/003.png)

- Ahora en la MV Cliente, pondremos como servidor DNS a nuestro servidor para que haya comunicación entre ellos.

![](img-linux/027.png)

![](img-linux/028.png)

### **1. Indicaremos a Linux que el servidor DNS es él mismo ``(/etc/resolv.conf)``**

- `sudo nano /etc/resol.conf`

![](img-linux/001.png)

### **2. Instalamos y configuraremos bind9**

![](img-linux/004.png)

- Una vez que hayamos instalado todos los paquetes anteriores, nos movemos al directorio del programa `/etc/bind`, que es donde empezaremos a configurar los archivos necesarios.

![](img-linux/005.png)

### **2.1 Configuraremos los fowarders de bind usando servidores DNS públicos (servidor DNS caché)**

![](img-linux/006.png)

- Reinicamos el servicio.

![](img-linux/007.png)

- Ahora comprobaremos de que al ejecutar el comando ``nslookup``, veremos que nuestro servidor DNS ha resuelto un dominio correctamente.

- **Servidor**

![](img-linux/031.png)

- **Cliente**

![](img-linux/032.png)

### **3. Configuramos como DNS maestro instalando un dominio ficticio y añadiendo configuración para búsquedas ``(/etc/bind/named.conf.local)``**

![](img-linux/033.png)

### **4. Creamos y configuramos un archivo de ZBD y otro de ZBI**

- **Zona de búsqueda directa**

![](img-linux/034.png)

- Guardamos la configuración y comrpobamos que la sintaxis está correcta.

![](img-linux/015.png)

- **Zona de búsqueda inversa**

![](img-linux/025.png)

- Guardamos la configuración y comrpobamos que la sintaxis está correcta.

![](img-linux/022.png)

### **5. Comprobaremos de que se resuelven todos los nombres desde la consola del servidor**

- ZBD

![](img-linux/017.png)

![](img-linux/019.png)

- Algunos nombres no dan ping, ya que son ficticios.

- ZBI

![](img-linux/023.png)

### **6. Comprobamos desde el Cliente que se resuelven correctamente los nombres dados de alta en el servidor**

![](img-linux/030.png)
