
# Capítulo I: Presentación
## 1.1. Startup Profile

### 1.1.1. Descripción de la Startup

StockWise es un aplicativo movil de gestión de inventarios dirigida a pequeñas y medianas empresas, startups y bodegas especializadas. Su objetivo principal es facilitar el control eficiente de entradas y salidas de productos, la gestión de usuarios, la configuración de alertas inteligentes, la generación de reportes detallados y de boleta de venta, todo a través de una interfaz intuitiva y accesible desde cualquier dispositivo.

La solución responde a una problemática concreta: muchos negocios aún utilizan métodos manuales (como hojas de cálculo o registros en papel) para administrar sus inventarios y pagos, lo cual genera errores, desorganización, sobrecompras y pérdidas económicas. StockWise busca resolver este problema digitalizando y centralizando el control del inventario y de las ganancias de la tienda, permitiendo a los negocios tomar decisiones basadas en datos y optimizar su operación mediante cuatro planes de funcionalidad avanzada:

- **Plan A – Entrada por voz:** Permite registrar productos mediante comandos de voz (ejemplo: “Agregar 20 botellas de agua al inventario”), ofreciendo mayor rapidez y comodidad, especialmente en situaciones donde el personal no pueda usar el teclado.

- **Plan B – Geolocalización (GPS):** Integra funciones de ubicación para optimizar la trazabilidad y distribución de productos, permitiendo identificar su procedencia, registrar puntos de entrega y visualizar en un mapa interactivo las distintas sedes o sucursales vinculadas a la tienda principal.

- **Plan C – Localización y predicción inteligente:**
  - Localiza: Utiliza un mapa interactivo con integración de códigos QR para ubicar productos dentro del almacén de manera precisa.
  - Predice: Implementa un sistema de reabastecimiento inteligente basado en patrones de ventas, que sugiere cuándo y cuánto stock reponer para evitar quiebres de inventario.

- **Plan D – Escaneo por lotes con cámara rápida:** En lugar de códigos de barras, la app toma una foto del producto o lote y una API de visión (como Google ML Kit) devuelve etiquetas genéricas. El usuario confirma el producto exacto y la cantidad en un menú antes de registrarlo, pudiendo ver directamente su ubicación en el almacén virtual.

<br>
<b>Misión: </b>Brindar a pequeñas y medianas empresas una solución de gestión de inventarios y pagos sencilla, accesible y eficiente, que les permita digitalizar su operación, reducir errores logísticos y tomar decisiones basadas en datos reales, apoyando así su crecimiento sostenible.

<br>
<b>Visión: </b>StockWise se enfoca en ser una aplicación preferida de los empresarios que buscan una gestión de inventarios, herramientas de alto valor con un modelo escalable, adaptable y centrado en el usuario.

### 1.1.2. Perfiles de integrantes del equipo
<table>
  <tr>
    <th>
      <img src="assets/Chapter-1/fotoJocy.png" alt="Foto de perfil de " width="800px">
    </th>
    <td valign="top">
      <p><b>Jocelyn Damaly Almerco Rohas</b></p>
      <p>
        Soy estudiante de Ingeniería de Software y actualmente curso el 5to ciclo. En mi tiempo libre me gusta tocar ukelele, leer libros, resolver sudoku, escuchar música y ver series.
      </p>
    </td>
  </tr>
  <tr>
    <th>
      <img src="https://imgur.com/ylpKMx2.png" alt="Foto de perfil de Jeremy" width="800px">
    </th>
    <td valign="top">
      <p><b>Jeremy Paucar Meneses</b></p>
      <p>
        Estudiante de Ingeniería de Software, apacionado a programar, tengo conocimientos en c++, js, c#, y algunos frameworks como Vue, dentro de mis pasatiempos esta escuchar musica, ver futbol y ver series
      </p>
    </td>
  </tr>
  <tr>
    <th>
      <img src="assets/Chapter-1/fotocam.png" alt="Foto de perfil de Camila" width="800px">
    </th>
    <td valign="top">
      <p><b>Sánchez Ríos, Camila Cristina</b></p>
      <p>
        Soy estudiante de la carrera de Ingeniería de Software en la Universidad Peruana de Ciencias Aplicadas, actualmente me encuentro en el octavo ciclo. Me gusta escuchar música y leer en los ratos libres y aprender más sobre la carrera.
      </p>
    </td>
  </tr>
  <tr>
    <th>
      <img src="assets/Chapter-1/fotoKevin.jpg" alt="Foto de perfil de Kevin" width="800px">
    </th>
    <td valign="top">
      <p><b>Chi Cruzatt, Kevin Jorge</b></p>
      <p>
        Actualmente estoy cursando la carrera de ingeniería de Software y me encuentro en el 6° ciclo. Tengo experiencia utilizando diferentes metodologías de diseño, como Domain Driven Design (DDD) y CMV, además de frameworks como Laravel y Spring en lenguajes como Java, PHP, etc. Me considero una persona paciente y perseverante en situaciones difíciles.
      </p>
    </td>
  </tr>
  <tr>
    <th>
      <img src="assets/Chapter-1/fotoAlejo.png" alt="Foto de perfil de Alejandro" width="800px">
    </th>
    <td valign="top">
      <p><b>Oroncoy Almeyda, Alejandro Daniel</b></p>
      <p>
      Mi nombre es Alejandro Oroncoy. Tengo 19 años, soy estudiante de la carrera de ingeniería de software, estoy en 6to ciclo. Me considero una persona proactiva, autodidacta y orientada a objetivos.
      </p>
    </td>
  </tr>
    <tr>
  </tr>
