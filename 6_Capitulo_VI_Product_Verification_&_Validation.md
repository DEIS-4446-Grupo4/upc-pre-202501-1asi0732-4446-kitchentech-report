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
### 6.1.3 Core Behavior-Driven Development
Esta sección se centra en cómo el equipo definirá y validará el comportamiento esperado de nuestra aplicación web KitchenTech directamente desde la perspectiva de nuestros usuarios. Utilizaremos Cucumber como nuestra herramienta principal, redactando escenarios de usuario claros y concisos que describan el flujo de interacción con KitchenTech. Estos escenarios serán comprobados utilizando selenium.

| Historia de Usuario | E07_US030                                |
|---------------------|------------------------------------------|
|Descripción          | Ingresar nuevos productos al inventario. |
|Cucumber             | Scenario: Se agrega producto nuevo <br> Given que el usuario agrega un producto nuevo <br> When hace click en "add Supply" and completa el formulario and hace click en "save" <br> Then el producto se añade a la lista de productos <br> ![add suply BDD](Resources/images/Capitulo%206/AddSupply1.png) <br> ![add suply BDD](Resources/images/Capitulo%206/AddSupply2.png) <br> ![add suply BDD](Resources/images/Capitulo%206/AddSupply3.png)    |
|Resultado            | Se puede observar que la funcionalidad de añadir un nuevo producto es funcional para los usuarios y puede ser automatizada. |


### 6.1.4 Core System Tests
Para llevar a cabo las core system test se ha utilizado "Lighthouse" como herramienta. Con esta herramienta se han realizado las pruebas de rendimiento general de la aplicación web kitchentech ya desplegada, accesibilidad y mejores prácticas. La siguiente figura muestra los resultados de dichas pruebas.

![core system test](Resources/images/Capitulo%206/CoreSystemTest.jpg)
