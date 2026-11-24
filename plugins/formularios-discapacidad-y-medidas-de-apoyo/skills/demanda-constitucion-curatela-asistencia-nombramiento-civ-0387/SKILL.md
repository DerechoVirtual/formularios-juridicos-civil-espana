---
name: demanda-constitucion-curatela-asistencia-nombramiento-civ-0387
description: "Demanda de constitución de curatela o asistencia y nombramiento de curador (Derecho foral aragonés). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de constitución de curatela o asistencia y nombramiento de curador (Derecho foral aragonés)

> Formulario **CIV-0387** del plugin **Discapacidad y medidas de apoyo (Ley 8/2021)** (`formularios-discapacidad-y-medidas-de-apoyo`) · Civil › Capacidad y medidas de apoyo · normativa revisada el 24-11-2026.

## Qué es

Demanda de provisión de medidas judiciales de apoyo a una persona con discapacidad, de vecindad civil aragonesa, solicitando la constitución de la curatela o asistencia y el nombramiento como curador/a de la persona designada por delación voluntaria de los padres en escritura pública, una vez fallecidos éstos y tras haberse archivado el expediente de jurisdicción voluntaria previo por oposición del Ministerio Fiscal (arts. 756 y siguientes LEC).

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de constitución de curatela o asistencia y nombramiento de curador (Derecho foral aragonés)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de constitución de curatela o asistencia y nombramiento de curador (Derecho foral aragonés)” para mi caso». También puedes invocarla directamente con `/formularios-discapacidad-y-medidas-de-apoyo:demanda-constitucion-curatela-asistencia-nombramiento-civ-0387`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-discapacidad-y-medidas-de-apoyo:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Discapacidad y medidas de apoyo (Ley 8/2021)) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (7 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] ESTADO CIVIL (3 veces)
- [ ] FECHA (3 veces)
- [ ] Nº (3 veces)
- [ ] Nº DE PROCEDIMIENTO (3 veces)
- [ ] NOMBRE Y APELLIDOS DE LA PERSONA CON DISCAPACIDAD (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL DEMANDANTE (2 veces)
- [ ] SEDE (2 veces)
- [ ] AÑO
- [ ] CALLE
- [ ] DNI/NIE
- [ ] DOMICILIO
- [ ] DOMICILIO PROFESIONAL
- [ ] DÍA
- [ ] EDAD
- [ ] MES
- [ ] MES Y AÑO
- [ ] NOMBRE Y APELLIDOS DEL ABOGADO/A
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] NOMBRE Y APELLIDOS, Nº DE COLEGIADO
- [ ] Nº DE COLEGIADO
- [ ] Nº DE FOLIOS
- [ ] PROFESIÓN

## Normas que cita el formulario

- art. 756 LEC
- art. 753 LEC
- art. 759 LEC
- art. 757.1 LEC
- art. 757.3 LEC
- art. 757.4 LEC
- art. 5.2 Ley Orgánica 1/2025
- art. 249 Código Civil
- art. 276 Código Civil
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

- Al principio del formulario: el original no traía el texto actualizado a la Ley 8/2021, de 2 de junio, de reforma de la legislación civil y procesal para el apoyo a las personas con discapacidad. Los artículos del Código del Derecho Foral de Aragón citados (arts. 100 y siguientes, 115, 116.3 y 119) y los de la LEC (arts. 756 a 763) deben comprobarse en su redacción vigente, así como su adaptación a la citada ley, antes de presentar el escrito.
- Junto a «…FANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA N.º [Nº] DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
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

[OPCIONAL — si ha lugar: adaptar al caso real los datos del modelo (parentesco, enfermedad, designación voluntaria de curador, expediente previo).]

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA N.º [Nº] DE [SEDE]

[NOTA: si en la sede existe Sección de Familia, Infancia y Capacidad, dirigir el escrito a dicha Sección; en un asunto ya repartido, indicar «DE [SEDE], PLAZA N.º [Nº]».]

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, actuando en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDANTE], mayor de edad, de estado civil [ESTADO CIVIL], de profesión [PROFESIÓN], vecino/a de esta ciudad, calle [CALLE], tal y como consta en la copia electrónica del poder notarial de representación (digitalizada) que se adjunta [OPCIONAL — si ha lugar: o según acreditaré mediante apoderamiento apud acta el día y hora a determinar por este Tribunal al que me dirijo], actuando bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS DEL ABOGADO/A], colegiado/a n.º [Nº DE COLEGIADO], con domicilio profesional en [DOMICILIO PROFESIONAL], ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que en la indicada representación formulo demanda de adopción de medidas judiciales de apoyo a personas con discapacidad respecto de D./Dña. [NOMBRE Y APELLIDOS DE LA PERSONA CON DISCAPACIDAD], de vecindad civil aragonesa, provisto/a de DNI [DNI/NIE], nacido/a en [LOCALIDAD] en fecha [FECHA], de estado civil [ESTADO CIVIL], con domicilio en [DOMICILIO]; se aporta como DOCUMENTO N.º 1 certificación literal de nacimiento expedida por el Registro Civil de [LOCALIDAD], todo ello en base a los siguientes

