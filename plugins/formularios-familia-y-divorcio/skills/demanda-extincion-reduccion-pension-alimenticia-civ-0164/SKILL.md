---
name: demanda-extincion-reduccion-pension-alimenticia-civ-0164
description: "Demanda de extinción o reducción de la pensión alimenticia por disminución de ingresos del obligado. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de extinción o reducción de la pensión alimenticia por disminución de ingresos del obligado

> Formulario **CIV-0164** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda de modificación de medidas definitivas (arts. 90, 91 CC y 775 LEC) por la que el progenitor obligado al pago pide la extinción, la suspensión o, subsidiariamente, la reducción de la pensión de alimentos de un hijo menor, por la disminución sustancial y no voluntaria de sus ingresos (por ejemplo, tras un despido) y la mejor situación económica del otro progenitor.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de extinción o reducción de la pensión alimenticia por disminución de ingresos del obligado» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de extinción o reducción de la pensión alimenticia por disminución de ingresos del obligado” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-extincion-reduccion-pension-alimenticia-civ-0164`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (11 veces)
- [ ] IMPORTE (10 veces)
- [ ] AÑO (9 veces)
- [ ] DÍA (9 veces)
- [ ] IMPORTE EN LETRA (9 veces)
- [ ] MES (9 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] Nº DE DOCUMENTO (5 veces)
- [ ] NOMBRE Y APELLIDOS DEL DEMANDADO (4 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL HIJO/A (2 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] CATEGORÍA PROFESIONAL
- [ ] CAUSA
- [ ] COLEGIO DE ABOGADOS
- [ ] DNI/NIF
- [ ] DOCUMENTO QUE ACREDITA EL INTENTO DE SOLUCIÓN EXTRAJUDICIAL
- [ ] DOMICILIO
- [ ] EDAD
- [ ] EMPRESA
- [ ] INDICAR EL MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] NOMBRE DEL HIJO/A
- [ ] NOMBRE Y APELLIDOS DEL DEMANDANTE
- [ ] NOMBRE Y APELLIDOS DEL LETRADO
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº DE ESTIPULACIÓN
- [ ] O SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD
- [ ] PERIODOS
- [ ] PORCENTAJE
- [ ] PROFESIÓN U OCUPACIÓN
- [ ] SEDE

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

Que por medio del presente escrito y en la representación que ostento, interpongo DEMANDA DE MODIFICACIÓN DE MEDIDAS DEFINITIVAS adoptadas en sentencia de [ELEGIR: divorcio / separación] dictada en el procedimiento [ELEGIR: de mutuo acuerdo / contencioso], seguido ante este Tribunal al cual me dirijo, número de procedimiento [Nº DE PROCEDIMIENTO], en solicitud de extinción o, subsidiariamente, reducción de la pensión de alimentos establecida en favor del hijo menor común de las partes, contra D./Dª [NOMBRE Y APELLIDOS DEL DEMANDADO], mayor de edad, con DNI/NIF [DNI/NIF] y con domicilio, a efectos de citación y emplazamiento, en [DOMICILIO].

La presente demanda se basa en los siguientes

HECHOS

PRIMERO.- D./Dª [NOMBRE Y APELLIDOS] y D./Dª [NOMBRE Y APELLIDOS] contrajeron entre sí matrimonio civil en la ciudad de [LOCALIDAD], el día [DÍA] de [MES] de [AÑO]. Dicho matrimonio consta inscrito en el Registro Civil de dicha ciudad, [DATOS REGISTRALES: Tomo, libro, página].

Se acompaña como DOCUMENTO Nº [Nº DE DOCUMENTO] certificado literal de matrimonio, expedido por el Registro Civil.

SEGUNDO.- De dicho matrimonio nació en [LOCALIDAD] un hijo/a, [NOMBRE DEL HIJO/A], el día [DÍA] de [MES] de [AÑO], cuyo nacimiento consta inscrito en el Registro Civil de dicha ciudad, [DATOS REGISTRALES: Tomo, libro, página].

Se acompaña como DOCUMENTO Nº [Nº DE DOCUMENTO] certificado literal de nacimiento, expedido por el Registro Civil.

TERCERO.- Como consecuencia de la crisis de su matrimonio, los cónyuges formularon demanda de [ELEGIR: divorcio / separación] de mutuo acuerdo que se siguió ante este Tribunal al que me dirijo, con el número [Nº DE PROCEDIMIENTO], recayendo, en fecha [DÍA] de [MES] de [AÑO], sentencia de [ELEGIR: divorcio / separación], en la que se procedió a homologar el convenio regulador de fecha [DÍA] de [MES] de [AÑO], presentado por las partes.

[NOTA: si el procedimiento fue contencioso, las referencias que se hacen al convenio regulador judicialmente homologado deberán sustituirse por referencias a las medidas adoptadas por el Tribunal en la sentencia.]

En la estipulación [Nº DE ESTIPULACIÓN] del citado convenio, en la que se regula la contribución a las cargas familiares y alimentos, se establece una pensión alimenticia de [IMPORTE EN LETRA] euros ([IMPORTE] €) en favor del hijo menor de la pareja, [NOMBRE Y APELLIDOS DEL HIJO/A], de periodicidad mensual y actualizable anualmente de acuerdo con las variaciones que experimente el IPC. El tenor literal de la citada estipulación es el siguiente: [TRANSCRIPCIÓN DE LA ESTIPULACIÓN EN LA QUE SE FIJA LA PENSIÓN DE ALIMENTOS].

Se acompaña testimonio de la citada sentencia, en el que consta su firmeza, así como del convenio regulador que la misma homologaba, como DOCUMENTO Nº [Nº DE DOCUMENTO], con remisión, a efectos probatorios, a los archivos de este Tribunal.

CUARTO.- Mi representado/a ha venido satisfaciendo puntualmente hasta la fecha la pensión de alimentos convenida.

QUINTO.- Cuando se dictó la citada sentencia, mi representado/a ocupaba un puesto de trabajo en la empresa [EMPRESA], con la categoría de [CATEGORÍA PROFESIONAL], por el que percibía un salario de [IMPORTE EN LETRA] euros ([IMPORTE] €) netos mensuales.

Desde que se dictó la referida sentencia, las circunstancias laborales de mi representado/a han variado de modo sustancial, conduciéndolo a una situación en la que apenas dispone de medios propios para subsistir. Se debe esto a que, en fecha [DÍA] de [MES] de [AÑO], fue objeto de despido laboral como consecuencia de [CAUSA DEL DESPIDO: p. ej., los ajustes de plantilla realizados en su empresa, afectada por la situación del sector económico en el que se mueve], despido por el que cobró, en concepto de indemnización, la cantidad de [IMPORTE EN LETRA] euros ([IMPORTE] €), que le ha permitido subsistir e ir satisfaciendo hasta el momento actual la pensión alimenticia en favor de su hijo, además de pagar algunas deudas pendientes. Por otra parte, la cantidad que cobra en la actualidad como prestación por desempleo, de [IMPORTE EN LETRA] euros ([IMPORTE] €), es claramente insuficiente para atender a sus necesidades más perentorias y, además, satisfacer la pensión de alimentos fijada en la sentencia.

Pese a realizar esfuerzos continuos para encontrar un nuevo trabajo, lo cierto es que no lo ha conseguido y, finalmente, se ha trasladado al domicilio de sus padres, que actualmente lo mantienen al no poder él/ella cubrir sus gastos más elementales, pues, agotada la indemnización por despido, carece de patrimonio y no obtiene más ingresos que el referido subsidio de desempleo, que dejará de percibir en fecha [DÍA] de [MES] de [AÑO].

Se acompañan los siguientes documentos con el fin de acreditar los hechos expuestos: carta de despido, como DOCUMENTO Nº [Nº]; declaración de la renta de los dos últimos años, como DOCUMENTOS Nº [Nº] y Nº [Nº]; justificante de hallarse inscrito en la oficina de empleo, como DOCUMENTO Nº [Nº]; justificante de la cuantía de la prestación o subsidio por desempleo que ha percibido en los siguientes periodos: [PERIODOS], y la que percibe en la actualidad, como DOCUMENTO Nº [Nº]; y cualquier otro documento que sirva para probar los hechos alegados, p. ej., recibos de las deudas que hayan podido ser pagadas con la indemnización por despido para acreditar el consumo de su importe.

Las circunstancias descritas alteran sustancialmente las tenidas en cuenta cuando se fijó la pensión alimenticia, en el contexto de las relaciones y posiciones contempladas para su fijación, quedando patente que tanto cualitativa como cuantitativamente aquéllas suponen un cambio sustancial y profundo, que exige ajustar la pensión a la nueva situación.

SEXTO.- El otro progenitor y parte en el citado procedimiento, D./Dª [NOMBRE Y APELLIDOS DEL DEMANDADO], se encuentra, en cambio, en una holgada situación económica, gracias a los elevados ingresos que obtiene como [PROFESIÓN U OCUPACIÓN]. Además, dispone de varios inmuebles de su propiedad. Por todo lo cual tiene capacidad económica suficiente para atender a las necesidades de su hijo.

Para acreditarlo se acompañan, como DOCUMENTOS Nº [Nº] y Nº [Nº], los siguientes: certificaciones expedidas por los Registros de la Propiedad de [LOCALIDAD] y [LOCALIDAD] (oficinas núms. [Nº] y [Nº], respectivamente), en las que consta la propiedad de D./Dª [NOMBRE Y APELLIDOS DEL DEMANDADO] sobre los inmuebles ubicados en las citadas localidades, y los demás que se consideren convenientes y de los que disponga el solicitante.

SÉPTIMO.- En consecuencia, se reclama que se declare extinguida la obligación de prestación de alimentos que en su día se fijó en el citado convenio regulador o, en su defecto, que se suspenda temporalmente mientras persistan las circunstancias que han conducido a mi representado/a a la situación de incapacidad económica para prestar aquellos alimentos en la que se encuentra. De no estimarse lo anterior, se solicita una reducción de la pensión a [IMPORTE EN LETRA] euros ([IMPORTE] €) mensuales, en lugar de los [IMPORTE EN LETRA] euros ([IMPORTE] €) actuales.

Concurren en el caso presente todos los requisitos para ello, a saber: alteración sustancial de las circunstancias que se tuvieron en cuenta al establecer la pensión de alimentos, por nuevos hechos posteriores a la sentencia en la que se fijó aquélla, que determinan la disminución de ingresos de mi representado/a, disminución que porcentualmente puede fijarse en un [PORCENTAJE] por ciento; situación tendencialmente permanente, no siendo previsible que pueda variar a corto plazo; situación no provocada por la voluntad o negligencia de mi representado/a; y acreditación de la referida alteración mediante los documentos que se acompañan y el resto de pruebas que, de ser admitidas, se practiquen en el momento procesal oportuno.

OCTAVO.- Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial. En este sentido, se acudió a [INDICAR EL MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO] [DOCUMENTO QUE ACREDITA EL INTENTO DE SOLUCIÓN EXTRAJUDICIAL].

Resultan aplicables a los citados hechos los siguientes

FUNDAMENTOS DE DERECHO

I. COMPETENCIA.- Es competente el Tribunal al que me dirijo, de acuerdo con el artículo 769 de la Ley de Enjuiciamiento Civil, en relación con el artículo 775 de la misma Ley.

II. CAPACIDAD Y LEGITIMACIÓN.- Tiene mi mandante capacidad procesal, conforme a lo dispuesto en los artículos 6 y siguientes de la Ley de Enjuiciamiento Civil.

La legitimación de ambas partes deriva del artículo 775 de la Ley de Enjuiciamiento Civil y de los artículos 90 y 91 del Código Civil. Conforme al art. 749.2 de la Ley de Enjuiciamiento Civil, debe intervenir el Ministerio Fiscal, por encontrarse interesados menores.

III. PROCEDIMIENTO.- Arts. 770 y 775.2 de la Ley de Enjuiciamiento Civil.

IV. REPRESENTACIÓN Y DEFENSA.- El/La demandante comparece representado/a y defendido/a, respectivamente, por el Procurador y el Letrado que constan en el encabezamiento de este escrito, de acuerdo con lo dispuesto en el artículo 750 de la Ley de Enjuiciamiento Civil, en relación con los artículos 770 y 775.2 de la misma Ley.

V. CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.- La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4.º y 399.3, en relación con el art. 437.1 de la Ley de Enjuiciamiento Civil, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VI. DERECHO SUSTANTIVO.- El art. 90.3, primer inciso, del Código Civil dispone: "Las medidas que el Juez adopte en defecto de acuerdo o las convenidas por los cónyuges judicialmente, podrán ser modificadas judicialmente o por nuevo convenio aprobado por el Juez, cuando así lo aconsejen las nuevas necesidades de los hijos o el cambio de las circunstancias de los cónyuges". Su párrafo segundo, introducido por la Ley 17/2021, de 15 de diciembre, añade que podrá modificarse el convenio o solicitarse modificación de las medidas sobre los animales de compañía si se hubieran alterado gravemente sus circunstancias. Todo ello en relación con el art. 775.1 de la Ley de Enjuiciamiento Civil, que regula la modificación de las medidas definitivas y que señala: "El Ministerio Fiscal, habiendo hijos menores o con discapacidad y, en todo caso, los cónyuges, podrán solicitar del tribunal que acordó las medidas definitivas, la modificación de las medidas convenidas por los cónyuges o de las adoptadas en defecto de acuerdo, siempre que hayan variado sustancialmente las circunstancias tenidas en cuenta al aprobarlas o acordarlas". En el mismo sentido, el art. 91 del Código Civil señala que las medidas judiciales "podrán ser modificadas cuando se alteren sustancialmente las circunstancias".

El art. 154.III.1 del Código Civil, en relación con los arts. 142 y siguientes del mismo Código; en especial, el art. 146, según el cual la cuantía de los alimentos será proporcionada al caudal o medios de quien los da y a las necesidades de quien los recibe; el art. 147, en cuya virtud los alimentos se reducirán o aumentarán proporcionalmente según el aumento o disminución que sufran las necesidades del alimentista y la fortuna del que hubiese de satisfacerlos; y el art. 152.2.º, a cuyo tenor cesará la obligación de dar alimentos cuando la fortuna del obligado a darlos se hubiese reducido hasta el punto de no poder satisfacerlos sin desatender sus propias necesidades. Así pues, cuando ambos progenitores están obligados a contribuir a la manutención de su hijo, la cuantía de los alimentos a cargo de cada uno de ellos debe venir determinada proporcionalmente en relación con la capacidad económica de uno y otro.

De lo anterior resulta que la reducción de los medios económicos del obligado al pago constituye motivo suficiente que justifica una modificación de la pensión de alimentos cuando supone una modificación sustancial y con visos de permanencia respecto de las circunstancias existentes en el momento de su adopción. Estos requisitos se cumplen en el presente caso, dado que la situación de desempleo de mi representado/a, que tuvo su origen en [CAUSA], dura ya [Nº] años y, dada la edad de aquél/ella ([EDAD] años) y la coyuntura económica actual, puede considerarse que la situación de desempleo se halla consolidada o tiene visos de permanencia. La actual situación de mi representado/a es sustancialmente diferente a la que se tuvo en cuenta al dictar la sentencia en que se fijó la pensión, pues entonces se hallaba trabajando y percibía un sueldo de [IMPORTE EN LETRA] euros ([IMPORTE] €) mensuales, muy superior a los [IMPORTE EN LETRA] euros ([IMPORTE] €) mensuales que cobra en la actualidad en concepto de subsidio de desempleo y que dejará de percibir en fecha [DÍA] de [MES] de [AÑO], por finalizar el periodo durante el cual tiene derecho a aquél según la Ley.

La citada cantidad no alcanza a satisfacer las necesidades básicas de mi representado/a, por lo que mucho menos es suficiente para poder prestar alimentos. Pero, aun de no considerarlo así el Tribunal, procede, al menos, reducir la cuantía de la pensión inicialmente fijada a la vista de la disminución de los ingresos del obligado a su pago, de modo que se mantenga la proporcionalidad entre estos y la cantidad a satisfacer. Lo cual no obsta a que, si en un futuro se produce una nueva alteración sustancial de las circunstancias, a favor o en contra de mi representado/a, se proceda a una nueva modificación de la pensión.

VII. COSTAS.- Procede imponer al/a la demandado/a el pago de las costas, en virtud de lo dispuesto en el art. 394 de la Ley de Enjuiciamiento Civil, en la medida en que se oponga a la presente demanda.

VIII. Iura novit curia y las demás normas que resulten procedentes.

Por lo expuesto,

SUPLICO AL TRIBUNAL:

Que, tras admitir este escrito con los documentos que lo acompañan y sus copias, me tenga por comparecido y parte en la representación que ostento, entendiéndose conmigo las sucesivas diligencias, y tenga por interpuesta DEMANDA DE MODIFICACIÓN DE MEDIDAS DEFINITIVAS DE [ELEGIR: DIVORCIO / SEPARACIÓN], que habrá de sustanciarse por los trámites del juicio verbal, con las especialidades del art. 770 de la Ley de Enjuiciamiento Civil, conforme con lo establecido en el art. 775.2 de la misma Ley, contra D./Dª [NOMBRE Y APELLIDOS DEL DEMANDADO]; y, previos los trámites legales que procedan, entre ellos el traslado de la presente demanda al/a la demandado/a y al Ministerio Fiscal, dicte sentencia por la que, estimando íntegramente la demanda, se modifiquen las medidas dictadas en la sentencia de [ELEGIR: divorcio / separación] de fecha [DÍA] de [MES] de [AÑO], en los siguientes extremos: pensión de alimentos fijada en favor del hijo menor de los cónyuges, [NOMBRE Y APELLIDOS DEL HIJO/A], resolviendo la extinción de la misma o su suspensión mientras persistan las actuales circunstancias económicas y laborales de mi representado/a o, subsidiariamente, su reducción a la cantidad de [IMPORTE EN LETRA] euros ([IMPORTE] €) mensuales, o la que el Tribunal considere justa, a satisfacer dentro de los cinco primeros días de cada mes y actualizable anualmente de acuerdo con las variaciones del IPC, debido a la alteración sustancial de las circunstancias que se tuvieron en cuenta cuando se estableció dicha pensión alimenticia. Todo ello con expresa imposición de costas al/a la demandado/a si se opusiere a la presente demanda.

OTROSÍ DIGO.- En cumplimiento de lo dispuesto en el art. 253 de la Ley de Enjuiciamiento Civil, esta parte fija la cuantía del procedimiento, calculada de acuerdo con lo dispuesto en el art. 251.7 de la misma Ley, en [IMPORTE] euros.

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma y número del Letrado Firma del Procurador

NOTA EXPLICATIVA.- La Ley de Jurisdicción Voluntaria modificó la redacción del art. 90.3 del Código Civil, sustituyendo la anterior expresión «cuando se alteren sustancialmente las circunstancias» por la actual «cuando así lo aconsejen las nuevas necesidades de los hijos o el cambio de las circunstancias de los cónyuges». Aunque en teoría esto podría plantear la duda de si la alteración de circunstancias que fundamenta la modificación de la medida debe ser sustancial, debe interpretarse la norma en el mismo sentido que la anterior y, por tanto, requiriendo sustancialidad en el cambio de circunstancias. En este sentido juega el tenor del art. 775 de la Ley de Enjuiciamiento Civil y del art. 91 del Código Civil, que mantienen expresamente este requisito y que deben ser objeto de interpretación sistemática junto con el art. 90.3 del Código Civil.
