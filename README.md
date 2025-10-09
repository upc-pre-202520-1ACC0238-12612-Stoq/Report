# Capítulo IV: Product Implementation & Validation
En este apartado se resume todo el contenido recopilado, examinando los procedimientos a seguir y evaluando el estado emocional.
## 4. Product Implementation & Validation
### 4.1. Software Configuration Management
En la siguiente sección se detalla la ruta de acceso de cada uno de los productos de software, facilitando a cualquier miembro del equipo el desarrollo de cada aspecto del trabajo:
#### 4.1.1. Software Development Environment Configuration
* **Android Studio:** Entorno de desarrollo.\
![image](https://upload.wikimedia.org/wikipedia/commons/c/c1/Android_Studio_icon_%282023%29.svg)
* **GitHub:** Repositorio colaborativo en la nube.\
![image](https://cdn-1.webcatalog.io/catalog/github/github-icon-filled-256.png?v=1744774208192)
* **Netifly:** Plataforma que facilita implementar despliegues sencillos para nuestras páginas web.\
![image](https://cmscritic.com/ms-content/uploads/2023/11/netlifty-icon.png?format=auto&width=256)
* **Vertabelo:** Plataforma colaborativa para la creación de diagramas de base de datos.\
![image](https://hackmd.io/_uploads/r1BjjyQgC.png)
* **Visual Studio Code:** Entorno de desarrollo para diseño de base de datos.\
![image](https://hackmd.io/_uploads/Hy8d2y7lR.png)
* **Figma:** Herramienta colaborativa que permite elaborar wireframes y mockups.\
![image](https://hackmd.io/_uploads/BJ99okXeR.png)

#### 4.1.2. Source Code Management
**Repositorio de la Landing Page:** 

**Implementación de GitFlow:**

Para nuestra estrategia de gestión de versiones con Git, nos hemos inspirado en el artículo "A successful Git branching model" de Vincent Driessen, adoptando el modelo de ramificación GitFlow. Este enfoque nos permite establecer claramente las convenciones de ramificación que aplicamos en nuestro proyecto.

![image](https://hackmd.io/_uploads/rJt95BobA.png)
* **Rama Principal (Main branch):** Contiene el código en producción y se conoce como la Master branch o Main branch.
    * Notación: main
* **Rama de Desarrollo (Develop branch):** Acumula las últimas actualizaciones y cambios para la próxima versión. Funciona como un entorno de integración y prueba continua.
    * Notación: develop
* **Rama de Lanzamiento (Release branch):** Facilita la preparación de una nueva versión del producto, permitiendo correcciones de errores y recibiendo más actualizaciones de Develop.
    * Debe derivarse de: develop
    * Debe fusionarse con: develop y master/main
    * Notación: release
* **Rama de Características (Feature branch):** Se utiliza para desarrollar nuevas funcionalidades para la siguiente versión o futuras iteraciones.
    * Debe derivarse de: develop
    * Debe fusionarse de vuelta a: develop
    * Notación: feature
* **Rama de Corrección Rápida (Hotfix branch):** Aborda errores críticos en producción, permitiendo la implementación rápida de soluciones.
    * Debe derivarse de: master/main
    * Debe fusionarse con: develop y master/main
    * Notación: hotfix

**Conventional Commits:** 
Adoptamos esta metodología para estructurar los mensajes de confirmación de cambios de manera estándar y semántica, lo que facilita la comunicación y la automatización de registros de cambios.

**Tipos de Commits Convencionales:**
* feat: Nuevas características o funcionalidades.
* fix: Correcciones de errores.
* docs: Cambios o mejoras en la documentación.
* style: Cambios de formato que no afectan la funcionalidad.
* refactor: Mejoras en la estructura o legibilidad del código.
* test: Adición o modificación de pruebas.
* chore: Cambios en el proceso de construcción o tareas de mantenimiento.
* perf: Mejoras de rendimiento en el código.

#### 4.1.3. Source Code Style Guide & Conventions
### HTML

| Regla                                   | Ejemplo / Explicación                                                   |
|----------------------------------------|--------------------------------------------------------------------------|
| Etiquetas y atributos en minúsculas    | `<div class="container">`, `<img src="logo.png" alt="Logo">`           |
| Atributos ordenados lógicamente        | `class`, `id`, `name`, `type`, `value`, etc.                           |
| Uso de comillas dobles                 | `<input type="text" name="username">`                                  |
| Indentación consistente (2 o 4 espacios) | No mezclar espacios con tabs                                            |

---

### CSS

| Regla                                   | Ejemplo / Explicación                                                   |
|----------------------------------------|--------------------------------------------------------------------------|
| Nombres de clases en `kebab-case`      | `.main-header`, `.user-profile-card`                                   |
| Propiedades en minúsculas y ordenadas  | `color: #333; font-size: 16px; margin-top: 20px;`                       |
| Uso de comentarios                     | `/* Sección de estilos para el header */`                              |
| Indentación consistente                | 2 o 4 espacios, no usar tabs                                            |

---

### JavaScript

| Regla                                       | Ejemplo / Explicación                                                   |
|--------------------------------------------|--------------------------------------------------------------------------|
| Variables y funciones en `camelCase`       | `let userName = "Juan";`, `function getUserData() {}`                  |
| Clases en `PascalCase`                     | `class UserProfile {}`                                                 |
| Constantes en `UPPER_SNAKE_CASE`           | `const API_URL = "https://api.example.com";`                           |
| Uso de `const` y `let`                     | Evitar `var`, usar `const` por defecto y `let` si se necesita mutabilidad |
| Punto y coma al final de líneas            | `let nombre = "Carlos";`                                               |
| Indentación consistente (2 o 4 espacios)   | Mantener el mismo estilo en todo el proyecto                           |

---

### Kotlin

| Regla                                         | Ejemplo / Explicación                                                   |
|----------------------------------------------|--------------------------------------------------------------------------|
| Variables y funciones en `camelCase`         | `val userName = "Juan"`, `fun getUserData() {}`                         |
| Clases y objetos en `PascalCase`             | `class UserProfile`, `object AppConfig`                                 |
| Constantes en `UPPER_SNAKE_CASE`             | `const val MAX_USERS = 100`                                             |
| Archivos nombrados igual que la clase        | `UserProfile.kt`                                                        |
| Indentación con 4 espacios                   | No usar tabs                                                            |
| Uso de `val` por defecto, `var` si mutable   | Promueve inmutabilidad                                                  |
| Expresiones lambda con `it`   | `users.filter { it.isActive }` |

#### 4.1.4. Software Deployment Configuration
**Deployment Landing Page:** 

En esta sección, detallamos el proceso de implementación de nuestra landing page en la plataforma de GitHub.

1. Se crea un repositorio en GitHub para alojar el código de nuestra landing page.

![image](https://imgur.com/4J7UJO8.png)

2. Agregamos a los participantes:

![image](https://imgur.com/BZ8WX95.png)

1. Habilitamos Netlifly para poder importar nuestro proyecto:

![image](https://imgur.com/KcnDArx.png)


4. Finalmente, se confirma el despliegue de nuestra página web después de completar todo el procedimiento.

![image](https://imgur.com/FAx39hz.png)

Este proceso garantiza el despliegue satisfactorio de nuestra landing page en la plataforma de Netlifly, siguiendo las especificaciones y requisitos de nuestro proyecto.

**Enlace de la Landing Page: https://stockwiselanding.netlify.app/**
<br>
**About the product: https://youtu.be/gKQCMO4rORw?si=j6qLgCYkp8SHd2Py**
<br>
**Deployment Backend:**
En esta sección, detallamos el proceso de implementación de nuestro backend en la plataforma de

### 4.2. Landing Page & Mobile Application Implementation
#### 4.2.1. Sprint 1
Este informe documenta el progreso realizado durante la fase de definición de requisitos del proyecto, que incluye entrevistas con los interesados y creación de artefactos antes y después de la implementación de la aplicación mobile. Proporcionar una visión clara del avance y garantizar una comunicación efectiva entre el equipo de desarrollo y los interesados son los objetivos principales.

Durante esta etapa, se realizaron extensas entrevistas con los interesados para comprender sus necesidades, expectativas y requisitos particulares para la aplicación. Las entrevistas proporcionaron información útil que ayudó a definir los requisitos del proyecto.

Se realizaron actividades de creación de artefactos antes y después de la implementación de la aplicación mobile, además de entrevistas. Estos objetos fueron:
##### 4.2.1.1. Sprint Planning 1
| Sprint # | Sprint 1  | 
|--------------------|------------|
| Sprint Planning Background | 
| Date | 2025-10-8 | 
| Time |  22:23 PM |
| Location |  UPC - Monterrico |
| Preparate by| Camila Sanchez Rios | 
|  Attendees (to planning meeting) | Jocelyn Almerco, Kevin Chi, Alejandro Oroncoy, Jeremy Paucar | 
| Sprint n-1 Review Summary | En resumen se desarrollaron avances en la landing page, backend y frontend mobile | 
| Sprint Planning Background | Durante esta etapa, se llevó a cabo una exhaustiva verificación de la funcionalidad de la landing page diseñada para el proyecto. El objetivo principal fue asegurar que la landing page cumpla con los estándares de calidad y proporcionar una experiencia óptima para los visitantes. Asimismo, se realizó la primera implementación de la aplicación mobil y el despliegue del backend |
| Sprint Goal & User Stories | 
| Sprint 1 Goal | Desarrolar la funcionalidad de la página web con i18n e implementar el backend. Se considerará que el objetivo del sprint se ha cumplido si todas las historias de usuario relacionadas con la landing page están implementadas y si todas las historias de usuario relacionadas con la implementación de APIs para la gestión de una entidad están completadas en un 80%. |  
| Sprint Velocity | Se establece un Velocity de 24 Story Points para este Sprint. | 
| Sum of Story Points | 24 Story Points | 

##### 4.2.1.2. Sprint Backlog 1

##### 4.2.1.3. Development Evidence for Sprint Review
Durante este sprint, se han realizado avances significativos en la implementación de la Landing Page, backend y frontend del aplicativo mobile. Se han completado varias historias de usuario tanto de la landing page como del backend y se han realizado múltiples commits en los repositorios correspondientes.

<table>
   <tr>
      <td>Repository</td>
      <td>Branch</td>
      <td>Component</td>
      <td>Commit Id</td>
      <td>Commit Message</td>
      <td>Commited on (Date)</td>
   </tr>
   <tr>
      <td>https://github.com/upc-pre-202520-1ACC0238-12612-Stoq/Web-Services</td>
      <td>Development</td>
      <td>Backend</td>
      <td>xxx</td>
      <td>xxxtd>
      <td>Mes Dia, 2025</td>
   </tr>
   <tr>
      <td>https://github.com/upc-pre-202520-1ACC0238-12612-Stoq/Landing-Page</td>
      <td>Develop</td>
      <td>Landing Page</td>
      <td>27811d1b1f7fae66c103cf20dd69dde3615c416b</td>
      <td>initialize React application with Vite</td>
      <td>Octubre 2, 2025</td>
   </tr>
   <tr>
      <td>https://github.com/upc-pre-202520-1ACC0238-12612-Stoq/Native-mobile-development</td>
      <td>Development</td>
      <td>Mobile Frontend</td>
      <td>xxx</td>
      <td>xxx</td>
      <td>Ocrubre 9, 2025</td>
   </tr>
</table>

##### 4.2.1.4. Testing Suite Evidence for Sprint Review
##### 4.2.1.5. Execution Evidence for Sprint Review
Durante este Sprint, se han alcanzado varios hitos importantes en la implementación de la Landing Page. Además se realizaron avances en el frontend de la aplicaciones mobile. Se han completado las siguientes tareas:

- Implementación de la sección Beneficios
- Visualización de funcionalidades.
- Visualización de planes disponibles.
- Implementacion de la Internacionalizacion

### Screenshots

#### Landing Page
![Landing Page](https://imgur.com/FAx39hz.png)

#### Funciones claves
![Características](https://imgur.com/UWonPsf.png)

#### Sección de Planes Disponibles
![Planes Disponibles](https://imgur.com/xjaqRsc.png)

### Seccion de cambio de idioma

![I18n](https://imgur.com/8Bs1Hul.png)

#### Mobile Frontend

![Dashboard](xxx)

##### 4.2.1.6. Services Documentation Evidence for Sprint Review

[Falta]

##### 4.2.1.7. Software Deployment Evidence for Sprint Review

##### Landing Page

Para el despliegue de la landing page se realizaron los siguientes pasos:

#### 1. Preparación del proyecto
Se organizó el proyecto con todos los archivos necesarios del sitio web:
- Archivos HTML, CSS, JavaScript e imágenes
- Estructura de carpetas clara (`/css`, `/js`, `/images`, etc.)

#### 2. Creación de cuenta o acceso a Netlify
Se accedió a [https://www.netlify.com](https://www.netlify.com) para iniciar sesión o crear una cuenta, vinculándola con un proveedor de repositorios como GitHub, GitLab o Bitbucket.

#### 3. Nuevo sitio desde Git
Se eligió la opción **"Add new site" > "Import an existing project"** para conectar el repositorio del proyecto de la landing page.

#### 4. Autorización y selección del repositorio
Se autorizó a Netlify a acceder al repositorio y se seleccionó el repositorio correspondiente al proyecto.

#### 5. Configuración del despliegue
Durante la configuración:
- Se indicó la rama que contiene el código (por ejemplo, `main`)
- Se dejó vacío el campo de build si el proyecto no requiere compilación
- Se indicó el directorio de publicación (por ejemplo, `/` si los archivos están en la raíz)

#### 6. Despliegue automático
Se lanzó el primer despliegue, y Netlify generó automáticamente una URL pública para acceder al sitio.

#### 7. Personalización de dominio (opcional)
Se puede añadir un dominio personalizado desde la sección de configuración de dominio. Netlify gestiona automáticamente el certificado SSL (HTTPS).

#### 8. Actualizaciones automáticas
Cada vez que se realice un push a la rama seleccionada, Netlify desplegará automáticamente los nuevos cambios.

#### 9. Monitoreo del sitio
Desde el panel de control de Netlify es posible:
- Consultar el historial de despliegues
- Ver errores si los hay
- Configurar variables de entorno
- Ver estadísticas básicas del sitio

![Netlify](https://imgur.com/8rSU9Xp.png)

##### Backend

Para el despliegue del backend se realizaron los siguientes pasos:

##### 4.2.1.8. Team Collaboration Insights during Sprint

En esta sección se proporcionan los insights para el sprint 1.

**Documentation**

En esta sección, el equipo destacó la importancia de mantener una documentación clara y actualizada que facilite la colaboración y el entendimiento común. Se identificó que una buena documentación agiliza la resolución de dudas y mejora la calidad del desarrollo. 

A continuación se muestran los insights del equipo para la sección correspondiente:

![Doc](vvv.png)

**Landing Page** 

El equipo observó que la landing page funciona como la primera ventana de contacto con el usuario, por lo que es vital que sea atractiva y fácil de navegar. Se resaltó la necesidad de optimizar los textos y elementos visuales para maximizar la conversión y el enganche inicial. 

A continuación se muestran los insights del equipo para la sección correspondiente:

[![Landing](https://imgur.com/0sc9mos.png)](https://imgur.com/0sc9mos.png)

**Backend**

En equipo analizamos que la arquitectura del backend debía ser robusta y escalable para soportar las futuras demandas. Identificamos retos en la gestión de datos y seguridad, lo que motivó la implementación de buenas prácticas para garantizar la integridad y eficiencia. 

A continuación se muestran los insights del equipo para la sección correspondiente:

[![Back](vv.png)](d)


**Mobile Frontend**

Se destacó la relevancia de adaptar la experiencia a distintos dispositivos, asegurando una interfaz intuitiva y rápida; además de evitar la saturación de pantallas. 

[![Front](vv.png)](d)

### 4.3. Validation Interviews
#### 4.3.1. Diseño de Entrevistas

**Segmento #1: Bodegas especializadas por rubro**

**Presentación del entrevistado**

* ¿Cuál es tu nombre?
  
* ¿Qué edad tienes?

* ¿Desde cuándo gestionas esta bodega?

* ¿Cuál es el rubro principal de tu bodega?

El usuario interactúa con la app móvil de la plataforma para gestión de inventarios.

Landing page

Acciones clave dentro del sistema

Navegación interactivo por la interfaz app móvil 

**User Goal: Registrar**

El usuario selecciona la opción "Register", completa los campos solicitados y hace clic en el botón "Registrar".

A continuación, se muestra el panel "Add Card", donde debe llenar los campos relacionados con su tarjeta y correo electrónico.

Una vez que el proceso de pago se complete exitosamente, se notifica al usuario con un mensaje confirmando el vínculo de su tarjeta con la plataforma.

Del mismo modo, si el usuario desea retirar su información o actualizarla, lo podrá hacer a través de su perfil.

Finalmente, hacer clic en el botón "Aceptar".


**User Goal: Iniciar sesión**

El usuario introduce su correo y contraseña.

Luego hace clic en el botón "Log In".

Después, se le redirige al panel de perfil.

Allí puede editar su información personal y acceder a herramientas según su perfil ("Administrador" o "Empleado").

**User Goal: Navegar por el Dashboard**

El usuario inicia sesión desde la Landing Page.

Ingresa a la vista principal del Dashboard.

Visualiza el total de productos registrados y la fecha del último proveedor.

Visualiza un resumen de productos próximos a caducar con su respectiva fecha y stock disponible.

Accede a botones de acción rápida como “Historial”, “Inventario”, “Añadir Productos”, “Kits” y “Devolución de productos”.

**User Goal: Inventario (Producto / Lote)**

Ingresa a la sección de Inventario.

Revisa el listado de productos presionando el botón "por producto".

Filtra los productos por categoría, nombre del producto, fecha o stock mínimo.

Consulta el listado con información clave: fecha de entrada, cantidad por unidad, precio, stock mínimo y unidad de medida.


**User Goal: Botones Principales (Agregar Producto y Kits)**

Pulsa el botón "Agregar Producto".

Rellena los campos solicitados para registrar uno nuevo.

Pulsa el botón "Crear Kit".

Combina productos existentes para crear un kit nuevo.

El usuario pulsa el botón “Añadir Productos” desde el Dashboard.

Visualiza una galería de productos existentes y accede a opciones para editarlos o duplicarlos.

Puede agregar uno nuevo haciendo clic en el botón “+”, donde se despliega un formulario con campos como nombre, etiquetas, cantidad, lote, precios, fecha de caducidad y notas.

Desde el menú principal, también accede a la opción “Kits”.

En esta sección, selecciona productos existentes y los combina mediante el botón “Seleccionar para kit”, indicando cantidad e inventario disponible.

**User Goal: Historial de Movimientos**

Navega a la sección de Historial.

Visualiza entradas y salidas de productos.

Filtra movimientos por fecha, producto o lote.

El usuario accede a la sección de Historial desde el panel principal.

Filtra los registros por tipo de gestión, categoría, stock promedio y fecha.

Visualiza los movimientos realizados, incluyendo datos como nombre del producto, fecha de consulta, precio unitario, cantidad y total.

Consulta métricas como el stock promedio, estado del producto y stock ideal.

Cuenta con botones para editar o eliminar cada registro y, para los stock promedio, exportar la información y realiza un ticket promedio.


**User Goal: Alerta de Stock**

El usuario accede a la sección de Alertas desde el menú superior.

Consulta una lista de productos que presentan alertas por stock mínimo o por cercanía a su fecha de vencimiento.

Visualiza detalles como categoría de alerta, tipo de producto, nombre y fecha de alerta.

Puede ingresar a una vista de detalles, generar reportes o confirmar acciones desde botones individuales por producto.

También puede eliminar una alerta específica luego de una confirmación emergente.

**Preguntas principales:**

* ¿Te resultó fácil encontrar cómo agregar un producto?
  
* ¿Qué tal fue el proceso para registrar el stock por producto y por lote?
  
* ¿Te resultó claro el apartado de “Próximos a caducar”? ¿Te pareció útil?
  
* ¿Probaste la sección de kits? ¿Te resultó útil combinar productos?
  
* ¿Hubo algo que no entendiste o que te confundió mientras usabas la app?
  
* ¿Qué te pareció el diseño general de la landing page?
  
* ¿Tuviste alguna dificultad visual o técnica durante la navegación?

**Valoración de experiencia**

* Del 1 al 10, ¿qué tan útil te pareció la app para tu bodega?
  
* ¿Qué funcionalidad te pareció más valiosa?
  
* ¿Qué función le agregarías sí o sí?
  
* ¿Recomendarías esta plataforma a otros dueños de bodegas? ¿Por qué?

**Segmento #2: Startups y emprendedores con necesidades logísticas**

**Presentación del entrevistado**

* ¿Cuál es tu nombre?
* ¿Qué edad tienes?
* ¿Qué tipo de producto vendes o almacenas?
* ¿Tienes local físico, almacén propio o trabajas con terceros?
  
Interactúa el usuario con la landing page y la versión web de nuestra plataforma para gestión gestionar stock, registrar compras y generar reportes.

**Landing page**

Acciones clave dentro del sistema

Navegación interactivo por la interfaz app móvil 

**User Goal: Registrar**

El usuario selecciona la opción "Register", completa los campos solicitados y hace clic en el botón "Registrar".

A continuación, se muestra el panel "Add Card", donde debe llenar los campos relacionados con su tarjeta y correo electrónico.

Una vez que el proceso de pago se complete exitosamente, se notifica al usuario con un mensaje confirmando el vínculo de su tarjeta con la plataforma.

Del mismo modo, si el usuario desea retirar su información o actualizarla, lo podrá hacer a través de su perfil.

Finalmente, hacer clic en el botón "Aceptar".

**User Goal: Iniciar sesión**

El usuario introduce su correo y contraseña.

Luego hace clic en el botón "Log In".

Después, se le redirige al panel de perfil.

Allí puede editar su información personal y acceder a herramientas según su perfil ("Administrador" o "Empleado").

**User Goal: Navegar por el Dashboard**

El usuario inicia sesión desde la Landing Page.

Ingresa a la vista principal del Dashboard.

Visualiza el total de productos registrados y la fecha del último proveedor.

Visualiza un resumen de productos próximos a caducar con su respectiva fecha y stock disponible.

Accede a botones de acción rápida como “Historial”, “Inventario”, “Añadir Productos”, “Kits” y “Devolución de productos”.

**User Goal: Inventario (Lote)**

Accede a la sección de Inventario por lote.

Filtra los lotes por nombre del producto, proveedor, fecha de entrada, cantidad o precio.

Consulta el listado con información detallada como proveedor, producto, fecha, cantidad por unidad, precio y unidad de medida.

Gestiona las acciones disponibles para cada lote desde la columna correspondiente.

*User Goal: Botones Principales (Agregar Producto y Kits)*

Pulsa el botón "Agregar Producto".

Rellena los campos solicitados para registrar uno nuevo.

Pulsa el botón "Crear Kit".

Combina productos existentes para crear un kit nuevo.

El usuario pulsa el botón “Añadir Productos” desde el Dashboard.

Visualiza una galería de productos existentes y accede a opciones para editarlos o duplicarlos.

Puede agregar uno nuevo haciendo clic en el botón “+”, donde se despliega un formulario con campos como nombre, etiquetas, cantidad, lote, precios, fecha de caducidad y notas.

Desde el menú principal, también accede a la opción “Kits”.

En esta sección, selecciona productos existentes y los combina mediante el botón “Seleccionar para kit”, indicando cantidad e inventario disponible.

**User Goal: Historial de Movimientos**

Navega a la sección de Historial.

Visualiza entradas y salidas de productos.

Filtra movimientos por fecha, producto o lote.

El usuario accede a la sección de Historial desde el panel principal.

Filtra los registros por tipo de gestión, categoría, stock promedio y fecha.

Visualiza los movimientos realizados, incluyendo datos como nombre del producto, fecha de consulta, precio unitario, cantidad y total.

Consulta métricas como el stock promedio, estado del producto y stock ideal.

Cuenta con botones para editar o eliminar cada registro y, para los stock promedio, exportar la información y realiza un ticket promedio.

**User Goal: Alerta de Stock**

El usuario accede a la sección de Alertas desde el menú superior.

Consulta una lista de productos que presentan alertas por stock mínimo o por cercanía a su fecha de vencimiento.

Visualiza detalles como categoría de alerta, tipo de producto, nombre y fecha de alerta.

Puede ingresar a una vista de detalles, generar reportes o confirmar acciones desde botones individuales por producto.

También puede eliminar una alerta específica luego de una confirmación emergente.

**Preguntas principales:**

* ¿Qué opinas de las alertas de stock mínimo/máximo y vencimiento? ¿Son suficientes?
* ¿La sección de historial de movimientos te pareció útil para revisar tus registros?
* ¿Te resultó útil la opción de devolución de productos?
* ¿Los reportes del historial son útiles para tomar decisiones?
* ¿Hubo algo que no entendiste o que te confundió mientras usabas la app?
* ¿Qué te pareció el diseño general de la landing page?
* ¿Tuviste alguna dificultad visual o técnica durante la navegación?
  
**Valoración de experiencia**

* Del 1 al 10, ¿qué tan útil te pareció la app móvil  para tu bodega?
* ¿Qué funcionalidad te pareció más valiosa?
* ¿Qué función le agregarías sí o sí?
* ¿Recomendarías esta plataforma a otros emprendedores? ¿Por qué?


#### 4.3.2. Registro de Entrevistas
#### 4.3.3. Evaluaciones según heurísticas
