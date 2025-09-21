
# Capítulo IV: Product Design

## 4.1. Style Guidelines

A continuación se plantean los estilos y herramientas que se están utilizando como guías para el desarrollo de la aplicación web.


### 4.1.1. General Style Guidelines

Historia de la marca

En esta sección se mostrará de manera organizada los Branding, Typography, Colors y Spacing que se usarán para diseñar nuestra solución.

Brand Overview: Simplificar y digitalizar la gestión de hostales y pequeños hoteles con una herramienta accesible y escalable.

Brand Name: El nombre de nuestra aplicación web es Hostel Manager.

Personalidad de marca: Confiable, moderna, cercana y eficiente.

Tono de comunicación: Profesional pero amigable, con un lenguaje claro y directo para administradores de hoteles.

Typography: El tipo de tipografía de letra elegido fue Poppins debido a que es moderna, legible y profesional, cuya integración fue fácil gracias a Google Fonts.

Colors:
- Fondo (Claro - #EAF0F2).
- Primario (Negro - #000000) para textos.
- Secundario (Dorado/Beige - #C1A15A) para detalles destacados, íconos, botones.

Spacing: Padding amplio en Desktop (24px) y en Mobile (16px), espacio entre secciones en Desktop (80p), en mobile (32px).


### 4.1.2. Web Style Guidelines

La aplicación web se adaptará a todo tipos de dispositivos tecnológicos usados por nuestros segmentos objetivos, garantizando que la usabilidad se mantenga en todo momento. Esto ofrecerá una experiencia de usuario satisfactoria y coherente, independientemente del dispositivo que use el usuario en ese momento.

Se utilizará un patrón Z para el diseño de nuestro landing page, dado que queremos que el usuario mire primero nuestro logo para luego proceder con las opciones del navegador, donde luego vea el contenido de cada sección y termine con el texto que contiene cada una de las secciones.

Para la aplicación web pensamos usar el patrón F porque queremos que el usuario vea las opciones disponibles para navegar para luego proceder con sus respectivas búsquedas y usos en la aplicación web.


**Animaciones y transiciones:**
- Transiciones suaves (0.2s-0.3s) para cambios de estado
- Animaciones funcionales (no decorativas) para mejorar UX
- Feedback visual inmediato para acciones del usuario

**Accesibilidad:**
- Contraste de color que cumple WCAG 2.1 AA
- Textos alternativos para todas las imágenes
- Navegación completa por teclado
- Etiquetas ARIA para componentes personalizados

## 4.2. Information Architecture

En esta sección, estableceremos la estructura de las secciones de nuestro software que incluye el landing page y la aplicación web para cada segmento objetivo.

### 4.2.1. Organization Systems

Jerárquica:
- Landing Page: Títulos grandes para características principales, subtítulos para beneficios y características.

Secuencial:
- Procesos críticos: Check-in/out, pago y reservas paso a paso en la plataforma.

Matricial:
- Reportes y dashboards: Tablas y gráficos con filtros según fecha, ocupación, ingresos, room service.

Esquemas de categorización:
- Alfabético para los servicios y habitaciones.
- Cronológico para el historial de reservas y pagos.

### 4.2.2. Labeling Systems
  
- Se usarán etiquetas claras y cortas como: “Reservas”, “Habitaciones”, “Pagos”, “Room Service”, “Reportes”.
- Iconografía simple y universal para acciones clave: check-in, check-out, editar, eliminar.
- Mensajes de alerta concisos: “Reserva confirmada”, “Pago exitoso”, “Error de conexión”.

### 4.2.3. SEO Tags and Meta Tags

**Landing Page:**

```html
<title>HostelManager - Gestiona tu hostal con facilidad</title>
<meta name="description" content="Plataforma web para centralizar reservas, pagos, room service y reportes de tu hostal o pequeño hotel en LATAM.">
<meta name="keywords" content="hotelera, reservas online, hotel pequeño, hostal, software hotel.
">
```

**Web Application**
```html
<head>
  <title>Hostel Manager – App de Gestión.</title>
  <meta name="description" content="Administra tus habitaciones, reservas y servicios adicionales de manera simple y efectiva.">
  <meta name="keywords" content="Administración hotelera, reservas, reportes, room service">
  <meta name="author" content="Hostel Manager Team">
</head>

```

### 4.2.4. Searching Systems

- Barra de búsqueda global en Dashboard
- Filtros disponibles:
 - Habitaciones → tipo, disponibilidad, capacidad.
 - Reservas → fecha, huésped, estado de pago.
 - Room Service → tipo de servicio, estado, fecha.


### 4.2.5. Navigation Systems

- Menú superior fijo con secciones: “Reservas”, “Habitaciones”, “Room Service”, “Reportes”, “Promociones”.
- Botones CTA en secciones clave (reservar, pagar, generar reporte).
- Navegación adaptada a Mobile: menú hamburguesa y accesos rápidos.


## 4.3. Landing Page UI Design

### 4.3.1. Landing Page Wireframe

La wireframe de la landing page de HostelManager presenta una estructura clara y orientada a la conversión, con las siguientes secciones:


### 4.3.2. Landing Page Mock-up

El mock-up de alta fidelidad incorpora todos los elementos de la wireframe con el diseño visual completo:


## 4.4. Web Applications UX/UI Design

### 4.4.1. Web Applications Wireframes

<img src="images/WireRegistro.jpg">

<img src="images/WireHuespedes.jpg">

<img src="images/WireHuesped.jpg">

<img src="images/WireSuscripción.jpg">

### 4.4.2. Web Applications Wireflow Diagrams


### 4.4.2. Web Applications Mock-ups

Los mock-ups de alta fidelidad implementan todos los elementos de los wireframes con el diseño visual completo:

**Características visuales destacadas:**
- Paleta completa de colores aplicada coherentemente
- Tipografía Roboto para textos y Montserrat para títulos
- Iconografía Material Design personalizada
- Elementos interactivos con estados visuales claros
- Jerarquía visual definida con tamaños y pesos tipográficos

**Dashboard administrativo:**
- Widgets con información crítica resaltada
- Gráficos con paleta de colores consistente
- Indicadores visuales de estado (semáforo para ocupación)
- Accesos rápidos a funciones frecuentes

**Sistema de reservas:**
- Calendario con indicadores visuales de disponibilidad
- Formularios con validación visual inmediata
- Proceso paso a paso con indicador de progreso
- Confirmaciones visualmente destacadas

**Room service digital:**
- Catálogo visual con imágenes de alta calidad
- Estados de pedido claramente diferenciados por color
- Notificaciones push para actualizaciones de estado
- Interfaces adaptadas para acceso desde dispositivo del huésped

### 4.4.3. Web Applications User Flow Diagrams

## 4.5. Web Applications Prototyping

## 4.6. Domain-Driven Software Architecture
### 4.6.1. Design-Level EventStorming

### 4.6.2. Software Architecture Context Diagram

En esta sección se presenta el Software Architecture Context Diagram, un diagrama que proporciona una visión general del sistema en su contexto de operación. Su objetivo principal es mostrar cómo el sistema interactúa con los actores externos, como otros sistemas, usuarios y servicios. Este diagrama es fundamental para comprender el entorno en el que el sistema se despliega y cómo se conecta con componentes externos.

<img src="images/context.png">


### 4.6.3. Software Architecture Container Diagrams

En esta sección se presenta el Software Architecture Container Diagrams, diagrama que representa los principales contenedores del sistema y cómo se comunican entre sí. Un contenedor, en este contexto, hace referencia a una unidad de ejecución que encapsula un conjunto de funcionalidades del sistema. Estos contenedores pueden ser aplicaciones, bases de datos, servicios o cualquier otro componente que ejecute código o almacene datos de manera independiente.

<img src="images/container.png">

### 4.6.4. Software Architecture Components Diagrams

En esta sección se presenta el Software Architecture Components Diagrams, diagrama que detalla los componentes internos del sistema a un nivel más bajo de granularidad que los Container Diagrams. Este diagrama tiene como objetivo representar cómo los componentes individuales dentro de cada contenedor interactúan entre sí y cómo se organizan para cumplir con las funcionalidades del sistema.

<img src="images/components.png">

## 4.7. Software Object-Oriented Design
### 4.7.1. Class Diagrams

En esta sección se presentan el Diagrama de Clases, una representación clave del diseño orientado a objetos del sistema HostelManager. Este diagrama permite visualizar la estructura estática del sistema, describiendo las clases principales que lo componen, sus atributos, métodos, relaciones y jerarquías.

<img src="images/db.png">

## 4.8. Database Design
### 4.8.1. Database Diagrams

En esta sección se presenta el Diagrama de base de datos, lo cual presenta la estructura lógica del modelo de datos que sustenta el sistema HostelManager. Este diagrama describe las principales entidades del sistema, sus atributos y las relaciones entre ellas, sirviendo como guía para la implementación de la base de datos relacional.

<img src="images/dbb.png">


