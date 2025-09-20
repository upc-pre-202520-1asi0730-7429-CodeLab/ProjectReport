
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



### 5.1.4. Software Deployment Configuration

A continuación se mencionan las convenciones y guías de estilo adoptadas para el desarrollo del proyecto **HostelManager**, siguiendo lineamientos internacionales y buenas prácticas de codificación.  
Toda la nomenclatura será escrita en **inglés**, independientemente del lenguaje utilizado.  

El proyecto se desarrollará en tres entornos principales:  
- **Visual Studio Code** para la Landing Page (HTML, CSS y JavaScript).  
- **WebStorm** para el frontend en **Vue/TypeScript**.  
- **JetBrains IntelliJ IDEA** para el backend en **Node.js/Java**.  


## HTML
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
