---
name: contestacion-demanda-divorcio-reconviniendo-prestacion-civ-0001
description: "Contestación a demanda de divorcio reconviniendo por la prestación compensatoria del Derecho catalán. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contestación a demanda de divorcio reconviniendo por la prestación compensatoria del Derecho catalán

> Formulario **CIV-0001** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Contestación a demanda de divorcio en que se reconviene solicitando el reconocimiento del derecho a una prestación compensatoria conforme a Derecho civil especial de Cataluña.

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contestación a demanda de divorcio reconviniendo por la prestación compensatoria del Derecho catalán» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contestación a demanda de divorcio reconviniendo por la prestación compensatoria del Derecho catalán” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:contestacion-demanda-divorcio-reconviniendo-prestacion-civ-0001`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] NÚMERO (4 veces)
- [ ] IMPORTE (3 veces)
- [ ] Nº (3 veces)
- [ ] EXPONER LOS HECHOS (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] AÑO
- [ ] CALLE
- [ ] DESCRIBIR
- [ ] Nº DE DOCUMENTO
- [ ] SEDE

## Normas que cita el formulario

- art. 81.2.º CC
- art. 86 CC
- art. 233 CC
- art. 749.2 LEC
- art. 394 LEC
- art. 770.2.ª LEC
- art. 409 LEC
- art. 253 LEC
- art. 251 LEC

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

- Junto a «…AMILIA, INFANCIA Y CAPACIDAD DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Denominación legal: Sección de Familia, Infancia y Capacidad. Si no existe en el partido, conoce la Sección Civil o la Única (art. 86.3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).
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

A LA SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D./Dña. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, que actúa en nombre y representación de Dña. [NOMBRE Y APELLIDOS], como acredito mediante apoderamiento cuya escritura aporto para unión a los autos mediante testimonio y devolución a esta parte, bajo la dirección del Letrada D./Dña. [NOMBRE Y APELLIDOS], colegiada n.º [NÚMERO] del Iltre. Colegio de [LOCALIDAD], con despacho abierto en [LOCALIDAD], calle [CALLE], n.º [NÚMERO], en autos de Juicio de divorcio n.º [NÚMERO]/[AÑO] promovido por D. [NOMBRE Y APELLIDOS], ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que, en la representación que ostento y dentro del plazo legal, vengo a CONTESTAR a la demanda y formular RECONVENCIÓN.

1º.- Fundamento la CONTESTACIÓN A LA DEMANDA en los siguientes hechos y consideraciones jurídicas:

HECHOS

PRIMERO.- De acuerdo con el correlativo de la demanda, sobre los datos del matrimonio celebrado, filiación, domicilio familiar, régimen económico de los cónyuges y la vecindad civil catalana de ambos, negando el resto de los hechos alegados en la misma, en los que justifica la solicitud de las medidas relativas al hijo menor y la determinación de la contribución económica para su manutención y educación.

SEGUNDO.- Respecto a la situación laboral y capacidad económica de los cónyuges, esta parte manifiesta [EXPONER LOS HECHOS]

TERCERO.- Por lo que hace a los efectos y medidas solicitados de contrario respecto del hijo menor debe señalarse que [EXPONER LOS HECHOS] Se solicita por lo expuesto la adopción de las medidas solicitadas en los siguientes términos:

En cumplimiento de lo dispuesto en el art. 233-8.2 del Libro II del Código Civil de Cataluña aprobado por Ley 25/2010 de 29 de julio (en adelante, CCC), se acompaña al presente escrito como documento n.º [NÚMERO], propuesta de Plan de Parentalidad con el contenido exigido por el art. 233-9 de la citada norma.

FUNDAMENTOS DE DERECHO

I.- Conformes con la competencia objetiva y territorial del Tribunal, la legitimación de los cónyuges, y el procedimiento adecuado escogido, compareciendo esta parte con la debida representación técnica y asistencia letrada.

II.- El fondo de la pretensión actora consiste en la declaración de divorcio, a fin de la disolución del matrimonio, a instancia del marido, de conformidad con el art. 81.2.º CCiv, por remisión del art. 86 CCiv, sin necesidad de que se produzca causa legal alguna, sino por la pura voluntad del casado, siendo suficiente que uno de los cónyuges no desee la continuación del matrimonio para que pueda pretender el divorcio, y sin que mi representada pueda oponer motivos materiales a la consideración judicial, al fundarse en la voluntad de no permanecer casado, como corolario legal del derecho del art. 32 CE a contraer matrimonio.

III.- Resultan de aplicación los arts. 233-1 a 233-25 CCC sobre los efectos de la nulidad del matrimonio, del divorcio y de la separación judicial.

En cuanto a la guarda de los hijos y relaciones personales son de especial consideración los arts. 233-10 y 233-11 CCC, sobre el ejercicio de la guarda y los criterios para determinar el régimen y la forma de ejercer la guarda.

IV.- Dada la existencia de un menor de edad, es preceptiva la intervención del Ministerio Fiscal, según lo establecido en los arts. 749.2 y 753 LEC.

V.- Las costas deben imponerse a la actora, de conformidad con lo dispuesto en el art. 394 LEC.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL

Que teniendo por presentado este escrito con los documentos adjuntos y sus copias, se sirva admitirlo, habiéndome por comparecido y parte en representación de Dña. [NOMBRE Y APELLIDOS], y por presentada en tiempo y forma CONTESTACIÓN A LA DEMANDA interpuesta por el demandante, y seguido que sea el juicio por sus trámites legales, dicte en su día sentencia que acuerde el divorcio de los cónyuges, y conforme a las demás pretensiones expresadas en la demanda, salvo en lo referente al ejercicio de las responsabilidades parentales con respecto a la guarda, cuidado y educación de los hijos comunes, que se solicita se aprueben las medidas recogidas en el Plan de Parentalidad que se adjunta al presente escrito.

2º.- Al propio tiempo esta parte formula RECONVENCIÓN contra el actor D. [NOMBRE Y APELLIDOS] en solicitud del pronunciamiento que en el suplico se concretará, y que se basa en los siguientes:

HECHOS

PRIMERO.- Se tienen por expresamente reproducidos los hechos que, al contestar a la demanda, se han ordenado como realidad adversa a la que relaciona la demanda.

SEGUNDO.- Como consecuencia del divorcio, mi mandante queda en peor situación económica que el demandado, por lo que tiene derecho a solicitar de éste una prestación compensatoria que no exceda del nivel de vida que gozaba hasta ahora ni del que pueda mantener en lo sucesivo el demandado, en consideración a su pasada atención a la familia, sus futuras perspectivas económicas y la duración de la convivencia.

Por ello, se solicita una pensión compensatoria de [IMPORTE] € mensuales, actualizables anualmente de acuerdo con el IPC, según el art. 233-14 y ss. CCC, con un límite temporal de [Nº] años.

Se adjunta como prueba documental de ello documentos números [Nº DE DOCUMENTO], consistentes en [DESCRIBIR]

FUNDAMENTOS DE DERECHO

I.- Es Juez competente para conocer de la demanda reconvencional el que esté conociendo de la demanda principal.

II.- Conforme al art. 770.2.ª LEC"La reconvención se propondrá con la contestación a la demanda. El actor dispondrá de 10 días para contestarla (...) Solo se admitirá la reconvención (...) d) Cuando el cónyuge demandado pretenda la adopción de medidas definitivas, que no hubieran sido solicitadas en la demanda, y sobre las que el tribunal no deba pronunciarse de oficio."

El art. 409 LEC señala a este respecto que la reconvención se sustanciará y resolverá al propio tiempo y en la misma forma que la cuestión principal del pleito y será resuelta con éste en la sentencia definitiva.

III.- Las partes en la cuestión reconvencional son las mismas que en la demanda principal, pero con su papel invertido, esto es, el actor en la principal es aquí el demandado reconvencional, y el demandado es aquí demandante reconvencional.

IV.- Conforme a la admonición del art. 253 LEC, puesto que se reclama una prestación pecuniaria, cifro la cuantía de esta reconvención en [IMPORTE] euros, que es la pensión compensatoria anualizada multiplicada por diez, en armonía con la regla 7.ª del art. 251 LEC.

V.- Fundamento legal de la reconvención. El art. 233-14.1 CCC establece el derecho del cónyuge cuya situación económica, como consecuencia de la ruptura de la convivencia resulte más perjudicado a solicitar en el primer proceso matrimonial una prestación compensatoria que no exceda del nivel de vida de que gozaba durante el matrimonio ni del que pueda mantener el cónyuge obligado al pago.

El art. 233-17.1 del citado texto legal recoge la posibilidad de que la prestación compensatoria pueda atribuirse en forma de pensión. El apartado 3 del precepto establece el pago en dinero de la misma y el establecimiento de criterios objetivos y automáticos de actualización de su cuantía.

VI.- Con arreglo al art. 394 LEC han de imponerse al demandado reconvencional, por el vencimiento.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que teniendo por presentado este escrito y por formulada en tiempo y forma demanda reconvencional, la admita a trámite y previos los que le correspondan por el tribunal se fije en concepto de pensión compensatoria a favor de Dña. la cantidad de [IMPORTE] euros mensuales, durante [Nº] años actualizables anualmente de acuerdo con las variaciones positivas del IPC que publique el INE u Organismo que lo sustituya.

Todo ello con expresa imposición de costas a la parte contraria.

Firma del Abogado/a	Firma del Procurador/a

========================================================================
