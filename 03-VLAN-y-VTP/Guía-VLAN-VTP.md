# Segmentación Lógica: VLANs y Dominios VTP

* Responsable: Saymon.
* Dispositivos: Switches de capa 2 (`SW`, `SW3`, `SW4`, `SW5`).

## Descripción de la Implementación
* Creación y propagación de VLANs mediante **VTP (VLAN Trunking Protocol)** para separar el tráfico por departamentos.
* Configuración de enlaces troncales **802.1Q** entre switches y puertos de acceso hacia los equipos finales (`FIN1`, `ACA1`, `DOC1`, `EST1`, `GES1`).
* Asignación de puertos sin utilizar a la **VLAN Blackhull** por seguridad.
