# Informe Final – Capacitación sobre APIs REST

## Portada

**Universidad de San Carlos de Guatemala**  
**Facultad de Ingeniería**  
**Ingeniería en Ciencias y Sistemas**  
**Curso:** Comunicación Asertiva  
**Proyecto 1:** Capacitación sobre APIs REST  

### Integrantes Grupo 1

| No. | Nombre | Carnet | Usuario de GitHub |
|---:|---|---|---|
| 1 | Denis Abad | 202504781 | sebasjsx |
| 2 | Esther Garcia | 202500170 |  |
| 3 | Pablo Colop | 202500752 | Pablocob |
| 4 | Walter Martinez | 202500147 | walm1 |
| 5 | Aura Marina |202500244  | 202500244 |
| 6 | Chung Kim | 202501625 | 3629846541801-ops |

**Fecha de entrega:** 23/09/2026

---

## 1. Introducción

La capacitación tuvo como propósito explicar de forma clara y práctica qué son las APIs REST, cómo funcionan y por qué son importantes en el desarrollo de aplicaciones modernas. Este tipo de API permite la comunicación entre diferentes sistemas, facilitando el intercambio de información entre el frontend, el backend y la base de datos mediante peticiones y respuestas.

La importancia de las APIs REST radica en que son ampliamente utilizadas para conectar aplicaciones y servicios, permitiendo realizar operaciones como consultar, crear, actualizar o eliminar información mediante métodos HTTP.

El objetivo general del proyecto fue que los participantes comprendieran el funcionamiento básico de una API REST y pudieran identificar sus principales componentes y métodos a través de explicaciones, ejemplos y una demostración práctica.

---

## 2. Objetivos

### 2.1 Objetivo general

Explicar de manera clara y práctica el funcionamiento de las APIs REST, sus principales componentes y métodos HTTP, mediante ejemplos de situaciones cotidianas y una demostración práctica, con el fin de facilitar la comprensión de su importancia en el intercambio de información entre diferentes aplicaciones y sistemas.

### 2.2 Objetivos específicos

-Identificar los principales componentes de una API REST, incluyendo clientes, servidores, endpoints, métodos HTTP, URL, parámetros, headers y body.

-Explicar cómo se realiza el intercambio de información mediante APIs REST, utilizando ejemplos cotidianos y formatos como JSON para facilitar la comprensión de los conceptos técnicos.

-Demostrar mediante ejemplos prácticos el funcionamiento de las peticiones y respuestas HTTP, incluyendo los métodos GET, POST, PUT, PATCH y DELETE, así como los principales códigos de respuesta HTTP.

---

## 3. Descripción general del tema y subtemas elegidos

### 3.1 Tema principal: APIs REST

Explicacion general de que son las APIs REST, para que sirven y por qué se eligió este tema.

### 3.2 Subtemas desarrollados

#### Introducción a las API REST
- Definición de API.
- Significado de REST.
- Propósito.
- Ejemplos cotidianos.

#### Arquitectura y funcionamiento
* **Cliente:** Es el quien que inicia la comunicación. En términos resumidos, es cualquier dispositivo, navegador web o aplicación móvil que necesita acceder a una información o servicio. El cliente es el responsable de generar y enviar la solicitud inicial.

* **Servidor:** Equipo remoto que recibe la solicitud, procesa la lógica del sistema y entrega el resultado.

- **API (Interfaz de Programación de Aplicaciones):** Actúa como el puente estandarizado entre el cliente y el servidor. Define las reglas, protocolos y formatos de mensajes que ambos deben usar para entenderse mutuamente.

- **Interfaz / Frontend:** Es la capa con la que el usuario interactúa visualmente en el cliente.

- **Backend:** Es toda la infraestructura tecnológica que opera "detrás de escena" y que el usuario final no ve. El backend engloba al servidor, la lógica de negocio de la aplicación, las medidas de seguridad y la conexión con el almacenamiento de datos.

- **Base de datos:** Sistema de almacenamiento estructurado donde se guardan datos como usuarios, fotos y registros.

- **Endpoints (Puntos finales):** Son las rutas, URLs o direcciones web específicas que la API expone para que el cliente acceda a recursos concretos. Cada punto final representa una función o conjunto de datos particular.

- **Peticiones y respuestas:** 

  * **Petición (Request):** Es el mensaje estructurado que el cliente envía al servidor, indicando qué acción desea realizar y a qué punto final se dirige.

  * **Respuesta (Response):** Es el paquete de datos que el servidor devuelve al cliente; incluye la información solicitada  y un mensaje de estado.

#### Métodos HTTP (encargado: Walter Martínez)
- **GET:** Solicita la lectura o recuperación de datos de un recurso en el servidor sin modificarlo.
- **POST:** Envía datos al servidor para crear un recurso nuevo.
- **PUT:** Actualiza o reemplaza por completo un recurso existente en el servidor con los datos enviados.
- **PATCH:** Aplica modificaciones parciales a un recurso existente, actualizando solo los campos especificados.
- **DELETE:** Elimina un recurso específico del servidor.
  
