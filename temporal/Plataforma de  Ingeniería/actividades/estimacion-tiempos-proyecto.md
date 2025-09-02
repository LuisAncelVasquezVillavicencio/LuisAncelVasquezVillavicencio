# Estimación de Tiempos por Fase y Módulo - Plataforma de Ingeniería

Esta estimación está basada en el plan de actividades detallado para la Plataforma de Ingeniería. Los tiempos son orientativos y asumen un equipo de 6-8 personas con experiencia en proyectos similares.

---

## Estimación por Fase

> **Nota:** La siguiente tabla muestra la estimación de esfuerzo y duración por fase/módulo. El cronograma visual por semanas, que aparece más abajo, representa la distribución y solapamiento de actividades en el tiempo. Ambas tablas son complementarias y no contradictorias.

| Fase / Módulo                                 | Descripción                                                                 | Tiempo estimado |
|-----------------------------------------------|-----------------------------------------------------------------------------|-----------------|
| 1. Inicio y Planificación                     | Definición de alcance, cronograma, recursos y plan de trabajo del proyecto | 3 días          |
| 2. Análisis y Montaje de Scripts de Integración| Análisis de scripts existentes, refactorización y preparación para integración | 3-4 semanas*    |
| 3. Diseño General y Arquitectura              | Arquitectura modular orientada a microservicios sin servidor, documento de arquitectura e infraestructura, especificación técnica de integración, estructura de base de datos | 1 semana        |
| 4. UX/UI Design                               | Diseño de prototipos  | 3 semanas       |
| 5. Configuración de Entornos y Herramientas   | Configuración de ambientes de desarrollo, calidad y producción              | 1 semana        |
| 6.1. Usuarios                   | Gestión de usuarios y perfiles con control de acceso basado en roles (RBAC), integración con microservicios existentes para logueo (ver anexo - Estándar y lineamientos Desarrollo, anexo - Lineamientos de desarrollo seguro) | 2 semanas       |
| 6.2. Permisos                                | Sistema de gestión de permisos y accesos a recursos del sistema con control granular por acciones (leer, escribir, ejecutar, eliminar) | 1 semana        |
| 6.3. Roles                                   | Definición e implementación de roles de usuario (RBAC) con perfiles diferenciados (ingeniero de datos, analista, líder técnico, administrador) | 0.5 semana      |
| 6.4. Autenticación y Seguridad                | Implementación de OAuth 2.0 con Google Workspace y sistema de seguridad (Firestore Security Rules) | 1.5 semanas     |
| 6.5. Flujos de Aprobación                    | Sistema de solicitudes y aprobaciones para accesos a recursos técnicos (scripts) con workflow configurable por roles | 3 semanas       |
| 6.6. Scripts Shell (incluye formularios parametrizados) | Integración de scripts shell existentes con interfaz web parametrizada, ejecución segura y asincrónica mediante Cloud Functions, almacenamiento de parámetros y resultados en Firestore | 3.5 semanas     |
| 6.7. Ayuda y Documentación                   | Sistema de ayuda técnica y funcional con recursos multimedia (FAQ, manuales, videos) almacenados en Firestore y Cloud Storage | 2 semanas       |
| 6.8. Módulo PISystem (CRÍTICO)               | Administrador de TAGs del PISystem para integración con Data Lake         | 5-7 semanas     |
| 6.9. Módulo de Auditoría y Logs              | Sistema de registro y auditoría de todas las operaciones del sistema con logs automáticos (timestamps, usuario, acción, resultado) almacenados en Firestore | 2 semanas       |
| 6.10. Módulo de Monitoreo y Métricas (Dashboard)        | Dashboard de métricas clave (filas procesadas, latencia, estado de ejecuciones) con alertas por correo en caso de fallos o retrasos | 1.5-2 semanas   |
| 6.11. Módulo de Automatización de Backups    | Sistema de ejecución y monitoreo de procesos de respaldo automático con historial de backups, estados (éxito, error, en progreso) y ejecución manual desde interfaz web | 3.5 semanas     |
| 7. Pruebas Generales y Validación            | Testing integral del sistema, pruebas de usabilidad con usuarios reales, feedback continuo e iterativo, validación de funcionalidades y corrección de bugs | 3 semanas       |
| 8. Despliegue y Puesta en Producción         | Despliegue en ambiente de producción y configuración final del sistema     | 1.5 semanas     |
| 9. Capacitación, Documentación y Mantenimiento| Capacitación de usuarios, documentación final y plan de mantenimiento     | 1.5 semanas     |
| 10. Soporte                                   | Soporte post-implementación y resolución de incidencias                    | 2 semanas       |
| 11. Transferencia de Conocimiento            | Transferencia de conocimiento técnico al equipo interno                    | 1 semana        |

---

## Cronograma Visual por Semanas

