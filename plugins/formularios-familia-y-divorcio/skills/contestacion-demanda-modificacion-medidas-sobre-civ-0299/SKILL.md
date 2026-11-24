---
name: contestacion-demanda-modificacion-medidas-sobre-civ-0299
description: "Contestación a la demanda de modificación de medidas sobre aumento de gastos de los hijos. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contestación a la demanda de modificación de medidas sobre aumento de gastos de los hijos

> Formulario **CIV-0299** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Escrito de contestación a la demanda de modificación de medidas definitivas en relación con la solicitud del incremento de la cuantía de los gastos derivados de actividades escolares y extraescolares.

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contestación a la demanda de modificación de medidas sobre aumento de gastos de los hijos» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contestación a la demanda de modificación de medidas sobre aumento de gastos de los hijos” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:contestacion-demanda-modificacion-medidas-sobre-civ-0299`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] AÑO (5 veces)
- [ ] NOMBRE DEL CENTRO (3 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] FECHA (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] CALLE
- [ ] COLEGIO
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] NOMBRE DEL MENOR
- [ ] SEDE

## Normas que cita el formulario

- art. 90 CC
- art. 394 LEC

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

- Junto a «…MILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, que actúa en nombre y representación de D. [NOMBRE Y APELLIDOS], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], bajo la dirección del/la Letrado/a D./Dña. [NOMBRE Y APELLIDOS], colegiado/a n.º [NÚMERO] del Iltre. Colegio de Abogados de [COLEGIO], con despacho abierto en [LOCALIDAD], calle [CALLE], en autos de incidente de modificación de medidas definitivas de separación n.º [NÚMERO]/[AÑO], promovido por Dña. [NOMBRE Y APELLIDOS], ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que, en la representación que ostento y dentro del plazo legal, vengo a CONTESTAR A LA DEMANDA DE MODIFICACIÓN DE MEDIDAS DEFINITIVAS de la sentencia de separación de fecha [FECHA] dictada por ese Tribunal interpuesta contra mi mandante por Dña. [NOMBRE Y APELLIDOS], en base a los siguientes hechos y consideraciones jurídicas:

HECHOS

PRIMERO.- Nada objeta esta representación en lo relativo a la relación fáctica desarrollada de adverso.

SEGUNDO.- No podemos sino contradecir las afirmaciones formuladas en el correlativo de la demanda, en cuanto se alega de contrario que se ha producido una modificación sustancial de las circunstancias tenidas en cuenta a la hora de adoptar las medidas definitivas en la sentencia de separación, concretamente que el/la hijo/a menor [NOMBRE DEL MENOR] ha crecido y con ello sus necesidades económicas derivadas de sus estudios, particularmente los gastos derivados de actividades escolares y extraescolares.

Los gastos que se relacionan no son diferentes a los que por conceptos similares se devengaban en el momento de acordarse las medidas en la sentencia de separación y que, por lo tanto, fueron tenidos en cuenta, toda vez que la menor acude el presente curso escolar al Colegio público [NOMBRE DEL CENTRO], por el que no tiene que abonar prestación alguna, a diferencia de cuando acudía a la escuela infantil-guardería [NOMBRE DEL CENTRO], y obteniendo el montante producido por las cantidades abonadas en concepto de pago por asistencia a la citada guardería infantil privada cabe señalar que es incluso superior al producido en la actualidad por los dichos gastos derivados de la educación de la menor al margen de la enseñanza reglada gratuita.

Se adjuntan recibos de pagos efectuados a la guardería [NOMBRE DEL CENTRO] en los años [AÑO] como documentos números [Nº DE DOCUMENTO]

TERCERO.- Absolutamente incierto. Por más que se empeñe la demandante, no se ha producido un incremento de la capacidad económica del esposo en relación a la tenida en consideración en la sentencia de separación.

En efecto, en ella se partía de unos beneficios obtenidos por el marido en el año [AÑO] de [IMPORTE] euros y en el año [AÑO] ha declarado a la Hacienda unos ingresos netos de [IMPORTE] euros, sin que pueda tenerse en consideración la adquisición de un vehículo, pues éste es de segunda mano y D. lo precisa para el desarrollo de su trabajo como representante comercial.

Dicho extremo se acredita mediante declaración del IRPF presentada por el Sr. [NOMBRE Y APELLIDOS] para el ejercicio fiscal [AÑO], que se aporta como documento número [Nº DE DOCUMENTO]

FUNDAMENTOS DE DERECHO

Conforme con los fundamentos jurídicos I a VI del escrito de demanda.

VII.- FONDO DEL ASUNTO

Los arts. 90 y 91 del CC establecen que las medidas subsiguientes a la separación o al divorcio convenidas entre los cónyuges y las adoptadas judicialmente en defecto de convenio o de la no aprobación del mismo podrán ser modificadas cuando se alteren sustancialmente las circunstancias tenidas en consideración. Para que esta alteración tenga eficacia es preciso que el cambio sea sustancial o esencial, no secundaria o accesoria, y que goce de una cierta permanencia en el tiempo, lo que impide que sea reconocido en los casos de modificaciones temporales o transitorias. Además, deberá resultar de la comparación de las circunstancias habidas en el momento de la primitiva resolución y las existentes en el tiempo de la solicitud de modificatoria, y deberán ser acreditadas suficientemente por el que pretende la alteración de las medidas.

Los hechos invocados por la actora no implican una alteración sustancial de circunstancias, requisito imprescindible para la viabilidad de la acción ejercitada.

El supuesto aumento de los gastos por razón de estudios y por la mayor edad de la hija menor, no implica una variación sustancial de circunstancias; se trata de un proceso natural de evolución ya tomado en consideración por el órgano jurisdiccional a la hora de fijar la pensión alimenticia, que ha de responder a procesos dinámicos en los que las demandas de los hijos y sus necesidades no son siempre las mismas en el tiempo, apareciendo y desapareciendo unas a la vez que se incrementan y disminuyen otras, de ahí que las mismas se calculen atendiendo a valores medios.

VIII.- COSTAS.

Las costas procesales deben ser impuestas a la parte demandante, al ver desestimadas sus precisas pretensiones, con arreglo al art. 394 LEC.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito y por formulada en tiempo y forma contestación a la demanda de modificación de medidas interpuesta contra mi mandante por Dña. [NOMBRE Y APELLIDOS], se digne admitirla a trámite junto con los documentos acompañados y sus copias, y previo el procedimiento que le corresponda, se venga dictar sentencia por la que, con desestimación íntegra de la demanda, se absuelva libremente a la demandada de cuantos concretos pedimentos se le dirigen, manteniendo íntegramente las medidas acordadas en sentencia de separación dictada por ese Tribunal el día [FECHA], con expresa condena en costas a la contraparte.

Es de Justicia que se pide en [LUGAR], a OTROSÍ DIGO: Que por necesitar para otros usos la escritura de poder acreditativa de la representación del suscrito Procurador, intereso y

SUPLICO AL TRIBUNAL

se sirva acordar su desglose y devolución a esta parte, dejando en autos testimonio de la misma.

Reitero Justicia en lugar y fecha "ut supra ".

Firma del Abogado/a	Firma del Procurador/a

========================================================================
