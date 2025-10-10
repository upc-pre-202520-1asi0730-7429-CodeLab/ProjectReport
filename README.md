
# Capítulo V: Product Implementation, Validation & Deployment

## 5.1. Software Configuration Management

En esta sección el equipo define las decisiones, herramientas y convenciones necesarias para mantener la consistencia durante todo el ciclo de desarrollo del proyecto “Hostel Manager”. Esto incluye la gestión del entorno de desarrollo, la administración del código fuente, las guías de estilo de programación y la configuración de despliegue.


### 5.1.1. Software Development Environment Configuration

Asegurando la homogeneidad entre los integrantes del equipo, se establecen las siguientes herramientas y entornos de desarrollo del proyecto:

| Herramienta                 | Propósito                                                  | Tipo        | Referencia/Descarga                                                   |
|-----------------------------|------------------------------------------------------------|-------------|-----------------------------------------------------------------------|
| Visual Studio Code          | Desarrollo de la Landing Page                              | IDE         | https://code.visualstudio.com/                                        |
| JetBrains WebStorm (Angular CLI) | Desarrollo del Frontend Web Application en Angular       | IDE         | https://www.jetbrains.com/help/webstorm/angular.html                  |
| JetBrains IntelliJ IDEA     | Desarrollo del Backend (RESTful API) en Node.js/Java       | IDE         | https://www.jetbrains.com/idea/                                       |
| Node.js                     | Entorno de ejecución para el Backend y gestión de dependencias (npm) | Runtime     | https://nodejs.org/es                                                 |
| PostgreSQL                  | Base de datos principal del sistema.                       | DBMS        | https://www.postgresql.org/                                           |
| MySQL Server                | Base de datos alternativa para pruebas e integraciones.    | DBMS        | https://www.mysql.com/                                                |
| Postman                     | Pruebas de endpoints y validación de APIs                  | Testing Tool| https://www.postman.com/                                              |
| GitHub                      | Repositorios de control de versiones                       | SCM         | https://github.com/                                                   |
| Figma                       | Diseño de UI/UX para Landing Page y WebApp                 | Diseño      | https://www.figma.com/es-es/                                          |



### 5.1.2. Source Code Management

Para llevar una correcta administración del código fuente se utilizará “GitHub” como plataforma central de control de versiones. Cada módulo del proyecto tendrá su propio repositorio:
 
 - Landing Page: https://github.com/upc-pre-202520-1asi0729-7338-CodeLab/LandingPage.git
 - Frontend WebApp: Por definir.
 - Web Service (API): Por definir.

GitFlow Workflow:

Se adoptará el modelo de branching “GitFlow” (Vincent Driessen) con las siguientes ramas principales:

 - main: versión completa en producción.
 - develop: integración de nuevas funcionalidades antes del release.
 - feat/nombre: ramas para nuevas características, en nuestro caso dividida en capítulos. Ejemplo: feat/chapter-1

Conventional Commits:

Se usará el estándar de Conventional Commits para mensajes de los commits:
 - feat: nueva funcionalidad en código.
 - fix: correción de bug.
 - docs: cambios en documentación.
 - style: formato y estilo (sin cambios funcionales).
 - refactor: cambios internos en el código.
 - test: pruebas añadidas o modificadas.
Ejemplo: git commit -m “feat: add room service request module”


### 5.1.3. Source Code Style Guide & Conventions


A continuación se mencionan las convenciones y guías de estilo adoptadas para el desarrollo del proyecto **HostelManager**, siguiendo lineamientos internacionales y buenas prácticas de codificación.  
Toda la nomenclatura será escrita en **inglés**, independientemente del lenguaje utilizado.  

El proyecto se desarrollará en tres entornos principales:  
- **Visual Studio Code** para la Landing Page (HTML, CSS y JavaScript).  
- **WebStorm** para el frontend en **Vue/TypeScript**.  
- **JetBrains IntelliJ IDEA** para el backend en **Node.js/Java**.  


