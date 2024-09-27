# Capítulo IV: Solution Software Design

## 4.1. Strategic-Level Domain-Driven-Design

En el siguiente apartado, se detalla una serie de enfoques clave en el proceso de Diseño Dirigido por el Dominio a nivel estratégico (Strategic-Level Domain-Driven Design). Estos enfoques fueron fundamentales para establecer una base sólida para definir y modelar dominios complejos. A través de técnicas como Event Storming, Context Mapping y la definición de la Arquitectura de Software, se logró obtener una comprensión profunda de los elementos esenciales necesarios para la creación de sistemas efectivos y bien estructurados. A continuación, se describen los puntos clave que se abordaron en esta sección.

### 4.1.1. Event Storming

Se abordó un enfoque colaborativo y visual que permitió modelar el contexto del dominio. Se exploraron las etapas de Candidate Context Discovery, Domain Message Flows Modeling y la creación de Bounded Context Canvases.

**Unstructured Exploration**

Es un enfoque visual que reúne a todas las partes interesadas para explorar el dominio de un sistema. Se utilizan notas adhesivas de diferentes colores para representar distintos elementos, facilitando la discusión y el descubrimiento de requisitos.

<img src="./Resources/images/EventStorming.png" >

**Pain Points**

Son los problemas o dificultades que enfrentan los usuarios y las partes interesadas en el contexto del sistema. Identificarlos ayuda a priorizar características y soluciones que realmente aborden las necesidades del usuario.

<img src="./Resources/images/PainPoints.png" >

**Timelines**

Se refiere a la secuencia de eventos que ocurren en el sistema a lo largo del tiempo. Establecer una línea de tiempo ayuda a visualizar cómo los eventos interactúan y afectan el flujo de trabajo, así como a identificar puntos críticos en el proceso.

<img src="./Resources/images/TimeLines.png" >

**Pivotal Points**

Son momentos clave en el flujo de eventos que pueden cambiar el estado del sistema o influir significativamente en la experiencia del usuario. Identificar estos puntos ayuda a concentrar esfuerzos en las áreas más críticas.

<img src="./Resources/images/PivotalPoints.png" >

**Commands**

Son las acciones o instrucciones que un usuario o sistema puede ejecutar para provocar un cambio en el estado del sistema. Por ejemplo, "Crear Pedido" o "Actualizar Inventario".

<img src="./Resources/images/Commands.png" >

**Policies**

Son las reglas o directrices que rigen cómo se deben tomar las decisiones dentro del sistema. Pueden incluir reglas de negocio que determinan cuándo se deben ejecutar ciertos comandos o cómo se deben manejar ciertos eventos.

<img src="./Resources/images/Policies.png" >

**Read Models**

Son las representaciones de los datos que se utilizan para responder a consultas o solicitudes de información. Los modelos de lectura están diseñados para optimizar la consulta de datos, separándose de los modelos de escritura para mejorar el rendimiento y la escalabilidad.

<img src="./Resources/images/ReadModels.png" >

**External Systems**

Se refiere a otros sistemas o servicios que interactúan con el sistema principal. Identificar estos sistemas ayuda a entender las dependencias y las integraciones necesarias para el funcionamiento del sistema.

<img src="./Resources/images/ExternalSystems.png" >

**Aggregates**

Son grupos de objetos que se tratan como una única unidad para la gestión de datos y la lógica de negocio. Un agregado garantiza la consistencia de sus partes en las operaciones y encapsula la lógica de negocio relacionada.

<img src="./Resources/images/Aggregates.png" >

**Bounded Context**

Es un límite claro dentro del dominio del sistema donde un modelo particular se aplica. Define la frontera en la que un conjunto de conceptos y términos tiene un significado específico, ayudando a evitar confusiones y a manejar complejidades en sistemas grandes y distribuidos.

<img src="./Resources/images/BoundedContext.png" >

Link del Event Storming: https://miro.com/app/board/uXjVKkI6spU=/

#### 4.1.1.1 Candidate Context Discovery

Empleando la metodología de Eventstorming con enfoque en la técnica de "start-with-simple", utilizamos la línea de tiempo para identificar posibles candidatos para nuestro contexto delimitado, los cuales son los siguientes: 

**Profile Managment:**

