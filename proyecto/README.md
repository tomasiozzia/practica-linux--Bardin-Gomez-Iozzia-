# Trabajo Práctico – Administración de Sistemas Linux con Vagrant

Repositorio: `practica-linux--Bardin-Gomez-Iozzia-`  
Integrantes: Bardin – Gómez – Iozzia  

## Roles del equipo

- Alumno A: creación y corrección de `docker-compose.yml`, networking.  
- Alumno B: variables de entorno, parte de LVM y estructura de archivos.  
- Alumno C: testing de contenedores, documentación de errores y capturas de pantalla.  

## Requisitos

- Vagrant y VirtualBox instalados en el host  
- Git instalado dentro de la VM  
- Docker y Docker Compose instalados dentro de la VM  

## Cómo levantar la VM
   `vagrant up `
   `vagrant ssh `
   `cd ~/practica-linux--Bardin-Gomez-Iozzia-/proyecto `

## Estructura del proyecto

- `informacion/`  
  - `ip_vm.txt`: dirección IP asignada a la VM  
  - `system_info.txt`: salida de fastfetch de cada alumno  

- `permisos/`  
  - `usuarios_[apellido].txt`: información del usuario y grupos  
  - `verificacion_permisos_[apellido].txt`: verificaciones de permisos y grupos  

- `lvm/`  
  - `lvm-[apellido].txt`: creación, montaje y verificaciones de LVM  

- `archivos/`  
  - `verificacion_archivos.txt`: comprobación de estructura y operaciones con archivos  

- `contenedores/`  
  - `docker-compose.yml`: servicios nginx, redis, postgres, prometheus, loki, grafana  
  - `prometheus.yml`: configuración de Prometheus  
  - `errores_encontrados.md`: errores del compose y cómo se resolvieron  
  - `logs_completos.txt`: salida completa de logs  
  - `verificacion_contenedores.txt`: verificación de contenedores, redes y volúmenes  
  - `capturas/`:  
    - `docker_ps.png`  
    - `grafana_datasources.png`  
    - `grafana_dashboard.png`  
    - `prometheus_targets.png`  
    - `resolucion_errores.png`  

- `lamp/` (opcional – bonus)  
  - `verificacion_lamp.txt`  
  - `capturas/`: `index_html.png`, `info_php.png`, `test_db_php.png`  

## 🐋 Cómo levantar los contenedores
 ```cd contenedores ```
 ```docker-compose up -d ```
 ```docker ps ```

## Servicios web principales

(Usar la IP listada en `informacion/ip_vm.txt`)

- Grafana: `http://IP_VM:3000` (usuario `admin`, contraseña `practica123`)  
- Prometheus: `http://IP_VM:9090`  
- Nginx: `http://IP_VM:8081`

- 📝 Conclusiones

Este proyecto nos permitió practicar virtualización, administración Linux, Docker,
monitoreo de sistemas, y trabajo colaborativo con Git, completando un entorno
completo de servidor moderno.

-El proyecto nos ayudo a adquirir experiencia en:

-Configuración de entornos reproducibles

-Automatización mediante Vagrant

-Gestión profesional de repositorios

-Debugging real de contenedores

-Monitoreo con herramientas de nivel industria
