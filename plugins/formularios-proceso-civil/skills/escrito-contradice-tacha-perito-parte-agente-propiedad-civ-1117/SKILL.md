---
name: escrito-contradice-tacha-perito-parte-agente-propiedad-civ-1117
description: "Escrito que contradice la tacha de un perito de parte (agente de la propiedad inmobiliaria). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito que contradice la tacha de un perito de parte (agente de la propiedad inmobiliaria)

> Formulario **CIV-1117** del plugin **Proceso civil: demandas, contestaciones, prueba y vista** (`formularios-proceso-civil`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 24-11-2026.

## Qué es

Escrito, dirigido al Tribunal de Instancia, por el que el demandado en un juicio ordinario contradice o niega la tacha de un perito (Agente de la Propiedad Inmobiliaria).

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito que contradice la tacha de un perito de parte (agente de la propiedad inmobiliaria)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito que contradice la tacha de un perito de parte (agente de la propiedad inmobiliaria)” para mi caso». También puedes invocarla directamente con `/formularios-proceso-civil:escrito-contradice-tacha-perito-parte-agente-propiedad-civ-1117`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-proceso-civil:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso civil: demandas, contestaciones, prueba y vista) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] FECHA (3 veces)
- [ ] AÑO
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] Nº DE PROCEDIMIENTO
- [ ] SEDE

## Normas que cita el formulario

- art. 343.2 LEC
- art. 344.2 LEC
- art. 276 LEC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, representante procesal de D./Dña. [NOMBRE Y APELLIDOS], demandado en el Juicio Ordinario n.º [Nº DE PROCEDIMIENTO]/[AÑO], ante el Tribunal comparezco, y como mejor en Derecho proceda, DIGO:

Que por medio del presente escrito, vengo a contradecir la tacha del perito D./Dña. [NOMBRE Y APELLIDOS], con base en las siguientes:

ALEGACIONES

PRIMERA.- El perito D./Dña. [NOMBRE Y APELLIDOS], Agente de la Propiedad Inmobiliaria de [LOCALIDAD], emitió dictamen por escrito que se acompañó con el escrito de contestación, para oponer prueba de hechos enfrentados a los de la demanda, que también venía acompañada de dictamen pericial de otro Agente.

Por consiguiente, según dispone el art. 343.2 LEC, como se trata de un juicio ordinario, la tacha del perito autor de dictamen aportado con la contestación a la demanda, debió proponerse en la audiencia previa al juicio, que se celebró el pasado día [FECHA], de modo que la formulada después resulta extemporánea y rechazable.

SEGUNDA.- El [FECHA], ciertamente D./Dña. [NOMBRE Y APELLIDOS] parece que se encontró con la actora D./Dña. [NOMBRE Y APELLIDOS], a la que conocía, y tuvieron un intercambio de pareceres a propósito de la valoración del inmueble que es objeto del pleito, pero ni se dijo lo que asevera el escrito de la tacha, ni tal cosa es cierta en absoluto, habida cuenta que el dicho perito nunca ha parlamentado con el Letrado suscrito, y más bien fue la actora la que indujo al perito a deslizarse en opiniones sobre los dictámenes de autos.

TERCERA.- La prueba que puede justificar una tacha de perito no cabe sea testifical, según indica el art. 343.2 "in fine" LEC, dado que se neutralizaría entonces una prueba de índole técnico por el sencillo expediente de reclutar un testigo adverso, siendo ya irremediable la duda valorativa.

Y la prueba documental pública que se propone con el escrito de tacha constituye ruidosamente una testifical preconstituida, además sin las garantías de contradicción e inmediación judicial necesarias, puesto que se trata de un acta notarial de comparecencia y manifestación, que ha de verse privada de efecto alguno.

CUARTA.- La ausencia de veracidad en la tacha, su extemporaneidad, y el temerario intento de probarla con testigos, hace acreedora a la parte actora de una severa multa, conforme al art. 344.2 LEC.

Por lo expuesto,

AL TRIBUNAL SUPLICO

que, teniendo por presentado este escrito, junto con recibo de haberse realizado el traslado que impera el art. 276 LEC a la representación procesal de la contraparte, se digne admitirlo, y por causadas las manifestaciones antecedentes, se tenga por negada o contradicha la tacha del perito D./Dña. [NOMBRE Y APELLIDOS], de modo que se prescinda de la misma en el momento de valorar la prueba, imponiéndose por ello a la parte actora, previa audiencia, la multa que determine S.Sª.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