<img src="./Resources/images/Capitulo 4/Profile_Management.png" >

**Identity and Access Management:**

<img src="./Resources/images/Capitulo 4/Identity_Access_Management.png" >

**Business Managment System:**

<img src="./Resources/images/Capitulo 4/Bussiness_Management_System.png" >

**IoT Asset Management:**

<img src="./Resources/images/Capitulo 4/IoT_Asset_Management.png" >

**Subscription and Payments:**

<img src="./Resources/images/Capitulo 4/Subscription_Payments.png" >

**Notification Managment:**

<img src="./Resources/images/Capitulo 4/Notification_management.png" >

**Data Report and Analytics:**

<img src="./Resources/images/Capitulo 4/Data_Report_Analytics.png" >

#### 4.1.1.2 Domain Message Flows Modeling

1. Scenario: Registering in the app
   
<img src="./Resources/images/Capitulo 4/41121.png" >

2. Scenario: Pay a subscription

<img src="./Resources/images/Capitulo 4/41122.png" >

3. Real-Time Progress Record

<img src="./Resources/images/Capitulo 4/41123.png" >
   
4. Alert the waiter plates ready to be collected

<img src="./Resources/images/Capitulo 4/41124.png" >

#### 4.1.1.3 Bounded Context Canvases

1. Profile Management

<img src="./Resources/images/Capitulo 4/41131.png" >

2. Identity and access management

<img src="./Resources/images/Capitulo 4/41132.png" >

3. Agricultural Management System

<img src="./Resources/images/Capitulo 4/41133.png" >

4. IoT Assets Management

<img src="./Resources/images/Capitulo 4/41134.png" >

5. Data report & Analytics

<img src="./Resources/images/Capitulo 4/41135.png" >

6. Subscription and Payments

<img src="./Resources/images/Capitulo 4/41136.png" >

7. Notification Management

<img src="./Resources/images/Capitulo 4/41137.png" >

### 4.1.2	Context Mapping

<img src="./Resources/images/Capitulo 4/412.png" >

### 4.1.3	Software Architecture

#### 4.1.3.1	Software Architecture System Landscape Diagram

<img src="./Resources/images/Capitulo 4/4131.png" >

#### 4.1.3.2	Software Architecture Context Level Diagrams

<img src="./Resources/images/Capitulo 4/4132.png" >

#### 4.1.3.3	Software Architecture Container Level Diagrams

<img src="./Resources/images/Capitulo 4/4133.png" >

#### 4.1.3.4	Software Architecture Deployment Diagrams

<img src="./Resources/images/Capitulo 4/4134.png" >

## 4.2. Tactical-Level Doamin-Driven-Design
### 4.2.1 Bounded Context: Profile Management
#### 4.2.1.1 Domain Layer
- **UserProfile:** Esta entidad representa el perfil del usuario y puede contener atributos como nombre, apellidos, dirección de correo electrónico, número de teléfono, foto de perfil, y otros detalles personales. También puede incluir métodos para actualizar la información del perfil. 

- **ProfilePrivacySettings:** Esta entidad define la configuración de privacidad del perfil, permitiendo a los usuarios controlar quién puede ver ciertos elementos de su perfil. Puede contener atributos como configuraciones de privacidad para la foto de perfil, la dirección de correo electrónico, la lista de amigos, etc. 

- **ProfileActivity:** Esta entidad registra la actividad del usuario en su perfil, como cambios de foto de perfil, actualizaciones de información, etc. Esto puede ayudar a rastrear el historial de actividad del perfil y puede ser útil para funcionalidades como la generación de noticias o mejoras al servicio de riego automático de actividad para los usuarios.
  
#### 4.2.1.2 Interface Layer
- **ProfileViewController:** Este controlador maneja las solicitudes relacionadas con la visualización del perfil del usuario. Permite a los usuarios ver su información de perfil y configurar la privacidad de sus datos. 

- **ProfileUpdateController:** Este controlador se encarga de las solicitudes de actualización de información de perfil. Facilita a los usuarios la capacidad de modificar su información personal, incluyendo la foto de perfil. 

- **ProfileDeleteController:** Este controlador se encarga de las solicitudes de eliminación del perfil. Permite a los usuarios la capacidad de eliminar su información de su perfil de la base de datos.
  
