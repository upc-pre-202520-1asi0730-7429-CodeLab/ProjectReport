<div align="center">

# Universidad Peruana De Ciencias Aplicadas
<img src = "https://upload.wikimedia.org/wikipedia/commons/f/fc/UPC_logo_transparente.png"></img>
<br/> **Carrera:** Ingeniería de Software
<br/> **Ciclo:** 202520
<br/> **Curso:** 1ASI0730 - Aplicaciones Web
<br/> **NRC:** 7429
<br/> **Profesor:** Villafuerte Bazan, Oscar Ivan
<br/> **Informe del Trabajo Final**
<br/> **Startup:** Codelab
<br/> **Producto:** HostelManager

|             Integrantes           |   Código   |
|-----------------------------------|------------|
|    Bautista Rivera, Jose Diego    | u202310949 |
|    Curi Marcelo, Angelo Marcio    | u202022387 |
|  Janampa Gutierrez, Jhoan Darner  | u202323319 |
|   Quiroz Caceres, Adrian Alonso   | u202214864 |
|  Velarde Gonzales, Nestor Hernan  | u20211c221 |

</div>

# Registro de Versiones del Informe
| Versión | Fecha      | Autor | Descripción de modificación|
|---------|------------|-------|----------------------------|
| V0.1    | 01/09/2025 | Todos | Creación del repositorio   |

# Project Report Collaboration Insights

