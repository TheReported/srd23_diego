# **Práctica Servidor DNS Linux bind9**

### **0. Configuración de red de la MV Servidor DNS**

![](img-linux/029.png)

- Reiniciamos la MV y comrpobamos que se han guardado los cambios.

![](img-linux/003.png)

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

### **3. Configuramos como DNS maestro instalando un dominio ficticio y añadiendo configuración para búsquedas (/etc/bind/named.conf.local)**

- Zona directa