#### 4.2.1.3 Application Layer
- **ProfileViewService:** Este servicio de aplicación se encarga de procesar las solicitudes de visualización de perfiles de usuario. Accede a la base de datos para recuperar la información del perfil y aplica las configuraciones de privacidad antes de mostrarla al usuario. 

- **ProfileUpdateService:** Se encarga de procesar las solicitudes de actualización de información de perfil. Valida los cambios propuestos por el usuario, actualiza los datos en la base de datos y registra la actividad correspondiente en el perfil. 

- **ProfileDeleteService:** Se encarga de procesar las solicitudes de eliminación del perfil, actualiza los datos en la BD correspondiente a su perfil.

#### 4.2.1.4 Infraestructure Layer
- **ProfileRepository:** Esta clase interactúa con la base de datos para realizar operaciones de lectura y escritura de información de perfiles de usuario. Almacena y recupera datos de perfil, configuraciones de privacidad y actividad. Puede implementar métodos como getUserProfile, updateUserProfile, getPrivacySettings, updatePrivacySettings, getActivityLog, etc. 

- **ImageStorageService:** Este servicio se encarga de almacenar y recuperar imágenes de perfil de usuario, como las fotos de perfil. Puede estar conectado a un sistema de almacenamiento de objetos para gestionar eficazmente las imágenes. Puedes implementar métodos como uploadImage, getImage, deleteImage, etc. 

- **PrivacySettingsRepository:** Esta clase almacena y recupera la configuración de privacidad de los perfiles de usuario. Puedes implementar métodos como getPrivacySettings, updatePrivacySettings, etc. 

- **ActivityLogRepository:** Esta clase registra y recupera la actividad del perfil de usuario. Puedes implementar métodos como logActivity, getActivityLog, etc. 

#### 4.2.1.5 Bounded Context Software Architecture Component Level Diagrams

<img src="./Resources/images/Capitulo 4/4215.png" >

#### 4.2.1.6 Bounded Context Software Achitecture Code Level Diagrams
4.2.1.6.1 Bounded Context Domain Layer Class Diagrams

<img src="./Resources/images/Capitulo 4/42161.png" >

4.2.1.6.2 Bounded Context Database Design Diagram 

<img src="./Resources/images/Capitulo 4/42162.png" >

### 4.2.2 Bounded Context: Identity and Access Management
#### 4.2.2.1 Domain Layer
- **User:** Clase que representa entidades como User (características del usuario), Role (definición del usuario), y Permission (acciones a las que puede acceder). 

- **DomainService:** Métodos y funciones que realizan operaciones relacionadas con la gestión de la identidad y acceso, como la creación de usuario, asignación de roles o revocar permisos.  

- **PermissionService:** Lógica que determina qué acciones están permitidas para un usuario según su rol y permisos, como verificar si un usuario tiene autorización para realizar ciertas operaciones.

#### 4.2.2.2 Interface Layer
- **UserController:** Esta capa podría incluir vistas para que los administradores gestionen usuarios, roles y permisos. 

- **ValidationController:** Validación para asegurar que los datos de los usuarios sean precisos y seguros, así como que los cambios a los permisos se realicen de acuerdo con las políticas de seguridad.

#### 4.2.2.3 Application Layer
- **ValidationService:** Implementación de funciones específicas como el manejo de roles o la autenticación de usuarios que coordinan las operaciones necesarias para la gestión de identidad y acceso. 

- **WorkService:** Procesos que definen cómo se manejan tareas como la creación de nuevos usuarios o la actualización de permisos. 

- **ManagementService:** Asegurar que las operaciones de cambios en roles, permisos y otros datos de usuarios se realicen de manera segura y consistente.

#### 4.2.2.4 Infrastructure Layer
- **DataRespository:** Herramienta de almacenamiento para guardar y recuperar datos de usuarios, roles y permisos. 

- **AuthenticationRepository:** Herramientas para el manejo de la autenticación y autorización de usuarios, como la integración con sistemas de autenticación externos.  

- **MonitoringRepository:** Herramientas para registrar y monitorear los intentos de autenticación, cambios de permisos y otras actividades de usuarios para detectar comportamientos inusuales o potenciales amenazas de seguridad.

#### 4.2.2.5 Bounded Context Software Architecture Component Level Diagrams 

