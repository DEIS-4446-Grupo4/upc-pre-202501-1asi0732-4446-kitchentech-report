# Capítulo VIII: Experiment-Driven Development

## 8.1. Experiment Planning

Este capítulo se centra en la planificación de experimentos, que es una parte crucial del desarrollo impulsado por
experimentos. Aquí se definen las preguntas de investigación, se identifican las hipótesis y se planifican los
experimentos necesarios para validar o refutar estas hipótesis.

### 8.1.1. As-Is Summary

Kitchentech es una solución ERP para restaurantes, orientada a mejorar la eficiencia operativa y la experiencia del
usuario mediante nuevas funcionalidades. El desarrollo ágil permite iterar rápidamente, pero es fundamental validar el
impacto real de cada mejora a través de experimentos controlados y medibles

### 8.1.2. Raw Material: Assumptions, Knowledge Gaps, Ideas, Claims.

**Assumptions**:

1. Los usuarios de Kitchentech valoran la eficiencia operativa y la facilidad de uso.
2. Las nuevas funcionalidades propuestas pueden impactar positivamente la experiencia del usuario y la eficiencia
   operativa.
3. Los usuarios están dispuestos a adoptar nuevas características si estas son fáciles de usar y aportan valor.
4. Los usuarios tienen diferentes necesidades y preferencias que deben ser consideradas al diseñar nuevas
   características.
5. La implementación de nuevas características no afectará negativamente a las funcionalidades existentes.

**Knowledge Gaps**:

1. ¿Qué funcionalidades valoran más los usuarios actuales?
2. ¿Qué problemas específicos enfrentan los usuarios al utilizar Kitchentech?
3. ¿Cómo se pueden medir de manera efectiva las mejoras en la experiencia del usuario y la eficiencia operativa?
4. ¿Qué métricas son más relevantes para evaluar el éxito de las nuevas características?
5. ¿Qué impacto tendrán las nuevas características en la carga de trabajo de los usuarios y en la eficiencia operativa
   general?

**Ideas**:

1. Implementar un historial de pedidos por mesa para que los meseros puedan recuperar rápidamente información de pedidos
   activos o previos.
2. Desarrollar una función de división automática de cuentas entre comensales para agilizar el proceso de cobro.
3. Añadir un panel de "Top productos" en el dashboard del administrador para facilitar la toma de decisiones sobre el
   menú.
4. Habilitar una mensajería interna entre meseros y cocina para mejorar la comunicación y coordinación.

**Claims**:

1. La implementación de un historial de pedidos mejorará la precisión y velocidad del servicio.
2. La división automática de cuentas reducirá el tiempo de cobro y minimizará errores.
3. Mostrar los productos más vendidos optimizará la gestión del menú y aumentará las ventas.
4. Una mensajería interna mejorará la coordinación entre meseros y cocina, reduciendo errores.

### 8.1.3. Experiment-Ready Questions

1. ¿Tener un historial de pedidos por mesa mejora la precisión y velocidad del servicio?
2. ¿La visibilidad de los productos más vendidos mejora la gestión del menú?
3. ¿Una mensajería interna mejora la coordinación entre meseros y cocina?
4. ¿La implementación de un historial de pedidos reduce los errores en la toma de pedidos?
5. ¿La división automática de cuentas disminuye el tiempo de espera para los clientes?

### 8.1.4. Question Backlog

| # | Pregunta                                                                                | Impacto Potencial                       |
|---|-----------------------------------------------------------------------------------------|-----------------------------------------|
| 1 | ¿Tener un historial de pedidos por mesa mejora la precisión y velocidad del servicio?   | Alto (mejora servicio y reduce errores) |
| 2 | ¿La visibilidad de los productos más vendidos mejora la gestión del menú?               | Medio (optimiza decisiones de menú)     |
| 3 | ¿Una mensajería interna mejora la coordinación entre meseros y cocina?                  | Alto (reduce errores y demoras)         |
| 4 | ¿La implementación de un historial de pedidos reduce los errores en la toma de pedidos? | Alto (reduce errores operativos)        |
| 5 | ¿La división automática de cuentas disminuye el tiempo de espera para los clientes?     | Medio-Alto (agiliza cobro y rotación)   |

### 8.1.5. Experiment Cards

### 🧪 *Experiment Card 1: Historial de pedidos por mesa*

| *Supuestos*                                                                    | *Question Backlog*                                                                    |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| Los meseros suelen olvidar detalles de pedidos anteriores si deben retomarlos. | ¿Tener un historial de pedidos por mesa mejora la precisión y velocidad del servicio? |

| *Experiment Card* |                                                                                                                          |
|-------------------|--------------------------------------------------------------------------------------------------------------------------|
| *Question*        | ¿Tener un historial de pedidos por mesa mejora la precisión y velocidad del servicio?                                    |
| *Why*             | Permite a los meseros recuperar rápidamente información de pedidos activos o previos.                                    |
| *What*            | Agregar una sección de historial de pedidos por mesa en la app del mesero. Probar durante una semana.                    |
| *Hypothesis*      | Si los meseros consultan el historial de pedidos, reducirán errores en 30% y aumentarán la velocidad de atención en 10%. |
| *Métricas*        | Número de errores en pedidos y tiempo promedio por pedido.                                                               |
| *Metas*           | -30% en errores y +10% en velocidad de atención.                                                                         |

