
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
El propósito de StockWise es proporcionar una aplicación intuitiva y accesible para que pequeñas y medianas empresas, startups y bodegas especializadas puedan gestionar su inventario de forma eficiente, digitalizada y sin complicaciones técnicas ni altos costos.

El problema se encuentra en que muchos de estos negocios aún dependen de métodos manuales como hojas de cálculo, cuadernos físicos o herramientas no especializadas para registrar y controlar su stock. Esto genera errores frecuentes, pérdidas de productos, compras innecesarias, falta de trazabilidad y escasa visibilidad sobre la operación logística.

Hemos observado que esta situación impacta negativamente en la productividad del negocio, la satisfacción del cliente y la capacidad de tomar decisiones basadas en datos. A medida que estos negocios escalan, el desorden operativo se vuelve insostenible, provocando sobrecostos y afectando su crecimiento.

¿Cómo podríamos diseñar una aplicación de gestión de inventarios que sea lo suficientemente simple, funcional y adaptable para cubrir las necesidades reales de estos negocios en expansión, facilitando el control del inventario, reduciendo errores y mejorando la toma de decisiones, con métricas que midan eficiencia operativa, precisión del stock y satisfacción del usuario?

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

**Hipótesis 1:** Creemos que los usuarios valorarán las alertas inteligentes push.</br> Sabremos que es cierto. 
</br>Cuando al menos el 80% de los usuarios activos tengan las notificaciones activadas y reporten una reducción en quiebres de stock en encuestas de satisfacción.

**Hipótesis 2:** Creemos que los usuarios encontrarán valiosos los reportes visuales optimizados para móvil.</br> Sabremos que es cierto .
</br>el módulo de reportes muestre una tasa de uso semanal superior al 40% y contribuya a un aumento del 20% en la retención de usuarios.

**Hipótesis 3:** Creemos que ofrecer una versión gratuita con funcionalidades básicas incentivará la adopción inicial y las conversiones a premium.</br>
 Sabremos que es cierto</br>
si la tasa de conversión de usuarios gratuitos a premium supera el 5% y el tiempo hasta la conversión es menor a 90 días.

**Hipótesis 4:** Creemos que implementar alertas inteligentes por stock bajo y fechas de vencimiento reducirá significativamente los quiebres de inventario.</br>
Sabremos que tenemos razón </br>
Cuando los usuarios que activan las alertas experimenten una reducción del 30% en incidentes de stock cero en un período de 3 meses.

**Hipótesis 5:** Creemos que implementar  la generación de boletas de venta directamente en la app agilizará el proceso de cierre de ventas y el control de ingresos.</br>
Sabremos que tenemos razón, </br>
Cuando los usuarios que utilizan la función reporten un ahorro de tiempo mínimo de 1 hora diaria en administración y un control más preciso de su flujo de caja diario.  

#### 1.2.2.4. Lean UX Canvas

 <img src="assets/Chapter-1/Lean Ux canvas.png" alt="Lean Ux canvas" width="800px">

 *Imagen (N°1). Elaboración propia. Realizado en Canva*