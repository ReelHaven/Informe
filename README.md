# Universidad Peruana De Ciencas Aplicadas

## Open Source SW51

![LOGO](logo_upc.png)

## "Informe de Trabajo Final"

## ReelHaven - MindFlix

## Profesor: Hugo Allan Mori Paiva

## Integrantes:

* ### 1 Piero Miranda
* ### 2 Sebastian De Las Casas
* ### 3 Gabriel Lapa
* ### 4 Niurka Huarcaya
* ### 5 Johan Bottger

-----

## Registro de Versiones Del Informe

| Version | Fecha    | Autor        | Descripcion de modificacion       |
|---------|----------|--------------|-----------------------------------|
|         |          |              |                                   |  
|         |          |              |                                   |
|         |          |              |                                   |
|         |          |              |                                   |
|         |          |              |                                   |
|         |          |              |                                   |
|         |          |              |                                   |


## Project Report Collaboration Insights 






------

## Contenido

#### Capitulo I: Introducción

- [1.1. Startup Profile](#11-startup-profile)
    - [1.1.1. Descripción de la Startup](#111-descripción-de-la-startup)
    - [1.1.2. Perfiles de Integrantes del equipo](#112-perfiles-de-integrantes-del-equipo)
- [1.2. Solution Profile](#12-solution-profile)
    - [1.2.1. Antecedentes y problematica](#121-antecedentes-y-problematica)
    - [1.2.2. Lean UX Process](#122-lean-ux-process)
        - [1.2.2.1. Lean UX Problem Statements](#1221-lean-ux-problem-statements)
        - [1.2.2.2. Lean UX Assumptions](#1222-lean-ux-assumptions)
        - [1.2.2.3. Lean UX Hypothesis Statements](#1223-lean-ux-hypothesis-statements)
        - [1.2.2.4. Lean UX Canvas](#1224-lean-ux-canvas)
- [1.3. Segmentos Objetivos](#13-segmentos-objetivos)

#### Capitulo II: Requirements Elicitation & Analysis

- [2.1. Competidores](#21-competidores)
    - [2.1.1. Análisis Competitivo](#211-análisis-competitivo)
    - [2.1.2. Estrategias y Tácticas Frente a Competidores](#212-estrategias-y-tácticas-frente-a-competidores)
- [2.2. Entrevistas](#22-entrevistas)
    - [2.2.1. Diseño de Entrevistas](#221-diseño-de-entrevistas)
    - [2.2.2. Registro de Entrevistas](#222-registro-de-entrevistas)
    - [2.2.3. Análisis de Entrevistas](#223-análisis-de-entrevistas)
- [2.3. Needfinding](#23-needfinding)
    - [2.3.1. User Personas](#231-user-personas)
    - [2.3.2. User Task Matrix](#232-user-task-matrix)
    - [2.3.3. User Journey Mapping](#233-user-journey-mapping)
    - [2.3.4. Empathy Mapping](#234-empathy-mapping)
    - [2.3.5. As-is Scenario Mapping](#235-as-is-scenario-mapping)

#### Capitulo III: Requirements Specification

- [3.1. To-Be Scenario Mapping](#31-to-be-scenario-mapping)
- [3.2. User Stories](#32-user-stories)
- Las User Stories, o historias de usuario, son descripciones breves y centradas en el usuario de una funcionalidad específica del producto. Nos ayudan a comprender las necesidades y expectativas de nuestros usuarios al abordar qué quieren lograr y por qué. Al escribir User Stories, nos centramos en el valor que proporcionará la funcionalidad para el usuario y en cómo la utilizará en su contexto. Esto nos permite priorizar las características del producto de acuerdo con su importancia para el usuario y desarrollar soluciones que realmente resuelvan sus problemas y satisfagan sus necesidades.
Para elaborar user stories que pertenecen a un epic. A continuación, las epics que consideramos como equipo:

| Código | Título | Epic |
|--------|--------|------|
|EP01 | Gestión de cuentas | Como usuario quiero poder gestionar mi cuenta, para cambiar y actualizar la información de la misma, así como mis preferencias y ajustes de privacidad.
|EP02|Visualización de User Interface|Como usuario de la plataforma, quiero poder ver la interfaz de usuario del landing page y la plataforma, para explorar todas las funcionalidades disponibles y entender cómo interactuar con la plataforma.
|EP03|Interacción con la plataforma|Como usuario quiero poder interactuar con la plataforma para crear, editar o eliminar mi contenido, e interactuar con otros usuarios.
|EP04|Desarrollo de funcionalidades principales|Como equipo de desarrollo quiero implementar las funcionalidades básicas, para establecer una base sólida donde poder desarrollar nuevas características.
|EP05|Funcionalidad del Landing Page de la plataforma|Como usuario quiero poder utilizar las diferentes características de la plataforma en su landing page para conocer información y detalles de la misma

A continuación, la realización de los user stories con sus criterios de aceptación con escenarios e ID de Épica:

| ID User Story | Título | Descripción | Criterios de aceptación | ID Epic |
|---------------|--------|-------------|-------------------------|---------|
|US01|Iniciar sesión|Como usuario registrado, quiero poder iniciar sesión en mi cuenta, para utilizar las funciones disponibles de la plataforma.|Happy Path: Given el usuario tiene credenciales válidas.<br>Then el usuario accede a la plataforma con su usuario.<br>When el usuario ingresa sus credenciales válidas y presiona "Iniciar sesión".<br>Unhappy Path: Given el usuario tiene credenciales inválidas.<br>When el usuario ingresa credenciales inválidas y presiona "Iniciar sesión".<br>Unhappy Path: Given el usuario no tiene una cuenta.<br>When el usuario intenta iniciar sesión sin estar registrado.<br>Then el sistema muestra un mensaje de error junto con un enlace para registrarse.|EP01|
|US02|Recuperar Contraseña|Como usuario de la plataforma, Quiero poder recuperar mi contraseña olvidada, Para poder acceder nuevamente a mi cuenta.	|Happy Path: Given el usuario ha olvidado su contraseña.<br>When el usuario solicita restablecer la contraseña.<br>Then el sistema envía un correo electrónico con un enlace de restablecimiento.<br>Unhappy Path: Given el usuario no ha olvidado su contraseña.<br>When el usuario intenta restablecerla sin haber olvidado la contraseña.<br>Then el sistema muestra un mensaje indicando que la contraseña es incorrecta.<br>Unhappy Path: Given el usuario no tiene una cuenta.<br>When el usuario intenta restablecer la contraseña sin estar registrado.<br>Then el sistema muestra un mensaje indicando que la cuenta no existe.|EP01|
|US03|Actualizar Información Personal|Como usuario registrado, Quiero poder actualizar mi información personal en mi perfil, Para mantenerla actualizada y precisa.| Happy Path: Given que el usuario desea cambiar su información personal.<br>When el usuario realiza cambios en su perfil y guarda.<br>Then el sistema actualiza la información en la base de datos.<br>Unhappy Path: Given que el usuario intenta guardar información inválida.<br>When el usuario intenta guardar cambios con campos obligatorios vacíos.<br>Then el sistema muestra un mensaje indicando los campos obligatorios.<br>Unhappy Path: Given que el usuario desea eliminar su foto de perfil.<br>When el usuario elimina la foto y guarda los cambios.<br>Then el sistema elimina la foto de perfil y actualiza la información en la base de datos.| EP01|
|US04|Filtrar Contenido por Categoría|Como usuario, Quiero poder filtrar el contenido por categoría, Para encontrar información relevante más fácilmente.|Happy Path: Given que el usuario desea ver contenido específico.<br>When el usuario selecciona una categoría de filtrado.<br>Then la plataforma muestra solo el contenido de esa categoría.<br>Unhappy Path: Given que el usuario intenta filtrar contenido con una categoría no existente.<br>When el usuario selecciona una categoría inexistente.<br>Then la plataforma no muestra ningún contenido y muestra un mensaje informativo.<br>Unhappy Path: Given que el usuario intenta filtrar contenido sin seleccionar ninguna categoría.<br>When el usuario intenta aplicar un filtro sin seleccionar una categoría.<br>Then la plataforma no realiza cambios y muestra un mensaje informativo.<br>|EP02|
|US05|Dar “Me Gusta” a contenido|Como usuario de la plataforma, Quiero poder dar "Me Gusta" al contenido de otros usuarios, Para mostrar aprecio por el contenido.|Happy Path: Given que el usuario ve una publicación que le gusta.<br>When el usuario hace clic en el botón "Me Gusta".<br>Then el sistema incrementa el contador de "Me Gusta" en la publicación.<br>Unhappy Path: Given que el usuario intenta dar "Me Gusta" a una publicación ya gustada.<br>When el usuario intenta dar "Me Gusta" a una publicación que ya ha sido gustada por él.<br>Then el sistema no realiza cambios en el contador de "Me Gusta".<br>Unhappy Path: Given que el usuario intenta dar "Me Gusta" a una publicación sin estar autenticado.<br>When el usuario intenta dar "Me Gusta" a una publicación sin haber iniciado sesión.<br>Then el sistema redirige al usuario a la página de inicio de sesión.<br>|EP03|
|US06|Compartir publicaciones|Como usuario, Quiero poder compartir publicaciones en mis redes sociales, Para compartir contenido interesante con otros.|Happy Path: Given que el usuario desea compartir una publicación.<br>When el usuario hace clic en el botón de compartir y selecciona una red social.<br>Then el sistema abre la página de la red social seleccionada.<br>Unhappy Path: Given que el usuario intenta compartir una publicación sin seleccionar una red social.<br>When el usuario intenta compartir una publicación sin seleccionar una red social.<br>Then el sistema muestra un mensaje indicando que se debe seleccionar una red social.<br>Unhappy Path: Given que el usuario intenta compartir una publicación sin estar autenticado.<br>When el usuario intenta compartir una publicación sin haber iniciado sesión.<br>Then el sistema redirige al usuario a la página de inicio de sesión.<br>|EP03|
|TS070|Configurar Entorno de Desarrollo|Como desarrollador, Quiero configurar mi entorno de desarrollo local, Para poder comenzar a trabajar en el proyecto.|Happy Path: Given que el desarrollador necesita configurar su entorno de desarrollo.<br>When el desarrollador sigue las instrucciones de configuración.<br>Then el entorno de desarrollo local se configura correctamente y está listo para trabajar.<br>Unhappy Path: Given que el desarrollador no sigue las instrucciones de configuración.<br>When el desarrollador no completa la configuración correctamente.<br>Then el entorno de desarrollo local no está listo para trabajar y se muestra un mensaje de error.<br>|EP04|
|TS08|Implementar Funcionalidad Esencial|Como desarrollador, Quiero implementar la funcionalidad esencial del sistema, Para tener una base funcional sobre la cual construir.|Happy Path: Given que el desarrollador necesita implementar la funcionalidad esencial.<br>When el desarrollador sigue el diseño y las especificaciones.<br>Then la funcionalidad esencial se implementa correctamente y pasa las pruebas de unidad.<br>Unhappy Path: Given que el desarrollador intenta implementar la funcionalidad sin tener especificaciones claras.<br>When el desarrollador procede sin una guía clara.<br>Then la implementación es incorrecta y se requiere revisión.<br>|EP04|
|US09|Visualización de contenido|Como usuario quiero poder seleccionar contenido, Para poder visualizarlo en su entereza.|Happy Path: Given que el usuario con conexión a la red desea consumir contenido en la plataforma.<br>When el usuario selecciona uno de los medios audiovisuales.<br>Then el medio audiovisual se empezará a reproducir en su pantalla.<br>Unhappy Path: Given que el usuario sin conexión a la red desea consumir contenido en la plataforma.<br>When el usuario selecciona uno de los medios audiovisuales.<br>Then el medio audiovisual no se empezará a reproducir en su pantalla.<br>|EP04|
|US10|Ver lista de recomendaciones|Como usuario quiero poder acceder a una lista de recomendaciones Para visualizar contenido basado en mis gustos.|Happy Path: Given que el usuario desea ver su lista de recomendaciones.<br>When el usuario selecciona la pestaña recomendaciones.<br>Then la lista de recomendaciones basada en sus gustos aparecerá.<br>Unhappy Path: Given que el usuario desea ver su lista de recomendaciones sin haber establecido sus gustos.<br>When el usuario selecciona la pestaña recomendaciones.<br>Then la lista de recomendaciones basada en sus gustos aparecerá vacía.<br>|EP02|
|US11|Unirse a comunidades|Como usuario quiero poder unirme a comunidades Para compartir mis gustos y opiniones con otros usuarios.|Happy Path: Given el usuario quiere unirse a una comunidad.<br>When el usuario encuentre una comunidad y le de click a l botón unirse.<br>Then el usuario se unirá a la comunidad y podrá interactuar con otros usuarios dentro de la misma.<br>Unhappy Path: Given el usuario quiere unirse a una comunidad sin cumplir los requisitos.<br>When el usuario encuentre una comunidad y le de click a l botón unirse.<br>Then el usuario se unirá a la comunidad y podrá interactuar con otros usuarios dentro de la misma.<br>|EP03|
|US12|Visualizar contenido en tamaño de dispositivo|Como usuario quiero poder acceder a la landing page desde dispositivos de cualquier tamaño Para visualizarla de manera efectiva.|Happy Path: Given el usuario quiere acceder desde un dispositivo con tamaño soportado por la plataforma<br>When el usuario accede a la landing page<br>Then el usuario visualizará la landing page sin problemas<br>Unhappy Path: Given el usuario quiere acceder desde un dispositivo con tamaño no soportado por la plataforma<br>When el usuario accede a la landing page<br>Then el usuario no podrá visualizar la landing page de manera cómoda o efectiva.<br>|EP05|
|US13|Saber los beneficios ofrecidos|Como usuario quiero poder acceder a una página dentro de la landing page Para que me explique los servicios ofrecidos.|Happy Path: Given el usuario está interesado conocer los beneficios ofrecidos.<br>When el usuario hace click en la pestaña de beneficios.<br>Then se muestran los beneficios que recibirá el usuario por el uso de la plataforma.<br>Unhappy Path: Given el usuario quiere conocer los beneficios ofrecidos.<br>When el usuario hace click en la pestaña de beneficios.<br>Then no se muestran los beneficios que recibirá el usuario por el uso de la plataforma.<br>|EP05|
|US14|Desplazar de forma efectiva por la web|Como usuario quiero poder desplazarme por la landing page de forma efectiva Para no confundirme y perder tiempo.|Happy Path: Given el usuario quiere desplazarse por la landing page.<br>When el usuario entre en la landing page.<br>Then el usuario se desplazará de forma intuitiva por la landing page.<br>Unhappy Path: Given  el usuario quiere desplazarse por la landing page mal organizada.<br>When el usuario entre en la landing page.<br>Then el usuario no podrá desplazarse por la página debido a su mala organización.<br>|EP05|
|US15|Contar con información de contacto|Como usuario quiero poder contar con información de contacto Para comunicarme en caso tenga una consulta.|Happy Path: Given el usuario quiere acceder a la información de contacto.<br>When el usuario haga click en la pestaña “Contáctanos”.<br>Then el usuario se encontrará con toda la información de contacto del equipo desarrollador.<br>Unhappy Path: Given el usuario quiere acceder a la información de contacto.<br>When el usuario haga click en la pestaña “Contáctanos”.<br>Then el usuario no encontrará la información de contacto del equipo desarrollador.<br>|EP05|
|US16|Redes sociales|Como usuario quiero encontrar las redes sociales de la plataforma Para conocer más sobre sus planes y decisiones.|Happy Path: Given el usuario quiere ver las redes sociales de la plataforma.<br>When el usuario haga click en los iconos de la respectiva red en la landing page.<br>Then el usuario será redireccionado a las páginas de la red social de la plataforma.<br>Unhappy Path: Given el usuario quiere ver las redes sociales de la plataforma.<br>When el usuario haga click en los iconos de la respectiva red en la landing page.<br>Then el usuario no será redireccionado a las páginas de la red social de la plataforma.<br>|EP05|
|US17|Conocer las membresías|Como usuario quiero acceder a la información de las membresías desde la landing page Para tomar una decisión informada.|Happy Path: Given el usuario quiere conocer las membresías disponibles.<br>When el usuario haga click en la pestaña “membresías”.<br>Then se encontrará con toda la información de las membresías disponibles.<br>Unhappy Path: Given el usuario quiere conocer las membresías disponibles.<br>When el usuario haga click en la pestaña “membresías”.<br>Then no se encontrará con toda la información de las membresías disponibles.<br>|EP05|

- [3.3. Impact Mapping](#33-impact-mapping)
- Impact Mapping es una herramienta poderosa que nos ayudará a visualizar y planificar cómo nuestro proyecto puede generar un impacto significativo en nuestros usuarios y en nuestro objetivo final. Nos permitirá identificar claramente los resultados deseados, los comportamientos esperados de nuestros usuarios y las acciones necesarias para alcanzar esos objetivos. Al utilizar Impact Mapping, podremos alinear mejor nuestras actividades con nuestros objetivos, tomar decisiones más informadas y maximizar el impacto de nuestro proyecto.
  
![Impact map Mindflix1](https://github.com/user-attachments/assets/57a6eab9-ae70-4f41-a071-9a5156b81d16)

- [3.4. Product Backlog](#34-product-backlog)
  
| Orden | User Story ID | Título | Descripción | Story Points |
|-------|---------------|--------|-------------|--------------|
|1|US09|Visualización de contenido|Como usuario quiero poder seleccionar contenido, Para poder visualizarlo en su entereza.|5|
2|US06|Compartir publicaciones|Como usuario, Quiero poder compartir publicaciones en mis redes sociales, Para compartir contenido interesante con otros.	|5|
3|TS07|Configurar Entorno de Desarrollo|Como desarrollador, Quiero configurar mi entorno de desarrollo local, Para poder comenzar a trabajar en el proyecto.	|5|
4|TS08|Implementar Funcionalidad Esencial|Como desarrollador, Quiero implementar la funcionalidad esencial del sistema, Para tener una base funcional sobre la cual construir.	|3|
5|US04|Filtrar Contenido por Categoría|Como usuario, Quiero poder filtrar el contenido por categoría, Para encontrar información relevante más fácilmente.	|3|
6|US03|Actualizar Información Personal|Como usuario registrado, Quiero poder actualizar mi información personal en mi perfil, Para mantenerla actualizada y precisa.	|2|
7|US01|Iniciar sesión|Como usuario registrado, quiero poder iniciar sesión en mi cuenta, para utilizar las funciones disponibles de la plataforma.|3|
8|US02|Recuperar Contraseña|Como usuario de la plataforma, Quiero poder recuperar mi contraseña olvidada, Para poder acceder nuevamente a mi cuenta.	|2|
9|US05|Dar “Me Gusta” a contenido|Como usuario de la plataforma, Quiero poder dar "Me Gusta" al contenido de otros usuarios, Para mostrar aprecio por el contenido.|1|
10|US10|Ver lista de recomendaciones|Como usuario quiero poder acceder a una lista de recomendaciones Para visualizar contenido basado en mis gustos.|2|
11|US11|Unirse a comunidades|Como usuario quiero poder unirme a comunidades Para compartir mis gustos y opiniones con otros usuarios.|3|
12|US12|Visualizar contenido en tamaño de dispositivo|Como usuario quiero poder acceder a la landing page desde dispositivos de cualquier tamaño Para visualizarla de manera efectiva.|3|
13|US13|Saber los beneficios ofrecidos|Como usuario quiero poder acceder a una página dentro de la landing page Para que me explique los servicios ofrecidos.|2|
14|US14|Desplazar de forma efectiva por la web|Como usuario quiero poder desplazarme por la landing page de forma efectiva Para no confundirme y perder tiempo.|1|
15|US15|Contar con información de contacto|Como usuario quiero poder contar con información de contacto Para comunicarme en caso tenga una consulta.|1
16|US16|Redes sociales|Como usuario quiero encontrar las redes sociales de la plataforma Para conocer más sobre sus planes y decisiones.|2|
17|US17|Conocer las membresías|Como usuario quiero acceder a la información de las membresías desde la landing page Para tomar una decisión informada.|2|

#### Capitulo IV: Product  Design

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
    - [4.4.1. Web Application Wireframes](#441-web-application-wireframes)
    - [4.4.2. Web Application Wireflow Diagrams](#442-web-application-wireflow-diagrams)
    - [4.4.3. Web Application Mock-ups](#443-web-application-mock-ups)
    - [4.4.4. Web Application User Flow Diagrams](#444-web-application-user-flow-diagrams)
- [4.5. Web Applications Prototyping](#45-web-applications-prototyping)
- [4.6. Domain-Driven Software Architecture](#46-domain-driven-software-architecture)
- La arquitectura de software orientada al dominio es un enfoque de diseño que se centra en la estructura y organización del software en torno a los conceptos y procesos clave de un dominio específico. Este enfoque nos permite crear sistemas que reflejen con precisión los requisitos y la lógica del negocio, lo que facilita la implementación de funcionalidades específicas y la adaptación a los cambios en el dominio. Con MindFlix, utilizamos una arquitectura de software orientada al dominio para estructurar nuestro sistema de manera coherente y escalable, lo que nos permitirá desarrollar una aplicación robusta y fácil de mantener.
    - [4.6.1. Software Architecture Context Diagram](#461-software-architecture-context-diagram)
      
      ![structurizr-82724-SystemContext-001](https://github.com/user-attachments/assets/504962e6-59dd-4ff4-9866-f99d0e2b6c1d)
      
    - [4.6.2. Software Architecture Container Diagrams](#462-software-architecture-container-diagrams)
      
      ![structurizr-82724-Container-001](https://github.com/user-attachments/assets/e21413d0-a6e5-414f-b025-00936dbd77da)

    - [4.6.3. Software Architecture Components Diagrams](#463-software-architecture-components-diagrams)
    
      ![structurizr-82724-Component-001](https://github.com/user-attachments/assets/14320f16-0c71-4c96-a579-6faea98c21ce)
        
- [4.7. Software Object-Oriented Design](#47-software-object-oriented-design)
    - [4.7.1. Class Diagrams](#471-class-diagrams)
    - [4.7.2. Class Dictionary](#472-class-dictionary)
- [4.8. Database Design](#48-database-design)
    - [4.8.1. Database Diagram](#481-database-diagram)

#### Capitulo V: Product Implementation, Validation & Deployment
- [5.1. Software Configuration Management](#51-software-configuration-management)
    - [5.1.1. Software Development Environment Configuration](#511-software-development-environment-configuration)
    - [5.1.2. Source Code Management](#512-source-code-management)
    - [5.1.3. Source Code Style Guide & Conventions](#513-source-code-style-guide--conventions)
    - [5.1.4. Software Deployment Configuration](#514-software-deployment-configuration)
- [5.2. Landing Page, Services & Applications Implementation](#52-landing-page-services--applications-implementation)
    - [5.2.1. Sprint 1](#521-sprint-1)
        - [5.2.1.1. Sprint Planning 1](#5211-sprint-planning-1)
        - [5.2.1.2. Sprint Backlog 1](#5212-sprint-backlog-1)
        - [5.2.1.3. Development Evidence for Sprint Review](#5213-development-evidence-for-sprint-review)
        - [5.2.1.4. Testing Suite Evidence for Sprint Review](#5214-testing-suite-evidence-for-sprint-review)
        - [5.2.1.5. Execution Evidence for Sprint Review](#5215-execution-evidence-for-sprint-review)
        - [5.2.1.6. Services Documentation Evidence for Sprint Review](#5216-services-documentation-evidence-for-sprint-review)
        - [5.2.1.7. Software Deployment Evidence for Sprint Review](#5217-software-deployment-evidence-for-sprint-review)
        - [5.2.1.8. Team Collaboration Insights during Sprint](#5218-team-collaboration-insights-during-sprint)
