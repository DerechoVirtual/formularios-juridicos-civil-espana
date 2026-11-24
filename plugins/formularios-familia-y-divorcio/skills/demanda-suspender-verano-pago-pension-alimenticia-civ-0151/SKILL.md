---
name: demanda-suspender-verano-pago-pension-alimenticia-civ-0151
description: "Demanda para suspender en verano el pago de la pensión alimenticia. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda para suspender en verano el pago de la pensión alimenticia

> Formulario **CIV-0151** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda para suspender en verano el pago de la pensión alimenticia» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda para suspender en verano el pago de la pensión alimenticia” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-suspender-verano-pago-pension-alimenticia-civ-0151`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] AÑO (7 veces)
- [ ] IMPORTE (6 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] DÍA (4 veces)
- [ ] MES (4 veces)
- [ ] Nº DE DOCUMENTO (4 veces)
- [ ] Nº (3 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] SEDE (2 veces)
- [ ] CALLE
- [ ] COLEGIO
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] NIF

## Normas que cita el formulario

- art. 775 LEC
- art. 90 CC
- art. 749.2 LEC
- art. 750 LEC
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 93.2 CC
- art. 146 CC
- art. 394 LEC
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

Que por medio del presente escrito y en la representación que ostento, interpongo DEMANDA DE MODIFICACIÓN DE MEDIDAS DEFINITIVAS adoptadas en sentencia de divorcio o separación dictada en el procedimiento de mutuo acuerdo o contencioso, seguido ante este Tribunal al cual me dirijo, número de procedimiento [Nº DE PROCEDIMIENTO]/[AÑO], en solicitud de suspensión del pago de la pensión de alimentos establecida en favor del hijo mayor de edad de los cónyuges, contra D./Dª [NOMBRE Y APELLIDOS], mayor de edad, con DNI/NIF [NIF] y con domicilio, a efectos de citación y emplazamiento, en [LOCALIDAD], calle [CALLE], nº [NÚMERO], pta. La presente demanda se basa en los siguientes

HECHOS

En fecha [DÍA] de [MES] de [AÑO], se dictó por el Tribunal al que me dirijo, sentencia en el procedimiento de divorcio o de separación de mutuo acuerdo núm. [Nº]/[AÑO] puede tratarse también de un procedimiento contencioso, en cuyo caso, las referencias que se hacen a continuación al convenio regulador judicialmente homologado, lo serían a las medidas adoptadas por el Juez, en la que se procedió a homologar el Convenio regulador de fecha [DÍA] de [MES] de [AÑO], presentado por las partes.

Se acompaña testimonio de la citada sentencia, en que consta su firmeza, así como del convenio regulador que la misma homologaba, como DOCUMENTO Nº [Nº DE DOCUMENTO] con remisión, a efectos probatorios, a los archivos de este Tribunal.

En la estipulación [Nº] del citado Convenio, en la que se regula la contribución a las cargas familiares y alimentos, se establece una pensión alimenticia de [IMPORTE] euros ( €) mensuales, actualizables anualmente de acuerdo con las variaciones del IPC, a cargo de mi representado/a en favor del hijo mayor de edad de la pareja, que se encuentra todavía en período de formación, y convive con el otro progenitor. El tenor literal de la citada estipulación es el siguiente:

Desde que se dictó la citada sentencia, han variado sustancialmente las circunstancias que se tuvieron en cuenta para fijar el montante de la pensión. El beneficiario de la misma realiza trabajos temporales los meses de verano (julio y agosto), por los que cobra una cantidad de [IMPORTE] euros mensuales, suficiente para cubrir sus gastos durante esos mismos meses, reanudando sus estudios cuando aquéllos finalizan. Esta situación se ha producido ya durante dos años consecutivos, siendo previsible que persista en el futuro.

Se acompañan como DOCUMENTOS Nos a [Nº DE DOCUMENTO], los siguientes, para acreditar los hechos referidos.

Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

Resultan aplicables a los citados hechos los siguientes

FUNDAMENTOS DE DERECHO

COMPETENCIA.- Es competente el Tribunal al que me dirijo, de acuerdo con el artículo 775 LEC.

LEGITIMACIÓN.- La de ambas partes deriva del artículo 775 LEC y de los artículos 90 y 91 CC. Conforme al art. 749.2 LEC, debe intervenir el Ministerio Fiscal, por encontrarse interesados menores.

PROCEDIMIENTO.- Arts. 770 y 775.2 LEC.

REPRESENTACIÓN Y DEFENSA.- El/La demandante comparece representado y defendido, respectivamente, por el Procurador y el Letrado que constan en el encabezamiento de este escrito, de acuerdo con lo dispuesto en el artículo 750 LEC, en relación con los artículos 770 y 775.2 LEC.

CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.- La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

DERECHO SUSTANTIVO.- El art. 93.2 CC señala: "Si convivieran en el domicilio familiar hijos mayores de edad o emancipados que carecieran de ingresos propios, el Juez, en la misma resolución, fijará los alimentos que sean debidos conforme a los artículos 142 y siguientes de este Código".

Por su parte, el artículo 146 CC dispone: "La cuantía de los alimentos será proporcionada al caudal o medios de quien los da y a las necesidades de quien los recibe". Y el artículo 147 señala: "Los alimentos, en los casos a que se refiere el anterior, se reducirán o aumentarán proporcionalmente según el aumento o disminución que sufran las necesidades del alimentista y la fortuna del que hubiere de satisfacerlos".

La percepción de los ingresos referidos por parte del beneficiario de los alimentos hace procedente un reajuste de la pensión que viene obligado a satisfacer mi representado/a, en el sentido de que se le releve de la obligación de pagarla durante los meses de julio y agosto, en que su hijo trabaje y perciba ingresos suficientes, considerándose como tales los que igualen o superen la cantidad de [IMPORTE] euros mensuales; o, alternativamente, se reduzca el montante mensual de la pensión proporcionalmente a la capacidad económica de su hijo resultante de los ingresos obtenidos por éste.

Puede citarse jurisprudencia en apoyo de lo solicitado.

COSTAS.- Se impondrán de acuerdo con lo dispuesto en el art. 394 LEC.

Iura novit curia y las demás normas que resulten procedentes.

Por lo expuesto

SUPLICO AL TRIBUNAL:

Que tras admitir este escrito con los documentos que lo acompañan y sus copias, me tenga por comparecido y parte en la representación que ostento, entendiéndose conmigo las sucesivas diligencias, y tenga por interpuesta DEMANDA, que habrá de sustanciarse por los trámites del juicio verbal, contra D./Dª [NOMBRE Y APELLIDOS], SOBRE MODIFICACIÓN DE PENSIÓN ALIMENTICIA; y, previos los trámites legales que procedan, dicte sentencia por la que, estimando íntegramente la demanda, se suspenda el pago de la citada pensión durante los meses de julio y agosto que el beneficiario trabaje y obtenga ingresos no inferiores a [IMPORTE] euros ( €); o, subsidiariamente, se reduzca la cuantía de la pensión alimenticia fijada en la sentencia del Tribunal de Instancia de [SEDE], plaza n.º [NÚMERO], de fecha [DÍA] de [MES] de [AÑO], procedimiento número [Nº DE PROCEDIMIENTO]/[AÑO], fijándola en [IMPORTE] euros ( €) mensuales, como consecuencia de la disminución de las necesidades del alimentista al obtener ingresos por su trabajo temporal.

OTROSÍ DIGO.- En cumplimiento de lo dispuesto en el art. 253 LEC, esta parte fija la cuantía del procedimiento, calculada de acuerdo con lo dispuesto en el art. 251.7 LEC en [IMPORTE] euros.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma y número del Letrado	Firma del Procurador

========================================================================
