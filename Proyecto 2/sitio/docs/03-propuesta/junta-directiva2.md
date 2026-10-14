---
sidebar_position: 2
---

# Junta Directiva Técnica

## 1. Introducción

La junta directiva técnica forma parte del Proyecto 2 del curso Comunicación Asertiva. Su propósito es evaluar las soluciones propuestas para **Manos Sobre la Pizza**, a partir de la información obtenida durante la entrevista con el encargado del negocio. Se busca comparar las alternativas desde las perspectivas del cliente, la gestión del proyecto, el desarrollo del sistema y el control de calidad.

El ejercicio permite aplicar la comunicación asertiva y la negociación técnica para definir una solución que responda a necesidades reales, sin perder de vista el tiempo de desarrollo, el costo, la facilidad de uso y los riesgos de implementación.

## 2. Objetivo

Analizar las oportunidades de mejora identificadas en Manos Sobre la Pizza, comparar diferentes soluciones tecnológicas y establecer criterios para seleccionar una alternativa viable, considerando las necesidades del negocio y las limitaciones de un proyecto de desarrollo de software.

## 3. Información del negocio

**Nombre:** Manos Sobre la Pizza  
**Actividad:** Venta de pizzas y otros alimentos en un kiosco universitario, además de servicios de catering para eventos.  
**Ubicación de la actividad entrevistada:** Universidad de San Carlos de Guatemala.  
**Modalidad prevista de la junta:** Presencial.  
**Fecha, lugar y duración de la junta:** Se registrarán de acuerdo con la grabación definitiva.

La entrevista se realizó con el encargado del negocio, Hans Escobedo, quien explicó el funcionamiento del kiosco, el procedimiento para atender clientes y la forma en que administran productos y eventos.

### Participantes de la simulación

El grupo está conformado por Denis Abad, Esther García, Pablo Colop, Walter Martínez, Aura Marina y Chung Kim. Los seis roles contemplados en el proyecto son **Product Manager**, **Tech Lead / Arquitecto**, **Cliente / Stakeholder**, **QA / Auditor**, **Scrum Master / Mediador** y **Desarrollador**. La asignación de cada papel se confirmará con el video de la junta para no registrar información incorrecta.

## 4. Información obtenida durante la entrevista

### 4.1 Funcionamiento diario

El kiosco normalmente atiende de **9:00 a. m. a 6:00 p. m.**, aunque las ventas varían de acuerdo con la actividad y la temporada universitaria. El negocio prepara alimentos para venderlos frescos y calientes. El tiempo de preparación de una pizza puede rondar los diez minutos, mientras que la entrega de un producto solicitado suele tomar pocos minutos, dependiendo de la demanda.

El trabajo se distribuye entre la preparación de suministros, el armado del producto, el horneado y el despacho. Cuando hay mayor movimiento, las pizzas salen del horno y se entregan con rapidez; cuando la demanda es baja, puede ser necesario esperar a que el producto se prepare o caliente.

### 4.2 Inventario y ventas

Para controlar los productos, el personal cuenta los suministros al comenzar la jornada y vuelve a contarlos al cierre. A partir de la diferencia estima lo vendido. El encargado indicó que utiliza **WhatsApp** como apoyo para llevar registros y que los costos de los suministros ya están establecidos.

En la entrevista no se reportaron pérdidas frecuentes de información ni errores graves de registro. Sin embargo, el encargado consideró útil la posibilidad de contar con un inventario digital que actualice las existencias conforme se registren las ventas.

### 4.3 Atención de pedidos

Los clientes solicitan y pagan sus productos directamente en el kiosco, ya sea en efectivo o mediante pago con QR. En momentos de mayor afluencia es importante respetar el orden de llegada y de entrega. Por ello, se identificó la oportunidad de mantener un registro sencillo de los pedidos pendientes, en preparación y entregados.

### 4.4 Servicios de catering

El negocio también ofrece servicios para eventos. Para elaborar una cotización, primero consulta la cantidad de invitados y las porciones requeridas. Una vez aprobado el presupuesto, el cliente realiza un **anticipo del 50 %** y paga el **50 % restante al finalizar el evento**. El servicio incluye trasladar el horno y contar con personal para preparar y servir las pizzas en el lugar.

