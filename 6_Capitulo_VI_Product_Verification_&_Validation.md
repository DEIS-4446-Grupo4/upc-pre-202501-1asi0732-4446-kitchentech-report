# Capitulo VI: Product Verification & Validation

## 6.1 Testing Suites & Validation
### 6.1.1 Core Entities Unit Tests
Realizar pruebas unitarias a las distintas entidades del sistema y sus metodos es fundamental para asegurar que cada componente funcione de manera independiente y cumpla con los requisitos establecidos. En este caso, se han realizado pruebas unitarias a las entidades de la aplicación web KitchenTech, utilizando la herramienta "JUnit" y "Mockito" para validar el correcto funcionamiento de las clases y métodos implementados.

Para ello, se han creado pruebas unitarias para las siguientes entidades:
### **Authentication**
![authentication](Resources/UnitTests/AuthUnitTest.png)
### **Client**
![client](Resources/UnitTests/ClientUnitTest.png)
### **Product**
![product](Resources/UnitTests/ProductUnitTest.png)
### **Supply**
![supply](Resources/UnitTests/SupplyUnitTest.png)
### **Table**
![table](Resources/UnitTests/TableUnitTest.png)

### 6.1.2 Core Integration Tests

Esta prueba verifica que el servicio de cuentas (`AccountService`) funcione correctamente cuando interactúa con su repositorio y la base de datos, específicamente para el proceso de creación de cuentas y cálculo automático del total.

#### Componentes bajo prueba:
- **AccountServiceImpl**: Servicio principal que contiene la lógica de negocio
- **AccountRepository**: Repositorio para persistencia y recuperación de datos

#### Flujo de integración:
1. Se preparan los objetos necesarios (cliente, mesa, productos)
2. Se crea una cuenta con productos asociados
3. Se invoca `accountService.createAccount()` que debe:
    - Guardar la información en la base de datos
    - Calcular el total sumando los productos
4. Se recupera la cuenta desde el repositorio para verificar la persistencia

#### Verificaciones:
- Se genera un ID válido para la cuenta creada
- La cuenta persiste correctamente en la base de datos
- El nombre de la cuenta se guarda correctamente
- El cálculo del total es correcto: 35.0 (10×2 + 5×3)

![integration test 1](Resources/integration_test1.png)
![integartion test 1 result](Resources/integration_test1_result.png)

Esta prueba verifica que el método `createProduct` del `ProductController` funcione correctamente al crear un nuevo producto en el sistema. El método debe validar la existencia del restaurante, mapear los datos del producto y persistirlo en la base de datos.

#### Componentes simulados:
- **RestaurantRepository**: Para verificar la existencia del restaurante
- **ProductRepository**: Para persistir el nuevo producto
- **ProductService**: Servicio de productos (aunque no se utiliza directamente en este método)

#### Flujo del proceso verificado:
1. Se recibe un objeto Product como cuerpo de la petición
2. Se verifica que el restaurante asociado exista
3. Se mapean los datos del producto desde el DTO recibido
4. Se persiste el producto en la base de datos
5. Se devuelve el producto creado con un código HTTP 201 (CREATED)

#### Verificaciones:
- El código de respuesta HTTP es 201 (CREATED)
- El objeto devuelto no es nulo
- Todos los campos del producto devuelto coinciden con los valores esperados:
    - ID: 1
    - Nombre: "Lomo Saltado"
    - Precio: 27.0
    - URL de imagen: "https://www.google.com"
    - Categoría: "Almuerzo"
    - ID de Restaurante: 1

![integration test 2](Resources/integration_test2.png)
![integration test 2 result](Resources/integration_test2_result.png)


### 6.1.3 Core Behavior-Driven Development
Esta sección se centra en cómo el equipo definirá y validará el comportamiento esperado de nuestra aplicación web KitchenTech directamente desde la perspectiva de nuestros usuarios. Utilizaremos Cucumber como nuestra herramienta principal, redactando escenarios de usuario claros y concisos que describan el flujo de interacción con KitchenTech. Estos escenarios serán comprobados utilizando selenium.

