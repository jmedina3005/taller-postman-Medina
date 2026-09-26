# taller-postman-Medina

Estudiante: Juan David Medina Correa
Código: 1114151459
Asignatura: Ingeniería de Software II — Cotecnova

Marco Conceptual
https://www.redhat.com/es/topics/api/what-is-a-rest-api
https://www.ibm.com/mx-es/think/topics/api-endpoint
https://medium.com/@srinivasakysj/mastering-crud-operations-with-http-status-codes-e954a9473248
https://pasqualepillitteri.it/es/news/1010/codigos-http-guia-completa-familias-status-codes
https://learn.microsoft.com/es-es/troubleshoot/developer/webapps/iis/site-behavior-performance/troubleshoot-http-error-code
https://restfulapi.net/idempotent-rest-apis/

Tarea 2 Los métodos HTTP y el CRUD

| Método HTTP | Operación CRUD                   | ¿Qué hace?                                                                |
| ----------- | -------------------------------- | ------------------------------------------------------------------------- |
| GET         | Read (Leer)                      | Obtiene o consulta información de uno o varios recursos sin modificarlos. |
| POST        | Create (Crear)                   | Crea un nuevo recurso dentro de la API.                                   |
| PUT         | Update (Actualizar)              | Actualiza o reemplaza completamente un recurso existente.                 |
| PATCH       | Update (Actualizar parcialmente) | Modifica solamente una parte o uno de los campos de un recurso existente. |
| DELETE      | Delete (Eliminar)                | Elimina un recurso existente de la API.                                   |

Fase 1 Investiga Antes de Probar 

Tarea 1 ¿Qué es una API REST?

Una API REST es un estilo de arquitectura que permite que se comuniquen clientes con servidores http
Un recurso es cualquier entidad de informacion y un endpoint es la URL con la cual se accede a dicho recurso 
Un ejemplo cotidiano seria una aplicacion del clima que consulta datos a un servidor externo usando APIs

Tarea 3 Las familias de códigos de estado
1xx (Informativas): Petición recibida el proceso continua (ej 100 Continue)
2xx (exito): Peticion recibida y procesada con exito (ej 200 OK, 201 Created)
3xx (Redireccion): Se requieren acciones adicionales para completar la solicitud (ej 301 Moved Permanently)
4xx (Error del cliente): El cliente envio una peticion incorrecta o el recurso no existe (ej 404 Not Found)
5xx (Error del servidor): El servidor fallo al procesar una peticion valida (ej 500 Internal Server Error)

¿Por qué se separan los 4xx de los 5xx?
Se separan por su responsablidad los 4xx indican que la culpa es de quien hace la solicitud y los 5xx muestran que la culpa es del servidor que colapso


