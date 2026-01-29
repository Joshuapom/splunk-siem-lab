## Splunk SIEM Lab – SSH Brute Force Detection & Alerting.

Este laboratorio reproduce un escenario de detección ante un ataque de fuerza bruta SSH utilizando Splunk Enterprise.
La idea es reproducir un flujo de trabajo típico de un analista SOC: preparar el entorno, ingerir datos, analizarlos, detectar actividad sospechosa y finalmente generar una alerta automática
El repositorio está dividido en varias carpetas, cada una con su propia documentación y capturas del proceso.

---

## Estructura del proyecto
01-environment-setup
Preparación del entorno Splunk y del sistema Linux que genera los logs.

02-data-ingestion
Ingestión del archivo auth.log en Splunk y validación de los datos.

03-detection-ssh-bruteforce
Búsquedas SPL para identificar actividad de fuerza bruta SSH por IP y por usuario.

04-alerting
Creación de una alerta programada en Splunk para detectar automáticamente el ataque.

---

## Objetivo del laboratorio
Simular un ataque de fuerza bruta SSH y demostrar cómo un analista SOC:
- Ingiere y valida datos en Splunk
- Analiza logs de autenticación
- Identifica patrones de ataque
- Construye detecciones con SPL
- Configura alertas automáticas
- Documenta el proceso de forma profesional

---

## Resumen de cada fase
1. Environment Setup
- Instalación y configuración inicial de Splunk Enterprise
- Preparación del entorno Linux
- Ajustes necesarios para recibir logs de autenticación
2. Data Ingestion
- Ingestión del archivo auth.log
- Verificación del sourcetype auth
- Confirmación de que los eventos contienen los campos necesarios
3. Detection – SSH Brute Force
- Extracción de IP origen mediante expresiones regulares
- Conteo de intentos fallidos por IP
- Conteo de intentos fallidos por usuario
- Identificación de un patrón claro de fuerza bruta vertical
4. Alerting
- Creación de una alerta programada cada minuto
- Umbral: más de 10 intentos fallidos en 60 segundos
- Acción: añadir a Triggered Alerts
- Validación de que la alerta se ejecuta correctamente

---

## Objetivo del proyecto
El propósito es mostrar un flujo completo de trabajo SOC, desde la llegada del dato hasta la alerta final, todo documentado paso a paso.

