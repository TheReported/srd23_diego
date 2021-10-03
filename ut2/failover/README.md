# **DHCP Failover en Windows 2016 Server**

### **0. Preparativos**
- Recordad de tener la MV en **Red interna**

| MV     | IP     |
| :------------- | :------------- |
| Windows Server - peraza23ws | 172.19.23.11 |
| Windows Server - peraza23ws2 | 172.19.23.34 |
| Windows Cliente| DHCP   |

### **1. Configurar conmutación por error**

- Iremos al primer servidor de DHCP para configurar el Failover, para ello iremos a ``Herramientas > DHCP > IPv4`` y le damos click derecho en el mismo.

![](img/010.png)

- Seleccionaremos todo y siguiente.

![](img/011.png)

- Ahora pondremos la ip del otro servidor DHCP, en servidor asociado y le daremos a siguiente.

![](img/015.png)

- Pondremos una contraseña y le daremos a siguiente:

![](img/016.png)

- Y por último le daremos a finalizar.

![](img/017.png)

### **1.1 Comprobaciones**

- Comprobamos que en el otro servidor se ha duplicado el mismo contenido.

![](img/018.png)

- Ahora en la máquina cliente veremos que se ha conectado al primer servidor DHCP.

![](img/026.png)

- Modificaremos el plazo de cliente máximo y el intervalo de cambio de estado a 1 min.

![](img/025.png)

### **2. Comprobar que funciona el Failover**

- En este punto apagaremos el servidor DHCP ``peraza23ws`` , lo cual el servidor DHCP ``peraza23ws2`` actuará de respaldo.

- Comprobaremos mediante comandos en el cliente que se ha cambiado la ip.

- Primero pondremos el comando `ipconfig /relase` para liberar la ip , lo segundo `ipconfig /renew` para renovar la ip, y por último pondremos `ipconfig /all` para ver que se ha conectado al otro servidor.

![](img/027.png)

![](img/028.png)