| Historia de Usuario | E07_US030                                |
|---------------------|------------------------------------------|
|Descripción          | Ingresar nuevos productos al inventario. |
|Cucumber             | Scenario: Se agrega producto nuevo <br> Given que el usuario agrega un producto nuevo <br> When hace click en "add Supply" and completa el formulario and hace click en "save" <br> Then el producto se añade a la lista de productos <br> ![add suply BDD](Resources/images/Capitulo%206/AddSupply1.png) <br> ![add suply BDD](Resources/images/Capitulo%206/AddSupply2.png) <br> ![add suply BDD](Resources/images/Capitulo%206/AddSupply3.png)    |
|Resultado            | Se puede observar que la funcionalidad de añadir un nuevo producto es funcional para los usuarios y puede ser automatizada. |

| Historia de Usuario | E07_US032                                |
|---------------------|------------------------------------------|
|Descripción          | Editar insumos existentes. |
|Cucumber             | Scenario: Se selecciona un insumo existente <br> Given que el usuario edite el insumo seleccionado <br> When hace click en "Edit" and renueve los datos en el formulario and hace click en "Update" <br> Then los datos se actualizan en la lista de insumos <br> ![add suply BDD](Resources/images/Capitulo%206/KT1.png) <br> ![add suply BDD](Resources/images/Capitulo%206/KT2.png) <br> ![add suply BDD](Resources/images/Capitulo%206/KT3.png) <br> ![add suply BDD](Resources/images/Capitulo%206/KT4.png) <br> ![add suply BDD](Resources/images/Capitulo%206/KT5.png) |
|Resultado            | Se puede observar que la funcionalidad de editar un insumo existente es funcional para los usuarios y puede ser automatizada. |

### 6.1.4 Core System Tests
Para llevar a cabo las core system test se ha utilizado "Lighthouse" como herramienta. Con esta herramienta se han realizado las pruebas de rendimiento general de la aplicación web kitchentech ya desplegada, accesibilidad y mejores prácticas. La siguiente figura muestra los resultados de dichas pruebas.

![core system test](Resources/images/Capitulo%206/CoreSystemTest.jpg)

## 6.2 Static Testing & Verification
### 6.2.1 Static Code Analysis
#### 6.2.1.1. Coding Standard & Code Conventions
En el desarrollo del proyecto KitchenTech, implementamos estrictos estándares de codificación para mantener la consistencia y legibilidad del código. Para el frontend con Vue.js, utilizamos ESLint con la configuración estándar de Vue, mientras que para el backend con Spring Boot, seguimos las convenciones de Oracle para Java.
Aplicamos las siguientes prácticas:
- **Nomenclatura**: Utilizamos camelCase para variables y métodos, PascalCase para clases y componentes, y UPPER_SNAKE_CASE para constantes.
- **Indentación**: 2 espacios para JavaScript/Vue y 4 espacios para Java.
- **Comentarios**: Documentación JavaDoc para clases y métodos públicos, y comentarios explicativos para lógica compleja.
- **Organización de archivos**: Estructura organizada por módulos funcionales tanto en frontend como en backend.

#### 6.2.1.2. Code Quality & Code Security
Para asegurar la calidad y seguridad del código en KitchenTech, implementamos varias prácticas manuales:
- **Revisiones exhaustivas**: Realizamos inspecciones de código periódicas para identificar posibles problemas de calidad y seguridad sin depender de herramientas automatizadas.
- **Seguridad**: Implementamos prácticas OWASP como:
  - Validación estricta de entradas de usuario
  - Uso de Prepared Statements para prevenir inyección SQL
  - Implementación de HTTPS para todas las comunicaciones
  - Tokens JWT con tiempos de expiración cortos
- **Revisiones de código**: Cada pull request requiere la aprobación de al menos un desarrollador adicional, con énfasis en revisiones de seguridad para componentes críticos.
- **Estándares documentados**: Mantenemos una guía de mejores prácticas que todos los desarrolladores deben seguir para asegurar un código de alta calidad.

