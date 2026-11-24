---
name: demanda-separacion-hijos-menores-sustituye-definitivas-civ-0297
description: "Demanda de separación con hijos menores que sustituye por definitivas las medidas previas. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de separación con hijos menores que sustituye por definitivas las medidas previas

> Formulario **CIV-0297** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda de separación matrimonial solicitando se determinen las medidas definitivas que han de sustituir a las provisionales previas adoptadas por otro Tribunal, existiendo hijos menores de edad. Aunque la cuestión es discutida por la doctrina, el modelo contempla la NO sujeción al previo intento de resolución de controversias en vía no jurisdiccional por tratarse de materias excluidas del requisito de procedibilidad de acuerdo con el art. 4.1 II LO 1/2025, entre las cuales se encuentran los conflictos que afecten a derechos y obligaciones que no estén a disposición de las partes.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de separación con hijos menores que sustituye por definitivas las medidas previas» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de separación con hijos menores que sustituye por definitivas las medidas previas” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-separacion-hijos-menores-sustituye-definitivas-civ-0297`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (11 veces)
- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] FECHA (6 veces)
- [ ] Nº DE DOCUMENTO (5 veces)
- [ ] CALLE (3 veces)
- [ ] SEDE (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] NOMBRE DEL MENOR (2 veces)
- [ ] Nº (2 veces)
- [ ] BARRIO
- [ ] COLEGIO
- [ ] DENOMINACIÓN SOCIAL
- [ ] LUGAR
- [ ] NOMBRE DE LA CLÍNICA
- [ ] Nº DE COLEGIADO
- [ ] NÚMERO

## Normas que cita el formulario

- art. 437 LEC
- art. 753 LEC
- art. 770 LEC
- art. 81 CC
- art. 4.1 LO 1/2025
- art. 81.2.º CC
- art. 91 CC
- art. 772.1 LEC
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

- Junto a «…CIA [ELEGIR: SECCIÓN CIVIL / SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD] DE [SEDE]»: Denominación legal: Sección de Familia, Infancia y Capacidad. Si no existe en el partido, conoce la Sección Civil o la Única (art. 86.3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).

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

AL TRIBUNAL DE INSTANCIA [ELEGIR: SECCIÓN CIVIL / SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD] DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, que actúa en nombre y representación de D. [NOMBRE Y APELLIDOS] provisto de D.N.I. nº [NÚMERO],con domicilio en [LOCALIDAD], calle [CALLE], lo que acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], bajo dirección de el/la Letrado/a D./Dña. [NOMBRE Y APELLIDOS], colegiada nº [Nº DE COLEGIADO] del Iltre. Colegio de Abogados de [COLEGIO], cuyo despacho se abre en [LOCALIDAD], calle [CALLE], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que por medio del presente escrito, siguiendo la instrucción de mi mandante, vengo a formular demanda de SEPARACIÓN DEL MATRIMONIO frente a su esposa Dña. [NOMBRE Y APELLIDOS], con domicilio actual en [DOMICILIO], y consulta profesional en la clínica dental [NOMBRE DE LA CLÍNICA] de [LOCALIDAD], calle [CALLE], y frente al MINISTERIO FISCAL, con base a los siguientes datos y argumentos:

HECHOS

PRIMERO.- Mi mandante contrajo matrimonio civil con Dña. [NOMBRE Y APELLIDOS], en [LOCALIDAD], el día [FECHA]. Se acompaña la correspondiente certificación de matrimonio expedida por el Registro Civil de [LOCALIDAD] DOCUMENTO Nº [Nº DE DOCUMENTO].

De dicha unión nació un hijo, de nombre [NOMBRE DEL MENOR], nacido el [FECHA], por lo que sigue bajo la patria potestad de sus progenitores. Se adjunta la correspondiente certificación de nacimiento que ha emitido el Registro Civil de [LOCALIDAD] DOCUMENTO Nº [Nº DE DOCUMENTO].

SEGUNDO.- Si bien durante el período de tiempo que siguió a la celebración del matrimonio y hasta que tuvieron su hijo no hubo entre los esposos otros problemas que los normales en todo matrimonio, a partir del nacimiento de [NOMBRE DEL MENOR], que infortunadamente padece ‘síndrome de Down’, los casados fueron avanzando rápidamente en una línea de desafecto, acuciándose las discusiones, por diferencia de culturas -mi mandante es ciudadano extranjero, natural de [LOCALIDAD] - y por el impacto de la crianza de quien nació con discapacidad psíquica en la personalidad de la madre, de modo que resultaban cada día más insoportables, refugiándose ambos cónyuges en sus respectivas carreras profesionales (la esposa es odontóloga y el demandante es agente de comercio, teniendo que pasar D. la mayor parte del año en viajes de negocios, puesto que representa a la [DENOMINACIÓN SOCIAL] en [LOCALIDAD] y [LOCALIDAD]).

TERCERO.- Habiéndose hecho insoportable el sostenimiento artificial de tal situación, los cónyuges decidieron separarse de hecho, abandonando mi representado la vivienda de que disfrutaba la familia, apartamento dúplex en [LOCALIDAD], barrio [BARRIO], y pasando a vivir la mayoría del año en Hamburgo, de modo que asumió no visitar a su hijo, sin que hubiera de hacerse responsable de ninguna aportación económica al sostenimiento de la familia por razón de los pingües rendimientos de la demandada, a la que dejó el uso de hasta entonces patrimonio ganancial, para lo que se suscribió documento que se elevó a público el [FECHA], junto con el otorgamiento de capitulaciones matrimoniales que disolvieron el régimen de gananciales -sin que hasta ahora se hayan liquidado dichos bienes-, incluida la citada vivienda y la segunda residencia de [LOCALIDAD], así como de todo el mobiliario y ajuar de ambas.

Se acompaña copia del dicho pacto y de las capitulaciones (DOCUMENTOS Nos [Nº] y [Nº]), así como certificado de empadronamiento municipal, en que consta que la demandada vive sola con su hijo (DOCUMENTO Nº [Nº DE DOCUMENTO]).

CUARTO.- Cuando mi mandante ha intentado acomodar esta situación provisional, de nuevo domiciliado en [DOMICILIO], de modo que se le facilite un régimen de comunicación con el hijo, y liquidar el régimen de bienes conyugal, ha encontrado la más cerrada oposición de la demandada, lo que motivó la solicitud de medidas provisionales previas ante el Tribunal de Instancia de [SEDE], que se acordaron en Auto de [FECHA], (Se acompaña testimonio como DOCUMENTO Nº [Nº DE DOCUMENTO]), por lo que, forzado al litigio ante la imposibilidad de acuerdo, antes del transcurso del plazo legal de treinta días, se formula esta demanda, a fin de obtener la separación y resolver los problemas económicos y de custodia referidos al hijo común.

FUNDAMENTOS DE DERECHO

I.- Es competente la Sección Civil del Tribunal de Instancia del lugar del domicilio de la demandada, que es el último domicilio conyugal común, conforme al art. 769.1.pfo.1º LEC.

II.- El proceso adecuado es el del juicio verbal (arts. 437 LEC y ss.), como se diseña especialmente por el art. 753 LEC, y con las peculiaridades del art. 770 LEC para conocer de las demandas contenciosas de separación.

III.- Tiene legitimación activa ordinaria el demandante por hallarse en la situación jurídica de relación conyugal, como detenta la pasiva su esposa demandada (arts. 81 CC y 10.1 LEC), siendo el objeto del proceso principal la pretensión de separación conyugal y la adopción de medidas definitivas derivadas de la misma.

IV.- La presente demanda no está sujeta al previo intento de resolución de controversias en vía no jurisdiccional por tratarse de materias excluidas del requisito de procedibilidad de acuerdo con el art. 4.1 II LO 1/2025, entre las cuales se encuentran los conflictos que afecten a derechos y obligaciones que no estén a disposición de las partes.

V.- El fondo de la pretensión consiste en la declaración de separación conyugal sin consenso de los cónyuges, a instancia de uno de ellos (art. 81.2.º CCiv), sin otra base que la libre voluntad del consorte, transcurridos más de tres meses desde la celebración del matrimonio.

VI.- Conforme a los arts. 91 y 106 CCiv y 774 LEC, el Tribunal deberá pronunciarse en definitiva sobre las medidas que se solicitaron y se adoptaron con carácter de provisionales previas por Auto de [FECHA], dictado por el Tribunal de Instancia de [SEDE], acerca de los hijos, vivienda y cargas familiares, y régimen matrimonial de bienes, que se mantendrán hasta entonces automáticamente (art. 772.1 LEC), y cuyo mantenimiento definitivo se solicita.

VII.- Las costas procesales deben ser impuestas a la parte demandada, por criterio del íntegro vencimiento, en atención al art. 394 LEC.

Y demás normas y jurisprudencia de general y pertinente aplicación.

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito con los documentos que se acompañan y sus copias, se digne admitirlos, tenerme por comparecida y parte en la representación que ostento, y por interpuesta demanda de separación conyugal, y seguido que sea el procedimiento por sus pertinentes trámites, con citación del Ministerio Fiscal, se sirva dictar Sentencia por la que, estimando la presente demanda, decrete la separación de matrimonio formado por D [NOMBRE Y APELLIDOS] y Dña. [NOMBRE Y APELLIDOS], determinándose las medidas definitivas que han de sustituir a las provisionales y que expresamente se piden coincidentes con las acordadas con carácter previo, y expresa imposición de las costas procesales a la demandada si no consiente la pretensión actora que ha forzado.

Como es Justicia de hacerse en [LUGAR], a [FECHA].

OTROSÍ DIGO: Que por necesitar para otros usos la copia de escritura de poder acreditativa de la representación del suscrito Procurador, intereso y

SUPLICO AL TRIBUNAL. Se sirva acordar su desglose y devolución a esta parte, dejando en autos testimonio de la misma.

Reitero Justicia en lugar y fecha "ut supra ".

Firma del Abogado/a	Firma del Procurador/a

========================================================================
