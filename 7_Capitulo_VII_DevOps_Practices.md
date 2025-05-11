# Capítulo VII: DevOps Practices

## 7.1. Continuous Integration
### 7.1.1. Tools and Practices.
Para implementar integración continua en KitchenTech, utilizamos las siguientes herramientas y prácticas:

- **GitHub**: Es nuestra plataforma principal de control de versiones. Nos permite trabajar en ramas separadas, realizar revisiones de código y mantener un historial claro de cambios. Utilizamos GitFlow como estrategia de ramificación para mantener la estabilidad en main y la evolución continua en develop.

- **GitHub Actions**: Configuramos flujos de trabajo automatizados que se ejecutan cada vez que se hace un push o pull request en ramas clave. Estos workflows realizan compilación, pruebas y validaciones.

Pruebas automatizadas:

- **JUnit**: Se utiliza para ejecutar pruebas unitarias en los módulos backend desarrollados en Java Spring Boot.

- **Selenium**: Para pruebas de interfaz en los flujos principales de interacción del sistema (reservas, pedidos, cobros).

Estas herramientas nos permiten detectar errores de forma temprana y asegurar la calidad del código desde las primeras etapas del desarrollo.

### 7.1.2. Build & Test Suite Pipeline Components.

Hemos definido un pipeline de integración continua en GitHub Actions con los siguientes componentes:

- **Trigger**: Cada vez que se realiza un push a las ramas main o develop.

- **Build Stage**: Se compila el código de backend utilizando Maven.

- **Test Stage**:
    - Se ejecutan pruebas unitarias con JUnit.

    - Se lanzan pruebas automáticas de interfaz con Selenium sobre entornos de staging.

Esto garantiza que los cambios nuevos no afecten funcionalidades críticas y se mantenga la calidad del sistema antes de pasar a etapas de entrega.

## 7.2. Continuous Delivery
### 7.2.1. Tools and Practices.

Utilizamos GitHub Actions también como soporte para la entrega continua. Una vez validadas las pruebas, el código se empaqueta y prepara automáticamente para despliegue.

- **GitHub Actions**: Orquesta la automatización del proceso de entrega.

- **Vercel**: Es nuestra plataforma de hosting para el frontend web, que se actualiza automáticamente cuando se realiza un push exitoso en la rama main.

Esta automatización nos permite reducir tiempos de entrega, mantener versiones consistentes y facilitar pruebas por parte de stakeholders.

### 7.2.2. Stages Deployment Pipeline Components.

Nuestro pipeline de entrega está estructurado en las siguientes etapas:

- **Source Stage**: Detección automática de cambios en main.

- **Build Stage**: Instalación de dependencias (npm para frontend), compilación del frontend.

- **Test Stage**: Ejecución de pruebas unitarias y de integración.

- **Approval Stage**: Aprobación manual de pull requests.

- **Deployment Stage**: Despliegue automático a producción vía Vercel.

- **Monitoring Stage**: En esta etapa aún estamos evaluando herramientas como Prometheus y Grafana para integración futura.

## 7.3. Continuous deployment
### 7.3.1. Tools and Practices.
Para KitchenTech, el despliegue continuo se logra a través de la integración directa de GitHub con Vercel. Cada commit aprobado y mergeado en main genera un despliegue automático a producción, sin necesidad de intervención manual.

Esta práctica elimina el tiempo muerto entre codificación y disponibilidad del sistema para usuarios reales, acelerando nuestro ciclo de entregas.

### 7.3.2. Production Deployment Pipeline Components.
El pipeline de producción incluye las siguientes etapas:

- **Build**: Se construye automáticamente el frontend con npm run build al hacer push en main.

- **Test**: Se ejecutan pruebas automatizadas de funcionalidad con Selenium.

- **Deployment**: Vercel realiza el despliegue inmediato al entorno productivo.

- **Feedback**: El equipo recibe notificaciones sobre el estado del build, errores y versiones desplegadas.


