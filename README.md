
# Capítulo IV: Product Design

## 4.1. Style Guidelines

A continuación se plantean los estilos y herramientas que se están utilizando como guías para el desarrollo de la aplicación web.


### 4.1.1. General Style Guidelines

1. **Misión**
   Desarrollar una plataforma integral y accesible que permita a los administradores de hostales y hoteles pequeños gestionar reservas, huéspedes y servicios adicionales de manera eficiente, mejorando la rentabilidad y experiencia de los huéspedes.

2. **Visión**
   Ser la plataforma líder en la digitalización de la gestión hotelera en América Latina, conocida por su simplicidad, accesibilidad y su enfoque en pequeñas y medianas empresas del sector turístico.

3. **Brand Name**
   El nombre del producto es **Hostel Manager**, una solución web diseñada para optimizar las operaciones de hostales y hoteles independientes. El logo de la marca está compuesto por una combinación de símbolos que representan la simplicidad y eficiencia, con un uso predominante del color **azul**, que transmite confianza y seguridad.

4. **Logo**
   
   <img width="261" height="51" alt="Image" src="https://github.com/user-attachments/assets/edc18bba-60fc-4d95-ad42-4b4a8bb4140e" />

5. **Colores** 
    Hemos elegido una paleta de colores que incluye verde claro, lila y azul, creando una combinación ligera y agradable a la vista para usuarios de diversas edades.

    <img width="1019" height="610" alt="Image" src="https://github.com/user-attachments/assets/0cf71c5b-69e7-4de8-8dda-74bda1549cfe" />

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

<img src="images/LandingPage Wireframes.png" style="width: 400px; height: auto;">



### 4.3.2. Landing Page Mock-up

El mock-up de alta fidelidad incorpora todos los elementos de la wireframe con el diseño visual completo:


## 4.4. Web Applications UX/UI Design

### 4.4.1. Web Applications Wireframes

<img src="images/WireRegistro.jpg">

<img src="images/WireHuespedes.jpg">

<img src="images/WireHuesped.jpg">

<img src="images/WireSuscripción.jpg">

Figma: https://www.figma.com/design/THILrBvLxbxNYgkxg87gPv/Untitled?node-id=16-680&t=O7qhBrZR5laBKvN3-0

### 4.4.2. Web Applications Wireflow Diagrams



En esta sección se presentan los Wireflow Diagrams desarrollados para una aplicación web, los cuales combinan wireframes de baja fidelidad con la representación visual de los flujos de usuario asociados a funciones clave de la plataforma.

Estos wireflows permiten visualizar tanto la estructura básica de las pantallas como la navegación entre vistas, mostrando cómo los usuarios interactúan con el sistema a través de distintas funcionalidades.

Se diseñaron wireflows específicos para las siguientes acciones principales de la aplicación:

- Inicio de Sesión: Representa el flujo desde la pantalla de acceso hasta la validación de credenciales y el ingreso exitoso al sistema.

- Editar: Muestra cómo un usuario puede acceder a un registro existente y modificar su contenido.

- Buscar: Ilustra la interacción con el motor de búsqueda y visualización de resultados.

- Crear Huésped: Describe el proceso completo para agregar un nuevo huésped al sistema, desde la apertura del formulario hasta la confirmación.

- Cancelar Suscripción: Detalla los pasos necesarios para dar de baja una suscripción, incluyendo confirmaciones.

Estos wireflows sirvieron como base para validar los flujos de navegación, identificar mejoras en la experiencia de usuario y alinear al equipo de diseño y desarrollo en torno a una visión compartida del funcionamiento de la aplicación.

#### Inicio de Sesión:

<img src="images/Aut.jpg">

#### Agregar Huesped

<img src="images/agregarHuesped.jpg">

#### Editar Huesped  

<img src="images/EditarHuesped.jpg">

#### Buscar Huesped  

<img src="images/BuscarHuesped.jpg">

#### Cancelar Suscripción 

<img src="images/CancelarSuscripcion.jpg">


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

<img src="images/Mock1.jpg">

<img src="images/Mock2.jpg">

<img src="images/Mock3.jpg">

<img src="images/Mock4.jpg">

<img src="images/Mock5.jpg">

Figma: https://www.figma.com/design/THILrBvLxbxNYgkxg87gPv/Untitled?node-id=16-680&t=O7qhBrZR5laBKvN3-0

### 4.4.3. Web Applications User Flow Diagrams

En esta sección se presentan los User Flows (flujos de usuario) diseñados para representar las rutas que sigue un usuario dentro de la aplicación web para alcanzar objetivos específicos. Un User Flow es un diagrama que ilustra, de forma lógica y secuencial, cómo interactúa un usuario con el sistema, desde el punto de entrada hasta la finalización de una tarea.


#### Inicio de Sesión:

<img src="images/Aut.jpg">

#### Agregar Huesped

<img src="images/agregarHuesped.jpg">

#### Editar Huesped  

<img src="images/EditarHuesped.jpg">

#### Buscar Huesped  

<img src="images/BuscarHuesped.jpg">

#### Cancelar Suscripción 

<img src="images/CancelarSuscripcion.jpg">

## 4.5. Web Applications Prototyping

En esta sección se aborda el proceso de prototipado aplicado al desarrollo de aplicaciones web. El prototyping consiste en crear una representación interactiva del producto, que permite simular su funcionamiento antes de pasar a la etapa de desarrollo final.

<img src="images/Proto.jpg">

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


