# CyberLab - Pentesting Lab

## Descripción

CyberLab es un laboratorio práctico de ciberseguridad diseñado para desarrollar y demostrar habilidades de pentesting en entornos controlados.

El proyecto documenta paso a paso el proceso completo de una auditoría de seguridad sobre la máquina vulnerable Metasploitable 2 utilizando Kali Linux como sistema atacante.

---

## Objetivos

* Construir un entorno de pentesting aislado.
* Realizar reconocimiento y enumeración de servicios.
* Identificar vulnerabilidades.
* Validar hallazgos mediante explotación controlada.
* Documentar todas las fases de la auditoría.
* Generar evidencia técnica profesional para portafolio.

---

## Entorno del Laboratorio

### Máquina atacante

* Sistema Operativo: Kali Linux
* Dirección IP: 192.168.56.102

### Máquina objetivo

* Sistema Operativo: Metasploitable 2
* Dirección IP: 192.168.56.101

### Topología

```text
Kali Linux (192.168.56.102)
            |
            |
Metasploitable 2 (192.168.56.101)
```

---

## Herramientas Utilizadas

* VirtualBox
* Kali Linux
* Metasploitable 2
* Nmap
* Nikto
* Gobuster
* Git
* GitHub

---

## Metodología

### Fase 1 - Reconocimiento

* Descubrimiento de hosts.
* Identificación de servicios.
* Enumeración inicial de puertos.

### Fase 2 - Enumeración

* Enumeración web.
* Descubrimiento de directorios.
* Identificación de aplicaciones expuestas.

### Fase 3 - Análisis de Vulnerabilidades

* Evaluación de servicios vulnerables.
* Revisión de versiones obsoletas.
* Clasificación de hallazgos.

### Fase 4 - Explotación Controlada

* Validación de vulnerabilidades.
* Obtención de acceso inicial.
* Documentación de evidencias.

### Fase 5 - Post Explotación

* Recolección de información.
* Enumeración interna.
* Análisis de impacto.

---

## Evidencias

### Escaneos

```text
scans/
├── nmap/
├── nikto/
└── gobuster/
```

### Capturas

```text
screenshots/
├── infraestructura/
├── reconocimiento/
├── enumeracion/
├── vulnerabilidades/
└── explotacion/
```

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
* DNS
* Apache HTTP Server
* Samba
* MySQL
* PostgreSQL
* Apache Tomcat

Además, se identificaron aplicaciones web accesibles como:

* phpMyAdmin
* phpinfo.php
* TWiki

---

## Estado Actual

* [x] Infraestructura configurada
* [x] Descubrimiento de hosts
* [x] Enumeración de servicios
* [x] Enumeración web
* [ ] Análisis de vulnerabilidades
* [ ] Explotación controlada
* [ ] Post explotación
* [ ] Informe final

---

## Autor

Juan Diego

Proyecto desarrollado con fines educativos y de aprendizaje en ciberseguridad ofensiva dentro de un entorno controlado.
