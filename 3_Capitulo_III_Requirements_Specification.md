# Capítulo III: Requirements Specification

## 3.1. To-Be Scenario Mapping.
En la siguiente seccion, presentaremos el Mapeo de Escenarios Futuros específicamente diseñado para el proyecto. Este mapa representa una visión de cómo se implementan cambios y mejoras en los procesos y sistemas. A continuación, se incluye una representación gráfica del mismo: 
- Segmento de Mesero:

<img src="./Resources/images/sm1.png" >

- Segmento de Administrador

<img src="./Resources/images/sm2.png" >

## 3.2. User Stories.


<table>
  <tr>
    <th>Epic / Story ID</th>
    <th>Title</th>
    <th>Descripción</th>
    <th>Criterios de Aceptación</th>
  </tr>
  <tr>
    <td colspan="4"><strong>Épica 1: Landing page</strong><br>Como usuario<br>Quiero visualizar una página dedicada a la aplicación<br>Para saber acerca de ella e ingresar a la aplicación</td>
  </tr>
  <tr>
    <td>E01_US001</td>
    <td>Desarrollar el header de la web</td>
    <td>COMO usuario QUIERO visualizar un encabezado de página que contenga opciones de navegación PARA poder desplazarme por la página</td>
    <td><strong>Escenario 1:</strong> Se visualiza el header<br>Dado que se visualiza el header. Cuando se ubique en la parte superior de la página. Entonces podrá visualizar las distintas opciones disponibles para navegar por la página.<br><br><strong>Escenario 2:</strong> No se visualiza el header. Dado que no se visualiza el header.      Cuando se ubique en la parte superior de la página.<br>Entonces no podrá navegar fácilmente.</td>
  </tr>
  <tr>
    <td>E01_US002</td>
    <td>Desarrollar el footer de la web</td>
    <td>COMO usuario QUIERO visualizar un pie de página que contenga información relevante del negocio PARA un mejor entendimiento del mismo. </td>
    <td><strong>Escenario 1:</strong> Se visualiza el footer<br>Dado que se visualiza el footer.<br>Cuando se ubique en la parte inferior de la página.<br>Entonces podrá visualizar informacion relevante del negocio. <br><br><strong>Escenario 2:</strong> No se visualiza el footer<br>Dado que no se visualiza el header.<br>Cuando se ubique en la parte inferior de la pagina.<br>Entonces no podra visualizar informacion relevante del negocio</td>
  </tr>
  <tr>
    <td>E01_US003</td>
    <td>Desarrollar Barra de Navegación</td>
    <td>COMO usuario QUIERO presionar botones en el header del landing page que me lleven a otras partes de la página PARA poder desplazarme con facilidad.</td>
    <td><strong>Escenario1:</strong> Los botones funcionan correctamente.<br>Dado que se visualiza el header. Cuando se presione un boton de navegacion. Entonces el usuario sera redireccionado a otra seccion de la web. <br><br><strong>Escenario 2:</strong> Los botones no funcionan.<br>Dado que se visualiza el header. Cuando se presione un boton de navegacion. Entonces el usuario se mantendra en la seccion actual sin ningun cambio</td>
  </tr>
  <tr>
    <td>E01_US004</td>
    <td>Implementar seccion sobre Descripción de la Start-Up</td>
    <td>COMO usuario QUIERO observar una descripcion del negocio PARA poder conocer sobre qué trata.</td>
    <td><strong>Escenario 1:</strong> Se visualiza la descripcion de la Start-Up<br>Dado que se visualiza la descripcion de la Start-Up. Cuando se presione el boton de descripcion. Entonces la vista del usuario se desplazara a la seccion de la descripcion.<br><br><strong>Escenario 2:</strong> No se visualiza la descripcion de la Start-Up<br>Dado que no se visualiza la descripcion de la Start-Up. Cuando se presione el boton de descripcion. Entonces la vista del usuario se desplazara a la seccion de la descripcion pero no muestra informacion. </td>
  </tr>
  <tr>
    <td>E01_US005</td>
    <td>Implementar Botón para ver más información </td>
    <td>COMO usuario QUIERO visualizar más información PARA poder comprender y entender más sobre la start-up.</td>
    <td><strong>Escenario 1:</strong> El boton funciona correctamente<br>Dado que el usuario se encuentra en la landing page. Cuando se presione el boton de ver mas. Entonces el usuario sera redireccionado a una seccion con mayor detalle del negocio.<br><br> <strong>Escenario 2:</strong> El boton no funciona. <br>Dado que el usuario se encuentra en la landing page. Cuando se presione el boton de ver mas. Entonces el usuario se mantendra en la seccion actual. </td>
  </tr>
  <tr>
    <td>E01_US006</td>
    <td>Desarrollar Sección de contacto</td>
    <td>COMO usuario QUIERO observar una seccion de “Contacto” PARA poder comunicarme directamente con el equipo de desarrollo.</td>
    <td><strong>Escenario 1:</strong> Se visualiza la informacion de contacto <br>Dado que se visualiza la informacion de contacto. Cuando se presione el boton de contacto. Entonces la vista del usuario se desplazara a la seccion de contacto.<br><br> <strong>Escenario 2:</strong> No se visualiza la informacion de contacto.<br>Dado que no se visualiza la informacion de contacto. Cuando se presione el boton de contacto. Entonces la vista del usuario se mantendra en la seccion actual.</td>
  </tr>
  <tr>
    <td>E01_US007</td>
    <td>Desarrollar Sección de información del equipo </td>
    <td>COMO usuario QUIERO poder observar informacion del equipo de desarrollo PARA conocer más de ellos </td>
    <td><strong>Escenario 1:</strong> Se visualiza la informacion del equipo.<br>Dado que se visualiza la informacion del equipo. Cuando se presione el boton de "Equipo". Entonces la vista del usuario se desplazara a la seccion de equipo.<br><br> <strong>Escenario 2:</strong> No se visualiza la informacion del equipo.<br>Dado que no se visualiza la informacion del equipo.Cuando se presione el boton de "Equipo".Entonces la vista del usuario se mantendra en la seccion actual.</td>
  </tr>
  <tr>
    <td>E01_TS001</td>
    <td>Optimizar la velocidad de carga de la Landing Page</td>
    <td>COMO desarrollador QUIERO optimizar la velocidad de carga de la página PARA brindar comodidad al usuario</td>
    <td><strong>Escenario 1:</strong> La página cargará en menos de 3 segundos.<br>Dado que la página carga en menos de 3 segundos. Cuando un usuario ingresa en ella. Entonces está conforme con el servicio brindado<br><br> <strong>Escenario 2:</strong> La página cargará en 3 segundos o más.<br>Dado que la página demora en cargar 3 segundos o más. Cuando un usuario ingresa en ella. Entonces no está conforme con el servicio brindado.</td>
  </tr>
  <tr>
    <td colspan="4"><strong>Épica 2: Funcionalidades de Autenticación y Seguridad </strong><br>Como usuario<br>Quiero validar mis datos y poder navegar en la aplicación<br>Para mantener mi cuenta segura y encontrar todas las secciones de forma rápida</td>
  </tr>
  <tr>
    <td>E02_US008</td>
    <td>Implementar Login con PIN/clave</td>
    <td>COMO usuario QUIERO acceder a la aplicación mediante un usuario y contraseña PARA mantener mi información del negocio segura</td>
    <td><strong>Escenario 1:</strong> El usuario ingresa correctamente el usuario y contraseña.<br>Dado que el cliente ingresa sus credenciales válidas. Cuando dé click al botón de "Ingresar". Entonces será dirigido a la página principal de la app. <br><br> <strong>Escenario 2:</strong> El usuario ingresa un usuario o contraseña incorrecto. <br>Dado que el cliente ingresó sus credenciales inválidas. Cuando dé click al botón de "Ingresar". Entonces mostrará un mensaje de error</td>
  </tr>
  <tr>
    <td>E02_US009</td>
    <td>Implementar boton para Cerrar Sesion</td>
    <td>COMO usuario QUIERO salir de la aplicación PARA evitar el uso de mi cuenta en manos de otras personas.</td>
    <td><strong>Escenario 1:</strong> El usuario cierra sesión correctamente.<br>Dado que el usuario quiere cerrar su sesión. Cuando le de click al botón de “Cerrar sesión”. Entonces se cerrara la sesion del usuario y se redireccionara a la pagina principal. <br><br> <strong>Escenario 2:</strong> El usuario no puede cerrar sesion. <br>Dado que el usuario quiere cerrar su sesion. Cuando le de click al botón de “Cerrar sesión”. Entonces se mostrara un mensaje de error y se mantendra en la vista actual.</td>
  </tr>
  <tr>
    <td>E02_US010</td>
    <td>Implementar metodo de Recuperacion de contraseña</td>
    <td>COMO cliente QUIERO recuperar mi contraseña PARA ingresar a la aplicación. </td>
    <td><strong>Escenario 1:</strong> El usuario recuperar su contraseña con exito.<br>Dado que el usuario olvido su contraseña. Cuando el usuario presione el botón de “Recuperar contraseña”. Entonces será dirigido a una página donde se realizará una validación mediante su correo electrónico, dirigiendolo a una nueva pagina para cambiar su contraseña.<br><br> <strong>Escenario 2:</strong> El usuario no tiene acceso a su correo vinculado.<br>Dado que el usuario olvido su contraseña y presiono el botón de “Recuperar contraseña”. Cuando se le envia el correo de confirmacion y no pueda acceder a el. Entonces no puede restablecer su contraseña <br><br> <strong>Escenario 3:</strong> El usuario falla al crear una nueva constraseña.<br>Dado que el usuario olvido su contraseña y presiono el botón de “Recuperar contraseña”. Cuando se le envia el correo de confirmacion y  se le solicite crear una nueva contraseña y no cumpla con los requisitos. Entonces se mostrara una alerta solicitando modificar la contraseña.</td>
  </tr>
  <tr>
    <td>E02_US011</td>
    <td>Implementar navegacion mediante Menú.</td>
    <td>COMO usuario QUIERO visualizar un menú PARA acceder a las funciones de la aplicación de forma más rápida y sencilla.</td>
    <td><strong>Escenario 1:</strong> El usuario visualiza el menu y funcionan correctamente los botones.<br>Dado que el usuario visualiza correctamente el menu. Cuando da click en algun boton de este. Entonces es redirigido a la seccion correspondiente. <br><br> <strong>Escenario 2:</strong> El usuario visualiza el menu pero no funcionan los botones<br>Dado que el usuario visualiza correctamente el menu. Cuando da click en algun boton de este. Entonces no ocurre nada manteniendose en la seccion en la que se encuentra. <br><br><strong>Escenario 3:</strong> El usuario no visualiza el menu <br>Dado que el usuario no visualiza el menu. Cuando intente navegar por la aplicacion. Entonces tendra dificultades para llegar a la seccion deseada de manera rapida</td>
  </tr>
  <tr>
    <td>E02_US012</td>
    <td>Implementar vista de inicio de sesión.</td>
    <td>COMO usuario QUIERO poder ingresar a mi cuenta PARA poder acceder a las funcionalidades.</td>
    <td><strong>Escenario 1:</strong> El usuario visualiza la vista de iniciar sesion. <br>Dado que el usuario visualiza el inicio de sesion. Cuando intente ingresar sus credenciales. Entonces podra ingresar a la aplicacion.<br><br> <strong>Escenario 2:</strong> El usuario no visualiza la vista de iniciar sesion.<br>Dado que el usuario no puede visualizar el inicio de sesion. Cuando no encuentre como ingresar a la aplicacion. Entonces el usuario generara un reporte al negocio por un mal funcionamiento de la plataforma.</td>
  </tr>
  <tr>
    <td>E02_US013</td>
    <td>Implementar Sección de regístrate.</td>
    <td>COMO usuario QUIERO visualizar una opcion que me permita registrarme con un plan para mi negocio PARA poder tener acceso a las funcionalidades de la aplicacion.</td>
    <td><strong>Escenario 1:</strong>  El usuario crea correctamente su usuario. <br>Dado que el usuario intenta crear un usuario. Cuando realice todos los pasos y seleccione un plan. Entonces su usuario sera creado y sera redireccionado a la pestaña de Login.<br><br> <strong>Escenario 2:</strong>El usuario no puede crear su usuario <br>Dado que el usuario intenta crear un usuario. Cuando realice todos los pasos y seleccione un plan pero exista una falla en el sistema. Entonces se desplegara una alerta informando que se intente nuevamente mas tarde.<br><br><strong>Escenario 3:</strong> El usuario no puede crear su usuario por no seleccionar un plan.<br>Dado que el usuario intenta crear un usuario. Cuando realice todos los pasos y seleccione un plan pero no seleccione un plan de pago. Entonces se desplegara una alerta informando que debe seleccionar un plan y configurar un metodo de pago.</td>
  </tr>
  <tr>
    <td>E02_TS002</td>
    <td>Implementar bloqueo de cuenta después de 5 de intentos fallidos de inicio de sesión.</td>
    <td>COMO desarrollador QUIERO implementar un bloqueo de cuenta al fallar reiteradas veces en iniciar sesion PARA brindar seguridad al usuario</td>
    <td><strong>Escenario 1:</strong>La cuenta se bloquea tras 5 intentos fallidos de iniciar sesion.<br>Dado que la cuenta se bloquea. Cuando un usuario falla en ingresar 5 veces. Entonces se le ha brindado seguridad al usuario<br><br> <strong>Escenario 2:</strong> La cuenta no se bloquea tras fallar en iniciar sesion multiples vecec.<br> Dado que la cuenta no se bloquea nunca. Cuando un usuario falla en ingresar multiples veces. Entonces su informacion esta desprotegida y es propenso a un ataque de fuerza bruta</td>
  </tr>
  <tr>
    <td colspan="4"><strong>Épica 3: Gestión de perfil y preferencias de usuario  </strong><br>Como usuario<br>Quiero visualizar un seccion para mi perfil<br>Para saber los datos que tengo y poder modificarlos cuando quiera</td>
  </tr>
  <tr>
    <td>E03_US014</td>
    <td>Dirigir a perfil de usuario.</td>
    <td>COMO usuario QUIERO ir a mi perfil PARA cambiar cualquier dato que necesite actualización.</td>
    <td><strong>Escenario 1:</strong> El usuario es redireccionado a su perfil. <br>Dado que el perfil de usuario funciona. Cuando el usuario de click en el boton de perfil. Entonces sera redirigido a su perfil. <br><br> <strong>Escenario 2:</strong> El usuario no es redireccionado a su perfil. <br>Dado que el perfil de usuario no se encuentra en funcionamiento. Cuando el usuario de click en el boton de perfil. Entonces no sera redirigido a su perfil, en cambio se mantendra en la vista actual.</td>
  </tr>
  <tr>
    <td>E03_US015</td>
    <td>Ver y editar datos de usuario.</td>
    <td>COMO usuario QUIERO ver y editar mi información PARA mantenerla actualizada.</td>
    <td><strong>Escenario 1:</strong>  El usuario visualiza su información <br>Dado que el usuario desea ver su informacion. Cuando da click en el boton perfil. Entonces visualiza su informacion <br><br> <strong>Escenario 2:</strong> El usuario modifica su informacion.<br>Dado que el usuario quiere modificar su informacion y el sistema funciona correctamente. Cuando da click en el boton de moficar perfil dentro del perfil, cambia su informacion y da click en el boton guardar. Entonces actualiza su informacion correctamente.<br><br><strong>Escenario 3:</strong> El usuario no es capaz de modificar su informacion. <br>Dado que el usuario quiere modificar su informacion y el sistema no funciona segun lo esperado. Cuando da click en el boton de moficar perfil dentro del perfil, cambia su informacion y da click en el boton guardar. Entonces se mostrará una alerta indicando que hubo un error en el sistema.</td>
  </tr>
  <tr>
    <td colspan="4"><strong>Épica 4: Notificacion de servicio.</strong><br>Como usuario mesero<br>Quiero poder recibir notificaciones sobre el estado de un cliente y su orden.<br>Para poder tener mayor eficiencia al atender.</td>
  </tr>
  <tr>
    <td>E04_US016</td>
    <td>Recibir alerta cuando un cliente cruza la puerta del local.</td>
    <td>COMO mesero QUIERO recibir una alerta cuando un cliente cruza la puerta del local PARA poder atenderlo a la brevedad.</td>
    <td><strong>Escenario 1:</strong> Una notificacion es mandada al sistema. <br>Dado que soy un mesero y el sistema funciona correctamente. Cuando un cliente cruza la puerta del local. Entonces visualizo en el sistema una alerta de ello. <br><br> <strong>Escenario 2:</strong> No se envia correctmante la notificacion. <br>Dado que soy un mesero pero el sistema no funciona segun lo esperado. Cuando un cliente cruza la puerta del local Entonces no se visualiza ninguna alerta en el sistema.</td>
  </tr>
  <tr>
    <td>E04_US017</td>
    <td>Recibir alerta cuando un cliente se sienta en alguna mesa.</td>
    <td>COMO mesero QUIERO recibir una alerta cuando un cliente se sienta en alguna mesa PARA poder generar el pedido en dicha mesa.</td>
    <td><strong>Escenario 1:</strong> Se recibe una alerta cuando un cliente se sienta.<br>Dado que un cliente ingresa al local. Cuando se sienta en alguna mesa. Entonces se muestra una alerta en el sistema indicando el hecho. <br><br> <strong>Escenario 2:</strong> No se recibe la alerta cuando un cliente se sienta. <br>Dado que un cliente ingresa al local. Cuando se sienta en alguna silla. Entonces no se muestra ninguna alerta, dificultando su atención.</td>
  </tr>
  <td>E04_US018</td>
    <td>Dirigir a perfil de usuario.</td>
    <td>COMO usuario QUIERO ir a mi perfil PARA cambiar cualquier dato que necesite actualización.</td>
    <td><strong>Escenario 1:</strong> Se muestra una alerta cuando un cliente deja la mesa. <br>Dado que un cliente ha consumido en el local. Cuando deja su mesa. 
