# Lista Completa de Actividades - Plataforma de Ingeniería

Este documento contiene la lista completa de todas las actividades del proyecto organizadas por release, fase/módulo y actividad.

---

## 📋 RELEASE 1 - FUNDACIÓN Y ARQUITECTURA (Semanas 1-5)

### **Fase 1: Inicio y Planificación**
- **1.1 Presentación de Kick-off**
  - **Detalle Actividades:** Presentación de kick-off y acuerdos
  - **Actividades del Cliente:** Participar en reunión, definir stakeholders clave y aprobar acuerdos

### **Fase 2: Análisis y Montaje de Scripts**
- **2.1 Análisis de Scripts**
  - **Detalle Actividades:** Inventario de scripts con descripción funcional, análisis de dependencias y requisitos, documentación de parámetros de entrada/salida
  - **Actividades del Cliente:** Entregar scripts existentes, documentación técnica y acceso a sistemas donde se ejecutan

### **Fase 3: Diseño General y Arquitectura**
- **3.1 Documento de Arquitectura Cloud**
  - **Detalle Actividades:** Diseño de arquitectura modular, modelado de datos, especificación de infraestructura GCP y estrategia de despliegue
  - **Actividades del Cliente:** Validar conformidad de arquitectura cloud, proporcionar políticas de seguridad y reglas de negocio

### **Fase 4: UX/UI Design**
- **4.2 Wireframes y Prototipos**
  - **Detalle Actividades:** Mapa del sitio, wireframes y prototipo
  - **Actividades del Cliente:** Participar en entrevistas de usuarios, proporcionar Bricks Design System (se usará en desarrollo) y aprobar wireframes

### **Fase 5: Configuración de Entornos**
- **5.1 Setup de Ambientes de Desarrollo**
  - **Detalle Actividades:** Configuración de:
    - GitHub (repositorios, branches, permisos)
    - Firebase (Auth, Firestore, Functions, Hosting)
    - GCP (API Gateway, Cloud Storage)
    - Accesos a APIs REST existentes para logueo
    - CI/CD pipeline básico
    - Documentación de setup
  - **Actividades del Cliente:** Crear cuentas GCP, proporcionar credenciales de APIs existentes, accesos a PI System APIs y definir políticas de acceso
- **5.2 Configuración de Herramientas**
  - **Detalle Actividades:** Configuración de:
    - ESLint, Prettier
    - Angular CLI
    - Firebase CLI
    - TypeScript
    - Node.js
    - npm/yarn
    - Git hooks y Husky
  - **Actividades del Cliente:** Proporcionar estándares de código, políticas de desarrollo y Bricks Design System (se usará en desarrollo, ver anexo RFP)
- **5.3 Configuración de Firebase**
  - **Detalle Actividades:** Setup inicial de Firebase, configuración de Firestore database y Firebase Authentication
  - **Actividades del Cliente:** Proporcionar credenciales de Firebase y definir estructura de datos inicial

### **Fase 6: Usuarios**
- **6.1 Gestión de Usuarios**
  - **Detalle Actividades:** Desarrollo de:
    - Formularios de creación y edición de usuarios
    - Listado y búsqueda de usuarios
    - Asignación de perfiles y roles
    - Gestión de estados de usuario (activo/inactivo)
    - Pantalla de perfil del usuario
    - Configuración de doble autenticación (2FA) por usuario
  - **Actividades del Cliente:** Proporcionar estructura de usuarios, perfiles corporativos y campos adicionales necesarios

### **Fase 7: Permisos**
- **7.1 Gestión de Permisos**
  - **Detalle Actividades:** Desarrollo de:
    - Formularios de creación y edición de permisos
    - Listado y búsqueda de permisos
    - Asignación de permisos a roles
    - Configuración de permisos por recursos (etiqueta tipo de recurso)
    - Control granular por acciones (leer, escribir, ejecutar, eliminar)
  - **Actividades del Cliente:** -

### **Fase 8: Roles**
- **8.1 Gestión de Roles**
  - **Detalle Actividades:** Desarrollo de:
    - Formularios de creación y edición de roles
    - Listado y búsqueda de roles
    - Asignación de permisos a roles
    - Configuración de perfiles diferenciados
  - **Actividades del Cliente:** Proporcionar roles corporativos y perfiles diferenciados

