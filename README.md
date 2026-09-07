# ATS de Selección con IA

Sistema automatizado de selección de personal que integra inteligencia artificial, gobernanza de datos y validación humana.

**Proyecto final – IA Automation | Coderhouse**

**Autora: Gabriela Fasanella**

## Descripción del proyecto

El proyecto automatiza el ingreso, registro y análisis inicial de postulaciones para una vacante.

El sistema recibe datos desde Google Forms y Google Sheets, registra la información en Airtable, procesa y seudonimiza el CV, compara el perfil con los requisitos de la vacante mediante IA y solicita una decisión humana antes de enviar cualquier comunicación a la persona candidata.

El objetivo es mejorar la eficiencia del proceso de selección sin delegar la decisión final en la inteligencia artificial.

## Flujo general

1. Recepción de la postulación y validación del consentimiento.
2. Detección de candidatos duplicados.
3. Creación o actualización de la identidad en Airtable.
4. Registro de la postulación.
5. Extracción del texto del CV.
6. Seudonimización y control de datos sensibles.
7. Análisis de compatibilidad mediante OpenAI.
8. Validación humana mediante un proceso Human-in-the-loop.
9. Envío de invitación a screening o comunicación de no avance.
10. Registro de resultados, ejecuciones y errores.

## Tecnologías utilizadas

* **n8n:** orquestación de los workflows.
* **Airtable:** base de datos, memoria operativa y dashboard.
* **OpenAI:** seudonimización y análisis estructurado de compatibilidad.
* **Google Forms y Google Sheets:** recepción de postulaciones.
* **Google Drive:** almacenamiento controlado de CV.
* **Gmail:** comunicaciones y trazabilidad mediante identificadores de hilo.
* **Telegram:** intervención humana para aprobar o rechazar el avance.

## Componentes principales

* Workflow de ingreso y registro de postulaciones.
* Workflow centralizado de gestión de errores.
* Workflow de prueba controlada del camino de error.
* Base relacional de candidatos, postulaciones, vacantes y ejecuciones.
* Dashboard de control con indicadores operativos.
* Validación humana previa a toda comunicación.
* Política de conservación y minimización de datos.

## Documentación

* [Manual operativo y documentación completa](./Manual_Entrega_Final_ATS_IA.pdf)
* [Diagrama de arquitectura](./Arquitectura_ATS_IA_Final.pdf)


## Workflows sanitizados

Los archivos fueron exportados sin credenciales, API keys, webhooks activos ni información personal real.

* [Ingreso y registro de postulaciones](./ATS%20%E2%80%93%2001%20Ingreso%20y%20registro%20de%20postulaciones_GitHub.json)
* [Registro centralizado de errores](./ATS%20%E2%80%93%20Registro%20centralizado%20de%20errores%281%29_GitHub.json)
* [Prueba controlada de errores](./ATS%20%E2%80%93%20Prueba%20controlada%20de%20errores_GitHub.json)

## Enlaces públicos

* [Dashboard de control – KPI y tasa de errores](https://airtable.com/appDLuVv0eYArcrmJ/shreOQxbb2Kk7Ro8W/tblevK0wyQxzUrESe)
* [Base de postulaciones seudonimizadas – modo lectura](https://airtable.com/appDLuVv0eYArcrmJ/shrOUdDQFp7fRtsb4/tblt5XMppJZPx3iQI)
- [Video demostrativo del sistema](https://drive.google.com/file/d/1T7b_34qQH5bZFdGopDNWuvPDmzxPuMIG/view?usp=sharing)

## Resultados de las pruebas

El sistema fue probado mediante recorridos exitosos y caminos de error controlados.

* 16 postulaciones registradas.
* 8 postulaciones procesadas por IA.
* 4 aprobadas para screening.
* 3 no aprobadas.
* 1 pendiente de decisión humana.
* 6 comunicaciones enviadas.
* 15 ejecuciones registradas.
* 11 errores históricos utilizados durante el desarrollo y las pruebas.
* 4 ejecuciones exitosas registradas en el workflow centralizado.

La tasa histórica de error refleja las pruebas realizadas durante la construcción y estabilización del sistema, y no una tasa esperada para su operación productiva.

## Seguridad, privacidad y gobernanza

* Consentimiento informado al inicio del proceso.
* Separación entre identidad y postulaciones.
* Seudonimización previa al análisis con IA.
* Minimización de datos enviados al modelo.
* Validación humana antes de contactar al candidato.
* Registro centralizado de ejecuciones y errores.
* Conservación de datos durante seis meses.
* Vistas públicas sin nombres, correos, teléfonos, CV ni datos identificatorios.
* Workflows publicados sin credenciales ni información sensible.

## Alcance

Este proyecto constituye un prototipo funcional y demostrativo. Antes de utilizarlo en un entorno productivo deben revisarse las credenciales, permisos, políticas de conservación, costos, límites de las APIs y requisitos legales aplicables.
