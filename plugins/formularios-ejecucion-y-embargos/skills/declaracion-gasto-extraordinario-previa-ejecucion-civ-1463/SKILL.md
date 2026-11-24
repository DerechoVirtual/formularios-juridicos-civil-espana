---
name: declaracion-gasto-extraordinario-previa-ejecucion-civ-1463
description: "Declaración de gasto extraordinario previa a la ejecución por el carné de ciclomotor del hijo. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Declaración de gasto extraordinario previa a la ejecución por el carné de ciclomotor del hijo

> Formulario **CIV-1463** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Declaración de gasto extraordinario previa a la ejecución por el carné de ciclomotor del hijo» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Declaración de gasto extraordinario previa a la ejecución por el carné de ciclomotor del hijo” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:declaracion-gasto-extraordinario-previa-ejecucion-civ-1463`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (4 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] AÑO
- [ ] CALLE
- [ ] COLEGIO
- [ ] DÍA
- [ ] LUGAR
- [ ] MES
- [ ] NOMBRE DEL CENTRO
- [ ] NOMBRE DEL HIJO
- [ ] NÚMERO
- [ ] NÚMERO DE LA CALLE

## Normas que cita el formulario

- art. 776.4 LEC

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

- Junto a «…ontencioso: / A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA NÚMERO DE [LOCALIDAD]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

Antecedentes:

Sección Civil del Tribunal de Instancia Número [NÚMERO] De [LOCALIDAD]

Procedimiento de divorcio/separación de mutuo acuerdo/contencioso: /

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA NÚMERO DE [LOCALIDAD]

D./Dª [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en nombre y representación de D./Dª [NOMBRE Y APELLIDOS], cuya representación acredito mediante escritura de poder que acompaño, comparezco en este TRIBUNAL y como mejor proceda en Derecho DIGO:

Que mediante el presente escrito, y con la asistencia del Letrado D./Dª [NOMBRE Y APELLIDOS], del Ilustre Colegio de Abogados de [COLEGIO], al amparo de lo previsto en el artículo 776.4 de la LEC solicito sea declarado gasto extraordinario, a los efectos de su posterior ejecución forzosa, el derivado de la obtención del carné de conducir ciclomotores que ha tenido que obtener el hijo de mi mandante (o el gasto que proceda), debiendo entenderse dicha solicitud con su progenitor D./Dª [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], calle [CALLE], nº [NÚMERO DE LA CALLE]

Basamos la solicitud en las siguientes:

ALEGACIONES

En la sentencia recaída en los autos de divorcio de referencia se acordaba que los gastos extraordinarios serían abonados por ambos progenitores por mitad. Ahora bien, no se especificaba que gastos debían de ostentar tal naturaleza.

Adjunto aportamos como DOCUMENTO NÚM. UNO copia testimoniada de la sentencia.

El hijo del matrimonio [NOMBRE DEL HIJO], de 17 años de edad, cursa estudios de primero de bachiller en el colegio [NOMBRE DEL CENTRO], siendo que el domicilio del progenitor custodio, mi mandante, se encuentra en la localidad de [LOCALIDAD], que carece de transporte público que permita al menor desplazarse a diario al centro escolar, sin que pueda acompañarlo su madre dado su horario laboral.

Por tal motivo, el menor se ha visto en la necesidad de obtener el carné de conducir ciclomotores que en conjunto, incluida la matrícula, prácticas y derechos de examen ha ascendido a un gasto de 457 €, tal y como acreditamos mediante DOCUMENTOS NÚMS. DOS al CINCO adjuntos.

Se considera gastos extraordinarios a aquellos que no tienen periodicidad prefijada, en cuanto dimanantes de sucesos de difícil e imposible previsión apriorística, de tal modo que los mismos pueden seguir o no, habiendo de ser vinculados a necesidades que han de cubrirse económicamente de modo ineludible, en orden al cuidado, desarrollo y formación, en todos los órdenes del alimentista, y ello en contraposición al concepto de lo superfluo o secundario, de lo que, obviamente, puede prescindirse, sin menoscabo para el alimentista. En definitiva, los gastos extraordinarios comprenden aquellas sumas destinadas a atender las necesidades de los menores que por su carácter imprevisto no pueden ser satisfechos con el importe ordinario de la pensión de alimentos (SS. A.P de Madrid, Sección 22, de 18 de octubre de 2007, rec. 384/2007 y A.P de Sevilla, Sección 2ª, de 18 de febrero de 2008, rec. 4246/2007, entre otras muchas).

El artículo 776.4 de la LEC dispone que cuando deban ser objeto de ejecución forzosa gastos extraordinarios, no expresamente previstos en las medidas definitivas o provisionales, deberá solicitarse previamente al despacho de ejecución la declaración de que la cantidad reclamada tiene la consideración de gasto extraordinario. Del escrito solicitando la declaración de gasto extraordinario se dará vista a la contraria y, en caso de oposición dentro de los cinco días siguientes, el Tribunal convocará a las partes a una vista que se sustanciará con arreglo a lo dispuesto en los arts. 440 y siguientes y que resolverá mediante auto.

Por lo expuesto:

SUPLICO AL TRIBUNAL tenga por presentado este escrito junto con los documentos que se acompañan, lo admita, y en su mérito y previo traslado a la contraparte y al Ministerio Fiscal por cinco días para oposición, si no se opone, o, de oponerse, tras la celebración de la preceptiva comparecencia, se dicte auto por el que se declare que los gastos producidos como consecuencia de la obtención del carné de conducir ciclomotores por parte del hijo del matrimonio, tiene la naturaleza de gasto extraordinaio.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma y número del Letrado	Firma del Procurador

========================================================================
