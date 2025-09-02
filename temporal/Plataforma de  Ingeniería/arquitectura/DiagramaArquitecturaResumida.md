# Plataforma de Ingeniería - Arquitectura Resumida

Este documento explica el diagrama de arquitectura de la "Plataforma de Ingeniería" para Cementos Pacasmayo, alineado con los requerimientos funcionales y técnicos del proyecto. La plataforma está diseñada para facilitar la gestión, automatización y control de procesos de ingeniería y datos, integrando herramientas y flujos de trabajo en una solución web moderna, segura y escalable.

---

## Descripción General del Diagrama

El diagrama representa la arquitectura lógica y tecnológica de la plataforma, mostrando cómo interactúan los diferentes componentes y servicios, tanto internos como externos.

### 1. **Usuario y Seguridad**
- **Usuarios** acceden a la plataforma desde cualquier dispositivo (PC, tablet, móvil).
- **Cloudflare** actúa como capa de seguridad perimetral (CDN/DNS), protegiendo el acceso y mejorando el rendimiento global.

### 2. **Hosting**
- **Firebase Hosting** (Google Cloud) aloja el frontend de la aplicación, sirviendo la web de manera rápida, segura y escalable.

### 3. **Control de Versiones y Entornos**
- **GitHub** se utiliza para el control de versiones del código fuente.
- Se gestionan diferentes entornos: Desarrollo (Dev), Calidad (QA) y Producción (Prod), permitiendo flujos de integración y despliegue continuo.

### 4. **Frontend**
- **Angular 18+**: Framework principal para el desarrollo de la interfaz de usuario.
- **Material UI & Bricks Design System**: Garantizan una experiencia visual coherente, moderna y alineada a la identidad de la empresa.
- **Google Identity Platform (OAuth 2.0)**: Autenticación centralizada con cuentas corporativas de Google Workspace.
- **API Gateway**: Todas las comunicaciones del frontend con el backend pasan por el API Gateway, asegurando conexiones HTTPS y control de acceso.
- **Módulos funcionales**:
  - **Usuarios, Permisos, Roles**: Gestión de cuentas, permisos y perfiles de usuario.
  - **Ayuda**: Acceso a documentación y soporte.
  - **Flujos de Aprobación**: Interfaz para gestionar solicitudes y aprobaciones de acciones críticas.
  - **Scripts Shell**: Ejecución de scripts y comandos automatizados sobre nubes externas.

### 5. **Backend**
- **API Gateway**: Centraliza y protege el acceso a los servicios backend.
- **Node.js Functions (Cloud Functions)**: Lógica de negocio serverless, ejecutando operaciones bajo demanda.
- **Firebase Authentication**: Servicio de autenticación adicional para usuarios y servicios.
- **Firestore Security Rules**: Políticas de seguridad para el acceso a la base de datos.
- **Cloud IAM**: Gestión de identidades y permisos a nivel de Google Cloud.
- **Cloud Logging**: Registro y auditoría de todas las operaciones y eventos relevantes.
- **Lógica de Aprobación**: Implementa los flujos de aprobación para acciones críticas, incluyendo el envío de notificaciones por correo electrónico a los responsables (el servicio de email se definirá en la implementación).
- **Docker**: Permite la ejecución de scripts o microservicios en contenedores, facilitando la integración y portabilidad.

### 6. **Datos**
- **Firestore**: Base de datos NoSQL para almacenar información de la plataforma (usuarios, permisos, logs, etc.).
- **Cloud Storage**: Almacenamiento de archivos y datos no estructurados.

### 7. **Integraciones Externas**
- **APIs Internas y Scripts Shell**: Permiten la automatización y orquestación de tareas en nubes externas.
- **Nubes externas**: La plataforma puede interactuar con servicios y recursos en Google Cloud, Azure y AWS, ejecutando scripts o consumiendo APIs según las necesidades del negocio.

---

## Ventajas de la Arquitectura
- **Escalabilidad**: Uso de servicios serverless y desacoplados.
- **Seguridad**: Autenticación centralizada, reglas de acceso, protección perimetral y auditoría.
- **Flexibilidad**: Integración con múltiples nubes y servicios externos.
- **Experiencia de usuario**: Interfaz moderna, responsiva y alineada a la marca.
- **Automatización y control**: Flujos de aprobación, ejecución de scripts y registro de todas las operaciones.

---

## Notas adicionales
- El envío de correos electrónicos para notificaciones de aprobación está contemplado en la lógica de backend, pero el servicio específico de email se definirá en la etapa de implementación.
- El diseño y los módulos pueden evolucionar según las necesidades del negocio y feedback de los usuarios.

---