### 6.2.2 Reviews
En KitchenTech, realizamos revisiones de código de manera regular para asegurar la calidad y consistencia del código. Estas revisiones se llevan a cabo en las siguientes etapas:
- **Pull Requests**: Cada vez que un desarrollador crea un pull request, se asigna a al menos un revisor. El revisor verifica la calidad del código, la adherencia a los estándares y la ausencia de errores.
- **Revisiones de Sprint**: Al final de cada sprint, se realiza una revisión del código desarrollado. Se evalúa la implementación de las historias de usuario y se discuten posibles mejoras.
- **Revisiones de Seguridad**: Se realizan revisiones específicas para identificar vulnerabilidades de seguridad, especialmente en componentes críticos como autenticación y manejo de datos sensibles.
- **Revisiones de Arquitectura**: En momentos clave del proyecto, se revisa la arquitectura general para asegurar que las decisiones tomadas sigan alineadas con los objetivos del sistema y las mejores prácticas.
- **Revisiones de Documentación**: Se revisa la documentación del código para asegurar que esté actualizada y sea clara, facilitando la comprensión del sistema por parte de nuevos desarrolladores.
- **Revisiones de Integración Continua**: Cada vez que se ejecuta un pipeline de CI/CD, se revisan los resultados de las pruebas automatizadas para asegurar que no se introduzcan errores en el código base.
- **Revisiones de Código de Terceros**: Si se integran bibliotecas o componentes de terceros, se revisa su código para asegurar que cumplan con los estándares de calidad y seguridad del proyecto.

De esta manera, KitchenTech mantiene un alto estándar de calidad en su código, asegurando que cada componente sea revisado y validado antes de ser integrado al sistema.

## 6.3 Validation Interviews
### 6.3.1. Diseño de Entrevistas

- ¿Qué tan fácil te resultó navegar por la landing page y encontrar información relevante sobre el sistema?

- ¿La información proporcionada en la landing page te ayudó a comprender cómo la solución IoT podría mejorar la atención en el restaurante?
- ¿Qué aspectos de la aplicación te resultaron intuitivos o confusos al tomar un pedido?
- ¿Qué tan fácil te resultó recibir y gestionar notificaciones sobre el estado de las mesas (como la llegada de clientes o platos por recoger)?
- ¿Sientes que el proceso de enviar pedidos a cocina y caja desde la aplicación agiliza tu flujo de trabajo?
- ¿Cómo evaluas la velocidad y precisión de la aplicación al registrar cambios en los pedidos?
- ¿La interfaz de la aplicación facilita la gestión de cuentas y pagos de los clientes? ¿Por qué?
- ¿Qué tan útil te resulta la opción de recibir alertas cuando los clientes entran o salen del restaurante?
- ¿Crees que el sistema IoT implementado mejora la experiencia de servicio para el cliente? ¿En qué aspectos?
- ¿Qué cambiarías o mejorarías en la aplicación para facilitar aún más la atención a los clientes?


### 6.3.2. Registro de Entrevistas

-  Primera Entrevista:
-  Segmento: Meseros
-  Nombre: Yeret Yucta
-  Edad: 21
-  Ocupación: Estudiante universitario y mesero a tiempo parcial
-  Enlace: https://upcedupe-my.sharepoint.com/:v:/g/personal/u202110966_upc_edu_pe/ESsC5d2geJZHmvEWDpBGKLgBcXgkFYSqc4YfkWn7CYaRBQ?e=sOxJuy
-  Duración: 0:00 a 11:21 (11 minutos 21 segundos)

<img src="./Resources/images/ev1.png" width="600" >