### 4.5 Promociones y entregas

El encargado manifestó interés en atraer más clientes mediante promociones y presencia en redes sociales. También indicó que ha considerado implementar entregas a pie dentro de la universidad, ya que algunos clientes se las han solicitado. Actualmente reciben consultas mediante WhatsApp.

Un criterio importante señalado por el encargado es que cualquier nueva herramienta debe **simplificar el trabajo y no complicarlo**.

## 5. Propuestas de solución

A partir de estos hallazgos se prepararon seis propuestas distintas para su evaluación:

| Propuesta | Descripción | Beneficio esperado |
| --- | --- | --- |
| Inventario digital | Registrar cantidades iniciales y descontar productos conforme se venden. | Consultar existencias y facilitar el control diario. |
| Organización de pedidos | Registrar el número y estado de cada pedido. | Mantener el orden de atención en horas de mayor demanda. |
| Gestión de eventos y cotizaciones | Registrar fechas, invitados, presupuestos, anticipos y pagos pendientes. | Organizar la información de los servicios de catering. |
| Entregas dentro de la USAC | Registrar producto, ubicación y contacto del cliente, con apoyo de WhatsApp. | Facilitar la coordinación de entregas dentro del campus. |
| Promociones digitales | Planificar publicaciones de productos, ofertas y servicios. | Mejorar la visibilidad del negocio y atraer clientes. |
| Registro y análisis de ventas | Guardar ventas por producto y consultar resúmenes por períodos. | Identificar productos de mayor demanda y apoyar las compras. |

Estas propuestas representan **alternativas de mejora**, no funcionalidades que el negocio ya tenga implementadas ni decisiones que deban considerarse aprobadas de antemano.

## 6. Comparación de alternativas

Para evaluar el alcance de una posible solución se definieron tres alternativas generales:

| Alternativa | Características | Ventajas | Limitaciones |
| --- | --- | --- | --- |
| **A. Sistema completo** | Incluye inventario, ventas, pedidos, entregas, eventos y promociones. | Centraliza varios procesos del negocio. | Requiere mayor tiempo de desarrollo, capacitación y pruebas. |
| **B. Implementación por etapas** | Comienza con inventario y registro de ventas; incorpora otras funciones posteriormente. | Permite comprobar primero las funciones esenciales y mantener un alcance manejable. | Las demás necesidades quedan pendientes para futuras etapas. |
| **C. Priorizar pedidos y entregas** | Registra pedidos y posibles entregas, conservando WhatsApp como medio de comunicación. | Aprovecha una herramienta que el encargado ya conoce. | El inventario continúa gestionándose por el procedimiento actual. |

### Criterios de evaluación

**Tiempo de desarrollo.** Un sistema con muchas funciones necesita más planificación, implementación y pruebas. Una primera versión reducida puede estar disponible antes.

**Costo.** Deben contemplarse los recursos necesarios para desarrollar, utilizar y mantener la herramienta. La complejidad adicional no siempre representa un beneficio inmediato para un negocio pequeño.

**Facilidad de uso.** La solución debe adaptarse al trabajo cotidiano del encargado y su personal. Una interfaz complicada podría aumentar el tiempo necesario para atender clientes.

**Calidad.** Se deben verificar los registros de ventas, las cantidades disponibles, los cambios de estado de los pedidos y la recuperación ante errores. Reducir el alcance no debe significar omitir controles básicos.

**Utilidad para el negocio.** Las funciones seleccionadas deben responder a oportunidades mencionadas en la entrevista y aportar mejoras concretas, en lugar de incluir características solamente por su atractivo técnico.

## 7. Análisis técnico y de negocio

### 7.1 Alcance del sistema

Una solución que reúna todas las propuestas podría ser útil a largo plazo, pero también implicaría un desarrollo más amplio. En particular, los pedidos a distancia y las entregas requieren definir quién los recibirá, cómo se confirmarán, qué zonas se atenderán y qué sucede si se cancela una solicitud.

Por otro lado, el inventario y el registro de ventas están estrechamente relacionados. Si se registra una venta y se descuenta automáticamente el producto correspondiente, el encargado podría consultar existencias sin depender exclusivamente del conteo de cierre. No obstante, sería necesario contemplar casos como errores de captura, devoluciones o productos desperdiciados.

