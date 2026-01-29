## Environment Setup

Esta sección documenta la instalación y configuración inicial del entorno SIEM basado en Splunk.  
Incluye la verificación del servicio, la interfaz web, el estado del puerto de recepción (9997) y la conexión del Universal Forwarder.

---

## Splunk Web (Interfaz principal)

La interfaz web confirma que Splunk Enterprise está instalado correctamente y accesible desde el navegador.

![splunk-web-home](https://github.com/user-attachments/assets/d4758899-6d26-4baa-8286-04d4cbe99140)


---

## Puerto 9997 escuchando (Recepción de logs)

Splunk Enterprise debe escuchar en el puerto **9997** para recibir datos desde el Universal Forwarder.  
Esta captura demuestra que el servicio está activo y preparado para recibir eventos.

![splunk-port-9997-listening](https://github.com/user-attachments/assets/c5579f82-8ce5-44bc-84eb-5cf992717588)


---

## Listmonitor (Monitoreo de inputs)

El comando list monitor permite verificar qué archivos está monitorizando Splunk.  
Aquí se confirma que el sistema está preparado para recibir y procesar logs del host Ubuntu.

![splunk-listmonitor](https://github.com/user-attachments/assets/e944f1a0-31b4-4446-814b-6836737cf0fd)


---

## Conexión del Universal Forwarder

Universal Forwarder está correctamente configurado y enviando datos al Splunk Server.  
La captura muestra el estado de la conexión con el comando splunk list forward-server.

![splunk-forward-server-status png](https://github.com/user-attachments/assets/9cb855e4-27ad-4ff4-a97a-8889901b6c3d)


---

Estado del entorno

El entorno SIEM funciona y esta operativo.

