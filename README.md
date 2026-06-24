# AAY1108 - Evaluación Parcial 3
## Sistemas y Servicios en Cloud — Duoc UC

**Estudiante:** Vicente Salazar

Este repositorio contiene la evidencia fotográfica del despliegue de dos servidores en AWS (AWS Academy Learner Lab), correspondiente a la Evaluación Parcial 3.

---

## Ítem 1 — Servidor Linux (RHEL 9)

**Configuración:**
- Instancia EC2: Red Hat Enterprise Linux 9
- Tipo de instancia: t3.medium (2 vCPU, 4 GB RAM)
- Security Group: SSH (puerto 22) y HTTP (puerto 80) abiertos, origen 0.0.0.0/0

**Pasos realizados:**

1. Creación de la instancia EC2 con RHEL 9.
   ![Paso 1](./01_image13.png)

2. Configuración del Security Group permitiendo tráfico SSH y HTTP.
   ![Paso 2](./02_image10.png)

3. Creación del par de claves (key pair) para acceso seguro.
   ![Paso 3](./03_image35.png)

4. Conexión remota a la instancia mediante PuTTY (SSH).
   ![Paso 4](./04_image3.png)

5. Instalación del servidor web Apache (`httpd`).
   ![Paso 5](./05_image15.png)

6. Verificación del estado del servicio e inicio del mismo (`systemctl status/start httpd`).
   ![Paso 6](./06_image32.png)

7. Descarga del logo de Duoc UC y alojamiento en el servidor (`/var/www/html/`).
   ![Paso 7](./08_image27.png)

8. Modificación de la página de bienvenida (`index.html`) con nombre del estudiante y logo institucional.
   ![Paso 8](./09_image6.png)

9. Verificación del sitio web desde el navegador.
   ![Paso 9](./11_image4.png)

10. Detención de la instancia.
    ![Paso 10](./12_image20.png)

---

## Ítem 2 — Servidor Windows Server 2019

**Configuración:**
- Instancia EC2: Microsoft Windows Server 2019 Datacenter (con GUI)
- Tipo de instancia: t3.medium (2 vCPU, 4 GB RAM)
- Security Group: RDP (puerto 3389), HTTP (puerto 80) y FTP (puerto 21) abiertos, origen 0.0.0.0/0

**Pasos realizados:**

1. Creación de la instancia EC2 con Windows Server 2019 Base.
   ![Paso 1](./13_image2.png)

2. Configuración del Security Group permitiendo tráfico RDP, HTTP y FTP.
   ![Paso 2](./14_image7.png)

3. Creación del par de claves para desencriptar la contraseña de administrador.
   ![Paso 3](./15_image33.png)

4. Conexión remota mediante Escritorio Remoto (RDP).

5. Instalación del rol "Servidor web (IIS)" junto con el servicio FTP (FTP Server).

6. Verificación de la correcta instalación del rol y servicios.

7. Descarga del logo de Duoc UC y alojamiento en el servidor (`C:\inetpub\wwwroot\`).

8. Creación de una página de bienvenida (`index.html`) con nombre del estudiante y logo institucional.

9. Configuración de un sitio FTP en IIS sobre la misma carpeta de contenido.

10. Verificación del sitio web (HTTP) y del servicio FTP desde el navegador.
    ![Paso final](./16_image9.png)

11. Detención de la instancia.

---

## Evidencias

Todas las capturas de pantalla del proceso se encuentran en este repositorio, numeradas en el orden en que se realizaron los pasos.

---

## Notas

- Ambos servidores fueron desplegados en la región `us-east-1` (Norte de Virginia) utilizando AWS Academy Learner Lab.
- Las contraseñas y claves privadas utilizadas durante el proceso no se incluyen en este repositorio por motivos de seguridad.
