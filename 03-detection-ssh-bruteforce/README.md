# 03 – Detection: SSH Brute Force

Esta sección documenta la detección de un ataque de fuerza bruta SSH mediante búsquedas SPL en Splunk.  
Se analiza el volumen de intentos fallidos por IP y por usuario, identificando patrones típicos de ataque automatizado.

---

## Intentos fallidos por IP

Esta búsqueda permite identificar la IP origen responsable de los intentos fallidos de autenticación.
En este caso, se observa que una única IP genera un volumen elevado de intentos fallidos, lo que es un claro indicador de actividad de fuerza bruta.



![intentos por ip](https://github.com/user-attachments/assets/69e1bcc3-fd22-4d80-aed4-995d4faa7d6a)



## Intentos fallidos por Usuario 

Esta búsqueda identifica qué cuentas del sistema fueron objetivo del ataque.  
En este caso, el usuario `testubuntu` recibió **70 intentos fallidos**, lo que indica un ataque dirigido y persistente contra una única cuenta.



![intentos por usuario](https://github.com/user-attachments/assets/515510ca-6162-4056-8819-91972efdfd30)