HECHOS

Relaciones de parentesco

El demandado/la demandada es hermano/a de mi mandante, tal y como se acredita mediante la certificación literal expedida por el Registro Civil de [LOCALIDAD] que se aporta como DOCUMENTO N.º 1, de estado civil [ESTADO CIVIL], habiendo fallecido sus padres en fecha [FECHA], tal y como se acredita mediante la aportación del certificado de defunción como DOCUMENTOS N.º 2 y 3, y teniendo otros [Nº] hermanos según se acredita mediante certificaciones del Registro Civil que se acompañan como DOCUMENTOS N.º 4 a 6.

En relación con la enfermedad padecida y su evolución

D./Dña. [NOMBRE Y APELLIDOS] tiene en la actualidad [EDAD] años de edad y está afecto/a de [ENFERMEDAD O DISCAPACIDAD, p. ej. síndrome de Down] desde su nacimiento, tal como se acredita por el informe del Dr./de la Dra. [NOMBRE Y APELLIDOS], que se aporta como DOCUMENTO N.º 7, en el cual se expresa que la enfermedad ha venido progresando de forma degenerativa, estando totalmente impedido/a para gobernarse por sí mismo/a.

Hasta el momento, el demandado/la demandada había vivido con sus padres, quienes lo/la habían cuidado y no habían instado el correspondiente proceso judicial de provisión de apoyos; sin embargo, al haber fallecido éstos y habiendo sido designado como curador mi representado/a, según se expondrá seguidamente, nos vemos en la obligación de promover la constitución de la curatela.

Expediente de jurisdicción voluntaria previo

La situación de discapacidad del demandado/de la demandada determinó que mi representado/a instara expediente de jurisdicción voluntaria de provisión de medidas judiciales de apoyo respecto de su hermano/a ante el Tribunal al que me dirijo, siguiéndose procedimiento número [Nº DE PROCEDIMIENTO], el cual finalizó al haberse formulado oposición por el Ministerio Fiscal, lo que determina la interposición de la presente demanda, de conformidad con lo dispuesto en el art. 756 y siguientes de la LEC.

De la situación actual

Así las cosas, nos encontramos con que el estadio de la patología padecida por D./Dña. [NOMBRE Y APELLIDOS] es calificado, conforme con el último examen médico realizado a fecha de [FECHA], que se aporta como DOCUMENTO N.º 8, de muy intenso y totalmente irreversible, necesitando cuidados permanentes de una tercera persona y no pudiendo gobernarse por sí mismo/a.

De ello se deriva la idoneidad de las medidas propuestas, que se acredita mediante los diferentes informes de los facultativos que han venido atendiendo la patología del demandado/de la demandada durante estos años, así como del informe de los servicios sociales del Ayuntamiento de [LOCALIDAD], los cuales se acompañaron con la solicitud presentada en el expediente de jurisdicción voluntaria seguido con el número [Nº DE PROCEDIMIENTO] en este Tribunal, cuya incorporación por testimonio a este proceso se solicita desde este momento, designando los particulares que comprenden dichos informes obrantes en los folios [Nº DE FOLIOS].

Relaciones familiares y situación de guarda

El demandado/La demandada D./Dña. [NOMBRE Y APELLIDOS] está residiendo en la actualidad en el domicilio de mi representado/a, quien se ocupa de forma exclusiva de sus cuidados desde el fallecimiento de sus padres el pasado mes de [MES Y AÑO], y cumpliendo la voluntad de éstos, quienes encomendaron a mi mandante la guarda y custodia de su hermano/a en caso de fallecimiento, como seguidamente se referirá.

Delación voluntaria del nombramiento de curador

Como se ha venido exponiendo, los padres de mi representado/a, previendo la posibilidad de premoriencia respecto del demandado/de la demandada, confiaron a mi representado/a que cuidara del mismo/de la misma en caso de que ellos murieran y, al efecto, conforme autoriza el artículo 115 del Código del Derecho Foral de Aragón, otorgaron escritura pública nombrando a mi representado/a como curador/a de la persona y bienes de su hermano/a en el caso de fallecimiento, de la cual consta la correspondiente indicación en el Registro Civil de [LOCALIDAD] y la cual se acompaña como DOCUMENTO N.º 9.

En consecuencia, y siendo vinculante el nombramiento realizado por delación voluntaria, según dispone el artículo 119 del Código del Derecho Foral de Aragón, se interesa que se nombre a mi representado/a como curador/a en este mismo proceso, no concurriendo en mi mandante ninguna de las causas de inhabilitación, tal y como se determina en el certificado de antecedentes penales que se aporta como DOCUMENTO N.º 10 y en la certificación expedida por el Registro Civil de [LOCALIDAD], y siendo asimismo de interés de la persona con discapacidad, dados los lazos afectivos de mi mandante con su hermano/a, como se acreditará en este proceso.

