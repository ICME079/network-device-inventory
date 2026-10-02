# network-device-inventory
Script de descubrimiento de activos de red que automatiza el mapeo de subredes locales, la detección de hosts activos y la documentación técnica del entorno.

Este proyecto reúne utilidades de administración de red para resolver la falta de visibilidad en segmentos locales sin depender de software pesado de pago:

1. **Módulo de Descubrimiento de Capa 2 y 3 (`net_mapper.py`):**
   - Implementa solicitudes ICMP (Ping) y consultas ARP para censar equipos encendidos en el rango de red especificado.
2. **Identificador de Fabricante (OUI Lookup):**
   - Analiza los primeros 24 bits de las direcciones MAC recopiladas para identificar la empresa fabricante de la tarjeta de red (Cisco, Dell, HP, Apple, etc.), facilitando la clasificación del tipo de dispositivo.
3. **Resolución Inversa de Nombres:**
   - Realiza peticiones DNS PTR para asociar cada IP descubierta con su nombre de host corporativo o de dominio local.
4. **Módulo de Salida:**
   - Diseñado para volcar los resultados en archivos CSV delimitados, permitiendo exportar directamente el inventario a hojas de cálculo para control administrativo y auditorías de inventario de TI.
