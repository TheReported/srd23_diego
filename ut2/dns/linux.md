# **Práctica Servidor DNS Linux bind9**

|  MV    | Equipo     | IP|
| :------------- | :------------- | :------------- |
| Servidor DNS Master      | peraza23u2       | 172.19.23.31|
| Servidor DNS Slave      | peraza23u3       | 172.19.23.32|
|Cliente      | peraza23u1       | 172.19.23.50|

### **0. Configuración de red de la MV Servidor DNS**

- Editaremos el siguiente fichero para que nuestro Servidor DNS, este configurado con IP estática, además añadiremos que él es el propio DNS.

![](img-linux/029.png)

- Reiniciamos la MV y comrpobamos que se han guardado los cambios.

![](img-linux/003.png)

- Ahora en la MV Cliente, pondremos como servidor DNS a nuestro servidor para que haya comunicación entre ellos.

![](img-linux/027.png)

![](img-linux/028.png)

### **1. Indicaremos a Linux que el servidor DNS es él mismo ``(/etc/resolv.conf)``**

- `sudo nano /etc/resolv.conf`

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

- Guardamos la configuración y comprobamos que la sintaxis está correcta.

![](img-linux/015.png)

- **Zona de búsqueda inversa**

![](img-linux/025.png)

- Guardamos la configuración y comprobamos que la sintaxis está correcta.

![](img-linux/022.png)

### **5. Comprobaremos de que se resuelven todos los nombres desde la consola del servidor**

- **ZBD**

![](img-linux/017.png)

![](img-linux/019.png)

- Algunos nombres no dan ping, ya que son ficticios.

- **ZBI**

![](img-linux/023.png)

### **6. Comprobamos desde el Cliente que se resuelven correctamente los nombres dados de alta en el servidor**

![](img-linux/030.png)

### **7. Investigación: Cloanremos la MV del servidor bind9 y configura el nuevo linux para que bind9 se comporte como un servidor esclavo (slave) del principal (master).Comprueba el funcionamiento entre maestro, esclavo y cliente.**

- **Slave**

![](img-linux/052.png)

![](img-linux/053.png)

![](img-linux/035.png)

- **Master**

![](img-linux/054.png)

![](img-linux/038.png)

![](img-linux/046.png)

- **Cliente**

![](img-linux/051.png)

- **Comprobaciones:**

- Para hacer la comprobación desactivaremos el servicio bind9 en el servidor Master, para que el servidor Slave nos haga de soporte.

- Después vamos al cliente y comprobamos los nombres y también pondremos nslookup para comprobar de que el servidor DNS Slave está actuando.

![](img-linux/048.png)

![](img-linux/055.png)


***Hasta aquí queda por finalizada la actividad.***
