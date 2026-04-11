# 📄 Informe Técnico del Taller
## 🔖 Nombre del Taller

_Taller 6: Checklist de Cumplimiento Normativo_

## 👥 Integrantes del equipo
- Jonatan David Vergara Suárez (github.com/JonatnV)
- Carlos David Bello Ortiz
- Jhojan Camilo Jiménez Amaya

## 🧠 Descripción general del trabajo

El presente taller tiene como objetivo evaluar el nivel de cumplimiento normativo y de seguridad de la información de la empresa cliente, tomando como base marcos regulatorios y buenas prácticas como la Ley 1581 de 2012 (Habeas Data), la norma ISO/IEC 27001 y lineamientos de protección de datos personales.

Para el desarrollo de la actividad se utilizó un enfoque basado en checklist tipo GobData, que permite identificar de forma estructurada el grado de cumplimiento de la organización frente a distintos criterios legales, técnicos y organizacionales. A partir de esta evaluación, se identificaron brechas, riesgos asociados y oportunidades de mejora, priorizando aquellas que tienen mayor impacto en la continuidad del negocio y la protección de la información.

El análisis se centró en los principales activos de la empresa, como el ERP, bases de datos, almacenamiento en la nube (Google Drive), red interna y procesos comerciales, administrativos e industriales.

## 🔧 Proceso de desarrollo

El desarrollo del taller se realizó en varias etapas:

Identificación del contexto del negocio
Se analizaron los procesos principales de la empresa: comercialización de productos electrónicos, fabricación de sensores e integración de sistemas industriales. También se identificaron los sistemas utilizados (ERP World Office, CRM, Google Drive) y la forma en que interactúan.
Selección de marcos normativos y de referencia
Se definieron como base:
Ley 1581 de 2012 (Habeas Data)
ISO/IEC 27001
Normativa de comercio electrónico y facturación (DIAN)
Buenas prácticas de protección de datos y gobernanza TI

Construcción del checklist de cumplimiento
Se elaboró una tabla estructurada con criterios de cumplimiento, evaluando cada uno como:

✅ Cumple
⚠️ Parcial
❌ No cumple

En esta etapa se tomó la decisión de reflejar la realidad operativa del negocio, considerando que muchos controles existen de forma implícita pero no formalizada.

Identificación de brechas y riesgos
A partir del checklist, se construyó una segunda tabla enfocada en:
Brechas identificadas
Riesgos asociados
Recomendaciones priorizadas
Priorización de acciones
Se priorizaron las acciones con base en el impacto en:
Seguridad de la información
Continuidad del negocio
Cumplimiento legal

Durante el proceso, se optó por un enfoque práctico, orientado a decisiones reales de la empresa, evitando un análisis puramente teórico.

## 🧩 Análisis del modelo propuesto
### 📌 Estructura del modelo

El modelo se estructura en dos componentes principales:

Checklist de cumplimiento (Hoja 1)
Permite evaluar de forma general el estado de la organización frente a distintos criterios legales y de seguridad, utilizando una clasificación simple (cumple, parcial, no cumple) acompañada de evidencia y recomendaciones.
Matriz de brechas y plan de acción (Hoja 2)
Profundiza en los hallazgos del checklist, identificando las principales debilidades, los riesgos asociados y las acciones necesarias para mitigarlos, junto con su nivel de prioridad.

Esta estructura facilita tanto el análisis técnico como la toma de decisiones a nivel ejecutivo.

### 📌 Representación de las necesidades del cliente

El modelo representa adecuadamente la realidad de la empresa, ya que:

Considera su dependencia de sistemas clave como el ERP y el almacenamiento en la nube.
Refleja el uso de procesos manuales en áreas críticas como el cálculo de precios y la gestión de información.
Identifica riesgos reales del negocio, como:
Fuga de información en Google Drive
Falta de integración entre sistemas
Dependencia de un único servidor
Integra tanto aspectos tecnológicos como operativos, alineando la seguridad con procesos comerciales, administrativos e industriales.

Además, el modelo evidencia que, aunque la empresa cumple con aspectos generales de Habeas Data, existen debilidades importantes en la formalización y control de los procesos.

### 📌 Supuestos del análisis

Para el desarrollo del modelo se tomaron los siguientes supuestos:

