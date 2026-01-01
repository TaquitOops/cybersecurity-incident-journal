#  Diario del Gestor de Incidentes: Portafolio Final

Este documento recopila las actividades, investigaciones y herramientas utilizadas durante mi formación en gestión de incidentes, alineado con los marcos de trabajo de **NIST**.

---

## Entradas del Diario

### Entrada #1
* **Fecha:** 2026-01-05
* **Descripción:** Análisis de tráfico sospechoso en un archivo PCAP para identificar una posible filtración de datos. Esta actividad pertenece a la fase de **Detección y análisis** del NIST, ya que buscamos confirmar una anomalía en la red.
* **Herramientas utilizadas:** **Wireshark**.

#### Las 5 W's del incidente:
* **¿Quién (Who)?:** Una dirección IP externa desconocida (203.0.113.5).
* **¿Qué (What)?:** Un volumen inusualmente alto de paquetes HTTP POST hacia un puerto no estándar.
* **¿Cuándo (When)?:** El incidente ocurrió el 15 de diciembre durante horas no laborales.
* **¿Dónde (Where)?:** El tráfico se originó en el servidor de finanzas de la empresa.
* **¿Por qué (Why)?:** Posible robo de credenciales que permitió el acceso no autorizado a datos sensibles.

---

### Entrada #2
* **Fecha:** 2026-01-10
* **Descripción:** Configuración y prueba de reglas de alerta en un IDS basado en firmas. Esta tarea corresponde a la fase de **Preparación** del NIST, asegurando que el entorno pueda detectar patrones maliciosos conocidos antes de un ataque real.
* **Herramientas utilizadas:** **Suricata**.
* **Notas adicionales:** Se validó que las reglas personalizadas para detectar túneles ICMP generaran las alertas correctas en el log.

---

### Entrada #3
* **Fecha:** 2026-01-15
* **Descripción:** Investigación de múltiples intentos fallidos de inicio de sesión seguidos de uno exitoso. Se sitúa en la fase de **Detección y análisis**, utilizando logs para evidenciar un ataque de fuerza bruta.
* **Herramientas utilizadas:** **Splunk**.

#### Las 5 W's del incidente:
* **¿Quién (Who)?:** Un script automatizado proveniente de una red botnet detectada.
* **¿Qué (What)?:** Ataque de fuerza bruta dirigido a la cuenta del administrador del sistema.
* **¿Cuándo (When)?:** Iniciado el 12 de enero a las 02:00 AM.
* **¿Dónde (Where)?:** Registros de autenticación del controlador de dominio principal.
* **¿Por qué (Why)?:** El atacante buscaba obtener privilegios elevados para realizar movimiento lateral en la red.

---

### Entrada #4
* **Fecha:** 2026-01-20
* **Descripción:** Búsqueda de telemetría histórica para localizar indicadores de compromiso (IoC) en grandes conjuntos de datos. Esta actividad es parte de la fase de **Contención, erradicación y recuperación**, asegurando que no queden restos de la amenaza.
* **Herramientas utilizadas:** **Chronicle**.
* **Notas adicionales:** La capacidad de correlacionar hashes de archivos con IPs permitió identificar rápidamente tres estaciones de trabajo infectadas.

---

## Reflexiones / Notas

### 1. ¿Hubo alguna actividad específica que supusiera un reto para ti?
Analizar paquetes en **Wireshark** fue el mayor reto debido al volumen de tráfico. Filtrar protocolos específicos requería precisión técnica para no perder detalles críticos. Sin embargo, entender la estructura de los paquetes a nivel granular mejoró significativamente mi capacidad de diagnóstico técnico en redes.

### 2. ¿Ha cambiado su comprensión de la detección y respuesta ante incidentes?
Mi comprensión ha pasado de ver la respuesta como algo lineal a entenderla como un proceso cíclico y estructurado. Gracias al marco del **NIST**, ahora valoro la importancia de la actividad posterior al incidente para fortalecer la postura de seguridad y prevenir futuros ataques repetitivos.

### 3. ¿Ha habido alguna herramienta o concepto específico que le haya gustado más?
Me gustó mucho utilizar **Splunk** por su potente capacidad de visualización de datos. Transformar miles de logs crudos en dashboards visuales facilita mucho la detección de patrones de ataque que serían imposibles de ver manualmente, optimizando el tiempo de respuesta del analista.
