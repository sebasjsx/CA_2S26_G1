# DOCUMENTO POST-MORTEM

## Sistema de Registro de Ventas y Control de Inventario

**Negocio:** Manos Sobre la Pizza  
**Fecha del incidente:** 12 de octubre de 2026  
**Horario:** 1:00 p. m. a 3:00 p. m.  
**Tipo de incidente:** Error de actualización del inventario  
**Gravedad:** Alta

*Nota: El incidente presentado es una simulación académica basada en la solución propuesta para el negocio. No corresponde a una falla real confirmada.*

## 1. Resumen del incidente

El 12 de octubre de 2026, aproximadamente a la 1:25 p. m., durante las pruebas de implementación del sistema de registro de ventas y control de inventario para Manos Sobre la Pizza, se identificó un error que impedía actualizar correctamente las existencias de determinados productos.

El sistema permitía registrar las ventas realizadas en efectivo, pero cuando se procesaban varias ventas consecutivas, algunas cantidades vendidas no se descontaban correctamente del inventario.

Como consecuencia, el sistema mostraba productos disponibles que ya habían sido vendidos, generando diferencias entre las cantidades registradas digitalmente y las existencias físicas.

El problema afectó principalmente tres áreas: el registro de ventas, el control de inventario y la consulta de disponibilidad de productos.

Al detectar la inconsistencia, el equipo decidió suspender temporalmente la actualización automática del inventario, revisar el código y realizar pruebas adicionales.

El incidente fue solucionado dentro del horario establecido para la simulación, finalizando aproximadamente a las 3:00 p. m.

## 2. Línea de tiempo (Timeline)

| Hora       | Descripción del acontecimiento                                                               |
| ---------- | -------------------------------------------------------------------------------------------- |
| 1:00 p. m. | El equipo inicia las pruebas del sistema de ventas e inventario.                             |
| 1:12 p. m. | Se registran las primeras ventas de prueba sin presentar inconvenientes.                     |
| 1:25 p. m. | Se identifica una diferencia entre el inventario digital y los productos vendidos.           |
| 1:32 p. m. | El encargado de QA confirma que algunas ventas no descuentan correctamente las existencias.  |
| 1:40 p. m. | El Tech Lead solicita detener temporalmente las actualizaciones automáticas.                 |
| 1:48 p. m. | El desarrollador reproduce el error al registrar dos ventas consecutivas del mismo producto. |
| 2:05 p. m. | Se identifica una falla en el manejo de actualizaciones simultáneas de inventario.           |
| 2:20 p. m. | Se aplica una corrección para evitar que una actualización sobrescriba a otra.               |
| 2:35 p. m. | QA realiza nuevas pruebas y comprueba que las existencias se descuentan correctamente.       |
| 2:48 p. m. | Se verifican los registros de ventas y se corrigen las cantidades inconsistentes.            |
| 3:00 p. m. | Se finaliza la revisión y se declara solucionado el incidente simulado.                      |

## 3. Impacto

El incidente afectó la confiabilidad de la información mostrada por el sistema y la capacidad del personal para consultar correctamente los productos disponibles.

**Usuarios afectados**

El encargado del negocio, responsable de registrar las ventas y consultar las existencias, tuvo que recurrir a un conteo manual para verificar las cantidades reales.

El personal encargado de preparar y entregar los productos también se vio afectado, debido a que no podía confiar completamente en la disponibilidad que mostraba el sistema.

**Efectos directos**

- Diferencias entre el inventario digital y las existencias físicas.

- Interrupción temporal del proceso de actualización automática.

- Necesidad de revisar manualmente las cantidades.

- Retrasos durante la validación de los registros de ventas.

- Trabajo adicional para identificar y corregir las inconsistencias.

**Efectos indirectos**

El problema podría haber provocado que el personal ofreciera productos agotados, ocasionando inconvenientes en la atención de los clientes.

También representaba un riesgo para la toma de decisiones relacionadas con la reposición de productos y la planificación de suministros.

**Nivel de gravedad**

El incidente se clasificó como de gravedad alta, debido a que afectó una de las funciones principales de la solución propuesta.

Sin embargo, al tratarse de una simulación en un entorno de pruebas, no se registraron pérdidas económicas reales ni afectaciones confirmadas a clientes.

## 4. Causa raíz

Para identificar el origen del incidente, el equipo utilizó la técnica de los cinco porqués.

**Problema principal:** el inventario mostraba cantidades incorrectas después de registrar varias ventas consecutivas.

**Primer porqué: ¿Por qué el inventario mostraba cantidades incorrectas?**

Porque algunas ventas registradas no descontaban correctamente los productos del inventario.

**Segundo porqué: ¿Por qué no se descontaban correctamente los productos?**

Porque dos operaciones de venta realizadas con poca diferencia de tiempo podían utilizar la misma cantidad inicial del inventario.

**Tercer porqué: ¿Por qué podían utilizar la misma cantidad inicial?**

Porque la actualización del inventario no se realizaba mediante una operación que garantizara que cada descuento se completara correctamente antes de procesar otro.

**Cuarto porqué: ¿Por qué no se había detectado este error antes?**

Porque las pruebas iniciales se realizaron principalmente con ventas individuales y no contemplaron suficientes escenarios de ventas consecutivas o simultáneas.

**Quinto porqué: ¿Por qué no se realizaron esas pruebas?**

Porque durante la planificación se priorizó comprobar el funcionamiento básico del sistema, sin establecer criterios específicos para validar la consistencia del inventario cuando se procesaran múltiples operaciones.

