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

Por ejemplo:

- En **Home**, los usuarios pueden crear kits o combos de productos, generar alertas por bajo stock, gestionar proveedores, revisar el historial de movimientos y acceder a estadísticas claves como los productos más vendidos o el ticket promedio.

- El módulo de **Inventario** ofrece un entorno completo para registrar nuevos productos, gestionar precios, unidades, ubicaciones físicas (estanterías), etiquetas, notas internas, devoluciones y caducidades, así como personalizar columnas para facilitar la visualización.

- En **Configuración**, se pueden gestionar los roles de usuario (Administrador o Empleado), permisos según el plan activo, y actualizar perfiles a través de un asistente guiado.

La interfaz adapta su contenido según el tipo de usuario:

- **Administradores** tienen acceso completo a la configuración del sistema y la gestión general.

- **Empleados** acceden a funciones operativas esenciales, sin comprometer la seguridad ni integridad de la información.

La disposición lógica de las herramientas, acompañada de una navegación consistente, etiquetas claras y una estructura jerárquica coherente, garantiza que tanto nuevos usuarios como operadores frecuentes puedan comprender rápidamente el flujo de trabajo y realizar sus tareas con eficiencia.
#### 3.1.2.2. Labelling Systems
En StockWise ha sido diseñado para mejorar la organización, búsqueda, pagos y clasificación de productos dentro del inventario, facilitando la gestión y toma de decisiones por parte de los usuarios.

| Elemento de Navegación  | Descripción     |
|----------------------------|-----------------------|
| Sistema de Etiquetas         | Permite asignar múltiples etiquetas a productos para mejorar la organización, búsqueda y clasificación dentro del inventario.                   |
| Creación de Etiquetas        | Los usuarios pueden crear nuevas etiquetas o seleccionar etiquetas ya existentes mediante autocompletado en el formulario del producto.         |
| Visualización de Etiquetas   | Las etiquetas se muestran como chips de colores junto al nombre del producto, permitiendo una identificación rápida y visual.                   |
| Filtro por Etiquetas         | En la vista de inventario se puede filtrar por una o varias etiquetas, facilitando la segmentación de productos.                              |
| Permisos por Rol             | Administradores pueden crear/editar/eliminar etiquetas globales. Empleados pueden aplicar etiquetas existentes o proponer nuevas.              |
| Sugerencia de Etiquetas      | El sistema sugiere etiquetas ya existentes mientras se escriben nuevas, para evitar duplicados y mantener consistencia.                        |
| Accesibilidad y Estilo       | Las etiquetas tienen colores accesibles y tipografía legible, respetando la paleta y el diseño UI de StockWise.                                |
| Aplicación en Reportes       | Las etiquetas también pueden utilizarse como criterio para generar reportes filtrados de productos e inventario.                               |

#### 3.1.2.3. SEO Tags and Meta Tags
#### 3.1.2.4. Searching Systems
#### 3.1.2.5. Navigation Systems
### 3.1.3. Landing Page UI Design
#### 3.1.3.1. Landing Page Wireframe
#### 3.1.3.2. Landing Page Mock-up
### 3.1.4. Mobile Applications UX/UI Design
#### 3.1.4.1. Mobile Applications Wireframes
#### 3.1.4.2. Mobile Applications Wireflow Diagrams
#### 3.1.4.3. Mobile Applications Mock-ups
#### 3.1.4.4. Mobile Applications User Flow Diagrams
#### 3.1.4.5. Mobile Applications Prototyping
