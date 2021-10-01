# **Instalación y Configuración DHCP Linux**

### **1. Instalación del servicio DHCP en Ubuntu Linux**

![](img/103.png)

### **2. Configuración del servicio DHCP**

- Para modificar el fichero de configuración del servicio DHCP nos pondremos como superusuario e iremos a la siguiente ruta `/etc/dhcp/` y editaremos el siguiente archivo:

![](img/104.png)

### **3. Comprobar funcionamiento DHCP configurando adecuadamente la máquina cliente y anotando parámetros recibidos.**

![](img/105.png)

#### **3.1 Aplicar un rango de ip's a la red**

- Recordamos que el rango de ip's es ``172.19.23.50-172.19.23.70``

![](img/104.png)

- Comprobamos que se ha aplicado el rango:

![](img/106.png)

![](img/107.png)

#### **3.2 Hacer reserva para un host**

![](img/108.png)

- Comprobamos la Reserva

![](img/109.png)

#### **3.3 Exclusión**

![](img/111.png)

- Comprobamos la Exclusión

![](img/112.png)

### **4. Tener en cuenta que el servidor no debe estar abierto a la red (configurar adaptador en red interna) para no provocar conflictos de direcciones.**

![](img/101.png)

![](img/102.png)