</table>
<br>

## 1.2. Solution Profile
### 1.2.1 Antecedentes y problemática

- **Who (¿Quiénes?)**<br>
Emprendedores, startups y pequeñas/medianas empresas con bodegas físicas que almacenan productos de distintos rubros como ropa, calzado, electrodomésticos, ferretería o alimentos. 

- **What (¿Qué sucede?)**<br>
A medida que sus negocios escalan, la gestión manual del inventario con hojas de cálculo o registros físicos se vuelve ineficiente, generando pérdidas, errores, quiebres de stock, sobrecompras y desorden logístico.

- **When (¿Cuándo ocurre?)**<br>
En el momento en que el negocio empieza a crecer, aumentar su variedad de productos o abrir múltiples canales de venta, como tiendas físicas y plataformas online.

- **Where (¿Dónde ocurre?)**<br>
En bodegas físicas propias, espacios alquilados o incluso en el hogar del emprendedor, especialmente en etapas tempranas o de expansión del negocio.

- **Why (¿Por qué es un problema?)**<br>
La falta de un sistema centralizado y en tiempo real impide tomar decisiones estratégicas basadas en datos. Esto afecta la planificación de compras, genera pérdidas económicas, y daña la experiencia del cliente final.

- **How (¿Cómo lo solucionan hoy?)**<br>
Mediante herramientas manuales como cuaderno o hojas de papel, inventarios escritos o software no especializado, que resultan limitados, propensos a errores y poco escalables.

- **How much (¿Cuánto cuesta no resolverlo?)**<br>
El costo se traduce en pérdidas económicas significativas por productos no vendidos, errores de stock, tiempo invertido en tareas manuales y menor competitividad frente a negocios más organizados.

### 1.2.2 Lean UX Process
#### 1.2.2.1. Lean UX Problem Statements
El propósito de StockWise es proporcionar una aplicación intuitiva y accesible para que empresas pequeñas y medianas, startups y bodegas especializadas puedan gestionar su inventario de forma eficiente, digitalizada y sin complicaciones técnicas ni altos costos.

Actualmente, muchos de estos negocios aún dependen de métodos manuales  para registrar y controlar su stock. Este enfoque genera errores frecuentes, tales como registros incorrectos, desactualización en tiempo real o pérdidas de productos. Como resultado, se producen compras innecesarias, falta de trazabilidad, escasa visibilidad sobre los niveles de inventario y una gestión logística ineficiente. Según un estudio de NetSuite (2024), el promedio de precisión de inventario en empresas es de aproximadamente 83 %, lo que refleja un margen de error significativo que afecta los costos operativos y la toma de decisiones.

Diversas investigaciones sostienen que una gestión ineficiente del inventario repercute directamente en la productividad empresarial, la satisfacción del cliente y la rentabilidad general del negocio, además de generar sobrecostos en almacenamiento y desperdicio de recursos (Altavant Consulting, 2024; Arce-Gonzales & Sandoval, 2023). A medida que estas empresas escalan, el desorden operativo se vuelve insostenible, reduciendo su capacidad de respuesta ante la demanda y su competitividad en el mercado.

Por lo tanto, surge la necesidad de diseñar una aplicación de gestión de inventarios que sea simple, funcional y adaptable, capaz de atender las necesidades reales de las pymes en crecimiento. Esta herramienta debe facilitar el control exacto del inventario, reducir errores humanos, mejorar la trazabilidad y proporcionar información en tiempo real para respaldar decisiones basadas en datos.

#### 1.2.2.2. Lean UX Assumptions
**Business Assumptions:**

1. Creemos que los negocios emergentes necesitan digitalizar su gestión de inventarios a través de una solución móvil accesible.

2. Estas necesidades se pueden satisfacer con una aplicación móvil intuitiva, escalable y de bajo costo.

3. Nuestros clientes iniciales serán emprendedores, startups y pequeñas empresas con bodegas especializadas que operan de manera ágil.

4. El principal valor que busca el cliente es tener control y visibilidad total de su inventario en tiempo real, desde cualquier lugar.

5. El cliente obtendrá además alertas inteligentes, reportes automáticos, generación de boletas de venta y una experiencia de usuario móvil optimizada.

6. Adquiriremos la mayoría de nuestros clientes mediante publicidad en redes sociales dirigida, ASO (Optimización de la App Store) y asociaciones con comunidades de emprendedores.