y se muestra una alerta en el sistema indicando esto asi como un link a su cuenta. Entonces puedo verificar si su cuenta fue cancelada.<br><br> <strong>Escenario 2:</strong> No se muestra una alerta cuando un cliente deja la mesa. <br>Dado que un cliente ha consumido en el local. Cuando deja su mesa y no se muestra una alerta en el sistema. Entonces no puedo estar atento de verificar si su cuenta fue cancelada.</td>
  </tr>
  <tr>
    <td>E04_US019</td>
    <td>Recibir alerta cuando hay platos en la mesa y no hay cliente sentado.</td>
    <td>COMO mesero QUIERO recibir una alerta cuando hay platos en la mesa y no hay cliente en ella PARA darme cuenta y recoger los platos sucios.</td>
    <td><strong>Escenario 1:</strong> Se envia una alerta de platos en mesa. <br>Dado que un cliente consumio y dejo su mesa. Cuando hayan platos en la mesa y no un cliente sentado. Entonces se enviara una alerta para recoger los platos. <br><br> <strong>Escenario 2:</strong> No se envia ninguna alerta de platos en mesa. <br>Dado que un cliente consumio y dejo su mesa pero el sistema no funcione. Cuando hayan platos en la mesa y no un cliente sentado. Entonces no se enviara una alerta evitando que el mesero se percate de ello dejando el local sucio.</td>
  </tr>
  <tr>
    <td>E04_TS004</td>
    <td>Mostrar información detallada del cliente en la notificación</td>
    <td>COMO desarrollador QUIERO brindar informacion detallada de la mesa en la notificacion PARA brindar comodidad y eficiencia al mesero</td>
    <td><strong>Escenario 1:</strong>La notificación muestra información relevante sobre el pedido.<br>Dado que la notificacion muestra informacion relevante. Cuando un mesero la lee. Entonces es capaz de reaccionar a la brevedad<br><br> <strong>Escenario 2:</strong> La notificación no muestrs información relevante sobre el pedido.<br>Dado que la notificacion no muestra informacion relevante. Cuando un mesero la lee. Entonces no sera capaz de reaccionar a la brevedad, teniendo que ampliarla o ingresar a la aplicacion</td>
  </tr>
  <td colspan="4"><strong>Épica 5: Toma de pedidos.</strong><br>Como usuario mesero<br>Quiero poder tomar pedidos y enviarlos a otras áreas.<br>Para poder agilizar el flujo de trabajo.</td>
  <tr>
    <td>E05_US020</td>
    <td>Tomar pedidos de la mesa.</td>
    <td>COMO mesero QUIERO poder tomar pedidos desde una aplicación PARA poder agilizar la toma de ordenes.</td>
    <td><strong>Escenario 1:</strong> La funcion de agregar pedidos a la orden funciona correctamente.<br>Dado que soy un mesero. Cuando quiero agregar un producto al pedido. Entonces se agrega correctamente a la orden.<br><br> <strong>Escenario 2:</strong> La funcion de agregar pedidos a la orden no funciona.<br>Dado que soy un mesero. Cuando quiero agregar un producto al pedido y no funciona el sistema. Entonces no se agrega el producto y debo tomarlo manualmente perdiendo tiempo.</td>
  </tr>
  <tr>
    <td>E05_US021</td>
    <td>Guardar orden.</td>
    <td>COMO mesero QUIERO poder guardar las ordenes de una mesa PARA enviarlos a caja o cocina.</td>
    <td><strong>Escenario 1:</strong> La funcion de guardar ordenes funciona correctamente.<br>Dado que soy un mesero. Cuando quiero guardar un pedido. Entonces se guarda correctamente. <br><br> <strong>Escenario 2:</strong> La funcion de guardar ordenes no funciona.<br>Dado que soy un mesero. Cuando quiero guardar la orden y no funciona el sistema. Entonces no se guarda y debo tomarlo manualmente perdiendo tiempo.</td>
  </tr>
  <tr>
    <td>E05_US022</td>
    <td>Enviar pedido guardado a cocina y caja.</td>
    <td>COMO mesero QUIERO poder enviar pedidos a cocina o caja PARA poder continuar con el flujo de trabajo sin necesidad de dictar la orden personalmente demorando la atencion de otros pedidos.</td>
    <td><strong>Escenario 1:</strong> La funcion de enviar ordenes funciona correctamente. <br>Dado que soy un mesero. Cuando quiero enviar una orden a cocina o caja y el sistema funciona. Entonces se envia correctamente. <br><br> <strong>Escenario 2:</strong> La funcion de enviar ordenes no funciona. <br>Dado que soy un mesero. Cuando quiero enviar una orden a cocina o caja y el sistema no funciona. Entonces se no se envia la orden provocando que lo tenga que llevar manualmente.</td>
  </tr>
  <tr>
    <td>E05_TS005</td>
    <td>Mantener las cuentas y mesas guardadas actualizadas en tiempo real para todos los usuarios del negocio</td>
    <td>COMO Desarrollador QUIERO implementar un sistema que sincronice en tiempo real las cuentas y estados de las mesas PARA garantizar que toda la información esté actualizada y sea accesible para los usuarios del negocio.</td>
    <td>
        <strong>Escenario 1:</strong> Sincronización en tiempo real de cuentas y mesas<br>
        Dado que el sistema está configurado para sincronización en tiempo real.<br>
        Cuando un usuario realiza un cambio en las cuentas o mesas (como añadir un pedido o marcar una mesa como ocupada).<br>
        Entonces estos cambios se reflejan inmediatamente en todas las interfaces conectadas.<br><br>
        <strong>Escenario 2:</strong> Fallo en la sincronización en tiempo real<br>
        Dado que el sistema experimenta un problema de sincronización.<br>
        Cuando un usuario realiza un cambio en las cuentas o mesas.<br>
        Entonces los cambios no se reflejan en las interfaces de otros usuarios, y se muestra un mensaje de error indicando el problema.
    </td>
  </tr>

  <td colspan="4"><strong>Épica 6: Facturación del negocio.</strong><br>Como usuario administrador<br>Quiero realizar facturaciones.<br>Para brindarle al cliente su comprobante de pago.</td>
  <tr>
    <td>E06_US023</td>
    <td>Crear un cliente con DNI o RUC.</td>
    <td>COMO administrador QUIERO crear nuevos clientes con DNI o RUC PARA poder crear documentos de venta personalizados.</td>
    <td><strong>Escenario 1:</strong> El sistema se vincula con SUNAT.<br>Dado que soy un administrador. Cuando intento agregar un clinete y el sistema con SUNAT funciona. Entonces se encuentra al cliente rapidamente.<br><br> <strong>Escenario 2:</strong> El vinculo con SUNAT no funciona.<br>Dado que soy un administrador. Cuando intento agregar un clinete y el sistema con SUNAT no funciona. Entonces debo llenar los campos de RUC/DNI, nombre del cliente/empresa y direccion de facturacion.</td>
  </tr>
  <tr>
    <td>E06_US024</td>
    <td>Imprimir Pre-cuenta.</td>
    <td>COMO administrador QUIERO poder imprimir el resumen de una orden PARA poder brindarle al cliente previo al pago.</td>
    <td><strong>Escenario 1:</strong> Se imprimer la pre-cuenta correctamente. <br>Dado que soy un administrador. Cuando me solicitan imprimir la precuenta y le doy click al boton correspondiente. Entonces se imprime y se la entrego al cliente o mesero. <br><br> <strong>Escenario 2:</strong> No se imprime la pre-cuenta. <br>Dado que soy un administrador. Cuando me solicitan imprimir la precuenta y le doy click al boton correspondiente pero no funciona. Entonces no se imprime y el cliente o mesero queda inconforme.</td>
  </tr>
  <tr>
    <td>E06_US025</td>
    <td>Cobrar orden.</td>
    <td>COMO administrador QUIERO poder cobrar la orden de un cliente con diversos metodos de pago PARA brindar comodidad al cliente.</td>
    <td><strong>Escenario 1:</strong> Se cobra la orden. <br>Dado que soy un administrador. Cuando quiero cobrar la orden con diversos metodos de pago. Entonces los metodos de pago son añadidos y se cobra la orden. <br><br> <strong>Escenario 2:</strong> No se cobra la orden. <br>Dado que soy un administrador. Cuando quiero cobrar la orden con diversos metodos de pago y el sistema no funciona. Entonces no se añaden los metodos de pago y no puedo cobrar la orden.</td>
  </tr>
  <tr>
    <td>E06_US026</td>
    <td>Boletear o facturar la orden.</td>
    <td>COMO administrador QUIERO poder boletear o facturar la orden del cliente cerrando la orden PARA poder emitir los documentos a la SUNAT.</td>
    <td><strong>Escenario 1:</strong> Se emite documento de venta. <br>Dado que soy un administrador. Cuando quiero emitir un documento de venta y el sistema funciona. Entonces se imprime el documento. <br><br> <strong>Escenario 2:</strong> No se emite documento de venta. <br>Dado que soy un administrador. Cuando quiero emitir un documento de venta y el sistema no funciona. Entonces no se imprime el documento y se muestra un error en pantalla.</td>
  </tr>
  <tr>
    <td>E06_TS006</td>
    <td>Asociar productos y servicios a categorias</td>
    <td>COMO desarrollador QUIERO implementar categorias a los productos PARA que el administrador pueda filtrarlos de mejor manera</td>
    <td><strong>Escenario 1:</strong>Los productos pueden tener una categoria<br>Dado que un producto tiene una categoria. Cuando un administrador filtra los productos. Entonces es capaz de ver con mayor detalle los consumos realizados<br><br> ><strong>Escenario 2:</strong>Los productos no pueden tener una categoria<br>Dado que un producto no puede tener una categoria. Cuando un administrador filtra los productos. Entonces sera mas dificil para el visualizar donde esta su mayor cantidad de ventas<br><br> 
  </tr>
  <tr>
    <td>E06_TS009</td>
    <td>El cliente creado debe guardarse en la base de datos para poder acceder a él en caso se solicite nuevamente</td>
    <td>COMO Desarrollador QUIERO implementar una funcionalidad que registre los datos de los clientes en la base de datos PARA asegurar que estén disponibles para futuras consultas y operaciones.</td>
    <td>
        <strong>Escenario 1:</strong> Registro exitoso del cliente<br>
        Dado que el sistema recibe datos válidos de un cliente.<br>
        Cuando el cliente es creado en el sistema.<br>
        Entonces los datos se guardan correctamente en la base de datos y se genera un identificador único para el cliente.<br><br>
        <strong>Escenario 2:</strong> Fallo en el registro del cliente<br>
        Dado que el sistema recibe datos incompletos o inválidos para el cliente.<br>
        Cuando se intenta crear el cliente en el sistema.<br>
        Entonces el sistema responde con un mensaje de error indicando el problema y no guarda los datos en la base de datos.
    </td>
  </tr>
  <td colspan="4"><strong>Épica 7: Control de inventarios.</strong><br>Como usuario administrador<br>Quiero poder ver un resumen de los platos vendidos y cuanto se consumió en cada uno. <br>Para poder llevar un control de mis inventarios como negocio.</td>
  <tr>
    <td>E07_TS008</td>
    <td>Los insumos deben relacionarse con los productos. Al guardar uno en una cuenta, los productos o insumos deben restarse del stock</td>
    <td>COMO desarrollador QUIERO quiero que los insumos tengan opción de anidarse a productos mediante SQL PARA poder añadir y quitar insumos durante la inserción de un producto</td>
    <td><strong>Escenario 1:</strong> Los insumos se relacionan correctamente con los productos. <br>Dado que soy desarrollador Cuando asocio un insumo a un producto y realizo una venta. Entonces los insumos y productos relacionados se descuentan correctamente del stock, y se muestra un mensaje de confirmación indicando la operación exitosa. <br><br> <strong>Escenario 2:</strong> Error al relacionar insumos con productos. <br>Dado que soy desarrollador Cuando intento asociar un insumo a un producto y se produce un error en la base de datos, 