<img src="./Resources/images/Capitulo 4/4225.png" >

#### 4.2.2.6 Bounded Context Software Architecture Code Level Diagrams
4.2.2.6.1 Bounded Context Domain Layer Class Diagrams 

<img src="./Resources/images/Capitulo 4/42261.png" >

4.2.2.6.2 Bounded Context Database Design Diagram 

<img src="./Resources/images/Capitulo 4/42262.png" >

### 4.2.3 Bounded Context: Business Management System
#### 4.2.3.1 Domain Layer
- **Business:** Representa conceptos para el sector de comida clave como los platillos, el tipo de negocio de comida y sus comensales. 

- **Business Service:** Métodos y funciones que realizan operaciones automatizadas de gestión de restaurantes, como detectar la llegada de clientes, asignar mesas automáticamente, gestionar pedidos y actualizar el estado de las mesas. 

- **Business Rule:** Lógica que establece reglas para automatizar la gestión del servicio, como asignar mesas en función de la ocupación y la disponibilidad, priorizar los pedidos según el tiempo de espera, y gestionar la recolección de platos en función del estado de las mesas.

#### 4.2.3.2 Interface Layer
- **BusinessController:** Vistas y componentes de la interfaz de usuario que permiten a los administradores gestionar mesas, pedidos y el estado del restaurante de manera automatizada. 

- **BusinessDataController:** Validadores para asegurar que los datos proporcionados por los usuarios (como pedidos o cambios de estado de mesas) sean correctos y seguros, garantizando una gestión eficiente.

#### 4.2.3.3 Application Layer
- **RestaurantService:** Funciones específicas como ManageTables (Gestionar mesas) o OptimizeOrderFlow (Optimizar flujo de pedidos), que orquestan las operaciones necesarias para la gestión eficiente del restaurante. 

- **RestaurantWorkflowService:** Procesos que definen cómo se llevan a cabo tareas como asignar mesas, procesar pedidos, y gestionar el servicio en función del estado del restaurante. 

- **OperationsService:** Mecanismos para asegurar la consistencia y seguridad de las operaciones del restaurante, como la gestión de pedidos y la automatización del control de mesas y platos.

#### 4.2.3.4 Infrastructure Layer
- **RestaurantDataRepository:** Herramienta de almacenamiento para gestionar los datos del restaurante, como información sobre mesas, pedidos, y disponibilidad de personal. 

- **RestaurantIntegrationsRepository:** Integración con servicios externos, como proveedores de pagos digitales, sistemas de reservas o plataformas de entrega a domicilio. 

- **RestaurantMonitoringRepository:** Herramientas para monitorear el estado de las mesas, la ocupación, y analizar los datos del restaurante para optimizar el servicio y la atención al cliente.

#### 4.2.3.5 Bounded Context Software Architecture Component Level Diagrams 

<img src="./Resources/images/Capitulo 4/4235.png" >

#### 4.2.3.6 Bounded Context Software Architecture Code Level Diagrams 
4.2.3.6.1 Bounded Context Domain Layer Class Diagrams 

<img src="./Resources/images/Capitulo 4/42361.png" >

4.2.3.6.2 Bounded Context Database Design Diagram 

<img src="./Resources/images/Capitulo 4/42362.png" >

### 4.2.4 Bounded Context: IoT Asset Management 
#### 4.2.4.1 Domain Layer 
- **Asset:** Representa los conceptos claves de los Dispositivos IoT 

- **AssetService:** Métodos y funciones que realizan operaciones relacionadas con activos de IoT, como registrar un nuevo dispositivo, el estado de un dispositivo y gestionar datos de sensores. 

- **AssetRule:** Lógica que establece normas para las operaciones relacionadas con los activos de IoT. 

- **ProgressRecord:** Esta entidad representa el registro del progreso en tiempo real respecto a la información que digiere constantemente referente al cliente.

#### 4.2.4.2 Interface Layer 
- **AssetController:** Este controlador maneja solicitudes respecto a los sensores IoT y recibe datos en tiempo real, desencadenando acciones dentro del sistema según las condiciones detectadas. 

- **ProgressRecordController:** Este controlador se encarga de las supervisar y actualizar los procesos de negocio que está siendo supervisado mediante los dispositivos IoT.

