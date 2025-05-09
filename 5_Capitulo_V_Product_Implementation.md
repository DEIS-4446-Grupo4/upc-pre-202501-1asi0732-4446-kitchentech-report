# Capitulo V: Product Implementation

## 5.1 Software Configuration Management 
### 5.1.1 Software Development Environment Configuration
En esta sección se presentan los softwares correspondientes utilizados por los miembros del equipo y los enlaces utilizados para que cada uno tenga asignado el rol de administrador y pueda ejecutar sus cambios al proyecto:  
- **Miro:** Event Storming, Candidate Context Discovery, Domain Message Flows Modeling, Bounded Context Canvases
*Imagen*

Enlace del miro: https://miro.com/app/board/uXjVKkI6spU=/ 

- *Lucidchart:* Context Mapping, DDD Bounded Context Class Diagram
  
*Imagen*

- *Structurizr:* C4 Model System, Container, Component Diagram
  
*Imagen*

- *Vertabelo:* DDD Database Diagram
  
*Imagen*

- *Visual Paradigm:* Bounded Context Component Diagram
  
*Imagen*

- *Visual Studio Code:* Software Development
  
*Imagen*

  
- *Figma:* Web/Mobile Prototype & User Flow
  
*Imagen*

Enlace del figma: https://www.figma.com/design/R6y8A0ThMExKQZWHWnzsS8/KitchenTech---Landing-Page?m=auto&t=n8aCxpzzdt35lHmn-6 

### 5.1.2 Source Code Management
El manejo y la gestión de las diferentes modificaciones que se llevaron a cabo, fueron mediante una organización de GitHub para nuestro Startup. 

Organización: https://github.com/DEIS-4446-Grupo4

Repositorio de Landing Page: https://github.com/DEIS-4446-Grupo4/landing-page.git 

Deployment del Landing Page: https://landing-page-kitchentech.vercel.app 

Asimismo, se establecieron dos ramas correspondientes para el desarrollo:  

- Main: esta rama cuenta con la versión estable de nuestra landing page luego de que cada componente haya sido aprobado mediante una pull request. 

- develop: esta rama cuenta con versiones donde se pusieron a prueba los componentes que cada integrante implemento a la landing page

### 5.1.3 Source Code Style Guide & Conventions

### HTML:
Se aplicarán las directrices de “HTML Style Guide and Coding” de W3Schools, destacando convenciones clave como declarar siempre el tipo de documento (<!DOCTYPE>), utilizar etiquetas y atributos en minúsculas para mantener un código limpio y organizado, y cerrar todas las etiquetas para prevenir errores. Se colocarán comillas en los valores de los atributos y se especificarán siempre los atributos alt, width y height en las imágenes para mejorar la accesibilidad y el SEO. Además, no se omitirán las etiquetas <head> y los metadatos esenciales para la optimización en motores de búsqueda.

### CSS:
Basado en la “Google HTML/CSS Style Guide”, se seguirán prácticas recomendadas como usar nombres de clase generales, cortos y descriptivos, empleando guiones para separar palabras. Se evitarán los selectores de ID, priorizando selectores de clase, y se utilizarán propiedades abreviadas como margin, padding, y border para mejorar la legibilidad y reducir el número de líneas de código. Estas convenciones aseguran un estilo CSS más limpio y escalable.

### JavaScript:
Se implementarán las “JavaScript Best Practices” recomendadas por el W3C, priorizando nombres cortos y fáciles de entender para variables y funciones. Se evitará el uso de variables globales (var), prefiriendo let o const para evitar colisiones de nombres y errores a largo plazo. Se documentarán y comentarán solo las partes necesarias del código, explicando las secciones complejas, y se adoptarán notaciones y operadores sencillos para manipular estructuras de datos.

### Gherkin:
Para las pruebas, se seguirá la guía “Gherkin Conventions for Readable Specifications”, organizando claramente los bloques Given-When-Then mediante la indentación adecuada y el uso de la palabra clave "And" para pasos adicionales. Se utilizarán tablas cuando los pasos requieran mayor información y se emplearán comillas simples para los parámetros en los escenarios, mejorando la legibilidad. Los escenarios múltiples se separarán con comentarios para facilitar la organización visual.

