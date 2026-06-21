#  Historias de Usuario - Proyecto: ReporteCiudadano

Este documento contiene las historias de usuario principales para el desarrollo del Producto Mínimo Viable (MVP) del sistema de Gestión de Fallas Urbanas.

---

###  HU-01: Reporte de Fallas con Evidencia y Ubicación
* **Como:** Ciudadano preocupado por mi comunidad,
* **Quiero:** Reportar una falla urbana subiendo una foto y mi ubicación exacta,
* **Para:** Que las autoridades municipales conozcan el problema preciso y puedan atenderlo.

####  Criterios de Aceptación:
* **Dado que** estoy en el formulario de reporte, 
* **Cuando** selecciono un tipo de falla, adjunto una foto y permito el acceso al GPS, 
* **Entonces** el sistema debe capturar las coordenadas automáticamente y habilitar el botón de enviar.

---

###  HU-02: Historial y Seguimiento de Reportes (Dashboard Ciudadano)
* **Como:** Vecino que realizó una denuncia,
* **Quiero:** Ver una lista con el historial y el estado en tiempo real de mis reportes,
* **Para:** Saber si las autoridades están trabajando en resolverlo o si ya fue solucionado.

#### 📋 Criterios de Aceptación:
* **Dado que** inicié sesión en la app, 
* **Cuando** entro al Dashboard, 
* **Entonces** debo ver mis reportes ordenados cronológicamente con etiquetas de color según su estado (*Reportado, En Proceso, Solucionado*).

---

###  HU-03: Actualización de Estatus de Fallas
* **Como:** Administrador o personal del gobierno municipal,
* **Quiero:** Cambiar el estado de un reporte ciudadano a través de un panel básico,
* **Para:** Notificar a la comunidad sobre el avance de la reparación de la falla.

####  Criterios de Aceptación:
* **Dado que** estoy en el panel de administración, 
* **Cuando** selecciono un reporte "Pendiente" y cambio su estatus a "En Proceso", 
* **Entonces** el cambio debe reflejarse inmediatamente en el Dashboard del ciudadano correspondiente.

---

###  HU-04: Filtro de Reportes por Estado
* **Como:** Usuario del sistema (ciudadano o administrador),
* **Quiero:** Filtrar los reportes en el mapa o lista según su estado actual,
* **Para:** Enfocarme únicamente en las fallas que siguen pendientes de resolver.

####  Criterios de Aceptación:
* **Dado que** estoy visualizando el listado general, 
* **Cuando** selecciono el filtro "Solucionado", 
* **Entonces** la pantalla debe ocultar automáticamente todos los reportes que estén en estado *Reportado* o *En Proceso*.