#### HTML
- Declarar el tipo de documento en la primera línea.  
- Usar etiquetas en minúscula.  
- Cerrar todas las etiquetas.  
- Atributos en minúscula y siempre entre comillas dobles.  
- Todas las imágenes deben incluir `alt`, `width` y `height`.  
- Evitar espacios innecesarios en atributos.  

```html
<!-- Declaración del tipo de documento -->
<!DOCTYPE html>

<!-- Uso de etiquetas en minúscula -->
<section>
  <p>This is a paragraph.</p>
</section>

<!-- Atributos en minúscula y entre comillas -->
<div class="menu"></div>

<!-- Imagen con alt, width y height -->
<img src="logo.png" alt="Company Logo" width="128" height="128" />

<!-- Evitar espacios innecesarios en atributos -->
<link rel="stylesheet" href="style.css" />
 ```

#### CSS

- Se adopta la metodología BEM (Block, Element, Modifier).

- Indentar con 2 espacios.

- Evitar IDs, preferir clases.

```html

/* Block */
.card {
  background-color: #eee; /* Fondo gris claro */
}

/* Element */
.card__title {
  color: #111; /* Texto oscuro */
}

/* Modifier */
.card--dark {
  background-color: #111; /* Fondo oscuro */
}


 ```

#### JavaScript

- Basado en las guías de MDN y W3C.

- Usar comillas simples ' '.

- Llaves de apertura en la misma línea.

- Punto y coma obligatorio.

- Arrow functions para callbacks.

- Constantes en UPPER_CASE_SNAKE_CASE.

 ``` html

// Saludo de ejemplo
const greeting = 'Hello World';

// Condición con llaves en la misma línea
if (true) {
  console.log('Valid');
}

// Arrow function
const sum = (a, b) => a + b;

// Constante global
const API_URL = 'https://api.hostelmanager.com';


 ```

#### VUE (FRONTEND)

- Componentes y clases: PascalCase.

- Interfaces: prefijo I.

- Servicios: sufijo Service.

- Módulos/Stores: PascalCase.

- Props y variables: camelCase.

```html 
<template>
  <!-- Sección principal de reservas -->
  <section class="booking">
    <!-- Mostrar el ID de reserva -->
    <h2>Booking ID: {{ reservationId }}</h2>

    <!-- Botón que confirma la reserva -->
    <button @click="confirmBooking">Confirm</button>
  </section>
</template>

<script setup lang="ts">
// Importación de ref para variables reactivas
import { ref } from 'vue'
import { BookingService } from '@/services/BookingService'

// Variable reactiva que almacena el ID de reserva
const reservationId = ref<number>(0)

// Instancia del servicio de reservas
const bookingService = new BookingService()

// Método que confirma la reserva usando el servicio
const confirmBooking = (): void => {
  bookingService.confirm(reservationId.value)
}
</script>

<style scoped>
/* Estilos locales para el componente Booking */
.booking {
  padding: 1rem; /* Espaciado interno */
}
</style>
```


#### Java (Backend)

- Paquetes: lowercase.

- Clases: PascalCase.

- Métodos y variables: camelCase.

- Constantes: UPPER_CASE.

- Apertura de llaves en la misma línea.

- Usar final para constantes inmutables.

- Manejar excepciones solo cuando sea necesario.

```html

// Clase Reservation que representa una reserva
public class Reservation {
    // Nombre del huésped
    private String guestName;

    // Número de habitación
    private int roomNumber;

    /**
     * Método que confirma la reserva.
     * Ejemplo de uso de Javadoc para documentación.
     */
    public void confirmBooking() {
        System.out.println("Booking confirmed");
    }
}


```


### 5.1.4. Software Deployment Configuration



#### Estrategia de Despliegue

La estrategia de despliegue se realizará considerando cada componente del sistema:

#### Landing Page
- **Hospedaje:** GitHub Pages o Vercel.  
- **Proceso:**
  1. Push en rama `main`.
  2. GitHub Actions ejecuta build automático.
  3. Publicación automática en URL de producción.

