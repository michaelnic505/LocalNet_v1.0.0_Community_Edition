
🚀 LocalNet v1.0.0 - Community Edition
Lanzamiento oficial: 19/01/2026

LocalNet es una suite de infraestructura de red desarrollada en Java, diseñada para transformar una computadora convencional en el nodo central de una Intranet Soberana. Es la herramienta ideal para centros educativos (escuelas, institutos, universidades) y servicios internos que buscan autonomía digital y control total sobre su tráfico local.

✨ Características Principales
🌐 Web Server (Puerto 80)
Permite hostear aplicaciones y páginas web para servicios internos, como sistemas de registro de estudiantes, control de asistencia o plataformas de consulta de notas. Facilita la implementación de herramientas institucionales accesibles exclusivamente desde la red local, reduciendo la carga administrativa.

🔍 DNS Server (Puerto 53)
Resuelve dominios personalizados de forma local. Olvida las direcciones IP difíciles de recordar; con este módulo, los usuarios pueden acceder a los servicios internos escribiendo nombres de dominio amigables directamente en el navegador. Además, funciona como puente para el tráfico de red de los dispositivos vinculados.

📡 DHCP Server (Puertos 67 y 68)
Es el núcleo de control de LocalNet. Intercepta las peticiones UDP de broadcast de los dispositivos que buscan conexión. El servidor procesa estas solicitudes y responde con un paquete de configuración que incluye:

Asignación de IP dinámica.

Identificación del Servidor DHCP y DNS.

Máscara de subred y Puerta de enlace.

🚫 Blacklist & Filtrado
Control exhaustivo sobre el acceso a contenidos. Permite crear listas de dominios restringidos para evitar el mal uso de los recursos de la red. Incluye una consola de monitoreo en tiempo real para visualizar intentos de acceso bloqueados e identificar las IPs de origen.

🛠️ Instrucciones de Configuración
1. Módulo DHCP (Prioridad Alta)
Es fundamental para el control total de la red. Requiere el ingreso de los Datos Maestros de tu infraestructura:

Define el segmento de red de tu router (Ej: 192.168.100.0).

Configura la IP de la PC Reina como el servidor DNS para que el sistema pueda interceptar y resolver peticiones.

Es obligatorio que el Módulo DNS esté activo para que el tráfico fluya correctamente.

2. Módulo DNS e Intranet
Ideal para entornos educativos. Permite simular el funcionamiento global del internet dentro de una red privada. La consola integrada te permitirá visualizar el flujo de datos de todos los equipos, convirtiendo tu computadora en el filtro principal de la red.

3. Publicación Web
Para publicar tus sitios, asegúrate de que el puerto 80 esté disponible. Esto permitirá que cualquier dispositivo en la red acceda a tus herramientas locales simplemente conectándose al WiFi o LAN gestionada por LocalNet.

4. Gestión de Seguridad (Blacklist)
Utiliza la consola de seguridad para supervisar el comportamiento de los usuarios. Si detectas un uso indebido, añade el dominio a la lista negra y el servidor DNS de LocalNet se encargará de denegar el acceso instantáneamente.

⚠️ Requisitos Críticos de Ejecución
[!IMPORTANT] Privilegios de Sistema: LocalNet requiere ejecutarse con permisos de Administrador para poder realizar el binding de los puertos privilegiados (80, 53, 67, 68).

Firewall: Es estrictamente necesario revisar y ajustar las Reglas de Entrada y Salida del Firewall de Windows para permitir el tráfico UDP y TCP de estos servicios.
