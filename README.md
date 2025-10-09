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
| Date | 2025-05-14 | 
| Time |  10:00 AM |
| Location |  UPC - Monterrico |
| Preparate by| Maycol Jhordan Rojas Velasquez | 
|  Attendees (to planning meeting) | Gómez Vallejos Sergio André ,Aranda Vallejos, Oscar Gabriel ,Ticona Panduro, Estrella del Pilar ,Durand Vera, Gianfranco Angel, Miranda Sinarahua, Piero Stephano  | 
| Sprint n-1 Review Summary | En resumen se desarrollaron avances en la landing page, backend y frontend mobile | 
| Sprint Planning Background | Durante esta etapa, se llevó a cabo una exhaustiva verificación de la funcionalidad de la landing page diseñada para el proyecto. El objetivo principal fue asegurar que la landing page cumpla con los estándares de calidad y proporcionar una experiencia óptima para los visitantes. Asimismo, se realizó la primera implementación de la aplicación mobil y el despliegue del backend |
| Sprint Goal & User Stories | 
| Sprint 1 Goal | Desarrolar la funcionalidad de la página web con i18n e implementar CRUD en el backend. Se considerará que el objetivo del sprint se ha cumplido si todas las historias de usuario relacionadas con la landing page están implementadas y si todas las historias de usuario relacionadas con la implementación de APIs para la gestión de una entidad están completadas en un 80%. |  
| Sprint Velocity | Se establece un Velocity de 36 Story Points para este Sprint. | 
| Sum of Story Points | 36 Story Points | 
##### 4.2.1.2. Sprint Backlog 1
##### 4.2.1.3. Development Evidence for Sprint Review
##### 4.2.1.4. Testing Suite Evidence for Sprint Review
##### 4.2.1.5. Execution Evidence for Sprint Review
##### 4.2.1.6. Services Documentation Evidence for Sprint Review
##### 4.2.1.7. Software Deployment Evidence for Sprint Review
##### 4.2.1.8. Team Collaboration Insights during Sprint

### 4.3. Validation Interviews
#### 4.3.1. Diseño de Entrevistas
#### 4.3.2. Registro de Entrevistas
#### 4.3.3. Evaluaciones según heurísticas