### Frontend y Backend:
La landing page y las aplicaciones web seguirán las pautas de diseño de Material Design, utilizando Angular Material como biblioteca de componentes de UI. El frontend será desarrollado en Angular Framework, combinando HTML5, CSS3 y JavaScript/TypeScript para los aspectos estáticos y lógicos de las aplicaciones. En el backend, se implementarán servicios web bajo el estilo arquitectónico RESTful API usando Spring Boot y Java como lenguaje principal.

### Control de versiones:
El control de versiones será gestionado con GIT desde GitHub, siguiendo las prácticas de GitFlow Workflow junto con Conventional Commits y Semantic Versioning. Esto permitirá una integración continua, con despliegues automáticos y manejo eficiente de hotfixes.


### 5.1.4 Software Deployment Configuration
La siguiente tabla presenta los commits del repositorio del landing page en GitHub:

| Id del commit                            | Commit                                                             |
|------------------------------------------|--------------------------------------------------------------------|
| babf1bf8b1439d841dc4fde5b33f2aac61105ce0 | Initial commit                                                     |
| 6aff73d0b39a7c9a4d5ae1c99d9338f9c6bd662d | Part 1                                                             |
| b001457e48e36f514a12f978dbb9475c25c50e06 | Part 2                                                             |
| -                                        | Merge branch 'main' of https://landing-page-kitchentech.vercel.app |
| 70f08b4f25df21ae3535a38c6a58269014181cfd | Part 3                                                             |
| bd7bee8feec07792a080e8d29913ebeb7db84b6e | Part 4                                                             |
| d38272d239da0f26d26452496e6d3e89f8a871fe | (feat) "add header & footer"                                       |

## 5.2 Produt Implementation & Deployment
En esta sección, se explicará y evidenciará el proceso de despliegue para la Landing page de nuestro startup, utilizando la herramienta de despliegue. Para lograr este objetivo se utilizó el CLI de esta herramienta y el GitHub donde se creó el repositorio. 

### 5.2.1 Sprint Backlogs