### Causa raíz identificada

La causa principal fue la falta de un mecanismo seguro para actualizar las existencias durante operaciones consecutivas o simultáneas.

A esto se sumó una planificación de pruebas insuficiente, que no contempló desde el inicio escenarios de mayor demanda.

El equipo concluyó que la falla no se relacionaba con el procedimiento de inventario utilizado por el negocio, sino con una deficiencia técnica en el desarrollo y la validación del software.

## 5. Acciones tomadas para solucionarlo

Al identificar el problema, los integrantes del equipo coordinaron las siguientes acciones:

**Scrum Master**

Organizó la comunicación entre los integrantes y coordinó una revisión del incidente. También propuso detener temporalmente la actualización automática para evitar nuevas inconsistencias durante las pruebas.

**Tech Lead**

Analizó el comportamiento general del sistema y determinó que el problema estaba relacionado con la forma en que se procesaban las actualizaciones del inventario.

Supervisó la aplicación de una solución que permitiera manejar correctamente las operaciones consecutivas.

**Desarrollador**

Revisó el código encargado de registrar las ventas y descontar los productos.

Modificó la lógica de actualización para utilizar operaciones atómicas, evitando que dos ventas sobrescribieran las cantidades registradas.

**QA / Auditor**

Realizó pruebas con ventas consecutivas, verificando que cada producto vendido se descontara correctamente.

Además, comparó los resultados del sistema con un inventario de prueba para comprobar la efectividad de la corrección.

**Product Manager**

Reorganizó las prioridades del proyecto, estableciendo que la corrección del error debía completarse antes de continuar desarrollando funciones adicionales.

**Cliente / Stakeholder**

Revisó que el procedimiento corregido siguiera siendo sencillo de utilizar y que el sistema mantuviera el registro de pagos únicamente en efectivo.

### Resultado de las acciones

Después de realizar los cambios, el equipo repitió las pruebas y comprobó que las ventas se registraban y las existencias se actualizaban de forma correcta.

También se realizó una conciliación de los datos utilizados durante la simulación.

A las 3:00 p. m. se consideró solucionado el incidente, quedando pendiente aplicar las medidas preventivas necesarias para evitar futuros errores.

## 6. Acciones a futuro

Para reducir la posibilidad de que ocurra nuevamente un incidente similar, el equipo propuso implementar las siguientes acciones.

### 6.1. Mejorar la actualización del inventario

**Acción:** utilizar operaciones atómicas para garantizar que cada venta registrada actualice correctamente las existencias.

**Responsables:** Tech Lead y Desarrollador.

**Relación con la causa raíz:** evita que dos operaciones sobrescriban información al ejecutarse consecutivamente.

### 6.2. Implementar pruebas de ventas simultáneas

**Acción:** realizar pruebas con múltiples ventas del mismo producto, incluyendo operaciones consecutivas, cancelaciones y cantidades cercanas a cero.

**Responsable:** QA / Auditor.

**Relación con la causa raíz:** permite detectar errores que no aparecen durante las pruebas de ventas individuales.

### 6.3. Incorporar alertas de inconsistencias

**Acción:** generar una advertencia cuando una venta se registre, pero el descuento correspondiente no pueda completarse.

**Responsables:** Desarrollador y Tech Lead.

**Relación con la causa raíz:** facilita identificar rápidamente fallos en el proceso de actualización.

### 6.4. Mantener un historial de movimientos

**Acción:** almacenar información sobre cada movimiento del inventario, incluyendo fecha, hora, producto, cantidad y venta asociada.

**Responsable:** Desarrollador.

**Relación con la causa raíz:** permite identificar qué operación produjo una diferencia y facilita la recuperación de información.

### 6.5. Realizar verificaciones diarias

**Acción:** comparar las existencias registradas en el sistema con un conteo físico al finalizar la jornada.

**Responsables:** Encargado del negocio y personal autorizado.

**Relación con la causa raíz:** permite detectar diferencias que no hayan sido identificadas automáticamente.

### 6.6. Fortalecer la planificación de pruebas

**Acción:** definir criterios de aceptación y casos de prueba antes de implementar cada nueva funcionalidad.

**Responsables:** Product Manager, Scrum Master y QA.

**Relación con la causa raíz:** evita que el equipo considere terminada una función sin evaluar situaciones de uso intensivo y posibles errores.

### 6.7. Capacitar al personal

**Acción:** explicar al encargado cómo registrar ventas en efectivo, consultar existencias y actuar cuando el sistema detecte un error.

**Responsables:** Scrum Master y representante del negocio.

**Relación con la causa raíz:** permite mantener la continuidad de las operaciones y responder adecuadamente a futuras contingencias.

## Conclusión

El incidente simulado permitió identificar la importancia de realizar pruebas completas antes de utilizar un sistema de registro de ventas e inventario en un negocio real.

Aunque la solución propuesta buscaba simplificar las actividades de Manos Sobre la Pizza, el error demostró que una herramienta digital también puede generar dificultades cuando no garantiza la confiabilidad de sus registros.

El equipo reconoció que las pruebas iniciales fueron insuficientes y que era necesario implementar mejores mecanismos de actualización, validación y seguimiento.

Como aprendizaje principal, se estableció que la calidad del software y la facilidad de uso deben considerarse desde las primeras etapas del desarrollo.

Las acciones correctivas y preventivas propuestas permitirán mejorar la estabilidad del sistema y reducir la posibilidad de que se repitan incidentes similares durante futuras implementaciones.
