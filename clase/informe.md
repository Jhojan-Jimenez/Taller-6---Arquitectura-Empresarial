# Informe Técnico - Taller 6: Checklist de Cumplimiento Normativo

## Nombre del Taller
Taller 6 - Checklist de Cumplimiento Normativo (Normatividad y Protección de Datos)

## Integrantes del equipo
- _(Nombre 1)_
- _(Nombre 2)_
- _(Nombre 3)_

---

## Descripción general del trabajo

El presente taller tiene como objetivo verificar el cumplimiento de aspectos legales, normativos y de seguridad de la información en sistemas que procesan datos personales de ciudadanos. Para ello se utilizó una lista de control basada en los marcos ISO/IEC 27001, la Ley 1581 de 2012 (Habeas Data) y las directrices de la Superintendencia de Industria y Comercio (SIC) de Colombia.

El trabajo se desarrolló en dos fases: primero, la aplicación del checklist al caso base **GobData** (portal estatal de trámites ciudadanos), y segundo, la aplicación del mismo instrumento al sistema real del cliente asignado al equipo.

---

## Proceso de desarrollo

1. **Revisión normativa:** Se identificaron los marcos aplicables: Ley 1581 de 2012, Decreto 1377 de 2013, Circular 002 de 2015 de la SIC e ISO/IEC 27001:2022.
2. **Definición de categorías:** Se estructuró el checklist en 9 categorías que cubren el ciclo de vida del dato: desde el consentimiento hasta la gestión de incidentes.
3. **Evaluación del caso GobData:** Se evaluaron 38 criterios con tres niveles: ✅ Cumple, ⚠️ Parcial, ❌ No cumple, acompañados de evidencia y justificación legal.
4. **Evaluación del cliente real:** Se replicó el mismo instrumento adaptando los criterios al contexto operativo del cliente.
5. **Análisis de brechas:** Se priorizaron los hallazgos por nivel de riesgo e impacto normativo.
6. **Redacción de recomendaciones:** Cada brecha identificada cuenta con una recomendación accionable basada en la normativa aplicable.

---

## Análisis del checklist GobData (Caso Base)

### Resumen de cumplimiento

| Nivel             | Cantidad | Porcentaje |
|-------------------|----------|------------|
| ✅ Cumple         | 10       | 26%        |
| ⚠️ Parcial        | 19       | 50%        |
| ❌ No cumple      | 9        | 24%        |
| **Total**         | **38**   | **100%**   |

### Análisis por categoría

**1. Consentimiento Informado**
GobData cuenta con un aviso de privacidad y mecanismo de aceptación, cumpliendo los requisitos básicos del Art. 15 de la Ley 1581. Sin embargo, el sistema no diferencia el tratamiento de datos sensibles (historial clínico, antecedentes) del tratamiento de datos ordinarios, incumpliendo el Art. 6 de la misma ley. La ausencia de un flujo para menores de edad representa el riesgo legal más crítico de esta categoría.

**2. Protección de Datos Personales (Ley 1581)**
La plataforma está registrada ante la SIC y define finalidades claras. No obstante, el proceso para ejercer derechos ARCO (acceso, rectificación, cancelación, oposición) depende exclusivamente de correo electrónico sin trazabilidad ni SLA documentado. El principio de minimización también presenta brechas al solicitar datos innecesarios en algunos formularios.

**3. Seguridad de la Información (ISO 27001)**
El cifrado en tránsito es adecuado (TLS 1.3). Las principales brechas se encuentran en la falta de pentesting reciente, la ausencia de cifrado en ambientes de respaldo, y un plan de continuidad que existe documentado pero nunca ha sido probado mediante simulacros.

**4. Control de Acceso y Roles**
Esta es la categoría con mayor número de brechas críticas. La existencia de cuentas activas de funcionarios retirados y la falta de recertificación periódica representan un riesgo directo de acceso no autorizado a datos de ciudadanos, incluyendo datos de categoría especial (historial médico).

**5. Retención y Eliminación de Datos**
La política de retención existe pero no diferencia por tipo de dato. La eliminación es manual, sin proceso certificado ni automatización, incumpliendo el principio de temporalidad del Art. 4 de la Ley 1581.

**6. Protección contra Fugas (DLP)**
Categoría con brechas más graves en términos de riesgo operativo. La ausencia de herramienta DLP y el uso de datos reales en ambientes de desarrollo exponen a la entidad a incidentes de fuga masiva sin mecanismos de detección o contención.

**7. Auditoría y Trazabilidad**
El sistema genera logs de auditoría para las transacciones del portal, lo cual es positivo. Sin embargo, los logs se retienen solo 6 meses y no se almacenan en repositorios inmutables separados.

**8. Gestión de Incidentes**
El procedimiento de gestión de incidentes no contempla los tiempos de notificación a la SIC establecidos en la Circular 002 de 2015 (máximo 15 días hábiles). La ausencia de un sistema centralizado de registro de incidentes impide el aprendizaje organizacional.

**9. Transferencia de Datos**
Las transferencias internacionales no aplican, lo cual es un punto positivo. Sin embargo, algunas integraciones con entidades del sector salud carecen de acuerdos de tratamiento formalizados conforme al Art. 25 de la Ley 1581.

---

## Componentes y actores del sistema GobData

