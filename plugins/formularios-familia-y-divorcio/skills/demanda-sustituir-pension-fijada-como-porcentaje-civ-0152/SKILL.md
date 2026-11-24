---
name: demanda-sustituir-pension-fijada-como-porcentaje-civ-0152
description: "Demanda para sustituir la pensión fijada como porcentaje de ingresos por una cantidad fija. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda para sustituir la pensión fijada como porcentaje de ingresos por una cantidad fija

> Formulario **CIV-0152** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda para sustituir la pensión fijada como porcentaje de ingresos por una cantidad fija» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda para sustituir la pensión fijada como porcentaje de ingresos por una cantidad fija” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-sustituir-pension-fijada-como-porcentaje-civ-0152`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] AÑO (6 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] Nº (5 veces)
- [ ] MES (4 veces)
- [ ] DÍA (3 veces)
- [ ] IMPORTE (3 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] NÚMERO (2 veces)
- [ ] SEDE (2 veces)
- [ ] CALLE
- [ ] COLEGIO
- [ ] FECHA
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] NIF
- [ ] NOMBRE DEL MENOR
- [ ] Nº DE PROCEDIMIENTO

## Normas que cita el formulario

- art. 769 LEC
- art. 775 LEC
- art. 90 CC
- art. 749.2 LEC
- art. 750 LEC
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 93.1 CC
- art. 90.2 CC
- art. 93 CC
- art. 90.3 CC
- art. 146 CC
- art. 394 LEC
- art. 770 LEC
- art. 775.2 LEC
- art. 253 LEC
- art. 251.7 LEC

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

- Junto a «…Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).
- Junto a «…2666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.

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

Que por medio del presente escrito y en la representación que ostento, interpongo DEMANDA DE MODIFICACIÓN DE MEDIDAS DEFINITIVAS, adoptadas en sentencia de divorcio o separación dictada en el procedimiento de mutuo acuerdo o contencioso, seguido ante este Tribunal al cual me dirijo, número de procedimiento /, contra D./Dª [NOMBRE Y APELLIDOS], mayor de edad, con DNI/NIF [NIF] y con domicilio, a efectos de citación y emplazamiento, en [LOCALIDAD], calle [CALLE], nº [NÚMERO], pta.. La presente demanda se basa en los siguientes

HECHOS

En fecha [DÍA] de [MES] de [AÑO], se dictó por el Tribunal al que me dirijo, sentencia en el procedimiento de divorcio o de separación de mutuo acuerdo núm. [Nº]/[AÑO] puede tratarse también de un procedimiento contencioso, en cuyo caso, las referencias que se hacen a continuación al convenio regulador judicialmente homologado, lo serían a las medidas adoptadas por el Juez, en la que se procedió a homologar el Convenio regulador de fecha [DÍA] de [MES] de [AÑO], presentado por las partes.

En la estipulación [Nº] del citado Convenio regulador, relativa a la contribución a las cargas familiares y alimentos, se establece una pensión alimenticia consistente en un [Nº] por ciento de los ingresos netos mensuales del progenitor no custodio en favor del hijo menor de la pareja, [NOMBRE DEL MENOR] nombre y apellidos del hijo. El tenor literal de la citada estipulación es el siguiente: se transcribe la estipulación en la que se fija la pensión de alimentos.

Se acompaña testimonio de la citada sentencia, en el que consta su firmeza, así como del convenio regulador que la misma homologaba, como DOCUMENTO Nº con remisión, a efectos probatorios, a los archivos de este Tribunal.

SEGUNDO.- Aunque ambos cónyuges estuvieron de acuerdo en su momento solo en el caso de que el procedimiento fuese de mutuo acuerdo y se hubiese pactado este tipo de pensión en el Convenio regulador en fijar la pensión alimenticia por referencia a un porcentaje de los ingresos del obligado a su pago, lo cierto es que el paso del tiempo ha demostrado que esta forma de determinación de la cuantía provoca inseguridad y fomenta la arbitrariedad en el cálculo de la pensión, pues el obligado a su pago no cuenta con un salario fijo que permita proceder a un cálculo objetivo de la suma concreta, siendo frecuentes las discusiones de los progenitores por esta cuestión lo que afecta negativamente a su relación en perjuicio de su hijo. Por ello, se solicita la modificación de la pensión en el sentido de determinar una cantidad fija a satisfacer con periodicidad mensual y actualizable de acuerdo con el IPC, estimándose dicha cantidad en [IMPORTE] euros ( €), que resulta de obtener la media de los satisfecho durante los últimos doce meses.

Se acompaña como DOCUMENTO Nº [Nº DE DOCUMENTO], extracto bancario en que consta el montante de los ingresado en concepto de pensión alimenticia en favor del hijo en los últimos doce meses, en la cuenta que a tal efecto convieron los cónyuges en el Convenio regulador de su separación o divorcio.

TERCERO.- Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

Resultan aplicables a los citados hechos los siguientes

FUNDAMENTOS DE DERECHO

I. COMPETENCIA.- Es competente el Tribunal al que me dirijo, de acuerdo con el artículo 769 LEC en relación con el artículo 775 LEC.

II. LEGITIMACIÓN.- La de ambas partes deriva del artículo 775 LEC y de los artículos 90 y 91 CC. Conforme al art. 749.2 LEC, debe intervenir el Ministerio Fiscal, por encontrarse interesados menores.

III. PROCEDIMIENTO.- Arts. 770 y 775.2 LEC.

IV. REPRESENTACIÓN Y DEFENSA.- El/La demandante comparece representado y defendido, respectivamente, por el Procurador y el Letrado que constan en el encabezamiento de este escrito, de acuerdo con lo dispuesto en el artículo 750 LEC, en relación con los artículos 770 y 775.2 LEC.

V. CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.- La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VI. DERECHO SUSTANTIVO.- El art. 93.1 CC señala: “El Juez, en todo caso, determinará la contribución de cada progenitor para satisfacer los alimentos y adoptará las medidas convenientes para asegurar la efectividad y acomodación de las prestaciones a las circunstancias económicas y necesidades de los hijos en cada momento”.

La fijación de la cuantía de la pensión alimenticia mediante un cálculo porcentual sobre los ingresos del alimentante no sólo genera inseguridad y continuas disputas entre los progenitores, en perjuicio del hijo, cuyo daño debe ser en cualquier caso evitado (cfr. art. 90.2 CC), sino que es contraria a la “ratio legis” del art. 93 CC, que ordena al Juez determinar la contribución de cada progenitor a los alimentos de los hijos acomodando las prestaciones a las circunstancias de las necesidades de éstos, a las que resulta ajeno el anterior cálculo porcentual, que peca de relatividad e imprecisión, aunque en su momento fuera consensuado. En el mismo sentido, el art. 90.3 CC obliga a atender debidamente a las necesidades de los hijos, lo que, en el caso presente, no se ha logrado con el sistema inicialmente acordado.

En el mismo sentido juega el art. 154.III.1 CC, en relación con los arts. 142 y ss del Código civil, en especial, el art. 146 CC, según el cual, la cuantía de los alimentos será proporcionada al caudal o medios de quien los da y a las necesidades de quien los recibe.

La inconcreción y ambigüedad de la cuantía de la pensión fijada sobre el porcentaje de los ingresos totales del obligado justifica su sustitución por una pensión de cuantía fija y periodicidad mensual, proporcionada a las necesidades del hijo y a la capacidad del obligado, actualizable anualmente de acuerdo con el IPC.

Son numerosos los pronunciamientos jurisprudenciales en el sentido expuesto. Entre otras, pueden citarse las siguientes sentencias:

VII. COSTAS.- Se impondrán de acuerdo con lo dispuesto en el art. 394 LEC.

VIII.Iura novit curia y las demás normas que resulten procedentes.

Por lo expuesto

SUPLICO AL TRIBUNAL:

Que tras admitir este escrito con los documentos que lo acompañan y sus copias, me tenga por comparecido y parte en la representación que ostento, entendiéndose conmigo las sucesivas diligencias, y tenga por interpuesta DEMANDA, que habrá de sustanciarse por los trámites del juicio verbal con las especialidades del art. 770 LEC, conforme a lo establecido en el art. 775.2 LEC, contra D./Dª [NOMBRE Y APELLIDOS], SOBRE MODIFICACIÓN DE MEDIDAS DEFINITIVAS DE DIVORCIO O DE SEPARACIÓN RELATIVAS A LA FIJACIÓN DE PENSIÓN ALIMENTICIA; y, previos los trámites legales que proceda, dicte resolución por la que, estimando íntegramente la demanda, se sustituya la pensión alimenticia fijada en la sentencia del Tribunal de Instancia de [SEDE], plaza n.º [NÚMERO], de fecha [FECHA], de [MES], de [AÑO], procedimiento número [Nº DE PROCEDIMIENTO]/[AÑO], en un [Nº] por ciento de los ingresos netos de mi representado/o por una pensión de cuantía fija de [IMPORTE] euros ( €) mensuales, a satisfacer dentro de los cinco primeros días de cada mes, en la misma cuenta bancaria en la que se viene haciendo hasta la fecha o la que señale el/la demandado/a, y actualizable anualmente de acuerdo con las variaciones del IPC.

OTROSÍ DIGO.- En cumplimiento de lo dispuesto en el art. 253 LEC, esta parte fija la cuantía del procedimiento, calculada de acuerdo con lo dispuesto en el art. 251.7 LEC en [IMPORTE] euros.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma y número del Letrado	Firma del Procurador

========================================================================