Entonces se muestra un mensaje de error indicando que la operación no pudo completarse, y el stock permanece sin cambios.</td>
  </tr>
  <tr>
    <td>E07_US027</td>
    <td>Ver resumen de ventas.</td>
    <td>COMO administrador QUIERO poder ver el resumen de ventas por dias PARA poder saber cuanto se vendio.</td>
    <td><strong>Escenario 1:</strong> Se puede ver el resumen de ventas. <br>Dado que soy administrador. Cuando ingreso a la seccion de reportes de ventas. Entonces puedo ver un grafico con el resumen de ventas y diversos filtros. <br><br> <strong>Escenario 2:</strong> El resumen de ventas no carga correctamente. <br>Dado que soy administrador. Cuando ingreso a la seccion de reportes de ventas y no funciona. 
Entonces no se generan los graficos y se muestra un error indicando que no se pudo cargar el reporte.</td>
  </tr>
  <tr>
    <td>E07_US028</td>
    <td>Filtrar ventas por platos.</td>
    <td>COMO administrador QUIERO poder filtrar las ventas por platos PARA saber que platos se vendieron mas que otros.</td>
    <td><strong>Escenario 1:</strong> La funcion de filtrar ventas por platos funciona. <br>Dado que soy un administrador. Cuando selecciono la opcion de filtrar por plato en el reporte. Entonces puedo ver la lista de ventas segun cada plato. <br><br> <strong>Escenario 2:</strong> Dado que soy un administrador. Cuando selecciono la opcion de filtrar por plato en el reporte y este no funciona. Entonces se muestra un error indicando que no se pudo seleccionar el filtro.</td>
  </tr>
  <tr>
    <td>E07_US029</td>
    <td>Ver resumen de productos restantes.</td>
    <td>COMO administrador QUIERO saber cuantos insumos me quedan en stock despues de haber vendido los platos PARA poder llevar un buen inventario.</td>
    <td><strong>Escenario 1:</strong> La seccion de ver resumen de productos restantes funciona. <br>Dado que soy administrador. Cuando accedo a la sección de inventario. Entonces puedo ver una lista detallada de todos los insumos en stock, incluyendo su cantidad. <br><br> <strong>Escenario 2:</strong> No se actualiza el reporte en tiempo real<br>Dado que soy administrador. Cuando accedo a la seccion de inventario y no se actualiza con las ventas de platos. Entonces se muestra un mensaje indicando que los datos podrian estar desactualizados.</td>
  </tr>
  <tr>
    <td>E07_US030</td>
    <td>Ingresar nuevos productos al inventario.</td>
    <td>COMO administrador QUIERO anadir insumos a mi stock al momento de realizar una compra PARA poder mantener mi inventario actualizado.</td>
    <td><strong>Escenario 1:</strong>  Se agrega insumo nuevo correctamente. <br>Dado que soy administrador. Cuando quiero agregar un insumo nuevo, lleno los campos y doy click al boton crear. Entonces el producto se añade correctamente.<br><br> <strong>Escenario 2:</strong> El insumo ingresado ya existe.<br>Dado que soy administrador. Cuando quiero agregar un producto nuevo y este ya existe. Entonces muestra una alerta indicando que se modifique el nombre del producto.<br><br><strong>Escenario 3:</strong> No se puede agregar el nuevo insumo. <br>Dado que soy administrador. Cuando quiero agregar un producto nuevo, lleno los campos y doy click al boton crear pero el sistema no funciona. Entonces el insumo no se añade y muestra una alerta indicando el erro.</td>
  </tr>
  <tr>
    <td>E07_US031</td>
    <td>Crear platos nuevos.</td>
    <td>COMO administrador QUIERO poder crear nuevos platos con sus precios, insumos necesarios, etc. PARA que los meseros puedan seleccionarlos al momento de tomar una orden.</td>
    <td><strong>Escenario 1:</strong>  Se agrega plato nueva correctamente. <br>Dado que soy administrador. Cuando quiero agregar un plato nuevo, lleno los campos y doy click al boton crear. Entonces el plato se añade correctamente. <br><br> <strong>Escenario 2:</strong> El plato ingresado ya existe. <br>Dado que soy administrador. Cuando quiero agregar un plato nuevo y este ya existe. Entonces muestra una alerta indicando que se modifique el nombre del plato.<br><br><strong>Escenario 3:</strong> No se puede agregar el nuevo plato. <br>Dado que soy administrador. Cuando quiero agregar un plato nuevo, lleno los campos y doy click al boton crear pero el sistema no funciona. Entonces el plato no se añade y muestra una alerta indicando el error.</td>
  </tr>
  </tr>
  <tr>
    <td>E07_US032</td>
    <td>Editar insumos existentes.</td>
    <td>COMO administrador QUIERO poder editar los datos de los insumos que ya tengo creados PARA poder actualizarlos en caso sea necesario.</td>
    <td><strong>Escenario 1:</strong> Se modifica el insumo correctemante. <br>Dado que soy administrador. Cuando quiero modificar un insumo y le doy click al boton guardar. Entonces el insumo se modifica correctamente. <br><br> <strong>Escenario 2:</strong> No es posible modificar el insumo <br> Dado que soy administrador. Cuando quiero modificar un insumo y le doy click al boton guardar pero el sistema no funciona. Entonces el insumo no se modifica y se muestra una alerta indicando el error.</td>
  </tr>
  </tr>
  <tr>
    <td>E07_US033</td>
    <td>Eliminar insumos existentes.</td>
    <td>COMO administrador QUIERO Poder eliminar los insumos existentes PARA mantener mis platos actualizados.</td>
    <td><strong>Escenario 1:</strong>  El producto se elimina correctamente.<br>Dado que soy administrador. Cuando doy click al boton de eliminar producto. Entonces el producto se elimina correctamente. <br><br> <strong>Escenario 2:</strong> El producto no ha sido eliminado<br>Dado que soy administrador. Cuando doy click al boton de eliminar insumo pero el sistema no funciona. Entonces el producto no se elimina y muestra un mensaje de error</td>
  </tr>
  <tr>
    <td colspan="4"><strong>Épica 8: Estadísticas de negocio</strong><br>Como Administrador del Restaurante<br>Quiero visualizar y gráficos de las cuentas creadas mensualmente y del desempeño del personal en la atención que brinda<br>Para monitorear la eficiencia de la aplicación en la empresa</td>
  </tr>
  <tr>
    <td>E08_US034</td>
    <td>Ver resumen de ventas.</td>
    <td>COMO administrador QUIERO visualizar un resumen de las ventas realizadas POR cada período de tiempo PARA analizar el rendimiento de los platos y tomar decisiones informadas.</td>
    <td><strong>Escenario 1:</strong> El resumen de ventas se muestra correctamente.<br>Dado que soy administrador. Cuando selecciono un período de tiempo en el filtro y solicito el resumen de ventas. Entonces el sistema genera y muestra un informe con los datos de ventas detallados y organizados por plato, fecha y cantidad.  
    <br> <strong>Escenario 2:</strong> El resumen de ventas no se muestra.<br>Dado que soy administrador. Cuando selecciono un período de tiempo y solicito el resumen, pero ocurre un error en el sistema. Entonces se muestra un mensaje indicando que el resumen de ventas no está disponible en ese momento y recomendando reintentar más tarde.</td>
  </tr>
  <tr>
    <td>E08_US035</td>
    <td>Filtrar ventas por productos</td>
    <td>COMO administrador QUIERO filtrar las ventas por productos específicos PARA identificar los más vendidos y optimizar la oferta del menú.</td>
    <td><strong>Escenario 1:</strong> Las ventas filtradas por producto se muestran correctamente.<br>Dado que soy administrador. Cuando selecciono un producto específico en el filtro y solicito ver las ventas. Entonces el sistema muestra un resumen detallado de las ventas relacionadas con ese producto, incluyendo fecha, cantidad vendida y total generado.  
    <br> <strong>Escenario 2:</strong> Las ventas filtradas por producto no se muestran.<br>Dado que soy administrador. Cuando selecciono un producto específico en el filtro y solicito las ventas, pero ocurre un error en el sistema. Entonces se muestra un mensaje indicando que las ventas no están disponibles en ese momento y recomendando reintentar más tarde.</td>
