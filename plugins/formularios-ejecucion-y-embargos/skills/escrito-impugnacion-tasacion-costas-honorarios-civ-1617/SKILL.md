---
name: escrito-impugnacion-tasacion-costas-honorarios-civ-1617
description: "Escrito de impugnación de la tasación de costas por honorarios indebidos. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito de impugnación de la tasación de costas por honorarios indebidos

> Formulario **CIV-1617** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Escrito impugnando la tasación de costas practicada por considerar indebidamente incluidos los honorarios del Letrado/a.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito de impugnación de la tasación de costas por honorarios indebidos» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito de impugnación de la tasación de costas por honorarios indebidos” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:escrito-impugnacion-tasacion-costas-honorarios-civ-1617`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (5 veces)
- [ ] NOMBRE DE LA PARTE (5 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] IMPORTE (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] IMPORTE EN CIFRA
- [ ] LUGAR
- [ ] Nº DE PROCEDIMIENTO
- [ ] NÚMERO
- [ ] SEDE

## Normas que cita el formulario

- art. 244.1 LEC
- art. 1.138 CC

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

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, que actúa en nombre y representación de [NOMBRE DEL REPRESENTADO/A], según consta acreditado en los autos de Juicio Ordinario [Nº DE PROCEDIMIENTO] seguidos con el número [NÚMERO] a instancias de D./Dña. [NOMBRE Y APELLIDOS] contra mi representada y [NOMBRE DE LA PARTE], ante el Tribunal comparezco y como mejor proceda en Derecho, digo:

Que se ha dado vista a esta parte de la tasación de costas practicada por la Sra. Letrado/a de la Administración de Justicia en estos autos con fecha [FECHA], y dentro del término establecido en el art. 244.1 LEC, impugno por el presente la misma por considerar indebidamente incluidos los honorarios del Letrado/a D./Dña. [NOMBRE Y APELLIDOS], conforme a lo previsto en el art. 245.2 de dicha Ley Adjetiva. Y ello en base a los siguientes:

HECHOS

PRIMERO

Mi mandante resulta deudora de la obligación del pago de las costas procesales a que se le condenó en sentencia de [FECHA], junto con [NOMBRE DE LA PARTE], pero ha cumplido voluntariamente el fallo.

YY, S.L. es además deudora del pago de las costas que se han ocasionado en las diligencias para el cumplimiento de la ejecutoria, habiéndose despachado la ejecución de la deuda pecuniaria no satisfecha en providencia de [FECHA], y practicada diligencia de embargo —al fin suspendida— el día [FECHA] siguiente.

Ello es posible porque hay una condena dineraria líquida principal que es solidaria para mi representada e [NOMBRE DE LA PARTE], la que se ha pagado, y otra de [IMPORTE] euros, que sólo afecta a esa última sociedad.

SEGUNDO

La condena en costas —ilíquida— no discriminaba, puesto que se imponía a la parte demandada (cualesquier número de litigantes siempre harán dos posiciones procesales, y una es la de parte demandada), y aunque el débito principal es solidario, el derivado por costas no se especificaba que lo fuera, por lo que mi representada [NOMBRE DEL REPRESENTADO/A] no debe más que el 50% de los honorarios del Letrado/a de la contraparte D./Dña. [NOMBRE Y APELLIDOS]

TERCERO

En todo caso, [NOMBRE DE LA PARTE] no debe las costas tasadas por la ejecución, ya que la sentencia ha tenido que ejecutarse por no haberse cumplido voluntariamente por [NOMBRE DE LA PARTE] en su porción de deuda no solidarizada con la primera.

FUNDAMENTOS DE DERECHO

I

Art. 246.4 LEC, para su tramitación por el procedimiento señalado de audiencia a la otra parte por tres días, y resolución por el Letrado/a de la Administración de Justicia judicial en tres días mediante decreto.

II

Art. 539.2 II LEC, conforme al que las costas de la ejecución proceden de la norma, sin precisión de expresa condena en la resolución judicial, siendo que no media ejecución respecto de mi mandante, que ha cumplido pacíficamente con su obligación.

III

El art. 1.138 CCiv, según el que nuestro Derecho de obligaciones presume la mancomunidad de obligaciones, siendo que la solidaridad, también en el campo de las costas, tiene que especificarse.

IV

El art. 243.2 párrafo 1.º LEC, que relaciona entre las partidas que no debe incluir el Letrado/a de la Administración de Justicia judicial los derechos correspondientes a escritos o actuaciones no autorizadas por la Ley, u honorarios que no se hayan devengado en el pleito.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito, lo admita y una a los autos, teniendo por impugnada la tasación de costas practicada en estos autos por concepto de INDEBIDA la inclusión de los honorarios del Letrado/a D./Dña. [NOMBRE Y APELLIDOS], en lo que excedan del cincuenta por ciento de los correspondientes a la fase declarativa, y previos los trámites oportunos, se dicte decreto que estime la impugnación y reduzca la partida, aprobando la tasación reducida a la cantidad resultante de [IMPORTE] euros ([IMPORTE EN CIFRA] €), con expresa condena en costas del incidente a la parte que se oponga.

Es justicia de hacerse en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