-  Resumen:
   Yeret, un estudiante universitario de 21 años que trabaja a tiempo parcial como mesero en una restaurante familiar, es analítico e ingenioso, lo que le permite actuar de manera correcta con los clientes.
   Comenta que la landing page le ayudó a entender cómo el sistema IoT agiliza su trabajo al permitirle gestionar notificaciones en tiempo real sobre el estado de las mesas y pedidos. Esta información le permite organizarse mejor y reducir tiempos de espera.
   Aspectos intuitivos y confusos: Al tomar un pedido, Yeret encontró que el menú digital es fácil de navegar y le permite incluir especificaciones, aunque sugiere mejorar algunos íconos para que sean más claros.
   Gestión de notificaciones: Yeret considera muy útil la función de notificaciones, ya que son visibles y manejables sin interrumpir su flujo de trabajo, lo cual reduce desplazamientos innecesarios y facilita su labor.
   Envío de pedidos a cocina y caja: Destaca la eficiencia de poder enviar los pedidos directamente a cocina y caja desde la app, ahorrando tiempo y evitando errores durante horas pico.
   Velocidad y precisión de la app: La rapidez y precisión de Kitchen Tech al registrar cambios en pedidos es clave para mejorar la satisfacción del cliente y evitar confusiones.
   Gestión de cuentas y pagos: La interfaz para gestionar cuentas resulta sencilla y permite dividir pagos o registrar transacciones sin dificultad, minimizando errores.
   Alertas de entrada y salida de clientes: Yeret aprecia esta función, ya que le permite atender a los clientes más oportunamente y preparar mesas rápidamente para nuevos clientes.
   Experiencia del cliente: Cree que el sistema IoT mejora la experiencia de servicio, ya que los clientes perciben un servicio más atento y eficiente, con pedidos que llegan rápido y la cuenta lista a tiempo.
   Sugerencias de mejora: Sugiere añadir funciones de recomendaciones para upselling o sugerencias de platos, además de optimizar íconos y descripciones para hacer la app aún más intuitiva.

### 6.3.3. Evaluación según heurísticas
**CARRERA**: Ingeniería de Software  
**CURSO**: Diseño de Experimentos de Ingeniería de Software   
**SECCIÓN**: 4446
**PROFESORES**: Todos  
**AUDITOR**: Command Testers
**CLIENTE(S)**: Usuarios entrevistados

---

**SITE o APP A EVALUAR**: Kitchen Tech

---

### TAREAS A EVALUAR:

El alcance de esta evaluación incluye la revisión de la usabilidad de las siguientes tareas:

1. Crear botón para desplegar menú de opciones de usuario
2. Implementar botón de ver perfil en menú desplegable
3. Implementar botón de crear nuevo mesero en menú desplegable
4. Crear vista de cuentas guardadas, con search bar y cards que incluyan nombre de la cuenta, cliente, costo y botones
5. Guardar orden en una cuenta
6. Implementar botón para eliminar cuenta
7. Guardar orden en una mesa
8. Actualización de los pedidos y mesas
9. Implementar botón para cambiar la vista de cuentas guardadas a mesas junto al search bar
10. Implementar navegación a la página de caja con el pedido guardado al dar clic en la cuenta
11. Crear botón de agregar nuevos productos
12. Implementar validaciones para el guardado de productos
13. Crear vista de productos
14. Cargar la vista de nuevo producto con los datos del producto guardado para su edición
15. Crear botón de eliminar producto
16. Desarrollar vista en la web app de inicio de sesión
17. Implementar validaciones de credenciales en la vista de iniciar sesión
18. Crear botón de cerrar sesión en menú desplegable

---

No están incluidas en esta versión de la evaluación las siguientes tareas:

1. Crear vista de caja con searchbar y sección acceso directo de productos
2. Implementar la vista de mesas con sus métodos CRUD
3. Implementar vista de recuperar contraseña
4. Implementar validaciones para vista de recuperar contraseña
5. Implementar ver contraseña en vista de recuperar contraseña
6. Bloquear acceso a la cuenta tras fallar en iniciar sesión 5 veces
7. Crear validaciones para registro de nuevo mesero
8. Crear un Sidebar que incluya los botones de navegación a todas las opciones de Mesero

---

### ESCALA DE SEVERIDAD:

Los errores serán puntuados tomando en cuenta la siguiente escala de severidad