</tr>
<tr>
    <td>E08_US036</td>
    <td>Filtrar ventas por productos</td>
    <td>COMO administrador QUIERO filtrar las ventas por productos específicos PARA evaluar el desempeño individual de cada producto y tomar decisiones basadas en datos.</td>
    <td><strong>Escenario 1:</strong> Las ventas filtradas por producto se muestran correctamente.<br>
    Dado que soy administrador. Cuando selecciono un producto específico desde el filtro y hago clic en "Ver resumen". Entonces el sistema genera y muestra un informe detallado de las ventas del producto, que incluye fecha, unidades vendidas, ingresos totales y comparación con otros períodos.  
    <br><br> <strong>Escenario 2:</strong> El sistema muestra un error al filtrar ventas.<br>
    Dado que soy administrador. Cuando selecciono un producto específico y solicito ver el resumen de ventas, pero el sistema falla. Entonces se muestra un mensaje de error indicando que los datos no están disponibles y sugiriendo intentar nuevamente o contactar al soporte técnico.</td>
</tr>
  <tr>
    <td>E08_US037</td>
    <td>Generar salida de dinero en caja</td>
    <td>COMO administrador QUIERO registrar las salidas de dinero de la caja PARA llevar un control preciso de los movimientos financieros y justificar los gastos realizados.</td>
    <td><strong>Escenario 1:</strong> La salida de dinero se registra correctamente.<br>
    Dado que soy administrador. Cuando ingreso los detalles de una salida de dinero, como el monto, la fecha, y el motivo, y hago clic en "Registrar salida". Entonces el sistema guarda la información correctamente y la muestra en el historial de movimientos financieros.  
    <br><br> <strong>Escenario 2:</strong> El sistema muestra un error al registrar la salida.<br>
    Dado que soy administrador. Cuando ingreso los detalles de una salida de dinero y hago clic en "Registrar salida", pero ocurre un error en el sistema. Entonces se muestra un mensaje de error indicando que no se pudo completar el registro y sugiriendo reintentar o contactar al soporte técnico.</td>
