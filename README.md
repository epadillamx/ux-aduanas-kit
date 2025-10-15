# Sistema de Fiscalización - MINIMIS

Sistema web para la gestión y fiscalización de operaciones de Courier, desarrollado con el Framework de Gobierno Digital de Chile.

## Descripción

Sistema de fiscalización que permite la gestión y control de listas de carga de Courier, incluyendo la búsqueda, selección y administración de manifiestos y guías.

## Tecnologías Utilizadas

- **Framework:** [Gobierno Digital Chile](https://framework.digital.gob.cl/) v3.0.10
- **CSS Framework:** Bootstrap 4 (incluido en @gobdigital-cl/gob.cl)
- **JavaScript:** Vanilla JS + jQuery
- **Tipografías:** Roboto y Roboto Slab

## Requisitos Previos

- Node.js (versión 14 o superior)
- npm (versión 6 o superior)
- Navegador web moderno (Chrome, Firefox, Edge)

## Instalación

1. Clonar el repositorio:
```bash
git clone <url-del-repositorio>
cd fiscalizacion
```

2. Instalar dependencias:
```bash
npm install
```

3. Las dependencias instaladas incluyen:
   - `@gobdigital-cl/gob.cl@^3.0.10` - Framework oficial del Gobierno de Chile
   - jQuery (como dependencia del framework)

## Estructura del Proyecto

```
fiscalizacion/
├── node_modules/           # Dependencias del proyecto
├── login.html             # Página de inicio de sesión
├── courier.html           # Vista principal del sistema Courier
├── package.json           # Configuración del proyecto
└── README.md             # Este archivo
```

## Archivos Principales

### login.html
Página de autenticación con:
- Validación de RUT chileno
- Formato automático de RUT
- Validación de contraseña
- Diseño responsive con Framework GobCL

### courier.html
Vista principal del sistema con:
- Sidebar de navegación
- Formulario de búsqueda con múltiples filtros
- Tabla de resultados de listas de carga
- Funcionalidades de selección y modificación
- Pestañas de navegación (Seleccionar, Registro de Resultados, Resumen)

## Scripts Disponibles

```bash
# Iniciar servidor de desarrollo con caché deshabilitado
npm run dev
```

## Uso del Sistema

### 1. Inicio de Sesión

1. Abrir `login.html` en el navegador
2. Ingresar RUT válido (formato: 12.345.678-9)
3. Ingresar contraseña (mínimo 6 caracteres)
4. El sistema valida el RUT con dígito verificador

### 2. Vista Courier

**Filtros de Búsqueda:**
- Número Manifiesto
- Guía Courier
- Tipo de Courier (Normal/Expreso)
- Emisor
- Rango de fechas de emisión
- Estado (Pendientes/Procesados/Todos)

**Funcionalidades:**
- Búsqueda de listas de carga
- Selección de registros
- Modificación de marcas
- Visualización de datos detallados

**Columnas de la Tabla:**
- Manifiesto
- Tipo
- Nro. Master/MIC
- Nro. Vuelo/Patente
- Compañía Courier
- Peso Bruto
- Valor Total
- Guías (Total, Seleccionadas, $2500 USD)
- Estado (Revisado/Conformado)
- Fechas (Aceptación/Impresión)

## Documentación del Framework

### Framework de Gobierno Digital Chile
- **Documentación UX:** https://framework.digital.gob.cl/
- **Kit Digital:** https://kitdigital.gob.cl/
- **Paquete NPM:** [@gobdigital-cl/gob.cl](https://www.npmjs.com/package/@gobdigital-cl/gob.cl)

### Recursos del Framework

**CSS Principal:**
```html
<link rel="stylesheet" href="node_modules/@gobdigital-cl/gob.cl/dist/css/gob.cl.css">
```

**JavaScript:**
```html
<script src="node_modules/@gobdigital-cl/gob.cl/dist/js/gob.cl.js"></script>
```

**Tipografías:**
```html
<link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700&family=Roboto+Slab:wght@400;700&display=swap" rel="stylesheet">
```

## Características del Framework GobCL

- Basado en Bootstrap 4
- Componentes prediseñados para sitios gubernamentales
- Diseño responsive y accesible
- Cumple con estándares de gobierno digital
- Paleta de colores oficial del Gobierno de Chile
- Componentes de formularios, tablas, navegación, etc.

## Paleta de Colores Oficial

- **Azul Primario:** `#0f69b4`
- **Azul Oscuro:** `#003d82`
- **Azul Medio:** `#0056a3`
- **Azul Claro:** `#b8d4f1`
- **Fondo:** `#f5f5f5`

## Navegadores Soportados

- Chrome (última versión)
- Firefox (última versión)
- Safari (última versión)
- Edge (última versión)

## Desarrollo

### Agregar Nuevas Vistas

1. Crear nuevo archivo HTML
2. Incluir los estilos y scripts del framework
3. Seguir la estructura de `courier.html` como plantilla
4. Mantener consistencia con el diseño gubernamental

### Buenas Prácticas

- Usar componentes del Framework GobCL
- Mantener accesibilidad (atributos ARIA)
- Validar datos del lado del cliente
- Seguir nomenclatura en español para el contexto gubernamental
- Documentar cambios significativos

## Integración con Backend

El sistema está preparado para integrarse con un backend. Los puntos de integración están identificados en los archivos JavaScript:

```javascript
// En login.html
// Aquí iría la lógica de autenticación
console.log('Login exitoso:', { rut, remember });

// En courier.html
// Aquí iría la lógica de búsqueda en el backend
function buscarListasCarga() { ... }
```

## Seguridad

- Validación de RUT con algoritmo de dígito verificador
- Validación de formularios del lado del cliente
- Preparado para integración con sistema de autenticación seguro
- No almacena credenciales en el frontend

## Próximas Funcionalidades

- [ ] Integración con API backend
- [ ] Sistema de autenticación real
- [ ] Exportación de datos a Excel/PDF
- [ ] Filtros avanzados de búsqueda
- [ ] Historial de modificaciones
- [ ] Dashboard con estadísticas
- [ ] Gestión de permisos de usuario

## Soporte y Contacto

Para dudas sobre el Framework de Gobierno Digital:
- Sitio oficial: https://framework.digital.gob.cl/
- Kit Digital: https://kitdigital.gob.cl/

## Licencia

ISC

## Autor

ARKHO - MINIMIS

---

**Última actualización:** Octubre 2025