#### Frontend Web Application (Vue)
- **Hospedaje:** Vercel o Netlify.  
- **Proceso:**
  1. Merge a `main` desde `develop`.
  2. Pipeline CI/CD ejecuta `npm run build`.
  3. Despliegue automático en entorno productivo.

#### Backend (RESTful API en Node.js)
- **Hospedaje:** Heroku, Render o AWS EC2.  
- **Proceso:**
  1. Pipeline en CI/CD compila y ejecuta pruebas.
  2. Despliegue de contenedor **Docker** en servidor.
  3. Base de datos conectada a **PostgreSQL** en AWS RDS o ElephantSQL.

#### Base de Datos
- **Motor:** PostgreSQL desplegado en entorno cloud (AWS RDS o ElephantSQL).  
- **Migraciones:** Administradas con **Sequelize** o **TypeORM**.

#### Notificaciones y Servicios Externos
- **Integraciones:** Stripe, PayPal, MercadoPago, WhatsApp Cloud API.  
- **Seguridad:** Variables sensibles gestionadas mediante `.env` y **GitHub Secrets**.



## 5.2. Landing Page, Services & Applications Implementation
### 5.2.1. Sprint 1

El primer sprint es un hito importante en nuestro proceso de desarrollo ágil. Durante este período, nos enfocamos en la implementación de las características y funcionalidades prioritarias identificadas en la planificación inicial. Esto implica traducir los requisitos y especificaciones en código funcional, desarrollando las bases de nuestro producto de manera iterativa.

#### 5.2.1.1. Sprint Planning 1

El sprint planning es una reunión en la metodología ágil donde el equipo planifica las actividades del próximo sprint. Define qué trabajo se hará, cuánto tiempo tomará y quién será responsable. El objetivo es establecer un plan claro y alcanzable para el equipo, fomentando la colaboración y asegurando que todos estén alineados en cuanto a objetivos y prioridades.

<table  style="text-align: center;">
    <tbody>
        <tr>
			<td colspan="1">Sprint #</td>
            <td colspan="1"> Sprint 1  </td>
		</tr>
        <tr>
			<td colspan="2">Sprint Planning Background </td>
		</tr>
        <tr>
			<td colspan="1">Date</td>
            <td colspan="1"> 2025-09-21 </td>
		</tr>
        <tr>
			<td colspan="1">Time</td>
            <td colspan="1"> 11:00 PM </td>
		</tr>
        <tr>
			<td colspan="1">Location</td>
            <td colspan="1">Microsoft Teams (Reunion virtual)</td>
		</tr>
        <tr>
			<td colspan="1">Prepared By</td>
            <td colspan="1">Janampa Gutierrez, Jhoan Darner</td>
		</tr>
        <tr>
			<td colspan="1"> Attendees (to planning meeting)</td>
            <td colspan="1">Bautista Rivera, Jose Diego // Curi Marcelo, Angelo Marcio //  Janampa Gutierrez, Jhoan Darner // Quiroz Caceres, Adrian Alonso // Velarde Gonzales, Nestor Hernan </td>
		</tr>
         <tr>
			<td colspan="1">Sprint 1 – 1 Review Summary </td>
            <td colspan="1">En el Sprint 1 se definieron el alcance general del proyecto y los objetivos principales que guiarán el desarrollo del MVP. Se realizaron los wireframes tanto para la landing page como para el frontend, permitiendo establecer una visión clara del diseño y la experiencia de usuario. Además, se completó el despliegue de la landing page, dejándola operativa en el entorno de producción. Este sprint sentó las bases visuales y estratégicas del proyecto, alineando al equipo en torno a una misma dirección.</td>
		</tr>
         <tr>
			<td colspan="1">Sprint 1 – 1 Retrospective Summary </td>
            <td colspan="1">Durante este Sprint 1 se presentaron dificultades en la organización y gestión del tiempo, lo que representó un desafío para el equipo. Sin embargo, a pesar de estos inconvenientes, se logró completar el trabajo dentro del plazo establecido. Este resultado dejó en evidencia la necesidad de mejorar la planificación y coordinación interna, aspectos que se abordarán con mayor atención en los próximos sprints para optimizar la eficiencia y el trabajo en equipo."</td>
		</tr>
         <tr>
			<td colspan="2">Sprint Goal & User Stories </td>
		</tr>
         <tr>
			<td colspan="1">Sprint 1 Goal</td>
            <td colspan="1">En este Sprint se cumplieron los objetivos planteados, entre los que se incluyeron la definición del alcance, propósito y objetivos del proyecto. Además, se logró desplegar correctamente la landing page desde el repositorio, asegurando su funcionamiento sin inconvenientes. También se completó el diseño inicial para el frontend, lo que sienta una base visual sólida para el desarrollo posterior."</td>
		</tr>
        <tr>
			<td colspan="1">Sprint 1 Velocity </td>
            <td colspan="1">Para este sprint se han elegido 7 User Stories.</td>
		</tr>
        <tr>
			<td colspan="1">Sum of Story Points </td>
            <td colspan="1">35</td>
		</tr>
