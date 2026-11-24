---
name: demanda-reduccion-pension-alimenticia-nacimiento-nuevo-civ-0148
description: "Demanda de reducción de la pensión alimenticia por el nacimiento de un nuevo hijo. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de reducción de la pensión alimenticia por el nacimiento de un nuevo hijo

> Formulario **CIV-0148** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda de modificación de medidas definitivas (arts. 90, 91 CC y 775 LEC) por la que el progenitor obligado al pago pide reducir la pensión de alimentos fijada en favor de un hijo menor, por el nacimiento de nuevos hijos que también debe mantener.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de reducción de la pensión alimenticia por el nacimiento de un nuevo hijo» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de reducción de la pensión alimenticia por el nacimiento de un nuevo hijo” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-reduccion-pension-alimenticia-nacimiento-nuevo-civ-0148`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] AÑO (6 veces)
- [ ] DÍA (6 veces)
- [ ] MES (6 veces)
- [ ] Nº (5 veces)
- [ ] IMPORTE (4 veces)
- [ ] IMPORTE EN LETRA (3 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] Nº DE PROCEDIMIENTO (3 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL DEMANDADO (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL HIJO/A (2 veces)
- [ ] SEDE (2 veces)
- [ ] COLEGIO DE ABOGADOS
- [ ] DNI/NIF
- [ ] DOCUMENTO QUE ACREDITA EL INTENTO DE SOLUCIÓN EXTRAJUDICIAL
- [ ] DOMICILIO
- [ ] INDICAR EL MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] NOMBRE Y APELLIDOS DEL DEMANDANTE
- [ ] NOMBRE Y APELLIDOS DEL LETRADO
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] NOMBRE/S DE LOS NUEVOS HIJOS
- [ ] Nº DE ESTIPULACIÓN
- [ ] Nº DE NUEVOS HIJOS
- [ ] O SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD
- [ ] RELACIÓN DE DOCUMENTOS

## Normas que cita el formulario

- art. 90 Código Civil
- art. 5 Ley Orgánica 1/2025
- art. 90.3 Código Civil
- art. 91 Código Civil

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

- Junto a «…s "podrán ser modificadas cuando se alteren sustancialmente las circunstancias".»: la referencia a hijos «incapacitados» del art. 775.1 LEC se ha adaptado a la terminología de la Ley 8/2021; contrastar la redacción literal vigente del precepto antes de presentar.

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

A LA SECCIÓN CIVIL [O SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D./Dª [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, en nombre y representación de D./Dª [NOMBRE Y APELLIDOS DEL DEMANDANTE], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], comparezco en este Tribunal con la asistencia del Letrado D./Dª [NOMBRE Y APELLIDOS DEL LETRADO], del Ilustre Colegio de Abogados de [COLEGIO DE ABOGADOS], y DIGO:

Que por medio del presente escrito y en la representación que ostento, interpongo DEMANDA DE MODIFICACIÓN DE MEDIDAS DEFINITIVAS adoptadas en sentencia de [ELEGIR: divorcio / separación] dictada en el procedimiento [ELEGIR: de mutuo acuerdo / contencioso], seguido ante este Tribunal al cual me dirijo, número de procedimiento [Nº DE PROCEDIMIENTO], en solicitud de reducción de la pensión de alimentos establecida en favor del hijo menor de los cónyuges, contra D./Dª [NOMBRE Y APELLIDOS DEL DEMANDADO], mayor de edad, con DNI/NIF [DNI/NIF] y con domicilio, a efectos de citación y emplazamiento, en [DOMICILIO].

La presente demanda se basa en los siguientes

HECHOS

PRIMERO.- En fecha [DÍA] de [MES] de [AÑO] se dictó por el Tribunal al que me dirijo sentencia en el procedimiento de [ELEGIR: divorcio / separación] de mutuo acuerdo núm. [Nº DE PROCEDIMIENTO], en la que se procedió a homologar el convenio regulador de fecha [DÍA] de [MES] de [AÑO], presentado por las partes.

[NOTA: si el procedimiento fue contencioso, las referencias que se hacen a continuación al convenio regulador judicialmente homologado deberán sustituirse por referencias a las medidas adoptadas por el Tribunal en la sentencia.]

En la estipulación [Nº DE ESTIPULACIÓN] del citado convenio regulador, en la que se determina la contribución a las cargas familiares y alimentos, se establece una pensión alimenticia de [IMPORTE EN LETRA] euros ([IMPORTE] €), a cargo de mi representado/a, en favor del hijo menor de la pareja, y único de mi representado/a en aquella fecha, [NOMBRE Y APELLIDOS DEL HIJO/A], de periodicidad mensual y actualizable anualmente de acuerdo con las variaciones que experimente el IPC. El tenor literal de la citada estipulación es el siguiente: [TRANSCRIPCIÓN DE LA ESTIPULACIÓN EN LA QUE SE FIJA LA PENSIÓN DE ALIMENTOS].

Se acompaña testimonio de la citada sentencia, en el que consta su firmeza, así como del convenio regulador que la misma homologaba, como DOCUMENTO Nº [Nº DE DOCUMENTO], con remisión, a efectos probatorios, a los archivos de este Tribunal.

SEGUNDO.- Desde que se dictó la citada sentencia se ha producido una alteración sustancial y permanente de las circunstancias que se tuvieron en cuenta para fijar la referida pensión de alimentos. Ello es debido al nacimiento, en fecha [DÍA] de [MES] de [AÑO], de [Nº DE NUEVOS HIJOS] nuevo/s hijo/s de mi representado/a, de nombre [NOMBRE/S DE LOS NUEVOS HIJOS], a los que éste/a tiene igualmente obligación de mantener.

Se acompañan como DOCUMENTOS Nº [Nº] y [Nº] certificación literal de la inscripción de nacimiento de los citados hijos en el Registro Civil de [LOCALIDAD], expedida por el mismo.

TERCERO.- Los hechos anteriores inciden directamente en la capacidad económica de mi representado/a, cuyos ingresos no han variado desde que se dictó la citada sentencia, para atender al pago de la pensión alimenticia, pues ello le deja sin ingresos suficientes para contribuir a los gastos más perentorios de sus nuevos hijos, cuando lo cierto es que todos sus hijos tienen igual derecho a ser mantenidos por su progenitor.

[OPCIONAL — incluir si procede]

Por otra parte, su actual pareja, [ELEGIR: madre / padre] de los nuevos hijos, se halla en situación de paro laboral desde el día [DÍA] de [MES] de [AÑO], cobrando un subsidio de desempleo de [IMPORTE EN LETRA] euros ([IMPORTE] €) mensuales, claramente insuficiente para atender las necesidades de sus hijos.

Se acompañan como DOCUMENTOS Nº [Nº] a [Nº] los siguientes: [RELACIÓN DE DOCUMENTOS], justificativos de los hechos descritos.

CUARTO.- Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial. En este sentido, se acudió a [INDICAR EL MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO] [DOCUMENTO QUE ACREDITA EL INTENTO DE SOLUCIÓN EXTRAJUDICIAL].

Resultan aplicables a los citados hechos los siguientes

FUNDAMENTOS DE DERECHO

I. COMPETENCIA.- Es competente el Tribunal al que me dirijo, de acuerdo con el artículo 769 de la Ley de Enjuiciamiento Civil, en relación con el artículo 775 de la misma Ley.

II. PROCEDIMIENTO.- Conforme al art. 775.2 de la Ley de Enjuiciamiento Civil es pertinente seguir el procedimiento por los cauces del juicio verbal, con las especialidades del art. 770 de la misma Ley.

III. LEGITIMACIÓN.- La de ambas partes deriva del artículo 775 de la Ley de Enjuiciamiento Civil y de los artículos 90 y 91 del Código Civil. Conforme al art. 749.2 de la Ley de Enjuiciamiento Civil, debe intervenir el Ministerio Fiscal, por encontrarse interesados menores.

IV. REPRESENTACIÓN Y DEFENSA.- El/La demandante comparece representado/a y defendido/a, respectivamente, por el Procurador y el Letrado que constan en el encabezamiento de este escrito, de acuerdo con lo dispuesto en el artículo 750 de la Ley de Enjuiciamiento Civil, en relación con los artículos 770 y 775.2 de la misma Ley.

V. CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.- La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4.º y 399.3, en relación con el art. 437.1 de la Ley de Enjuiciamiento Civil, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VI. DERECHO SUSTANTIVO.- El art. 154.III.1 del Código Civil, en relación con los arts. 142 y siguientes del mismo Código; en especial, el art. 145.1, según el cual cuando recaiga sobre dos o más personas la obligación de dar alimentos (como ocurre cuando ambos progenitores están obligados a prestarlos) se repartirá entre ellas el pago de la pensión en cantidad proporcional a su caudal respectivo; el art. 146, según el cual la cuantía de los alimentos será proporcionada al caudal o medios de quien los da y a las necesidades de quien los recibe; y el art. 147, en cuya virtud los alimentos se reducirán o aumentarán proporcionalmente según el aumento o disminución que sufran las necesidades del alimentista y la fortuna del que hubiese de satisfacerlos.

Así pues, cuando ambos progenitores vienen obligados a contribuir a la manutención de su hijo, la cuantía de los alimentos a cargo de cada uno de ellos debe venir determinada proporcionalmente en relación con la capacidad económica de uno y otro.

El art. 90.3, primer inciso, del Código Civil dispone: "Las medidas que el Juez adopte en defecto de acuerdo o las convenidas por los cónyuges judicialmente, podrán ser modificadas judicialmente o por nuevo convenio aprobado por el Juez, cuando así lo aconsejen las nuevas necesidades de los hijos o el cambio de las circunstancias de los cónyuges", en relación con el art. 775.1 de la Ley de Enjuiciamiento Civil, que regula la modificación de las medidas definitivas y que señala: "El Ministerio Fiscal, habiendo hijos menores o con discapacidad y, en todo caso, los cónyuges, podrán solicitar del tribunal que acordó las medidas definitivas, la modificación de las medidas convenidas por los cónyuges o de las adoptadas en defecto de acuerdo, siempre que hayan variado sustancialmente las circunstancias tenidas en cuenta al aprobarlas o acordarlas". En el mismo sentido, el art. 91 del Código Civil señala que las medidas judiciales "podrán ser modificadas cuando se alteren sustancialmente las circunstancias".

De lo anterior resulta que el incremento sustancial de los gastos de mi representado/a como consecuencia del nacimiento de nuevos hijos, a cuyas necesidades también debe atender, supone una alteración sustancial y tendencialmente permanente de las circunstancias que se tuvieron en cuenta al fijar el montante de la pensión y afecta a su capacidad económica que, junto con las necesidades del alimentista, constituye parámetro a tener en cuenta para establecer la cuantía de la pensión. En atención a todo ello, la pensión a cargo de mi representado/a debe ser reajustada con el fin de recuperar el equilibrio perdido, en el sentido de disminuirse su cuantía.

Cierto que el nacimiento de los nuevos hijos fruto de una nueva unión ha sido un acto voluntario y libre y podría sostenerse que, desde ese punto de vista, no puede redundar en perjuicio del hijo del primer matrimonio, pero sobre esta consideración deben sobreponerse las siguientes: mi representado/a no solicita una disminución del montante de la pensión a su cargo porque así deba resultar automáticamente del nacimiento de sus nuevos hijos (conviene insistir en este extremo, dado que existe jurisprudencia consolidada negando este automatismo y exigiendo, para que se modifique la pensión, disminución de ingresos en el obligado al pago o que aquéllos con los que cuente sean insuficientes para asistir debidamente a todos sus hijos si no se produce la rebaja solicitada), sino porque, dada su situación económica, aquél no puede soportar la carga sin menoscabo de otros derechos igualmente atendibles, como lo son los de sus nuevos hijos, lo que no puede dejar de ser ponderado a los efectos expuestos. Otra cosa supondría romper la proporcionalidad entre la capacidad económica del alimentante y la cuantía de la pensión tenida en cuenta en el momento de fijarse ésta y, al mismo tiempo, implicaría un trato desigual de los hijos habidos de distintas uniones.

Por lo expuesto,

SUPLICO AL TRIBUNAL:

Que, tras admitir este escrito con los documentos que lo acompañan y sus copias, me tenga por comparecido y parte en la representación que ostento, entendiéndose conmigo las sucesivas diligencias, y tenga por interpuesta DEMANDA DE MODIFICACIÓN DE MEDIDAS DEFINITIVAS DE [ELEGIR: DIVORCIO / SEPARACIÓN], que habrá de sustanciarse por los trámites del juicio verbal con las especialidades del art. 770 de la Ley de Enjuiciamiento Civil, conforme a lo establecido en el art. 775.2 de la misma Ley, contra D./Dª [NOMBRE Y APELLIDOS DEL DEMANDADO]; y, previos los trámites legales que procedan, entre ellos el traslado de la presente demanda al/a la demandado/a y al Ministerio Fiscal, dicte resolución por la que se modifiquen las medidas dictadas en la sentencia de [ELEGIR: divorcio / separación] dictada por el Tribunal de Instancia de [SEDE] en fecha [DÍA] de [MES] de [AÑO], procedimiento núm. [Nº DE PROCEDIMIENTO], en los siguientes extremos: pensión de alimentos fijada en favor del hijo menor de los cónyuges, [NOMBRE Y APELLIDOS DEL HIJO/A], resolviendo su disminución a la cantidad de [IMPORTE EN LETRA] euros ([IMPORTE] €) mensuales, o la que el Tribunal considere justa, a satisfacer dentro de los cinco primeros días de cada mes y actualizable anualmente de acuerdo con las variaciones del IPC, debido a la alteración sustancial de las circunstancias que se tuvieron en cuenta cuando se estableció dicha pensión alimenticia, en concreto, debido al nacimiento de nuevos hijos del obligado al pago y a la insuficiencia de sus ingresos para atenderlos a todos ellos convenientemente si no se estima lo solicitado.

OTROSÍ DIGO.- En cumplimiento de lo dispuesto en el art. 253 de la Ley de Enjuiciamiento Civil, esta parte fija la cuantía del procedimiento, calculada de acuerdo con lo dispuesto en el art. 251.7 de la misma Ley, en [IMPORTE] euros.

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma y número del Letrado Firma del Procurador

NOTA EXPLICATIVA.- La Ley de Jurisdicción Voluntaria modificó la redacción del art. 90.3 del Código Civil, sustituyendo la anterior expresión «cuando se alteren sustancialmente las circunstancias» por la actual «cuando así lo aconsejen las nuevas necesidades de los hijos o el cambio de las circunstancias de los cónyuges». Aunque en teoría esto podría plantear la duda de si la alteración de circunstancias que fundamenta la modificación de la medida debe ser sustancial, debe interpretarse la norma en el mismo sentido que la anterior y, por tanto, requiriendo sustancialidad en el cambio de circunstancias. En este sentido juega el tenor del art. 775 de la Ley de Enjuiciamiento Civil y del art. 91 del Código Civil, que mantienen expresamente este requisito y que deben ser objeto de interpretación sistemática junto con el art. 90.3 del Código Civil.
