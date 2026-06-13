Actualización para Pull Request

# CITY_REPORTS_PROJECT
Gestion de fallas urbanas
.
=======
#Proyecto: ReporteCiudadano (Gestión de Fallas Urbanas)
 
 Integrantes
Christopher Armando Lepe Guardado 

 Yordi Gustavo Velazquez Ramirez 


 #Visión del MVP (Producto Mínimo Viable)
1. El Problema (Pain Point)
Actualmente, los ciudadanos no tienen un canal directo y transparente para reportar fallas en los servicios públicos (baches, luminarias fundidas, fugas de agua). El proceso actual es burocrático, requiere llamadas telefónicas largas o visitas a oficinas, y el ciudadano nunca sabe si su reporte está siendo atendido o si fue ignorado.

2. La Propuesta de Valor
Nuestra plataforma simplifica el reporte ciudadano permitiendo que cualquier persona denuncie una falla en menos de un minuto desde su celular, con evidencia fotográfica y geolocalización automática. A diferencia de los métodos tradicionales, el sistema ofrece un seguimiento visual por estados (Reportado, En Proceso, Solucionado), devolviendo la confianza al usuario.

3. El Alcance Crítico (MVP)
Para que este producto funcione en su etapa inicial, estas son las funciones indispensables:

Formulario de Reporte: Permite al usuario subir una foto, elegir el tipo de falla y capturar la ubicación.

Dashboard de Seguimiento: Una vista donde el usuario puede ver el listado de sus reportes y el estado actual de cada uno.

Panel de Administración (Básico): Interfaz para que el personal encargado cambie el estado del reporte (ej. de "Pendiente" a "Reparado").

4. Métrica de Éxito
Sabremos que el MVP es exitoso si logramos reducir el tiempo de comunicación del reporte en un 70% (comparado con el sistema de llamadas actual) y si el 100% de los reportes generados reciben al menos un cambio de estado en sus primeros 7 días.

## 🌐 Documentación de Arquitectura de API (Estándar Swagger)

A continuación se definen las interacciones técnicas para las dos pantallas clave del MVP:

### 1. Pantalla: Formulario de Reporte de Falla (HU-01)
* **Método HTTP:** `POST`
* **Endpoint** `/api/v1/reportes`
* **Descripción:** Se utiliza el método `POST` porque la pantalla tiene la función de **crear un nuevo recurso** en el servidor (un reporte de bache, luminaria, etc.) que no existía previamente. El cuerpo de la petición (Body) envía los datos capturados en el archivo `pantalla_reporte.json`.
* **Código de respuesta esperado:** `201 Created` (Éxito al crear el reporte).

### 2. Pantalla: Dashboard de Seguimiento Ciudadano (HU-02 / HU-04)
* **Método HTTP:** `GET`
* **Endpoint:** `/api/v1/usuarios/{id_usuario}/reportes`
* **Descripción:** Se utiliza el método `GET` porque la pantalla tiene la función exclusiva de **consultar y leer información** existente en la base de datos para mostrar el listado histórico de denuncias de un usuario. Permite parámetros de consulta (Query Parameters) como `?estado=En+Proceso` para ejecutar los filtros de la HU-04.
* **Código de respuesta esperado:** `200 OK` (Éxito al retornar los datos).

## Tablero del Proyecto

Tablero de seguimiento en Jira:
https://cesunbc-team2-cityreport.atlassian.net/jira/software/projects/SCRUM/summary?atlOrigin=eyJpIjoiMTNlYmEyYTZmMTY4NDYzZTg4NmY1YzMwMGE4YTJmMzciLCJwIjoiaiJ9

## Enlace a stitch(tipo Figma):
https://stitch.withgoogle.com/projects/5504479962085551709
