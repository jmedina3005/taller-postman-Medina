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

