# Configuración de Switch Multicapa (SWM1)

* **Responsable:** Riquelme Ortiz / Equipo de Inter-VLAN Routing
* **Dispositivo:** `SWM1` (Switch L3)

## Descripción de la Implementación
El switch multicapa `SWM1` realiza el enrutamiento interno del bloque izquierdo de la topología mediante interfaces virtuales conmutadas (**SVI**).

1. **Enrutamiento L3:** Habilitado globalmente mediante `ip routing` e `ipv6 unicast-routing`.
2. **Gateways (SVIs):**
   * **VLAN 30 (Académicos):** `172.16.9.1/25` | `2001:25:16:3::1/64`
   * **VLAN 40 (Finanzas):** `172.16.9.129/25` | `2001:25:16:4::1/64`
   * **VLAN 50 (Datacenter):** `172.16.10.1/26` | `2001:25:16:5::1/64`
   * **VLAN 80 (Blackhull):** `172.16.10.129/28` | `2001:25:16:8::1/64`
3. **Enlace Punto a Punto (`Ethernet0/1` hacia `R1`):** Puerto enrutado (`no switchport`) con `172.16.10.145/30` (IPv4), `2001:25:16:9::/127` (IPv6) y dirección link-local `FE80::2`.
4. **Enrutamiento Estático:** Rutas IPv4 e IPv6 apuntando hacia `R1` (`172.16.10.146` y `2001:25:16:9::1`) para alcanzar las redes de Estudiantes, Docentes, Gestión y Voz.
