# Ficha de versión y verificación · Sprint 0

**Proyecto Final:** Sistemas Operativos (750001C)  
**Semestre:** 2026-2  
**Subgrupo:** 1B (Entrega individual)  
**Integrante:** Emma D. Álvarez Orozco  

---

## Software base y versiones de las distribuciones

| Componente / Elemento | Distribución / Software | Versión exacta | Propósito en el proyecto |
| --- | --- | --- | --- |
| **Hipervisor** | Oracle VM VirtualBox | 7.x | Entorno de virtualización para alojar las dos VMs del proyecto. |
| **VM Gráfica** (`g01b-grafica`) | Kubuntu (Escritorio) | 26.04.1 LTS (o versión estable vigente) | Entorno gráfico de usuario, navegación web, edición y gestión general. |
| **VM de Consola** (`g01b-consola`) | Debian (Servidor / Base) | 12.x / 13.x (o versión estable vigente) | Servidor dedicado de consola para pruebas de red, Docker y Kubernetes. |
| **Imagen base Docker** | Ubuntu | Última versión estable oficial | Imagen base ligera utilizada para construir el Dockerfile propio del proyecto. |

---

## Criterios de verificación inicial
- **Compatibilidad de arquitectura:** Imágenes de 64 bits (AMD64) compatibles con la virtualización por hardware (VT-x / AMD-V) activada en el equipo anfitrión.
- **Sistemas de archivos:** Uso predeterminado de `ext4` para los sistemas operativos Linux y esquemas de particionado manual específicos en cada máquina virtual.
