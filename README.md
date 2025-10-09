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
#### 4.1.4. Software Deployment Configuration

### 4.2. Landing Page & Mobile Application Implementation
#### 4.2.1. Sprint n
##### 4.2.1.1. Sprint Planning n
##### 4.2.1.2. Sprint Backlog n
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