# Configuración de Router Core (R1) y Enrutamiento Inter-VLAN

* **Responsable:** Nashley Arias / Equipo Inter-VLAN Routing
* **Dispositivo:** `R1` (Cisco IOS)

## Descripción de la Implementación
El router `R1` funciona como puerta de enlace principal para las redes de usuarios del bloque derecho de la topología y establece la interconexión de capa 3 con el switch multicapa `SWM1`:

1. **Router-on-a-Stick (`Ethernet0/1` hacia `SW4`):** Se dividió la interfaz física en subinterfaces virtuales etiquetadas con **IEEE 802.1Q (`dot1Q`)** para gestionar el tráfico entre las VLANs:
   * **VLAN 10 (Estudiantes):** `172.16.0.1/21` | `2001:25:16:1::1/64`
   * **VLAN 20 (Docentes):** `172.16.8.1/24` | `2001:25:16:2::1/64`
   * **VLAN 60 (Gestión):** `172.16.10.65/27` | `2001:25:16:6::1/64`
   * **VLAN 70 (Voz):** `172.16.10.97/27` | `2001:25:16:7::1/64`
   * **VLAN 80 (Blackhole):** `172.16.10.129/28` | `2001:25:16:8::1/64`
     
2. **Enlace Punto a Punto (`Ethernet0/0` hacia `SWM1`):** Configurado en doble pila con `172.16.10.146/30` (IPv4), `2001:25:16:9::1/127` (IPv6) y dirección link-local `FE80::1`.
3. **Enrutamiento Estático:** Rutas IPv4 e IPv6 apuntando hacia `SWM1` (`172.16.10.145` y `2001:25:16:9::`) para alcanzar las redes de Académicos, Finanzas y Datacenter.
4. **Seguridad:** Acceso administrativo protegido mediante llaves RSA de 2048 bits y **SSHv2**.
