# Ficha de versión y verificación · Sprint 0

**Proyecto Final:** Sistemas Operativos (750001C)  
**Semestre:** 2026-2  
**Subgrupo:** 1B (Entrega individual)  
**Integrante:** Emma D. Álvarez Orozco  

---

## Ficha de versión · Kubuntu (VM gráfica `g01b-grafica`)

| Pregunta | Respuesta | Enlace |
| --- | --- | --- |
| Versión y fecha | Kubuntu 24.04 LTS ("Noble Numbat"), versión de soporte extendido estable y recomendada por su facilidad de uso y compatibilidad con VirtualBox. | https://kubuntu.org/getkubuntu/ |
| Actualizaciones de seguridad | Soporte oficial de actualizaciones de seguridad durante 3 años para el entorno Kubuntu y 5 años en la base Ubuntu LTS (hasta abril de 2029). | https://ubuntu.com/about/release-cycle |
| Requisitos de hardware y VirtualBox | Compatible con Oracle VM VirtualBox 7.x con entorno gráfico (KDE Plasma); arquitectura de 64 bits (AMD64) con virtualización por hardware (VT-x / AMD-V) activada. | https://kubuntu.org/ |
| Manual del particionado | Sí, el instalador permite particionado manual con sistema de archivos `ext4` (por ejemplo `/`, `swap` y `/home`). | https://help.ubuntu.com/ |
| Guía oficial de Docker Engine | Sí, compatible con instalación de Docker Engine desde el repositorio oficial para Ubuntu. | https://docs.docker.com/engine/install/ubuntu/ |
| Imagen base en Docker Hub | No aplica directamente a esta VM gráfica (la imagen base asignada al Subgrupo 1B para el `Dockerfile` es Ubuntu). | https://hub.docker.com/_/ubuntu |

---

## Ficha de versión · Debian (VM de consola `g01b-consola`)

| Pregunta | Respuesta | Enlace |
| --- | --- | --- |
| Versión y fecha | Debian 13 ("Trixie"), rama estable vigente (lanzada inicialmente el 9 de agosto de 2025). | https://www.debian.org/releases/ |
| Actualizaciones de seguridad | Soporte estándar del equipo de seguridad de Debian (aproximadamente 3 años desde el lanzamiento), seguido de soporte LTS. | https://www.debian.org/security/ |
| Requisitos de hardware y VirtualBox | Compatible con Oracle VM VirtualBox 7.x sin entorno gráfico; 2 GB de RAM (ampliables a 3 GB en el Sprint 3 para Minikube), 25 GB de disco y 2 CPU. | https://www.debian.org/releases/stable/ |
| Manual del particionado | Sí, el instalador de Debian permite particionado manual en `ext4` para crear `/` (mínimo 10 GB), `/var`, `swap` y `/home`. | https://www.debian.org/doc/ |
| Guía oficial de Docker Engine | Sí, guía oficial paso a paso para instalar Docker Engine desde el repositorio oficial de Docker para Debian. | https://docs.docker.com/engine/install/debian/ |
| Imagen base en Docker Hub | No aplica a esta VM (la imagen base asignada al Subgrupo 1B para el `Dockerfile` es Ubuntu). | https://hub.docker.com/_/ubuntu |

---

## Ficha de versión · Ubuntu (imagen base del Dockerfile)

| Pregunta | Respuesta | Enlace |
| --- | --- | --- |
| Versión y fecha | Ubuntu 24.04 LTS ("Noble Numbat"), etiqueta oficial `ubuntu:24.04` (versión de soporte extendido estable recomendada). | https://ubuntu.com/about/release-cycle |
| Actualizaciones de seguridad | Soporte estándar de seguridad durante 5 años (hasta abril de 2029). | https://ubuntu.com/security/ |
| Requisitos de hardware y VirtualBox | No aplica máquina virtual propia; se usa como imagen base ligera de contenedor dentro de Docker sobre el host Debian. | https://docs.docker.com/get-started/docker-overview/ |
| Manual del particionado | No aplica (los contenedores usan el sistema de archivos en capas de Docker). | https://docs.docker.com/storage/ |
| Guía oficial de Docker Engine | Sí, Ubuntu cuenta con soporte y repositorio oficial completo en la documentación de Docker Engine. | https://docs.docker.com/engine/install/ubuntu/ |
| Imagen base en Docker Hub | Sí, disponible como *Docker Official Image* bajo el nombre `ubuntu` con etiqueta LTS verificada (`ubuntu:24.04`). | https://hub.docker.com/_/ubuntu |

---

## Criterios de verificación inicial

* **Hipervisor:** Oracle VM VirtualBox 7.x.
* **Compatibilidad de arquitectura:** Imágenes de 64 bits (AMD64) compatibles con la virtualización por hardware (VT-x / AMD-V) activada en el equipo anfitrión.
* **Sistemas de archivos:** Uso predeterminado de `ext4` para los sistemas operativos Linux y esquemas de particionado manual específicos en cada máquina virtual.