#### 4.2.4.3 Application Layer 

- **IoTService:** Funciones específicas como gestionar dispositivos o analizar datos de sensores que orquestan las operaciones necesarias para gestionar los activos. 

- **IoTWorkService:** Procesos que definen cómo se llevan a cabo tareas como registrar dispositivos, gestionar sensores, y trabajar con datos de dispositivos. 

- **IoTManagementService:** Mecanismos para asegurar la consistencia y seguridad de las operaciones relacionadas con activos de IoT, como la actualización de dispositivos y la gestión de datos de sensores.

#### 4.2.4.4 Infrastructure Layer
- **IoTDataRepository:** Herramienta de almacenamiento para gestionar los datos de dispositivos y sensores. 

- **IntegrationRepository:** Integración con servicios externos, como servicios de nube o plataformas de terceros. 

- **IoTMonitoringRepository:** Herramientas para monitorear el estado de los dispositivos, el rendimiento de los sensores, y realizar análisis de datos para mejorar la gestión de activos de IoT.

#### 4.2.4.5 Bounded Context Software Architecture Component Level Diagrams 

<img src="./Resources/images/Capitulo 4/4245.png" >

#### 4.2.4.6 Bounded Context Software Architecture Code Level Diagrams 

4.2.4.6.1 Bounded Context Domain Layer Class Diagrams 

<img src="./Resources/images/Capitulo 4/42461.png" >

4.2.4.6.2 Bounded Context Database Design Diagram 

<img src="./Resources/images/Capitulo 4/42462.png" >

### 4.2.5 Bounded Context: Subscription and Payments
#### 4.2.5.1 Domain Layer
- **Subscription:** Representa conceptos clave relacionados con las suscripciones, como suscripción y del cliente. 

- **Payment:** Clase que representan conceptos clave relacionados con los pagos, como pago y factura. 

- **SubscriptionRule:** Reglas que definen políticas y condiciones para gestionar suscripciones y pagos, como reglas de renovación automática, cancelación, y manejo de facturación.

#### 4.2.5.2 Interface Layer 

- **PaymentController:** Componente de la interfaz de usuario que permiten a los clientes gestionar suscripciones, revisar facturas, y realizar pagos. 

- **PaymentValidationController:** Mecanismos para verificar la validez de la información de pago proporcionada por los clientes, como métodos de pago aceptados y detalles de tarjetas de crédito. 

- **SubscriptionManagementController:** Un portal de gestión de suscripciones que permite a los clientes revisar, actualizar, o cancelar suscripciones existentes. También les permite ver y gestionar sus métodos de pago guardados, ajustar preferencias de facturación, y acceder a un historial de transacciones y pagos. 

#### 4.2.5.3 Application Layer 

- **SubscriptionService:** Funciones para gestionar suscripciones, incluyendo la creación, actualización, y cancelación de suscripciones. 

- **PaymentService:** Procesos para gestionar pagos de clientes, como autorización, captura, y reembolso de pagos. 

- **InvoiceService:** Procesos para generar, enviar, y administrar facturas para las suscripciones de los clientes.

#### 4.2.5.4 Infrastructure Layer 

- **PaymentRepository:** Integración con pasarelas de pago externas para procesar transacciones de pago de forma segura. 

- **PaymentStorageRepository:** Herramienta de almacenamiento para gestionar datos relacionados con clientes, suscripciones, pagos, y facturas. 

- **PaymentSecurityRepository:** Herramienta para garantizar la seguridad y cumplimiento de las transacciones de pago y datos de clientes.

#### 4.2.5.5 Bounded Context Software Architecture Component Level Diagrams 

<img src="./Resources/images/Capitulo 4/4255.png" >

#### 4.2.5.6 Bounded Context Software Architecture Code Level Diagrams 
4.2.5.6.1 Bounded Context Domain Layer Class Diagrams 

<img src="./Resources/images/Capitulo 4/42561.png" >

4.2.5.6.2 Bounded Context Database Design Diagram 

<img src="./Resources/images/Capitulo 4/42562.png" >

### 4.2.6 Bounded Context: Notification Management 
#### 4.2.6.1 Domain Layer
- **Notification:** Clase que representa conceptos clave relacionados con las notificaciones, como notificación, y plantilla. 

