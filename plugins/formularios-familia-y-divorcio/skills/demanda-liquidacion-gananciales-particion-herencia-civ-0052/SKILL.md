---
name: demanda-liquidacion-gananciales-particion-herencia-civ-0052
description: "Demanda de liquidación de gananciales y partición de herencia de un hijo adoptivo del fallecido. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de liquidación de gananciales y partición de herencia de un hijo adoptivo del fallecido

> Formulario **CIV-0052** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de liquidación de gananciales y partición de herencia de un hijo adoptivo del fallecido» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de liquidación de gananciales y partición de herencia de un hijo adoptivo del fallecido” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-liquidacion-gananciales-particion-herencia-civ-0052`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (18 veces)
- [ ] AÑO (5 veces)
- [ ] DÍA (5 veces)
- [ ] MES (5 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] IMPORTE (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] FINCA
- [ ] LUGAR
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] NÚMERO
- [ ] SEDE

## Normas que cita el formulario

- art. 85.1 LOPJ
- art. 782 LEC
- art. 108 Código Civil
- art. 810 LEC
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 1392 Código Civil
- art. 85 CC
- art. 1396 CC
- art. 1051 Código Civil
- art. 394 LEC
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

- Junto a «…MILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.

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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D [NOMBRE Y APELLIDOS] Procurador de los Tribunales, actuando en representación de [NOMBRE DEL REPRESENTADO/A], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que por medio del presente escrito solicito la LIQUIDACIÓN DEL RÉGIMEN ECONÓMICO MATRIMONIAL DE GANANCIALES existente entre mi difunto padre, D [NOMBRE Y APELLIDOS], y su actual esposa Dª [NOMBRE Y APELLIDOS], ya disuelto por fallecimiento de éste, y acción acumulada de DIVISIÓN JUDICIAL DEL PATRIMONIO HEREDITARIO del finado D [NOMBRE Y APELLIDOS], dirigiéndose la presente solicitud frente a Dª [NOMBRE Y APELLIDOS], de acuerdo a los siguientes,

HECHOS

Primero.- D [NOMBRE Y APELLIDOS], y su actual esposa Dª [NOMBRE Y APELLIDOS], contrajeron matrimonio civil en [LOCALIDAD], con fecha [DÍA] de [MES] de [AÑO], siendo su régimen económico matrimonial el de gananciales.

Aportamos como documento nº 1 certificado de matrimonio expedido por el Registro Civil de [LOCALIDAD]

Segundo.- D [NOMBRE Y APELLIDOS] falleció el pasado [DÍA] de [MES] de [AÑO], casado en segundas nupcias con Dª [NOMBRE Y APELLIDOS]

Acompañamos como documento nº 2, certificado de defunción de D [NOMBRE Y APELLIDOS]

Tercero.- El demandante fue adoptado por el causante, el [DÍA] de [MES] de [AÑO], junto con su primera esposa, Dª [NOMBRE Y APELLIDOS]

Acompañamos como documento nº 3 resolución judicial mediante la que se acuerda la adopción de nuestro mandante por el finado.

Igualmente acompañamos, como documento nº 4, libro de familia de D [NOMBRE Y APELLIDOS] donde se puede apreciar que no tenía más descendientes.

Cuarto.- D [NOMBRE Y APELLIDOS] falleció habiendo otorgado testamento, con fecha [DÍA] de [MES] de [AÑO], ante el Notario D [NOMBRE Y APELLIDOS], y con número de protocolo

Aportamos como documentos nº 5 y 6 últimas voluntades del finado, y copia autorizada del testamento que otorgó.

En el citado testamento instituyó heredero único al demandante, debiendo respetar el usufructo legal de su esposa.

Quinto.- Habida cuenta de la voluntad del actor de proceder a la división de la herencia, y no habiendo sido posible llegar a un acuerdo con la actual esposa de su finado padre, mediante el presente escrito solicita la liquidación del régimen económico matrimonial de gananciales de su padre, fruto de la disolución matrimonial causada por su fallecimiento, y como paso previo ineludible para interesar, mediante la misma demanda, la división judicial de su patrimonio.

Sexto.- Constituye el activo de la sociedad de gananciales un bien inmueble sito en [LOCALIDAD], con número de finca registral [FINCA], inscrito en el Registro de la Propiedad número [NÚMERO] de

Acompañamos nota simple del Registro de la Propiedad como documento nº 7.

No consta, por el contrario, la existencia de ningún tipo de pasivo de la sociedad de gananciales a fecha de la interposición de la demanda.

Se atribuye un valor al inmueble que ha sido descrito de [IMPORTE] euros.

Séptimo.- Dada la existencia de un único bien de la sociedad de gananciales, se interesa como propuesta de liquidación que la mitad del mismo sea adjudicada a la esposa Dª [NOMBRE Y APELLIDOS], y la otra mitad al causante D [NOMBRE Y APELLIDOS], sin que proceda realizar compensación alguna entre los cónyuges.

Octavo.- Una vez se proceda a la liquidación del régimen económico matrimonial de gananciales, según la propuesta del demandante, se interesa que el activo adjudicado a D [NOMBRE Y APELLIDOS], conforme el activo de su herencia, dado que D [NOMBRE Y APELLIDOS] no tenía ningún bien de carácter privativo.

Del mismo modo, no se conoce ningún tipo de pasivo del finado a fecha de interposición de la demanda.

Noveno.- La propuesta de liquidación de la herencia del causante se formula en cumplimiento del testamento otorgado:

- Instituye heredero al demandante, luego se le debe adjudicar la nuda propiedad de la mitad del inmueble que constituye el activo del finado.

- Lega el usufructo universal a la esposa, luego se le debe adjudicar el usufructo de la mitad del inmueble que constituye el activo del finado.

Noveno.- Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

FUNDAMENTOS DE DERECHO

Competencia

Corresponde la competencia para conocer de esta clase de procesos al Tribunal de Instancia del domicilio del finado, por aplicación del artículos 45, 52.1.4º y 807 de la LEC, en relación con lo dispuesto en el art. 85.1º LOPJ.

Legitimación

El demandante tiene legitimación activa como heredero del finado que desea proceder a la división de la herencia (artículo 782 de la LEC), y ostenta la pasiva la demandada, como esposa del causante, y legataria.

También resultan de aplicación los artículos 108 y siguientes del Código Civil, que equiparan los derechos de filiación de los hijos nacidos del matrimonio, con los de los hijos adoptados.

Procedimiento

Resulta de aplicación a la formación de inventario y liquidación del régimen económico matrimonial de gananciales, el procedimiento establecido en el artículo 810 y siguientes de la LEC, como procedimiento específico establecido por la ley rituaria, siéndole igualmente de aplicación las normas generales del juicio verbal.

Igualmente resultan de aplicación el procedimiento regulado en los artículos 782 y siguientes de la LEC en lo relativo a la división judicial de la herencia.

Cumplimiento de los requisitos de procedibilidad

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

Fondo del asunto

Acumulamos la acción de liquidación del régimen económico matrimonial de sociedad de gananciales y la acción de división de herencia, dado que resulta ineludible liquidar el régimen económico matrimonial antes que proceder con la división de la herencia, y porque coinciden las partes afectadas por ambas solicitudes.

Resulta de aplicación el artículo 1392 del Código Civil que establece que la sociedad de gananciales puede liquidarse cuando se disuelve el matrimonio, siendo una de las formas de disolución la prevista por muerte de uno de los cónyuges (artículo 85 del CC).

Una vez disuelta la sociedad de gananciales, cabe su liquidación, debiéndose proponer un inventario que comprenda el activo y el pasivo de la misma, como paso previo a su adjudicación al cónyuge superviviente y los herederos del finado (artículo 1396 y siguientes del CC, y artículo 1051 y siguientes del Código Civil).

Y ello porque ningún coheredero podrá ser obligado a permanecer en la indivisión de la herencia.

Al objeto de llevar a cabo las solicitudes de esta parte, habrá de formarse el inventario, tanto de la sociedad de gananciales, como del finado, una vez liquidada la primera, para lo cual esta parte realiza una propuesta, y el Secretario habrá de emplazar a los herederos a la correspondiente junta.

Una vez aprobado el inventario, procederá su adjudicación a las partes del litigio, en virtud de la legislación vigente y el testamento otorgado por el finado.

Costas

En materia de costas el art 394 LEC señala que las de primera instancia se imponen a la parte que vea en primera instancia rechazadas sus pretensiones

En base a lo anterior,

SUPLICO AL TRIBUNAL que tenga por presentada la presente demanda con los documentos a ella adjuntos y sus copias por parte en la representación que ostento y, tras la pertinente tramitación, se dicte por ese Tribunal sentencia por la que:

1) se declare disuelto el régimen económico matrimonial de gananciales, y liquidado el mismo según la propuesta realizada por esta parte, debiendo convocar a la esposa del finado al objeto de continuar con los trámites del procedimiento.

2) se proceda a la división de la herencia del finado, y se adjudique su bien entre los herederos, a quienes igualmente habrá de convocarse para proseguir con los trámites del procedimiento.

3) se condene al pago de las costas de este proceso a la citada demandada.

OTROSÍ PRIMERO DIGO que, de conformidad con lo dispuesto en los artículos 251 y 252 de la LEC, se fija la cuantía del presente procedimiento en [IMPORTE] euros.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma Abogado	Firma Procurador

========================================================================
