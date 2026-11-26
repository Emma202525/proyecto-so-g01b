**Subgrupo 1B · Entrega individual.** Este sitio documenta el desarrollo del proyecto final de Sistemas Operativos (750001C) en la Universidad del Valle, Semestre 2026-2. No es un sitio oficial de la Universidad del Valle.

## Objetivo

Montar dos máquinas virtuales con Linux en VirtualBox, configurarlas, publicar en Docker Hub una imagen propia, desplegarla en Kubernetes y documentar todo el proceso en este sitio web.

## Integrante y lo que hizo

| Integrante | Parte del proyecto |
| --- | --- |
| Emma D. Álvarez Orozco | Coordinación y repositorio, máquinas virtuales y red, seguridad y usuarios, scripts y procesos, Docker, Kubernetes y sitio web |

## Distribuciones asignadas y versiones (Subgrupo 1B)

| VM gráfica (`g01b-grafica`) | VM de consola (`g01b-consola`) | Imagen base del Dockerfile |
| --- | --- | --- |
| Kubuntu | Debian 13 | Ubuntu |

La versión elegida y su verificación están en la [ficha de versión](plan/ficha-version.md). La planeación y cronograma están en el [plan de trabajo](plan/plan-de-trabajo.md).

## Páginas del proyecto

- [Sprint 0 · Plan de trabajo](plan/plan-de-trabajo.md) y [Ficha de versión](plan/ficha-version.md)
- **Sprint 1 · Montaje** *(completado — configuración de `g01b-grafica` y `g01b-consola`, capturas cargadas y [video de demostración en YouTube](https://youtu.be/d89MGlPl4Uw) publicado)*
- **Sprint 2 · Servicios** *(en preparación — consolidación de servicios y comparativa técnica)*
- **Sprint 3 · Cierre** *(pendiente)*

## Avances del Sprint 1 (`g01b-grafica` · Kubuntu y `g01b-consola` · Debian 13)

- **Máquinas virtuales y usuario:** VMs `g01b-grafica` (Kubuntu) y `g01b-consola` (Debian 13) configuradas en VirtualBox con usuario `emma`.
- **Particiones y snapshots:** Esquema de particiones (`/`, `swap`, `/home`, `/var`), adaptadores de red configurados (Adaptador 1 en NAT y Adaptador 2 en Solo-anfitrión) e instantáneas de instalación limpia creadas en VirtualBox.
- **Verificación en terminal:** Comprobación de identidad, discos, particiones, memoria y red en ambas máquinas mediante comandos en consola (`hostnamectl`, `whoami`, `lsblk`, `df -h`, `free -h` e `ip -br a`).
- **Evidencias, video y repositorio:** Capturas con prompt visible subidas a `sprint 1 capturas` en el repositorio (`proyecto-so-g01b`), documentación actualizada (`plan/ficha-version.md`, `assets/ css/style.scss`, `_config.yml`) y video de demostración del Sprint 1 completado y publicado en YouTube: [https://youtu.be/d89MGlPl4Uw](https://youtu.be/d89MGlPl4Uw) (duración: 2 minutos y 34 segundos).

### Capturas del Sprint 1 (`g01b-consola` · Debian 13)

Evidencias de configuración y verificación de la máquina virtual en Debian 13 (`g01b-consola`):

| Captura 1 | Captura 2 | Captura 3 |
| --- | --- | --- |
| ![Captura 1 del Sprint 1](sprint%201%20capturas/1795563075590-c1aecd66-892a-416c-be16-d90ef3702f1f_1.jpg) | ![Captura 2 del Sprint 1](sprint%201%20capturas/1795563075590-c1aecd66-892a-416c-be16-d90ef3702f1f_2.jpg) | ![Captura 3 del Sprint 1](sprint%201%20capturas/1795563075590-c1aecd66-892a-416c-be16-d90ef3702f1f_3.jpg) |
| *Verificación 1 en `g01b-consola` (Debian 13)* | *Verificación 2 en `g01b-consola` (Debian 13)* | *Verificación 3 en `g01b-consola` (Debian 13)* |

## Sprint 2 · Servicios *(en preparación)*

- **Enfoque de la fase:** Consolidación de servicios en las máquinas virtuales y completado de la comparativa técnica entre las distribuciones del proyecto (Kubuntu en `g01b-grafica`, Debian 13 en `g01b-consola` y base Ubuntu).
- **Base del Sprint 1:** Se apoya en las máquinas virtuales creadas en VirtualBox, los adaptadores de red y snapshots configurados, las capturas subidas a `sprint 1 capturas`, el video del Sprint 1 ([https://youtu.be/d89MGlPl4Uw](https://youtu.be/d89MGlPl4Uw)) y la estructura publicada en `proyecto-so-g01b`.

## Cuadro comparativo (Sprint 1 y Sprint 2 · Kubuntu y Debian 13)

| Criterio / Concepto | Sprint 1 · Montaje (`g01b-grafica` · Kubuntu y `g01b-consola` · Debian 13) | Sprint 2 · Servicios y comparativa (Kubuntu / Debian 13) |
| --- | --- | --- |
| Distribución y versión | Debian 13 (`g01b-consola`) / Kubuntu (`g01b-grafica`) | Contrastar comportamiento y servicios entre Kubuntu y Debian 13 (con base Ubuntu en Dockerfile para etapas posteriores) |
| Estado de la fase | Completado: configuración y capturas `.jpg` en `sprint 1 capturas`, más [video de demostración en YouTube](https://youtu.be/d89MGlPl4Uw) (2:34) publicado | En preparación (consolidación de servicios y criterios comparativos) |
| Instalador y ficha de versión | Documentación de versión actualizada en `plan/ficha-version.md` | Completar y contrastar instaladores de Kubuntu y Debian 13 |
| Herramienta de particionado | Particiones (`/`, `swap`, `/home`, `/var`), verificación en consola (`lsblk`, `df -h`, `free -h`) y snapshots en VirtualBox | Documentar y comparar herramientas de particionado en ambas distribuciones |
| Comando para instalar y actualizar paquetes | Entorno base en Kubuntu y Debian 13 | Documentar y comparar comandos de gestión de paquetes entre Kubuntu y Debian 13 |
| Red y firewall | Adaptador 1 (NAT), Adaptador 2 (Solo-anfitrión), interfaces `lo`, `enp0s3`, `enp0s8` y verificación con `ip -br a` | Detallar y comparar configuración de firewall y servicios de red |
| Grupo de administradores | Usuario `emma` configurado y verificado (`whoami`, `hostnamectl`) en `g01b-grafica` y `g01b-consola` | Verificar y comparar grupos de administración en Kubuntu y Debian 13 |
| Comando para iniciar y detener servicios | Verificación de entorno y servicios en terminal (`systemctl`) | Profundizar gestión y control de servicios (`systemctl`) en el Sprint 2 |
| Gestión web, rutas y control de cambios | Sitio en GitHub Pages (`_config.yml`, `assets/ css/style.scss`, `README.md`), enlace de video [https://youtu.be/d89MGlPl4Uw](https://youtu.be/d89MGlPl4Uw) y rutas en `sprint%201%20capturas` | Mantener actualizada la documentación de servicios y evidencias en el sitio web |

## Conclusiones

*(Se redactará al finalizar el proyecto, detallando lo aprendido, una dificultad con su solución y qué haría distinto).*

## Uso de inteligencia artificial

Para el desarrollo de la estructura de este sitio web en GitHub Pages, la personalización de estilos y la orientación general en el seguimiento de las guías del proyecto, se utilizó el apoyo de la herramienta de inteligencia artificial Gemini. Todas las configuraciones en las máquinas virtuales, particionado, ejecución de comandos en terminal, evidencias gráficas y videos son de autoría propia.

## Repositorio

[https://github.com/Emma202525/proyecto-so-g01b](https://github.com/Emma202525/proyecto-so-g01b)