</tbody>
</table>

#### 5.2.1.2. Aspect Leaders and Collaborators

La tabla Aspect Leaders and Collaborators es una herramienta de gestión esencial que proporciona una visión clara y concisa de las responsabilidades individuales dentro del equipo en relación con los diversos aspectos del Sprint.

| Team Member (Last Name, First Name) | GitHub Username    | Landing Page (L/C) | Front-End Prototype (L/C) | Documentation (L/C) |
|---|---|---|---|---|
| Bautista Rivera, Jose Diego | Gogotes17 | C | C |  L |
| Curi Marcelo, Angelo Marcio | AngeloC999 | - | C |  C |
| Janampa Gutierrez, Jhoan Darner | orraiAKBDFSK | L | - |  C |
| Quiroz Caceres, Adrian Alonso | Aqc1019 | C | C | C  |
| Velarde Gonzales, Nestor Hernan | VelardeSoft | L | L | C  |

#### 5.2.1.3. Sprint Backlog 1

En este primer sprint, nos enfocamos en la implementación de la Landing Page del sistema, abarcando la estructura general, el diseño visual y la navegación básica. Además, se trabajó en el prototipo visual del frontend, permitiendo validar las principales funcionalidades desde la perspectiva del usuario.

### Sprint Backlog 1 - Entregables: Landing Page + Prototipo Web

| # | User Story ID | Título                       | Prioridad | Story Points | Estado     |
|---|---------------|------------------------------|-----------|--------------|------------|
| 1 | US25          | Información en landing page  | Alta      | 3            | Hecho      |
| 2 | US26          | Registro rápido en landing   | Media     | 5            | Hecho      |
| 3 | US27          | Formulario de contacto       | Media     | 3            | Hecho      |
| 4 | US28          | Visualizar planes y precios  | Alta      | 3            | Hecho      |
| 5 | US01          | Buscar disponibilidad        | Alta      | 5            | Prototipo  |
| 6 | US02          | Crear reserva                | Alta      | 8            | Prototipo  |
| 7 | US05          | Reserva en línea             | Alta      | 8            | Prototipo  |
| 8 | -             | Documentación del Sprint     | Media     | 3  | Hecho      |
| 9 | -             | Despliegue de Landing Page   | Alta      | 3  | Hecho      |


#### 5.2.1.4. Development Evidence for Sprint Review

En esta sección se explican y presentan los avances de implementación en relación con la solución desarrollada, según el alcance definido para el sprint. En esta iteración, se completó la implementación de la Landing Page en su totalidad.

