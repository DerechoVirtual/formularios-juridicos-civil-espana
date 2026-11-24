---
name: auto-despacha-ejecucion-laudo-arbitral-decreta-embargo-civ-1881
description: "Auto que despacha ejecución de laudo arbitral y decreta el embargo de bienes. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Auto que despacha ejecución de laudo arbitral y decreta el embargo de bienes

> Formulario **CIV-1881** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

Auto despachando ejecución de laudo arbitral y decretando el embargo de bienes titularidad de la ejecutada.

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Auto que despacha ejecución de laudo arbitral y decreta el embargo de bienes» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Auto que despacha ejecución de laudo arbitral y decreta el embargo de bienes” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:auto-despacha-ejecucion-laudo-arbitral-decreta-embargo-civ-1881`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (10 veces)
- [ ] IMPORTE (8 veces)
- [ ] NOMBRE DE LA PARTE (4 veces)
- [ ] NÚMERO (4 veces)
- [ ] ACTO O RESOLUCIÓN (2 veces)
- [ ] CALLE (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] IMPORTE EN CIFRA (2 veces)
- [ ] SEDE (2 veces)
- [ ] APELLIDOS
- [ ] AÑO
- [ ] FECHA
- [ ] LUGAR
- [ ] NOMBRE DEL COLEGIO
- [ ] Nº

## Normas que cita el formulario

- art. 517 LEC
- art. 44 Ley 60/2003
- art. 546 LEC
- art. 549 LEC
- art. 550.1.1.º LEC
- art. 551 LEC
- art. 553 LEC
- art. 551.4 LEC

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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Junto a «…SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

- Ninguna.

### Flujo

1. **Paso 0**: comprueba Jurisprudenciator (arriba).
2. Lee entero el «Texto del formulario» (al final de este fichero) y la parte de `../indice/marco.md` que afecte al caso. Limítate a la materia de este formulario: no añadas contenido ajeno a él.
3. Pide los datos de la lista en una sola tanda. Si un dato aparece varias veces, aclara a qué persona o acto corresponde cada vez. Lo que el usuario no sepa se queda como hueco visible con su etiqueta (p. ej. [FECHA]).
4. Resuelve cada [ELEGIR …] y cada [OPCIONAL …] según los hechos, y sustituye cualquier indicación entre paréntesis del formulario («(se describirá…)», «(indicar…)») por el contenido que corresponda. Redacta las partes que dependen del caso (hechos, motivos, descripción de bienes).
5. Aplica los avisos de actualización en el lugar que indican. Comprueba con `buscar_articulo` cada norma citada; si alguna ha cambiado, usa la redacción vigente. Si citas jurisprudencia, localízala con `buscar_sentencias` o `buscar_por_cita` y léela con `leer_sentencias`.
6. Antes de entregarlo, pasa `verificar_escrito` con las frases que citan normas o sentencias y corrige lo que señale.
7. **Documento final = el formulario tal cual, rellenado y limpio.**
   - Empieza exactamente por la primera línea del «Texto del formulario» y sigue su estructura y su orden hasta la firma.
   - No pongas en el documento título, nombre del formulario o de la skill, código, encabezados, «Para qué sirve», leyendas, avisos, notas de uso, comentarios ni explicaciones. Tampoco marcas [ELEGIR…] u [OPCIONAL…]: ya están resueltas.
   - Formato Word (.docx, con la skill de Word disponible): **Times New Roman 12 pt** en todo el documento, **interlineado 1,15**, **texto justificado**, márgenes de 2,5 cm. Los rótulos del formulario (REUNIDOS, CLÁUSULAS, HECHOS, SUPLICO…) en su propia línea y en negrita, sin cambiar su texto.
8. En el chat (nunca dentro del documento): datos pendientes, partes redactadas por ti, normas y sentencias comprobadas con Jurisprudenciator (y, si algún dato sale de internet, cuál y su enlace) y, si es un escrito judicial o administrativo, el plazo y el órgano ante el que se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.

## Texto del formulario

Lo que sigue, hasta el final de este fichero, es el formulario tal cual: desde su primera línea hasta la firma.

SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

Tfno.: Fax:

N.I.G.:

Ejecución Título Judicial n.º [NÚMERO]/[AÑO]

Demandante: D./Dña. [NOMBRE Y APELLIDOS]

Abogado/a: D./Dña. [NOMBRE Y APELLIDOS] Procurador: D./Dña. [NOMBRE Y APELLIDOS]

Demandada: [NOMBRE DE LA PARTE].

AUTO

Ilmo. Sr./a. D./Dña. [NOMBRE Y APELLIDOS], Magistrado-Juez de la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [NÚMERO]

En [LUGAR], a [FECHA].

ANTECEDENTES DE HECHO

PRIMERO.- Por la Procurador/a Sr./a [NOMBRE Y APELLIDOS], en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], se presentó escrito en que solicitaba despacho de ejecución frente a [ACTO O RESOLUCIÓN], con fundamento en laudo arbitral, que se acompañaba, siendo el convenio arbitral de constitución automática en régimen de arbitraje de consumo, junto con el documento acreditativo de la notificación a las partes, siendo su tenor:

"Estimar parcialmente la pretensión de D./DÑA. [NOMBRE Y APELLIDOS], en consecuencia, en la sede social de ésta, en el plazo de quince días, contados a partir del siguiente al de la notificación del presente Laudo, abonará a la reclamante [IMPORTE] euros () de la cual [IMPORTE] euros corresponden a la indemnización de los daños causados en la prenda y complementos, y [IMPORTE] euros a la restitución del importe en su día pagado por la prestación del servicio solicitado, y finalmente realizado en forma negligente.

Por su parte D./DÑA. [NOMBRE Y APELLIDOS] entregará la prenda a [NOMBRE DE LA PARTE]., quedando ésta en su poder, a los efectos que considere oportunos".

SEGUNDO.- Los pronunciamientos pedidos en la demanda ejecutiva son:

1.- Despacho de la ejecución por importe de la cantidad de [IMPORTE] xx [IMPORTE] euros ( €) en concepto de principal, más otros [IMPORTE EN CIFRA] yy [IMPORTE] euros ( €) presupuestados provisionalmente para los intereses que puedan generarse durante la ejecución y las costas de ésta.
2.- Embargo de los derechos de los derechos de crédito de [NOMBRE DE LA PARTE]. frente al [NOMBRE DE LA PARTE], domiciliado en [DOMICILIO], calle [CALLE], n.º [NÚMERO], y frente al Colegio San [NOMBRE DEL COLEGIO], domiciliado en [DOMICILIO], calle [CALLE], n.º [NÚMERO], por contratas de limpieza en vigor, que habrá de asegurarse mediante la comunicación de sendos atentos oficios a las entidades deudoras para la retención de cantidades e ingreso en la cuenta de depósitos del Tribunal

FUNDAMENTOS DE DERECHO

PRIMERO.- El laudo arbitral presentado es título que lleva aparejada ejecución conforme a lo que establece el ordinal 2.º del apartado 2 del art. 517 de LEC, la cual rige en el caso con arreglo al art. 44 Ley 60/2003 de 23 de diciembre, de Arbitraje (LA), y examinada de oficio la competencia de este tribunal como impera el art. 546 LEC, este Tribunal es competente objetiva y territorialmente para conocer de la ejecución, según lo dispuesto en los arts. 8.4 LA y 545.2 LEC

SEGUNDO.- El escrito de demanda ejecutiva reúne los requisitos del art. 549 LEC, se acompañan los documentos exigidos para los laudos arbitrales en el segundo párrafo del art. 550.1.1.º LEC, y cumple con los presupuestos contemplados en el art. 551 LEC, por lo que, como dispone esta última norma, procede despachar la ejecución solicitada.

PARTE DISPOSITIVA

Previa admisión de la demanda ejecutiva formulada por D./Dña. [NOMBRE Y APELLIDOS] ISABEL [APELLIDOS], representada por la Procurador/a de los Tribunales D./Dña. [NOMBRE Y APELLIDOS], a la que se tiene por comparecida y parte ejecutante en este procedimiento, SE DESPACHA EJECUCIÓN contra [ACTO O RESOLUCIÓN], por el importe de la cantidad de [IMPORTE] euros ( €) en concepto de principal, más otros [IMPORTE EN CIFRA] yy [IMPORTE] euros ( €) para los intereses que puedan generarse durante la ejecución y las costas, sin perjuicio de definitiva tasación.

Así lo acuerdo, mando y firmo:

Firma del Juez/a:

Esta resolución se notificará a las partes, al ejecutado con copia de la demanda ejecutiva sin citación ni emplazamiento, para que pueda personarse en el proceso, entendiéndose en tal caso con éste las ulteriores diligencias (art. 553 LEC), y advirtiéndose de que no cabe recurso ordinario alguno en cuanto al despacho de ejecución, sin perjuicio de la oposición que, con arreglo a la LEC, pueda deducir el ejecutado (art. 551.4 LEC).

========================================================================