</tr>
  
<tr>
    <td>E08_US038</td>
    <td>Generar ingreso de dinero en caja</td>
    <td>COMO administrador QUIERO registrar los ingresos de dinero en la caja PARA llevar un control financiero y justificar los depósitos realizados.</td>
    <td><strong>Escenario 1:</strong> El ingreso de dinero se registra correctamente.<br>
    Dado que soy administrador. Cuando ingreso los detalles de un ingreso de dinero, como el monto, la fecha, y el motivo, y hago clic en "Registrar ingreso". Entonces el sistema guarda la información correctamente y la muestra en el historial de movimientos financieros.  
    <br><br> <strong>Escenario 2:</strong> El sistema muestra un error al registrar el ingreso.<br>
    Dado que soy administrador. Cuando ingreso los detalles de un ingreso de dinero y hago clic en "Registrar ingreso", pero ocurre un error en el sistema. Entonces se muestra un mensaje de error indicando que no se pudo completar el registro y sugiriendo reintentar o contactar al soporte técnico.</td>
</tr>
<tr>
    <td>E08_US039</td>
    <td>Ver historial de ventas</td>
    <td>COMO administrador QUIERO visualizar el historial de ventas realizadas PARA analizar el rendimiento general de la caja y realizar auditorías.</td>
    <td><strong>Escenario 1:</strong> El historial de ventas se muestra correctamente.<br>
    Dado que soy administrador. Cuando accedo a la sección de historial de ventas y selecciono un rango de fechas. Entonces el sistema muestra un listado detallado con las transacciones realizadas, incluyendo fecha, productos vendidos y montos.  
    <br><br> <strong>Escenario 2:</strong> El historial de ventas no se muestra.<br>
    Dado que soy administrador. Cuando accedo a la sección de historial de ventas y selecciono un rango de fechas, pero ocurre un error en el sistema. Entonces se muestra un mensaje indicando que los datos no están disponibles y sugiriendo reintentar más tarde o contactar al soporte técnico.</td>