<table>
  <tr>
    <th colspan="2">Sprint #</th>
    <th colspan="6">Sprint 1</th>
  </tr>
  <tr>
    <th colspan="2">User Story</th>
    <th colspan="6">Work-Item / Task</th>
  </tr>
  <tr>
    <th>Id</th>
    <th>Title</th>
    <th>Id</th>
    <th>Title</th>
    <th>Description</th>
    <th>Estimation (Hours)</th>
    <th>Assigned to</th>
    <th>Status</th>
  </tr>
  <tr>
    <th>US001</th>
    <th>Seccion de Header </th>
    <th>2</th>
    <th>Seccion de Header</th>
    <th>COMO usuario QUIERO visualizar un encabezado de página que contenga opciones PARA una mejor navegación por la página. </th>
    <th>2</th>
    <th>Johan Príncipe Godoy</th>
    <th>Done</th>
  </tr>
  <tr>
    <th>US002</th>
    <th>Seccion de Footer</th>
    <th>3</th>
    <th>Seccion de Footer</th>
    <th>COMO usuario QUIERO visualizar pie de página que contenga información PARA un mejor entendimiento de la página. </th>
    <th>1</th>
    <th>Nicolas Zagal</th>
    <th>Done</th>
  </tr>
  <tr>
    <th>US005</th>
    <th>Boton para ver mas informacion</th>
    <th>4</th>
    <th>Boton para ver mas informacion</th>
    <th>COMO usuario QUIERO ver más información sobre la página PARA comprender más sobre la start-up.  </th>
    <th>1</th>
    <th>Diego Jesus Alonso Garay</th>
    <th>Done</th>
  </tr>
  <tr>
    <th>US006</th>
    <th>Sección de contacto </th>
    <th>5</th>
    <th>Sección de contacto </th>
    <th>COMO usuario QUIERO observar una seccion que contenga información de la página PARA poder conocer sobre qué se trata. </th>
    <th>2</th>
    <th>Gabriel Anthony Braithuaite Toledo</th>
    <th>Done</th>
  </tr>
  <tr>
    <th>US003</th>
    <th>Barra de Navegación </th>
    <th>13</th>
    <th>Barra de Navegación </th>
    <th>COMO usuario QUIERO presionar botones en el encabezado del landing page para desplazarme por la página.  </th>
    <th>3</th>
    <th>Nicolas Zagal</th>
    <th>Done</th>
  </tr>
  <tr>
    <th>US004</th>
    <th>Descripción de la Start-Up </th>
    <th>14</th>
    <th>Descripción de la Start-Up </th>
    <th>COMO usuario QUIERO observar una seccion “Contacto” PARA poder comunicarme directamente con el equipo de desarrollo.</th>
    <th>2</th>
    <th>Johan Príncipe Godoy</th>
    <th>Done</th>
  </tr>
  <tr>
    <th>US007</th>
    <th>Sección de información del equipo </th>
    <th>15</th>
    <th>Sección de información del equipo </th>
    <th>COMO usuario QUIERO observar en el encabezado una seccion de información del equipo PARA conocer más a fondo su desarrollo. </th>
    <th>3</th>
    <th>Diego Jesus Alonso Garay</th>
    <th>Done</th>
  </tr>
  <tr>
    <th>US009</th>
    <th>Logout </th>
    <th>1</th>
    <th>Logout </th>
    <th>COMO cliente QUIERO salir de la aplicación PARA evitar el uso de mi cuenta por otras personas.  </th>
    <th>1</th>
    <th>Gabriel Anthony Braithuaite Toledo</th>
    <th>Done</th>
  </tr>
  <tr>
    <th>US014</th>
    <th>Sección de inicio de sesión  </th>
    <th>9</th>
    <th>Sección de inicio de sesión  </th>
    <th>COMO usuario QUIERO iniciar sesión en mi cuenta PARA acceder a la información de la plataforma.  </th>
    <th>2</th>
    <th>Johan Principe Godoy</th>
    <th>Done</th>
  </tr>
  <tr>
    <th>US015</th>
    <th>Sección de registro  </th>
    <th>10</th>
    <th>Sección de registro  </th>
    <th>COMO usuario QUIERO observar una seccion de “Regístrate” PARA crear una cuenta nueva.  </th>
    <th>2</th>
    <th>Nicolas Zagal</th>
    <th>Done</th>
  </tr>
  <tr>
    <th>US016</th>
    <th>Dirigir a perfil de usuario  </th>
    <th>18</th>
    <th>Dirigir a perfil de usuario  </th>
    <th>COMO cliente QUIERO acceder a mi perfil PARA cambiar cualquier dato que necesite actualización. </th>
    <th>3</th>
    <th>Gabriel Anthony Braithuaite Toledo</th>
    <th>Done</th>
  </tr>
  <tr>
    <th>US018</th>
    <th>Ver y editar datos de usuario  </th>
    <th>19</th>
    <th>Ver y editar datos de usuario  </th>
    <th>COMO usuario QUIERO ver y editar mi información PARA mantenerla actualizada.  </th>
    <th>3</th>
    <th>Diego Jesus Alonso Garay</th>
    <th>In Progress </th>
  </tr>
  <tr>
    <th>US025</th>
    <th>Enviar pedido guardado a cocina y caja  </th>
    <th>28</th>
    <th>Enviar pedido guardado a cocina y caja  </th>
    <th>COMO mesero QUIERO enviar pedidos a cocina o caja PARA continuar con el flujo de trabajo sin necesidad de dictar la orden manualmente. </th>
    <th>4</th>
    <th>Johan Principe Godoy</th>
    <th>In Progress </th>
  </tr>
  <tr>
    <th>US013</th>
    <th>Ver resumen de ventas</th>
    <th>30</th>
    <th>Ver resumen de ventas</th>
    <th>COMO administrador QUIERO ver el resumen de ventas por días PARA saber cuánto se vendió en cada jornada.  </th>
    <th>4</th>
    <th>Nicolas Zagal</th>
    <th>In Progress </th>
  </tr>
</table>


### 5.2.2 Implemented Landing Page Evidence
Vistas desarrolladas: Landing page (Hero section):

<img src="./Resources/Evidences/Landing/1.jpg" >

Landing page (About us):