7. Nuestro modelo de ingresos se basará en un esquema freemium dentro de la app, con upgrade a planes premium que desbloqueen funcionalidades avanzadas.

8. Nuestra competencia directa e indirecta incluye aplicaciones genéricas como hojas de cálculo móviles (Excel, Sheets), recordatorios básicos (Calendar) y ERPs complejos con apps móviles poco intuitivas.

9. Nuestra ventaja competitiva radicará en la simplicidad móvil, el enfoque específico en las pymes y la especialización en la gestión de inventarios sobre la marcha.

10. El mayor riesgo para el negocio es una baja tasa de adopción o la percepción de que la app es compleja o redundante frente a métodos manuales.

11. Mitigaremos este riesgo realizando pruebas de usabilidad móvil con usuarios reales, iteraciones rápidas basadas en feedback y una estrategia de onboarding dentro de la app que guíe al usuario paso a paso.

**User Assumptions:**</br>
- **¿Quién es el usuario?** Dueños de negocios, encargados de bodegas o logística en pymes/startups que necesitan gestionar inventarios de forma remota.
  
- **¿Qué problemas busca resolver nuestro producto?** La falta de control inmediato del stock, los errores por registros manuales en papel, los sobrecostos por pérdidas y las ventas fallidas debido a quiebres de stock inesperados.

- **¿Qué características son importantes?** Un registro rápido de productos (por voz, cámara o manual), un historial de movimientos accesible, alertas push personalizables, reportes visuales simplificados y la generación de boletas de venta directamente desde el dispositivo móvil.

- **¿Dónde encaja nuestro producto en su trabajo?** Se integra en su flujo de trabajo diario para la gestión del inventario en la bodega, en el punto de venta o durante las rondas de reposición, permitiendo decisiones informadas desde cualquier lugar.

- **¿Cuándo y cómo es usado nuestro producto?** Se utiliza de manera frecuente a lo largo del día, directamente desde sus teléfonos inteligentes, para registrar entradas/salidas al momento, consultar niveles de stock en tiempo real y generar comprobantes al instante.

- **¿Cómo debe verse y comportarse?** Debe tener una interfaz de usuario (UI) móvil limpia, simple y con navegación táctil intuitiva. Debe ser rápida, responsiva y funcionar sin conexión para casos de uso críticos.

**Feature Assumptions:**

Creemos que la aplicación móvil debe contar con una interfaz táctil intuitiva y diseños adaptados a dispositivos móviles que permitan a emprendedores y administradores adoptarla sin dificultad, minimizando la curva de aprendizaje.

Creemos que la app debe proporcionar notificaciones push y alertas personalizables (por stock bajo, fechas de vencimiento o pedidos de proveedores) que mantendrán a los usuarios informados de manera proactiva para prevenir errores operativos.

Creemos que el sistema debe incluir un módulo de reportes y dashboards visuales optimizados para móvil que permitan visualizar de un vistazo métricas clave (productos más vendidos, niveles de stock, tendencias), facilitando la toma de decisiones ágiles.

#### 1.2.2.3. Lean UX Hypothesis Statements

**Hipótesis 1:** Creemos que las alertas inteligentes push resolverán el problema de pérdidas económicas por quiebres de stock inesperados que enfrentan las pymes.  
Sabremos que es cierto  
Cuando al menos el 80% de los usuarios activos reporten una reducción del 25% en pérdidas por productos agotados y mejoren su planificación de reabastecimiento en encuestas trimestrales.

**Hipótesis 2:** Creemos que los reportes visuales móviles resolverán la falta de visibilidad sobre el rendimiento del inventario que impide a los emprendedores tomar decisiones estratégicas basadas en datos.  
Sabremos que es cierto  
Cuando el 70% de los usuarios utilicen los reportes semanalmente y reporten una mejora del 30% en sus decisiones de compra y gestión de stock.

**Hipótesis 3:** Creemos que el modelo freemium resolverá la barrera económica que impide a pequeños negocios acceder a herramientas profesionales de gestión de inventarios.  
Sabremos que es cierto  
Cuando logremos una adopción del 15% de usuarios gratuitos que conviertan a premium en 60 días, demostrando el valor percibido de la solución.

**Hipótesis 4:** Creemos que las alertas automatizadas por stock bajo resolverán el problema de sobrecostos operativos causados por el monitoreo manual del inventario.  
Sabremos que tenemos razón  
Cuando los usuarios reduzcan en 40% el tiempo dedicado a control manual de stock y eliminen el 90% de los quiebres de inventario críticos.

**Hipótesis 5:** Creemos que la generación digital de boletas de venta resolverá los errores de facturación y la desorganización financiera que afecta el flujo de caja de las pymes.  
Sabremos que tenemos razón  
Cuando los usuarios reporten una reducción del 50% en errores de facturación y mejoren en 35% la precisión de su control de ingresos diarios.  

#### 1.2.2.4. Lean UX Canvas

 <img src="assets/Chapter-1/Lean Ux canvas.png" alt="Lean Ux canvas" width="800px">

 *Imagen (N°1). Elaboración propia. Realizado en Canva*