# 02 – Data Ingestion

Esta sección documenta la ingesta de logs desde el host Ubuntu hacia Splunk Enterprise.  
Se verifica que los eventos de autenticación (auth.log) están llegando correctamente, incluyendo intentos fallidos de acceso, cierres de conexión y eventos PAM.

---

## Eventos de autenticación: "Failed password"

La búsqueda `index=* sourcetype=auth "Failed password"` muestra múltiples intentos fallidos de autenticación SSH.  
Estos eventos son clave para detectar ataques de fuerza bruta.

![failed password](https://github.com/user-attachments/assets/45d5e78b-ab0b-419b-bb79-9de959984df2)


---

## Eventos de cierre de conexión: "Connection closed"

La búsqueda `index=* sourcetype=auth "Connection closed"` revela múltiples cierres de sesión por usuarios inválidos.  
Estos eventos complementan la detección de accesos no autorizados.

![connection closer](https://github.com/user-attachments/assets/526f05fc-b264-47e2-afaa-49183acab9c0)


---

## Eventos PAM

La búsqueda `index=* sourcetype=auth "PAM"` muestra actividad del módulo PAM, incluyendo fallos de autenticación y sesiones abiertas/cerradas.  
Estos eventos aportan contexto adicional sobre el comportamiento del sistema.


![pam](https://github.com/user-attachments/assets/9969d518-f664-42c5-8c36-31ce119d477d)

---

## Vista cronológica de intentos fallidos

La búsqueda con `timechart` permite visualizar la frecuencia de intentos fallidos por segundo.  
Esto ayuda a identificar patrones de ataque en el tiempo.

![splunk-time-chart](https://github.com/user-attachments/assets/e0227d7e-4a93-4e8d-96ae-9d933ecf06d8)



