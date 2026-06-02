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

### Fase 1 - Reconocimiento y Enumeración

**Archivo:**

`docs/01-reconocimiento-y-enumeracion.md`

Actividades realizadas:

* Descubrimiento de hosts.
* Enumeración de servicios.
* Identificación de versiones.
* Enumeración web.
* Recolección de evidencias.

### Fase 2 - Análisis de Vulnerabilidades

**Archivo:**

`docs/02-analisis-de-vulnerabilidades.md`

Hallazgos documentados:

| Vulnerabilidad        | Servicio | Estado   |
| --------------------- | -------- | -------- |
| VSFTPD 2.3.4 Backdoor | FTP      | Validada |

## Evidencias

Las capturas de pantalla se encuentran organizadas en:

* screenshots/infraestructura/
* screenshots/reconocimiento/
* screenshots/enumeracion/
* screenshots/explotacion/

## Estado Actual

* [x] Infraestructura configurada
* [x] Descubrimiento de hosts
* [x] Enumeración de servicios
* [x] Enumeración web
* [x] Análisis de vulnerabilidades
* [x] Explotación controlada
* [ ] Post-explotación
* [ ] Informe final

## Autor

Juan Diego Chiquillo Pedraza

## Descargo de responsabilidad

Este proyecto se desarrolla únicamente con fines educativos y de investigación en entornos autorizados y controlados.