#### Intercambio de información
El intercambio de información en una API REST se realiza mediante solicitudes y respuestas entre el cliente y el servidor. Para explicarlo de forma sencilla, se utilizó como ejemplo la solicitud de un producto.

-URL: indica la dirección del recurso solicitado.

-Parámetros: especifican información adicional de la solicitud, como el producto o la cantidad.

-Headers: contienen información adicional sobre la petición, como el tipo de contenido.

-Body: contiene los datos que se envían al servidor.

-JSON: formato utilizado para organizar y transmitir los datos.

-Códigos HTTP: indican el resultado de la solicitud, por ejemplo, 200 para una solicitud exitosa, 404 cuando no se encuentra el recurso y 500 cuando ocurre un error en el servidor.

De esta manera, una API REST permite que diferentes aplicaciones intercambien información de forma estructurada mediante peticiones y respuestas.

#### Seguridad en API REST (encargado: Chung Kim)
Para garantizar que los datos estén protegidos y evitar accesos no deseados, una API debe implementar las siguientes medidas clave:

- HTTPS: Es el protocolo que cifra la comunicación entre el cliente y el servidor, asegurando que nadie pueda interceptar o leer los datos en tránsito.
  
- Autenticación: Es el proceso de verificar la identidad del usuario o sistema que intenta acceder a la API (saber "quién eres", usualmente con usuario/contraseña).
  
- Autorización: Es el paso posterior a la autenticación que verifica qué acciones o recursos tienes permitido utilizar (saber "qué puedes hacer").
  
- Tokens: Son cadenas de texto seguras (como los JWT) que se le dan al usuario una vez autenticado. Se envían en cada petición para comprobar su identidad sin tener que pedir la contraseña cada vez.
  
- Roles: Son grupos de permisos predefinidos (ej. Administrador, Editor, Lector) que se asignan a los usuarios para facilitar el control de autorización.
  
- Validación: Es la revisión obligatoria de toda la información que el cliente envía a la API para asegurar que tenga el formato correcto y no contenga código malicioso.

#### Ejercicio práctico (encargado: Denis Abad)
Para ejemplificar de mejor manera la teoría explicada, se utilizó una aplicación de gestión de tareas. El backend fue desarrollado con Node.js y Express, el frontend con React y la base de datos con MongoDB. Su principal objetivo fue demostrar de forma práctica el funcionamiento de los métodos HTTP dentro de una aplicación real.

---

## 4. Autoevaluación de la conferencia mediante FODA

## 4.1 FODA por integrante

### Denis Abad

#### Fortalezas
- Escucho y tomo en cuenta las opiniones de los demás.
- Estoy dispuesto a asumir responsabilidades y apoyar al grupo.
- Me preparé para explicar el ejemplo práctico del gestor de tareas.

#### Oportunidades
- Mejorar mi seguridad al hablar frente a muchas personas.
- Fortalecer mi liderazgo y mi forma de explicar temas técnicos.
- Desarrollar una mejor interacción con el público.

#### Debilidades
- A veces puedo sentirme tímido o nervioso al exponer.
- Me cuesta mantener el contacto visual con la audiencia.
- En ocasiones se me dificulta mantener una comunicación constante con el público.

#### Amenazas
- Los nervios pueden afectar mi fluidez al explicar.
-  La presión o el estrés pueden afectar mi confianza al momento de tomar decisiones.

### Marina Mejia 

#### Fortalezas
* Tengo facilidad para expresarme y comunicar ideas de manera clara frente a otras personas.
* Tengo buena capacidad de retención y puedo aprender y recordar información en poco tiempo.
* Cuando conozco y comprendo el tema, puedo transmitir la información con seguridad y entusiasmo.

#### Oportunidades
* Mejorar mi manejo de los nervios al hablar frente a un grupo de personas.
* Fortalecer mi contacto visual y mi interacción con el público durante futuras exposiciones.
* Desarrollar estrategias para mantener la concentración aunque ocurran imprevistos durante una actividad.

#### Debilidades
* Tiendo a estresarme cuando las cosas no salen de acuerdo con lo planificado.
* El contacto visual directo con muchas personas puede aumentar mis nervios y dificultar que recuerde lo que debo explicar.
* En ocasiones puedo ser demasiado precipitada al realizar actividades o tomar decisiones.

#### Amenazas
* Los nervios durante una exposición pueden afectar mi fluidez y la forma de transmitir la información.
* Los errores de otros integrantes pueden afectar mi concentración si me enfoco demasiado en corregirlos.
* La presión de cumplir con el tiempo establecido puede hacer que explique la información de manera demasiado rápida.

### Chung Kim

#### Fortalezas
- Logré un buen dominio de mi tema sobre la seguridad en las APIs.
- Interactué con el público realizando preguntas para asegurarme de que realmente estaban comprendiendo la explicación.

#### Oportunidades
- Aprender a controlar el nerviosismo al momento de exponer frente a una audiencia.
- Practicar para hablar de forma más lenta, clara y pausada.
- Desarrollar técnicas para asegurar y mantener la atención del público durante toda la presentación.