La empresa cumple con los principios básicos de la Ley 1581 de 2012 (Habeas Data), especialmente en la recolección y uso de datos personales dentro de sus procesos comerciales.
No existe una formalización completa de políticas, procedimientos y registros ante entidades regulatorias.
La infraestructura tecnológica es básica, con:
Un servidor principal sin alta disponibilidad
Uso de herramientas en la nube sin integración automatizada
Los controles de seguridad actuales son limitados, incluyendo:
Autenticación básica
Falta de monitoreo centralizado
Ausencia de gestión formal de incidentes
Los procesos manuales siguen siendo una parte importante de la operación, lo que incrementa el riesgo de errores e inconsistencias.

Estos supuestos permiten construir un escenario realista que refleja el nivel de madurez actual de la empresa en términos de seguridad y cumplimiento.

## 🔍 Investigación complementaria
### Tema investigado:
Normativas locales o sectoriales que impacten a nuestra empresa **(A&C Ingeniería S.A.S)**

### Resumen:
En el ámbito de la automatización industrial en Colombia, las normativas locales clave impactan las empresas mediante requisitos estrictos de protección de datos personales y gestión de seguridad de la información, aplicables a sistemas como SCADA, IoT y procesos automatizados que manejan datos sensibles. La Ley 1581 de 2012, reglamentada por el Decreto 1377 de 2013, la Ley 1266 de 2008 sobre habeas data financiero y la Ley 527 de 1999 sobre comercio electrónico exigen consentimiento, finalidad y medidas de seguridad en la recolección y procesamiento de datos de empleados, clientes o activos, evitando sanciones por incumplimiento. La Superintendencia de Industria y Comercio (SIC) refuerza esto con la Circular Externa 002 de 2015 para incidentes de seguridad, la guía de accountability y el RNBD, obligando a protocolos de reporte y registro de bases de datos.

Estos marcos se complementan con estándares internacionales como ISO/IEC 27001:2022, ISO/IEC 27002:2022, ISO/IEC 27701:2019 y NIST SP 800-53 Rev. 5, junto a guías de MinTIC, OWASP Top Ten y ENISA, que orientan controles de ciberseguridad y privacidad para mitigar riesgos en entornos industriales. Esto se puede verificar mediante el uso de el checklist que permite evaluar y documentar el alineamiento de procesos automatizados con estas disposiciones, identificando brechas en protección de datos y seguridad para generar un plan de acción correctiva.



## 📚 Referencias
- [1] Congreso de la República de Colombia. Ley 1581 de 2012 - Por la cual se dictan disposiciones generales para la protección de datos personales. 2012. https://www.funcionpublica.gov.co/eva/gestornormativo/norma.php?i=49981
- [2] Presidencia de la República de Colombia. Decreto 1377 de 2013 - Por el cual se reglamenta parcialmente la Ley 1581 de 2012. 2013. https://www.funcionpublica.gov.co/eva/gestornormativo/norma.php?i=53646
- [3] Congreso de la República de Colombia. Ley 1266 de 2008 - Habeas Data Financiero. 2008. https://www.funcionpublica.gov.co/eva/gestornormativo/norma.php?i=34488
- [4] Congreso de la República de Colombia. Ley 527 de 1999 - Comercio electrónico y firmas digitales. 1999. https://www.funcionpublica.gov.co/eva/gestornormativo/norma.php?i=4276
- [5] Superintendencia de Industria y Comercio (SIC). Circular Externa 002 de 2015 - Gestión de incidentes de seguridad. 2015. https://www.sic.gov.co/
- [6] Superintendencia de Industria y Comercio (SIC). Guía para la implementación del principio de responsabilidad demostrada (accountability). 2018. https://www.sic.gov.co/recursos_user/2018/publicaciones/Guia_Accountability.pdf
- [7] uperintendencia de Industria y Comercio (SIC). Registro Nacional de Bases de Datos (RNBD) - Instructivo de inscripción. 2016. https://www.sic.gov.co/registro-nacional-de-bases-de-datos
- [8] nternational Organization for Standardization. ISO/IEC 27001:2022 - Information security management systems. 2022. https://www.iso.org/standard/27001
- [9] International Organization for Standardization. ISO/IEC 27002:2022 - Information security controls. 2022. https://www.iso.org/standard/75652.html
- [10] International Organization for Standardization. ISO/IEC 27701:2019 - Privacy information management. 2019. https://www.iso.org/standard/71670.html
- [11] National Institute of Standards and Technology (NIST). NIST SP 800-53 Rev. 5 - Security and Privacy Controls. 2020. https://csrc.nist.gov/publications/detail/sp/800-53/rev-5/final

---

_Este documento hace parte de la entrega del taller X del curso AREM (Arquitectura Empresarial) - Universidad de La Sabana._
