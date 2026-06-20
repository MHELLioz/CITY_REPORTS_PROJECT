🌐 Documentación de Arquitectura de API (Estándar Swagger)
A continuación se definen las interacciones técnicas para las dos pantallas clave del MVP:

1. Pantalla: Formulario de Reporte de Falla (HU-01)
Método HTTP: POST
Endpoint /api/v1/reportes
Descripción: Se utiliza el método POST porque la pantalla tiene la función de crear un nuevo recurso en el servidor (un reporte de bache, luminaria, etc.) que no existía previamente. El cuerpo de la petición (Body) envía los datos capturados en el archivo pantalla_reporte.json.
Código de respuesta esperado: 201 Created (Éxito al crear el reporte).
2. Pantalla: Dashboard de Seguimiento Ciudadano (HU-02 / HU-04)
Método HTTP: GET
Endpoint: /api/v1/usuarios/{id_usuario}/reportes
Descripción: Se utiliza el método GET porque la pantalla tiene la función exclusiva de consultar y leer información existente en la base de datos para mostrar el listado histórico de denuncias de un usuario. Permite parámetros de consulta (Query Parameters) como ?estado=En+Proceso para ejecutar los filtros de la HU-04.
Código de respuesta esperado: 200 OK (Éxito al retornar los datos).