| Repository | Branch | Commit ID | Commit Message | Commit Message Body | Commited on (Date) |
| ---------- | ------ | --------- | -------------- | ------------------- | ------------------ |
|upc-pre-202520-1asi0730-7429-CodeLab/LandingPage|main|74c53d5|Initial commit|-|17/09/2025|
|upc-pre-202520-1asi0730-7429-CodeLab/LandingPage|main|ca89c80|feat: Add style in the project|-|17/09/2025|
|upc-pre-202520-1asi0730-7429-CodeLab/LandingPage|main|2925f46|feat: Add functional in Javascript|-|17/09/2025|
|upc-pre-202520-1asi0730-7429-CodeLab/LandingPage|main|4bab0b8|feat: Add interfaces in html|-|17/09/2025|
|upc-pre-202520-1asi0730-7429-CodeLab/LandingPage|main|aad5c44|feat: upgrade landing page style.|-|20/09/2025|



#### 5.2.1.5. Execution Evidence for Sprint Review

Para este sprint, se logró implementar y desplegar correctamente la Landing Page de la aplicación, cumpliendo con el diseño y los requerimientos establecidos para la plataforma web del negocio. A continuación, se presentan capturas de las vistas implementadas correspondientes a esta sección.

<img src="images/Lan1.jpg">
<img src="images/Lan2.jpg">
<img src="images/Lan3.jpg">


#### 5.2.1.6. Services Documentation Evidence for Sprint Review

En esta sección se muestra la ejecución funcional de la landing page, junto con los wireframes y mockups correspondientes al diseño del frontend. Esto permite visualizar el resultado actual y compararlo con las etapas previas de diseño para validar la coherencia entre la planificación y la implementación.

<img src="images/evidenceDoc.jpg">

<img src="images/evidenceDoc2.jpg">

#### 5.2.1.7. Software Deployment Evidence for Sprint Review

Para realizar el despligue de la landing page, se utilizó la herramienta Github Pages el cuál permite desplegar páginas estáticas de forma sencilla y veloz. Además, proporciona un pipeline de CI/CD que permite desplegar a producción cada vez que se realiza un commit en la rama 'main'. 

Landing Page: https://aqc1019.github.io/#hero

<img src="images/evidence.jpg">

#### 5.2.1.8. Team Collaboration Insights during Sprint

Esta sección proporciona una visión detallada sobre cómo colaboró el equipo durante el desarrollo del sprint.

<img src="images/Insig.jpg">

### 5.2.2. Sprint 2

El Sprint 2 ha sido un hito crucial en nuestro desarrollo ágil, enfocado en establecer las herramientas fundamentales para la gestión tanto administrativa como de usuario. Durante este periodo, logramos implementar las funcionalidades operativas clave para el Administrador de Hoteles: se habilitó la creación de hoteles y habitaciones, sentando las bases del inventario, se completó la creación de su cuenta de acceso y se integró la función de verificación de reservas, dándole visibilidad inmediata sobre la ocupación. Paralelamente, para los Clientes, integramos las funcionalidades de creación de cuenta, la visualización de hoteles y habitaciones disponibles, y la reserva de habitaciones.

#### 5.2.2.1. Sprint Planning 2

El sprint planning es una reunión en la metodología ágil donde el equipo planifica las actividades del próximo sprint. Define qué trabajo se hará, cuánto tiempo tomará y quién será responsable. El objetivo es establecer un plan claro y alcanzable para el equipo, fomentando la colaboración y asegurando que todos estén alineados en cuanto a objetivos y prioridades.