# Contenido
- [Universidad Peruana De Ciencias Aplicadas](#universidad-peruana-de-ciencias-aplicadas)
- [Registro de Versiones del Informe](#registro-de-versiones-del-informe)
- [Project Report Collaboration Insights](#project-report-collaboration-insights)
- [Contenido](#contenido)
  - [Student Outcome](#student-outcome)
- [Capítulo I: Introducción](#capítulo-i-introducción)
  - [1.1. Startup Profile](#11-startup-profile)
    - [1.1.1. Descripción de la Startup](#111-descripción-de-la-startup)
    - [1.1.2. Perfiles de integrantes del equipo](#112-perfiles-de-integrantes-del-equipo)
  - [1.2. Solution Profile](#12-solution-profile)
    - [1.2.1. Antecedentes y problemática](#121-antecedentes-y-problemática)
    - [1.2.2. Lean UX Process](#122-lean-ux-process)
      - [1.2.2.1. Lean UX Problem Statements](#1221-lean-ux-problem-statements)
      - [1.2.2.2. Lean UX Assumptions](#1222-lean-ux-assumptions)
      - [1.2.2.3. Lean UX Hypothesis Statements](#1223-lean-ux-hypothesis-statements)
      - [1.2.2.4. Lean UX Canvas](#1224-lean-ux-canvas)
  - [1.3. Segmentos objetivo](#13-segmentos-objetivo)
- [Capítulo II: Requirements Elicitation \& Analysis](#capítulo-ii-requirements-elicitation--analysis)
  - [2.1. Competidores](#21-competidores)
    - [2.1.1. Análisis competitivo](#211-análisis-competitivo)
    - [2.1.2. Estrategias y tácticas frente a competidores](#212-estrategias-y-tácticas-frente-a-competidores)
  - [2.2. Entrevistas](#22-entrevistas)
    - [2.2.1. Diseño de entrevistas](#221-diseño-de-entrevistas)
    - [2.2.2. Registro de entrevistas](#222-registro-de-entrevistas)
    - [2.2.3. Análisis de entrevistas](#223-análisis-de-entrevistas)
  - [2.3. Needfinding](#23-needfinding)
    - [2.3.1. User Personas](#231-user-personas)
    - [2.3.2. User Task Matrix](#232-user-task-matrix)
    - [2.3.3. User Journey Mapping](#233-user-journey-mapping)
    - [2.3.4. Empathy Mapping](#234-empathy-mapping)
  - [2.4. Big Picture EventStorming](#24-big-picture-eventstorming)
  - [2.5. Ubiquitous Language](#25-ubiquitous-language)
- [Capítulo III: Requirements Specification](#capítulo-iii-requirements-specification)
  - [3.1. To-Be Scenario Mapping](#31-to-be-scenario-mapping)
  - [3.2. User Stories](#32-user-stories)
  - [3.3. Impact Mapping](#33-impact-mapping)
  - [3.4. Product Backlog](#34-product-backlog)
- [Capítulo IV: Product Design](#capítulo-iv-product-design)
  - [4.1. Style Guidelines](#41-style-guidelines)
    - [4.1.1. General Style Guidelines](#411-general-style-guidelines)
    - [4.1.2. Web Style Guidelines](#412-web-style-guidelines)
  - [4.2. Information Architecture](#42-information-architecture)
    - [4.2.1. Organization Systems](#421-organization-systems)
    - [4.2.2. Labeling Systems](#422-labeling-systems)
    - [4.2.3. SEO Tags and Meta Tags](#423-seo-tags-and-meta-tags)
    - [4.2.4. Searching Systems](#424-searching-systems)
    - [4.2.5. Navigation Systems](#425-navigation-systems)
  - [4.3. Landing Page UI Design](#43-landing-page-ui-design)
    - [4.3.1. Landing Page Wireframe](#431-landing-page-wireframe)
    - [4.3.2. Landing Page Mock-up](#432-landing-page-mock-up)
  - [4.4. Web Applications UX/UI Design](#44-web-applications-uxui-design)
    - [4.4.1. Web Applications Wireframes](#441-web-applications-wireframes)
    - [4.4.2. Web Applications Wireflow Diagrams](#442-web-applications-wireflow-diagrams)
    - [4.4.2. Web Applications Mock-ups](#442-web-applications-mock-ups)
    - [4.4.3. Web Applications User Flow Diagrams](#443-web-applications-user-flow-diagrams)
  - [4.5. Web Applications Prototyping](#45-web-applications-prototyping)
  - [4.6. Domain-Driven Software Architecture](#46-domain-driven-software-architecture)
    - [4.6.1. Design-Level EventStorming](#461-design-level-eventstorming)
    - [4.6.2. Software Architecture Context Diagram](#462-software-architecture-context-diagram)
    - [4.6.3. Software Architecture Container Diagrams](#463-software-architecture-container-diagrams)
    - [4.6.4. Software Architecture Components Diagrams](#464-software-architecture-components-diagrams)
  - [4.7. Software Object-Oriented Design](#47-software-object-oriented-design)
    - [4.7.1. Class Diagrams](#471-class-diagrams)
  - [4.8. Database Design](#48-database-design)
    - [4.8.1. Database Diagrams](#481-database-diagrams)
- [Capítulo V: Product Implementation, Validation \& Deployment](#capítulo-v-product-implementation-validation--deployment)
  - [5.1. Software Configuration Management](#51-software-configuration-management)
    - [5.1.1. Software Development Environment Configuration](#511-software-development-environment-configuration)
    - [5.1.2. Source Code Management](#512-source-code-management)
    - [5.1.3. Source Code Style Guide \& Conventions](#513-source-code-style-guide--conventions)
    - [5.1.4. Software Deployment Configuration](#514-software-deployment-configuration)
  - [5.2. Landing Page, Services \& Applications Implementation](#52-landing-page-services--applications-implementation)
    - [5.2.1. Sprint 1](#521-sprint-1)
      - [5.2.1.1. Sprint Planning 1](#5211-sprint-planning-1)
      - [5.2.1.2. Aspect Leaders and Collaborators](#5212-aspect-leaders-and-collaborators)
      - [5.2.1.3. Sprint Backlog 1](#5213-sprint-backlog-1)
      - [5.2.1.4. Development Evidence for Sprint Review](#5214-development-evidence-for-sprint-review)
      - [5.2.1.5. Execution Evidence for Sprint Review](#5215-execution-evidence-for-sprint-review)
      - [5.2.1.6. Services Documentation Evidence for Sprint Review](#5216-services-documentation-evidence-for-sprint-review)
      - [5.2.1.7. Software Deployment Evidence for Sprint Review](#5217-software-deployment-evidence-for-sprint-review)
      - [5.2.1.8. Team Collaboration Insights during Sprint](#5218-team-collaboration-insights-during-sprint)
- [Conclusiones](#conclusiones)
- [Bibliografía](#bibliografía)
- [Anexos](#anexos)

## Student Outcome
**El curso contribuye al cumplimiento del Student Outcome ABET:** ABET – EAC - Student Outcome 5
<br/> **Criterio:** La capacidad de funcionar efectivamente en un equipo cuyos miembros
juntos proporcionan liderazgo, crean un entorno de colaboración e inclusivo,
establecen objetivos, planifican tareas y cumplen objetivos.

|                                        Criterio específico                                     | Acciones realizadas | Conclusiones |
|------------------------------------------------------------------------------------------------|---------------------|--------------|
|                   Trabaja en equipo para proporcionar liderazgo en forma conjunta              |                     |              |
| Crea un entorno colaborativo e inclusivo, establece metas, planifica tareas y cumple objetivos |                     |              |

# Capítulo I: Introducción

## 1.1. Startup Profile
### 1.1.1. Descripción de la Startup
### 1.1.2. Perfiles de integrantes del equipo

## 1.2. Solution Profile
### 1.2.1. Antecedentes y problemática
### 1.2.2. Lean UX Process
#### 1.2.2.1. Lean UX Problem Statements
#### 1.2.2.2. Lean UX Assumptions
#### 1.2.2.3. Lean UX Hypothesis Statements
#### 1.2.2.4. Lean UX Canvas

## 1.3. Segmentos objetivo

# Capítulo II: Requirements Elicitation & Analysis

## 2.1. Competidores
### 2.1.1. Análisis competitivo
### 2.1.2. Estrategias y tácticas frente a competidores

## 2.2. Entrevistas
### 2.2.1. Diseño de entrevistas
### 2.2.2. Registro de entrevistas
### 2.2.3. Análisis de entrevistas

## 2.3. Needfinding
### 2.3.1. User Personas
### 2.3.2. User Task Matrix
### 2.3.3. User Journey Mapping
### 2.3.4. Empathy Mapping

## 2.4. Big Picture EventStorming
## 2.5. Ubiquitous Language

# Capítulo III: Requirements Specification

## 3.1. To-Be Scenario Mapping
## 3.2. User Stories
## 3.3. Impact Mapping
## 3.4. Product Backlog

# Capítulo IV: Product Design

## 4.1. Style Guidelines

### 4.1.1. General Style Guidelines

Para HostelManager, hemos definido las siguientes pautas de estilo general que proporcionarán consistencia en toda la plataforma:

**Paleta de colores:**
  

**Tipografía:**
  

**Iconografía:**


**Elementos de marca:**


### 4.1.2. Web Style Guidelines

**Responsive Design:**


**Componentes UI:**
- **Botones:**
  

- **Formularios:**
  

- **Tarjetas:**
  

- **Tablas:**
  

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

### 4.2.1. Organization Systems

HostelManager organiza su información siguiendo una estructura jerárquica y matricial para facilitar el acceso y gestión de datos:

**Estructura Jerárquica Principal:**
1. **Dashboard** - Vista general del estado del hostal/hotel
2. **Habitaciones** - Gestión de inventario y estado
3. **Reservas** - Administración de reservaciones
4. **Huéspedes** - Información de clientes
5. **Servicios** - Gestión de room service y adicionales
6. **Reportes** - Estadísticas y análisis
7. **Configuración** - Ajustes del sistema y plan de suscripción

**Organización Matricial:**
- **Por tipo de usuario:**
  - Administrador de hostal/hotel
  - Staff operativo
  - Huéspedes
- **Por función:**
  - Gestión operativa
  - Atención al cliente
  - Análisis financiero
- **Por temporalidad:**
  - Actividades diarias
  - Planificación semanal
  - Reportes mensuales/anuales

**Categorización de contenido:**
- Por tipo de habitación (Individual, Doble, Suite, etc.)
- Por estado de reserva (Confirmada, Pendiente, Cancelada)
- Por tipo de servicio (Desayuno, Limpieza, Lavandería)
- Por nivel de plan de suscripción (Básico, Estándar, Premium)

### 4.2.2. Labeling Systems

**Nomenclatura consistente:**
- **Habitaciones:** HAB-[número]-[tipo] (Ej: HAB-101-DBL para habitación doble 101)
- **Reservas:** RES-[ID]-[fecha] (Ej: RES-4582-25092025)
- **Huéspedes:** Nombre + ID único
- **Servicios:** [Tipo]-[ID] (Ej: DSYN-458 para desayuno)

**Etiquetado de funciones:**
- Verbos de acción claros: "Reservar", "Gestionar", "Configurar"
- Iconos acompañados de texto para mejorar comprensión
- Consistencia terminológica en toda la plataforma:
  - "Check-in" y "Check-out" (no alternando con "Entrada" y "Salida")
  - "Room Service" (no alternando con "Servicio a la habitación")

**Sistema de colores para estados:**
  

### 4.2.3. SEO Tags and Meta Tags

**Meta Tags básicos:**

```html
<title>HostelManager - Sistema de gestión para hostales y hoteles</title>
<meta name="description" content="Plataforma de gestión integral para hostales y pequeños hoteles. Administra reservas, clientes y servicios de room service con nuestra solución cloud por suscripción.">
<meta name="keywords" content="gestión hostal, software hotel, reservas hotel, sistema administración hostelería, room service digital">
```

**Meta Tags para redes sociales:**
```html
<!-- Open Graph (Facebook, LinkedIn) -->
<meta property="og:title" content="HostelManager - Digitaliza la gestión de tu hostal">
<meta property="og:description" content="Plataforma todo-en-uno para gestionar reservas, huéspedes y servicios en hostales y pequeños hoteles.">
<meta property="og:image" content="https://hostelmanager.com/images/og-image.jpg">
<meta property="og:url" content="https://hostelmanager.com">
<meta property="og:type" content="website">

<!-- Twitter Card -->
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="HostelManager - Gestión hotelera simplificada">
<meta name="twitter:description" content="Administra tu hostal o pequeño hotel con nuestra plataforma digital todo-en-uno.">
<meta name="twitter:image" content="https://hostelmanager.com/images/twitter-card.jpg">
```

**Etiquetas estructurales:**
- Implementación de Schema.org para mejorar el entendimiento de motores de búsqueda:
```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "SoftwareApplication",
  "name": "HostelManager",
  "applicationCategory": "BusinessApplication",
  "operatingSystem": "Web",
  "offers": {
    "@type": "Offer",
    "price": "99.90",
    "priceCurrency": "USD"
  },
  "description": "Sistema de gestión para hostales y pequeños hoteles con funcionalidades de reserva, check-in/out y room service digital."
}
</script>
```

### 4.2.4. Searching Systems

**Búsqueda global:**
- Barra de búsqueda persistente en la navegación principal
- Búsqueda predictiva con autocompletado
- Resultados categorizados (Reservas, Huéspedes, Habitaciones, Servicios)


### 4.2.5. Navigation Systems

## 4.3. Landing Page UI Design

### 4.3.1. Landing Page Wireframe

La wireframe de la landing page de HostelManager presenta una estructura clara y orientada a la conversión, con las siguientes secciones:


### 4.3.2. Landing Page Mock-up

El mock-up de alta fidelidad incorpora todos los elementos de la wireframe con el diseño visual completo:


## 4.4. Web Applications UX/UI Design

### 4.4.1. Web Applications Wireframes

**Wireframes principales:**


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
### 4.6.3. Software Architecture Container Diagrams
### 4.6.4. Software Architecture Components Diagrams

## 4.7. Software Object-Oriented Design
### 4.7.1. Class Diagrams

## 4.8. Database Design
### 4.8.1. Database Diagrams

# Capítulo V: Product Implementation, Validation & Deployment

## 5.1. Software Configuration Management
### 5.1.1. Software Development Environment Configuration
### 5.1.2. Source Code Management
### 5.1.3. Source Code Style Guide & Conventions
### 5.1.4. Software Deployment Configuration

## 5.2. Landing Page, Services & Applications Implementation
### 5.2.1. Sprint 1
#### 5.2.1.1. Sprint Planning 1
#### 5.2.1.2. Aspect Leaders and Collaborators
#### 5.2.1.3. Sprint Backlog 1
#### 5.2.1.4. Development Evidence for Sprint Review
#### 5.2.1.5. Execution Evidence for Sprint Review
#### 5.2.1.6. Services Documentation Evidence for Sprint Review
#### 5.2.1.7. Software Deployment Evidence for Sprint Review
#### 5.2.1.8. Team Collaboration Insights during Sprint

# Conclusiones

# Bibliografía

# Anexos
