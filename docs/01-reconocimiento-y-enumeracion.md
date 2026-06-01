Laboratorio de Pentesting - Metasploitable 2
Fase 1: Reconocimiento y Enumeración
Autor: Juan Diego Chiquillo Pedraza
Fecha: Mayo 2026
Máquina atacante: Kali Linux (192.168.56.102)
Máquina objetivo: Metasploitable 2 (192.168.56.101)
________________________________________
1. Objetivo
Realizar actividades de reconocimiento y enumeración sobre una máquina vulnerable Metasploitable 2 dentro de un entorno controlado de laboratorio, identificando hosts activos, servicios expuestos, aplicaciones web accesibles y posibles hallazgos de seguridad.
________________________________________
2. Infraestructura del Laboratorio
El laboratorio fue desplegado utilizando VirtualBox y una red Host-Only para aislar el entorno de pruebas.
Equipos involucrados
Equipo	Sistema Operativo	Dirección IP
Kali Linux	Kali Linux	192.168.56.102
Metasploitable 2	Ubuntu Linux Vulnerable	192.168.56.101
Evidencias
•	Captura de configuración IP de Kali Linux.
•	Captura de configuración IP de Metasploitable 2.
•	Prueba de conectividad mediante ICMP (ping).
________________________________________
3. Descubrimiento de Hosts
Se realizó un escaneo de descubrimiento utilizando Nmap para identificar dispositivos activos dentro de la red.
Comando utilizado
nmap -sn 192.168.56.0/24
Resultado
Se identificaron cuatro hosts activos dentro del segmento de red.
Evidencia
Archivo:
scans/nmap/01_host_discovery.txt
________________________________________
4. Enumeración de Servicios
Posteriormente se realizó un escaneo de versiones para identificar servicios y tecnologías expuestas en la máquina objetivo.
Comando utilizado
nmap -sV 192.168.56.101
Servicios identificados
Puerto	Servicio	Versión
21	FTP	vsftpd 2.3.4
22	SSH	OpenSSH 4.7p1
23	Telnet	Linux telnetd
25	SMTP	Postfix smtpd
53	DNS	ISC BIND 9.4.2
80	HTTP	Apache 2.2.8
111	RPCBind	RPC Service
139	NetBIOS	Samba
445	SMB	Samba
512	rexecd	Netkit-rsh
513	login	Remote Login
514	shell	Netkit rshd
1099	Java RMI	GNU Classpath
1524	Bind Shell	Root Shell
2049	NFS	Network File System
2121	FTP	ProFTPD 1.3.1
3306	MySQL	5.0.51
5432	PostgreSQL	8.3.x
5900	VNC	Protocol 3.3
6667	IRC	UnrealIRCd
8009	AJP13	Apache JServ
8180	HTTP	Apache Tomcat
Evidencia
Archivo:
scans/nmap/02_service_enumeration.txt
________________________________________
5. Enumeración Web
Se identificó un servidor Apache HTTP ejecutándose sobre el puerto 80 y un servidor Apache Tomcat sobre el puerto 8180.
Recursos descubiertos
•	phpMyAdmin
•	phpinfo.php
•	TWiki
•	Directorio /dav
•	Directorio /test
•	Apache Tomcat
________________________________________
6. Análisis con Nikto
Se ejecutó un escaneo web automatizado utilizando Nikto.
Comando utilizado
nikto -h http://192.168.56.101
Hallazgos relevantes
•	Apache 2.2.8 desactualizado.
•	PHP 5.2.4 desactualizado.
•	Archivo phpinfo.php accesible públicamente.
•	Directorios indexados.
•	Método HTTP TRACE habilitado.
•	phpMyAdmin accesible.
•	Ausencia de cabeceras de seguridad.
Evidencia
Archivo:
scans/nikto/01_nikto_scan.txt
________________________________________
7. Enumeración de Directorios
Se utilizó Gobuster para descubrir directorios y recursos accesibles.
Comando utilizado
gobuster dir -u http://192.168.56.101 -w /usr/share/wordlists/dirb/common.txt
Directorios encontrados
•	/dav/
•	/phpMyAdmin/
•	/phpinfo.php
•	/test/
•	/twiki/
Evidencia
Archivo:
scans/gobuster/01_gobuster_scan.txt
________________________________________
8. Hallazgos Iniciales
ID	Hallazgo	Riesgo
WEB-001	Apache 2.2.8 obsoleto	Medio
WEB-002	PHP 5.2.4 obsoleto	Alto
WEB-003	phpinfo.php expuesto	Medio
WEB-004	phpMyAdmin accesible	Medio
WEB-005	Directory Listing habilitado	Bajo
WEB-006	Método HTTP TRACE habilitado	Medio
WEB-007	Ausencia de cabeceras de seguridad	Bajo
________________________________________
9. Conclusiones
Durante la fase de reconocimiento y enumeración se identificó una amplia superficie de ataque compuesta por múltiples servicios de red, aplicaciones web vulnerables y configuraciones inseguras.
Los resultados obtenidos servirán como base para la siguiente fase del laboratorio, enfocada en el análisis de vulnerabilidades y validación controlada de los hallazgos identificados.
