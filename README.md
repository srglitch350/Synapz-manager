# Synapz - Sistema de Gestión de Permisos y Roles (RBAC)

![Estado](https://img.shields.io/badge/Estado-_En_Desarrollo-blue)
![Tipo](https://img.shields.io/badge/Tipo-RBAC_System-critical)
![Stack](https://img.shields.io/badge/Stack-MERN_Typescript-cyan)

##  Descripción

**Synapz** es un sistema completo de Control de Acceso Basado en Roles (RBAC - Role-Based Access Control) diseñado para gestionar permisos, políticas de acceso y roles de usuario en aplicaciones empresariales. Implementa un modelo de seguridad granular y escalable.

##  Problemática que Resuelve

Las empresas necesitan controlar quién puede:
- **Ver/Editar/Eliminar** recursos específicos
- **Acceder** a módulos particulares del sistema
- **Ejecutar** acciones críticas (ej: aprobaciones, pagos)
- **Administrar** otros usuarios y permisos

Synapz proporciona una solución flexible y auditable para estos requerimientos.

##  Características Principales

### **Núcleo RBAC**
- [ ] **Roles jerárquicos** (admin → manager → user)
- [ ] **Permisos granulares** (create, read, update, delete, approve)
- [ ] **Políticas de acceso** condicionales
- [ ] **Herencia de permisos** entre roles
- [ ] **Multi-tenancy** (soporte para múltiples organizaciones)

### **Seguridad y Auditoría**
- [ ] **Log de accesos** detallado
- [ ] **Doble verificación** para operaciones críticas
- [ ] **Expiración de permisos** temporales
- [ ] **Exportación de reports** de seguridad
- [ ] **API rate limiting** por rol

### **Gestión de Usuarios**
- [ ] **Invitation system** con enlaces únicos
- [ ] **Bulk operations** para gestión masiva
- [ ] **Perfiles personalizables** por usuario
- [ ] **Import/Export** de usuarios y permisos

### **Dashboard y Analytics**
- [ ] **Visualización de permisos** (mapa de calor)
- [ ] **Reportes de actividad** por usuario/rol
- [ ] **Alertas de seguridad** (permisos inusuales)
- [ ] **Sugerencias de optimización** de permisos

##  Arquitectura Técnica

### **Frontend (Admin Panel)**
- **React 18** + TypeScript + Vite
- **TanStack Table** para tablas de permisos
- **React Flow** para visualizar jerarquías
- **Tailwind CSS** + Shadcn/ui
- **Zod** para validación de formularios

### **Backend (API RBAC)**
- **Node.js** + Express + TypeScript
- **MongoDB** con referencias para relaciones
- **Redis** para cache de permisos (opcional)
- **JWT** con refresh tokens
- **Zod** para validación de esquemas

### **Modelo de Datos RBAC**
```typescript
// Estructura básica
User → Role → Permission → Resource
       ↑
  Role Hierarchy