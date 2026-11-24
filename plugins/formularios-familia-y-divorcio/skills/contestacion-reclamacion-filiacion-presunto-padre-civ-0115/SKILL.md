---
name: contestacion-reclamacion-filiacion-presunto-padre-civ-0115
description: "Contestación a la reclamación de filiación del presunto padre con impugnación de la contradictoria. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contestación a la reclamación de filiación del presunto padre con impugnación de la contradictoria

> Formulario **CIV-0115** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contestación a la reclamación de filiación del presunto padre con impugnación de la contradictoria» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contestación a la reclamación de filiación del presunto padre con impugnación de la contradictoria” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:contestacion-reclamacion-filiacion-presunto-padre-civ-0115`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (11 veces)
- [ ] DNI/NIE (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] AÑO
- [ ] CALLE
- [ ] COLEGIO
- [ ] DÍA
- [ ] MES
- [ ] NOMBRE DEL MENOR
- [ ] Nº
- [ ] Nº DE DOCUMENTO
- [ ] NÚMERO
- [ ] SEDE

## Normas que cita el formulario

- art. 50 LEC
- art. 133 CC
- art. 749 LEC
- art. 767.1 LEC
- art. 753 Ley 1/2000

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

- Junto a «…CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE] PLAZA Nº [NÚMERO]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE] PLAZA Nº [NÚMERO]

D./Dña [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales en nombre y representación de D [NOMBRE Y APELLIDOS] y Dña, [NOMBRE Y APELLIDOS] mayores de edad, casados, con DNI [DNI/NIE] y DIN [DNI/NIE], y domicilio a efectos de notificaciones en la calle [CALLE] sita en [LOCALIDAD], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], bajo la dirección técnica de D./Dña [NOMBRE Y APELLIDOS] Abogado/a del Ilustre Colegio de Abogados de [COLEGIO], Colegiado núm. [Nº], ante este Tribunal comparezco y, como mejor proceda en Derecho y

DIGO

Que mediante el presente escrito y siguiendo instrucciones de mi mandante formulo contestación a la demanda de reclamación de filiación paterna no matrimonial planteada de contrario por D. [NOMBRE Y APELLIDOS], e impugnación de la filiación contradictora contra mi mandante D. [NOMBRE Y APELLIDOS], quien hasta ahora ha actuado en calidad de padre del demandante y así figura en el Registro civil, que baso en los siguientes

HECHOS

Conforme esta parte con lo que se describe en la demanda en este apartado.

Disconforme esta parte con lo que se describe en la demanda por cuanto si bien es cierto que el demandante D. y Dña. coincidieron en el marco del Congreso de Medicina que se celebró en Valencia en junio de 2009, falta a la verdad que hubo algo más entre ellos que una relación de amistad sin más, no habiéndose producido los encuentros sexuales que refiere D. [NOMBRE Y APELLIDOS] en su demanda.

Disconforme por cuanto para poder quedar embarazada Dña. precisó en septiembre de 2009 de un proceso de estimulación ovárica y posterior inseminación artificial homóloga de quien hoy es su marido, como prueba el certificado médico que se aporta como documento núm.1 En consecuencia, no pudo quedarse embarazada tres meses antes como argumenta el demandante, por cuanto hubiera sido imposible que le practicaran este tipo de técnicas.

A estos hechos, son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

Competencia jurisdiccional

De acuerdo con los artículos que se refieren y que determinan como Juez competente el del domicilio del demandado, según el art. 50 LEC.

Legitimación de las partes

Conforme con lo determinado respecto a la legitimación activa y pasiva en este proceso, acreditada por los arts. 133 y 134 CC y por los arts. 749 y 766 LEC.

Derecho sustantivo

Asiste a mi mandante para oponerse a la reclamación de paternidad e impugnar la suya el juego de las presunciones de paternidad referidas en los arts. 116 y ss del Código civil. A mayor abundamiento, atendida la falta en la demanda formulada de contrario del principio de prueba básico exigible en toda acción dirigida a la determinación y/o impugnación de filiación, de conformidad con lo dispuesto en el art. 767.1 LEC, y el comportamiento desplegado por mi mandante respecto del actor de la demanda como a su hijo biológico que considera, debiera hacerse decaer el derecho de la parte demandante, máxime cuando además obra inscrita en el Registro civil la filiación de D. a favor de mi representado.

Procedimiento

Conforme con lo establecido respecto del procedimiento por el que se sustanciarán este tipo de proceso, como es el verbal de conformidad con el artículo 753 de la Ley 1/2000, de 7 de enero, de Enjuiciamiento Civil y el art. 405 de la misma respecto de la contestación de la demanda. Igualmente esta parte se muestra confrme posible imputar las costas derivadas del mismo de acuerdo con lo previsto en el artículo 394 de la citada Ley al demandante.

Por todo lo cual,

SUPLICO AL TRIBUNAL: Que tenga por presentado este escrito de contestación a la demanda así como los documentos que lo acompañan y copias de todo ello y se sirva admitirlo, teniéndome por parte en la representación acreditada, y por formulada CONTESTACIÓN A LA DEMANDA de reclamación de filiación no matrimonial de D. [NOMBRE Y APELLIDOS] contra Dña [NOMBRE Y APELLIDOS] y D [NOMBRE Y APELLIDOS] e impugnación de filiación contradictoria contra D. [NOMBRE Y APELLIDOS] y en tal sentido dicte, en su día, previo los trámites legales oportunos y la práctica de pruebas que considere pertinentes, sentencia por la que prevalezca la filiación formalmente determinada y acuerde declarar que mis mandantes son los progenitores de [NOMBRE DEL MENOR] y consiguientemente válida la filiación paterna que consta en el asiento de inscripción del nacimiento, y se desestime la demanda mandando en su día que se practiquen cuantas inscripciones se consideren oportunas en el Registro Civil para reflejar cuanto se ha acordado judicialmente; e imponga por último las costas que del procedimiento se deriven al demandante.

Es justicia que pido en la Ciudad de [LOCALIDAD] a [DÍA] de [MES] de [AÑO]

Fdo. Procurador/a	Fdo. Letrado/a
D./Dña D./Dña

========================================================================
