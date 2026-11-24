---
name: demanda-curatela-asistencia-nombramiento-curador-civ-0390
description: "Demanda de curatela o asistencia y nombramiento de curador o asistente (Derecho civil catalán). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de curatela o asistencia y nombramiento de curador o asistente (Derecho civil catalán)

> Formulario **CIV-0390** del plugin **Discapacidad y medidas de apoyo (Ley 8/2021)** (`formularios-discapacidad-y-medidas-de-apoyo`) · Civil › Capacidad y medidas de apoyo · normativa revisada el 24-11-2026.

## Qué es

Demanda de proceso especial de provisión de medidas judiciales de apoyo (curatela o asistencia) a favor de una persona con discapacidad, con designación previa de curador por la propia persona (autocuratela), conforme al Código Civil de Cataluña y a los artículos 756 y siguientes de la Ley de Enjuiciamiento Civil.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de curatela o asistencia y nombramiento de curador o asistente (Derecho civil catalán)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de curatela o asistencia y nombramiento de curador o asistente (Derecho civil catalán)” para mi caso». También puedes invocarla directamente con `/formularios-discapacidad-y-medidas-de-apoyo:demanda-curatela-asistencia-nombramiento-curador-civ-0390`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-discapacidad-y-medidas-de-apoyo:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Discapacidad y medidas de apoyo (Ley 8/2021)) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (8 veces)
- [ ] FECHA (5 veces)
- [ ] NOMBRE Y APELLIDOS DE LA PERSONA CON DISCAPACIDAD (4 veces)
- [ ] AÑO (3 veces)
- [ ] Nº DE PROCEDIMIENTO (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL DEMANDANTE (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] PARENTESCO (2 veces)
- [ ] ACTOS CONCRETOS: …
- [ ] DNI/NIE
- [ ] DOMICILIO PROFESIONAL
- [ ] DÍA
- [ ] FECHA O HECHO
- [ ] LOCALIDAD DE NACIMIENTO
- [ ] MES
- [ ] NOMBRE DEL NOTARIO
- [ ] NOMBRE Y APELLIDOS DE LAS PERSONAS AFECTADAS
- [ ] NOMBRE Y APELLIDOS DEL FACULTATIVO
- [ ] NOMBRE Y APELLIDOS DEL LETRADO
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR
- [ ] Nº
- [ ] Nº DE COLEGIADO
- [ ] Nº DE FOLIOS
- [ ] Nº DE PROTOCOLO
- [ ] OTRAS PERSONAS
- [ ] PROFESIÓN
- [ ] SEDE

## Normas que cita el formulario

- art. 223 Código Civil
- art. 5.2 Ley Orgánica 1/2025
- art. 249 Código Civil
- art. 226 Código Civil

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

### Avisos de actualización (4) — se aplican en el texto, nunca se copian en el documento

- Junto a «…MILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.
- Junto a «… acreditativos certificado negativo de antecedentes penales como DOCUMENTO Nº 9.»: el original citaba aquí el «art. 233-10» del Código Civil de Cataluña; se ha sustituido por el 223-10 por parecer errata, pero debe comprobarse el artículo exacto que se desee invocar.
- Junto a «…Barcelona de 17 de junio de 2008, de 19 de mayo de 2009 y de 15 de julio de 2009»: el original no traía el número de resolución de estas sentencias; completar con el ECLI o el número de recurso antes de citarlas

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

Don/Doña [NOMBRE Y APELLIDOS DEL PROCURADOR], Procurador de los Tribunales, actuando en nombre y representación de Don/Doña [NOMBRE Y APELLIDOS DEL DEMANDANTE], mayor de edad, [ESTADO CIVIL], de profesión [PROFESIÓN], vecino/a de [LOCALIDAD], con domicilio en [DOMICILIO], tal y como consta en la copia electrónica del poder notarial de representación [ELEGIR: que se adjunta / según acreditaré mediante apoderamiento apud acta el día y hora que determine este Tribunal], actuando bajo la dirección letrada de Don/Doña [NOMBRE Y APELLIDOS DEL LETRADO], colegiado/a nº [Nº DE COLEGIADO], con domicilio profesional en [DOMICILIO PROFESIONAL], ante el Tribunal comparezco y, como mejor proceda en Derecho, DIGO:

Que en la indicada representación formulo demanda de adopción de medidas judiciales de apoyo a personas con discapacidad respecto de [PARENTESCO: por ejemplo, la madre] de mi representado/a, Doña/Don [NOMBRE Y APELLIDOS DE LA PERSONA CON DISCAPACIDAD], provista de DNI [DNI/NIE], nacida en [LOCALIDAD DE NACIMIENTO] en fecha [FECHA], de estado civil [ESTADO CIVIL], con domicilio en [DOMICILIO]; se aporta como DOCUMENTO Nº 1 certificación literal de nacimiento expedida por el Registro Civil de [LOCALIDAD], todo ello en base a los siguientes

HECHOS

Relaciones de parentesco

PRIMERO.– La persona con discapacidad es [PARENTESCO] de mi mandante, tal y como se acredita mediante la certificación literal expedida por el Registro Civil de [LOCALIDAD] que se aporta como DOCUMENTO Nº 1. [OPCIONAL — si ha lugar] Es de estado civil viudo/a por haber fallecido en fecha [FECHA] su cónyuge, Don/Doña [NOMBRE Y APELLIDOS], tal y como se acredita mediante certificado de defunción que se aporta como DOCUMENTO Nº 2. Tiene [NÚMERO] hijos, según se acredita mediante certificaciones del Registro Civil que se acompañan como DOCUMENTOS Nº 3 a [Nº].

En relación con la enfermedad padecida y su evolución

SEGUNDO.– Doña/Don [NOMBRE Y APELLIDOS DE LA PERSONA CON DISCAPACIDAD] padece [DIAGNÓSTICO: por ejemplo, una enfermedad neurodegenerativa de larga evolución], diagnosticada por el Doctor Don/Doña [NOMBRE Y APELLIDOS DEL FACULTATIVO], tal y como consta acreditado en el informe elaborado por dicho facultativo, que se aporta como DOCUMENTO Nº 6, en el cual se expresa que padece dicha enfermedad desde el año [AÑO], con un progresivo deterioro cognitivo y trastornos conductuales. Si bien la enfermedad fue objeto de tratamiento desde su diagnóstico, ha venido progresando de forma degenerativa, en especial desde [HECHO RELEVANTE: por ejemplo, el fallecimiento del cónyuge en el año [AÑO]], presentando actualmente [DESCRIPCIÓN DE LA SITUACIÓN ACTUAL: por ejemplo, una situación de deterioro irreversible, con trastornos conductuales graves, estando impedida para gobernarse por sí misma] [OPCIONAL — si ha lugar] y comportamientos de agresividad que han derivado en varios episodios con consecuencias para la integridad física de [NOMBRE Y APELLIDOS DE LAS PERSONAS AFECTADAS].

Expediente de jurisdicción voluntaria previo

TERCERO.– La situación de discapacidad de la persona demandada determinó que mi representado/a instara expediente de jurisdicción voluntaria de provisión de medidas judiciales de apoyo ante el Tribunal al que me dirijo, siguiéndose el procedimiento número [Nº DE PROCEDIMIENTO], el cual finalizó al haberse formulado oposición por el Ministerio Fiscal, lo que determina la interposición de la presente demanda, de conformidad con lo dispuesto en el artículo 756 y siguientes de la Ley de Enjuiciamiento Civil.

De la situación actual

CUARTO.– El estadio de la patología padecida es calificado, conforme al último examen médico realizado a fecha [FECHA], que se aporta como DOCUMENTO Nº 7, de [GRAVEDAD: por ejemplo, muy intenso y totalmente irreversible], necesitando cuidados permanentes de una tercera persona.

La idoneidad de las medidas propuestas se acredita mediante los diferentes informes de los facultativos que han venido atendiendo la patología durante estos años, así como mediante el informe de los servicios sociales del Ayuntamiento de [LOCALIDAD], los cuales se acompañaron con la solicitud presentada en el expediente de jurisdicción voluntaria seguido con el número [Nº DE PROCEDIMIENTO] en este Tribunal, cuya incorporación por testimonio a este proceso se solicita desde este momento, designando los particulares que comprenden dichos informes, obrantes en los folios [Nº DE FOLIOS].

Relaciones familiares y situación de guarda

QUINTO.– [PARENTESCO] del demandante, Doña/Don [NOMBRE Y APELLIDOS DE LA PERSONA CON DISCAPACIDAD], está residiendo en la actualidad en el domicilio del demandante, quien se ocupa de forma exclusiva de sus cuidados desde [FECHA O HECHO]. La persona con discapacidad tiene otros [NÚMERO] hijos, que residen en [LOCALIDAD] y en [LOCALIDAD], respectivamente, si bien [DESCRIPCIÓN DE SU IMPLICACIÓN: por ejemplo, no se han ocupado de ella, habiendo propuesto en reiteradas ocasiones su internamiento en un centro cerrado, a lo cual siempre se ha negado mi representado/a por respeto a lo dispuesto por la persona con discapacidad en la escritura de autocuratela de fecha [FECHA], a la que seguidamente se hará referencia].

Autocuratela y designación de curador o asistente

SEXTO.– Tal como se ha indicado, la persona demandada, en fecha [FECHA], ostentando plena capacidad y en previsión de que su enfermedad progresaría de forma degenerativa, otorgó escritura pública de designación de curador y asistente a favor de mi representado/a ante el Notario de [LOCALIDAD], Don/Doña [NOMBRE DEL NOTARIO], con número de protocolo [Nº DE PROTOCOLO], manifestando su voluntad de ser cuidada en su persona y bienes por mi representado/a y de residir en su domicilio junto a la familia de este/a o, en otro caso, en compañía de [OTRAS PERSONAS], expresando que no quería ser internada en un centro, salvo que fuera estrictamente imprescindible (se acompaña como DOCUMENTO Nº 8 copia autorizada de la citada escritura de autocuratela).

Por este motivo, siendo la persona designada mi mandante y habiendo respetado la voluntad de la persona con discapacidad, se interesa que se le nombre curador/a o asistente, respetando el margen de autonomía de la voluntad que establece el artículo 222-4 en relación con los artículos 223-10 y 226-3 del Código Civil de Cataluña, y al no darse las limitaciones temporales establecidas en el apartado 3 del citado artículo 222-4, reuniendo mi representado/a las condiciones de aptitud e idoneidad establecidas legalmente, aportando a efectos acreditativos certificado negativo de antecedentes penales como DOCUMENTO Nº 9.

A los anteriores hechos les son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

Competencia

Se dirige la demanda a este Tribunal por ser el competente, de conformidad con lo previsto en el artículo 756, apartados 1 y 2, de la Ley de Enjuiciamiento Civil, siendo competente la autoridad judicial que conoció del previo expediente de jurisdicción voluntaria, al no haberse producido cambio de residencia.

Procedimiento

Se seguirá el cauce establecido en el artículo 758 en relación con el artículo 753 de la Ley de Enjuiciamiento Civil, con las especificaciones que incluyen estos preceptos y el artículo 759 de la misma ley.

Legitimación

Mi representado/a tiene legitimación activa conforme al artículo 757.1 de la Ley de Enjuiciamiento Civil, debiendo intervenir el Ministerio Fiscal y la propia persona con discapacidad, conforme a lo dispuesto en el artículo 757.3 de la misma ley, así como los demás legitimados, en su caso, según establece el artículo 757.4.

Cumplimiento de los requisitos de procedibilidad

La presente demanda no está sujeta al previo intento de resolución de controversias en vía no jurisdiccional por tratarse de un proceso excluido del requisito de procedibilidad de acuerdo con el artículo 5.2 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

Medidas judiciales de apoyo: curatela o asistencia

Artículos 222-1 y siguientes del Código Civil de Cataluña, en relación con los artículos 249 y siguientes del Código Civil, y artículos 223-1, 226-1 y siguientes del Código Civil de Cataluña en referencia a la curatela o asistencia.

Delación voluntaria: autocuratela

Artículo 222-4 del Código Civil de Cataluña. En el mismo sentido, artículo 226-3 del Código Civil de Cataluña, en cuanto establece que cualquier persona mayor de edad, en escritura pública, en previsión o apreciación de una situación de necesidad de apoyo, puede nombrar a una o más personas para que ejerzan la asistencia y puede establecer disposiciones con respecto al funcionamiento y al contenido del régimen de apoyo adecuado, incluso con respecto al cuidado de su persona.

[OPCIONAL — incluir si procede] En interpretación de estos preceptos se citan las sentencias de la Audiencia Provincial de Barcelona de 17 de junio de 2008, de 19 de mayo de 2009 y de 15 de julio de 2009 .

Costas

Artículo 394 de la Ley de Enjuiciamiento Civil, en caso de oposición con mala fe o temeridad.

En virtud de lo expuesto,

AL TRIBUNAL SUPLICO: Que tenga por presentado este escrito junto con el poder, documentos y copias, admitiéndolo y dando a las copias el curso legal correspondiente; me tenga por comparecido y parte en la representación que ostento en nombre de [NOMBRE Y APELLIDOS DEL DEMANDANTE], entendiéndose conmigo las sucesivas diligencias; tenga por promovida demanda de provisión de medidas judiciales de apoyo de Doña/Don [NOMBRE Y APELLIDOS DE LA PERSONA CON DISCAPACIDAD], cuyas circunstancias personales han sido ya referenciadas, y tras su sustanciación, con la preceptiva intervención del Ministerio Fiscal, dicte sentencia por la que se acuerde la adopción de las medidas de apoyo solicitadas, constituyendo la curatela o asistencia de la persona con discapacidad Doña/Don [NOMBRE Y APELLIDOS], determinando los actos para los que la persona requiere asistencia del curador o asistente en el ejercicio de su capacidad jurídica, atendiendo a sus concretas necesidades de apoyo conforme a lo expuesto [ACTOS CONCRETOS: …], y nombrando curador/a o asistente a mi representado/a, procediendo a darle posesión del cargo y señalando las medidas de control y vigilancia que en beneficio de la persona con discapacidad se consideren necesarias, junto a lo demás que en Derecho proceda, ordenando su inscripción en el Registro Civil, y con condena en costas a la parte demandada, si concurrieren las circunstancias previstas en el artículo 394 de la Ley de Enjuiciamiento Civil.

OTROSÍ PRIMERO DIGO: que solicito que se incorpore a estos autos, por original o testimonio, el expediente de jurisdicción voluntaria seguido a instancia de esta parte ante este mismo Tribunal con el número [Nº DE PROCEDIMIENTO].

SUPLICO AL TRIBUNAL: que tenga por hecha esta solicitud y acuerde de conformidad.

OTROSÍ SEGUNDO DIGO: que se acompaña en anexo relación de documentos e informe pericial presentados con esta demanda, debidamente foliados y con índice electrónico, para su debida localización y consulta.

SUPLICO AL TRIBUNAL: que tenga hecha esta manifestación a los efectos oportunos y por aportados los documentos e informe pericial relacionados en el anexo.

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado y del Procurador
