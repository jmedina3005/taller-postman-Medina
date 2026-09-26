Tarea 8 Idempotencia



Compruébalo en Postman: ejecuta varias veces la misma petición PUT y luego varias

veces la misma POST. ¿Qué diferencia observas en el resultado?



Un método es idempotente si realizar la misma petición varias veces produce exactamente el mismo efecto en el servidor



Idempotentes: GET, PUT, DELETE

No idempotentes: POST



¿Qué diferencia observas en el resultado?



La diferencia se observa en como cambian los datos del servidor las respuestas http por ejemplo el put crea el recurso por primera vez luego se sobrescribe la informacion y el post crea un nuevo recurso duplicado



Tarea 9 Las cabeceras de la respuesta



Content-Type: Es vital porque le indica al cliente el formato exacto en el que viaja la información 

Host: Define el dominio o servidor de destino al que va dirigida la solicitud

User-Agent: Identifica la aplicación o herramienta tecnológica que está haciendo la petición 



Tarea 12



¿Por qué es importante ver una prueba fallar antes de confiar en ella?



Es fundamental porque nos permite comprobar que la prueba realmente está evaluando y detectando errores



Tarea 13 Escribe tus propias pruebas



Prueba de Rendimiento : Utiliza pm.expect(pm.response.responseTime).to.be.below(500) para asegurar que la API responde en un tiempo óptimo menor a medio segundo.



Prueba de Estructura de Datos : Valida con to.have.property('title') que el JSON recibido incluya obligatoriamente el campo del título.



Prueba de Tipo y Valor : Emplea to.eql(1) y to.be.a('number') para constatar que el identificador sea exactamente el esperado y cumpla con el tipo de dato correcto.









