# Capitulo VI: Product Verification & Validation

## 6.1 Testing Suites & Validation
### 6.1.1 Core Entities Unit Tests
### 6.1.2 Core Integration Tests
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
