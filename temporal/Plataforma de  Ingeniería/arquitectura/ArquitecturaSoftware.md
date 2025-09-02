# Arquitectura de Software - Plataforma de Ingeniería

Este documento describe la arquitectura de software profesional propuesta para la Plataforma de Ingeniería, diferenciando la estructura y patrones para el frontend (Angular) y el backend (Firebase Functions con Node.js), integrando los servicios clave de Firebase y Google Cloud.

---

## 1. Frontend: Angular (MVVM, Escalable y Modular)

### Patrón principal: MVVM (Model-View-ViewModel)
- **Model:** Interfaces y clases TypeScript que representan los datos de negocio (usuarios, permisos, ejecuciones, etc.).
- **View:** Componentes y templates HTML que definen la presentación visual y la interacción con el usuario.
- **ViewModel:** Componentes y servicios Angular que gestionan el estado, la lógica de presentación y la comunicación con el backend.

### Estructura de carpetas recomendada (Angular escalable)
```
/src
  /app
    /core         # Servicios singleton, guards, interceptors, configuración global
    /shared       # Componentes, pipes, directivas y utilidades reutilizables
    /features     # Módulos funcionales independientes (lazy loading)
      /usuarios
      /permisos
      /roles
      /flujos-aprobacion
      /scripts-shell
      /auditoria
      /dashboard
      /ayuda
    /layouts      # Componentes de layout (main, auth, error, etc.)
    /assets       # Imágenes, fuentes, estilos globales
    app-routing.module.ts
    app.module.ts
    app.component.ts
```

### Buenas prácticas y responsabilidades
- **Lazy loading** de módulos de features para optimizar el rendimiento.
- **Gestión de rutas y guards** para proteger vistas según roles y autenticación.
- **Servicios** para comunicación con APIs REST (Cloud Functions vía API Gateway).
- **Gestión de estado** local (RxJS, servicios) y posibilidad de usar NgRx para proyectos grandes.
- **Integración con Firebase Authentication** (Google Identity Platform) para login seguro y centralizado.
- **Uso de Bricks Design System y Angular Material** para UI consistente, accesible y alineada a la marca.
- **Internacionalización (i18n)** y buenas prácticas de accesibilidad (a11y).
- **Testing**: Unitario (Jest/Karma), integración y E2E (Cypress).

---

## 2. Backend: Firebase Functions (Node.js, Serverless, Integración Firebase)

### Patrón principal: Microservicios serverless
- Cada función implementa una responsabilidad específica (usuarios, permisos, ejecución de scripts, auditoría, etc.).
- Exposición de endpoints HTTP vía API Gateway.
- Integración nativa con Firestore, Storage y otros servicios de Firebase.
- Desacoplamiento y escalabilidad automática.

### Estructura de carpetas recomendada (Functions)
```
/functions
  /src
    /api           # Endpoints HTTP agrupados por dominio
      /usuarios
      /permisos
      /roles
      /flujos-aprobacion
      /scripts-shell
      /auditoria
    /services      # Lógica de negocio y acceso a datos
    /middlewares   # Autenticación, validación, logging
    /utils         # Utilidades y helpers
    index.ts       # Entry point
  package.json
  tsconfig.json
```

### Buenas prácticas y responsabilidades
- **Recepción de peticiones HTTP** desde el frontend (API RESTful, JSON).
- **Validación de autenticación y roles** (middleware, integración con Firebase Authentication y Cloud IAM).
- **Lógica de negocio** para cada módulo (alta, edición, consulta, ejecución, etc.).
- **Integración con Firestore y Cloud Storage** para persistencia de datos y archivos.
- **Ejecución de scripts y orquestación de flujos de aprobación**.
- **Auditoría y logging** de todas las operaciones relevantes (Cloud Logging).
- **Envío de notificaciones (email)** en flujos de aprobación (servicio a definir).
- **Testing**: Unitario (Jest), integración y pruebas de endpoints.

---

## 3. Integración y Servicios Firebase
- **Firebase Authentication**: Autenticación centralizada, integración con Google Identity Platform (OAuth 2.0, Google Workspace).
- **Firestore**: Base de datos NoSQL para usuarios, permisos, logs, auditoría, etc.
- **Cloud Storage**: Almacenamiento de archivos y documentos.
- **Firebase Functions**: Backend serverless, lógica de negocio y APIs.
- **Firebase Hosting**: Servir el frontend Angular de manera segura y escalable.
- **Reglas de seguridad**: Firestore y Storage, control de acceso granular.
- **API Gateway**: Centraliza y protege el acceso a las funciones, validando tokens de Firebase Authentication.

---

## 4. Comunicación, Seguridad y Despliegue
- **Comunicación Frontend-Backend**: API RESTful vía API Gateway, intercambio de datos en JSON.
- **Autenticación y autorización**: Basada en tokens JWT de Firebase Authentication, validación de roles y permisos en backend.
- **Despliegue desacoplado**: Frontend y backend pueden evolucionar y desplegarse de manera independiente.
- **Escalabilidad y resiliencia**: Backend serverless escala automáticamente según la demanda.
- **Monitoreo y auditoría**: Cloud Logging, métricas de uso, auditoría de acciones críticas.
- **CI/CD recomendado**: GitHub Actions, Cloud Build o similar para automatizar pruebas y despliegues.

---

## 5. Consideraciones adicionales
- **Mantenibilidad**: Separación clara de responsabilidades, modularidad, uso de buenas prácticas y documentación.
- **Seguridad**: HTTPS, validación de tokens, reglas de Firestore y Storage, Cloud IAM.
- **Internacionalización y accesibilidad**: Soporte multilenguaje y cumplimiento de estándares a11y.
- **Evolutividad**: Arquitectura preparada para añadir nuevos módulos y servicios en el futuro.

---

Esta arquitectura permite un desarrollo ágil, seguro, escalable y mantenible, alineado con las mejores prácticas para aplicaciones modernas en la nube y equipos profesionales. 