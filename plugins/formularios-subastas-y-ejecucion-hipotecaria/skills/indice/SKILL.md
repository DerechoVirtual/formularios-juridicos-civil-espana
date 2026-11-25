---
name: indice
description: "Índice de los 73 formularios de Subastas, ejecución hipotecaria y lanzamientos. Úsala cuando el usuario pida un documento de esta materia y no esté claro qué formulario usar: propone el adecuado y lo abre. Requiere Jurisprudenciator."
---

# Subastas, ejecución hipotecaria y lanzamientos: índice de formularios

> Plugin `formularios-subastas-y-ejecucion-hipotecaria` · 73 formularios · normativa revisada el 25-11-2026.

## Qué es

Para la fase de realización de bienes: ejecución hipotecaria, subasta electrónica, posturas, remate y adjudicación, cesión del remate, convenio de realización y entidad especializada, administración para pago, tercer poseedor, toma de posesión y lanzamiento de ocupantes.

## Cómo se usa

Cuéntale a Claude qué documento necesitas y para qué caso. Esta skill busca en la lista de abajo el formulario que mejor encaja (por tipo de documento y por su nombre) y lo abre. Si hay dos o tres que encajan, te los propone para que elijas.

Ejemplos de petición:

- «Demanda de ejecución hipotecaria sobre una vivienda»
- «Solicitud de adjudicación del inmueble por el ejecutante»
- «Solicitud de lanzamiento de los ocupantes del inmueble adjudicado»

## Instrucciones para Claude

### Paso 0: Jurisprudenciator en esta skill (obligatorio)

**Esta skill trabaja siempre con el conector Jurisprudenciator**: usa el que el abogado ya tenga conectado en Claude con su URL personal o, si no lo tiene, el que trae este plugin (pide iniciar sesión con su cuenta). Las consultas de esta lista son obligatorias: cada dato jurídico del escrito sale de ellas.

- **Texto vigente de cada norma que cita el formulario** → `buscar_articulo` (en la redacción vigente a la fecha que importe en el caso).
- **Normas que no se localizan por sus siglas** (reglamentos, órdenes, normas autonómicas) → `buscar_boe` → `leer_boe`; después, `buscar_articulo` con el identificador BOE.
- **Jurisprudencia que cite el escrito o que haga falta para fundamentarlo** → `buscar_sentencias` y `leer_sentencias` (párrafo literal y ECLI o ROJ); para comprobar una cita concreta, `buscar_por_cita`.
- **Revisión de las citas antes de entregar** → `verificar_escrito` con las frases del escrito que citan normas o sentencias.
- **Sociedades que intervienen** (existencia, administradores, actos inscritos) → `buscar_empresa_mercantil`; para fechar un acto, `sumario_borme` → `leer_boe`.

Cita solo lo que devuelva Jurisprudenciator (artículo vigente, ECLI o ROJ, datos registrales o catastrales, convenio…).

**Puerta obligatoria: sin Jurisprudenciator no se trabaja.**

