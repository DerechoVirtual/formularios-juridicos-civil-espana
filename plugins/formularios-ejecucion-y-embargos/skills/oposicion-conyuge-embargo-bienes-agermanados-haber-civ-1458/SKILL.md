---
name: oposicion-conyuge-embargo-bienes-agermanados-haber-civ-1458
description: "Oposición del cónyuge al embargo de bienes agermanados por haber bienes privativos suficientes. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Oposición del cónyuge al embargo de bienes agermanados por haber bienes privativos suficientes

> Formulario **CIV-1458** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Oposición del cónyuge al embargo de bienes agermanados por haber bienes privativos suficientes» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Oposición del cónyuge al embargo de bienes agermanados por haber bienes privativos suficientes” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:oposicion-conyuge-embargo-bienes-agermanados-haber-civ-1458`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] AÑO (3 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] DÍA (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] MES (2 veces)
- [ ] CALLE
- [ ] COLEGIO
- [ ] DESCRIPCIÓN DE LOS DOCUMENTOS
- [ ] LUGAR
- [ ] Nº
- [ ] NÚMERO

## Normas que cita el formulario

- art. 1373 CC
- art. 541.3 LEC
- art. 562.1.3 LEC
- art. 541.4 LEC

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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…CIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA NÚMERO DE [LOCALIDAD]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.

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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA NÚMERO DE [LOCALIDAD]

D./Dª [NOMBRE Y APELLIDOS], Procurador de los Tribunales y de D./Dª [NOMBRE Y APELLIDOS], cuya representación acreditará cuando sea requerido para ello mediante comparecencia apud acta (o bien: representación que acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño a la presente), bajo la dirección técnica de D./Dª [NOMBRE Y APELLIDOS], Letrado del Ilustre Colegio de [COLEGIO], con despacho profesional en [LOCALIDAD], calle [CALLE], nº [NÚMERO], pta., ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que por medio del presente escrito, siguiendo instrucciones de mi representado/a, me OPONGO, en tiempo y forma, AL EMBARGO DE BIENES AGERMANADOS decretado en el procedimiento de Ejecución de Título Judicial o título ejecutivo que corresponda nº cónyuge de mi representado/a, por infracción de los arts. 1373 CC, aplicable por analogía, y 541.3 LEC, en el sentido de que se sustituya el embargo de tales bienes por el de los bienes privativos del deudor ejecutado, suficientes para cubrir la deuda, que luego se dirá./, seguido contra D./Dª [NOMBRE Y APELLIDOS],

Esta pretensión se basa en los siguientes

HECHOS

Por auto de fecha [DÍA] de [MES] de [AÑO] se le notificó a mi representado/a el embargo de bienes agermanados trabado en el procedimiento de Ejecución de Título Judicial o título ejecutivo que corresponda nº [Nº]/[AÑO], seguido contra su cónyuge, D./Dª [NOMBRE Y APELLIDOS], por deuda particular o privativa del mismo, dándole un plazo de diez días para que, en su caso, pudiera oponerse a la ejecución y solicitar la disolución de la sociedad conyugal en los términos y a los efectos establecidos en el art. 1373 CC, aplicable como Derecho supletorio a la germanía, en relación con el art. 541.3 LEC.

Sin embargo, no es necesario proceder a tal disolución por existir bienes privativos del deudor suficientes para satisfacer al acreedor, como a continuación se expone.

En virtud de estos preceptos, cuando la ejecución se sigue por deudas particulares o privativas de un cónyuge sólo pueden embargarse bienes agermanados con carácter subsidiario, ante la falta o insuficiencia de bienes privativos del cónyuge deudor.

Así pues, cuando al cónyuge del deudor se le notifique el embargo de bienes comunes por deudas particulares de su consorte éste puede señalar bienes privativos del deudor suficientes para satisfacer el crédito, en cuyo caso, deberá alzarse el embargo trabado sobre los bienes comunes.

El requisito de la subsidiariedad no se ha respetado en el presente caso, pues el deudor ejecutado cuenta con los siguientes bienes privativos cuyo valor basta para cubrir la deuda: Por ello, procede alzar el embargo practicado sobre los bienes agermanados y sustituirlo por el de los citados bienes privativos del deudor.

Se acompañan como Documentos nº [Nº DE DOCUMENTO], [Nº DE DOCUMENTO] y [Nº DE DOCUMENTO] los siguientes: [DESCRIPCIÓN DE LOS DOCUMENTOS], con el fin de justificar la titularidad privativa del ejecutado sobre los citados bienes y que su valor estimado es suficiente para cubrir la deuda ejecutada en relación con este último punto, puede incluirse informe de perito tasador.

Resultan aplicables a los anteriores hechos, los siguientes

FUNDAMENTOS DE DERECHO

LEGITIMACIÓN.- El art. 541.3 LEC obliga a notificar al cónyuge del deudor ejecutado el embargo de bienes gananciales cuando la ejecución se siga a causa de deudas propias o privativas del ejecutado, contemplando expresamente que en este caso, sólo pueden perseguirse bienes comunes a falta o por insuficiencia de los bienes privativos del deudor, en concordancia con el régimen sustantivo del art. 1373 CC.

Aunque tales preceptos se refieren expresamente a la ejecución en bienes gananciales, resultan aplicables, por analogía a la germanía.

Por su parte, el art. 562.1.3º LEC, señala que, con independencia de la oposición a la ejecución por el ejecutado según lo dispuesto en los artículos anteriores, todas las personas a que se refiere el artículo 538, entre las que debe entenderse incluido el cónyuge del ejecutado cuando se embargan bienes comunes, de los que aquél es cotitular, incluidos los agermanados, podrán denunciar la infracción de normas que regulen los actos concretos del proceso de ejecución. En el presente caso se ha conculcado la norma de los arts. 1373 CC y 541 LEC.

Finalmente, el art. 541.4 LEC, establece expresamente que "el cónyuge al que se haya notificado el embargo podrá interponer los recursos y usar de los medios de impugnación de que dispone el ejecutado para la defensa de los intereses de la comunidad de gananciales", resultando esta norma igualmente aplicable a la germanía por las razones ya expuestas.

DERECHO SUSTANTIVO.- El art. 1373 CC, en relación con el art. 541.3 LEC, en los que se establece el carácter subsidiario, en defecto de bienes privativos del deudor suficientes para hacer efectiva la deuda, de la responsabilidad con bienes comunes por deudas propias o privativas del cónyuge deudor.

Iura novit curia, y cuantas normas resulten procedentes.

En su virtud,

SUPLICO AL TRIBUNAL: Que teniendo por presentado este escrito en tiempo y forma, con los documentos que lo acompañan y el justificante de haber dado traslado de todo ello al Procurador de las partes ejecutante y ejecutada, se sirva admitirlo, y, previos los trámites legales oportunos, estime la pretensión ejercitada y dicte resolución por la que acuerde alzar el embargo del/de los bien/es agermanado/s trabados, sustituyéndolo por el del/de los bien/bienes privativos del ejecutado señalados en el cuerpo del escrito.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma y número del Letrado	Firma del Procurador

========================================================================
