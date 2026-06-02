# CyberLab

Laboratorio práctico de ciberseguridad enfocado en reconocimiento, enumeración, análisis de vulnerabilidades y explotación controlada sobre entornos vulnerables.

## Objetivos

* Practicar metodologías de pentesting en entornos controlados.
* Documentar hallazgos de seguridad de forma profesional.
* Validar vulnerabilidades conocidas.
* Construir un portafolio técnico orientado a ciberseguridad.

## Entorno del laboratorio

### Máquina atacante

* Kali Linux
* IP: 192.168.56.103

### Máquina objetivo

* Metasploitable 2
* IP: 192.168.56.101

## Metodología

1. Reconocimiento
2. Enumeración
3. Análisis de vulnerabilidades
4. Explotación controlada
5. Documentación de evidencias
6. Recomendaciones de mitigación

## Herramientas utilizadas

* Nmap
* Nikto
* Gobuster
* Metasploit Framework
* Git
* GitHub

## Documentación

### Reconocimiento y Enumeración

Archivo:

```text
docs/01-reconocimiento-y-enumeracion.md
```

Actividades realizadas:

* Descubrimiento de hosts.
* Enumeración de servicios.
* Identificación de versiones.
* Enumeración web.
* Recolección de evidencias.

### Análisis de Vulnerabilidades

Archivo:

```text
docs/02-analisis-de-vulnerabilidades.md
```

Hallazgos documentados:
| Vulnerabilidad        | Servicio | Estado   |
| --------------------- | -------- | -------- |
| VSFTPD 2.3.4 Backdoor | FTP      | Validada |

## Evidencias

Las capturas de pantalla se encuentran organizadas en:

```text
screenshots/explotacion/
```

## Descargo de responsabilidad

Este proyecto se desarrolla únicamente con fines educativos y de investigación en entornos autorizados y controlados.
### Documentación

```text
docs/
├── 01-Reconocimiento-y-Enumeracion.md
├── 02-Analisis-de-Vulnerabilidades.md
├── 03-Explotacion-Controlada.md
└── Informe-Final.md
```

---

## Hallazgos Iniciales

Durante la fase de reconocimiento se identificaron múltiples servicios expuestos, entre ellos:

* FTP
* SSH
* Telnet
* SMTP
* DN
