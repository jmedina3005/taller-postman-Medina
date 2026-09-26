\# Hallazgos de Experimentación



\## Tabla de Peticiones y Resultados



| # | Petición | Código esperado | Código obtenido | ¿Coincide? |

| :--- | :--- | :--- | :--- | :--- |

| 1 | `GET /posts/1` | 200 | 200 | Sí |

| 2 | `GET /posts` | 200 | 200 | Sí |

| 3 | `GET /posts/9999` | 404 | 404 | Sí |

| 4 | `POST /posts` | 201 | 201 | Sí |

| 5 | `PUT /posts/1` | 200 | 200 | Sí |

| 6 | `PATCH /posts/1` | 200 | 200 | Sí |

| 7 | `DELETE /posts/1` | 200 | 200 | Sí |



la peticion 1 trae el codigo 200 ok trae un solo elemento y trae un userid, id, tittle, body.

la peticion 2 trae el codigo 200 ok trae 100 elementos y trae cada uno un userid, id, tittle, body.



Los criterios de aceptacion cambian segun el alcance de la peticion: cuando pides un recurso individual, te enfocas en el detalle y la integridad de un solo elemento; cuando pides una colección, te enfocas en el manejo del volumen de datos, el orden y el rendimiento.



¿Qué pasaría si hubiera devuelto 200 con un cuerpo vacío?



Sí, sería un defecto, porque se esperaba un código 404 para indicar que el recurso no existe, pero la API estaría devolviendo 200, indicando que la petición fue procesada correctamente. El resultado obtenido sería diferente al resultado esperado, por lo que el caso de prueba fallaría.



Responde: ¿qué observaste? ¿Por qué crees que ocurre eso? ¿Cómo comprobarías, en una

API real, que el recurso se creó de verdad?



¿Qué observé?



Observé que las cinco peticiones POST devolvieron el código 201 Created y que en todas las respuestas se devolvió el ID 101.



¿Por qué creo que ocurre eso?



El POST simula la creación del recurso y devuelve una respuesta con un ID, pero el recurso no se almacena como ocurriría normalmente en una base de datos real.



¿Cómo comprobaría en una API real que el recurso se creó de verdad?



En una API real comprobaría el resultado haciendo posteriormente una petición GET utilizando el ID que devolvió el POST



Responde: ¿qué diferencia encontraste entre ambas respuestas? ¿Cuál usarías para

corregir un error de escritura en un solo campo, y por qué?



Diferencias 



PUT se utiliza para actualizar o reemplazar un recurso, mientras que PATCH se utiliza para modificar solamente una parte del recurso



¿Cuál usaría para corregir un error de escritura en un solo campo?



Usaría PATCH, porque solamente necesito modificar el campo title y no modificar el resto de los datos del recurso


Tarea 10: Encuentra el límite

Después responde: ¿cómo se llama ese tipo de caso de prueba? ¿Por qué se dice que los
defectos se concentran ahí?

ID más alto con respuesta 200: 100
Primer ID con respuesta 404: 101

¿Cómo se llama ese tipo de caso de prueba?
Análisis de Valores Límite

¿Por qué se dice que los defectos se concentran ahí?
Se dice que los defectos se concentran en los límites porque los desarrolladores suelen cometer errores frecuentes al implementar las condiciones lógicas de los rangos (por ejemplo, confundir operadores como estrictamente menor < con menor o igual <=).

Tarea 11: Explora otros recursos y rutas anidadas

JSONPlaceholder tiene más recursos además de /posts. Descúbrelos y prueba al
menos dos que no hayamos usado.

Recursos Adicionales Explorados (/todos y /users)

/todos: Al consultar este recurso la API devuelve un arreglo de tareas pendientes en formato JSON
/users: Al consultar este endpoint la respuesta entrega los perfiles de los usuarios del sistema

Rutas Anidadas (/posts/1/comments)

Al realizar la petición GET a el servidor responde con un código 200 OK y devuelve únicamente los comentarios vinculados de forma directa al post con ID

Deducción de la estructura de la ruta anidada:

¿Cómo funciona? 

La URL funciona como una jerarquía de carpetas. Primero indicamos el elemento principal (/posts/1) y luego el subelemento que queremos ver de ese elemento (/comments).



