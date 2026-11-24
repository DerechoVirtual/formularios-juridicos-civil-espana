---
name: contestacion-divorcio-medidas-reconvencion-alimentos-civ-0034
description: "Contestación a divorcio con medidas y reconvención de alimentos a hijo mayor, Derecho catalán. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contestación a divorcio con medidas y reconvención de alimentos a hijo mayor, Derecho catalán

> Formulario **CIV-0034** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Tribunal Comparecencia, representación y asistencia Letrada Contestación a la demanda e interposición de demanda reconvencional Hechos FUNDAMENTOS DE DERECHO Suplico Interposición de demanda reconvencional Firmas

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contestación a divorcio con medidas y reconvención de alimentos a hijo mayor, Derecho catalán» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contestación a divorcio con medidas y reconvención de alimentos a hijo mayor, Derecho catalán” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:contestacion-divorcio-medidas-reconvencion-alimentos-civ-0034`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº DE DOCUMENTO (9 veces)
- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] IMPORTE (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] AÑO (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] Nº (2 veces)
- [ ] PROFESIÓN (2 veces)
- [ ] CALLE
- [ ] CENTRO DE ESTUDIOS
- [ ] COLEGIO
- [ ] DÍA
- [ ] ESTUDIOS CURSADOS
- [ ] MES
- [ ] Nº DE CUENTA (IBAN)
- [ ] Nº DE PROCEDIMIENTO
- [ ] SEDE

## Normas que cita el formulario

- art. 750 LEC
- art. 770 LEC
- art. 233 Código Civil
- art. 233.20.2 Código Civil
- art. 394 LEC
- art. 93.2 CC
- art. 770.2 LEC
- art. 409 LEC
- art. 93.2 Código Civil

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

- Junto a «…Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Denominación legal: Sección de Familia, Infancia y Capacidad. Si no existe en el partido, conoce la Sección Civil o la Única (art. 86.3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «….3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D./Dª [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en nombre y representación de D./Dª [NOMBRE Y APELLIDOS], mayor de edad, de profesión [PROFESIÓN], con domicilio en [LOCALIDAD], calle [CALLE], nº [NÚMERO], pta., cuya representación acreditaré mediante comparecencia apud acta cuando sea requerido para ello, comparezco en este TRIBUNAL con la asistencia del Letrado D./Dª [NOMBRE Y APELLIDOS], del Ilustre Colegio de Abogados de [COLEGIO], y DIGO:

Que por medio del presente escrito y en la representación que ostento, tras habérseme dado traslado de la demanda de divorcio conforme a lo dispuesto en el art. 753 de la Ley de Enjuiciamiento Civil, me persono en los autos de juicio núm. [Nº DE PROCEDIMIENTO]/[AÑO], instados por D./Dª [NOMBRE Y APELLIDOS], y formulo dentro del plazo legal de veinte días CONTESTACIÓN A LA DEMANDA DE DIVORCIO e interpongo DEMANDA RECONVENCIONAL, con base en los siguientes

HECHOS:

PRIMERO De acuerdo con el correlativo de la demanda, en relación con los datos de celebración del matrimonio.

SEGUNDO De acuerdo con el correlativo de la demanda, en relación con la existencia y datos identificativos de los/las dos hijos/as comunes del matrimonio.

TERCERO De acuerdo con el correlativo de la demanda en cuanto al régimen económico matrimonial, que es el legal de separación de bienes

CUARTO De acuerdo con el correlativo de la demanda, en relación con la existencia de crisis matrimonial. Dado que han transcurrido más de tres meses desde el matrimonio, nada tiene que oponer mi representado/a a la pretensión de divorcio del/de la actor/a.

QUINTO En relación con el hijo menor de edad, mi mandante manifiesta su disconformidad respecto las circunstancias que, según el/la demandante, hacen conveniente el régimen de guarda y custodia compartida.

Por el contrario, es lo más conveniente para los intereses del citado menor que se atribuya la guarda individual a mi representado/a a la vista de las siguientes circunstancias:

Para acreditar los anteriores hechos se aportan como DOCUMENTOS Nª [Nº DE DOCUMENTO] a [Nº DE DOCUMENTO], los siguientes:

La atribución de la guarda y custodia a mi mandante, hace necesario fijar una pensión de alimentos a cargo del demandante, en favor del hijo menor. Para fijarla debe atenderse a las siguientes circunstancias relativas a las necesidades del menor y a la capacidad económica de ambos progenitores:

Para acreditar las anteriores circunstancias, se acompañan, como DOCUMENTOS Nº [Nº DE DOCUMENTO] a [Nº DE DOCUMENTO], los siguientes:

A la vista de las anteriores circunstancias y conforme con los criterios que resultan de las Tablas orientadoras para determinar las pensiones alimenticias de los hijos en los procesos de familia elaboradas por el Consejo General del Poder Judicial en julio de 2013, se propone la fijación de una pensión alimenticia a favor del menor por cuantía de [IMPORTE] euros mensuales, a satisfacer durante los cinco primeros días de cada mes, mediante ingreso en la cuenta corriente nº [NÚMERO], cuya titularidad corresponde a mi mandante, y actualizable anualmente de acuerdo con la variación que experimente el Índice de Precios al Consumo publicado por el Instituto Nacional de Estadística u organismo, público o privado, que en el futuro le sustituya.

En relación con el uso de la vivienda familiar, cuya titularidad corresponde en comunidad a ambos cónyuges, tal y como resulta de la certificación registral que se acompaña como DOCUMENTO Nª [Nº DE DOCUMENTO], se propone la atribución de su uso a mi mandante en coherencia con la solicitud de guarda individual a su favor.

SEXTO En cuanto al hijo mayor de edad, no por razón de su edad deja de tener derecho a percibir alimentos. Antes bien, al carecer de independencia económica y encontrarse todavía en periodo de formación, tiene derecho a percibirlos de sus progenitores. Al no haberse hecho alusión a ellos en la demanda que ahora se contesta, se solicitarán en la demanda reconvencional que también se interpone en este escrito.

Resultan aplicables a los citados hechos los siguientes

FUNDAMENTOS DE DERECHO

Competencia, procedimiento y legitimación

Conformes con la competencia objetiva y territorial del Tribunal, la legitimación de las partes, y el procedimiento.

Representación y defensa

Mi mandante comparece representado/a y defendido/a, respectivamente, por el Procurador y el Letrado que constan en el encabezamiento de este escrito, de acuerdo con lo dispuesto en el artículo 750 LEC, en relación con el artículo 770 LEC.

Derecho sustantivo

Dado que el vigente art. 86 del Código civil, no requiere causa alguna de divorcio, bastando para poder solicitarlo y que sea decretado por el Juez el transcurso de tres meses desde el matrimonio, nada hay que oponer a este extremo.

Sin embargo, al no estar de acuerdo con el contenido de las medidas definitivas solicitadas, en relación con la guarda y custodia de los hijos, los alimentos a favor de éstos y la atribución del uso de la vivienda habitual de la familia, se formula oposición en cuanto a estos extremos y, con amparo en los artículos 233-4 y ss. del Código Civil de Cataluña, se solicita la adopción de las siguientes medidas definitivas:

A) Guarda y custodia del/de la hijo/a menor.- El régimen de guarda y custodia que se propone atiende al interés del menor, que el art. 233-8.3 del Código Civil de Cataluña reconoce como prioritario, señalando el art. 233-10.2, en su último inciso, que la autoridad judicial puede disponer que la guarda se ejerza de modo individual si conviene más al interés del hijo.

Dado que en los HECHOS de esta Contestación se ha justificado la conveniencia para el menor de fijar la guarda y custodia individual a favor de mi mandante, conforme a los criterios determinados por el art. 233-11 del meritado Cuerpo Legal, se presenta el siguiente Plan de Parentalidad, ajustado a lo dispuesto en el art. 233-9 del Código Civil de Cataluña, para ordenar el citado régimen:

B) Alimentos en favor del/de la hijo/a menor.- El art. 236-17.1 del Código Civil de Cataluña dispone: "Relaciones entre padres e hijos. 1. Los progenitores, en virtud de sus responsabilidades parentales, deben cuidar de los hijos, prestarles alimentos en el sentido más amplio, convivir con ellos, educarlos y proporcionarles una formación integral. ()". El art. 233-10.3 del Código Civil de Cataluña señala que "La forma de ejercer la guarda no altera el contenido de la obligación de alimentos hacia los hijos comunes, si bien es preciso ponderar el tiempo de permanencia de los menores con cada uno de los progenitores y los gastos que cada uno de ellos haya asumido pagar directamente.()". Y los arts. 237-1 y ss. del Código Civil de Cataluña, regulan los alimentos entre parientes.

C) Atribución del uso de la vivienda familiar.- El art. 233.20.2 del Código Civil de Cataluña establece: "Si no existe acuerdo o si este no es aprobado, la autoridad judicial debe atribuir el uso de la vivienda familiar, preferentemente, al progenitor a quien corresponda la guarda de los hijos comunes mientras dure esta".

Costas

Las costas deben ser impuestas a la parte demandante conforme al art. 394 de la Ley de Enjuiciamiento Civil.

Iura novit curia y las demás normas que resulten procedentes.

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL

Que tras admitir este escrito con los documentos que lo acompañan, me tenga por comparecido y parte en la representación que ostento, entendiéndose conmigo las sucesivas diligencias, y tenga por interpuesta en tiempo y forma CONTESTACIÓN A LA DEMANDA CONTENCIOSA DE DIVORCIO y, previos los trámites procesales oportunos, dicte en su día sentencia por la que se estime el divorcio y se desestimen las medidas definitivas propuestas en la demanda, con estimación, en su lugar, de las que propone mi mandante, que han sido detalladas en los Fundamentos de Derecho de esta contestación y que reiteramos en esta Solicitud. Las medidas definitivas cuya adopción se solicita son las siguientes:

Así mismo, se solicita la imposición de las costas al demandado, conforme a lo dispuesto en el art. 394 LEC.

Interposición de demanda reconvencional

HECHOS

PRIMERO Dense por reiterados los hechos de la contestación.

SEGUNDO El hijo común de las partes en este procedimiento, de [Nº] años de edad y soltero, se encuentra todavía en proceso de formación, cursando estudios de [ESTUDIOS CURSADOS] en [CENTRO DE ESTUDIOS] con un rendimiento regular, sin que haya accedido todavía al mercado laboral y sin que disponga de medios propios para subsistir, pues carece de patrimonio y no obtiene ningún tipo de ingresos. Además, convive todavía en el domicilio familiar y seguirá haciéndolo con mi mandante en el futuro, hasta que no alcance independencia económica.

Como justificación de los anteriores hechos, se acompañan como DOCUMENTOS Nº [Nº DE DOCUMENTO] a [Nº DE DOCUMENTO], los siguientes:

TERCERO El demandado reconvencional, D./Dª [NOMBRE Y APELLIDOS], se encuentra en una holgada situación económica, gracias a los elevados ingresos que obtiene como [PROFESIÓN]. Además dispone de varios inmuebles de su propiedad:

Como justificación de los anteriores hechos, se acompañan como DOCUMENTOS Nº [Nº DE DOCUMENTO] a [Nº DE DOCUMENTO], los siguientes:

CUARTO En consecuencia, se reclama a la parte demandada en esta reconvención, una pensión de alimentos a favor del hijo común mayor de edad de [IMPORTE] euros mensuales, a satisfacer, con carácter anticipado, en los cinco primeros días de cada mes, mediante ingreso en la cuenta corriente [Nº DE CUENTA (IBAN)], de la que es titular mi representado/a, actualizable anualmente de acuerdo con las variaciones experimentadas por el IPC que señale el Instituto Nacional de Estadística u organismo que lo sustituya.

Resultan aplicables a los citados hechos los siguientes

FUNDAMENTOS DE DERECHO

I. Resulta competente para conocer de la demanda reconvencional el mismo Juez que esté conociendo de la demanda principal.

II. Está legitimado/a mi representado/a para solicitar alimentos para su hijo mayor de edad en este proceso de crisis matrimonial en virtud de lo dispuesto en el artículo 93.2º CC.

III. El art. 770.2ª LEC admite que se formule reconvención al contestar la demanda de separación o divorcio en los siguientes casos: a) Cuando se funde en alguna de las causas que puedan dar lugar a la nulidad del matrimonio. b) Cuando el cónyuge demandado de separación o de nulidad pretenda el divorcio. c) Cuando el cónyuge demandado de nulidad pretenda la separación. d) Cuando el cónyuge demandado pretenda la adopción de medidas definitivas, que no hubieran sido solicitadas en la demanda, y sobre las que el tribunal no deba pronunciarse de oficio. En el caso presente el supuesto se ajusta al enunciado bajo la letra d), debiendo sustanciarse y resolverse la reconvención conforme con lo prevenido en el art. 409 LEC.

IV. En relación con la pensión de alimentos en favor del hijo mayor de edad, los arts. 237-1 y ss. del Código Civil de Cataluña, además del art. 93.2 del Código Civil.

V. COSTAS.- Deben imponerse a la parte demandada en reconvención si se opone a la demanda reconvencional, conforme a lo dispuesto en el art. 394 de la Ley de Enjuiciamiento Civil.

IV.Iura novit curia.

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL

Que tenga por interpuesta en tiempo y forma DEMANDA RECONVENCIONAL contra D./Dª [NOMBRE Y APELLIDOS] y, previos los trámites procesales oportunos, y tras declarar el divorcio de las partes, acuerde el establecimiento de una pensión de alimentos a cargo de la parte demandada en la reconvención y a favor del hijo común y mayor de edad de los cónyuges, D./Dª [NOMBRE Y APELLIDOS], mientras se encuentre en periodo de formación y carezca de independencia económica por importe de [IMPORTE] euros mensuales, a pagar mediante ingreso en la cuenta corriente nº [NÚMERO], de la que es titular mi mandante, durante los cinco primeros días de cada mes y actualizable anualmente de acuerdo con las variaciones del IPC que señale el Instituto Nacional de Estadística u organismo que lo sustituya, con imposición de las costas de esta reconvención a la parte reconvenida si se opone a las pretensiones esgrimidas en la misma.

En [LOCALIDAD], a [DÍA], de [MES], de [AÑO]

Firma y número del Letrado	Firma del Procurador

========================================================================