### 🧪 *Experiment Card 2: División automática de cuenta entre comensales*

| *Supuestos*                                                        | *Question Backlog*                                                               |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------|
| Dividir la cuenta manualmente toma tiempo y puede generar errores. | ¿Los meseros atienden más rápido si el sistema divide la cuenta automáticamente? |

| *Experiment Card* |                                                                                                              |
|-------------------|--------------------------------------------------------------------------------------------------------------|
| *Question*        | ¿Los meseros atienden más rápido si el sistema divide la cuenta automáticamente?                             |
| *Why*             | Mejora la eficiencia del cobro y reduce errores en cálculos, generando mayor rotación de mesas.              |
| *What*            | Implementar opción de división automática de cuenta por monto o ítems seleccionados.                         |
| *Hypothesis*      | Si se activa la división automática, se reduce el tiempo de cobro en un 20% y se eliminan errores en un 90%. |
| *Métricas*        | Tiempo desde solicitud de cuenta hasta cobro, y cantidad de reclamos por error.                              |
| *Metas*           | -20% en tiempo de cobro, -90% en errores.                                                                    |

---

### 🧪 *Experiment Card 3: Vista rápida de productos más vendidos*

| *Supuestos*                                                                  | *Question Backlog*                                                        |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| Los administradores toman decisiones sin datos concretos de productos clave. | ¿La visibilidad de los productos más vendidos mejora la gestión del menú? |

| *Experiment Card* |                                                                                                            |
|-------------------|------------------------------------------------------------------------------------------------------------|
| *Question*        | ¿La visibilidad de los productos más vendidos mejora la gestión del menú?                                  |
| *Why*             | Permite tomar decisiones informadas sobre promociones y stock.                                             |
| *What*            | Añadir panel de “Top productos” al dashboard de administrador y evaluar uso semanal.                       |
| *Hypothesis*      | Si se muestra el top de productos vendidos, los administradores optimizan el menú y aumentan ventas en 5%. |
| *Métricas*        | Variación en las ventas y cambios en el menú.                                                              |
| *Metas*           | +5% en ventas semanales.                                                                                   |

---

### 🧪 *Experiment Card 4: Mensajes internos entre meseros y cocina*

| *Supuestos*                                                                 | *Question Backlog*                                                     |
|-----------------------------------------------------------------------------|------------------------------------------------------------------------|
| La comunicación oral entre meseros y cocina puede causar errores o demoras. | ¿Una mensajería interna mejora la coordinación entre meseros y cocina? |

| *Experiment Card* |                                                                                               |
|-------------------|-----------------------------------------------------------------------------------------------|
| *Question*        | ¿Una mensajería interna mejora la coordinación entre meseros y cocina?                        |
| *Why*             | Mejora la velocidad y precisión en solicitudes especiales o cambios de último minuto.         |
| *What*            | Habilitar chat interno por pedidos con etiquetas (urgente, sin sal, etc.). Test en 2 turnos.  |
| *Hypothesis*      | Si se habilita mensajería interna, se reducirá el tiempo de resolución de incidencias en 30%. |
| *Métricas*        | Tiempos de respuesta y cantidad de errores en cocina.                                         |
| *Metas*           | -30% en tiempo de respuesta.                                                                  |

---

### 🧪 *Experiment Card 5: Agregado rápido de productos frecuentes o recientes*

| *Supuestos*                                                                  | *Question Backlog*                                                                           |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| Los usuarios suelen añadir repetidamente los mismos productos al inventario. | ¿Un acceso rápido a productos frecuentes o recientes reduce el tiempo de alta en inventario? |

| *Experiment Card* |                                                                                              |
|-------------------|----------------------------------------------------------------------------------------------|
| *Question*        | ¿Un acceso rápido a productos frecuentes o recientes reduce el tiempo de alta en inventario? |
| *Why*             | Agiliza la operación y disminuye errores por búsquedas manuales repetidas.                   |
| *What*            | Añadir botones para repetir productos recientes o frecuentes y medir el tiempo de registro.  |
| *Hypothesis*      | El tiempo en gestionar el inventario disminuye en al menos 25%.                              |
| *Métricas*        | Tiempo promedio de gestión del inventario.                                                   |
| *Metas*           | -25% en tiempo de demora en gestionar el inventario.                                         |

---

## 8.2. Experiment Design

### 8.2.1. Hypotheses

### 8.2.2. Measures

### 8.2.3. Conditions

### 8.2.4. Scale Calculations and Decisions

### 8.2.5. Methods Selection

### 8.2.6. Data Analytics: Goals, KPIs and Metrics Selection.

### 8.2.7. Web and Mobile Tracking Plan.

## 8.3. Experimentation

### 8.3.1. To-Be User Stories

