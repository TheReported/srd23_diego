# **Instalación y Configuración DNS Windows Server.**

## **1. Realizamos la configuración de un servidor DNS.**

![](img/001.png)

#### **1.1 Crearemos una zona de búsqueda directa nueva para otro dominio.**

![](img/002.png)

![](img/003.png)

![](img/004.png)

![](img/005.png)

![](img/006.png)

![](img/007.png)

![](img/008.png)

#### **1.2 Crearemos una zona de búsqueda inversa nueva para el nuevo dominio.**

![](img/011-5.png)

![](img/012-5.png)

![](img/013.png)

![](img/014.png)

![](img/015.png)

![](img/016.png)

![](img/017.png)

## **2. Configuraremos el servidor para ser servidor DNS Caché.**

- **Configuración de red**:

- **Servidor**:

![](img/037.png)

- **Cliente**:

![](img/038.png)

- Comprobaremos el funcionamiento como caché DNS de ambas máquinas al acceder a sitios de Internet.

- **Servidor**:

![](img/041.png)

- **Cliente**:

![](img/042.png)

#### **2.1 Configurar reenviadores de DNS con puerta de enlace actual y DNS público.**

![](img/022.png)

#### **3. Configuraremos el servidor como DNS Maestro, además de Caché.**
#### **3.1 Añadiremos los siguientes registros en la zona de búsqueda directa.**

- Un alias para tu servidor denominado server.
- Una impresora con IP fija denominada printer.
- Un servidor de correo (ficticio) denominado correo, asociado a una dirección en tu servidor.

![](img/026.png)

- Crear una subzona denominada servicios (dominio nuevo) y agregar a ésta un servidor ftp (asociado a la misma IP del servidor), una impresora nueva (con una IP fija) y el equipo del administrador del sistema (también con IP fija).

![](img/027.png)

## **4. Comprobamos que se resuelven los nombres desde la consola del servidor.**

- **ZBD**

![](img/040.png)

- **Servicios**

![](img/032.png)

- **ZBI**

![](img/033.png)



## **5. Validamos un cliente al dominio y comprobamos que el nombre de su equipo aparece en la zona de búsqueda del servidor como un nuevo registro A.**

![](img/039.png)

![](img/012.png)

![](img/011.png)

## **6. Comprobamos desde la consola cliente que se resuelven correctamente los nombres dados de alta en el servidor.**

- **ZBD**

![](img/034.png)

- **Servicios**

![](img/035.png)

- **ZBI**

![](img/036.png)

## **7. Realizamos desde el cliente  algunas operaciones con nslookup tanto dentro como fuera de nuestra intranet**

![](img/029.png)
