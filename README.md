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
### Deployment Backend:
En esta sección, detallamos el proceso de implementación de nuestro backend en la plataforma de Google Cloud.

#### Creación de VPS en Google Cloud Platform (GCP)

A continuación se detallan los pasos para crear un servidor privado virtual (VPS) en Google Cloud Platform para el despliegue del backend:

##### 1. Configuración Inicial del Proyecto

**Paso 1: Crear un Proyecto en GCP**
1. Iniciar sesión en [Google Cloud Console](https://console.cloud.google.com/)
2. Hacer clic en el selector de proyectos en la parte superior
3. Seleccionar "NUEVO PROYECTO"
4. Asignar un nombre descriptivo al proyecto (ej: "stockwise-backend")
5. Hacer clic en "CREAR"

**Paso 2: Configurar Facturación**
1. Navegar a "Facturación" en el menú de navegación
2. Vincular una cuenta de facturación válida
3. Seleccionar el proyecto creado como proyecto de facturación

##### 2. Creación de la Instancia de VM

**Paso 3: Habilitar Compute Engine API**
1. En la barra de búsqueda, escribir "Compute Engine API"
2. Seleccionar la API y hacer clic en "HABILITAR"

**Paso 4: Crear Instancia de VM**
1. Navegar a "Compute Engine" > "Instancias de VM"
2. Hacer clic en "CREAR INSTANCIA"
3. Configurar los siguientes parámetros:

**Detalles de la Instancia:**
- **Nombre**: stockwise-backend-server
- **Región**: us-central1 (o la región más cercana a los usuarios)
- **Zona**: us-central1-a

**Configuración de Máquina:**
- **Tipo de máquina**: e2-medium (2 vCPU, 4 GB RAM)
- **Serie**: E2
- **Tipo de máquina**: Uso general

**Disco de arranque:**
- **Sistema operativo**: Ubuntu
- **Versión**: Ubuntu 20.04 LTS
- **Tipo**: Disco persistente equilibrado
- **Tamaño**: 30 GB

**Firewall (Reglas de red):**
-  Permitir tráfico HTTP
-  Permitir tráfico HTTPS
-  Permitir tráfico SSH

4. Hacer clic en "CREAR" para iniciar la creación de la instancia


##### 3. Configuración de Acceso y Seguridad

**Paso 5: Configurar Acceso SSH**
1. Una vez creada la instancia, hacer clic sobre el nombre de la instancia
2. En la sección "Conectarse", hacer clic en "Modificar" en "Control de acceso"
3. Agregar la clave SSH pública del equipo de desarrollo
4. Alternativamente, usar "Abrir en ventana del navegador" para acceso directo

**Paso 6: Configurar Reglas de Firewall Personalizadas**
1. Navegar a "Redes VPC" > "Firewall"
2. Hacer clic en "CREAR REGLA DE FIREWALL"
3. Configurar para el backend:
   - **Nombre**: backend-api-allow
   - **Dirección IP de origen**: 0.0.0.0/0 (para desarrollo)
   - **Protocolos y puertos**: TCP, puerto 8080 (o puerto del API)
4. Hacer clic en "CREAR"
<br>

![Dashboard de Google Cloud](assets/chapter-4/googleCloud-Dashboard.png)
<br>

![Swagger-1](assets/chapter-4/swagger-1.png)
<br>

![Swagger-2](assets/chapter-4/swagger-2.png)
<br>

![Swagger-3](assets/chapter-4/swagger-3.png)
<br>

![Swagger-4](assets/chapter-4/swagger-4.png)



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

En esta sección se evidencia la documentación de los servicios implementados para el sprint actual que conforman el backend.

Backend

![Swagger](assets/chapter-4/swagger-5.png)
<br>

Athentication 

![Swagger-1](assets/chapter-4/swagger-IAM.png)
<br>

Inventory

![Swagger-1](assets/chapter-4/swagger-inventory.png)
<br>

Products

![Swagger-1](assets/chapter-4/swagger-Products.png)
<br>

Combos

![Swagger-1](assets/chapter-4/swagger-Combos.png)
<br>

Report 
![Swagger-1](assets/chapter-4/swagger-Report.png)

<br>

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
#### 1. Configuración del Entorno Docker en el VPS

**Paso 1: Instalación de Docker y Docker Compose**
```bash
# Actualizar paquetes del sistema
sudo apt update && sudo apt upgrade -y

# Instalar dependencias necesarias
sudo apt install -y apt-transport-https ca-certificates curl software-properties-common

# Agregar la clave GPG oficial de Docker
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg

# Agregar el repositorio de Docker
echo "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

# Actualizar paquetes e instalar Docker
sudo apt update
sudo apt install -y docker-ce docker-ce-cli containerd.io docker-compose-plugin

# Iniciar y habilitar Docker
sudo systemctl start docker
sudo systemctl enable docker

# Añadir el usuario actual al grupo docker
sudo usermod -aG docker $USER
```

**Paso 2: Verificación de la instalación**
```bash
# Verificar versión de Docker
docker --version
docker compose version

# Probar Docker con un contenedor de prueba
docker run hello-world
```

#### 2. Preparación del Proyecto ASP.NET 9

**Paso 3: Creación del Dockerfile**
```dockerfile
# Usar imagen base de ASP.NET 9
FROM mcr.microsoft.com/dotnet/aspnet:9.0 AS base
WORKDIR /app
EXPOSE 8080
EXPOSE 8081

FROM mcr.microsoft.com/dotnet/sdk:9.0 AS build
WORKDIR /src
COPY ["StockWise.API/StockWise.API.csproj", "StockWise.API/"]
RUN dotnet restore "StockWise.API/StockWise.API.csproj"

COPY . .
WORKDIR "/src/StockWise.API"
RUN dotnet build "StockWise.API.csproj" -c Release -o /app/build

FROM build AS publish
RUN dotnet publish "StockWise.API.csproj" -c Release -o /app/publish /p:UseAppHost=false

FROM base AS final
WORKDIR /app
COPY --from=publish /app/publish .
ENTRYPOINT ["dotnet", "StockWise.API.dll"]
```

**Paso 4: Creación del archivo docker-compose.yml**
```yaml
version: '3.8'

services:
  stockwise-api:
    build:
      context: .
      dockerfile: Dockerfile
    ports:
      - "8080:8080"
      - "8081:8081"
    environment:
      - ASPNETCORE_ENVIRONMENT=Production
      - ASPNETCORE_URLS=http://+:8080
      - ConnectionStrings__DefaultConnection=Host=stockwise-db;Database=StockWiseDB;Username=stockwise_user;Password=TuPasswordSeguro123!
    depends_on:
      - stockwise-db
    networks:
      - stockwise-network
    restart: unless-stopped

  stockwise-db:
    image: postgres:15-alpine
    environment:
      - POSTGRES_DB=StockWiseDB
      - POSTGRES_USER=stockwise_user
      - POSTGRES_PASSWORD=TuPasswordSeguro123!
    ports:
      - "5432:5432"
    volumes:
      - postgres_data:/var/lib/postgresql/data
    networks:
      - stockwise-network
    restart: unless-stopped

volumes:
  postgres_data:

networks:
  stockwise-network:
    driver: bridge
```

#### 3. Despliegue de la Aplicación

**Paso 5: Clonación del Repositorio y Configuración**
```bash
# Crear directorio para la aplicación
sudo mkdir -p /opt/stockwise
cd /opt/stockwise

# Clonar el repositorio
git clone https://github.com/upc-pre-202520-1ACC0238-12612-Stoq/Web-Services.git .

# Construir las imágenes Docker
docker compose build

# Iniciar los servicios en modo detached
docker compose up -d

# Verificar el estado de los contenedores
docker compose ps
```

#### 4. Configuración de Nginx como Reverse Proxy

**Paso 6: Instalación y Configuración de Nginx**
```bash
# Instalar Nginx
sudo apt install -y nginx

# Configurar SSL con Let's Encrypt
sudo apt install -y certbot python3-certbot-nginx
sudo certbot --nginx -d tu-dominio.com
```

Este proceso completo asegura el despliegue robusto y escalable de la API ASP.NET 9 con PostgreSQL utilizando contenedores Docker en un VPS.

![Swagger-1](assets/chapter-4/googleCloud-Dashboard2.png)

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

**Segmento 1: Bodegas especializadas por rubro**

<table border="1">
  <tr>
    <th>Entrevista</th>
    <td>1</td>
    <th>Nombre</th>
    <td>Milagros Almerco</td>
  </tr>
  <tr>
    <th>Edad</th>
    <td>28</td>
    <th>Distrito</th>
    <td>San Martín de Porres</td>
  </tr>
  <tr>
    <th>Captura de la entrevista: <img src="assets/chapter-4/Segmento 1 - Milagros Almerco.png" alt="Captura de la entrevista" width="200"></th>
    <td colspan="3">
        Milagros Almerco, evaluó la app móvil StockWise y destacó su facilidad de uso al registrar productos y gestionar inventario. Aunque al inicio tuvo dudas sobre la diferencia entre “stock” y “lote”, logró comprenderlo rápidamente gracias a la interfaz intuitiva. Resaltó como funcionalidades más valiosas el control de productos próximos a vencer y la visualización por lotes, que considera claves para evitar pérdidas. Valoró también el diseño moderno y claro, sin presentar dificultades técnicas. Sugirió como mejora incluir un sistema para registrar pagos pendientes o créditos. En general, calificó la app como práctica, útil y recomendada para otros dueños de bodegas.
    </td>
  </tr>
  <tr>
    <th>URL de la grabación</th>
    <td colspan="3">
      <a href="https://upcedupe-my.sharepoint.com/:v:/g/personal/u20221g068_upc_edu_pe/EfICOj-xe6REtnBdqmvY7QsB40AX08yJQHh4VQP5k9XQUA?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJPbmVEcml2ZUZvckJ1c2luZXNzIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXciLCJyZWZlcnJhbFZpZXciOiJNeUZpbGVzTGlua0NvcHkifX0&e=SCUtfJ">
        Ver grabación
      </a>
    </td>
  </tr>
  <tr>
   <th>Timing</th>
    <td colspan="3">
         00:00 -5:48
    </td>
  </tr>
</table>
<br>

<table border="1">
  <tr>
    <th>Entrevista</th>
    <td>2</td>
    <th>Nombre</th>
    <td>Elvis Aranga Mesa</td>
  </tr>
  <tr>
    <th>Edad</th>
    <td>31</td>
    <th>Distrito</th>
    <td>Santiago de Surco</td>
  </tr>
  <tr>
    <th>Captura de la entrevista: <img src="assets/chapter-4/seg1-Elvis.png" alt="Captura de la entrevista" width="200"></th>
    <td colspan="3">
       Elvis Aranga Meza, encargado de un mini market en Surco, compartió su experiencia utilizando la app m´vil para la gestión de bodegas, destacando la facilidad de uso tanto para agregar productos como para navegar por las funciones principales, y calificando su utilidad con un 9 sobre 10. Consideró el diseño visual adecuado y sencillo, aunque sugirió mejorar el tamaño de la interfaz en dispositivos móviles. Resaltó la utilidad de funciones como la visualización de fechas de vencimiento para evitar mermas y la organización de productos por lote, lo cual facilita la gestión de promociones. Sugirió incorporar reportes y estadísticas que permitan proyectar ventas y establecer metas. Finalmente, recomendó la plataforma a otros bodegueros, especialmente por su precio y utilidad, aunque señaló la importancia de brindar asistencia a usuarios con menos experiencia tecnológica.
  </tr>
  <tr>
    <th>URL de la grabación</th>
    <td colspan="3">
      <a href="https://upcedupe-my.sharepoint.com/:v:/g/personal/u20221g068_upc_edu_pe/EfICOj-xe6REtnBdqmvY7QsB40AX08yJQHh4VQP5k9XQUA?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJPbmVEcml2ZUZvckJ1c2luZXNzIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXciLCJyZWZlcnJhbFZpZXciOiJNeUZpbGVzTGlua0NvcHkifX0&e=SCUtfJ">
        Ver grabación
      </a>
    </td>
  </tr>
  <tr>
   <th>Timing</th>
    <td colspan="3">
         5:48 - 11:47
    </td>
  </tr>
</table>

<table border="1">
  <tr>
    <th>Entrevista</th>
    <td>3</td>
    <th>Nombre</th>
    <td>Catalina Villa Guerra</td>
  </tr>
  <tr>
    <th>Edad</th>
    <td>28</td>
    <th>Distrito</th>
    <td>Breña</td>
  </tr>
  <tr>
    <th>Captura de la entrevista: <img src="assets/chapter-4/Interview-Catalina-Villa.png" alt="Captura de la entrevista" width="200"></th>
    <td colspan="3">
Catalina es una administradora de 28 años, encargada de gestionar una bodega familiar en el distrito de Breña. Ella menciona que las funciones que más le gustaron fueron la de alerta de productos próximos a vencer y la de control de stock, ya que considera que le ayudarían a evitar pérdidas por productos caducados y a mantener un mejor seguimiento de sus existencias. Sin embargo, percibe que estas funciones aún son básicas y podrían ofrecer opciones más avanzadas, como recordatorios personalizados o reportes automáticos. En cuanto a la interfaz, a Catalina le agradó el diseño sencillo y organizado, destacando que los botones son fáciles de identificar y las categorías están bien distribuidas. También comentó que la aplicación le resultaría útil para delegar mejor el control del inventario entre los miembros de su familia, facilitando así la administración general de la bodega.
    </td>
  </tr>
  <tr>
    <th>URL de la grabación</th>
    <td colspan="3">
      <a href="https://upcedupe-my.sharepoint.com/:v:/g/personal/u20221g068_upc_edu_pe/EfICOj-xe6REtnBdqmvY7QsB40AX08yJQHh4VQP5k9XQUA?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJPbmVEcml2ZUZvckJ1c2luZXNzIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXciLCJyZWZlcnJhbFZpZXciOiJNeUZpbGVzTGlua0NvcHkifX0&e=SCUtfJ">
        Ver grabación
      </a>
    </td>
  </tr>
  <tr>
   <th>Timing</th>
    <td colspan="3">
        11:48 - 21:31
    </td>
  </tr>
</table>

**Segmento 2: Startups y emprendedores en expansión con necesidades logísticas**

<table border="1">
  <tr>
    <th>Entrevista</th>
    <td>4</td>
    <th>Nombre</th>
    <td>Juan Carlos Ramírez</td>
  </tr>
  <tr>
    <th>Edad</th>
    <td>49</td>
    <th>Distrito</th>
    <td>Surquillo</td>
  </tr>
  <tr>
    <th>Captura de la entrevista: <img src="assets/chapter-4/seg2-carlitos.png" alt="Captura de la entrevista" width="200"></th>
    <td colspan="3">
      Juan Carlos Ramírez, emprendedor de 49 años, compartió su experiencia al utilizar la aplicación para la gestión de inventarios, destacando la facilidad de uso en el registro y control de productos, así como la organización del historial de movimientos. Consideró que estas herramientas podrían ayudarlo significativamente en su proceso de digitalización, ya que actualmente gestiona las entradas y salidas de manera manual mediante boletas y facturas físicas. En cuanto al diseño, señaló que la interfaz es clara y ordenada, aunque sugirió mejorar la personalización de reportes para adaptarlo mejor a las necesidades de su negocio. Finalmente, destacó que funcionalidades como la alerta de stock bajo y la gestión por lotes serían de gran apoyo para tener un control más preciso del inventario, y que la incorporación de estas herramientas digitales le permitiría automatizar procesos y liberar tiempo operativo en su gestión diaria.
    </td>
  </tr>
  <tr>
    <th>URL de la grabación</th>
    <td colspan="3">
      <a href="https://upcedupe-my.sharepoint.com/:v:/g/personal/u20221g068_upc_edu_pe/EfICOj-xe6REtnBdqmvY7QsB40AX08yJQHh4VQP5k9XQUA?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJPbmVEcml2ZUZvckJ1c2luZXNzIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXciLCJyZWZlcnJhbFZpZXciOiJNeUZpbGVzTGlua0NvcHkifX0&e=SCUtfJ">
        Ver grabación
      </a>
    </td>
  </tr>
  <tr>
   <th>Timing</th>
    <td colspan="3">
         21:31 - 25:14
    </td>
  </tr>
</table>

<table border="1">
  <tr>
    <th>Entrevista</th>
    <td>5</td>
    <th>Nombre</th>
    <td>Leonardo Gamboa</td></td>
  </tr>
  <tr>
    <th>Edad</th>
    <td>26</td>
    <th>Distrito</th>
    <td>San Miguel</td>
  </tr>
  <tr>
    <th>Captura de la entrevista: <img src="assets/chapter-4/Segmento2_Leo.png" alt="Captura de la entrevista" width="200"></th>
    <td colspan="3">
        Leonardo G., emprendedor que maneja actualmente su inventario de manera manual con hojas de Excel y una libreta, probó la plataforma y comentó que le pareció intuitiva, útil y eficaz para el control de su negocio. Señaló que la sección de alertas de stock le resultó especialmente atractiva, ya que le permitiría evitar ventas de productos agotados y responder más rápido a la demanda constante que maneja. En cuanto al diseño, mencionó que la interfaz es clara y sencilla, con botones fáciles de identificar y una navegación fluida. Leonardo destacó que la herramienta podría ayudarlo a organizar mejor sus pedidos y actualizar su inventario sin esfuerzo, reemplazando las hojas manuales que utiliza actualmente. También valoró que la plataforma sea accesible y de fácil uso, algo clave para quienes aún no están acostumbrados a los sistemas digitales, pero buscan dar ese paso hacia la automatización de su negocio.
    </td>
  </tr>
  <tr>
    <th>URL de la grabación</th>
    <td colspan="3">
      <a href="">
        Ver grabación
      </a>
    </td>
  </tr>
  <tr>
   <th>Timing</th>
    <td colspan="3">
         25:14 - 29:36
    </td>
  </tr>
</table>

<table border="1">
  <tr>
    <th>Entrevista</th>
    <td>6</td>
    <th>Nombre</th>
    <td>Gael Rivera</td>
  </tr>
  <tr>
    <th>Edad</th>
    <td>xx</td>
    <th>Distrito</th>
    <td>xx</td>
  </tr>
  <tr>
    <th>Captura de la entrevista: <img src="assets/chapter-4/seg2.png" alt="Captura de la entrevista" width="200"></th>
    <td colspan="3">
        Eduardo de Rivera Sosa, un emprendedor que importa productos desde Asia para venderlos en Perú, comentó que la idea del proyecto le pareció atractiva y muy necesaria para negocios que manejan múltiples referencias de productos. Durante la prueba, resaltó la facilidad de uso y la organización del panel principal, especialmente en el registro de productos y control de stock. Mencionó que actualmente lleva su inventario en Excel y organiza sus pedidos en Notion, por lo que considera que la app podría integrar y simplificar ambos procesos en un solo espacio digital. Valoró la función de alerta de stock bajo y las opciones de historial de movimientos, que le permitirían tener una visión más clara de sus existencias y reducir pérdidas por errores humanos o por actualizaciones tardías. En cuanto a la apariencia visual, Eduardo comentó que la landing page le pareció moderna y atractiva, destacando que transmite confianza y profesionalismo. Sin embargo, sugirió que la exportación de datos a Excel o PDF podría mejorarse con formatos más personalizables.
    </td>
  </tr>
  <tr>
    <th>URL de la grabación</th>
    <td colspan="3">
      <a href="https://upcedupe-my.sharepoint.com/:v:/g/personal/u20221g068_upc_edu_pe/EfICOj-xe6REtnBdqmvY7QsB40AX08yJQHh4VQP5k9XQUA?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJPbmVEcml2ZUZvckJ1c2luZXNzIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXciLCJyZWZlcnJhbFZpZXciOiJNeUZpbGVzTGlua0NvcHkifX0&e=SCUtfJ">
        Ver grabación
      </a>
    </td>
  </tr>
  <tr>
   <th>Timing</th>
    <td colspan="3">
       29:36 - 33:36 
    </td>
  </tr>
</table>

#### 4.3.3. Evaluaciones según heurísticas

**APP A EVALUAR**
**StockWise – App móvil de gestión de inventario para bodegas y emprendimientos**

---

**TAREAS A EVALUAR**

El alcance de esta evaluación incluye la revisión de la usabilidad en las siguientes tareas:

1. Registro de un nuevo usuario.  
2. Inicio de sesión con credenciales existentes.  
3. Registro y edición de productos.  
4. Búsqueda y filtrado de productos por nombre, categoría o lote.  
5. Visualización de productos próximos a vencer.  
6. Registro de salida o venta de productos.  
7. Consulta del historial de movimientos.  
8. Visualización de stock y control por lotes.  
9. Cierre de sesión.  

No están incluidas en esta versión de la evaluación las siguientes tareas:

1. Integración con sistemas externos de pago.  
2. Sincronización con otros dispositivos.  
3. Administración de usuarios con distintos roles.  
4. Funcionalidades futuras de geolocalización o predicción de demanda.  

---

**ESCALA DE SEVERIDAD**

| Nivel | Descripción |
|-------|--------------|
| **1** | Problema superficial: se supera fácilmente y no interfiere con la tarea. |
| **2** | Problema menor: ocurre con cierta frecuencia o requiere más esfuerzo. |
| **3** | Problema mayor: impide completar tareas o genera frustración frecuente. |
| **4** | Problema crítico: bloquea la tarea o impide el uso del sistema. |

---

**TABLA RESUMEN DE HALLAZGOS**

| # | Problema | Escala de severidad | Heurística/Principio violado(a) |
|---|-----------|---------------------|--------------------------------|
| 1 | No hay indicador visual claro de diferencia entre “Stock” y “Lote”, lo cual puede generar confusión inicial. | 2 | Usability – Claridad del lenguaje y correspondencia con el mundo real. |
| 2 | No existe un acceso rápido desde la pantalla principal al registro de ventas o salidas de productos. | 3 | Usability – Flexibilidad y eficiencia de uso. |
| 3 | No hay opción para registrar créditos o pagos pendientes dentro del flujo principal. | 3 | Information Architecture – Is it complete? |
| 4 | El tamaño de algunos botones y textos resulta pequeño en ciertos dispositivos móviles. | 2 | Inclusive Design – Accesibilidad visual. |
| 5 | No existe vista resumida o gráfica de reportes o estadísticas de ventas. | 2 | Usability – Visibilidad del estado del sistema. |
| 6 | La interfaz no muestra recordatorios personalizables para productos próximos a vencer. | 2 | Usability – Ayuda y prevención de errores. |

---

**DESCRIPCIÓN DE PROBLEMAS**

**PROBLEMA #1: Confusión inicial entre “Stock” y “Lote”**
**Severidad:** 2  
**Heurística violada:** Usabilidad – Correspondencia entre el sistema y el mundo real.  

**Problema:**  
Durante las pruebas, los usuarios Milagros y Catalina manifestaron dudas iniciales sobre la diferencia entre “stock” y “lote”. Aunque lograron comprenderlo después de explorar la app, el término no es intuitivo para todos los perfiles de usuarios, especialmente aquellos con poca experiencia digital.  

**Recomendación:**  
Agregar una breve descripción o globo de ayuda que explique la diferencia entre ambos términos (por ejemplo: “Stock: cantidad total disponible. Lote: grupo de productos con la misma fecha de vencimiento”).  

---

**PROBLEMA #2: Falta de acceso rápido al registro de ventas**
**Severidad:** 3  
**Heurística violada:** Usabilidad – Flexibilidad y eficiencia de uso.  

**Problema:**  
Usuarios como Elvis y Juan Carlos señalaron que, aunque el registro de productos es sencillo, no existe un acceso directo desde el dashboard para registrar ventas o salidas. Esto implica más pasos de navegación y retrasa la gestión diaria.  

**Recomendación:**  
Incluir un botón visible o un acceso rápido en el dashboard para registrar ventas o salidas directamente, sin pasar por el menú lateral.  

---

**PROBLEMA #3: Ausencia de módulo de pagos o créditos pendientes**
**Severidad:** 3  
**Heurística violada:** Information Architecture – Is it complete?  

**Problema:**  
Varios usuarios (Milagros y Juan Carlos) mencionaron la necesidad de registrar pagos pendientes o créditos, dado que muchas bodegas operan con ventas fiadas. La ausencia de esta función limita la utilidad integral de la app.  

**Recomendación:**  
Agregar un submódulo para registrar clientes con deudas y fechas de pago, con alertas visuales y posibilidad de marcar los pagos como cancelados.  

---

**PROBLEMA #4: Tamaño reducido de texto y botones**
**Severidad:** 2  
**Heurística violada:** Inclusive Design – Accesibilidad visual.  

**Problema:**  
Elvis mencionó que el tamaño de algunos elementos no se adapta correctamente en pantallas pequeñas, dificultando la interacción para usuarios con menos destreza táctil.  

**Recomendación:**  
Optimizar el diseño responsivo para móviles, asegurando un tamaño mínimo de toque de 44x44 px y contraste adecuado según WCAG 2.1.  

---

**PROBLEMA #5: Falta de reportes visuales o estadísticas**
**Severidad:** 2  
**Heurística violada:** Usabilidad – Visibilidad del estado del sistema.  

**Problema:**  
Los usuarios destacaron que la app podría mejorar si mostrara reportes o gráficos de ventas y stock. Actualmente, la información está distribuida, pero no se resume de forma visual.  

**Recomendación:**  
Incorporar una vista de “Resumen de actividad” con gráficos simples (barras o pastel) sobre productos más vendidos, alertas y stock por categoría.  

---

**PROBLEMA #6: Recordatorios limitados para productos próximos a vencer**
**Severidad:** 2  
**Heurística violada:** Usabilidad – Prevención de errores.  

**Problema:**  
Catalina valoró la alerta de productos próximos a vencer, pero comentó que sería mejor si pudiera configurar recordatorios personalizados según tipo de producto o periodo (por ejemplo, 5, 10 o 30 días antes del vencimiento).  

**Recomendación:**  
Permitir que el usuario ajuste la anticipación de alertas y el canal de notificación (push o correo).  

---

**CONCLUSIÓN GENERAL**

La app **StockWise** presenta una excelente base de usabilidad y accesibilidad, destacando por su claridad visual, fluidez de navegación y aprendizaje rápido incluso en usuarios con baja experiencia tecnológica.  

Las oportunidades de mejora se centran en profundizar funciones avanzadas de gestión (créditos, reportes, recordatorios personalizados) y refinar detalles visuales en dispositivos móviles.  

En general, los usuarios calificaron la experiencia como positiva, práctica y recomendable, con potencial para convertirse en una herramienta estándar para la gestión de bodegas pequeñas y medianas.

