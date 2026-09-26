Tarea 8 Idempotencia



Compruébalo en Postman: ejecuta varias veces la misma petición PUT y luego varias

veces la misma POST. ¿Qué diferencia observas en el resultado?



Un método es idempotente si realizar la misma petición varias veces produce exactamente el mismo efecto en el servidor



Idempotentes: GET, PUT, DELETE

No idempotentes: POST



¿Qué diferencia observas en el resultado?



La diferencia se observa en como cambian los datos del servidor las respuestas http por ejemplo el put crea el recurso por primera vez luego se sobrescribe la informacion y el post crea un nuevo recurso duplicado



Tarea 9 Las cabeceras de la respuesta

