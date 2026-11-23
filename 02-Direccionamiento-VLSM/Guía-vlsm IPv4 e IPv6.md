# Plan de Direccionamiento IPv4 e IPv6 (VLSM)

* **Responsable:** Manuel Maria.
* **Bloque Base IPv4:** `172.16.0.0/15`
* **Bloque Base IPv6:** `2001:25:16::/48`

## Criterios de Diseño
* Se aplicó **VLSM** en IPv4 ordenando las subredes de mayor a menor cantidad de hosts (desde Estudiantes hasta el enlace punto a punto).
* En IPv6 se asignaron prefijos `/64` para cada LAN modificando el hexteto de subred en el mismo orden de tamaño que en IPv4, y prefijo `/127` para el enlace punto a punto.