### 7.2 Experiencia del usuario

Durante la entrevista, el encargado explicó que ya conoce y utiliza WhatsApp. Por esta razón, cualquier propuesta debe evaluar si realmente es conveniente reemplazar esa herramienta o si resulta mejor complementarla con un registro simple. La prioridad debe ser que el personal pueda utilizar el sistema mientras atiende a los clientes, sin agregar pasos innecesarios.

### 7.3 Control de calidad

Antes de considerar una implementación, conviene definir pruebas para comprobar que cada venta se registre una sola vez, que el inventario no muestre cantidades incorrectas, que los pedidos conserven su orden y que los reportes correspondan a las operaciones realizadas. Estos controles deben formar parte de la planificación del sistema.

### 7.4 Viabilidad

Entre las alternativas comparadas, **la implementación por etapas es una opción razonable para presentar a discusión**, porque concentra el esfuerzo inicial en funciones relacionadas con el manejo actual de inventario y ventas. Esto no constituye una decisión final de la junta: la selección definitiva debe reflejar los argumentos y acuerdos reales de los participantes.

## 8. Negociación y toma de decisiones

La negociación técnica debe considerar que no todas las prioridades son iguales. Desde la perspectiva del negocio, interesa disponer de una solución útil, económica y sencilla. Desde el área técnica, es necesario considerar el tiempo disponible, la confiabilidad de los datos y el mantenimiento. Desde el control de calidad, es importante evitar que una implementación apresurada genere errores en los registros.

Los principales aspectos a negociar son:

1. **Alcance frente a tiempo:** desarrollar todas las funciones desde el inicio o seleccionar un conjunto reducido para una primera etapa.
2. **Nuevas herramientas frente a facilidad de uso:** introducir una página o aplicación adicional o conservar WhatsApp como apoyo en algunos procesos.
3. **Rapidez frente a calidad:** acelerar la entrega sin omitir las validaciones esenciales del inventario, ventas y pedidos.
4. **Necesidades actuales frente a crecimiento futuro:** priorizar funciones de uso diario y planificar para después las de eventos, promociones y entregas.

El resultado concreto de la negociación y los acuerdos aprobados por el equipo se documentan por separado en **Acuerdos y trade-offs**, una vez confirmados con lo ocurrido en la grabación.

## 9. Material de apoyo

Para analizar las necesidades y comparar las soluciones se prepararon los siguientes documentos:

- [Resumen de la entrevista](/documentos/01_resumen_entrevista.pdf)
- [Propuestas de solución](/documentos/02_propuestas_solucion.pdf)
- [Comparación de alternativas](/documentos/03_comparacion_alternativas.pdf)
- [Acta de reunión](/documentos/04_Acta.pdf)

Estos archivos corresponden al material preparado para la simulación. El acta definitiva debe reflejar las decisiones reales y estar debidamente completada.

## 10. Grabación de la junta directiva

La grabación presencial debe incorporarse aquí mediante el reproductor de YouTube, para que se pueda visualizar directamente desde Docusaurus. **El video todavía no fue proporcionado para este documento**, por lo que no se incluye una dirección ficticia.

<iframe width="1335" height="751" src="https://www.youtube.com/embed/mAKfh9VqZAI" title="12 de octubre de 2026" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

## 11. Conclusión

El análisis de Manos Sobre la Pizza permitió identificar oportunidades de mejora relacionadas con el inventario, el registro de ventas, la atención de pedidos, los servicios de catering y la promoción del negocio. La entrevista también dejó claro que el encargado valora la sencillez y que algunos de sus procedimientos actuales ya responden adecuadamente a sus necesidades.

Por ello, una solución tecnológica no debería buscar cambiar todo el funcionamiento del negocio, sino facilitar tareas específicas y ofrecer beneficios concretos. La comparación de alternativas permite evaluar el alcance, el tiempo, los costos y la calidad antes de tomar una decisión. La conclusión definitiva de la junta, así como la solución elegida y los acuerdos alcanzados, deberá coincidir con la discusión que efectivamente quedó registrada en el video.