| Elemento                      | Tipo           | Descripción                                                          | Normativa asociada        |
|-------------------------------|----------------|----------------------------------------------------------------------|---------------------------|
| Ciudadano                     | Actor          | Titular de los datos que realiza trámites en el portal               | Ley 1581 Art. 3           |
| Responsable del Tratamiento   | Rol            | Entidad estatal que define las finalidades del tratamiento           | Ley 1581 Art. 3           |
| Encargado del Tratamiento     | Rol            | Proveedores técnicos que procesan datos por cuenta de la entidad     | Ley 1581 Art. 3           |
| Base de datos de ciudadanos   | Activo         | Repositorio con datos de identidad, salud, impuestos y contacto      | ISO 27001 / Ley 1581      |
| Módulo de autenticación       | Componente     | Gestiona el acceso al portal mediante credenciales y MFA             | ISO 27001 A.9             |
| Logs de auditoría             | Activo         | Registro de operaciones y accesos al sistema                         | ISO 27001 A.12.4          |
| Sistema de trámites           | Componente     | Gestión de solicitudes, certificados y peticiones ciudadanas         | Ley 1581 / Decreto 1377   |
| Integraciones interinstitucionales | Interfaz  | Conexiones con entidades de salud, registro civil e impuestos        | Ley 1581 Art. 25          |

---

## Investigación complementaria

### Tema investigado: Marco normativo colombiano para protección de datos y seguridad de la información en entidades públicas

**Ley 1581 de 2012 y Decreto Reglamentario 1377 de 2013:**
La Ley 1581 establece los principios generales para el tratamiento de datos personales en Colombia: legalidad, finalidad, libertad, veracidad, transparencia, acceso restringido, seguridad y confidencialidad. El Decreto 1377 de 2013 la reglamenta en aspectos como la política de tratamiento, las condiciones para transferencias internacionales y el Registro Nacional de Bases de Datos. Para entidades públicas como GobData, el cumplimiento de esta ley no es opcional sino un imperativo legal cuyo incumplimiento puede generar sanciones de hasta 2.000 SMMLV por parte de la SIC.

**ISO/IEC 27001:2022:**
La versión 2022 del estándar ISO 27001 reorganizó los controles del antiguo Anexo A en cuatro temas: controles organizacionales, controles de personas, controles físicos y controles tecnológicos. Introdujo nuevos controles relevantes para GobData como gestión de amenazas de inteligencia (5.7), seguridad en la nube (5.23) y enmascaramiento de datos (8.11). La certificación ISO 27001 no es obligatoria para entidades públicas colombianas, pero su adopción demuestra madurez en seguridad y facilita el cumplimiento de la Ley 1581.

**Circular 002 de 2015 - SIC:**
Esta circular regula la gestión y notificación de incidentes de seguridad que involucren datos personales. Establece que los responsables del tratamiento deben notificar a la SIC dentro de los 15 días hábiles siguientes al conocimiento de una vulneración. También requiere que se comunique a los titulares afectados cuando el incidente pueda generarles un daño patrimonial o moral significativo. GobData, como plataforma que maneja datos sensibles de millones de ciudadanos, tiene una exposición muy alta bajo este marco.

---

## Recomendaciones prioritarias

Las siguientes recomendaciones se presentan ordenadas por nivel de criticidad:

### Crítico (requiere acción inmediata)

1. **Flujo para menores de edad:** Implementar un proceso de registro diferenciado con validación de representante legal conforme al Art. 7 de la Ley 1581, antes del próximo ciclo de auditoría de la SIC.

2. **Desactivación de cuentas:** Automatizar la desactivación de cuentas al momento de la desvinculación laboral mediante integración con el sistema de RRHH. Realizar una auditoría inmediata de cuentas activas sin actividad en los últimos 90 días.

3. **Datos en ambientes de desarrollo:** Prohibir inmediatamente el uso de datos reales de ciudadanos en ambientes de prueba. Implementar un proceso de enmascaramiento o generación de datos sintéticos.

4. **Protocolo de notificación de incidentes:** Actualizar el procedimiento de gestión de incidentes para incluir los tiempos y canales de notificación a la SIC establecidos en la Circular 002 de 2015.

### Alta prioridad (plazo máximo 3 meses)

5. **Recertificación de accesos:** Implementar un proceso trimestral de revisión y certificación de accesos, especialmente para roles con acceso a datos de categoría especial.

6. **Consentimiento diferenciado para datos sensibles:** Actualizar el aviso de privacidad y el formulario de consentimiento para separar explícitamente el tratamiento de datos sensibles con las finalidades específicas y los riesgos aplicables.

7. **Cifrado de backups:** Extender el cifrado AES-256 a todos los ambientes de almacenamiento incluyendo respaldos y entornos no productivos.

8. **Retención automatizada:** Definir plazos específicos de retención por categoría de dato e implementar un proceso automatizado de purga con generación de evidencia certificada.

### Mediano plazo (3 a 6 meses)

9. **Herramienta DLP:** Evaluar e implementar una solución de prevención de pérdida de datos que controle extracción masiva, transferencias no autorizadas y comunicaciones con datos sensibles.

10. **Pentesting anual:** Contratar evaluaciones de seguridad ofensiva con reporte documentado y plan de remediación con seguimiento verificable.

11. **Módulo ARCO:** Desarrollar un módulo dentro del portal ciudadano que permita gestionar solicitudes de acceso, rectificación, cancelación y oposición con tiempos de respuesta controlados (máximo 15 días hábiles).

12. **Simulacros de continuidad:** Ejecutar al menos un simulacro anual del BCP/DRP con medición de tiempos de recuperación (RTO/RPO) y registro de resultados.

---

_Este informe hace parte de la entrega del Taller 6 del curso AREM (Arquitectura Empresarial) - Universidad de La Sabana._