<table style="text-align: center;">
    <tbody>
        <tr>
            <td colspan="1">Sprint #</td>
            <td colspan="1"> Sprint 2 </td>
        </tr>
        <tr>
            <td colspan="2">Sprint Review Background</td>
        </tr>
        <tr>
            <td colspan="1">Date</td>
            <td colspan="1"> 2025-10-09 </td>
        </tr>
        <tr>
            <td colspan="1">Time</td>
            <td colspan="1"> 11:00 PM </td>
        </tr>
        <tr>
            <td colspan="1">Location</td>
            <td colspan="1">Microsoft Teams (Reunión virtual)</td>
        </tr>
        <tr>
            <td colspan="1">Prepared By</td>
            <td colspan="1">Velarde Gonzales, Nestor Hernan</td>
        </tr>
        <tr>
            <td colspan="1">Attendees (to review meeting)</td>
            <td colspan="1">Bautista Rivera, Jose Diego // Curi Marcelo, Angelo Marcio // Janampa Gutierrez, Jhoan Darner // Quiroz Caceres, Adrian Alonso // Velarde Gonzales, Nestor Hernan </td>
        </tr>
        <tr>
            <td colspan="1">Sprint 2 – Final Summary of Work Done</td>
            <td colspan="1">Este Sprint 2 se dedicó por completo a la **construcción y despliegue del *frontend***, creando la primera capa de interacción para nuestros usuarios clave. Se consolidaron las herramientas de **gestión hotelera** para el Administrador, implementando el flujo de **creación de hoteles y habitaciones**, además del control de acceso mediante la **creación de su cuenta**, la capacidad de **monitorear las reservas** y la integración de la gestión de **suscripciones disponibles**. Simultáneamente, se lanzó el ciclo de vida del **Cliente**, que ahora puede **registrar su cuenta**, **navegar por el inventario disponible** y **completar el proceso de reserva** de habitaciones.</td>
        </tr>
        <tr>
            <td colspan="1">Sprint 2 – Achieved Goal</td>
            <td colspan="1">Puesta en marcha de la interfaz de usuario funcional, validando y entregando el conjunto esencial de *User Stories* para la administración de inventario, gestión de suscripciones y la interacción completa del cliente.</td>
        </tr>
        <tr>
            <td colspan="1">Sprint 2 – Work Completed</td>
            <td colspan="1">7 User Stories (Ejecutadas).</td>
        </tr>
        <tr>
            <td colspan="1">Sum of Story Points Completed</td>
            <td colspan="1">35</td>
        </tr>
    </tbody>
</table>

#### 5.2.2.2. Aspect Leaders and Collaborators

La tabla Aspect Leaders and Collaborators es una herramienta de gestión esencial que proporciona una visión clara y concisa de las responsabilidades individuales dentro del equipo en relación con los diversos aspectos del Sprint.

| Team Member (Last Name, First Name) | GitHub Username    | Landing Page (L/C) | Front-End Prototype (L/C) | Documentation (L/C) |
|---|---|---|---|---|
| Bautista Rivera, Jose Diego | Gogotes17 | C | C |  L |
| Curi Marcelo, Angelo Marcio | AngeloC999 | - | C |  C |
| Janampa Gutierrez, Jhoan Darner | orraiAKBDFSK | L | - |  C |
| Quiroz Caceres, Adrian Alonso | Aqc1019 | C | C | C  |
| Velarde Gonzales, Nestor Hernan | VelardeSoft | L | L | C  |

#### 5.2.2.3. Sprint Backlog 1

En este primer sprint, nos enfocamos en la implementación de la Landing Page del sistema, abarcando la estructura general, el diseño visual y la navegación básica. Además, se trabajó en el prototipo visual del frontend, permitiendo validar las principales funcionalidades desde la perspectiva del usuario.

### Sprint Backlog 1 - Entregables: Landing Page + Prototipo Web

| # | User Story ID | Título                       | Prioridad | Story Points | Estado     |
|---|---------------|------------------------------|-----------|--------------|------------|
| 1 | US25          | Información en landing page  | Alta      | 3            | Hecho      |
| 2 | US26          | Registro rápido en landing   | Media     | 5            | Hecho      |
| 3 | US27          | Formulario de contacto       | Media     | 3            | Hecho      |
| 4 | US28          | Visualizar planes y precios  | Alta      | 3            | Hecho      |
| 5 | US01          | Buscar disponibilidad        | Alta      | 5            | Prototipo  |
| 6 | US02          | Crear reserva                | Alta      | 8            | Prototipo  |
| 7 | US05          | Reserva en línea             | Alta      | 8            | Prototipo  |
| 8 | -             | Documentación del Sprint     | Media     | 3  | Hecho      |
| 9 | -             | Despliegue de Landing Page   | Alta      | 3  | Hecho      |


