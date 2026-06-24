# AAY1108 - Evaluación Parcial 3
## Sistemas y Servicios en Cloud — Duoc UC

**Estudiante:** Vicente Salazar

Este repositorio contiene la evidencia fotográfica del despliegue de dos servidores en AWS (AWS Academy Learner Lab), correspondiente a la Evaluación Parcial 3.

---

## Paso a Paso Completo del Despliegue (16 Pasos)

### Paso 1: Creación de la instancia EC2 con RHEL 9
![Paso 1](./01_image13.png)

### Paso 2: Configuración del Security Group permitiendo tráfico SSH y HTTP
![Paso 2](./02_image10.png)

### Paso 3: Creación del par de claves (key pair) para acceso seguro
![Paso 3](./03_image35.png)

### Paso 4: Conexión remota a la instancia mediante PuTTY (SSH)
![Paso 4](./04_image3.png)

### Paso 5: Instalación del servidor web Apache (`httpd`)
![Paso 5](./05_image15.png)

### Paso 6: Verificación del estado del servicio e inicio del mismo (`systemctl status/start httpd`)
![Paso 6](./06_image32.png)

### Paso 7: Descarga del logo de Duoc UC y alojamiento en el servidor (`/var/www/html/`)
![Paso 7](./08_image27.png)

### Paso 8: Modificación de la página de bienvenida (`index.html`) con nombre del estudiante y logo institucional
![Paso 8](./09_image6.png)

### Paso 9: Verificación del sitio web desde el navegador (Servidor Linux)
![Paso 9](./11_image4.png)

### Paso 10: Detención de la instancia Linux
![Paso 10](./12_image20.png)

### Paso 11: Creación de la instancia EC2 con Windows Server 2019 Base
![Paso 11](./13_image2.png)

### Paso 12: Configuración del Security Group permitiendo tráfico RDP, HTTP y FTP
![Paso 12](./14_image7.png)

### Paso 13: Creación del par de claves para desencriptar la contraseña de administrador
![Paso 13](./15_image33.png)

### Paso 14: Conexión remota mediante Escritorio Remoto (RDP)
![Paso 14](./16_image9.png)

---

## Resumen de Configuraciones

### Ítem 1 — Servidor Linux (RHEL 9)

**Configuración:**
- Instancia EC2: Red Hat Enterprise Linux 9
- Tipo de instancia: t3.medium (2 vCPU, 4 GB RAM)
- Security Group: SSH (puerto 22) y HTTP (puerto 80) abiertos, origen 0.0.0.0/0

**Servicios instalados:**
- Servidor web Apache (httpd)
- Página de bienvenida con nombre del estudiante y logo de Duoc UC

**Pasos realizados (Pasos 1-10):**
1. Creación de la instancia EC2 con RHEL 9
2. Configuración del Security Group permitiendo tráfico SSH y HTTP
3. Creación del par de claves (key pair) para acceso seguro
4. Conexión remota a la instancia mediante PuTTY (SSH)
5. Instalación del servidor web Apache (httpd)
6. Verificación del estado del servicio e inicio del mismo (systemctl status/start httpd)
7. Descarga del logo de Duoc UC y alojamiento en el servidor (/var/www/html/)
8. Modificación de la página de bienvenida (index.html) con nombre del estudiante y logo institucional
9. Verificación del sitio web desde el navegador
10. Detención de la instancia

---

### Ítem 2 — Servidor Windows Server 2019

**Configuración:**
- Instancia EC2: Microsoft Windows Server 2019 Datacenter (con GUI)
- Tipo de instancia: t3.medium (2 vCPU, 4 GB RAM)
- Security Group: RDP (puerto 3389), HTTP (puerto 80) y FTP (puerto 21) abiertos, origen 0.0.0.0/0

**Servicios instalados:**
- Servidor web IIS (Internet Information Services)
- Servidor FTP
- Página de bienvenida con nombre del estudiante y logo de Duoc UC

**Pasos realizados (Pasos 11-16):**
11. Creación de la instancia EC2 con Windows Server 2019 Base
12. Configuración del Security Group permitiendo tráfico RDP, HTTP y FTP
13. Creación del par de claves para desencriptar la contraseña de administrador
14. Conexión remota mediante Escritorio Remoto (RDP)
15. Instalación del rol "Servidor web (IIS)" junto con el servicio FTP (FTP Server)
16. Verificación de la correcta instalación del rol y servicios, descarga del logo de Duoc UC, creación de página de bienvenida, configuración del sitio FTP

---

## Evidencias

Todas las capturas de pantalla del proceso (16 imágenes en total) se encuentran en este repositorio, numeradas del 01 al 16 en el orden secuencial en que se realizaron los pasos.

---

## Notas

- Ambos servidores fueron desplegados en la región `us-east-1` (Norte de Virginia) utilizando AWS Academy Learner Lab.
- Las contraseñas y claves privadas utilizadas durante el proceso no se incluyen en este repositorio por motivos de seguridad.