<img src="./Resources/Evidences/Landing/2.jpg" >

Landing page (Members):

<img src="./Resources/our_team_mockup.png">

Landing page (IOT features):

<img src="./Resources/Evidences/Landing/4.jpg" >

Landing page (Galelry section):

<img src="./Resources/Evidences/Landing/5.jpg" >

Landing page (Contact section y footer):

<img src="./Resources/Evidences/Landing/6.jpg" >


### 5.2.3 Implemented Frontend-Web Application Evidence

Vistas desarrolladas: Web app (profile):

<img src="./Resources/webapp/1.jpeg" >


Web app (login):

<img src="./Resources/webapp/2.jpeg" >

Web app (sign up):

<img src="./Resources/webapp/3.jpeg" >

Web app (caja):

<img src="./Resources/webapp/4.jpeg" >

Web app (cuentas guardadas):

<img src="./Resources/webapp/5.jpeg" >


Web app (mov. de caja):

<img src="./Resources/webapp/6.jpeg" >

Web app (productos):

<img src="./Resources/webapp/7.jpeg" >


### 5.2.4 Acuerdo de Servicio - SaaS

### 5.2.5. Implemented Native-Mobile Application Evidence


### 5.2.6. Implemented RESTful API and/or Serverless Backend Evidence

Esta sección recopila la evidencia del despliegue de software realizado durante el Sprint. Se incluyen capturas y registros que muestran el proceso de implementación en el entorno correspondiente, verificando que el despliegue se llevó a cabo correctamente y que el sistema cumple con los requisitos definidos para el Sprint Review.


<img src="./Resources/Evidences/backenddeployment1_kitchentech.png" >

<img src="./Resources/Evidences/backenddeployment2_kitchentech.png" >

### 5.2.7. RESTful API documentation

En esta sección, se realizaron **acceptance tests** en los endpoints de la API para cada una de las funcionalidades incluidas en este Sprint. Las funcionalidades relacionadas a estos tests son:

- **Login**: Endpoint para la autenticación de usuarios, donde se validó el acceso con credenciales correctas e incorrectas, garantizando que los usuarios puedan iniciar sesión de manera segura.
  <img src="Resources/Evidences/Login.jpeg" >
- **GetProductByRestaurant**: Endpoint para obtener productos específicos de un restaurante, donde se verificó que la consulta retorne correctamente los productos asociados a un restaurante dado.
  <img src="Resources/Evidences/GetProductByRestaurant.jpeg" >
- **GetRestaurant**: Endpoint para obtener detalles de un restaurante, validando que los datos del restaurante (nombre, dirección, tipo de cocina, etc.) se recuperen correctamente. 
  <img src="Resources/Evidences/getRestaurnant.jpeg" >
- **GetSupplyByRestaurant**: Endpoint para obtener los suministros disponibles para un restaurante, asegurando que la información de suministros esté correctamente asociada y se muestre sin errores.
  <img src="Resources/Evidences/GetSupplyByRestaurant.jpeg" >

Las pruebas realizadas en estos endpoints incluyen la validación de las respuestas (códigos de estado HTTP, datos retornados) y las condiciones de borde (por ejemplo, manejo de datos no encontrados, autenticación incorrecta). Las pruebas también se realizaron para asegurar que la API cumpla con los requisitos de rendimiento y seguridad establecidos para el Sprint.

### 5.2.8. Team Collaboration Insights

Para llevar a cabo los registros de nuestros avances durante el desarrollo de este Sprint, empleamos GitHub. Un miembro del equipo inició el proceso con un primer registro para establecer el repositorio y creó muchas ramas para poder trabajar sin interrumpir el avance de otro compañero. Posteriormente, hicimos una copia local del repositorio mediante Git, realizamos las modificaciones en GitHub. Finalmente, completamos el proceso con un registro de los cambios, el cual será examinado en el repositorio de GitHub.

<img src="./Resources/collaboration_insights1.png">

## 5.3. Video About-the-Product.

<img src="./Resources/Captura%20de%20pantalla%202024-11-20%20153403.jpg" width="600" >

Link del video: 

https://www.youtube.com/watch?v=rSsDI6MaP-4