#### 5.2.2.4. Development Evidence for Sprint Review

En esta sección se explican y presentan los avances de implementación en relación con la solución desarrollada, según el alcance definido para el sprint. En esta iteración, se completó la implementación de la Landing Page en su totalidad.

| Repository | Branch | Commit ID | Commit Message | Commit Message Body | Commited on (Date) |
| ---------- | ------ | --------- | -------------- | ------------------- | ------------------ |
|upc-pre-202520-1asi0730-7429-CodeLab/LandingPage|main|74c53d5|Initial commit|-|17/09/2025|
|upc-pre-202520-1asi0730-7429-CodeLab/LandingPage|main|ca89c80|feat: Add style in the project|-|17/09/2025|
|upc-pre-202520-1asi0730-7429-CodeLab/LandingPage|main|2925f46|feat: Add functional in Javascript|-|17/09/2025|
|upc-pre-202520-1asi0730-7429-CodeLab/LandingPage|main|4bab0b8|feat: Add interfaces in html|-|17/09/2025|
|upc-pre-202520-1asi0730-7429-CodeLab/LandingPage|main|aad5c44|feat: upgrade landing page style.|-|20/09/2025|



#### 5.2.2.5. Execution Evidence for Sprint Review

Para este sprint, se logró implementar y desplegar correctamente la Landing Page de la aplicación, cumpliendo con el diseño y los requerimientos establecidos para la plataforma web del negocio. A continuación, se presentan capturas de las vistas implementadas correspondientes a esta sección.

<img src="images/Lan1.jpg">
<img src="images/Lan2.jpg">
<img src="images/Lan3.jpg">


#### 5.2.2.6. Services Documentation Evidence for Sprint Review

En esta sección se muestra la ejecución funcional de la landing page, junto con los wireframes y mockups correspondientes al diseño del frontend. Esto permite visualizar el resultado actual y compararlo con las etapas previas de diseño para validar la coherencia entre la planificación y la implementación.

<img src="images/evidenceDoc.jpg">

<img src="images/evidenceDoc2.jpg">

#### 5.2.2.7. Software Deployment Evidence for Sprint Review

Para realizar el despligue de la landing page, se utilizó la herramienta Github Pages el cuál permite desplegar páginas estáticas de forma sencilla y veloz. Además, proporciona un pipeline de CI/CD que permite desplegar a producción cada vez que se realiza un commit en la rama 'main'. 

Landing Page: https://aqc1019.github.io/#hero

<img src="images/evidence.jpg">

#### 5.2.2.8. Team Collaboration Insights during Sprint

Esta sección proporciona una visión detallada sobre cómo colaboró el equipo durante el desarrollo del sprint.

<img src="images/Insig.jpg">



# Conclusiones

##### Establecimiento de la base visual del producto:
- La implementación de la **Landing Page** permitió crear una primera versión pública del sistema, que comunica la propuesta de valor a potenciales usuarios y clientes.
- Se logró un diseño visual claro, funcional y alineado con los objetivos del negocio.

##### Avance en la conceptualización del sistema:
- A través de los **prototipos del Front-End**, se validaron las vistas principales que compondrán el sistema, facilitando el entendimiento del flujo de usuario.
- Estos prototipos servirán como guía para el desarrollo funcional en los próximos sprints.

##### Organización y documentación inicial:
- Se documentó el **ciclo de vida del software** y se registraron las actividades realizadas durante el sprint, lo cual fortalece la planificación futura y la trazabilidad del proyecto.
- Esta base documental permite al equipo mantener claridad sobre los objetivos y decisiones técnicas adoptadas.

##### Despliegue exitoso del primer entregable:
- La **Landing Page** fue publicada en un entorno accesible públicamente, lo que permite mostrar el progreso del equipo de forma tangible a los stakeholders.


# Bibliografía

# Anexos


