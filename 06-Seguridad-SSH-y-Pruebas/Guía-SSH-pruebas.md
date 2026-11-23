# Seguridad SSH y Validación de Conectividad

* **Responsable:** Alizon Nova

## Descripción de la Implementación y Pruebas
* **Acceso Seguro:** Configuración de nombre de dominio, llaves criptográficas **RSA (2048 bits)**, autenticación local y transporte exclusivo por **SSHv2** en las líneas VTY de todos los equipos.
  
* **Pruebas de Conectividad:** Verificación de comunicación extremo a extremo (`ping`) entre todas las VLANs en **IPv4 e IPv6**.
* **Auditoría de Red:** Comprobación de tablas de enrutamiento, estado de troncales y sincronización VTP.
