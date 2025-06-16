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
**Preguntas Generales**
- Nombre completo
- Edad
- Ocupación
- Años de experiencia

**Segmento Meseros**
- ¿Qué tan intuitivo te pareció el proceso de registro de pedidos?
- ¿Encontraste alguna dificultad para modificar un pedido existente?
- ¿La visualización de mesas disponibles es clara y útil?
- ¿El proceso de cierre de cuenta es eficiente para tu flujo de trabajo habitual?
- ¿Qué funcionalidades adicionales te gustaría encontrar en el sistema?

**Segmento Administradores**
- ¿La información presentada en los dashboards es relevante para la toma de decisiones?
- ¿Qué tan sencillo resultó el proceso de actualización de inventario?
- ¿La gestión del menú satisface las necesidades de su restaurante?
- ¿Considera que el sistema podría ayudar a optimizar costos y reducir desperdicios?
- ¿Qué funcionalidades adicionales le gustaría ver implementadas en el sistema?


### 6.3.2. Registro de Entrevistas
### 6.3.3. Evaluación según heurísticas
**Tareas a Evaluar**
1. **Gestión de pedidos:**
    - Iniciar sesión en el sistema
    - Visualizar mesas disponibles
    - Asignar mesa a cliente
    - Registrar pedido de cliente
    - Modificar pedido existente
    - Enviar pedido a cocina
    - Verificar estado de pedido

2. **Cierre de cuenta:**
    - Verificar detalle de consumo
    - Generar cuenta para cliente
    - Procesar pago
    - Cerrar mesa

3. **Gestión de inventario:**
    - Iniciar sesión como administrador
    - Visualizar productos en inventario
    - Agregar nuevo producto
    - Editar producto existente
    - Eliminar producto del inventario

4. **Gestión de menú:**
    - Crear categorías de productos
    - Añadir nuevos platos/productos
    - Modificar precios
    - Activar/desactivar productos temporalmente

No están incluidas en esta versión de la evaluación las siguientes tareas:
1. **Gestión de usuarios:**
    - Crear nuevo usuario
    - Editar usuario existente
    - Asignar roles y permisos
2. **Reportes y análisis:**
    - Generar reporte de ventas
    - Analizar consumo por categoría
    - Identificar productos más vendidos

**Escala de Severidad**
Los errores serán puntuados tomando en cuenta la siguiente escala de severidad

| Nivel | Descripción                                                                                                                                                                                    |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | Problema superficial: puede ser fácilmente superador por el usuario ó ocurre con muy poco frecuencia. No necesita ser arreglado a no ser que exista disponibilidad de tiempo.                  |
| 2     | Problema menor: puede ocurrir un poco más frecuentemente o es un poco más difícil de superar para el usuario. Se le debería asignar una prioridad baja resolverlo de cara al siguiente reléase |
| 3     | Problema mayor: ocurre frecuentemente o los usuarios no son capaces de resolverlos. Es importante que sean corregidos y se les debe asignar una prioridad alta.                                |
| 4     | Problema muy grave: un error de gran impacto que impide al usuario continuar con el uso de la herramienta. Es imperativo que sea corregido antes del lanzamiento.                              |

**Tabla Resumen**

| # | Problema                                                                                             | Escala de Severidad | Heurística/Principio violada(o)                          |
|---|------------------------------------------------------------------------------------------------------|---------------------|----------------------------------------------------------|
| 1 | Al finalizar un pedido, no hay confirmación visual ni botón para volver al inicio                    | 3                   | Usability: Visibilidad del estado del sistema            |
| 2 | No se puede deshacer la asignación de mesa sin cerrar sesión o reiniciar flujo                       | 3                   | Usability: Libertad y control del usuario                |
| 3 | Campos como “ID producto” aparecen en interfaces para meseros                                        | 2                   | Usability: Relación entre sistema y mundo real           |
| 4 | Al editar un producto en inventario, no se muestra la información actual, el usuario debe recordarla | 3                   | Usability: Reconocer antes que recordar                  |
| 5 | Algunos botones de acción no siguen el mismo diseño o posición en todas las vistas                   | 2                   | Usability: Consistencia y estándares                     |
| 6 | Al intentar cerrar una cuenta con error de conexión, se muestra “error inesperado” sin guía clara    | 4                   | Usability: Ayuda a reconocer, diagnosticar y recuperarse |
| 7 | No hay acceso a una guía rápida o tutorial para el nuevo usuario al iniciar sesión                   | 2                   | Usability: Ayuda y documentación                         |


## 6.4 Auditoría de Experiencias de Usuario
### 6.4.1. Auditoría Realizada
#### 6.4.1.1. Información del grupo auditado
#### 6.4.1.2. Cronograma de auditoría realizada
#### 6.4.1.3. Contenido de auditoría realizada
### 6.4.2. Auditoría Recibida
#### 6.4.1.1. Información del grupo auditor
#### 6.4.1.2. Cronograma de auditoría recibida
#### 6.4.1.3. Contenido de auditoría recibida
#### 6.4.1.4. Resumen de modificaciones para subsanar hallazgos