| To-Be User Story ID | Título | Descripción | Criterios de aceptación |
|---|---|---|---|
| **Épica 1: Landing Page**<br>Como usuario<br>Quiero visualizar una página dedicada a la aplicación<br>Para saber acerca de ella e ingresar a la aplicación | | | |
| LP_US001 | Desarrollar el Header de la Web | COMO usuario QUIERO visualizar un encabezado de página que contenga opciones de navegación PARA poder desplazarme por la página. | **Escenario 1:** Se visualiza el header.<br>Dado que se visualiza el header. Cuando se ubique en la parte superior de la página. Entonces podrá visualizar las distintas opciones disponibles para navegar por la página.<br><br>**Escenario 2:** No se visualiza el header.<br>Dado que no se visualiza el header. Cuando se ubique en la parte superior de la página. Entonces no podrá navegar fácilmente. |
| LP_US002 | Desarrollar el Footer de la Web | COMO usuario QUIERO visualizar un pie de página que contenga información relevante del negocio PARA un mejor entendimiento del mismo. | **Escenario 1:** Se visualiza el footer.<br>Dado que se visualiza el footer. Cuando se ubique en la parte inferior de la página. Entonces podrá visualizar información relevante del negocio.<br><br>**Escenario 2:** No se visualiza el footer.<br>Dado que no se visualiza el footer. Cuando se ubique en la parte inferior de la página. Entonces no podrá visualizar información relevante del negocio. |
| LP_US003 | Desarrollar Barra de Navegación | COMO usuario QUIERO presionar botones en el header del landing page que me lleven a otras partes de la página PARA poder desplazarse con facilidad. | **Escenario 1:** Los botones funcionan correctamente.<br>Dado que se visualiza el header. Cuando se presione un botón de navegación. Entonces el usuario será redireccionado a otra sección de la web.<br><br>**Escenario 2:** Los botones no funcionan.<br>Dado que se visualiza el header. Cuando se presione un botón de navegación. Entonces el usuario se mantendrá en la sección actual sin ningún cambio. |
| LP_US004 | Implementar Sección sobre Descripción de la Start-Up | COMO usuario QUIERO observar una descripción del negocio PARA poder conocer sobre qué trata. | **Escenario 1:** Se visualiza la descripción de la Start-Up.<br>Dado que se visualiza la descripción de la Start-Up. Cuando se presione el botón de descripción. Entonces la vista del usuario se desplazará a la sección de la descripción.<br><br>**Escenario 2:** No se visualiza la descripción de la Start-Up.<br>Dado que no se visualiza la descripción de la Start-Up. Cuando se presione el botón de descripción. Entonces la vista del usuario se desplazará a la sección de la descripción pero no muestra información. |
| LP_US005 | Implementar Botón para ver más información | COMO usuario QUIERO visualizar más información PARA poder comprender y entender más sobre la start-up. | **Escenario 1:** El botón funciona correctamente.<br>Dado que el usuario se encuentra en la landing page. Cuando se presione el botón de "ver más". Entonces el usuario será redireccionado a una sección con mayor detalle del negocio.<br><br>**Escenario 2:** El botón no funciona.<br>Dado que el usuario se encuentra en la landing page. Cuando se presione el botón de "ver más". Entonces el usuario se mantendrá en la sección actual. |
| LP_US006 | Desarrollar Sección de Contacto | COMO usuario QUIERO observar una sección de “Contacto” PARA poder comunicarme directamente con el equipo de desarrollo. | **Escenario 1:** Se visualiza la información de contacto.<br>Dado que se visualiza la información de contacto. Cuando se presione el botón de contacto. Entonces la vista del usuario se desplazará a la sección de contacto.<br><br>**Escenario 2:** No se visualiza la información de contacto.<br>Dado que no se visualiza la información de contacto. Cuando se presione el botón de contacto. Entonces la vista del usuario se mantendrá en la sección actual. |
| LP_US007 | Desarrollar Sección de Información del Equipo | COMO usuario QUIERO poder observar información del equipo de desarrollo PARA conocer más de ellos. | **Escenario 1:** Se visualiza la información del equipo.<br>Dado que se visualiza la información del equipo. Cuando se presione el botón de "Equipo". Entonces la vista del usuario se desplazará a la sección de equipo.<br><br>**Escenario 2:** No se visualiza la información del equipo.<br>Dado que no se visualiza la información del equipo. Cuando se presione el botón de "Equipo". Entonces la vista del usuario se mantendrá en la sección actual. |
| **Épica 2: Funcionalidades de Autenticación y Seguridad**<br>Como usuario<br>Quiero validar mis datos y poder navegar en la aplicación<br>Para mantener mi cuenta segura y encontrar todas las secciones de forma rápida | | | |
| AS_US008 | Implementar Login con Credenciales | COMO usuario QUIERO acceder a la aplicación mediante un usuario y contraseña PARA mantener mi información del negocio segura. | **Escenario 1:** El usuario ingresa correctamente el usuario y contraseña.<br>Dado que el cliente ingresa sus credenciales válidas. Cuando dé clic al botón de "Ingresar". Entonces será dirigido a la página principal de la app.<br><br>**Escenario 2:** El usuario ingresa un usuario o contraseña incorrecto.<br>Dado que el cliente ingresó sus credenciales inválidas. Cuando dé clic al botón de "Ingresar". Entonces mostrará un mensaje de error. |
| AS_US009 | Implementar Botón para Cerrar Sesión | COMO usuario QUIERO salir de la aplicación PARA evitar el uso de mi cuenta en manos de otras personas. | **Escenario 1:** El usuario cierra sesión correctamente.<br>Dado que el usuario quiere cerrar su sesión. Cuando le dé clic al botón de “Cerrar sesión”. Entonces se cerrará la sesión del usuario y se redireccionará a la página principal.<br><br>**Escenario 2:** El usuario no puede cerrar sesión.<br>Dado que el usuario quiere cerrar su sesión. Cuando le dé clic al botón de “Cerrar sesión”. Entonces se mostrará un mensaje de error y se mantendrá en la vista actual. |
| AS_US010 | Implementar Método de Recuperación de Contraseña | COMO cliente QUIERO recuperar mi contraseña PARA ingresar a la aplicación. | **Escenario 1:** El usuario recupera su contraseña con éxito.<br>Dado que el usuario olvidó su contraseña. Cuando el usuario presione el botón de “Recuperar contraseña”. Entonces será dirigido a una página donde se realizará una validación mediante su correo electrónico, dirigiéndolo a una nueva página para cambiar su contraseña.<br><br>**Escenario 2:** El usuario no tiene acceso a su correo vinculado.<br>Dado que el usuario olvidó su contraseña y presionó el botón de “Recuperar contraseña”. Cuando se le envía el correo de confirmación y no pueda acceder a él. Entonces no puede restablecer su contraseña.<br><br>**Escenario 3:** El usuario falla al crear una nueva contraseña.<br>Dado que el usuario olvidó su contraseña y presionó el botón de “Recuperar contraseña”. Cuando se le envía el correo de confirmación y se le solicite crear una nueva contraseña y no cumpla con los requisitos. Entonces se mostrará una alerta solicitando modificar la contraseña. |
| AS_US011 | Implementar Navegación mediante Menú | COMO usuario QUIERO visualizar un menú PARA acceder a las funciones de la aplicación de forma más rápida y sencilla. | **Escenario 1:** El usuario visualiza el menú y funcionan correctamente los botones.<br>Dado que el usuario visualiza correctamente el menú. Cuando da clic en algún botón de este. Entonces es redirigido a la sección correspondiente.<br><br>**Escenario 2:** El usuario visualiza el menú pero no funcionan los botones.<br>Dado que el usuario visualiza correctamente el menú. Cuando da clic en algún botón de este. Entonces no ocurre nada, manteniéndose en la sección en la que se encuentra.<br><br>**Escenario 3:** El usuario no visualiza el menú.<br>Dado que el usuario no visualiza el menú. Cuando intente navegar por la aplicación. Entonces tendrá dificultades para llegar a la sección deseada de manera rápida. |
| AS_US012 | Implementar Vista de Inicio de Sesión | COMO usuario QUIERO poder ingresar a mi cuenta PARA poder acceder a las funcionalidades. | **Escenario 1:** El usuario visualiza la vista de iniciar sesión.<br>Dado que el usuario visualiza el inicio de sesión. Cuando intente ingresar sus credenciales. Entonces podrá ingresar a la aplicación.<br><br>**Escenario 2:** El usuario no visualiza la vista de iniciar sesión.<br>Dado que el usuario no puede visualizar el inicio de sesión. Cuando no encuentre cómo ingresar a la aplicación. Entonces el usuario generará un reporte al negocio por un mal funcionamiento de la plataforma. |
| AS_US013 | Implementar Sección de Registro | COMO usuario QUIERO visualizar una opción que me permita registrarme con un plan para mi negocio PARA poder tener acceso a las funcionalidades de la aplicación. | **Escenario 1:** El usuario crea correctamente su usuario.<br>Dado que el usuario intenta crear un usuario. Cuando realice todos los pasos y seleccione un plan. Entonces su usuario será creado y será redireccionado a la pestaña de Login.<br><br>**Escenario 2:** El usuario no puede crear su usuario.<br>Dado que el usuario intenta crear un usuario. Cuando realice todos los pasos y seleccione un plan pero exista una falla en el sistema. Entonces se desplegará una alerta informando que se intente nuevamente más tarde.<br><br>**Escenario 3:** El usuario no puede crear su usuario por no seleccionar un plan.<br>Dado que el usuario intenta crear un usuario. Cuando realice todos los pasos y seleccione un plan pero no seleccione un plan de pago. Entonces se desplegará una alerta informando que debe seleccionar un plan y configurar un método de pago. |
| **Épica 3: Gestión de Perfil y Preferencias de Usuario**<br>Como usuario<br>Quiero visualizar una sección para mi perfil<br>Para saber los datos que tengo y poder modificarlos cuando quiera | | | |
| GP_US014 | Dirigir a Perfil de Usuario | COMO usuario QUIERO ir a mi perfil PARA cambiar cualquier dato que necesite actualización. | **Escenario 1:** El usuario es redireccionado a su perfil.<br>Dado que el perfil de usuario funciona. Cuando el usuario dé clic en el botón de perfil. Entonces será redirigido a su perfil.<br><br>**Escenario 2:** El usuario no es redireccionado a su perfil.<br>Dado que el perfil de usuario no se encuentra en funcionamiento. Cuando el usuario dé clic en el botón de perfil. Entonces no será redirigido a su perfil, en cambio se mantendrá en la vista actual. |
| GP_US015 | Ver y Editar Datos de Usuario | COMO usuario QUIERO ver y editar mi información PARA mantenerla actualizada. | **Escenario 1:** El usuario visualiza su información.<br>Dado que el usuario desea ver su información. Cuando da clic en el botón perfil. Entonces visualiza su información.<br><br>**Escenario 2:** El usuario modifica su información.<br>Dado que el usuario quiere modificar su información y el sistema funciona correctamente. Cuando da clic en el botón de "modificar perfil" dentro del perfil, cambia su información y da clic en el botón "guardar". Entonces actualiza su información correctamente.<br><br>**Escenario 3:** El usuario no es capaz de modificar su información.<br>Dado que el usuario quiere modificar su información y el sistema no funciona según lo esperado. Cuando da clic en el botón de "modificar perfil" dentro del perfil, cambia su información y da clic en el botón "guardar". Entonces se mostrará una alerta indicando que hubo un error en el sistema. |
| **Épica 4: Notificación de Servicio**<br>Como usuario mesero<br>Quiero poder recibir notificaciones sobre el estado de un cliente y su orden.<br>Para poder tener mayor eficiencia al atender. | | | |
| NS_US016 | Recibir Alerta cuando un Cliente Entra al Local | COMO mesero QUIERO recibir una alerta cuando un cliente cruza la puerta del local PARA poder atenderlo a la brevedad. | **Escenario 1:** Una notificación es mandada al sistema.<br>Dado que soy un mesero y el sistema funciona correctamente. Cuando un cliente cruza la puerta del local. Entonces visualizo en el sistema una alerta de ello.<br><br>**Escenario 2:** No se envía correctamente la notificación.<br>Dado que soy un mesero pero el sistema no funciona según lo esperado. Cuando un cliente cruza la puerta del local. Entonces no se visualiza ninguna alerta en el sistema. |
| NS_US017 | Recibir Alerta cuando un Cliente se Sienta | COMO mesero QUIERO recibir una alerta cuando un cliente se sienta en alguna mesa PARA poder generar el pedido en dicha mesa. | **Escenario 1:** Se recibe una alerta cuando un cliente se sienta.<br>Dado que un cliente ingresa al local. Cuando se sienta en alguna mesa. Entonces se muestra una alerta en el sistema indicando el hecho.<br><br>**Escenario 2:** No se recibe la alerta cuando un cliente se sienta.<br>Dado que un cliente ingresa al local. Cuando se sienta en alguna silla. Entonces no se muestra ninguna alerta, dificultando su atención. |
| NS_US018 | Recibir Alerta cuando un Cliente Deja la Mesa | COMO mesero QUIERO recibir una alerta cuando un cliente deja la mesa PARA poder verificar si su cuenta fue cancelada. | **Escenario 1:** Se muestra una alerta cuando un cliente deja la mesa.<br>Dado que un cliente ha consumido en el local. Cuando deja su mesa y se muestra una alerta en el sistema indicando esto así como un link a su cuenta. Entonces puedo verificar si su cuenta fue cancelada.<br><br>**Escenario 2:** No se muestra una alerta cuando un cliente deja la mesa.<br>Dado que un cliente ha consumido en el local. Cuando deja su mesa y no se muestra una alerta en el sistema. Entonces no puedo estar atento de verificar si su cuenta fue cancelada. |
| NS_US019 | Recibir Alerta cuando hay Platos en Mesa sin Cliente | COMO mesero QUIERO recibir una alerta cuando hay platos en la mesa y no hay cliente en ella PARA darme cuenta y recoger los platos sucios. | **Escenario 1:** Se envía una alerta de platos en mesa.<br>Dado que un cliente consumió y dejó su mesa. Cuando hayan platos en la mesa y no un cliente sentado. Entonces se enviará una alerta para recoger los platos.<br><br>**Escenario 2:** No se envía ninguna alerta de platos en mesa.<br>Dado que un cliente consumió y dejó su mesa pero el sistema no funcione. Cuando hayan platos en la mesa y no un cliente sentado. Entonces no se enviará una alerta evitando que el mesero se percate de ello dejando el local sucio. |
| **Épica 5: Toma de Pedidos**<br>Como usuario mesero<br>Quiero poder tomar pedidos y enviarlos a otras áreas.<br>Para poder agilizar el flujo de trabajo. | | | |
| TP_US020 | Tomar Pedidos de la Mesa | COMO mesero QUIERO poder tomar pedidos desde una aplicación PARA poder agilizar la toma de órdenes. | **Escenario 1:** La función de agregar pedidos a la orden funciona correctamente.<br>Dado que soy un mesero. Cuando quiero agregar un producto al pedido. Entonces se agrega correctamente a la orden.<br><br>**Escenario 2:** La función de agregar pedidos a la orden no funciona.<br>Dado que soy un mesero. Cuando quiero agregar un producto al pedido y no funciona el sistema. Entonces no se agrega el producto y debo tomarlo manualmente perdiendo tiempo. |
| TP_US021 | Guardar Orden | COMO mesero QUIERO poder guardar las órdenes de una mesa PARA enviarlos a caja o cocina. | **Escenario 1:** La función de guardar órdenes funciona correctamente.<br>Dado que soy un mesero. Cuando quiero guardar un pedido. Entonces se guarda correctamente.<br><br>**Escenario 2:** La función de guardar órdenes no funciona.<br>Dado que soy un mesero. Cuando quiero guardar la orden y no funciona el sistema. Entonces no se guarda y debo tomarlo manualmente perdiendo tiempo. |
| TP_US022 | Enviar Pedido Guardado a Cocina y Caja | COMO mesero QUIERO poder enviar pedidos a cocina o caja PARA poder continuar con el flujo de trabajo sin necesidad de dictar la orden personalmente demorando la atención de otros pedidos. | **Escenario 1:** La función de enviar órdenes funciona correctamente.<br>Dado que soy un mesero. Cuando quiero enviar una orden a cocina o caja y el sistema funciona. Entonces se envía correctamente.<br><br>**Escenario 2:** La función de enviar órdenes no funciona.<br>Dado que soy un mesero. Cuando quiero enviar una orden a cocina o caja y el sistema no funciona. Entonces no se envía la orden provocando que lo tenga que llevar manualmente. |
| **Épica 6: Facturación del Negocio**<br>Como usuario administrador<br>Quiero realizar facturaciones.<br>Para brindarle al cliente su comprobante de pago. | | | |
| FN_US023 | Crear un Cliente con DNI o RUC | COMO administrador QUIERO crear nuevos clientes con DNI o RUC PARA poder crear documentos de venta personalizados. | **Escenario 1:** El sistema se vincula con SUNAT.<br>Dado que soy un administrador. Cuando intento agregar un cliente y el sistema con SUNAT funciona. Entonces se encuentra al cliente rápidamente.<br><br>**Escenario 2:** El vínculo con SUNAT no funciona.<br>Dado que soy un administrador. Cuando intento agregar un cliente y el sistema con SUNAT no funciona. Entonces debo llenar los campos de RUC/DNI, nombre del cliente/empresa y dirección de facturación. |
| FN_US024 | Imprimir Pre-cuenta | COMO administrador QUIERO poder imprimir el resumen de una orden PARA poder brindarle al cliente previo al pago. | **Escenario 1:** Se imprime la pre-cuenta correctamente.<br>Dado que soy un administrador. Cuando me solicitan imprimir la pre-cuenta y le doy clic al botón correspondiente. Entonces se imprime y se la entrego al cliente o mesero.<br><br>**Escenario 2:** No se imprime la pre-cuenta.<br>Dado que soy un administrador. Cuando me solicitan imprimir la pre-cuenta y le doy clic al botón correspondiente pero no funciona. Entonces no se imprime y el cliente o mesero queda inconforme. |
| FN_US025 | Cobrar Orden | COMO administrador QUIERO poder cobrar la orden de un cliente con diversos métodos de pago PARA brindar comodidad al cliente. | **Escenario 1:** Se cobra la orden.<br>Dado que soy un administrador. Cuando quiero cobrar la orden con diversos métodos de pago. Entonces los métodos de pago son añadidos y se cobra la orden.<br><br>**Escenario 2:** No se cobra la orden.<br>Dado que soy un administrador. Cuando quiero cobrar la orden con diversos métodos de pago y el sistema no funciona. Entonces no se añaden los métodos de pago y no puedo cobrar la orden. |
| FN_US026 | Boletear o Facturar la Orden | COMO administrador QUIERO poder boletear o facturar la orden del cliente cerrando la orden PARA poder emitir los documentos a la SUNAT. | **Escenario 1:** Se emite documento de venta.<br>Dado que soy un administrador. Cuando quiero emitir un documento de venta y el sistema funciona. Entonces se imprime el documento.<br><br>**Escenario 2:** No se emite documento de venta.<br>Dado que soy un administrador. Cuando quiero emitir un documento de venta y el sistema no funciona. Entonces no se imprime el documento y se muestra un error en pantalla. |
| **Épica 7: Control de Inventarios**<br>Como usuario administrador<br>Quiero poder ver un resumen de los platos vendidos y cuánto se consumió en cada uno.<br>Para poder llevar un control de mis inventarios como negocio. | | | |
| CI_US027 | Ver Resumen de Ventas | COMO administrador QUIERO poder ver el resumen de ventas por días PARA poder saber cuánto se vendió. | **Escenario 1:** Se puede ver el resumen de ventas.<br>Dado que soy administrador. Cuando ingreso a la sección de reportes de ventas. Entonces puedo ver un gráfico con el resumen de ventas y diversos filtros.<br><br>**Escenario 2:** El resumen de ventas no carga correctamente.<br>Dado que soy administrador. Cuando ingreso a la sección de reportes de ventas y no funciona. Entonces no se generan los gráficos y se muestra un error indicando que no se pudo cargar el reporte. |
| CI_US028 | Filtrar Ventas por Platos | COMO administrador QUIERO poder filtrar las ventas por platos PARA saber qué platos se vendieron más que otros. | **Escenario 1:** La función de filtrar ventas por platos funciona.<br>Dado que soy un administrador. Cuando selecciono la opción de filtrar por plato en el reporte. Entonces puedo ver la lista de ventas según cada plato.<br><br>**Escenario 2:** Dado que soy un administrador. Cuando selecciono la opción de filtrar por plato en el reporte y este no funciona. Entonces se muestra un error indicando que no se pudo seleccionar el filtro. |
| CI_US029 | Ver Resumen de Productos Restantes | COMO administrador QUIERO saber cuántos insumos me quedan en stock después de haber vendido los platos PARA poder llevar un buen inventario. | **Escenario 1:** La sección de ver resumen de productos restantes funciona.<br>Dado que soy administrador. Cuando accedo a la sección de inventario. Entonces puedo ver una lista detallada de todos los insumos en stock, incluyendo su cantidad.<br><br>**Escenario 2:** No se actualiza el reporte en tiempo real.<br>Dado que soy administrador. Cuando accedo a la sección de inventario y no se actualiza con las ventas de platos. Entonces se muestra un mensaje indicando que los datos podrían estar desactualizados. |
| CI_US030 | Ingresar Nuevos Productos al Inventario | COMO administrador QUIERO añadir insumos a mi stock al momento de realizar una compra PARA poder mantener mi inventario actualizado. | **Escenario 1:** Se agrega insumo nuevo correctamente.<br>Dado que soy administrador. Cuando quiero agregar un insumo nuevo, lleno los campos y doy clic al botón crear. Entonces el producto se añade correctamente.<br><br>**Escenario 2:** El insumo ingresado ya existe.<br>Dado que soy administrador. Cuando quiero agregar un producto nuevo y este ya existe. Entonces muestra una alerta indicando que se modifique el nombre del producto.<br><br>**Escenario 3:** No se puede agregar el nuevo insumo.<br>Dado que soy administrador. Cuando quiero agregar un producto nuevo, lleno los campos y doy clic al botón crear pero el sistema no funciona. Entonces el insumo no se añade y muestra una alerta indicando el error. |
| CI_US031 | Crear Platos Nuevos | COMO administrador QUIERO poder crear nuevos platos con sus precios, insumos necesarios, etc. PARA que los meseros puedan seleccionarlos al momento de tomar una orden. | **Escenario 1:** Se agrega plato nuevo correctamente.<br>Dado que soy administrador. Cuando quiero agregar un plato nuevo, lleno los campos y doy clic al botón crear. Entonces el plato se añade correctamente.<br><br>**Escenario 2:** El plato ingresado ya existe.<br>Dado que soy administrador. Cuando quiero agregar un plato nuevo y este ya existe. Entonces muestra una alerta indicando que se modifique el nombre del plato.<br><br>**Escenario 3:** No se puede agregar el nuevo plato.<br>Dado que soy administrador. Cuando quiero agregar un plato nuevo, lleno los campos y doy clic al botón crear pero el sistema no funciona. Entonces el plato no se añade y muestra una alerta indicando el error. |
| CI_US032 | Editar Insumos Existentes | COMO administrador QUIERO poder editar los datos de los insumos que ya tengo creados PARA poder actualizarlos en caso sea necesario. | **Escenario 1:** Se modifica el insumo correctamente.<br>Dado que soy administrador. Cuando quiero modificar un insumo y le doy clic al botón guardar. Entonces el insumo se modifica correctamente.<br><br>**Escenario 2:** No es posible modificar el insumo.<br>Dado que soy administrador. Cuando quiero modificar un insumo y le doy clic al botón guardar pero el sistema no funciona. Entonces el insumo no se modifica y se muestra una alerta indicando el error. |
| CI_US033 | Eliminar Insumos Existentes | COMO administrador QUIERO poder eliminar los insumos existentes PARA mantener mis platos actualizados. | **Escenario 1:** El producto se elimina correctamente.<br>Dado que soy administrador. Cuando doy clic al botón de eliminar producto. Entonces el producto se elimina correctamente.<br><br>**Escenario 2:** El producto no ha sido eliminado.<br>Dado que soy administrador. Cuando doy clic al botón de eliminar insumo pero el sistema no funciona. Entonces el producto no se elimina y muestra un mensaje de error. |
| **Épica 8: Estadísticas de Negocio**<br>Como Administrador del Restaurante<br>Quiero visualizar gráficos de las cuentas creadas mensualmente y del desempeño del personal en la atención que brinda<br>Para monitorear la eficiencia de la aplicación en la empresa. | | | |
| EN_US034 | Ver Resumen de Ventas Detallado | COMO administrador QUIERO visualizar un resumen de las ventas realizadas POR cada período de tiempo PARA analizar el rendimiento de los platos y tomar decisiones informadas. | **Escenario 1:** El resumen de ventas se muestra correctamente.<br>Dado que soy administrador. Cuando selecciono un período de tiempo en el filtro y solicito el resumen de ventas. Entonces el sistema genera y muestra un informe con los datos de ventas detallados y organizados por plato, fecha y cantidad.<br><br>**Escenario 2:** El resumen de ventas no se muestra.<br>Dado que soy administrador. Cuando selecciono un período de tiempo y solicito el resumen, pero ocurre un error en el sistema. Entonces se muestra un mensaje indicando que el resumen de ventas no está disponible en ese momento y recomendando reintentar más tarde. |
| EN_US035 | Filtrar Ventas por Producto Específico | COMO administrador QUIERO filtrar las ventas por productos específicos PARA identificar los más vendidos y optimizar la oferta del menú. | **Escenario 1:** Las ventas filtradas por producto se muestran correctamente.<br>Dado que soy administrador. Cuando selecciono un producto específico en el filtro y solicito ver las ventas. Entonces el sistema muestra un resumen detallado de las ventas relacionadas con ese producto, incluyendo fecha, cantidad vendida y total generado.<br><br>**Escenario 2:** Las ventas filtradas por producto no se muestran.<br>Dado que soy administrador. Cuando selecciono un producto específico en el filtro y solicito las ventas, pero ocurre un error en el sistema. Entonces se muestra un mensaje indicando que las ventas no están disponibles en ese momento y recomendando reintentar más tarde. |
| EN_US036 | Generar Salida de Dinero en Caja | COMO administrador QUIERO registrar las salidas de dinero de la caja PARA llevar un control preciso de los movimientos financieros y justificar los gastos realizados. | **Escenario 1:** La salida de dinero se registra correctamente.<br>Dado que soy administrador. Cuando ingreso los detalles de una salida de dinero, como el monto, la fecha, y el motivo, y hago clic en "Registrar salida". Entonces el sistema guarda la información correctamente y la muestra en el historial de movimientos financieros.<br><br>**Escenario 2:** El sistema muestra un error al registrar la salida.<br>Dado que soy administrador. Cuando ingreso los detalles de una salida de dinero y hago clic en "Registrar salida", pero ocurre un error en el sistema. Entonces se muestra un mensaje de error indicando que no se pudo completar el registro y sugiriendo reintentar o contactar al soporte técnico. |
| EN_US037 | Generar Ingreso de Dinero en Caja | COMO administrador QUIERO registrar los ingresos de dinero en la caja PARA llevar un control financiero y justificar los depósitos realizados. | **Escenario 1:** El ingreso de dinero se registra correctamente.<br>Dado que soy administrador. Cuando ingreso los detalles de un ingreso de dinero, como el monto, la fecha, y el motivo, y hago clic en "Registrar ingreso". Entonces el sistema guarda la información correctamente y la muestra en el historial de movimientos financieros.<br><br>**Escenario 2:** El sistema muestra un error al registrar el ingreso.<br>Dado que soy administrador. Cuando ingreso los detalles de un ingreso de dinero y hago clic en "Registrar ingreso", pero ocurre un error en el sistema. Entonces se muestra un mensaje de error indicando que no se pudo completar el registro y sugiriendo reintentar o contactar al soporte técnico. |
| EN_US038 | Ver Historial de Ventas Completas | COMO administrador QUIERO visualizar el historial de ventas realizadas PARA analizar el rendimiento general de la caja y realizar auditorías. | **Escenario 1:** El historial de ventas se muestra correctamente.<br>Dado que soy administrador. Cuando accedo a la sección de historial de ventas y selecciono un rango de fechas. Entonces el sistema muestra un listado detallado con las transacciones realizadas, incluyendo fecha, productos vendidos y montos.<br><br>**Escenario 2:** El historial de ventas no se muestra.<br>Dado que soy administrador. Cuando accedo a la sección de historial de ventas y selecciono un rango de fechas, pero ocurre un error en el sistema. Entonces se muestra un mensaje indicando que los datos no están disponibles y sugiriendo reintentar más tarde o contactar al soporte técnico. |
| EN_US039 | Ver Resumen de Inventario Actual | COMO administrador QUIERO visualizar un resumen de los productos restantes en inventario PARA gestionar las existencias y planificar compras de manera eficiente. | **Escenario 1:** El resumen de productos restantes se muestra correctamente.<br>Dado que soy administrador. Cuando accedo a la sección de inventario y solicito el resumen de productos. Entonces el sistema genera un informe con las cantidades disponibles de cada producto, organizadas por categoría y prioridad.<br><br>**Escenario 2:** El resumen de productos restantes no se muestra.<br>Dado que soy administrador. Cuando accedo a la sección de inventario y solicito el resumen de productos, pero ocurre un error en el sistema. Entonces se muestra un mensaje indicando que el resumen no está disponible y sugiriendo reintentar más tarde o contactar al soporte técnico. |

### 8.3.2. To-Be Product Backlog


