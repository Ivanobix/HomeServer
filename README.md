# **☢️ HOME SERVER ☢️**

![HomeServerWallpaper](https://github.com/Ivanobix/HomeServer/assets/56084434/85198abb-8ce6-4c72-aa98-6571ab62a77d)

Este documento ofrece un análisis detallado sobre la estructura y operatividad de un servidor basado en el sistema NAS QNAP TS-464. Este servidor, diseñado para brindar un rendimiento sólido y fiable, está equipado con componentes de hardware de nivel empresarial, lo cual supone un elevado coste inicial, pero que será completamente rentable a medio y largo plazo.

Para garantizar transferencias de datos veloces y eficaces, el servidor incorpora un router de alto rendimiento y ha sido configurado con diversas estrategias y tecnologías destinadas a optimizar tanto su rendimiento como su seguridad.

El mantenimiento regular y la seguridad son aspectos críticos en la configuración del servidor. Para asegurar un funcionamiento óptimo, se han establecido una serie de rutinas de mantenimiento programado. Paralelamente, se han instaurado diversas soluciones de software para salvaguardar el sistema frente a una extensa gama de amenazas potenciales.

Este servidor también implementa una estrategia de respaldo de datos multinivel para garantizar su protección integral, y se vale de una diversidad de software y servicios de terceros para potenciar su funcionalidad, rendimiento y seguridad. 

En resumen, este servidor ha sido meticulosamente diseñado y configurado para proporcionar un rendimiento óptimo y confiable, y para garantizar la seguridad e integridad de los datos almacenados en su interior.

## **⚙️ Configuración del Hardware**

### **🖥️ NAS QNAP TS-464**

El sistema NAS QNAP TS-464 es un dispositivo de almacenamiento robusto y confiable, diseñado para ofrecer rendimiento y flexibilidad. La especificación de hardware de este sistema incluye:

- **Procesador** - Intel Celeron N5105. Este procesador de cuatro núcleos, con cuatro hilos, ofrece una frecuencia base de 2GHz que puede subir hasta 2.9GHz cuando se necesita más rendimiento.

- **Memoria** - 16GB (2x8GB) DDR4 3200MHz CL22 por Crucial. Este módulo de memoria de alto rendimiento garantiza que el sistema pueda manejar múltiples tareas de manera eficiente.

- **Almacenamiento** - El sistema cuenta con dos unidades de estado sólido Crucial P5 Plus CT1000P5PSSD8 de 1TB y cuatro unidades de disco duro Seagate Exos 7E8 de 8TB.

- **Conexión** - El sistema dispone de dos conexiones Ethernet de 2.5 Gbit, proporcionando un enlace de red de alta velocidad para transferencias de datos rápidas y eficientes.

### **📡 Router TP-Link Archer AX73**

El TP-Link Archer AX73, seleccionado por su alto rendimiento y confiabilidad, es fundamental para el correcto funcionamiento de nuestro servidor. Con un potente procesador de cuatro núcleos a 1.5GHz, garantiza transferencias de datos rápidas y eficientes a través de sus puertos Ethernet Gigabit.

Además, el Archer AX73 ofrece una Calidad de Servicio (QoS) avanzada para optimizar el tráfico de red y cuenta con características de seguridad integradas, como firewalls, antivirus y la capacidad de configurar VPNs.

Su interfaz de usuario intuitiva facilita la gestión del router, lo que ayuda a minimizar los costos de administración y mantenimiento. 

## **💽 Configuración del Almacenamiento**

El sistema de almacenamiento está diseñado para proporcionar una mezcla de rendimiento y capacidad. Se han implementado varias tecnologías y estrategias para cumplir con estos requisitos.

### **Unidades de Estado Sólido (SSD)**
Las dos unidades de estado sólido Crucial P5 Plus CT1000P5PSSD8 de 1TB están configuradas en RAID 1. Esto significa que los datos se duplican en ambas unidades, lo que proporciona una protección completa contra la pérdida de datos en caso de un fallo de una unidad. Este arreglo está destinado a albergar el sistema operativo, los contenedores Docker/LXD, las máquinas virtuales y las configuraciones del sistema.

### **Unidades de Disco Duro (HDD)**
Las cuatro unidades de disco duro Seagate Exos 7E8 de 8TB están configuradas en RAID 5. Esto proporciona un equilibrio entre el rendimiento, la capacidad de almacenamiento y la protección de datos. En caso de fallo de un disco, los datos se pueden reconstruir a partir de los datos existentes en los otros discos. Este arreglo está destinado al almacenamiento de datos en general y al almacenamiento de contenido multimedia.

### **Almacenamiento en Medios Offline**
Para la redundancia adicional y la protección contra desastres, se dispone de dos unidades de disco duro WD My Book de 8TB. Estas unidades no están en RAID y se utilizan para respaldos manuales.

## **🛠️ Programaciones de Mantenimiento**

El mantenimiento regular es esencial para garantizar el rendimiento óptimo y la longevidad de las unidades de almacenamiento en nuestro sistema. Hemos programado una serie de tareas de mantenimiento para asegurar que nuestro sistema esté siempre en las mejores condiciones de funcionamiento.

- **Optimización de SSD** - Esta tarea se ejecuta semanalmente. Durante este proceso, se realizan operaciones de mantenimiento en nuestras unidades de estado sólido (SSD), como el recorte (trimming). Esta optimización regular ayuda a prolongar la vida útil de las SSD y a mantener su rendimiento a largo plazo.

- **Análisis S.M.A.R.T** - Esta tarea se ejecuta a semanalmente. Durante esta tarea, el sistema monitorea la salud de las unidades de disco utilizando la tecnología SMART (Self-Monitoring, Analysis, and Reporting Technology). Esta verificación regular nos permite detectar y abordar cualquier problema potencial con las unidades de disco antes de que se conviertan en problemas graves.

- **Limpieza RAID** - Esta tarea se ejecuta mensualmente. Durante este proceso, se realizan operaciones de mantenimiento en nuestros discos en RAID, como el chequeo de paridad y la reconstrucción del RAID si es necesario. Esta limpieza regular ayuda a mantener el rendimiento de nuestros discos en y a garantizar la integridad de los datos almacenados en ellos.

## **🔄 Programaciones de Actualizaciones**

Mantener el sistema actualizado es fundamental para garantizar su seguridad y rendimiento óptimo. Hemos programado una serie de actualizaciones regulares para asegurar que el sistema esté siempre al día con las últimas versiones de software y protecciones de seguridad. 

- **Antivirus** - El software antivirus está configurado para actualizar diariamente. Estas actualizaciones regulares garantizan que el sistema esté siempre protegido contra las últimas amenazas conocidas.

- **Malware Remover** - El Malware Remover está programado para actualizarse diariamente. Esta programación garantiza que el sistema esté constantemente monitoreado y protegido contra malware y otras amenazas de seguridad.

- **Firmware** - Las actualizaciones del firmware están programadas para ejecutarse diariamente. Estas actualizaciones regulares aseguran que el sistema esté protegido contra las últimas vulnerabilidades conocidas y que esté funcionando con la versión más reciente y segura del firmware.

- **Watchtower** - Watchtower está configurado para ejecutarse diariamente, monitoreando la disponibilidad de nuevas imágenes y actualizando los contenedores según sea necesario. Esto asegura que siempre estemos utilizando las versiones más recientes y seguras de nuestras aplicaciones Docker.

## **🔒 Configuraciones y Soluciones de Seguridad**

La seguridad es una prioridad en nuestro sistema y hemos implementado una serie de estrategias, programas y soluciones de software para garantizarla. Estos incluyen:

- **Malware Remover**: Semanalmente se realiza un escaneo completo de seguridad, el cual se vuelve a realizar de forma inmediata en caso de que las definiciones de virus se actualicen.

- **Antivirus (ClamAV)**: Semanalmente se realiza un escaneo rápido que proporciona una protección rápida y eficiente, y mensualmente se realiza un análisis más profundo y exhaustivo para garantizar que no se pase por alto ninguna amenaza.

- **Security Counselor**: Semanalmente se realiza un análisis exhaustivo del sistema y proporciona recomendaciones personalizadas para mejorar la seguridad. Esta herramienta es esencial para mantener un entorno seguro y protegido, ya que permite identificar y abordar cualquier vulnerabilidad potencial de manera proactiva.

- **QuFirewall**: QuFirewall es una solución de seguridad de red avanzada que protege el sistema NAS contra ataques cibernéticos. Al monitorear y controlar el tráfico de red, QuFirewall puede detectar y bloquear cualquier actividad sospechosa, asegurando la integridad de los datos almacenados en el sistema.
- **Wireguard:** Wireguard se trata de una solución VPN de alto rendimiento fácil de configurar que proporciona una forma segura de acceder a la red desde cualquier lugar mediante un túnel cifrado.

- **Cloudflare Access:** Esta solución de seguridad protege las aplicaciones y servicios internos sin necesidad de exponerlos directamente a Internet. Cloudflare Access establece un túnel seguro entre tu red y la red de Cloudflare, evitando la necesidad de abrir puertos innecesarios. Cuando un usuario intenta acceder a un servicio o aplicación, la solicitud se redirige a través de la red de Cloudflare y se transmite de manera segura a tu red. De esta manera, se obtiene una capa adicional de protección, manteniendo nuestras aplicaciones y servicios seguros y accesibles solo a través de conexiones autorizadas.
- **Traefik:** Actuando como un balanceador de carga y proxy inverso de avanzada y código libre, Traefik facilita la administración de enrutamientos y certificados SSL y proporciona una interfaz web para el usuario. En un esfuerzo adicional para fortalecer la seguridad, se ha integrado un plugin de bloqueo GeoIP, el cual concede la capacidad de limitar el acceso a servicios web basándose en la geolocalización del usuario. Este recurso se vuelve esencial para mantener la integridad de los datos y bloquear tráfico indeseado, especialmente para aquellos servicios que no se encuentran protegidos por Cloudflare y necesitan ser accesibles públicamente sin la utilización de una VPN.

## **💾 Copias de Seguridad y Respaldo**

La estrategia de respaldo y la protección de datos son componentes esenciales de la seguridad y la integridad de los datos en nuestro sistema. Hemos implementado una estrategia de respaldo en capas para garantizar la protección completa de los datos en diversas situaciones.

- **Instantáneas**: La creación de instantáneas se realiza diariamente. Estas instantáneas actúan como puntos de restauración, permitiendo la recuperación rápida y eficiente de los datos en caso de un fallo del sistema o la pérdida de datos debido a un borrado accidental. Al mantener una serie de instantáneas, podemos garantizar que siempre haya una versión reciente de los datos disponibles para la restauración.
- **Backup Cloud (HBS 3 Hybrid Backup Sync)**: El respaldo en la nube se ejecuta diariamente. Este respaldo, realizado con la herramienta HBS 3 Hybrid Backup Sync, proporciona una capa adicional de protección contra desastres, utilizando OneDrive (1 TB) para almacenar una copia de los datos en un servidor externo. Antes de la subida, los datos se encriptan para garantizar su seguridad durante la transferencia y el almacenamiento.

- **Backup Manual**: Este respaldo se realiza mensualmente o antes de realizar operaciones que puedan poner en riesgo los datos. Estos respaldos offline protegen los datos en caso de un fallo del sistema completo, proporcionando una capa adicional de seguridad y redundancia.

## **🎛️ Software Implementado**

Actualmente el servidor cuenta con una gran variedad de herramientas y servicios desplegados mediante diferentes enfoques y tecnologías, entre los que destacan:

### **Docker (Container Station)**

- **Portainer:** Esta herramienta proporciona una interfaz de usuario intuitiva para administrar todos tus contenedores. Permite un control total sobre tus entornos, facilitando la implementación, la actualización y el mantenimiento de las aplicaciones.

- **Nextcloud:** Es una solución de auto alojamiento que te permite mantener el control total sobre tus datos. Proporciona funcionalidades de almacenamiento en la nube, sincronización de archivos, compartición de archivos y mucho más, todo bajo tu control.

- **Jellyfin y Plex:** Estos servidores de medios permiten organizar, administrar y transmitir tu contenido multimedia. Jellyfin se utiliza para el acceso remoto, mientras que Plex se utiliza para el acceso local. 

- **Vaultwarden:** Es una implementación alternativa de Bitwarden, un gestor de contraseñas de código abierto. Te permite almacenar y administrar tus contraseñas de manera segura sin consumir una gran cantidad de recursos.

- **Homarr:** Esta herramienta proporciona una forma rápida y sencilla de acceder a todos tus servicios mediante la creación de un panel de control personalizable con widgets y marcadores.

- **NordVPN y qBittorrent:** NordVPN es un servicio de Red Privada Virtual (VPN) que te permite navegar por internet de manera segura y anónima. Por otro lado, qBittorrent es un cliente de descarga de archivos torrent de código abierto y multiplataforma. Al combinarse, estos dos servicios te permiten descargar y compartir archivos de manera segura y privada, protegiendo tu identidad y tus datos en línea. NordVPN te ayuda a enmascarar tu dirección IP, mientras que qBittorrent te proporciona una plataforma eficiente para descargar archivos torrent.

- **Resilio Sync:** Es una herramienta de sincronización de archivos peer-to-peer (P2P) que permite sincronizar datos entre múltiples dispositivos de forma rápida y segura. Utiliza la tecnología BitTorrent para transferir archivos, lo que asegura una sincronización eficiente incluso cuando se manejan grandes cantidades de datos. A diferencia de las soluciones tradicionales de almacenamiento en la nube, Resilio Sync no depende de un servidor centralizado, por lo que tus datos se transfieren directamente entre tus dispositivos sin pasar por un tercer intermediario. Esto no solo acelera el proceso, sino que también aumenta la privacidad y seguridad de tus datos. Ideal para realizar copias de seguridad, compartir archivos grandes o mantener a todo un equipo sincronizado.

### **Máquinas Virtuales (Virtualization Station)**

Las máquinas virtuales facilitan la ejecución de aplicaciones y programas que no son nativamente compatibles con el sistema operativo del NAS. 
- **Windows 10:** Para maximizar la versatilidad y la funcionalidad de nuestro sistema, utilizamos una máquina virtual que opera con Windows 10. Esta configuración nos permite ejecutar aplicaciones específicas que requieren este sistema operativo, proporcionando así una solución flexible que puede adaptarse a una amplia variedad de necesidades y requisitos.

## **🌐 Servicios de Terceros**

Para mejorar la funcionalidad, el rendimiento y la seguridad del sistema, se han integrado varios servicios de terceros. Estos servicios, seleccionados por su confiabilidad y eficacia, juegan un papel crucial en la optimización del sistema.

### **Cloudflare** 
Cloudflare es un proveedor líder de servicios de red que ofrece una variedad de soluciones para mejorar la seguridad y el rendimiento de la red. En nuestro sistema, utilizamos Cloudflare para una serie de funciones esenciales, incluyendo CDNA (DNS + Caché + Proxy), Access (Zero Trust Tunnel), WAF y protección contra DDoS. Estos servicios ayudan a proteger el sistema contra ataques potenciales, mejoran la velocidad y la eficiencia de la red y proporcionan una capa adicional de seguridad para garantizar la integridad de los datos.

### **Brevo (Sendinblue)** 
Brevo, anteriormente conocido como Sendinblue, se utiliza para el envío de correos automáticos. Este servicio es esencial para mantener una comunicación efectiva y oportuna, permitiendo el envío eficiente de notificaciones y alertas. Brevo ofrece una plataforma confiable y fácil de usar que garantiza que las comunicaciones importantes se entreguen de manera rápida y segura.

### **Next DNS**
Next DNS es un servicio que proporciona un DNS privado, lo que mejora significativamente la privacidad y la seguridad del sistema. Al utilizar Next DNS, podemos controlar y proteger el tráfico de red, bloquear el acceso a sitios web y servicios potencialmente dañinos y proteger los datos sensibles de las amenazas en línea.