### **Fase 9: Autenticación y Seguridad**
- **9.1 Implementación de Seguridad**
  - **Detalle Actividades:** Desarrollo de:
    - Pantalla de login con OAuth 2.0 y Google Workspace
    - Pantalla de doble autenticación (2FA)
    - Integración con microservicios existentes para logueo
    - Seguridad (Firestore Security Rules)
    - Gestión de sesiones y tokens
  - **Actividades del Cliente:** Proporcionar configuración de Google Workspace, políticas de seguridad, acceso a servicios de logueo y definir políticas de 2FA

---

## 📋 RELEASE 2 - FUNCIONALIDADES CORE (Semanas 6-11)

### **Fase 1: Flujos de Aprobación**
- **1.1 Solicitudes**
  - **Detalle Actividades:** Desarrollo de:
    - Formularios de solicitud de accesos a recursos técnicos
    - Workflow configurable por roles
    - Notificaciones automáticas de solicitudes
    - Estados de solicitud (pendiente, aprobada, rechazada)
    - Historial de solicitudes y aprobaciones
    - Lista de solicitudes pendientes con filtros por usuario, fecha y tipo de recurso
    - Plantillas de email para notificaciones
  - **Actividades del Cliente:** Aprobar diseño de plantillas de notificaciones email
- **1.2 Aprobaciones**
  - **Detalle Actividades:** Desarrollo de:
    - Pantallas de aprobación para líderes técnicos
    - Notificaciones por email
    - Integración con APIs de IAM (si aplica)
    - Plantillas de email para aprobaciones y rechazos
  - **Actividades del Cliente:** Aprobar diseño de plantillas de notificaciones email

### **Fase 2: Scripts Shell**
- **2.1 Integración Scripts**
  - **Detalle Actividades:** Desarrollo de:
    - Formularios parametrizados para ejecución de scripts
    - Ejecución segura y asincrónica
    - Almacenamiento de parámetros en Firestore
    - Validación de parámetros de entrada
  - **Actividades del Cliente:** -
- **2.2 Gestión Resultados**
  - **Detalle Actividades:** Desarrollo de:
    - Visualización de resultados de ejecución
    - Historial de ejecuciones por usuario
    - Estados de ejecución (éxito, error, en progreso)
  - **Actividades del Cliente:** -

### **Fase 3: Ayuda y Documentación**
- **3.1 Ayuda**
  - **Detalle Actividades:** Desarrollo de:
    - Mantenimiento de FAQ (crear, editar, eliminar, listar)
    - Carga de manuales (archivos, videos, PDF)
    - Búsqueda por título y categorización
    - Tags para filtrado por categoría
  - **Actividades del Cliente:** Proporcionar contenido inicial de FAQ y manuales
- **3.2 Recursos Multimedia**
  - **Detalle Actividades:** Desarrollo de:
    - Almacenamiento de videos tutoriales en Cloud Storage
    - Reproductor de videos integrado
    - Gestión de archivos adjuntos
    - Administración de contenido multimedia
  - **Actividades del Cliente:** Proporcionar videos tutoriales y recursos multimedia iniciales

---

## 📋 RELEASE 3 - MÓDULOS AVANZADOS (Semanas 12-18)

### **Fase 1: PISystem (CRÍTICO)**
- **1.1 TAGs PISystem**
  - **Detalle Actividades:** Desarrollo de:
    - Gestión de mallas con formularios individuales
    - Configuración de TAGs específicos por malla
    - Configuración de frecuencia de ingesta
    - Gestión de múltiples mallas en paralelo
    - Control de accesos por roles para administración de TAGs
  - **Actividades del Cliente:** Proporcionar acceso a PISystem APIs y definir TAGs críticos
- **1.2 APIs de Integración PISystem**
  - **Detalle Actividades:** Desarrollo de:
    - APIs en Node.js para invocar mallas existentes
    - Ejecución de mallas en paralelo
    - Almacenamiento de configuraciones en Firestore
    - Registros de ejecución en Firestore
  - **Actividades del Cliente:** Proporcionar acceso a APIs existentes y configuración de mallas
- **1.3 Monitoreo y Alertas PISystem**
  - **Detalle Actividades:** Desarrollo de:
    - Pantallas para visualizar métricas del PISystem
    - Consumo de APIs para obtener métricas:
      - Filas procesadas por malla
      - Latencia de ejecución
      - Estado de ejecuciones (éxito/error)
      - Tiempo de procesamiento
    - Alertas en caso de fallos o retrasos
    - Visualización de historial de ejecuciones y errores
  - **Actividades del Cliente:** Definir umbrales de alertas y contactos para notificaciones

