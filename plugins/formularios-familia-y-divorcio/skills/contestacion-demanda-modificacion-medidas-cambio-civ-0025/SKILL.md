---
name: contestacion-demanda-modificacion-medidas-cambio-civ-0025
description: "Contestación a la demanda de modificación de medidas por cambio de domicilio del progenitor custodio. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contestación a la demanda de modificación de medidas por cambio de domicilio del progenitor custodio

> Formulario **CIV-0025** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contestación a la demanda de modificación de medidas por cambio de domicilio del progenitor custodio» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contestación a la demanda de modificación de medidas por cambio de domicilio del progenitor custodio” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:contestacion-demanda-modificacion-medidas-cambio-civ-0025`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (4 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] Nº DE DOCUMENTO (4 veces)
- [ ] AÑO (3 veces)
- [ ] DÍA (2 veces)
- [ ] MES (2 veces)
- [ ] RELACIÓN DE DOCUMENTOS (2 veces)
- [ ] COLEGIO
- [ ] Nº DE PROCEDIMIENTO
- [ ] OTROS DATOS

## Normas que cita el formulario

- art. 91 CC
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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Junto a «…FANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA NUM DE [LOCALIDAD]»: Denominación legal: Sección de Familia, Infancia y Capacidad. Si no existe en el partido, conoce la Sección Civil o la Única (art. 86.3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA NUM DE [LOCALIDAD]

D./Dª [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en nombre y representación de D./Dª [NOMBRE Y APELLIDOS], cuya representación acreditaré mediante comparecencia apud acta cuando sea requerido para ello, comparezco en este TRIBUNAL con la asistencia del Letrado D./Dª [NOMBRE Y APELLIDOS], del Ilustre Colegio de Abogados de [COLEGIO], y DIGO:

Que por medio del presente escrito y en la representación que ostento, me persono en los autos de juicio núm. [Nº DE PROCEDIMIENTO]/[AÑO], instados por D./Dª [NOMBRE Y APELLIDOS], y formulo en tiempo y forma CONTESTACIÓN A LA DEMANDA, con base en los siguientes

HECHOS

PRIMERO De acuerdo con el correlativo de la demanda, relativo al régimen de guarda y custodia establecido en procedimiento de Divorcio [ELEGIR: contencioso / de mutuo acuerdo] de mutuo acuerdo /

SEGUNDO De acuerdo con el correlativo de la demanda, sobre el traslado del domicilio de mi mandante a [LOCALIDAD] en fecha [DÍA] de [MES] de [AÑO]

TERCERO En desacuerdo con los hechos de contrario expuestos en el correlativo de la demanda. Antes bien, el cambio de domicilio efectuado por mi mandante no ha sido innecesario, arbitrario o caprichoso, como lo califica dl demandante. Por el contrario, se encuentra justificado y es conveniente para los hijos menores. El traslado a un domicilio en localidad diferente a aquella en la que hasta entonces estaba fijado, obedece a cambios sobrevenidos en la situación laboral, profesional y económica de la madre. Como consecuencia del ERE que afectó a la empresa en que trabaja mi mandante, y en cumplimiento de los criterios sobre movilidad geográfica adoptados en el Convenio regulador del ERE, aquélla se vio abocada, por decisión de la empresa, a trasladarse la ciudad de [LOCALIDAD], quedándole como única alternativa posible el despido indemnizado. Por tanto, el cambio de domicilio deriva de una situación de necesidad por motivos laborales, que no es imputable a mi mandante.

Se acompañan como DOCUMENTOS Nº [Nº DE DOCUMENTO] a [Nº DE DOCUMENTO], los siguientes, para acreditar los citados hechos; [RELACIÓN DE DOCUMENTOS].

CUARTO En desacuerdo con los hechos de contrario expuestos en el correlativo de la demanda. Es la madre la que se ocupado del cuidado personal de los hijos desde que estos nacieron y no sólo desde la ruptura del matrimonio. Por otra parte, al margen de la incidencia normal que un cambio de domicilio puede tener en los menores, lo cierto es que estos se han adaptado perfectamente al mismo y a su nuevo entorno escolar, sin que pueda decirse que les haya resultado perjudicial. Por otra parte, el nuevo horario del que disfruta mi mandante en su actual lugar de trabajo, le permite mayor disponibilidad para ocuparse de sus hijos y estos realizan ahora actividades extraescolares deportivas que antes no podían realizar.

Se acompañan como DOCUMENTOS Nº [Nº DE DOCUMENTO] a [Nº DE DOCUMENTO], los siguientes, para acreditar los citados hechos: [RELACIÓN DE DOCUMENTOS].

QUINTO En desacuerdo con los hechos de contrario expuestos en el correlativo de la demanda. Aunque es cierto que la nueva situación impide que el padre pueda desarrollar las visitas intersemanales establecidas hasta el momento, los miércoles tarde, ello no justifica que se le atribuya a él la guarda y custodia de los menores, pues conviene más al interés de estos que se mantenga en favor de la madre, tal y como resulta de los hechos antes expuestos. Las visitas de fin de semana pueden mantenerse prácticamente en las mismas condiciones y puede compensarse la falta de visitas entre semanas por la ampliación de las que corresponden al padre en puentes escolares. En concreto, se propone la modificación del régimen de visitas en los siguientes términos:

1) Los hijos estarán con el padre dos fines de semana alternos de cada mes y todos los puentes escolares, fijándose el siguiente horario de entrega y recogida: Se consigna

2) Se dejan sin efecto las visitas de entre semanas.

3) Se mantiene el reparto de vacaciones de Navidad, Pascua y Verano.

A los anteriores hechos les son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

Competencia, procedimiento, legitimación y postulación procesal

Conformes con la competencia objetiva y territorial del Tribunal, la legitimación de las partes, y el procedimiento, compareciendo esta parte con la debida representación técnica y asistencia letrada.

Derecho sustantivo

El art. 19 CE, que reconoce el derecho fundamental a la elección del domicilio. Si bien es cierto que este derecho debe verse limitado por los intereses de los hijos menores de edad que convivan con el titular de este derecho, esto no impide cualquier cambio de domicilio, sino sólo los que se realicen de modo irresponsable o arbitrario, perjudicando al menor.

El art. 91 CC permite modificar las medidas definitivas adoptadas en procedimientos de crisis matrimonial cuando se alteren sustancialmente las circunstancias.

Costas

Deben ser impuestas al/ a la demandante, de acuerdo con el art. 394 de la Ley de Enjuiciamiento civil.

Por lo expuesto:

SUPLICO AL TRIBUNAL,

Que tras admitir este escrito con los documentos que lo acompañan, me tenga por comparecido y parte en la representación que ostento, entendiéndose conmigo las sucesivas diligencias, y tenga por interpuesta en tiempo y forma CONTESTACIÓN A LA DEMANDA SOBRE MODIFICACIÓN DE RÉGIMEN DE GUARDA Y CUSTODIA y, previos los trámites procesales oportunos, dicte en su día sentencia por la que, desestimando la demanda en relación con las medidas definitivas cuya modificación se pretende, dicte sentencia por la que se absuelva a la demandada de las pretensiones ejercitadas de contrario, y, atendiendo la solicitud de mi mandante, se modifique el régimen de visitas reconocido en favor del demandante en los siguientes términos:

1) Los hijos estarán con el padre dos fines de semana alternos de cada mes [OTROS DATOS] y todos los puentes escolares, fijándose el siguiente horario de entrega y recogida: Se consigna

2) Se dejan sin efecto las visitas de entre semanas.

3) Se mantiene el reparto de vacaciones de Navidad, Pascua y Verano.

Así mismo, se solicita la expresa condena en costas de la parte actora de acuerdo con el art. 394 LEC.

En [LOCALIDAD], a [DÍA], de [MES], de [AÑO]

Firma y número del Letrado	Firma del Procurador

========================================================================
