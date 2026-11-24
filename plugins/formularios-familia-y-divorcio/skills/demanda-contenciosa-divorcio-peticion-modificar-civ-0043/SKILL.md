---
name: demanda-contenciosa-divorcio-peticion-modificar-civ-0043
description: "Demanda contenciosa de divorcio con petición de modificar la pensión de alimentos. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda contenciosa de divorcio con petición de modificar la pensión de alimentos

> Formulario **CIV-0043** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda contenciosa de divorcio con petición de modificar la pensión de alimentos» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda contenciosa de divorcio con petición de modificar la pensión de alimentos” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-contenciosa-divorcio-peticion-modificar-civ-0043`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (8 veces)
- [ ] LOCALIDAD (8 veces)
- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] Nº DE DOCUMENTO (8 veces)
- [ ] AÑO (7 veces)
- [ ] DÍA (6 veces)
- [ ] MES (6 veces)
- [ ] Nº (4 veces)
- [ ] CALLE (2 veces)
- [ ] FU (2 veces)
- [ ] CATEGORÍA PROFESIONAL
- [ ] COLEGIO
- [ ] DATOS DE LA SENTENCIA
- [ ] DENOMINACIÓN SOCIAL
- [ ] DESCRIBIR
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] Nº DE ESTIPULACIÓN
- [ ] Nº DE OFICINA
- [ ] NÚMERO
- [ ] NÚMERO DE LA CALLE
- [ ] PROFESIÓN
- [ ] SEDE
- [ ] TEXTO LITERAL DE LA ESTIPULACIÓN

## Normas que cita el formulario

- art. 85.1 LOPJ
- art. 770 LEC
- art. 749.1 LEC
- art. 750 LEC
- art. 775.2 LEC
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 146 CC
- art. 147 CC
- art. 152.2 CC
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

### Avisos de actualización (3) — se aplican en el texto, nunca se copian en el documento

- Junto a «…nes específicas de "familia", deberá dirigirse la demanda a la Sección Civil. DE»: Denominación legal: Sección de Familia, Infancia y Capacidad. Si no existe en el partido, conoce la Sección Civil o la Única (art. 86.3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…amilia, Infancia y Capacidad del Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).
- Junto a «…petente la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia de»: Un solo TI por partido judicial (art. 84.1 LOPJ): sobra «de los de». Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

A LA SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD DEL TRIBUNAL DE INSTANCIA En las demarcaciones judiciales en las que no se haya creado Tribunal con funciones específicas de "familia", deberá dirigirse la demanda a la Sección Civil. DE

D./Dª [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en nombre y representación de D./Dª [NOMBRE Y APELLIDOS], mayor de edad, con domicilio en [LOCALIDAD], calle [CALLE], nº [NÚMERO], pta., cuya representación acreditaré mediante comparecencia apud acta cuando sea requerido para ello, comparezco en este TRIBUNAL con la asistencia del Letrado D. /Dª [NOMBRE Y APELLIDOS], del Ilustre Colegio de Abogados de [COLEGIO], y DIGO:

Que por medio del presente escrito y en la representación que ostento, interpongo DEMANDA CONTENCIOSA DE DIVORCIO CON SOLICITUD DE MODIFICACIÓN DE PENSIÓN DE ALIMENTOS ACORDADA EN PROCESO PREVIO DE SEPARACIÓN MATRIMONIAL. La presente demanda se basa en los siguientes

PRIMERO.- Don [NOMBRE Y APELLIDOS] y Doña [NOMBRE Y APELLIDOS] contrajeron entre sí matrimonio civil en la ciudad de [LOCALIDAD], el día [DÍA] de [MES] de [AÑO]. Dicho matrimonio consta inscrito en el Registro civil de dicha ciudad.

Se acompaña como DOCUMENTO NUM. certificado literal de matrimonio, expedido por el Encargado del Registro Civil.

SEGUNDO.- De dicho matrimonio nació en [LOCALIDAD] un hijo/a, [NOMBRE Y APELLIDOS] el día [DÍA] de [MES] de [AÑO], cuyo nacimiento consta inscrito en el Registro civil de dicha ciudad.

Se acompaña como DOCUMENTO NUM. certificado de nacimiento, expedido por el Encargado del Registro Civil.

Desde hace años el domicilio conyugal ha estado establecido en esta ciudad de [LOCALIDAD] en la calle [CALLE] núm. [NÚMERO DE LA CALLE]

TERCERO.- Como consecuencia de la crisis de su matrimonio, los cónyuges formularon demanda de separación de mutuo acuerdo que se siguió ante la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia de [SEDE], plaza n.º [Nº] esta ciudad, al número [Nº]/[AÑO] de procedimiento, recayendo sentencia de separación por la que además se homologaron las medidas propuestas en el convenio aportado por los demandantes.

Se acompaña como DOCUMENTO NUM. testimonio de la sentencia y del convenio.

CUARTO.- La situación de separación, con cese ininterrumpido de la convivencia, se ha mantenido hasta la actualidad, habiendo decidido mi representado/a solicitar el divorcio, sin que haya sido posible proceder de común acuerdo los cónyuges.

QUINTO.- En relación con las medidas definitivas acordadas por los esposos en el convenio regulador de su separación matrimonial y homologadas por el Tribunal en el procedimiento de separación a que se ha hecho referencia en el HECHO TERCERO de esta demanda, mi representado, considera que deben mantenerse algunas y modificarse otras.

En concreto, deben mantenerse tras el divorcio las medidas relativas a [DESCRIBIR]

Por el contrario, procede modificar la medida relativa a los alimentos a favor del hijo menor por alteración sustancial y permanente de las circunstancias que se tuvieron en cuenta al fijar la pensión alimenticia en la sentencia previa de separación, tal y como se expone a continuación.

SEXTO.- Acción que se ejercita. La estipulación [Nº DE ESTIPULACIÓN] del Convenio regulador de los efectos de la separación, en la que se regulaba la contribución a las cargas familiares y alimentos, se estableció, a cargo de mi representado/a, una pensión alimenticia de [IMPORTE] euros ( €) en favor del hijo menor de la pareja, de periodicidad mensual y actualizable anualmente de acuerdo con las variaciones que experimente el IPC. El tenor literal de la citada estipulación es el siguiente: [TEXTO LITERAL DE LA ESTIPULACIÓN].

SÉPTIMO.- Mi representado/a ha venido satisfaciendo puntualmente hasta la fecha la pensión de alimentos convenida.

OCTAVO.- Cuando se dictó la citada sentencia de separación, mi representado/a ocupaba un puesto de trabajo en la empresa [DENOMINACIÓN SOCIAL], con la categoría de [CATEGORÍA PROFESIONAL], por el que percibía un salario de [IMPORTE] euros ( €) netos mensuales.

Desde entonces, sus circunstancias laborales han variado de modo sustancial, conduciéndolo/a a una situación en la que apenas dispone de medios propios para subsistir. Se debe esto a que en fecha [DÍA] de [MES] de [AÑO], fue objeto de despido laboral como consecuencia de los ajustes de plantilla realizados en su empresa, gravemente afectada por la crisis económica que ha incidido de modo importante en el sector económico en el que aquélla se mueve - la construcción -, despido por el que cobró, en concepto de indemnización, la cantidad de [IMPORTE] euros ( €), que le ha permitido subsistir e ir satisfaciendo hasta el momento actual la pensión alimenticia en favor de su hijo. Por otra parte, la cantidad que cobra en la actualidad como prestación por desempleo, de [IMPORTE] euros ( €), es claramente insuficiente para atender a sus necesidades más perentorias y, además, satisfacer la pensión de alimentos fijada en la sentencia de divorcio [DATOS DE LA SENTENCIA].

Pese a realizar esfuerzos continuos para encontrar un nuevo trabajo, lo cierto es que no lo ha conseguido y finalmente, se ha trasladado al domicilio de sus padres que actualmente lo mantienes al no poder él cubrir sus gastos más elementales, pues, agotada la indemnización por despido, carece de patrimonio y no obtiene más ingresos que el referido subsidio de desempleo, que dejará de percibir en fecha [DÍA] de [MES] de [AÑO].

Se acompaña los siguientes documentos con el fin de acreditar los hechos expuestos: carta de despido, como DOCUMENTO Nº [Nº DE DOCUMENTO]; declaración de la renta de los dos últimos años como DOCUMENTOS Nº [Nº DE DOCUMENTO] y Nº [Nº DE DOCUMENTO]; justificante de hallarse inscrito en la oficina de empleo, como DOCUMENTO Nº [Nº DE DOCUMENTO]; justificante de la cuantía del subsidio por desempleo que ha percibido en los siguientes periodos: y la que percibe en la actualidad, como DOCUMENTO Nº [Nº DE DOCUMENTO];

Las circunstancias descritas alteran sustancialmente las tenidas en cuenta cuando se fijó la pensión alimenticia, en el contexto de las relaciones y posiciones contempladas para su fijación, quedando patente que tanto cualitativa como cuantitativamente aquéllas suponen un cambio sustancial y profundo, que exige ajustar la pensión a la nueva situación.

NOVENO.- El otro progenitor y parte demandada en este procedimiento de divorcio, D./Dª [NOMBRE Y APELLIDOS], se encuentra, en cambio, en una holgada situación económica, gracias a los elevados ingresos que obtiene como [PROFESIÓN]. Además dispone de varios inmuebles de su propiedad. Por todo lo cual tiene capacidad económica suficiente para atender a las necesidades de su hijo.

Para acreditarlo, se acompañan, como DOCUMENTOS Nº [Nº DE DOCUMENTO] y Nº [Nº DE DOCUMENTO], los siguientes: Certificaciones expedidas por los Registros de la Propiedad de [LOCALIDAD] y [LOCALIDAD] (oficinas núms. y [Nº DE OFICINA], respectivamente) en las que consta la propiedad de D./Dª [NOMBRE Y APELLIDOS], sobre dos pisos ubicados en las citadas localidades

DÉCIMO.- En consecuencia, se reclama que se declare extinguida la obligación de prestación de alimentos que en su día se fijó en el citado Convenio regulador de los efectos de la separación, o, en su defecto, se suspenda temporalmente, mientras persistan las circunstancias que han conducido a mi representado/a a la situación de incapacidad económica para prestar aquellos alimentos, en la que se encuentra. De no estimarse lo anterior, se solicita una reducción de la pensión a [IMPORTE] euros ( €) mensuales, en lugar de los [IMPORTE] euros ( €) actuales.

Concurren en el caso presente, todos los requisitos para ello, a saber: alteración sustancial de las circunstancias que se tuvieron en cuenta al establecer la pensión de alimentos, por nuevos hechos posteriores a la sentencia en la que se fijó aquélla, que determinan la disminución de ingresos de mi representado/a, disminución que porcentualmente puede fijarse en un [Nº] por ciento ( %); situación tendencialmente permanente, sobre todo en la actual coyuntura de crisis económica, no siendo previsible que pueda variar a corto plazo; situación no provocada por la voluntad o negligencia de mi representado; y acreditación de la referida alteración mediante los documentos que se acompañan y el resto de pruebas que, de ser aceptadas por el Juez, se practiquen en el momento procesal oportuno.

DÉCIMO PRIMERO.- En cumplimiento de lo previsto en el art. 81.2º, último inciso, en relación con el art. 86 del Código civil, adjunto aportamos como DOCUMENTO NUM. propuesta de medidas definitivas de los efectos del divorcio.

Resultan aplicables a los citados hechos los siguientes

DÉCIMO SEGUNDO.- Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

FUNDAMENTOS DE DERECHO

Competencia

Es competente la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia de la ciudad de [LOCALIDAD], al que se dirige esta demanda, al amparo del artículo 769.2 de la L.E.C., en relación con lo dispuesto en el art. 85.1º LOPJ.

Procedimiento

Deberá seguirse la demanda por los cauces procedimentales previstos para el divorcio contencioso en el artículo 770 de la LEC.

[FU]

Legitimación

Está legitimado activamente para solicitar el divorcio cualquiera de los cónyuges, en este caso mi representado/a, ostentando legitimación pasiva el otro cónyuge.

En relación con la petición de modificación de medidas, está igualmente legitimado mi representado/a, correspondiendo la legitimación pasiva al otro cónyuge.

Debe ser parte el Ministerio Fiscal al haber hijos menores de edad, al amparo del art. 749.1 de la LEC.

Representación y defensa

El/La demandante comparece representado y defendido, respectivamente, por el Procurador y el Letrado que constan en el encabezamiento de este escrito, de acuerdo con lo dispuesto en el artículo 750 LEC, en relación con los artículos 775.2 y 770 LEC.

Cumplimiento de los requisitos de procedibilidad.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

Acción que se ejercita

Se ejercita en la presente demanda acción contenciosa de disolución del matrimonio por divorcio, al amparo de los artículo 81 y 86 del código civil, habiendo transcurrido más de tres meses desde la celebración del matrimonio.

Asimismo se solicita la adopción de las medidas judiciales definitivas en el sentido expresado en la Propuesta de medidas definitivas que se acompaña a esta demanda.

Derecho sustantivo

Arts. 81, 86 y 90 a 97 del Código civil.

El art. 154.III.1 CC, en relación con los arts. 142 y ss del Código civil en la nueva redacción dada por la Ley 8/2021, de 2 de junio; en especial, el art. 146 CC, según el cual, la cuantía de los alimentos será proporcionada al caudal o medios de quien los da y a las necesidades de quien los recibe; el art. 147 CC, en cuya virtud, los alimentos se reducirán o aumentarán proporcionalmente según el aumento o disminución que sufran las necesidades del alimentista y la fortuna del que hubiese de satisfacerlos, y el art. 152.2º CC, a cuyo tenor, cesará la obligación de dar alimentos cuando la fortuna del obligado a darlos se hubiese reducido hasta el punto de no poder satisfacerlos sin desatender sus propias necesidades.

De lo anterior resulta que la reducción de los medios económicos del obligado al pago constituye motivo suficiente que justifica una modificación de la pensión de alimentos cuando supone una modificación sustancial y con visos de permanencia respecto de las circunstancias existentes en el momento de su adopción. Estos requisitos se cumplen en el presente caso, dado que la situación de desempleo de mi representado/a, que tuvo su origen en los ajustes de plantilla provocados por la actual crisis económica, dura ya [Nº] años y dada la edad de aquél/ella ( años) y la coyuntura económica actual puede considerarse que la situación de desempleo se haya consolidada o tiene visos de permanencia. La actual situación de mi representado es sustancialmente diferente a la que se tuvo en cuenta al dictar la sentencia en que se fijó la pensión, pues entonces se hallaba trabajando y percibía un sueldo de [IMPORTE] euros ( €) mensuales, muy superior a los [IMPORTE] euros ( €) mensuales que cobra en la actualidad en concepto de subsidio de desempleo y que dejará de percibir en fecha [DÍA] de [MES] de [AÑO], por finalizar el periodo durante el cual tiene derecho a aquél según la Ley.

La citada cantidad no alcanza a satisfacer las necesidades básicas de mi representado, por lo que mucho menos es suficiente para poder prestar alimentos. Pero, aun de no considerarlo así el Tribunal, procede, al menos, reducir la cuantía de la pensión inicialmente fijada a la vista de la disminución de los ingresos del obligado a su pago, de modo que se mantenga la proporcionalidad entre estos y la cantidad a satisfacer. Lo cual no obsta a que si en un futuro se produce una nueva alteración sustancial de las circunstancias, a favor o en contra de mi representado, se proceda a una nueva modificación de la pensión.

[FU]

Costas

Procede imponer al/a la demandado/a el pago de las costas, en virtud de lo dispuesto en el art. 394 LEC, en la medida en que se oponga a la presente demanda.

Iura novit curia

Y las demás normas que resulten procedentes.

Por lo expuesto:

SUPLICO AL TRIBUNAL que, tras admitir este escrito con los documentos que lo acompañan, me tenga por comparecido y parte en la representación que ostento, entendiéndose conmigo las sucesivas diligencias, y tenga por interpuesta DEMANDA CONTENCIOSA DE DIVORCIO y, previos los trámites procesales previstos en el art. 770 de la Ley de Enjuiciamiento Civil, dicte en su día sentencia por la que, estimando íntegramente la demanda, se decrete la disolución por divorcio del matrimonio contraído por mi representado/a y el/la demandado/a entre sí, con aprobación de las medidas que se contienen en la propuesta de medidas definitivas que se acompaña, con imposición de costas al/ a la demandado/a en caso de que se oponga a estas pretensiones, conforme con lo dispuesto en el art. 394 de la Ley de Enjuiciamiento Civil. Solicito así mismo, que se acuerde lo procedente para la constancia de la citada sentencia en el Registro civil.

En [LOCALIDAD], a [DÍA], de [MES], de [AÑO]

Firma y número del Letrado

Firma del Procurador

========================================================================
