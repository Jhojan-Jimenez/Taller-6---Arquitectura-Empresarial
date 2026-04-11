# 🗒️ Registro de Trabajo en Clase - Taller 6

## 📆 Fecha de la sesión
21 de Marzo 2026

## 👥 Integrantes presentes
- Jonatan David Vergara Suárez
- Carlos David Bello Ortiz
- Jhojan Camilo Jiménez Amaya

## 🧠 Actividades realizadas en clase

Durante la sesión se trabajó sobre el caso base **GobData**, un portal estatal de trámites ciudadanos que maneja datos personales sensibles como números de identificación, historial clínico, antecedentes y certificados digitales.

**Actividades desarrolladas:**

- Se revisó la plantilla de checklist de cumplimiento normativo y se definieron las 9 categorías de evaluación aplicables al sistema GobData.
- El equipo discutió qué normativas aplican: Ley 1581 de 2012 (Habeas Data), ISO/IEC 27001 y las circulares de la SIC.
- Se evaluaron 38 criterios de cumplimiento, clasificando cada uno como: ✅ Cumple, ⚠️ Parcial o ❌ No cumple.
- Se justificó cada criterio con evidencia concreta basada en el funcionamiento descrito del sistema.
- Se identificaron las brechas más críticas para priorizar en el informe de recomendaciones.

**Herramientas utilizadas:**
- Hoja de cálculo CSV con la plantilla del checklist.
- Documentación de referencia: texto de la Ley 1581, controles del Anexo A de ISO 27001, Circular 002 de 2015 de la SIC.

### Brechas críticas identificadas (❌)

| N° | Categoría                        | Brecha                                                                 |
|----|----------------------------------|------------------------------------------------------------------------|
| 5  | Consentimiento Informado         | No existe flujo diferenciado para menores de edad (Art. 7 Ley 1581).  |
| 16 | Seguridad / ISO 27001            | No se realizan pruebas de pentesting documentadas en los últimos 12 meses. |
| 21 | Control de Acceso                | No existe proceso de recertificación periódica de accesos.            |
| 22 | Control de Acceso                | Cuentas activas de funcionarios retirados sin deshabilitar.           |
| 25 | Retención y Eliminación          | Eliminación de datos manual y sin proceso sistemático certificado.    |
| 27 | Protección contra Fugas (DLP)    | No existe herramienta DLP implementada.                               |
| 29 | Protección contra Fugas (DLP)    | Se usan datos reales de ciudadanos en ambientes de desarrollo.        |
| 33 | Gestión de Incidentes            | Procedimiento no incluye tiempos de notificación a la SIC.            |
| 35 | Gestión de Incidentes            | No existe registro centralizado de incidentes con análisis de causa raíz. |

### Hallazgos parciales de mayor impacto (⚠️)

- **Consentimiento para datos sensibles** (ítem 3): El aviso actual no diferencia el tratamiento de datos de categoría especial, lo cual es un riesgo legal directo bajo el Art. 6 de la Ley 1581.
- **Evaluación de riesgos ISO 27001** (ítem 13): La última evaluación data de 2022; dos años sin revisión representa una brecha significativa.
- **Mínimo privilegio** (ítem 20): Funcionarios de soporte con acceso a historial clínico sin requerirlo es una violación al principio de necesidad.
- **Datos en respaldo sin cifrar** (ítem 15): Los backups no cifrados representan un vector de exposición masiva en caso de robo o pérdida de medios.

## 🔁 Tareas definidas para complementar el taller

Anote las responsabilidades acordadas entre los miembros del equipo para completar la entrega final:

| Tarea asignada | Responsable | Fecha estimada |
|----------------|-------------|----------------|
| Diligenciar checklist del cliente real | Jhojan Jiménez | 07/04 |
| Redacción del informe     | Jonatan Vergara | 08/04 |
| Investigación y referencias | Carlos Bello | 09/04 |

---

_Este documento resume el trabajo colaborativo realizado durante la sesión del taller X en el curso AREM - Universidad de La Sabana._