| Actividad / Semana                                      | S1 | S2 | S3 | S4 | S5 | S6 | S7 | S8 | S9 | S10 | S11 | S12 | S13 | S14 | S15 | S16 | S17 | S18 | S19 | S20 | S21 | S22 | S23 | S24 |
|---------------------------------------------------------|----|----|----|----|----|----|----|----|----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **🟢 RELEASE 1 - FUNDACIÓN Y ARQUITECTURA (S1-S5)**     | X  | X  | X  | X  | X  |    |    |    |    |     |     |     |     |     |     |     |     |     |     |     |     |     |     |
| Inicio y Planificación                                  | X  |    |    |    |    |    |    |    |    |     |     |     |     |     |     |     |     |     |     |     |     |     |
| Análisis y Montaje de Scripts de Integración            |    | X  | X  | X  | X  |    |    |    |    |     |     |     |     |     |     |     |     |     |     |     |     |     |
| Diseño General y Arquitectura                           |    | X  |    |    |    |    |    |    |    |     |     |     |     |     |     |     |     |     |     |     |     |     |
| UX/UI Design                                            | X  | X  | X  |    |    |    |    |    |    |     |     |     |     |     |     |     |     |     |     |     |     |     |
| Configuración de Entornos y Herramientas                |    | X  | X  |    |    |    |    |    |    |     |     |     |     |     |     |     |     |     |     |     |     |     |
| Usuarios                                                |    |    |    | X  | X  |    |    |    |    |     |     |     |     |     |     |     |     |     |     |     |     |     |
| Permisos                                                |    |    |    | X  | X  |    |    |    |    |     |     |     |     |     |     |     |     |     |     |     |     |     |     |
| Roles                                                   |    |    |    | X  | X  |    |    |    |    |     |     |     |     |     |     |     |     |     |     |     |     |     |     |
| Autenticación y Seguridad                               |    |    |    | X  | X  |    |    |    |    |     |     |     |     |     |     |     |     |     |
| **🟢 RELEASE 2 - FUNCIONALIDADES CORE (S6-S11)**        |    |    |    |    |    | X  | X  | X  | X  |  X  |  X  |     |     |     |     |     |     |     |
| Flujos de Aprobación                                    |    |    |    |    |    | X  | X  | X  |     |     |     |     |     |     |     |     |     |     |
| Scripts Shell (Formularios)                             |    |    |    |    |    |    |    | X  | X   | X   | X   |     |     |     |     |     |     |     |
| Ayuda y Documentación                                   |    |    |    |    |    |    |    |    |  X  |  X  |  X  |     |     |     |     |     |     |     |     |
| **🟢 RELEASE 3 - MÓDULOS AVANZADOS (S12-S18)**          |    |    |    |    |    |    |    |    |     |     |     |  X  |  X  |  X  |  X  |  X  |  X  |  X  |
| PISystem (CRÍTICO)                                      |    |    |    |    |    |    |    |    |     |     |     |  X  |  X  |  X  |  X  |  X  |  X  |  X  |
| Auditoría y Logs                                        |    |    |    |    |    |    |    |    |    |     |     |  X  |  X  |  X  |     |     |     |     |     |
| Monitoreo y Métricas                                    |    |    |    |    |    |    |    |    |    |     |     |     |     |  X  |  X  |  X  |     |     |
| Automatización de Backups                               |    |    |    |    |    |    |    |    |    |     |     |     |     |     |     |  X  |  X  |  X  |
| **🟢 RELEASE 4 - PRUEBAS Y DESPLIEGUE (S19-S22)**       |    |    |    |    |    |    |    |    |    |     |     |     |     |     |     |     |     |     |  X  |  X  |  X  |  X  |
| Pruebas Generales y Validación                          |    |    |    |    |    |    |    |    |    |     |     |     |     |     |     |     |     |     |  X  |  X  |     |     |
| Despliegue y Puesta en Producción                       |    |    |    |    |    |    |    |    |    |     |     |     |     |     |     |     |     |     |     |     |  X  |  X  |
| Capacitación, Documentación y Mantenimiento             |    |    |    |    |    |    |    |    |    |     |     |     |     |     |     |     |     |     |     |     |  X  |  X  |
| Transferencia de Conocimiento                           |    |    |    |    |    |    |    |    |    |     |     |     |     |     |     |     |     |     |     |     |  X  |  X  |
| **🟢 RELEASE 5 - SOPORTE POST-PRODUCCIÓN (S23-S24)**    |    |    |    |    |    |    |    |    |    |     |     |     |     |     |     |     |     |     |     |     |     |     |  X  |  X  |

---

## 🚀 Tecnologías y Requisitos Técnicos Requeridos

### **Frontend:**
- **Angular 18+** con Material UI
- **OAuth 2.0** con Google Sign-In
- **Lazy Loading** y componentes reutilizables
- **Bricks Design System** de la compañía
- **Responsive design** para dispositivos móviles

### **Backend:**
- **Node.js** con Cloud Functions
- **Firebase Authentication** para gestión de sesiones
- **Firestore** como base de datos NoSQL
- **Cloud Storage** para archivos multimedia

### **Infraestructura:**
- **Google Cloud Platform (GCP)**
- **Firebase Hosting** o Cloud Run para SSR
- **Despliegue automatizado** con pipeline CI/CD
- **Microservicios** habilitados por arquitectura TI existente

### **Integración:**
- **PI System** para TAGs y Data Lake
- **APIs REST** existentes para logueo
- **Scripts shell** existentes para integración

### **Despliegue Automatizado:**
El RFP especifica que se debe contar con **capacidad de actualizar el código fuente** y **pipeline CI/CD** para despliegue automatizado en los ambientes de desarrollo, calidad y producción existentes.

---

*La estimación depende de la complejidad y estado de los scripts a integrar (estimados 5 scripts). El tiempo puede variar si los scripts requieren refactorización, documentación adicional o integración compleja, ya que aún no se ha realizado un análisis detallado sobre su estado actual.

---

## Resumen Total Estimado
- **Mínimo realista:** 24 semanas (alrededor de 6 meses)
- **Con holgura y validaciones:** 26 semanas (6.5 meses)
- **Total de fases:** 15 fases distribuidas en 5 releases

---

## Notas Importantes
- Si el equipo es más pequeño, el tiempo puede aumentar.
- Si hay dependencias externas (espera de validaciones, cambios en scripts, etc.), sumar buffers.
- Si se requiere mucha personalización o integración compleja, sumar tiempo.
- Las fases de pruebas y validación suelen extenderse si hay muchos cambios o feedback de usuarios.

Esta estimación debe ser revisada y ajustada según la realidad y recursos del proyecto. 