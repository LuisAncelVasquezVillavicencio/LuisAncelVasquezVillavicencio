# RELEASE 1 - FUNDACIÓN Y ARQUITECTURA (Semanas 1-5)

Este release establece las bases técnicas y arquitectónicas del proyecto, incluyendo la planificación inicial, análisis de scripts, diseño de arquitectura, UX/UI y configuración de entornos.

---

## 📋 Tabla de Actividades

| Fase/Módulo | Actividad | Detalle Actividades | Entregables | Responsable | Actividades del Cliente |
|-------------|-----------|-------------|-------------|-------------|----------------------|
| **Fase 1: Inicio y Planificación** | 1.1 Presentación de Kick-off | Presentación de kick-off y acuerdos | • Presentación de kick-off<br>• Acta de acuerdos | Project Manager + Tech Lead | Participar en reunión, definir stakeholders clave y aprobar acuerdos |
| **Fase 2: Análisis y Montaje de Scripts** | 2.1 Análisis de Scripts | Inventario de scripts con descripción funcional, análisis de dependencias y requisitos, documentación de parámetros de entrada/salida | • Documento de análisis de scripts | Backend Developer + DevOps Engineer | Entregar scripts existentes, documentación técnica y acceso a sistemas donde se ejecutan |
| **Fase 3: Diseño General y Arquitectura** | 3.1 Documento de Arquitectura Cloud | Diseño de arquitectura modular, modelado de datos, especificación de infraestructura GCP y estrategia de despliegue | • Documento de arquitectura cloud<br>• Modelo de base de datos en Firebase | Solution Architect + DevOps Engineer | Validar conformidad de arquitectura cloud, proporcionar políticas de seguridad y reglas de negocio |
| **Fase 4: UX/UI Design** | 4.2 Wireframes y Prototipos | Mapa del sitio, wireframes y prototipo | • Mapa del sitio<br>• Prototipo de baja fidelidad | UX/UI Designer + Frontend Developer | Participar en entrevistas de usuarios, proporcionar Bricks Design System y aprobar wireframes |
| **Fase 5: Configuración de Entornos** | 5.1 Setup de Ambientes de Desarrollo | Configuración de:<br>• GitHub (repositorios, branches, permisos)<br>• Firebase (Auth, Firestore, Functions, Hosting)<br>• GCP (API Gateway, Cloud Storage)<br>• Accesos a APIs REST existentes para logueo<br>• CI/CD pipeline básico<br>• Documentación de setup | • Ambientes de desarrollo configurados | Solution Architect + DevOps Engineer | Crear cuentas GCP, proporcionar credenciales de APIs existentes, accesos a PI System APIs y definir políticas de acceso |
| **Fase 5: Configuración de Entornos** | 5.2 Configuración de Herramientas | Configuración de:<br>• ESLint, Prettier<br>• Angular CLI<br>• Firebase CLI<br>• TypeScript<br>• Node.js<br>• npm/yarn<br>• Git hooks y Husky | • Herramientas de desarrollo configuradas | Frontend Developer + Backend Developer | Proporcionar estándares de código, políticas de desarrollo y Bricks Design System (ver anexo RFP) |
| **Fase 5: Configuración de Entornos** | 5.3 Configuración de Firebase | Setup inicial de Firebase, configuración de Firestore database y Firebase Authentication | • Cuenta Firebase configurada | Backend Developer | Proporcionar credenciales de Firebase y definir estructura de datos inicial |
| **Fase 6: Usuarios** | 6.1 Gestión de Usuarios | Desarrollo de:<br>• Formularios de creación y edición de usuarios<br>• Listado y búsqueda de usuarios<br>• Asignación de perfiles y roles<br>• Gestión de estados de usuario (activo/inactivo)<br>• Pantalla de perfil del usuario<br>• Configuración de doble autenticación (2FA) por usuario | • Pantallas de administración de usuarios<br>• Pantalla de perfil | Frontend Developer + Backend Developer | Proporcionar estructura de usuarios, perfiles corporativos y campos adicionales necesarios |
| **Fase 7: Permisos** | 7.1 Gestión de Permisos | Desarrollo de:<br>• Formularios de creación y edición de permisos<br>• Listado y búsqueda de permisos<br>• Asignación de permisos a roles<br>• Configuración de permisos por recursos (etiqueta tipo de recurso)<br>• Control granular por acciones (leer, escribir, ejecutar, eliminar) | • Pantallas de administración de permisos | Backend Developer + Frontend Developer | - |
| **Fase 8: Roles** | 8.1 Gestión de Roles | Desarrollo de:<br>• Formularios de creación y edición de roles<br>• Listado y búsqueda de roles<br>• Asignación de permisos a roles<br>• Configuración de perfiles diferenciados | • Pantallas de administración de roles | Backend Developer + Frontend Developer | Proporcionar roles corporativos y perfiles diferenciados |
| **Fase 9: Autenticación y Seguridad** | 9.1 Implementación de Seguridad | Desarrollo de:<br>• Pantalla de login con OAuth 2.0 y Google Workspace<br>• Pantalla de doble autenticación (2FA)<br>• Integración con microservicios existentes para logueo<br>• Seguridad (Firestore Security Rules)<br>• Gestión de sesiones y tokens | • Pantalla de login<br>• Pantalla de doble autenticación<br>• Autenticación y seguridad configurado | Backend Developer + Frontend Developer + DevOps Engineer | Proporcionar configuración de Google Workspace, políticas de seguridad, acceso a servicios de logueo y definir políticas de 2FA |