</tr>
<tr>
    <td>E08_US040</td>
    <td>Ver resumen de productos restantes</td>
    <td>COMO administrador QUIERO visualizar un resumen de los productos restantes en inventario PARA gestionar las existencias y planificar compras de manera eficiente.</td>
    <td><strong>Escenario 1:</strong> El resumen de productos restantes se muestra correctamente.<br>
    Dado que soy administrador. Cuando accedo a la sección de inventario y solicito el resumen de productos. Entonces el sistema genera un informe con las cantidades disponibles de cada producto, organizadas por categoría y prioridad.  
    <br><br> <strong>Escenario 2:</strong> El resumen de productos restantes no se muestra.<br>
    Dado que soy administrador. Cuando accedo a la sección de inventario y solicito el resumen de productos, pero ocurre un error en el sistema. Entonces se muestra un mensaje indicando que el resumen no está disponible y sugiriendo reintentar más tarde o contactar al soporte técnico.</td>
</tr>

  
  <tr>
    <td colspan="4">
        <strong>Épica 9: Despliegue de aplicación</strong><br>
       COMO Administrador del Restaurante<br>
        QUIERO automatizar algunas funciones actualmente cubiertas por mi planilla<br>
        PARA optimizar los tiempos de ejecución de tareas, mejorar la productividad y definir con mayor claridad los roles y responsabilidades de mis empleados.
    </td>