A los anteriores hechos les son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

Competencia

Se dirige la demanda a ese Tribunal por ser el competente, de conformidad con lo previsto en el artículo 756, apartados 1 y 2, de la LEC, siendo competente la autoridad judicial que conoció del previo expediente de jurisdicción voluntaria, al no haberse producido cambio de residencia.

Procedimiento

Se seguirá el cauce establecido en el art. 758 en relación con el art. 753 de la LEC, con las especificaciones que incluyen estos preceptos y en el art. 759 de la LEC.

Legitimación

Mi representado/a tiene legitimación activa conforme al art. 757.1 de la LEC, debiendo intervenir el Ministerio Fiscal y la propia persona con discapacidad, conforme a lo dispuesto en el art. 757.3 de la LEC, así como los demás legitimados, en su caso, según establece el art. 757.4 de la LEC.

Cumplimiento de los requisitos de procedibilidad

La presente demanda no está sujeta al previo intento de resolución de controversias en vía no jurisdiccional por tratarse de materias excluidas del requisito de procedibilidad de acuerdo con el art. 5.2 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

Constitución de la curatela

Artículos 100 y siguientes del Código del Derecho Foral de Aragón, en relación con los artículos 249 y siguientes del Código Civil.

Nombramiento de curador por delación voluntaria

Es de aplicación el artículo 116.3 del Código del Derecho Foral de Aragón, el cual establece, en referencia a la delación voluntaria del cargo tutelar, que «Las mismas disposiciones podrán establecerse para la curatela a que quede sujeto el hijo emancipado». En el mismo sentido, artículo 276 del Código Civil.

Asimismo, es de aplicación el artículo 119.1 del mismo Código Foral, que establece: «Las designaciones, exclusiones y demás disposiciones voluntarias sobre la tutela o curatela vincularán al Juez, salvo que, de oficio o a instancia de cualquiera de las personas llamadas por ley a ejercer la tutela o curatela o del Ministerio Fiscal, y siempre mediante decisión motivada, aprecie que se ha producido una alteración sustancial de las circunstancias o que concurren hechos relevantes no tenidos en cuenta».

Costas

El artículo 394 LEC, debiendo imponerse a los demandados en caso de temeridad o mala fe.

En virtud de lo expuesto,

AL TRIBUNAL SUPLICO: Tenga por presentado este escrito junto con el poder, documentos y copias, admitiéndolo, dándose a las copias el curso legal correspondiente, acordando tenerme por comparecido y parte en la representación que ostento en nombre de [NOMBRE Y APELLIDOS DEL DEMANDANTE], entendiéndose conmigo las sucesivas diligencias, teniendo por promovida demanda de provisión de medidas judiciales de apoyo de D./Dña. [NOMBRE Y APELLIDOS DE LA PERSONA CON DISCAPACIDAD], cuyas circunstancias personales han sido ya referenciadas y, tras su sustanciación, con la preceptiva intervención del Ministerio Fiscal, se dicte sentencia por la que se acuerde la adopción de las medidas de apoyo solicitadas, constituyendo la curatela o asistencia de la persona con discapacidad D./Dña. [NOMBRE Y APELLIDOS], determinando los actos para los que la persona requiere asistencia del curador o asistente en el ejercicio de su capacidad jurídica, atendiendo a sus concretas necesidades de apoyo conforme a lo expuesto, y nombrándose curador/a o asistente a mi representado/a, procediendo a darle posesión del cargo y señalándose las medidas de control y vigilancia que en beneficio de la persona con discapacidad se consideren necesarias, junto a lo demás que en Derecho proceda, ordenando su inscripción en el Registro Civil, y con condena en costas a la parte demandada, si concurrieren las circunstancias previstas en el artículo 394 de la Ley de Enjuiciamiento Civil.

OTROSÍ PRIMERO DIGO que solicito que se incorpore a estos autos, por original o testimonio, el expediente de jurisdicción voluntaria seguido a instancia de esta parte ante este mismo Tribunal con el número [Nº DE PROCEDIMIENTO].

SUPLICO AL TRIBUNAL tenga por hecha esta solicitud y acuerde de conformidad.

OTROSÍ SEGUNDO DIGO que se acompaña en anexo relación de documentos e informe pericial presentados con esta demanda, debidamente foliados y con índice electrónico, para su debida localización y consulta.

SUPLICO AL TRIBUNAL tenga hecha esta manifestación a los efectos oportunos y por aportados los documentos e informe pericial relacionados en el anexo.

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma Abogado: [NOMBRE Y APELLIDOS, Nº DE COLEGIADO]

Firma Procurador: [NOMBRE Y APELLIDOS]