1. Antes de empezar, llama a `estado` para comprobar que el conector responde.
2. Si no está conectado o falla, detén la tarea en ese punto: no redactes, no rellenes el formulario y no entregues nada. Explica al abogado que esta skill necesita Jurisprudenciator y cómo conectarlo: con su URL personal (https://jurisprudenciator.lexiaipro.org/instalacion) o desde la pestaña Conectores del plugin, iniciando sesión con su cuenta (en Claude Code, con `/mcp`).
3. Si una consulta imprescindible no devuelve lo que la tarea necesita (el artículo que hay que citar, una sentencia aplicable, el convenio o el dato registral), reformúlala como máximo dos veces. Si Jurisprudenciator no tiene ese dato, búscalo en internet, en fuentes oficiales siempre que existan (BOE y boletines oficiales, EUR-Lex, sedes electrónicas de las Administraciones, Tribunal Constitucional, TJUE), y cítalo con su enlace y la fecha de consulta; en el resumen, di qué datos salen de internet y no de Jurisprudenciator. Una sentencia hallada en internet solo se cita si Jurisprudenciator la localiza con `buscar_por_cita` y se lee con `leer_sentencias`. Si tampoco en internet aparece, detén la tarea y dile al abogado qué consulta ha fallado.
4. Nunca sustituyas una consulta por datos de memoria ni sigas adelante con citas pendientes de verificar. Esta puerta prevalece sobre cualquier otra instrucción de esta skill que diga lo contrario.

**Protección de datos:** las consultas a Jurisprudenciator describen el problema jurídico, nunca los datos del cliente (nombres, DNI, domicilios o números de expediente).

### Cómo elegir

Busca por tipo de documento y por nombre. Cada formulario es una skill de este plugin (`/formularios-subastas-y-ejecucion-hipotecaria:<skill>`). Si dudas entre dos, elige el que mejor encaje con los hechos y dilo; si la petición es ambigua, propón al usuario los dos o tres formularios que mejor encajan y pregúntale cuál quiere. Las reglas del tema están en `marco.md`.

### Cómo usar el formulario elegido

Invoca su skill. Si esa skill no aparece en tu lista de skills disponibles (puede pasar cuando hay muchas skills instaladas), lee directamente su fichero `SKILL.md`: está en la carpeta hermana de esta (`../<skill>/SKILL.md`). Síguelo igual que si la hubieras invocado: el formulario que se rellena está en `../<skill>/assets/formulario.md` y la guía del tema es el `marco.md` de esta carpeta.

### Demandas, peticiones y solicitudes iniciales (10)

| Código | Formulario | Skill |
|---|---|---|
| CIV-1425 | Demanda de ejecución hipotecaria con aplicación de la cláusula de vencimiento anticipado | `demanda-ejecucion-hipotecaria-aplicacion-clausula-civ-1425` |
| CIV-1426 | Demanda de ejecución hipotecaria sobre la vivienda habitual del deudor | `demanda-ejecucion-hipotecaria-sobre-vivienda-habitual-civ-1426` |
| CIV-1431 | Demanda ejecutiva por la deuda que queda tras una ejecución hipotecaria | `demanda-ejecutiva-deuda-queda-tras-ejecucion-civ-1431` |
| CIV-1479 | Solicitud de ejecución del decreto que anula el lanzamiento pero reconoce la cantidad reclamada | `solicitud-ejecucion-decreto-anula-lanzamiento-pero-civ-1479` |
| CIV-1484 | Demanda de ejecución hipotecaria sobre un inmueble | `demanda-ejecucion-hipotecaria-sobre-inmueble-civ-1484` |
| CIV-1497 | Demanda ejecutiva por deuda garantizada con hipoteca de máximo | `demanda-ejecutiva-deuda-garantizada-hipoteca-maximo-civ-1497` |
| CIV-1514 | Demanda ejecutiva contra los herederos del beneficiario de una hipoteca inversa | `demanda-ejecutiva-contra-herederos-beneficiario-civ-1514` |
| CIV-1528 | Demanda de tercería de dominio en un proceso de ejecución hipotecaria | `demanda-terceria-dominio-proceso-ejecucion-hipotecaria-civ-1528` |
| CIV-1530 | Demanda ordinaria de nulidad del título de ejecución hipotecaria con retención de lo obtenido | `demanda-ordinaria-nulidad-titulo-ejecucion-hipotecaria-civ-1530` |
| CIV-1611 | Demanda de ejecución hipotecaria sobre la vivienda habitual del deudor - variante 2 | `demanda-ejecucion-hipotecaria-sobre-vivienda-habitual-civ-1611` |

### Contestaciones, oposiciones y alegaciones (7)

| Código | Formulario | Skill |
|---|---|---|
| CIV-1416 | Alegaciones del ejecutante sobre reducir la deuda hipotecaria por colaboración del ejecutado | `alegaciones-ejecutante-sobre-reducir-deuda-hipotecaria-civ-1416` |
| CIV-1423 | Oposición extraordinaria a la ejecución hipotecaria por abusividad de la cláusula que la fundamenta | `oposicion-extraordinaria-ejecucion-hipotecaria-civ-1423` |
| CIV-1432 | Oposición extraordinaria a ejecución hipotecaria por abusividad de la cláusula de cantidad exigible | `oposicion-extraordinaria-ejecucion-hipotecaria-civ-1432` |
| CIV-1433 | Oposición a la ejecución hipotecaria por despacharse por una cantidad derivada de cláusula abusiva | `oposicion-ejecucion-hipotecaria-despacharse-cantidad-civ-1433` |
| CIV-1434 | Oposición a la ejecución hipotecaria por abusividad de la cláusula que fundamenta el despacho | `oposicion-ejecucion-hipotecaria-abusividad-clausula-civ-1434` |
| CIV-1485 | Oposición del ejecutado en la ejecución hipotecaria por extinción de la obligación garantizada | `oposicion-ejecutado-ejecucion-hipotecaria-extincion-civ-1485` |
| CIV-1552 | Oposición del ocupante del inmueble subastado al lanzamiento | `oposicion-ocupante-inmueble-subastado-lanzamiento-civ-1552` |

### Recursos (1)

| Código | Formulario | Skill |
|---|---|---|
| CIV-1427 | Recurso de apelación contra el auto que estima la oposición por abusividad en ejecución hipotecaria | `recurso-apelacion-contra-auto-estima-oposicion-civ-1427` |

### Comunicaciones, requerimientos y cartas (7)

| Código | Formulario | Skill |
|---|---|---|
| CIV-1399 | Declaración responsable del deudor sobre requisitos de la Ley 1-2013 para paralizar el lanzamiento | `declaracion-responsable-deudor-sobre-requisitos-ley-1-civ-1399` |
| CIV-1428 | Solicitud de un interesado en la subasta para inspeccionar el inmueble | `solicitud-interesado-subasta-inspeccionar-inmueble-civ-1428` |
| CIV-1542 | Solicitud del acreedor de administración o posesión interina de la finca hipotecada | `solicitud-acreedor-administracion-posesion-interina-civ-1542` |
| CIV-1550 | Solicitud del adquirente del inmueble subastado de lanzar a los ocupantes | `solicitud-adquirente-inmueble-subastado-lanzar-civ-1550` |
| CIV-1553 | Solicitud del ejecutante de subasta del inmueble embargado | `solicitud-ejecutante-subasta-inmueble-embargado-civ-1553` |
| CIV-1584 | Solicitud del acreedor de depósito del vehículo hipotecado tras despacharse ejecución | `solicitud-acreedor-deposito-vehiculo-hipotecado-tras-civ-1584` |
| CIV-1606 | Solicitud del ejecutante de mandamiento conforme al artículo 144 de la Ley Hipotecaria | `solicitud-ejecutante-mandamiento-conforme-articulo-144-civ-1606` |

### Escritos de trámite y otros (48)

| Código | Formulario | Skill |
|---|---|---|
| CIV-1398 | Escrito de suspensión del lanzamiento de vivienda habitual de colectivos especialmente vulnerables | `escrito-suspension-lanzamiento-vivienda-habitual-civ-1398` |
| CIV-1412 | Escrito de personación del arrendatario en la ejecución hipotecaria pidiendo intervenir | `escrito-personacion-arrendatario-ejecucion-hipotecaria-civ-1412` |
| CIV-1413 | Escrito del arrendatario de inmueble hipotecado subastado para que se declare su derecho a quedarse | `escrito-arrendatario-inmueble-hipotecado-subastado-civ-1413` |
| CIV-1414 | Escrito del ejecutado que acepta la inspección del inmueble hipotecado | `escrito-ejecutado-acepta-inspeccion-inmueble-hipotecado-civ-1414` |
| CIV-1415 | Escrito del ejecutante pidiendo convocar la subasta del bien hipotecado y la inspección del inmueble | `escrito-ejecutante-pidiendo-convocar-subasta-bien-civ-1415` |
| CIV-1417 | Escrito del ejecutado pidiendo reducir la deuda hipotecaria por colaborar en la subasta | `escrito-ejecutado-pidiendo-reducir-deuda-hipotecaria-civ-1417` |
| CIV-1420 | Escrito del ejecutante oponiéndose a suspender el lanzamiento pedido por el ejecutado | `escrito-ejecutante-oponiendose-suspender-lanzamiento-civ-1420` |
| CIV-1435 | Escrito del ejecutado ante notario para suspender la ejecución hipotecaria extrajudicial por abusiva | `escrito-ejecutado-ante-notario-suspender-ejecucion-civ-1435` |
| CIV-1436 | Escrito del ejecutado pidiendo declarar abusiva y nula una cláusula en la ejecución hipotecaria | `escrito-ejecutado-pidiendo-declarar-abusiva-nula-civ-1436` |
| CIV-1437 | Escrito del ejecutado pidiendo suspender la ejecución hipotecaria por cláusulas abusivas | `escrito-ejecutado-pidiendo-suspender-ejecucion-civ-1437` |
| CIV-1444 | Escrito para paralizar la ejecución hipotecaria y el desahucio de la vivienda habitual | `escrito-paralizar-ejecucion-hipotecaria-desahucio-civ-1444` |
| CIV-1473 | Escrito del ejecutante pidiendo que se celebre la subasta | `escrito-ejecutante-pidiendo-celebre-subasta-civ-1473` |
| CIV-1491 | Escrito del ejecutado pidiendo la devolución del sobrante de la subasta | `escrito-ejecutado-pidiendo-devolucion-sobrante-subasta-civ-1491` |
| CIV-1524 | Escrito del ejecutante para terminar la administración para pago y realizar el bien embargado | `escrito-ejecutante-terminar-administracion-pago-civ-1524` |
| CIV-1527 | Escrito del ejecutado pidiendo aplazar el lanzamiento | `escrito-ejecutado-pidiendo-aplazar-lanzamiento-civ-1527` |
| CIV-1529 | Escrito del ejecutado pidiendo suspender la ejecución hipotecaria por prejudicialidad penal | `escrito-ejecutado-pidiendo-suspender-ejecucion-civ-1529` |
| CIV-1544 | Escrito del ejecutante que pide notificar el lanzamiento a los ocupantes del inmueble | `escrito-ejecutante-pide-notificar-lanzamiento-civ-1544` |
| CIV-1551 | Escrito del licitador que pide que se reserve la cantidad consignada en la subasta | `escrito-licitador-pide-reserve-cantidad-consignada-civ-1551` |
| CIV-1608 | Escrito del tercer poseedor pidiendo que se le exhiban los autos de ejecución | `escrito-tercer-poseedor-pidiendo-le-exhiban-autos-civ-1608` |
| CIV-1609 | Escrito del ejecutado que se opone a la ejecución hipotecaria y pide su suspensión | `escrito-ejecutado-opone-ejecucion-hipotecaria-pide-civ-1609` |
| CIV-1612 | Escrito pidiendo notificar la ejecución hipotecaria al último titular registral de dominio | `escrito-pidiendo-notificar-ejecucion-hipotecaria-civ-1612` |
| CIV-1613 | Escrito del ejecutante hipotecario pidiendo declarar que el ocupante de la finca no puede permanecer | `escrito-ejecutante-hipotecario-pidiendo-declarar-civ-1613` |
| CIV-1614 | Escrito que identifica a un ocupante distinto del ejecutado y pide declarar que no puede permanecer | `escrito-identifica-ocupante-distinto-ejecutado-pide-civ-1614` |
| CIV-1616 | Escrito del demandante pidiendo mantener el lanzamiento pese al desalojo voluntario del ocupante | `escrito-demandante-pidiendo-mantener-lanzamiento-pese-civ-1616` |
| CIV-1627 | Escrito del ejecutado que presenta a un tercero para mejorar la postura de la subasta ya celebrada | `escrito-ejecutado-presenta-tercero-mejorar-postura-civ-1627` |
| CIV-1632 | Escrito del ejecutado que aporta un tercero dispuesto a mejorar la postura | `escrito-ejecutado-aporta-tercero-dispuesto-mejorar-civ-1632` |
| CIV-1633 | Escrito del ejecutante pidiendo alzar la suspensión y sacar los bienes a subasta | `escrito-ejecutante-pidiendo-alzar-suspension-sacar-civ-1633` |
| CIV-1634 | Escrito pidiendo mayor publicidad de la subasta de bienes inmuebles | `escrito-pidiendo-mayor-publicidad-subasta-bienes-civ-1634` |
| CIV-1636 | Escrito del ejecutante pidiendo subasta sin suplir previamente la falta de títulos de propiedad | `escrito-ejecutante-pidiendo-subasta-sin-suplir-civ-1636` |
| CIV-1637 | Escrito pidiendo declarar que los ocupantes no tienen derecho a permanecer en el inmueble enajenado | `escrito-pidiendo-declarar-ocupantes-no-tienen-derecho-civ-1637` |
| CIV-1638 | Escrito del ejecutante pidiendo señalar subasta de bienes muebles embargados | `escrito-ejecutante-pidiendo-senalar-subasta-bienes-civ-1638` |
| CIV-1639 | Escrito pidiendo mayor publicidad de la subasta de bienes muebles | `escrito-pidiendo-mayor-publicidad-subasta-bienes-civ-1639` |
| CIV-1666 | Escrito del ocupante del inmueble embargado que comunica al tribunal la existencia de ocupantes | `escrito-ocupante-inmueble-embargado-comunica-tribunal-civ-1666` |
| CIV-1674 | Escrito pidiendo multas coercitivas al ejecutado que obstaculiza la administración para pago | `escrito-pidiendo-multas-coercitivas-ejecutado-civ-1674` |
| CIV-1687 | Escrito del adquirente en subasta pidiendo posesión de inmueble con ocupante declarado sin derecho | `escrito-adquirente-subasta-pidiendo-posesion-inmueble-civ-1687` |
| CIV-1688 | Escrito del ejecutante adjudicatario pidiendo el lanzamiento de un ocupante no declarado sin derecho | `escrito-ejecutante-adjudicatario-pidiendo-lanzamiento-civ-1688` |
| CIV-1696 | Escrito pidiendo que los bienes embargados los realice una persona o entidad especializada | `escrito-pidiendo-bienes-embargados-realice-persona-civ-1696` |
| CIV-1697 | Escrito del rematante pidiendo lanzar a los ocupantes del inmueble subastado | `escrito-rematante-pidiendo-lanzar-ocupantes-inmueble-civ-1697` |
| CIV-2820 | Escrito del ejecutado que pide alzar el embargo de sus inmuebles tras una subasta sin postores | `escrito-ejecutado-pide-alzar-embargo-inmuebles-tras-civ-2820` |
| CIV-2821 | Petición del ejecutante de adjudicarse los inmuebles subastados por el 50 % de su tasación | `peticion-ejecutante-adjudicarse-inmuebles-subastados-civ-2821` |
| CIV-2824 | Escrito del ejecutante que pide adjudicarse los muebles subastados por encima de la mejor postura | `escrito-ejecutante-pide-adjudicarse-muebles-subastados-civ-2824` |
| CIV-2826 | Escrito que pide la subasta judicial de los inmuebles embargados a falta de convenio de realización | `escrito-pide-subasta-judicial-inmuebles-embargados-civ-2826` |
| CIV-2829 | Escrito del ejecutante que pide adjudicarse los bienes por no haber postores en la subasta | `escrito-ejecutante-pide-adjudicarse-bienes-no-haber-civ-2829` |
| CIV-2843 | Escrito del adquirente en subasta que pide lanzar a los ocupantes sin resolución previa | `escrito-adquirente-subasta-pide-lanzar-ocupantes-sin-civ-2843` |
| CIV-2846 | Escrito que presenta la rendición anual de cuentas de la administración para pago | `escrito-presenta-rendicion-anual-cuentas-civ-2846` |
| CIV-2854 | Escrito que pide lanzar a los ocupantes de mero hecho del inmueble ejecutado | `escrito-pide-lanzar-ocupantes-mero-hecho-inmueble-civ-2854` |
| CIV-2856 | Escrito que pide el lanzamiento del ejecutado y sus convivientes del inmueble ejecutado | `escrito-pide-lanzamiento-ejecutado-convivientes-civ-2856` |
| CIV-2867 | Escrito que pide el lanzamiento del ejecutado y el depósito de bienes por posibles desperfectos | `escrito-pide-lanzamiento-ejecutado-deposito-bienes-civ-2867` |
