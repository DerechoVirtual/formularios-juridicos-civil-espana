---
name: providencia-suspende-proceso-comprobar-competencia-civ-1811
description: "Providencia que suspende el proceso para comprobar la competencia internacional (Reglamento 2201). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Providencia que suspende el proceso para comprobar la competencia internacional (Reglamento 2201)

> Formulario **CIV-1811** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

TRIBUNAL DE INSTANCIA DE , SECCIÓN CIVIL, PLAZA JUDICIAL N.º PROVIDENCIA. HECHOS RAZONAMIENTOS JURÍDICOS PARTE DISPOSITIVA

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Providencia que suspende el proceso para comprobar la competencia internacional (Reglamento 2201)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Providencia que suspende el proceso para comprobar la competencia internacional (Reglamento 2201)” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:providencia-suspende-proceso-comprobar-competencia-civ-1811`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] ACTO O RESOLUCIÓN (2 veces)
- [ ] FECHA (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] AÑO
- [ ] DOMICILIO
- [ ] DÍA
- [ ] LUGAR
- [ ] MES
- [ ] NOMBRE DE LA PARTE
- [ ] NÚMERO
- [ ] SEDE

## Normas que cita el formulario

- No cita artículos concretos; Claude localizará las normas aplicables con Jurisprudenciator si el documento las necesita.

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

### Avisos de actualización (0) — se aplican en el texto, nunca se copian en el documento

- Ninguno.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

El Reglamento (CE) n.º 2201/2003 fue completamente sustituido por el Reglamento (UE) 2019/1111 (Bruselas II ter) desde el 1 de agosto de 2022, pero se sigue aplicando a las demandas judiciales interpuestas, a los documentos públicos con fuerza ejecutiva formalizados y a los acuerdos registrados antes del 1 de agosto de 2022.

Cualquier litigio o trámite iniciado a partir de esa fecha se rige estrictamente por la nueva versión (Bruselas II ter).


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

TRIBUNAL DE INSTANCIA DE [SEDE], SECCIÓN CIVIL, PLAZA JUDICIAL N.º [NÚMERO]

PROVIDENCIA.

El/la MAGISTRADO- JUEZ D./Dña. [NOMBRE Y APELLIDOS]

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Dada cuenta del estado de los presentes Autos, procede acordar la suspensión de su tramitación de conformidad con los siguientes

HECHOS

Primero.- Que por la parte actora, D./D.ª [NOMBRE Y APELLIDOS], se presentó escrito de demanda de Juicio [Nº DE PROCEDIMIENTO] contra [ACTO O RESOLUCIÓN] domiciliado en [DOMICILIO], que fue admitida a trámite mediante Auto de fecha [FECHA], acordándose emplazar a la parte demandada, por término de

Segundo.- Que con fecha de [FECHA] consta el traslado al organismo transmisor competente de la Solicitud de Notificación o traslado de documentos al que se refiere el artículo 4.3 del Reglamento CE 1393/2007, de 13 de noviembre de 2007 relativo a la notificación y al traslado en los Estados miembros de documentos judiciales y extrajudiciales en materia civil o mercantil.

RAZONAMIENTOS JURÍDICOS

Primero.- El artículo 17 del Reglamento (CE) n.° 2201/2003 del Consejo de 27 de noviembre de 2003 relativo a la Competencia, el Reconocimiento y la Ejecución de Resoluciones judiciales en materia matrimonial y de Responsabilidad parental, aplicable al caso por razones de derecho intertemporal, establece que "El órgano jurisdiccional de un Estado miembro ante el que se inicie un procedimiento respecto del cual el presente Reglamento no establezca su competencia y del que sea competente en virtud del mismo un órgano jurisdiccional de otro Estado miembro, se declarará de oficio incompetente".

Nota: El artículo 18 del Reglamento 2201/2003 establece otra comprobación obligatoria cuando el demandado no comparece: "1. Cuando una parte demandada con residencia habitual en un Estado distinto del Estado miembro en el que se hubiera presentado la demanda no compareciere, el órgano jurisdiccional competente suspenderá el procedimiento hasta que se tenga constancia de que dicha parte demandada ha estado en condiciones de recibir, con suficiente antelación para defenderse, el escrito de demanda o documento equivalente o de que se han practicado todas las diligencias a tal fin.

2. Se aplicará el artículo 19 del Reglamento (CE) n.° 1348/2000 en lugar del apartado 1 del presente artículo, si el escrito de demanda o documento equivalente hubiera de transmitirse de un Estado miembro a otro de acuerdo con dicho Reglamento.

3. Cuando no sean aplicables las disposiciones del Reglamento (CE) n.° 1348/2000, se aplicará el artículo 15 del Convenio de La Haya de 15 de noviembre de 1965 relativo a la notificación o traslado en el extranjero de documentos judiciales y extrajudiciales en materia civil o comercial, si el escrito de demanda o documento equivalente hubiera de transmitirse al extranjero de acuerdo con dicho Convenio".

Segundo.- En aplicación de esta normativa, deberá este Tribunal, de Oficio, proceder a la inmediata suspensión del procedimiento, así como de los plazos inherentes a su tramitación, y comprobar su competencia judicial internacional con efecto suspensivo del curso de los presentes autos.

PARTE DISPOSITIVA

Se acuerda la suspensión del procedimiento de demanda de juicio [Nº DE PROCEDIMIENTO] promovido por [NOMBRE DE LA PARTE] contra [ACTO O RESOLUCIÓN] hasta tanto se verifique la validez de la notificación de la demanda y el emplazamiento al demandado; y, con su resultado, se acordará.

Lo acuerda y firma S.Sª.; doy fe.

El/la MAGISTRADO-JUEZ El/la LETRADO DE LA ADMINISTRACIÓN DE JUSTICIA

========================================================================