### **Fase 2: Auditoría y Logs**
- **2.1 Auditoría**
  - **Detalle Actividades:** Desarrollo de:
    - Registro automático de acciones específicas del portal:
      - Solicitudes de acceso a recursos técnicos
      - Aprobaciones y rechazos de solicitudes
      - Ejecución de scripts shell
      - Configuración de TAGs del PISystem
      - Ejecución de backups
      - Cambios en roles y permisos
    - Almacenamiento de logs en Firestore con:
      - Timestamps de cada operación
      - Usuario que ejecutó la acción
      - Acción realizada y parámetros utilizados
      - Resultado de la operación (éxito/error)
    - Búsqueda y filtrado de logs
    - Exportación de reportes de auditoría (CSV o Excel)
  - **Actividades del Cliente:** Definir políticas de retención de logs y formatos de reportes

### **Fase 3: Monitoreo y Métricas**
- **3.1 Monitoreo de Métricas Usuarios**
  - **Detalle Actividades:** Desarrollo de:
    - Monitoreo de actividades de los usuarios
    - Métricas de inicio de sesión (cuántas veces se conectan los usuarios)
    - Tiempo de sesión (cuánto tiempo permanecen conectados)
    - Visualización de métricas de usuarios
  - **Actividades del Cliente:** Definir umbrales de tiempo de sesión y métricas de usuarios

### **Fase 4: Automatización de Backups**
- **4.1 Backups**
  - **Detalle Actividades:** Desarrollo de:
    - Interfaz para ejecutar procesos de respaldo
    - Monitoreo de estado de backups
    - Historial de backups con estados
    - Configuración de frecuencia automática
    - Notificaciones de éxito/error (mail)
  - **Actividades del Cliente:** Proporcionar scripts de backup existentes y definir políticas de respaldo
- **4.2 Historial de Backups**
  - **Detalle Actividades:** Desarrollo de:
    - Visualización del historial de backups
    - Estados de ejecución (éxito, error, en progreso)
    - Posibilidad de ejecución manual
    - Historial de ejecuciones por usuario
  - **Actividades del Cliente:** Validar políticas de backup y definir reportes de cumplimiento

---

## 📋 RELEASE 4 - PRUEBAS Y DESPLIEGUE (Semanas 19-22)

### **Fase 1: Pruebas**
- **1.1 Testing Integral**
  - **Detalle Actividades:** Desarrollo de:
    - Pruebas de funcionalidad de todos los módulos
    - Pruebas de seguridad y autenticación
    - Definición de casos de prueba específicos
    - Validación de resultados
  - **Actividades del Cliente:** -
- **1.2 Corrección de Bugs**
  - **Detalle Actividades:** Desarrollo de:
    - Corrección de bugs identificados
    - Optimización de rendimiento
    - Validación de correcciones
  - **Actividades del Cliente:** -

### **Fase 2: Despliegue**
- **2.1 Acompañamiento para Despliegue**
  - **Detalle Actividades:**
    - Preparación de recursos para despliegue
    - Configuración de capacidad de actualizar código fuente
    - Acompañamiento durante el despliegue
  - **Actividades del Cliente:** Configurar ambiente de producción y realizar despliegue con acompañamiento técnico

### **Fase 3: Documentación**
- **3.1 Entrega de Documentación**
  - **Detalle Actividades:**
    - Compilación de documentación técnica generada
    - Documentación de arquitectura y código
    - Manuales de usuario finales
  - **Actividades del Cliente:** Recibir documentación final

### **Fase 4: Capacitación**
- **4.1 Capacitación de Usuarios**
  - **Detalle Actividades:**
    - 2 sesiones de capacitación sobre la herramienta
    - Capacitación basada en manual de usuario
  - **Actividades del Cliente:** Coordinar asistencia a capacitaciones

### **Fase 5: Transferencia**
- **5.1 Transferencia de Conocimiento**
  - **Detalle Actividades:**
    - 1 sesión sobre arquitectura del proyecto
    - 1 sesión sobre el código
  - **Actividades del Cliente:** Designar equipo interno para recibir transferencia

---

*Esta lista proporciona una visión completa de todas las actividades del proyecto, facilitando el seguimiento, planificación y gestión de recursos.*