</tr>
<tr>
    <td>E09_TS041</td>
    <td>Despliegue del Backend</td>
    <td>COMO Desarrollador DESEO contar con un sistema de despliegue automatizado y confiable para la aplicación backend, PARA que podamos implementar nuevas versiones sin interrupciones en el servicio y con un proceso que minimice los errores y reduzca los tiempos de inactividad.</td>
    <td>
        <strong>Escenario 1:</strong> Creación de recurso exitosa<br>
        Dado que el backend recibe una solicitud de creación de recurso con datos válidos.<br>
        Cuando el recurso se crea exitosamente<br>
        Entonces responde con un código de estado 201 Created y la respuesta incluye el identificador único del nuevo recurso<br><br>
        <strong>Escenario 2:</strong> Solicitud inválida debido a datos mal formateados<br>
        Dado el backend recibe una solicitud con datos mal formateados o incompletos.<br>
        Cuando el backend valida los datos de la solicitud .<br>
        Entonces sponde con un código de estado 400 Bad Request y la respuesta contiene un mensaje de error que describe el problema específico de la solicitud
    </td>
</tr>
<tr>
    <td>E09_TS042</td>
    <td>Despliegue del App Web</td>
    <td>COMO Desarrollador DESEO implementar una interfaz web que muestre en tiempo real la ocupación de las mesas y el número de clientes PARA facilitar la toma de decisiones rápidas y mejorar la experiencia de los administradores del restaurante.</td>
    <td>
        <strong>Escenario 1:</strong> Actualización en tiempo real<br>
        Dado que la App Web está conectada al Backend y sincronizada correctamente.<br>
        Cuando el estado de una mesa cambie a "Disponible" o "Ocupada".<br>
        Entonces la App Web reflejará automáticamente el nuevo estado en la interfaz del administrador.<br><br>
        <strong>Escenario 2:</strong> Error en la sincronización de datos<br>
        Dado que la App Web intenta sincronizarse con el Backend.<br>
        Cuando se produzca un fallo en la conexión o en el procesamiento de datos.<br>
        Entonces la App Web mostrará un mensaje de error indicando que los datos no están actualizados y sugerirá intentar nuevamente.
    </td>
</tr>
  
   <tr>
    <td colspan="4"><strong>Épica 10: Dispositivo IoT</strong><br>Como Administrador del Restaurante<br>Quiero automatizar algunas funciones cubiertas por mi planilla<br>Para mejorar los tiempos y definir mejor los roles de mis empleados</td>
  </tr>
  <tr>
    <td>E010_TS043</td>
    <td>Inventariado de Insumos mediante IoT</td>
    <td>COMO Desarrollador DESEO implementar un sistema que actualice automáticamente el inventario mediante dispositivos IoT PARA garantizar información precisa y alertar cuando los insumos críticos estén bajos,   evitando interrupciones en el servicio.</td>
    <td>
        <strong>Escenario 1:</strong> Registro automático del inventario<br>
        Dado que el dispositivo IoT está conectado correctamente.<br>
        Cuando se detecte una entrada o salida de insumos.<br>
        Entonces el sistema actualizará automáticamente el inventario en tiempo real.<br><br>
        <strong>Escenario 2:</strong> Alerta de nivel crítico de inventario<br>
        Dado que el nivel de un insumo está por debajo del umbral crítico definido.<br>
        Cuando el sistema reciba la lectura del dispositivo IoT.<br>
        Entonces se emitirá una alerta al administrador para reabastecer.
    </td>
  </tr>
  <tr>
    <td>E010_TS044</td>
    <td>Detectar Mesas y Clientes mediante IoT</td>
    <td>COMO Desarrollador DESEO integrar dispositivos IoT para detectar en tiempo real la ocupación de mesas y el número de clientes PARA optimizar la asignación de recursos y reducir los tiempos de espera en el restaurante.</td>
    <td>
        <strong>Escenario 1:</strong> Detección de ocupación de mesas<br>
        Dado que el dispositivo IoT está en funcionamiento.<br>
        Cuando una mesa sea ocupada.<br>
        Entonces el sistema actualizará el estado de la mesa a "Ocupada" en la interfaz del administrador.<br><br>
        <strong>Escenario 2:</strong> Estimación del número de clientes por mesa<br>
        Dado que el dispositivo IoT detecta clientes en una mesa.<br>
        Cuando los sensores identifiquen el número de personas.<br>
        Entonces el sistema reflejará esta información en la interfaz con un margen de error no mayor al 5%.
    </td>
  </tr>

</table>

## 3.3. Product Backlog

