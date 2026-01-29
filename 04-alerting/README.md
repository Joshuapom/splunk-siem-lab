## 04 – Alerting: SSH Brute Force
Esta sección documenta la creación de una alerta en Splunk para detectar ataques de fuerza bruta SSH en tiempo real.
La alerta se basa en la detección de múltiples intentos fallidos de autenticación desde una misma IP en un intervalo corto.
“Esta alerta utiliza la misma búsqueda documentada en la sección 03 – Detection, donde se identifican los intentos fallidos por IP."


---

## Configuración de la alerta
La alerta se configuró como programada cada minuto, con un rango de tiempo de los últimos 60 segundos y un umbral de más de 10 resultados.
La acción seleccionada fue añadir el evento a “Triggered Alerts”, con severidad Media.
La alerta quedó activada y lista para ejecutarse automáticamente.

![creando la alerta](https://github.com/user-attachments/assets/da03ede6-3926-4486-811f-7c33bb0ab627)

---


## Ejecución y resultados
La alerta se ejecutó correctamente y generó resultados en múltiples ocasiones.
Cada ejecución devolvió eventos, lo que confirma la condición de fuerza bruta.

![alerta saltando](https://github.com/user-attachments/assets/8b0c4b22-d91e-43c6-a510-166b54b273a1)

---

## Estado de la alerta
En esta vista se puede comprobar que la alerta está habilitada, configurada correctamente y lista para ejecutarse según el cron establecido.

![alerta creada](https://github.com/user-attachments/assets/5c508159-ceb8-4f93-8be1-9c05eec6dbf4)

---

## Registro de alertas
La alerta aparece registrada en el panel de búsquedas guardadas, con estado Enabled y próxima ejecución programada.
Desde esta vista es posible editarla, ejecutarla manualmente o revisar sus ejecuciones recientes.

![alerta en funcionamiento](https://github.com/user-attachments/assets/60b5b2c1-e5ad-4b4b-a9f0-5eabb0a28d19)

---


