# **Instalación y Configuración DHCP Windows**

### **1. Instalación del servicio DHCP en Windows 2016 Server**

![](img/001.png)

![](img/002.png)

![](img/003.png)

![](img/004.png)

![](img/005.png)

### **2. Configuración del servicio DHCP**

![](img/006.png)

![](img/007.png)

![](img/008.png)

![](img/009.png)

##### **2.1 Creación de un ámbito nuevo asociado al dominio con el intervalo de direcciones IP que consideres conveniente.**

![](img/010.png)

![](img/011.png)

![](img/013.png)

![](img/014.png)

##### **2.2 Agregar exclusiones de direcciones.**

![](img/015.png)

![](img/016.png)

##### **2.3 Configurar puerta de enlace y servidores DNS a suministrar a los clientes.**

![](img/017.png)

![](img/018.png)

![](img/019.png)

##### **2.4 Configurar resto de opciones necesarias.**

![](img/020.png)

![](img/021.png)

##### **2.5 Establecer una reserva de dirección asociada a un equipo específico (MAC).**

![](img/027.png)

![](img/028.png)

##### **2.6 Configurar algunas opciones de ámbito además de las habituales.**

![](img/025.png)

**- Reiniciamos la MV para que se aplique la exclusión.**

![](img/026.png)


### **3. Comprobar funcionamiento DHCP configurando adecuadamente la máquina cliente y anotando parámetros recibidos.**

![](img/022.png)

### **4. Tener en cuenta que el servidor no debe estar abierto a la red (configurar adaptador en red interna) para no provocar conflictos de direcciones.**

![](img/029.png)

![](img/030.png)