| #  | User Story ID | Título                                                           | Descripción                                                                                                                                                                                               | Story Points |
|----|---------------|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| 1  | E02_US_009    | Logout                                                           | COMO cliente QUIERO salir de la aplicación PARA evitar el uso de mi cuenta por otras personas.                                                                                                            | 1            |
| 2  | E01_US_001    | seccion de Header                                                | COMO usuario QUIERO visualizar un encabezado de página que contenga opciones PARA una mejor navegación por la página.                                                                                     | 2            |
| 3  | E01_US_002    | seccion de Footer                                                | COMO usuario QUIERO visualizar pie de página que contenga información PARA un mejor entendimiento de la página.                                                                                           | 2            |
| 4  | E01_US_004    | Botón para ver más información                                   | COMO usuario QUIERO ver más información sobre la página PARA comprender más sobre la start-up.                                                                                                            | 2            |
| 5  | E01_US_005    | Sección de Contacto                                              | COMO usuario QUIERO observar un seccion “Contacto” PARA comunicarme con el equipo de desarrollo.                                                                                                          | 2            |
| 6  | E01_US_011    | Validación de clave                                              | COMO cliente QUIERO validar mi clave PARA mantener mi cuenta segura.                                                                                                                                      | 1            |
| 7  | E01_US_012    | Despliegue de Menú                                               | COMO usuario QUIERO visualizar un menú PARA acceder a las funciones de la aplicación rápidamente.                                                                                                         | 2            |
| 8  | E02_US_013    | Salir de la sesión                                               | COMO usuario QUIERO cerrar sesión en mi cuenta PARA iniciar o crear otra cuenta.                                                                                                                          | 2            |
| 9  | E02_US_014    | Sección de inicio de sesión                                      | COMO usuario QUIERO iniciar sesión en mi cuenta PARA acceder a la información de la plataforma.                                                                                                           | 2            |
| 10 | E02_US_015    | Sección de registro                                              | COMO usuario QUIERO observar un seccion de “Regístrate” PARA crear una cuenta nueva.                                                                                                                      | 2            |
| 11 | E03_US_017    | Dirigir a ajustes de la aplicación                               | COMO usuario QUIERO ir a los ajustes de la aplicación PARA realizar cambios en la configuración.                                                                                                          | 2            |
| 12 | E07_US_037    | Eliminar platos existentes                                       | COMO administrador QUIERO eliminar platos del menú PARA mantener la oferta actualizada.                                                                                                                   | 3            |
| 13 | E01_US_003    | Barra de Navegación                                              | COMO usuario QUIERO presionar botones en el encabezado del landing page para desplazarme por la página.                                                                                                   | 2            |
| 14 | E01_US_004    | Descripción de la Start-Up                                       | COMO usuario QUIERO observar un seccion con información de la página PARA conocer sobre la start-up.                                                                                                      | 3            |
| 15 | E01_US_007    | Sección del equipo                                               | COMO usuario QUIERO observar un seccion sobre el equipo PARA conocer más sobre los desarrolladores.                                                                                                       | 3            |
| 16 | E02_US_008    | Login con PIN/clave                                              | COMO cliente QUIERO ingresar con PIN PARA acceder a la página principal.                                                                                                                                  | 3            |
| 17 | E02_US_010    | Recuperar contraseña                                             | COMO cliente QUIERO recuperar mi contraseña PARA ingresar a la aplicación.                                                                                                                                | 3            |
| 18 | E03_US_016    | Dirigir a perfil de usuario                                      | COMO cliente QUIERO acceder a mi perfil PARA cambiar cualquier dato que necesite actualización.                                                                                                           | 3            |
| 19 | E03_US_018    | Ver y editar datos de usuario                                    | COMO usuario QUIERO ver y editar mi información PARA mantenerla actualizada.                                                                                                                              | 3            |
| 20 | E04_US_022    | Recibir alerta cuando hay platos y no hay cliente en mesa        | COMO mesero QUIERO recibir una alerta cuando hay platos sucios en una mesa sin clientes PARA poder recogerlos.                                                                                            | 3            |
| 21 | E05_US_024    | Guardar pedidos                                                  | COMO mesero QUIERO guardar los pedidos de una mesa PARA enviarlos a caja o cocina.                                                                                                                        | 3            |
| 22 | E06_US_025    | Imprimir pre-cuenta                                              | COMO administrador QUIERO imprimir el resumen de una orden PARA entregárselo al cliente antes de pagar.                                                                                                   | 3            |
| 23 | E06_US_026    | Cobrar orden                                                     | COMO administrador QUIERO cobrar la orden de un cliente con diversos métodos de pago PARA brindar comodidad al cliente.                                                                                   | 3            |
| 24 | E06_US_030    | Boletear o facturar la orden                                     | COMO administrador QUIERO emitir una factura o boleta PARA enviarla a la SUNAT después del pago.                                                                                                          | 3            |
| 25 | E07_US_032    | Filtrar ventas por platos                                        | COMO administrador QUIERO filtrar ventas por platos PARA identificar los más vendidos.                                                                                                                    | 4            |
| 26 | E07_US_036    | Editar platos existentes                                         | COMO administrador QUIERO editar los datos de los platos creados PARA mantenerlos actualizados.                                                                                                           | 4            |
| 27 | E05_US_023    | Tomar pedidos de la mesa                                         | COMO mesero QUIERO tomar pedidos desde una aplicación PARA agilizar la toma de órdenes.                                                                                                                   | 4            |
| 28 | E05_US_025    | Enviar pedido guardado a cocina y caja                           | COMO mesero QUIERO enviar pedidos a cocina o caja PARA continuar con el flujo de trabajo sin necesidad de dictar la orden manualmente.                                                                    | 4            |
| 29 | E06_US_027    | Crear un cliente con DNI o RUC                                   | COMO administrador QUIERO crear nuevos clientes con DNI o RUC PARA emitir documentos personalizados.                                                                                                      | 4            |
| 30 | E07_US_031    | Ver resumen de ventas                                            | COMO administrador QUIERO ver el resumen de ventas por días PARA saber cuánto se vendió en cada jornada.                                                                                                  | 4            |
| 31 | E07_US_033    | Ver resumen de productos restantes                               | COMO administrador QUIERO ver cuántos insumos quedan en inventario después de las ventas PARA controlar el stock.                                                                                         | 4            |
| 32 | E07_US_034    | Ingresar nuevos productos al inventario                          | COMO administrador QUIERO añadir insumos al inventario después de una compra PARA mantener el stock actualizado.                                                                                          | 4            |
| 33 | E07_US_035    | Crear platos nuevos                                              | COMO administrador QUIERO crear nuevos platos con sus precios e insumos necesarios PARA que los meseros puedan seleccionarlos al tomar una orden.                                                         | 4            |
| 34 | E04_US_019    | Recibir alerta cuando llega un cliente cruza la puerta del local | COMO mesero QUIERO recibir una alerta cuando un cliente entra al local PARA poder atenderlo rápidamente.                                                                                                  | 4            |
| 35 | E04_US_020    | Recibir alerta cuando cliente toma asiento en una mesa           | COMO mesero QUIERO recibir una alerta cuando un cliente se sienta en una mesa PARA poder generar el pedido en dicha mesa.                                                                                 | 4            |
| 36 | E04_US_021    | Recibir alerta cuando un cliente deja la mesa                    | COMO mesero QUIERO recibir una alerta cuando un cliente se va sin pagar PARA tomar las acciones necesarias.                                                                                               | 4            |
| 43 | E010_US043    | Inventariado de Insumos mediante IoT                             | **COMO** Administrador de restaurante, **QUIERO** recibir información actualizada cuando los insumos críticos estén bajos, **PARA** planificar mejor las compras y evitar interrupciones en el servicio.  | 5            |
| 44 | E010_US044    | Detectar Mesas y Clientes mediante IoT                           | **COMO** Administrador de restaurante, **QUIERO** conocer en tiempo real la ocupación de las mesas y el número de clientes, **PARA** optimizar la asignación de recursos y reducir los tiempos de espera. | 8            |

Se realizó el product backlog en trello:


<img src="./Resources/Evidences/Trello.jpg" >

Link: https://trello.com/invite/b/66f6fd07c57d7ffb39fd1676/ATTIf7c73a2657fb52ec9e301974ed4454e430361341/sprint-1-tecnogurus


## 3.4. Impact Mapping.

**Segmento Mesero**

El mesero es un elemento fundamental en el sector de la restauración, ya que su desempeño influye directamente en la satisfacción del cliente. Enfrenta desafíos diarios relacionados con la gestión de múltiples pedidos y la necesidad de mantener una comunicación efectiva con la cocina. Al comprender las necesidades y problemas que enfrenta, se puede diseñar una estrategia que optimice su flujo de trabajo, mejorando así tanto su eficiencia como la experiencia del cliente. Este enfoque permitirá no solo reducir la carga de trabajo del mesero, sino también fomentar un ambiente más positivo y productivo en el restaurante.

<img src="./Resources/images/im1.png" >

**Segmento Administrador**

El administrador del restaurante juega un papel crucial en la supervisión y optimización de las operaciones del negocio. Su responsabilidad incluye garantizar que las actividades se realicen de manera eficiente y rentable, así como tomar decisiones informadas basadas en el rendimiento del personal y las ventas. Al identificar las necesidades y desafíos que enfrenta, se puede desarrollar una estrategia que mejore su capacidad para analizar datos y gestionar recursos, lo que no solo optimiza las operaciones, sino que también potencia el éxito y la rentabilidad del restaurante.

<img src="./Resources/images/im2.png" >

