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
6. ¿La implementación de un sistema de pago rápido reduce el tiempo de cobro y errores en el proceso?
7. ¿Un historial de ventas mejora la capacidad de los gerentes para obtener insights rápidos y tomar mejores decisiones?
8. ¿Un sistema de movimientos de caja mejora la transparencia y el control financiero?

### 8.1.4. Question Backlog

| # | Pregunta                                                                                | Impacto Potencial                       |
|---|-----------------------------------------------------------------------------------------|-----------------------------------------|
| 1 | ¿Tener un historial de pedidos por mesa mejora la precisión y velocidad del servicio?   | Alto (mejora servicio y reduce errores) |
| 2 | ¿La visibilidad de los productos más vendidos mejora la gestión del menú?               | Medio (optimiza decisiones de menú)     |
| 3 | ¿Una mensajería interna mejora la coordinación entre meseros y cocina?                  | Alto (reduce errores y demoras)         |
| 4 | ¿La implementación de un historial de pedidos reduce los errores en la toma de pedidos? | Alto (reduce errores operativos)        |
| 5 | ¿La división automática de cuentas disminuye el tiempo de espera para los clientes?     | Medio-Alto (agiliza cobro y rotación)   |
| 6 | ¿La implementación de un sistema de pago rápido reduce el tiempo de cobro y errores en el proceso? | Alto (mejora experiencia y reduce errores)         |
| 7 | ¿Un historial de ventas mejora la capacidad de los gerentes para obtener insights rápidos y tomar mejores decisiones? | Medio-Alto (mejora toma de decisiones) |
| 8 | ¿Un sistema de movimientos de caja mejora la transparencia y el control financiero?                | Alto (mejora control y reduce errores)             |
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

### 🧪 *Experiment Card 6: Pago de Cuentas*

| *Supuestos*                                                  | *Question Backlog*                                                         |
|--------------------------------------------------------------|----------------------------------------------------------------------------|
| El proceso de pago de cuentas es lento y propenso a errores. | ¿La implementación de un sistema de pago rápido reduce el tiempo de cobro? |

| *Experiment Card* |                                                                                                           |
|-------------------|-----------------------------------------------------------------------------------------------------------|
| *Question*        | ¿La implementación de un sistema de pago rápido reduce el tiempo de cobro?                                |
| *Why*             | Mejora la experiencia del cliente y reduce el tiempo de espera en el pago.                                |
| *What*            | Implementar un sistema de pago rápido con opciones de pago digital y medir el tiempo de cobro.            |
| *Hypothesis*      | Si se implementa un sistema de pago rápido, se reduce el tiempo de cobro en un 30% y se eliminan errores. |
| *Métricas*        | Tiempo promedio de cobro y cantidad de errores en el proceso de pago.                                     |
| *Metas*           | -30% en tiempo de cobro, -90% en errores, +15% en satisfacción del cliente                                |

### 🧪 *Experiment Card 7: Historial de Ventas*

| *Supuestos*                                                           | *Question Backlog*                                     |
|-----------------------------------------------------------------------|--------------------------------------------------------|
| Los gerentes necesitan analizar tendencias de ventas de forma rápida. | ¿Un historial de ventas  mejora la toma de decisiones? |

| *Experiment Card* |                                                                                                                                                                      |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Question*        | ¿Un historial de ventas mejora la capacidad de los gerentes para obtener insights rápidos?                                                                           |
| *Why*             | Permite a los gerentes y administradores identificar rápidamente patrones, productos de alta demanda o rendimientos individuales, facilitando la toma de decisiones. |
| *What*            | Implementar un historial de ventas accesible desde el dashboard del administrador                                                                                    |
| *Hypothesis*      | Si se implementa un historial de ventas, los gerentes podrán identificar tendencias y tomar decisiones más informadas, mejorando la eficiencia operativa en un 20%.  |
| *Métricas*        | Tiempo promedio para generar reportes de ventas y número de insights accionables identificados.                                                                      |
| *Metas*           | -20% en tiempo de generación de reportes, +30% en insights accionables identificados.                                                                                |

### 🧪 *Experiment Card 8: Movimientos de Caja*

| *Supuestos*                                                                | *Question Backlog*                                                               |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| La gestión de caja es propensa a errores y requiere seguimiento constante. | ¿Un sistema de movimientos de caja mejora la transparencia y control financiero? |

| *Experiment Card* |                                                                                                                                                                |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Question*        | ¿Un sistema de movimientos de caja mejora la transparencia y control financiero?                                                                               |
| *Why*             | Permite un seguimiento detallado de ingresos y egresos, facilitando control financiero.                                                                        |
| *What*            | Implementar un sistema de registro de movimientos de caja con reportes diarios accesibles.                                                                     |
| *Hypothesis*      | Si se implementa un sistema de movimientos de caja, se reducirá el número de errores en el cierre de caja en un 40% y se mejorará la transparencia financiera. |
| *Métricas*        | Número de errores en cierres de caja y tiempo promedio para generar reportes de caja.                                                                          |
| *Metas*           | -40% en errores de cierre de caja, +50% en transparencia financiera.                                                                                           |

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

### 8.3.2. To-Be Product Backlog