| Nivel | Descripción                                                                                                                                                                                       |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | Problema superficial: puede ser fácilmente superado por el usuario o ocurre con muy poca frecuencia. No necesita ser arreglado a no ser que exista disponibilidad de tiempo.                      |
| 2     | Problema menor: puede ocurrir un poco más frecuentemente o es un poco más difícil de superar para el usuario. Se le debería asignar una prioridad baja resolverlo de cara a la siguiente release. |
| 3     | Problema mayor: ocurre frecuentemente o los usuarios no son capaces de resolverlos. Es importante que sean corregidos y se les debe asignar una prioridad alta.                                   |
| 4     | Problema muy grave: un error de gran impacto que impide al usuario continuar con el uso de la herramienta. Es imperativo que sea corregido antes del lanzamiento.                                 |

---

### TABLA RESUMEN:

| # | Problema                                                                                                   | Escala de severidad | Heurística/Principio violado(a)             |
|---|------------------------------------------------------------------------------------------------------------|---------------------|---------------------------------------------|
| 1 | Cuestión de confusión entre vistas                                                                         | 3                   | Usability: Consistencia y estándares        |
| 2 | Mejorar la organización de funcionalidades                                                                 | 3                   | Information Architecture: Is it findable?   |
| 3 | Mejora en la sección de pedido para el caso de edición en escenarios de cambios de pedido a último momento | 4                   | Usability: Flexibilidad y eficiencia de uso |

---

### DESCRIPCIÓN DE PROBLEMAS:

**PROBLEMA #1**: Cuestión de confusión entre vistas  
**Severidad**: 3  
**Heurística violada**: Usability – Consistencia y estándares

**Problema**:  
Los usuarios encuentran dificultades para identificar a qué vista pertenecen ciertas opciones de menú. Esto genera confusión y aumenta el tiempo necesario para completar una tarea específica.

**Recomendación**:  
Reorganizar las vistas para mejorar la diferenciación visual entre ellas, asegurando que cada vista tenga elementos distintivos claros que guíen al usuario.

---

**PROBLEMA #2**: Mejorar la organización de funcionalidades  
**Severidad**: 3  
**Heurística violada**: Information Architecture – Is it findable?

**Problema**:  
La disposición de las funcionalidades no permite una rápida localización, lo cual impacta negativamente la experiencia del usuario.

**Recomendación**:  
Agrupar las funcionalidades de acuerdo con su propósito y frecuencia de uso, proporcionando accesos rápidos a las tareas más comunes.

---

**PROBLEMA #3**: Mejora en la sección de pedido para el caso de edición en escenarios de cambios de pedido a último momento  
**Severidad**: 4  
**Heurística violada**: Usability – Flexibilidad y eficiencia de uso

**Problema**:  
Cuando un usuario intenta realizar modificaciones de último momento en un pedido, se encuentra con limitaciones en la interfaz que dificultan completar el cambio sin reiniciar el proceso.

**Recomendación**:  
Implementar una opción de edición rápida para cambios de último momento, que permita al usuario modificar elementos del pedido sin necesidad de repetir los pasos previos.

## 6.4 Auditoría de Experiencias de Usuario
### 6.4.1. Auditoría Realizada
#### 6.4.1.1. Información del grupo auditado
En esta auditoría, se ha evaluado la experiencia de usuario de la aplicación web y móvil AidManager, enfocándose en la usabilidad y la satisfacción del usuario final. El grupo auditado está compuesto por un equipo de desarrollo y diseño de software conformado por los siguientes miembros:

| Nombre                           |
|----------------------------------|
| Juan Alejandro Cuadros Rodriguez |
| Nicolas Sebastian Esteban Garcia |
| Manuel Sebastian Peña Rivera     |
| Sebastián Ramírez Hoffmann       |
| Sebastian Andre Ramirez Mendez   |

- **Objetivo del negocio:** El principal objetivo de AidManager es proporcionar una plataforma intuitiva y eficiente que permita a los usuarios gestionar proyectos a ONGs de manera efectiva, facilitando la colaboración y el seguimiento de tareas.
- **Usuarios principales:** El principal segmnento objetivo de AidManager son los usuarios que trabajan en ONGs, quienes necesitan una herramienta que les permita gestionar proyectos de manera eficiente y colaborativa. Estos se subsegmentan en: Lider de proyecto y Colaborador.
#### 6.4.1.2. Cronograma de auditoría realizada
| Fecha      | Actividad                                      |
|------------|------------------------------------------------|
| 17/06/2025 | Revisión de la documentación del proyecto      |
| 18/05/2025 | Análisis de la arquitectura de la aplicación   |
| 19/05/2025 | Evaluación de la interfaz de usuario           |
| 20/05/2025 | Pruebas de usabilidad con usuarios reales      |