---

## 🎯 Criterios de Éxito

- ✅ **Arquitectura técnica aprobada** por stakeholders
- ✅ **Scripts existentes analizados** y documentados
- ✅ **Design system implementado** y validado
- ✅ **Ambientes de desarrollo funcionando** correctamente
- ✅ **Usuarios, permisos y roles** configurado
- ✅ **Autenticación y seguridad** implementada

---

## 🔗 Dependencias

### **Entradas (Inputs):**
- Documentos de requerimientos del RFP
- Scripts shell existentes y documentación técnica
- Bricks Design System de la compañía (ver anexo RFP)
- Infraestructura GCP existente
- Credenciales de APIs REST existentes para logueo
- Accesos a PI System APIs
- Estándares de código y políticas de desarrollo (ver anexo RFP)
- Configuración de Google Workspace y políticas de seguridad
- Estructura de usuarios, perfiles corporativos y roles

### **Salidas (Outputs):**
- Arquitectura técnica definida y aprobada
- Scripts analizados y documentados
- Prototipo de baja fidelidad validado
- Ambientes de desarrollo configurados
- Herramientas de desarrollo configuradas
- Cuenta Firebase configurada
- Usuarios, permisos y roles configurado
- Autenticación y seguridad implementado
- Base sólida para RELEASE 2

---

## ⚠️ Riesgos y Mitigaciones

| Riesgo | Probabilidad | Impacto | Mitigación |
|--------|--------------|---------|------------|
| Scripts existentes sin documentación | Media | Alto | Análisis detallado y documentación colaborativa con el cliente |
| Acceso tardío a APIs REST y PI System | Media | Alto | Solicitud temprana de credenciales y accesos en kick-off |
| Bricks Design System no disponible | Baja | Medio | Solicitud temprana del design system, uso de Material UI como fallback |
| Configuración compleja de Google Workspace | Media | Alto | Consulta temprana con equipo de IT y políticas de seguridad |
| Estructura de usuarios y roles no definida | Media | Medio | Definición temprana de perfiles corporativos y roles |
| Disponibilidad del equipo cliente | Baja | Alto | Planificación de reuniones con anticipación y flexibilidad |

---

## 📈 Métricas de Seguimiento

- **Progreso de actividades:** 9 actividades total
- **Cumplimiento de hitos:** 9 fases principales
- **Entregables completados:** Arquitectura, prototipos, configuración, usuarios/permisos/roles, autenticación
- **Calidad de entregables:** Revisión por pares y validación del cliente
- **Satisfacción del equipo:** Retrospectivas semanales

---

[← Volver al Índice](../README.md) | [Siguiente: RELEASE 2 →](./release-2-funcionalidades-core.md)