#### Debilidades
- Hablé muy rápido durante la charla.
- Me demoré un poco en terminar la parte del proyecto que me correspondía.
- Faltó proactividad de mi parte para tomar notas cuando el grupo se estaba poniendo de acuerdo.

#### Amenazas
- La dificultad para organizar y asimilar mi propia información puede afectar los tiempos de entrega del equipo.
- El estrés y la presión de hablar frente al público pueden provocar bloqueos o afectar mi claridad al exponer.

### Pablo Colop

#### Fortalezas
- Tengo facilidad al adaptar información compleja y explicarla de forma sencilla.
- Cuando presento un tema trato de no usar un lenguaje muy tecnico.
  
#### Oportunidades
- Mejorar mi confianza y fluidez al hablar frente a un público numeroso.
- Desarrollar una mejor interacción y manejo de la audiencia durante la exposición.
- Fortalecer mis habilidades de comunicación asertiva para proyectos futuros.
  
#### Debilidades
- Casi siempre al exponer me pongo nervioso.
- Suelo hablar mas rapido cuadno me dan nervios.
- Me cuesta mantener un contacto visual constante con todo el auditorio
  
#### Amenazas
- Que los nervios del momento afecten mi fluidez al explicar mi parte del tema.
- Que distracciones externas en el salón me hagan perder el hilo de mi discurso.

### Walter Martínez

#### Fortalezas
- Cuento con conocimientos previos sobre el tema, lo cual facilita la comprensión.
- Facilidad para trabajar y desarrollar proyectos en equipo.
- Tengo una buena capacidad de retención y comprensión, lo que me permite exponer conceptos tecnológicos con cierta facilidad.

#### Oportunidades
- Desarrollar técnicas para controlar mis nervios y proyectar más seguridad al exponer ante una audiencia.
- Fortalecer mis habilidades para comunicar conceptos avanzados de forma sencilla.
- Trabajar con técnicas para mantener la atención de la audiencia y mejorar la interacción.

#### Debilidades
- Nerviosismo al exponer frente a una audiencia.
- Dificultad para mantener el contacto visual con la audiencia.

#### Amenazas
- Interrupciones externas u otros factores en el aula que distraigan al grupo.
- Los nervios afectan mi confianza y fluidez al hablar.
---

### 4.2 FODA grupal

#### Fortalezas

#### Oportunidades

#### Debilidades

#### Amenazas

---

## 5. Conclusiones

- Las APIs REST son clave en la programación actual, ya que permiten que las distintas partes de una aplicación (frontend, backend y bases de datos) se comuniquen entre sí de una forma mucho más fácil y ordenada.
- La seguridad en una API es obligatoria. Proteger las conexiones, controlar quién entra al sistema usando tokens y revisar que la información enviada sea correcta, son pasos necesarios para mantener cualquier proyecto a salvo de ataques.
- Combinar la teoría con un ejemplo práctico, como lo hicimos con el gestor de tareas, es una excelente manera de ayudar a los estudiantes a visualizar y entender cómo funcionan realmente las peticiones y respuestas en una aplicación real.

---

## 6. Anexos

### 6.1 Material utilizado


- **Link de la presentación usada:** https://canva.link/xm84lbiabnp60ig
- **Proyecto usado en la capacitación:** https://github.com/sebasjsx/gestorDeTareas
- **Kahoot usado en la capacitación:** https://create.kahoot.it/share/apis-rest-y-tokens-ca/f601cc54-298a-4535-8ea9-3b5aa76f4522

---

### 6.2 Tabla de porcentaje de participación
| No. | Nombre | Carnet | Tareas realizadas | Participación (%) |
|:---:|:---|:---|:---|:---:|
| 1 | Denis Abad | 202504781 | Reunión de planificación, desarrollo de informes, exposición de presentación práctica (10 min). | 17.0% |
| 2 | Esther Garcia | 202500170 | Reunión de planificación, desarrollo de informes, preguntas Kahoot, exposición: Introducción (6 min). | 16.6% |
| 3 | Pablo Colop | 202500752 | Reunión de planificación, desarrollo de informes, preguntas Kahoot, exposición: Arquitectura (6 min). | 16.6% |
| 4 | Walter Martinez | 202500147 | Reunión de planificación, desarrollo de informes, preguntas Kahoot, exposición: Métodos HTTP (6 min). | 16.6% |
| 5 | Aura Marina | 202500244 | Reunión de planificación, desarrollo de informes, preguntas Kahoot, exposición: Intercambio de información (6 min). | 16.6% |
| 6 | Chung Kim | 202501625 | Reunión de planificación, desarrollo de informes, preguntas Kahoot, exposición: Seguridad en APIs REST (6 min). | 16.6% |
| | **Total** | | | **100%** |

---

## 7. Grabaciones

- **Link Video de la capacitación:** https://youtu.be/j8YB0FtYnBY?si=fOUoM-BSaACinW7o
- **Link Video de la planificacion:** https://youtu.be/uQWEjpbOrPs?si=kJoh5T_4E3hVt7oe
