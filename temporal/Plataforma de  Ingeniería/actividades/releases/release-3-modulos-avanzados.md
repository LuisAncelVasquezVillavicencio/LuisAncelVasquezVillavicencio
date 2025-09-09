# RELEASE 3 - MÓDULOS AVANZADOS (Semanas 12-18)

Este release se enfoca en los módulos más complejos y críticos del proyecto, incluyendo el módulo PISystem (crítico), auditoría y logs, monitoreo y métricas, y automatización de backups.

---

## 📋 Tabla de Actividades

| Fase/Módulo | Actividad | Detalle Actividades | Entregables | Responsable | Actividades del Cliente |
|-------------|-----------|-------------|-------------|-------------|----------------------|
| **Fase 1: PISystem (CRÍTICO)** | 1.1 TAGs PISystem | Desarrollo de:<br>• Gestión de mallas con formularios individuales<br>• Configuración de TAGs específicos por malla<br>• Configuración de frecuencia de ingesta<br>• Gestión de múltiples mallas en paralelo<br>• Control de accesos por roles para administración de TAGs | • Formularios de configuración de TAGs<br>• Pantalla lista de TAGs | Backend Developer + Frontend Developer | Proporcionar acceso a PISystem APIs y definir TAGs críticos |
| **Fase 1: PISystem (CRÍTICO)** | 1.2 APIs de Integración PISystem | Desarrollo de:<br>• APIs en Node.js para invocar mallas existentes<br>• Ejecución de mallas en paralelo<br>• Almacenamiento de configuraciones en Firestore<br>• Registros de ejecución en Firestore | • APIs de integración PISystem<br>• Ejecución de mallas | Backend Developer + DevOps Engineer | Proporcionar acceso a APIs existentes y configuración de mallas |
| **Fase 1: PISystem (CRÍTICO)** | 1.3 Monitoreo y Alertas PISystem | Desarrollo de:<br>• Pantallas para visualizar métricas del PISystem<br>• Consumo de APIs para obtener métricas:<br>  - Filas procesadas por malla<br>  - Latencia de ejecución<br>  - Estado de ejecuciones (éxito/error)<br>  - Tiempo de procesamiento<br>• Alertas en caso de fallos o retrasos<br>• Visualización de historial de ejecuciones y errores | • Pantallas de monitoreo PISystem<br>• Alertas configuradas | Frontend Developer + Backend Developer | Definir umbrales de alertas y contactos para notificaciones |
| **Fase 2: Auditoría y Logs** | 2.1 Auditoría | Desarrollo de:<br>• Registro automático de acciones específicas del portal:<br>  - Solicitudes de acceso a recursos técnicos<br>  - Aprobaciones y rechazos de solicitudes<br>  - Ejecución de scripts shell<br>  - Configuración de TAGs del PISystem<br>  - Ejecución de backups<br>  - Cambios en roles y permisos<br>• Almacenamiento de logs en Firestore con:<br>  - Timestamps de cada operación<br>  - Usuario que ejecutó la acción<br>  - Acción realizada y parámetros utilizados<br>  - Resultado de la operación (éxito/error)<br>• Búsqueda y filtrado de logs<br>• Exportación de reportes de auditoría | • Auditoría completa<br>• Pantallas de consulta de logs | Backend Developer + Frontend Developer | Definir políticas de retención de logs y formatos de reportes |
| **Fase 3: Monitoreo y Métricas** | 3.1 Monitoreo de Métricas Usuarios | Desarrollo de:<br>• Monitoreo de actividades de los usuarios<br>• Métricas de inicio de sesión (cuántas veces se conectan los usuarios)<br>• Tiempo de sesión (cuánto tiempo permanecen conectados)<br>• Visualización de métricas de usuarios | • Monitoreo de métricas de usuarios<br>• Visualización de métricas de sesiones | Frontend Developer + Backend Developer | Definir umbrales de tiempo de sesión y métricas de usuarios |
| **Fase 4: Automatización de Backups** | 4.1 Backups | Desarrollo de:<br>• Interfaz para ejecutar procesos de respaldo<br>• Monitoreo de estado de backups<br>• Historial de backups con estados<br>• Configuración de frecuencia automática<br>• Notificaciones de éxito/error (mail) | • Backups automatizados<br>• Pantallas de gestión de backups | Backend Developer + Frontend Developer | Proporcionar scripts de backup existentes y definir políticas de respaldo |
| **Fase 4: Automatización de Backups** | 4.2 Historial de Backups | Desarrollo de:<br>• Visualización del historial de backups<br>• Estados de ejecución (éxito, error, en progreso)<br>• Posibilidad de ejecución manual<br>• Historial de ejecuciones por usuario | • Historial de backups<br>• Consulta de ejecuciones | Frontend Developer + Backend Developer | Validar políticas de backup y definir reportes de cumplimiento |

---

## 🎯 Criterios de Éxito

- ✅ **PISystem** funcionando con integración completa
- ✅ **Auditoría** registrando operaciones del portal
- ✅ **Monitoreo de métricas** de usuarios operativo
- ✅ **Alertas** configuradas y funcionando
- ✅ **Backups** automatizados y operativos
- ✅ **Mallas** ejecutándose en paralelo

---

## 🔗 Dependencias

### **Entradas (Inputs):**
- Flujos de aprobación funcionando (Release 2)
- Scripts shell integrados (Release 2)
- Ayuda implementada (Release 2)
- Acceso a PISystem APIs
- Scripts de backup existentes

### **Salidas (Outputs):**
- PISystem completamente funcional
- Auditoría y logs implementados
- Monitoreo de métricas de usuarios operativo
- Alertas configuradas
- Backups automatizados funcionando
- Base sólida para RELEASE 4

---

## ⚠️ Riesgos y Mitigaciones

| Riesgo | Probabilidad | Impacto | Mitigación |
|--------|--------------|---------|------------|
| Complejidad de integración PISystem | Alta | Crítico | Análisis detallado previo y pruebas incrementales |
| Acceso tardío a PISystem APIs | Media | Alto | Solicitud temprana de credenciales |
| Scripts de backup no disponibles | Baja | Medio | Identificación temprana de scripts existentes |
| Disponibilidad del equipo cliente | Baja | Alto | Planificación de reuniones con anticipación |

---

## 📈 Métricas de Seguimiento

- **Progreso de actividades:** 6 actividades total
- **Cumplimiento de hitos:** 4 fases principales
- **Entregables completados:** PISystem, auditoría, métricas usuarios, backups
- **Calidad de entregables:** Revisión por pares y validación del cliente
- **Satisfacción del equipo:** Retrospectivas semanales

---

[← Volver al Índice](../README.md) | [Anterior: RELEASE 2 ←](./release-2-funcionalidades-core.md) | [Siguiente: RELEASE 4 →](./release-4-pruebas-despliegue.md)
