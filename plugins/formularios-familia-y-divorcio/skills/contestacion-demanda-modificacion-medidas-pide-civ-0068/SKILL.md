---
name: contestacion-demanda-modificacion-medidas-pide-civ-0068
description: "Contestación a la demanda de modificación de medidas que pide la custodia compartida. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contestación a la demanda de modificación de medidas que pide la custodia compartida

> Formulario **CIV-0068** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contestación a la demanda de modificación de medidas que pide la custodia compartida» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contestación a la demanda de modificación de medidas que pide la custodia compartida” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:contestacion-demanda-modificacion-medidas-pide-civ-0068`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] Nº DE DOCUMENTO (5 veces)
- [ ] AÑO (4 veces)
- [ ] DÍA (2 veces)
- [ ] MES (2 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] COLEGIO
- [ ] DIRECCIÓN
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] NOMBRE DEL CENTRO ESCOLAR
- [ ] Nº
- [ ] NÚMERO
- [ ] SEDE

## Normas que cita el formulario

- art. 90.3 CC
- art. 775.1 LEC
- art. 91 CC
- art. 775 LEC
- art. 92.8 CC

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

D./Dª [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en nombre y representación de D./Dª [NOMBRE Y APELLIDOS], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], comparezco en este TRIBUNAL con la asistencia del Letrado D./Dª [NOMBRE Y APELLIDOS], del Ilustre Colegio de Abogados de [COLEGIO], y DIGO:

Que por medio del presente escrito y en la representación que ostento, tras habérseme dado traslado de la demanda de modificación de medidas definitivas de divorcio o separación conforme a lo dispuesto en el art. 753 de la Ley de Enjuiciamiento Civil, me persono en los autos de juicio núm. [Nº DE PROCEDIMIENTO]/[AÑO], instados por D./Dª [NOMBRE Y APELLIDOS], y formulo dentro del plazo legal de veinte días CONTESTACIÓN A LA DEMANDA, con base en los siguientes

HECHOS

De acuerdo con el correlativo de la demanda, en relación con la existencia de la sentencia de divorcio/separación dictada en fecha [DÍA] de [MES] de [AÑO] por el Tribunal nº [NÚMERO] de [LOCALIDAD], en el seno del procedimiento de Divorcio o de Separación de mutuo acuerdo o contencioso [Nº DE PROCEDIMIENTO] / [AÑO] y con el contenido de las medidas acordadas en el convenio regulador homologado por la misma o medidas judiciales definitivas establecidas en la misma.

Se niega el correlativo de la demanda, en relación con la supuesta alteración de las circunstancias atendidas las cuales se acordó en su momento un régimen de guarda y custodia individual a favor de mi representado/a, y la obligación del demandante de satisfacer una pensión periódica de alimentos a favor del hijo/a común, así como la atribución del uso de la vivienda familiar.

Dicha alteración sustancial justificativa, según la demanda, de la modificación de las medidas vigentes no se ha producido. Por el contrario, sigue siendo de interés del/la menor el régimen de guarda y custodia individual en favor de mi representado/a.

Y ello por lo siguiente:

El/la menor padece un trastorno del espectro autista, con un grado de discapacidad reconocido del 40%, por la que precisa unas atenciones especiales que ni representado/a puede prestarle gracias a la flexibilidad de horario que le permite su profesión: Por otra parte mi representado cuenta con una experiencia a la hora de facilitar dichos cuidados a su hijo/a de la que carece el/la demandante, que nunca se ha ocupado personalmente de prestárselos. Entre estos cuidados, mi representado/a traslada a su hijo/a todas las semanas al centro [NOMBRE DEL CENTRO ESCOLAR], ubicado en [DIRECCIÓN], donde recibe atención especializada, observándose importantes progresos en su evolución. También lleva al menor a natación y a musicoterapia en la Escuela

Por otra parte, aunque es cierto que el/la demandante ha trasladado recientemente su residencia a la misma localidad y zona en que residen mi representado/a y el hijo/a común, lo cierto es que el trabajo desempeñado por aquél/aquella, le obliga a pasar largas temporadas fuera de su ciudad, lo que resulta incompatible con la prestación de los cuidados que requiere la salud de su hijo/a.

Finalmente, el/la demandante ni siquiera ha cumplido con el régimen de visitas estipulado hasta la fecha, alegando continuamente motivos laborales para ello.

Para acreditar los anteriores extremos, se acompañan como DOCUMENTOS Nº [Nº DE DOCUMENTO], Nº [Nº DE DOCUMENTO] y Nº [Nº DE DOCUMENTO], los siguientes:

Se acompaña, igualmente, como DOCUMENTO Nº [Nº DE DOCUMENTO], informe del/de la psicólogo/a D./Dª [NOMBRE Y APELLIDOS], en el que se pone de relieve que "lo más conveniente para el menor en este momento es continuar en el actual entorno familiar, pues satisface la necesidad del niño de adaptarse a un entorno lo más rutinario posible, lo que resulta esencial en relación con el tipo de trastorno que padece" y que "una vez establecida la red de apoyos en su centro escolar así como en un centro especializado, sería contraproducente para el progreso en su desarrollo cualquier cambio al respecto".

TERCERO.- Dado que no es conveniente, en interés del menor, ni se halla justificada la modificación del régimen de guarda y custodia individual, no procede tampoco alterar las medidas relativas a los alimentos ni a la atribución del uso de la vivienda habitual, que se fijaron de un modo coherente con dicho régimen de custodia individual.

Resultan aplicables a los citados hechos los siguientes

FUNDAMENTOS DE DERECHO

I. Competencia, procedimiento, legitimación y postulación procesal

Conformes con la competencia objetiva y territorial del Tribunal, la legitimación de las partes, y el procedimiento, compareciendo esta parte con la debida representación técnica y asistencia letrada.

II. Derecho sustantivo

El art. 90.3, primer inciso CC, que dispone: “Las medidas que el Juez adopte en defecto de acuerdo o las convenidas por los cónyuges judicialmente, podrán ser modificadas judicialmente o por nuevo convenio aprobado por el Juez, cuando así lo aconsejen las nuevas necesidades de los hijos o el cambio de las circunstancias de los cónyuges” "Asimismo podrá modificarse el convenio, o solicitarse modificación de las medidas sobre los animales de compañía si se hubieran alterado gravemente sus circunstancias." (párrafo introducido por Ley 17/2021, de 15 diciembre), en relación con el art. 775.1 LEC, que regula la modificación de las medidas definitivas y que señala: “El Ministerio Fiscal, habiendo hijos menores o incapacitados y, en todo caso, los cónyuges, podrán solicitar del tribunal que acordó las medidas definitivas, la modificación de las medidas convenidas por los cónyuges o de las adoptadas en defecto de acuerdo, siempre que hayan variado sustancialmente las circunstancias tenidas en cuenta al aprobarlas o acordarlas. En el mismo sentido, el art. 91 CC, señala que las medidas judiciales “podrán ser modificadas cuando se alteren sustancialmente las circunstancias”.

De estos preceptos, sistemáticamente interpretados, se deduce que la modificación de las medidas definitivas consensuadas o judicialmente decretadas solo procede ante la alteración sustancial de las circunstancias que se tuvieron en cuenta al decretarlas que justifique dicha modificación, alteración que no se da en el caso presente.

Es cierto que la Ley de la Jurisdicción Voluntaria ha modificado la redacción del art. 90.3 CC, sustituyendo la anterior expresión “cuando se alteren sustancialmente las circunstancias”, por la actual: “cuando así lo aconsejen las nuevas necesidades de los hijos o el cambio de las circunstancias de los cónyuges”. Aunque en teoría esto podría plantear la duda de si la alteración de circunstancias que fundamenta la modificación de la medida debe ser sustancial, debe interpretarse la norma en el mismo sentido que la anterior y, por tanto requiriendo sustancialidad en el cambio de circunstancias. En este sentido juega el tenor de los arts. 775 LEC y 91 CC que mantienen expresamente este requisito y que deben ser objeto de interpretación sistemática junto con el art. 90.3 CC.

Por su parte, el art. 92.8 del Código civil dispone que, excepcionalmente, aun cuando no haya acuerdo entre los progenitores, “el Juez, a instancia de una de las partes, con informe (Anteriormente el art. 92.8 CC hacía referencia al informe “favorable” del Ministerio Fiscal como requisito para que el Juez decretase la custodia compartida en defecto de acuerdo de los progenitores; sin embargo, el término entrecomillado ha sido declarado inconstitucional y nulo por Sentencia 185/2012, de 17 de octubre, del Pleno del Tribunal Constitucional - BOE. núm. 274, de 14 de noviembre de 2012 -) del Ministerio Fiscal, podrá acordar la guarda y custodia compartida, fundamentándola en que de esta forma se protege adecuadamente el interés superior del menor”. Ahora bien, tal y como queda de manifiesto a la vista de los hechos expuestos en este escrito de contestación, no resulta de interés para el hijo menor el acogimiento de una custodia compartida, por lo que debe desestimarse tal pretensión y, con ella, la de modificar el régimen de los alimentos y la relativa a la atribución del uso de la vivienda familiar, manteniéndose las medidas definitivas establecidas en la sentencia de divorcio/separación.

En este sentido falló la SAP de Huesca, Sección 1ª, de 28 de diciembre de 2011, rec. 197/2011, en la que se resolvía un caso similar al presente y ello incluso en un supuesto en que la decisión de mantener la custodia individual del padre atendiendo al interés del hijo menor implicaba la separación de éste de su hermano, que convivía con la madre. Aun así, el Tribunal consideró prioritaria la satisfacción de las necesidades del menor, que padecía un trastorno de desarrollo y a la que se daba mejor cumplimiento permaneciendo bajo la custodia paterna.

III. Costas

Deben ser impuestas al/ a la demandante, de acuerdo con el art. 394 de la Ley de Enjuiciamiento civil. Su mala fe resulta de ser plenamente consciente de que sus circunstancias actuales no le permiten atender adecuadamente a su hijo/a, no encontrándose justificada la modificación de medidas que solicita.

IV. Iura novit curia

Iura novit curia y las demás normas que resulten procedentes.

Por lo expuesto:

SUPLICO AL TRIBUNAL

Que tras admitir este escrito con los documentos que lo acompañan, me tenga por comparecido y parte en la representación que ostento, entendiéndose conmigo las sucesivas diligencias, y tenga por interpuesta en tiempo y forma CONTESTACIÓN A LA DEMANDA CONTENCIOSA DE MODIFICACIÓN DE MEDIDAS DEFINITIVAS y, previos los trámites procesales oportunos, dicte en su día sentencia por la que se desestime íntegramente la demanda de modificación de medidas definitivas, con expresa condena en costas de la parte actora.

En virtud de lo expuesto,

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma y número del Letrado	Firma del Procurador

========================================================================