- **NotificationRule:** Lógica que define cuándo y cómo se deben enviar notificaciones. 

#### 4.2.6.2 Interface Layer 

- **NotificationController:** Este controlador maneja las notificaciones, asegurándose de enviar avisos o alertas basadas en eventos o condiciones detectadas. 

#### 4.2.6.3 Application Layer 

- **NotificationService:** Planificación de notificaciones para determinar cuándo y a qué destinatarios se deben enviar, considerando factores como la zona horaria, la urgencia, y las preferencias del usuario. 

- **NotificationDeliveryService:** Seguimiento del envío de notificaciones a través de los distintos canales, asegurando la entrega correcta y oportuna de los mensajes. 

- **NotificationTrackingService:** Seguimiento del estado de las notificaciones, incluyendo la confirmación de entrega y la respuesta del destinatario si es relevante. 

#### 4.2.6.4 Infrastructure Layer 

- **NotificationRepository:** Herramienta necesaria para enviar notificaciones a través de distintos canales, como servicios de correo electrónico, SMS, y push notifications. 

- **NotificationStorageRepository:** Almacenamiento de datos de notificaciones, incluyendo historiales de mensajes enviados, recibidos, y pendientes de enviar. 

- **NotificatoinScalabilityRepository:** Herramientas y técnicas para manejar cargas de trabajo intensivas, especialmente durante períodos de alta demanda de notificaciones, asegurando un rendimiento estable y rápido. 

#### 4.2.6.5 Bounded Context Software Architecture Component Level Diagrams 

<img src="./Resources/images/Capitulo 4/4265.png" >

#### 4.2.6.6 Bounded Context Software Architecture Code Level Diagrams 
4.2.6.6.1 Bounded Context Domain Layer Class Diagrams 

<img src="./Resources/images/Capitulo 4/42661.png" >

4.2.6.6.2 Bounded Context Database Design Diagram 

<img src="./Resources/images/Capitulo 4/42662.png" >

### 4.2.7 Bounded Context: Data Report and Analytics 
#### 4.2.7.1 Domain Layer 

- **ReportEntity:** Clase que representa conceptos clave de informes, como Informe y Visualización. 

- **Afterservice:** Representa las definiciones respecto a las actividades que proceden después que el cliente se retire, como la limpieza de las mesas. 

- **ReportRule:** Reglas que definen las políticas y restricciones para la generación de informes, como reglas de privacidad de la información o los datos de la facturación. 

#### 4.2.7.2 Interface Layer 

- **ReportControllers:** Permitirá a los usuarios explorar y visualizar los datos obtenidos de la estadía de los usuarios de manera intuitiva y precisa. 

- **AccessController:** Mecanismos para gestionar el acceso de los usuarios a informes, análisis, y conjuntos de datos, asegurando la confidencialidad de la información. 

#### 4.2.7.3 Application Layer 

- **ReportService:** Funciones para gestionar la creación, programación, y entrega de informes, como programar informe o compartir informe. 

- **AnalysisService:** Análisis de datos, incluyendo la selección de modelos y métodos de análisis adecuados. 

- **VisualizationService:** Generación de visualizaciones efectivas y personalizadas para representar los resultados de análisis y datos de informes. 

#### 4.2.7.4 Infrastructure Layer 

- **ReportRepository:** Herramienta de almacenamiento de datos optimizado para facilitar la generación de informes y análisis, incluyendo bases de datos, data lakes, y data marts. 

- **AnalyticRepository:** Herramientas para realizar análisis avanzados, como bibliotecas de análisis de datos, motores de cálculo, y servicios de machine learning. 

- **ReportRepository:** Herramientas para la creación, personalización, y distribución de informes, incluyendo plataformas de generación de informes, editores de visualizaciones, y generadores de dashboards. 

#### 4.2.7.5 Bounded Context Software Architecture Component Level Diagrams

<img src="./Resources/images/Capitulo 4/4275.png" >

#### 4.2.7.6 Bounded Context Software Architecture Code Level Diagrams 
4.2.7.6.1 Bounded Context Domain Layer Class Diagrams

<img src="./Resources/images/Capitulo 4/42761.png" >

4.2.7.6.2 Bounded Context Database Design Diagram 

<img src="./Resources/images/Capitulo 4/42762.png" >
