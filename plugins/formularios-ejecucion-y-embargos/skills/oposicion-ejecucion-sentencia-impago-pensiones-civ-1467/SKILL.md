---
name: oposicion-ejecucion-sentencia-impago-pensiones-civ-1467
description: "Oposición a la ejecución de sentencia por impago de pensiones alegando el pago de lo reclamado. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Oposición a la ejecución de sentencia por impago de pensiones alegando el pago de lo reclamado

> Formulario **CIV-1467** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Oposición a la ejecución de sentencia por impago de pensiones alegando el pago de lo reclamado» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Oposición a la ejecución de sentencia por impago de pensiones alegando el pago de lo reclamado” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:oposicion-ejecucion-sentencia-impago-pensiones-civ-1467`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (6 veces)
- [ ] AÑO (5 veces)
- [ ] MES (4 veces)
- [ ] DÍA (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] Nº (2 veces)
- [ ] COLEGIO
- [ ] FECHA
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] Nº DE DOCUMENTO
- [ ] Nº DE PROCEDIMIENTO
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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).
- Junto a «…cedimiento: / A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA NÚMERO DE [LOCALIDAD]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº]

Procedimiento: /

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA NÚMERO DE [LOCALIDAD]

D./Dª [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en nombre y representación de D./Dª [NOMBRE Y APELLIDOS], representación que se encuentra acreditada en autos, bajo la dirección técnica de D./Dª [NOMBRE Y APELLIDOS], Letrado del Ilustre Colegio de Abogados de [COLEGIO], ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que por medio del presente escrito FORMULO OPOSICIÓN A LA EJECUCIÓN despachada contra mi representado/a en autos de ejecución núm. [Nº], por defectos formales y de fondo, con base en los siguientes

HECHOS

La SENTENCIA DE SEPARACIÓN (O DE DIVORCIO, O DICTADA EN JUICIO AUTÓNOMO DE ALIMENTOS, etc.), de fecha [DÍA] de [MES] de [AÑO], recaída en los autos nº [Nº DE PROCEDIMIENTO]/[AÑO] del Tribunal a que me dirijo, en la que se basa la demanda ejecutiva interpuesta contra mi representado, estableció la obligación de éste de abonar la suma de [IMPORTE] EUROS CON [IMPORTE] CÉNTIMOS DE EURO MENSUALES ( €) en concepto de pensión de alimentos (o de pensión compensatoria).

En la demanda de ejecución se reclama, en concepto de pensión de alimentos (o de pensión compensatoria), la suma de [IMPORTE] euros ( €) de principal más otros [IMPORTE] euros ( €) para intereses vencidos y otros [IMPORTE] euros ( €) para intereses presupuestados y costas de la ejecución; sin perjuicio de ampliar la ejecución a las mensualidades que vayan venciendo durante la substanciación del procedimiento y que no atienda mi representado.

[ELEGIR UNA OPCIÓN: Motivos de la oposición / Pago de la pensión / Pago de la matrícula]

Se acompañan los siguientes DOCUMENTOS para acreditar los hechos expuestos:

FUNDAMENTOS DE DERECHO

Es competente el Tribunal al que me dirijo a tenor de lo dispuesto en el artículo 545.1 de la Ley de Enjuiciamiento Civil.

La oposición ejercitada se funda en el art. 556.1 de la Ley de Enjuiciamiento Civil, de acuerdo con el cual: "Si el título ejecutivo fuera una resolución procesal o arbitral de condena o un acuerdo de mediación, el ejecutado, dentro de los diez días siguientes a la notificación del auto en que se despache ejecución, podrá oponerse a ella por escrito alegando el pago o cumplimiento de lo ordenado en la sentencia, laudo o acuerdo, que habrá de justificar documentalmente.

También se podrá oponer la caducidad de la acción ejecutiva, y los pactos y transacciones que se hubiesen convenido para evitar la ejecución, siempre que dichos pactos y transacciones consten en documento público."

No obsta a la oposición de mi representado, por no ser requisito al que aluda el citado precepto, que el pago no se haya efectuado en la cuenta corriente señalada al efecto en la sentencia cuya ejecución se pretende.

Debe considerarse como pago de la pensión de alimentos (o compensatoria) los pagos que, de acuerdo con el/la demandante, haya realizado mi representado/a directamente a terceros, de cantidades debidas por la manutención o educación de los hijos (o debidas por el/la demandante), siendo abusivo y contrario a la buena fe y también contrario a los propios actos, desde el momento en que aquél/aquélla prestó su consentimiento, pretender lo contrario.

Pueden citarse, en este sentido, las siguientes sentencias de diferentes audiencias provinciales:

Conforme a los artículos 241 y 539.2 de la Ley de Enjuiciamiento Civil, procede la condena en costas de ejecución a la parte ejecutante.

"Iura novit curia", y cuantos otros resulten de aplicación.

En su virtud:

SUPLICO AL TRIBUNAL: Que teniendo por presentado este escrito, con los documentos que se acompañan, y copia de todo ello, se sirva admitirlo, teniendo al procurador que suscribe por comparecido y parte en la representación que ostenta y consta acreditada, y por interpuesta OPOSICIÓN A LA EJECUCIÓN DE LA SENTENCIA DE FECHA [FECHA] DE [MES] DE [AÑO] DESPACHADA contra mi representado por resolución de fecha [DÍA] de [MES] de [AÑO], y previos los trámites legales oportunos, dicte Auto dejando sin efecto la misma y alzando el embargo, con condena en costas al/a la demandante.

OTROSÍ DIGO.-Que estando el presente escrito de oposición a la ejecución de títulos judiciales sujeto al abono de la tasa por el ejercicio de la potestad jurisdiccional fijada por la Ley 10/2012, de 20 de noviembre, modificada por Real Decreto Ley 3/2013, de 22 de febrero, y desarrollada por Orden HAP/2662/2012, de 13 de diciembre, modificada por Orden HAP/490/2013, de 27 de marzo, se acompaña a la presente demanda como documento nº [Nº DE DOCUMENTO] la correspondiente autoliquidación con el ejemplar para la Administración de Justicia debidamente validado y en el que consta el pago de la cantidad de 200 euros correspondiente a la cuota fija, más la cantidad de [IMPORTE] euros por la aplicación a la base imponible de la escala prevista en el artículo 7.3 de la citada Ley (caso de personas jurídicas, en el artículo 7.2 de la citada Ley; en su caso, fijando la base a estos efectos en la cantidad de dieciocho mil euros al ser la cuantía indeterminada o de imposible determinación conforme a las reglas de la LEC; en su caso, aplicando la bonificación del 10% por el uso de medios telemáticos).

En virtud de lo anterior,

SUPLICO AL TRIBUNAL que tenga por hecha la anterior manifestación a los efectos pertinentes y por acompañado el documento justificativo del abono de la tasa.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma y número del Letrado	Firma del Procurador

========================================================================
