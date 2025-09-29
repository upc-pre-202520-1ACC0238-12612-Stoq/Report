# Capítulo III: Solution UI/UX Design
## 3.1. Product design
### 3.1.1. Style Guidelines
Un "style guideline" o guía de estilo es un conjunto de reglas y pautas que establecen la forma en que se deben escribir, diseñar o presentar documentos, contenido web, software, o cualquier otro tipo de trabajo creativo. A continuación, se otorga especificación a los parámetros implementados en la estructura del proyecto:

#### 3.1.1.1. General Style Guidelines
**Branding**

StockWise es una marca pensada para ofrecer confianza, cercanía y eficiencia a pequeñas y medianas empresas, especialmente bodegas de barrio y emprendimientos. El branding refleja accesibilidad, modernidad y calidez. El enfoque está en facilitar la transformación digital de la gestión de inventarios con una interfaz clara, amigable y funcional.

**Logotipo**

El logo combina una bodega estilizada con colores cálidos y un código de barras, representando tanto la esencia física del negocio como la modernización a través de tecnología.

- La palabra "Stock" en rojo (#BC162A) resalta la acción y lo esencial del inventario.
- La palabra "Wise" en marrón oscuro (#302325) sugiere inteligencia y fiabilidad.

El código de barras integrado representa la gestión estructurada y la automatización del stock.

<center> <img src="assets/Chapter-3/logo.png" style="width: 250px;"/> </center>
<br>

**Tono de comunicación** 

Nos comunicamos como lo haría un buen amigo del barrio, claro, sin complicaciones, y con buena onda.  Queremos transmitir una sensación de seguridad y eficiencia, mientras mantenemos una comunicación cercana y amigable.

**Lenguaje (Language):**

Usamos términos fáciles de entender: “productos”, “alertas”, “entradas/salidas”, “usuarios”. Evitamos jerga técnica innecesaria o anglicismos si no son esenciales.

**Colores**

La paleta de colores de StockWise ha sido cuidadosamente seleccionada para transmitir profesionalismo, confianza y accesibilidad.

**Primary Colors:**
- #BC162A (Rojo intenso): Botones principales, acciones críticas, alertas importantes
- #EE7F27 (Naranja vibrante): Botones secundarios, estados activos, notificaciones
- #302325 (Marrón oscuro): Texto principal, headers, elementos de navegación

**Background Colors:**
- #F5E1A4 (Fondo cálido claro): Fondo general de la aplicación
- #D9D593 (Gris suave): Fondos de secciones, cards secundarios

**Functional Colors:**
- #27A300 (Verde éxito): Confirmaciones, estados positivos
- #FFC107 (Amarillo advertencia): Alertas moderadas, advertencias
- #DC3545 (Rojo error): Estados de error, acciones destructivas

<center> <img src="assets/Chapter-3/color.jpeg" style="width: 250px;"/> </center>
<br>

**Tipografía**

La elección tipográfica para StockWise es un componente esencial que complementa la identidad visual de la marca. Se han seleccionado dos familias tipográficas que juntas ofrecen versatilidad y coherencia, asegurando que la comunicación sea clara y efectiva en todos los medios.

**Font Families:**
- Inter: Para textos largos, body copy y contenido principal
- Nunito: Para headers, botones y elementos de interfaz

**Font Scale (Mobile First):**
- h1: 24px / 1.1 / Bold
- h2: 20px / 1.1 / SemiBold
- h3: 18px / 1.2 / Medium
- Body Large: 17px / 1.4 / Regular
- Body: 16px / 1.4 / Regular
- Small: 14px / 1.4 / Regular
- Caption: 12px / 1.3 / Regular

**Weights:**
- Bold (700): Títulos principales, acciones críticas
- SemiBold (600): Subtítulos, botones importantes
- Medium (500): Etiquetas, elementos interactivos
- Regular (400): Texto body, contenido principal
- Light (300): Texto secundario, descripciones

**Border Radius:**
- Small: 8px (botones pequeños, inputs)
- Medium: 12px (cards, modales)
- Large: 16px (containers principales)

**Spacing System (8px base):**
- xs: 4px
- sm: 8px
- md: 16px
- lg: 24px
- xl: 32px
- xxl: 48px

**Shadows:**
- Low: 0 2px 4px rgba(48, 35, 37, 0.1)
- Medium: 0 4px 8px rgba(48, 35, 37, 0.15)
- High: 0 8px 16px rgba(48, 35, 37, 0.2)

### 3.1.2. Information Architecture
La arquitectura de la información, también conocida como Information Architecture (IA), implica la organización de la información de manera clara y lógica, de modo que los usuarios puedan comprender su ubicación, lo que han descubierto, qué pueden esperar y qué está disponible a su alrededor. Esto tiene como objetivo permitir a los usuarios encontrar con facilidad lo que están buscando, y a los clientes, comprender las capacidades de la plataforma. Además, la arquitectura de la información posibilita la incorporación de nuevas funciones y la expansión del producto sin generar una estructura compleja o de difícil comprensión (Rosenfeld, Morville & Arango 2015).
#### 3.1.2.1. Organization Systems
La interfaz se divide en módulos bien definidos, accesibles desde un panel de navegación estructurado jerárquicamente. Estos módulos incluyen: Inicio, Home, Inventario y Configuración. Cada sección agrupa funciones específicas según su propósito, permitiendo que las tareas clave estén siempre al alcance del usuario.

# 3.1.2.1. Organization Systems

La arquitectura de organización de StockWise está diseñada siguiendo principios de agrupación lógica y progresiva de la información, permitiendo a los usuarios acceder rápidamente a las funciones necesarias según su rol y contexto de uso.

**Estructura Organizacional Principal**

| Módulo | Descripción | Funciones Principales | Acceso por Rol |
|--------|-------------|---------------------|----------------|
| **Dashboard Principal** | Vista consolidada del estado del inventario y métricas clave | - Resumen ejecutivo de stock<br>- Alertas prioritarias<br>- Acciones rápidas<br>- Métricas en tiempo real | Admin, Encargado |
| **Gestión de Inventario** | Núcleo operativo para administración completa de productos | - Registro y edición de productos<br>- Control de niveles de stock<br>- Categorización y etiquetado<br>- Gestión de ubicaciones físicas | Admin, Encargado, Empleado |
| **Operaciones Diarias** | Módulo para transacciones y movimientos regulares | - Registro de entradas/salidas<br>- Ajustes de inventario<br>- Historial de movimientos<br>- Devoluciones y mermas | Admin, Encargado, Empleado |
| **Reportes y Analytics** | Sistema de generación y visualización de datos | - Reportes personalizados<br>- Análisis de tendencias<br>- Métricas de rendimiento<br>- Exportación de datos | Admin, Encargado |
| **Configuración del Sistema** | Administración de preferencias y usuarios | - Gestión de perfiles de usuario<br>- Configuración de empresa<br>- Preferencias de notificaciones<br>- Backup y seguridad | Admin |

**Principios de Organización Aplicados**

1. **Agrupación por Funcionalidad**
Las características se organizan según su propósito común, facilitando la asociación mental y reduciendo la carga cognitiva.

1. **Jerarquía Visual Progresiva**
La información se presenta desde lo general hacia lo específico, permitiendo drill-down controlado según las necesidades del usuario.

1. **Contextualización Dinámica**
Las opciones disponibles se adaptan según el rol del usuario y el módulo activo, mostrando solo las funciones relevantes.

1. **Consistencia Transversal**
Mismos patrones organizativos se aplican en todos los módulos, creando una experiencia unificada y predecible.

**Organización de Contenido por Módulo**

**Módulo de Inventario**
- **Agrupación Primaria:** Por estado de stock (Normal, Bajo, Crítico)
- **Agrupación Secundaria:** Por categorías de producto
- **Agrupación Terciaria:** Por ubicación física en bodega

**Módulo de Reportes**
- **Agrupación Temporal:** Diario, Semanal, Mensual
- **Agrupación por Métrica:** Ventas, Stock, Rentabilidad
- **Agrupación por Producto:** Individual, Por categoría, Global

#### 3.1.2.2. Labelling Systems
El sistema de etiquetado en StockWise sigue principios de claridad, consistencia y contexto, asegurando que los usuarios comprendan inmediatamente la función de cada elemento.

**Principios de Etiquetado:**

- Lenguaje Natural: Usamos términos del dominio del usuario ("productos", "proveedores", "ventas")
- Consistencia: Mismo término para misma función en toda la aplicación
- Jerarquía Visual: Tamaño y peso tipográfico reflejan importancia
- Contexto: Las etiquetas cambian según el módulo y las acciones disponibles

**Sistema de Iconografía:**

- **Acciones Principales:**
  - ➕ Agregar/Registrar
  - ✏️ Editar/Modificar
  - 🗑️ Eliminar/Descartar
  - 🔍 Buscar/Filtrar
  - 📤 Exportar/Compartir

- **Módulos y Secciones:**
  - 📊 Dashboard - Vista general
  - 📦 Inventario - Gestión de productos
  - 🔄 Movimientos - Entradas y salidas
  - 📈 Reportes - Analytics y métricas
  - ⚙️ Configuración - Ajustes del sistema

- **Estados del Sistema:**
  - ✅ Completado/Éxito
  - ⚠️ Advertencia/Alerta
  - ❌ Error/Problema
  - 🔄 Procesando/En curso

**Microcopy y Mensajes:**

- **Botones de Acción:** "Agregar Producto", "Registrar Entrada", "Generar Reporte"
- **Mensajes de Confirmación:** "¿Estás seguro de eliminar este producto?"
- **Estados Vacíos:** "Aún no tienes productos registrados"
- **Guías Contextuales:** "Usa el código de barras para buscar más rápido"

#### 3.1.2.3. SEO Tags and Meta Tags
**SEO Tags**

SEO (Search Engine Optimization) Tags son elementos de HTML que ayudan a los motores de búsqueda a entender el contenido y la estructura de una página web. Estos tags influyen en cómo los motores de búsqueda indexan y clasifican tu sitio en los resultados de búsqueda. 

**Algunos ejemplos importantes de SEO Tags  para StockWise:**

**Title Tags para Páginas Principales:**

``` html
<!-- Página de Inicio -->
<title>StockWise - App de Gestión de Inventarios para PYMES</title>

<!-- Página de Características -->
<title>Gestión de Inventario Móvil | StockWise App</title>

<!-- Página de Precios -->
<title>Planes de Gestión de Inventario | StockWise</title>
```

**Header Tags Estructurados:**
``` html
<h1>Gestiona Tu Inventario desde tu Móvil</h1>
<h2>La solución simple para negocios en crecimiento</h2>
<h3>Control total de tu stock en tiempo real</h3>
```

**Meta Descriptions Optimizadas:**
``` html
<meta name="description" content="StockWise - App móvil de gestión de inventarios para PYMES. Controla stock, genera reportes y evita quiebres de inventario desde tu teléfono.">

<meta name="keywords" content="gestión inventarios, app móvil, control stock, PYMES, bodegas, emprendedores">
``` 
**Open Graph Tags para Redes Sociales:**
``` html
<meta property="og:title" content="StockWise - App de Inventarios">
<meta property="og:description" content="Gestiona tu inventario desde cualquier lugar con StockWise">
<meta property="og:image" content="/images/stockwise-social-preview.png">
``` 

#### 3.1.2.4. Searching Systems
El sistema de búsqueda de StockWise está diseñado para ser intuitivo y potente, permitiendo a los usuarios encontrar rápidamente la información que necesitan en su inventario.

**Características del Sistema de Búsqueda:**

- **Búsqueda Inteligente:**
  - Búsqueda por texto libre en múltiples campos (nombre, - código, categoría, proveedor)
  - Búsqueda por código de barras usando la cámara del dispositivo
  - Búsqueda por voz para hands-free operation
  - Búsqueda predictiva con sugerencias en tiempo real
- **Resultados de Búsqueda:**
  - Ordenamiento por relevancia, nombre, stock, fecha
  - Vista de tarjetas con información esencial
  - Acciones rápidas desde los resultados
  - Historial de búsquedas recientes
- **Búsqueda por Lotes:**
  - Escaneo múltiple de códigos de barras
  - Reconocimiento de imágenes para productos sin código
  - Procesamiento offline con sincronización posterior

#### 3.1.2.5. Navigation Systems
El sistema de navegación de StockWise está optimizado para dispositivos móviles, priorizando la accesibilidad y la eficiencia en las tareas diarias.

**Patrones de Navegación Principal:**

**Bottom Navigation Bar:**
``` text
[🏠 Inicio]  [📦 Inventario]  [➕ Agregar]  [📊 Reportes]  [👤 Perfil]
``` 
**Navegación por Gestos:**

- Deslizar hacia la derecha: Menú lateral
- Deslizar hacia abajo: Actualizar contenido
- Deslizar hacia arriba: Acciones rápidas
- Toque largo: Opciones contextuales

**Navegación Contextual:**

- Breadcrumbs para ubicación en estructuras profundas
- Botón "Atras" nativo del dispositivo
- Navegación por pestañas en secciones complejas
- Accesos directos personalizables según uso frecuente

**Navegación para Accesibilidad:**

- Soporte completo para lectores de pantalla
- Navegación por teclado en versiones tablet
- Tamaños de touch target mínimos de 44px
- Alto contraste y modos de daltonismo

### 3.1.3. Landing Page UI Design
#### 3.1.3.1. Landing Page Wireframe
El prototipado de la landing page cuenta diversas secciones:

- Header: Incluye botones para facilitar la navegación
- Hero Section: Con un botón CTA principal, un título y una imagen.
- Sección de Beneficios / Características: mostrara un resumen de 3 beneficios que ofrece la app
- Planes / Precios: Trendra 2 planes con su referente título y lista de características y contara con un botón CTA secundario por cada plan.
- Testimonios: Consta de un título y subtítulo, así como de unos testimonios de usuarios de cada segmento, lo que aumenta la confianza en los potenciales clientes.
- Llamado a la acción final (CTA grande) : Tiene un título y subtítulo, un boton CTA grande para "Try our app"
- Footer: Sección que da fin a la landing page, cuenta con las redes sociales de la plataforma.

**Wireframe Desktop**
<center> <img src="assets/Chapter-3/Wireframe-Desktop.png" style="width: 420px;"/> </center>
<br>

*Imagen (N°). Elaboración propia. Realizado en Figma*

**Wireframe Mobile**

En la versión mobile el navbar se reemplaza por un menu desplegable.

<center> <img src="assets/Chapter-3/Wireframe - Mobile.png" style="width: 420px;"/> </center>
<br>

*Imagen (N°). Elaboración propia. Realizado en Figma*
#### 3.1.3.2. Landing Page Mock-up
### 3.1.4. Mobile Applications UX/UI Design
#### 3.1.4.1. Mobile Applications Wireframes
#### 3.1.4.2. Mobile Applications Wireflow Diagrams
#### 3.1.4.3. Mobile Applications Mock-ups
#### 3.1.4.4. Mobile Applications User Flow Diagrams
#### 3.1.4.5. Mobile Applications Prototyping