#### 6.4.1.3. Contenido de auditoría realizada
- **Objetivo de la auditoría:** Evaluar la experiencia de usuario de AidManager, identificando áreas de mejora y validando la usabilidad de la aplicación.
- **Metodología utilizada:** Se utilizó una combinación de revisión de documentación, análisis de la arquitectura de la aplicación y pruebas de usabilidad con usuarios reales.
- **Áreas evaluadas:**
  - Usabilidad de la interfaz de usuario
  - Flujo de navegación
  - Accesibilidad de las funcionalidades principales: 
    - Gestión de proyectos
    - Colaboración entre usuarios
    - Creación y Seguimiento de tareas y plazos
  - Satisfacción del usuario final
- Principales hallazgos:
  - La interfaz de usuario es intuitiva y fácil de navegar.
  - Los usuarios valoran positivamente la funcionalidad de gestión de proyectos y la colaboración entre usuarios.
  - Se identificaron áreas de mejora en:
    - Visualización general del proyecto
    - Visualización de publicaciones
  - Recomendaciones clave:
    - Mejorar la visualización general del proyecto para que sea más clara y concisa.
    - Dividir la sección de comentarios en un card flotante para una mejor usabilidad.
### 6.4.2. Auditoría Recibida
#### 6.4.1.1. Información del grupo auditor
En esta auditoria se hace una evaluación del sistema de KitchenTech enfocándose en la app web y app móvil.

Miembros del equipo auditor:

| Nombre                           |
|----------------------------------|
| Juan Alejandro Cuadros Rodriguez |
| Nicolas Sebastian Esteban Garcia |
| Manuel Sebastian Peña Rivera     |
| Sebastián Ramírez Hoffmann       |
| Sebastian Andre Ramirez Mendez   |

##### Objetivos

El equipo 4 de la startup Kitchen Tech se enfocan en el rubro de la industria de Restaurantes y a lo largo del curso han realizado su aplicacion movil y web, en esta auditoria nos enfocaremos en utilizar las soluciones y el flujo principal.

Objetivo del negocio:

Usuarios Principales (Segmentos):
- 1 Meseros
- 2 Administradores


#### 6.4.1.2. Cronograma de auditoría recibida
Tomando en cuenta que el producto del grupo a auditar estaba en fase de pruebas cuando nos contactamos acordamos en hacer la auditoria el 18 de Junio del 2025.

- La auditoria inico el 18 de Junio del 2025

- La auditoria finalizó el 20 de Junio del 2025

#### 6.4.1.3. Contenido de auditoría recibida
Objetivos de la auditoría: Evaluar la usabilidad de la nueva funcionalidad de reporte y verificar la conformidad con principios de accesibilidad.

Metodología utilizada: Revisión heurística y análisis de flujo de usuario.

Áreas evaluadas: Registro de usuario, funciones principales como: Sistema core de la solucion.

Principales hallazgos y problemas identificados:

- Dificultad para encontrar la sección de ayuda
- Proceso de pago con demasiados pasos
- Botones de llamado a la acción no suficientemente visibles

Recomendaciones clave:
- Simplificar el proceso de registro a 3 pasos
- Rediseñar la navegación principal con etiquetas más claras
- Implementar iconos reconocibles en los botones

#### 6.4.1.4. Resumen de modificaciones para subsanar hallazgos
- Se simplificó el proceso de registro a 3 pasos, eliminando campos innecesarios de manera que sea más intuitivo para el usuario.
- Se rediseñó la navegación principal, utilizando etiquetas más claras y descriptivas para facilitar la comprensión de las secciones.
- Se implementaron iconos reconocibles en los botones de acción principal, mejorando su visibilidad y usabilidad.