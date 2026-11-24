---
name: demanda-mutuo-acuerdo-sobre-guarda-custodia-compartida-civ-0142
description: "Demanda de mutuo acuerdo sobre guarda y custodia compartida tras ruptura de pareja (Derecho catalán). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de mutuo acuerdo sobre guarda y custodia compartida tras ruptura de pareja (Derecho catalán)

> Formulario **CIV-0142** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda de mutuo acuerdo de dos progenitores, que formaron una pareja estable y ya no conviven, para que el Tribunal apruebe el convenio regulador y el plan de parentalidad con guarda y custodia compartida de su hijo menor, conforme al Código Civil de Cataluña (libros segundo, arts. 233 y 234 CCC).

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de mutuo acuerdo sobre guarda y custodia compartida tras ruptura de pareja (Derecho catalán)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de mutuo acuerdo sobre guarda y custodia compartida tras ruptura de pareja (Derecho catalán)” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-mutuo-acuerdo-sobre-guarda-custodia-compartida-civ-0142`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] Nº DE DOCUMENTO (6 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] NOMBRE DEL HIJO/A (3 veces)
- [ ] MES (2 veces)
- [ ] AÑO
- [ ] COLEGIO DE ABOGADOS
- [ ] DOMICILIO COMÚN
- [ ] DOMICILIO DE LA MADRE
- [ ] DOMICILIO DEL PADRE
- [ ] DOMICILIO PROFESIONAL
- [ ] DÍA
- [ ] FECHA
- [ ] FECHA DE NACIMIENTO
- [ ] NOMBRE Y APELLIDOS DEL LETRADO
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº
- [ ] Nº DE COLEGIADO
- [ ] O SECCIÓN CIVIL, SEGÚN LA ORGANIZACIÓN DE LA SEDE
- [ ] SEDE

## Normas que cita el formulario

- art. 234 CC
- art. 233 CC
- art. 1.2 Real Decreto 1322/1981

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

### Avisos de actualización (0) — se aplican en el texto, nunca se copian en el documento

- Ninguno.

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

AL TRIBUNAL DE INSTANCIA DE [SEDE]

SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD [O SECCIÓN CIVIL, SEGÚN LA ORGANIZACIÓN DE LA SEDE]

D./Dª [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, que actúa en nombre y representación de Doña [NOMBRE Y APELLIDOS] y Don [NOMBRE Y APELLIDOS], mayores de edad, solteros, vecinos de [LOCALIDAD] y con domicilio en [DOMICILIO DE LA MADRE] y [DOMICILIO DEL PADRE], respectivamente, según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como doc. n.º [Nº DE DOCUMENTO], bajo dirección del Letrado D./Dª [NOMBRE Y APELLIDOS DEL LETRADO], colegiado n.º [Nº DE COLEGIADO] del Ilustre Colegio de Abogados de [COLEGIO DE ABOGADOS], cuyo despacho se abre en [DOMICILIO PROFESIONAL], ante el Tribunal comparezco y, como mejor en Derecho proceda,

DIGO:

Que por medio del presente escrito, siguiendo las instrucciones de mis mandantes, vengo a formular DEMANDA DE MUTUO ACUERDO SOBRE GUARDA Y CUSTODIA DE HIJOS MENORES, con base en los siguientes

HECHOS

PRIMERO.- Doña [NOMBRE Y APELLIDOS] y Don [NOMBRE Y APELLIDOS] formaron familia natural desde la fecha [FECHA], en la que iniciaron su relación paramatrimonial con intención de permanencia y consolidación, como se acredita mediante certificación expedida por el Registro Municipal de Uniones Civiles del Ayuntamiento de [LOCALIDAD], que se acompaña como doc. n.º [Nº DE DOCUMENTO].

SEGUNDO.- Fruto de esta unión nació un hijo, de nombre [NOMBRE DEL HIJO/A], nacido el [FECHA DE NACIMIENTO], inscrito en el Registro Civil de [LOCALIDAD], [DATOS REGISTRALES: Libro, Tomo, Folio], por consiguiente menor de edad; aparece inscrito como hijo de mis mandantes, según se demuestra con la certificación literal de nacimiento que se acompaña como doc. n.º [Nº DE DOCUMENTO].

TERCERO.- Esta convivencia lo ha sido con carácter paramatrimonial, en el sentido de relación afectiva semejante a la de las parejas casadas, [ELEGIR: heterosexual / entre personas del mismo sexo], monógama, estable y duradera, puesto que alcanzó [Nº] años, apareciendo ante los vecinos, amigos, compañeros de trabajo y familiares como marido y mujer, compartiendo techo, ingresos y vida sentimental, siendo el último domicilio común [DOMICILIO COMÚN], como acredita el contrato de arrendamiento que se adjunta como doc. n.º [Nº DE DOCUMENTO].

CUARTO.- Desde el pasado mes de [MES], por desavenencias que no vienen al caso, mis mandantes viven de forma separada en los domicilios anteriormente referenciados, y han cursado además la baja como pareja estable en el citado Registro de Uniones de Hecho, cuyo certificado se aporta como doc. n.º [Nº DE DOCUMENTO].

QUINTO.- Tras un periodo de reflexión, convencidos de que la convivencia entre ambos era difícil y su mantenimiento podía perjudicar los intereses de su hijo común [NOMBRE DEL HIJO/A], han decidido definitivamente poner fin a su relación afectiva, según lo establecido por el art. 234-4.1 a) del Código Civil de Cataluña (en adelante, CCC) y, de mutuo acuerdo, suscribir propuesta de convenio regulador, en cumplimiento de lo establecido por el apartado 2 del art. 234-6 CCC, en relación con el art. 233-2 del mismo texto, para formalizar los efectos de su ruptura respecto a las relaciones paterno-filiales.

SEXTO.- Después de diversas conversaciones, Doña [NOMBRE Y APELLIDOS] y Don [NOMBRE Y APELLIDOS] están plenamente persuadidos de que la guarda y custodia compartida tiene evidentes beneficios tanto para el hijo, cuyo superior interés prevalece, como para los propios padres, por lo que han convenido de común acuerdo el establecimiento de dicho régimen, que habrá de regir las relaciones parentales del menor [NOMBRE DEL HIJO/A] con sus progenitores.

A estos efectos, se adjunta al presente escrito, como doc. n.º [Nº DE DOCUMENTO], la propuesta de convenio firmada por ambos progenitores, que incluye plan de parentalidad para el ejercicio de las responsabilidades parentales con respecto a la guarda, cuidado y educación del hijo común, ajustado a las exigencias del art. 233-9 CCC, cuya aprobación se interesa del Tribunal.

A los anteriores hechos son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

I.- CAPACIDAD.

Mis representados ostentan la capacidad procesal necesaria conforme a lo establecido en los arts. 6 y siguientes de la Ley de Enjuiciamiento Civil.

II.- LEGITIMACIÓN.

Mis representados se hallan legitimados por haber formado parte de la unión de hecho y en su condición de padres del menor sobre el que han de recaer los efectos del convenio suscrito entre las partes, habida cuenta de que son los que se hallan en la situación jurídica respectiva del derecho-deber de cuidar de los hijos menores no emancipados (arts. 236-1 y 236-17.1 CCC).

III.- JURISDICCIÓN.

Es competente la jurisdicción civil, conforme a lo dispuesto en los arts. 9.2 y 21.1 de la Ley Orgánica del Poder Judicial.

IV.- COMPETENCIA.

Es competente el Tribunal al que nos dirigimos de conformidad con lo dispuesto en el art. 769.3 de la Ley de Enjuiciamiento Civil [OPCIONAL — incluir si procede: en relación con el art. 1.2 del Real Decreto 1322/1981, de 3 de julio], que fija como fuero de competencia territorial el correspondiente al Tribunal del lugar del último domicilio común de los progenitores.

V.- PROCEDIMIENTO.

En cuanto al procedimiento a seguir, resulta de aplicación el trámite previsto en el art. 777 de la Ley de Enjuiciamiento Civil, que regula el procedimiento de mutuo acuerdo, y ello en virtud de la remisión que establece la disposición adicional 5.ª CCC en relación con el art. 748.4.º de la Ley de Enjuiciamiento Civil.

VI.- POSTULACIÓN.

Al amparo de lo dispuesto en el art. 750.2 de la Ley de Enjuiciamiento Civil, para el caso de solicitudes de común acuerdo se concurre con una sola defensa y representación.

VII.- FONDO DE LA PRETENSIÓN.

El art. 234-7 CCC regula el ejercicio de la guarda de los hijos y las relaciones personales tras la extinción de la pareja estable, con remisión a los genéricos arts. 233-8 a 233-13 CCC sobre las relaciones parentales tras las rupturas matrimoniales.

Es evidente, abstracción hecha de las opiniones que desde planteamientos militantes se han emitido profusamente en los últimos tiempos, que la llamada custodia compartida o conjunta por ambos progenitores presenta indudables ventajas para la evolución y desarrollo del niño en las situaciones de conflicto familiar producido por la ruptura, en la medida en que evita la aparición de los «conflictos de lealtades» de los menores para con sus padres, favorece la comunicación de éstos entre sí, aunque no sirva para disminuir las diferencias entre ellos —tampoco puede afirmarse que las acentúe— y, en fin, coadyuva, por un lado, a visualizar la ruptura familiar como un conflicto en el que no existen vencedores y vencidos ni culpables e inocentes, y por otro, a concebir el reparto equilibrado de cargas derivadas de la relación paterno-filial como algo consustancial y natural, y no como algo eventual o accidental, favoreciendo la implantación en los hijos de la idea de la igualdad de sexos.

En este sentido, resulta clarificadora la enumeración de efectos positivos contenida en la sentencia de la Audiencia Provincial de Barcelona (Sección 18.ª) de 20 de febrero de 2007, rec. 1002/2005, conforme a la cual:

«a) se garantiza a los hijos la posibilidad de disfrutar de la presencia de ambos progenitores, pese a la ruptura de las relaciones de pareja, siendo tal presencia similar de ambas figuras parentales y constituye el modelo de convivencia que más se acerca a la forma de vivir de los hijos durante la convivencia de pareja de sus padres, por lo que la ruptura resulta menos traumática; b) se evitan determinados sentimientos negativos en los menores, entre los cuales cabe relacionar los siguientes: miedo al abandono; sentimiento de lealtad; sentimiento de culpa; sentimiento de negación; sentimiento de suplantación; etc.; c) se fomenta una actitud más abierta de los hijos hacia la separación de los padres que permite una mayor aceptación del nuevo contexto y se evitan situaciones de manipulación consciente o inconsciente por parte de los padres frente a los hijos; e) se garantiza a los padres la posibilidad de seguir ejerciendo sus derechos y obligaciones inherentes a la potestad o responsabilidad parental y de participar en igualdad de condiciones en el desarrollo y crecimiento de sus hijos, evitando, así, el sentimiento de pérdida que tiene el progenitor cuando se atribuye la custodia al otro progenitor y la desmotivación que se deriva cuando debe abonarse la pensión de alimentos, consiguiendo, además, con ello, una mayor concienciación de ambos en la necesidad de contribuir a los gastos de los hijos; f) no se cuestiona la idoneidad de ninguno de los progenitores; g) hay una equiparación entre ambos progenitores en cuanto a tiempo libre para su vida personal y profesional, con lo que se evitan de esta manera dinámicas de dependencia en la relación con los hijos, pues en ocasiones el dolor y vacío que produce una separación se tiende a suplir con la compañía del hijo o hija que se convierte así en la única razón de vivir de un progenitor; y h) los padres han de cooperar necesariamente, por lo que el sistema de guarda compartida favorece la adopción de acuerdos, lo que se convierte asimismo en un modelo educativo de conducta para el menor.»

En la misma línea, el Informe de 1995 de la División 16 de la American Psychological Association ante la Comisión USA de Bienestar Infantil y Familiar concluía que «la custodia compartida se asocia con ciertos efectos favorables en los niños», sobre todo cuando se complementa con la mediación y los programas de educación parental, por lo que recomendaba «favorecer el incremento de la mediación, la custodia compartida y la educación de los progenitores».

Lo mismo se desprende de otros estudios ampliamente difundidos, tales como el Informe Bauserman —Child Adjustment in Joint-Custody Versus Sole-Custody Arrangements: A Meta-Analytic Review (2002)—, el Informe Kelly —Children's adjustment in conflicted marriage and divorce. A decade review of Research (2000)— o el documento Bailly —Etat des connaissances scientifiques sur la résidence alternée (2002)—, entre otros muchos.

Por otro lado, sin que pueda afirmarse que la coparentalidad y el mantenimiento de las responsabilidades parentales compartidas constituyan una solución única para todos los casos, nítidamente se construye en el diseño pergeñado por el CCC como una solución preferencial (cfr. art. 233-10 CCC), como viene haciéndose en otros países de nuestro entorno, entendiéndose que elimina las dinámicas de ganadores y perdedores, y favorece la colaboración en los aspectos afectivos, educativos y económicos, sin perjuicio de que la autoridad judicial deba decidir de acuerdo con las circunstancias de cada caso y en función del interés concreto de los hijos.

En el presente supuesto, la ponderación de las circunstancias del caso (cfr. art. 233-11 CCC), tales como la edad del hijo, el horario laboral y profesional de los progenitores, la proximidad del lugar de residencia de ambos progenitores, la disponibilidad por éstos de una residencia adecuada para tener consigo al hijo, el tiempo libre o de vacaciones y la propia opinión del menor al respecto, avala la conveniencia de establecer un sistema de custodia compartida como el que se propone, por todo lo cual se solicita su aprobación judicial en su integridad, en aras a garantizar el interés del menor.

VIII.- INTERVENCIÓN DEL MINISTERIO FISCAL.

Con arreglo al art. 749.2 de la Ley de Enjuiciamiento Civil, deberá ser parte el Ministerio Fiscal, por hacerse referencia a cuestiones en las que debe intervenir, dado que se trata de pactos relativos a medidas que afectan a menores.

IX.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda no está sujeta al previo intento de resolución de controversias en vía no jurisdiccional exigido por la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia, por tratarse en sí de un acuerdo consensual y voluntario entre las partes, necesitando únicamente la homologación del mismo por parte del Tribunal.

Por lo expuesto,

SUPLICO AL TRIBUNAL

Que, teniendo por presentado este escrito con los documentos que se acompañan y sus copias, se digne admitirlos, tenerme por comparecido y parte en la representación que ostento, entendiéndose conmigo las sucesivas diligencias, y previos los pertinentes trámites, los progenitores sean requeridos por el Letrado de la Administración de Justicia para que comparezcan y se ratifiquen por separado, con citación del Ministerio Fiscal, dictándose en su día sentencia por la que, estimando la presente DEMANDA SOBRE GUARDA Y CUSTODIA DEL HIJO MENOR, se acuerde aprobar judicialmente en su integridad la propuesta de convenio regulador y el plan de parentalidad que contiene, presentado de mutuo acuerdo, acordándose el establecimiento del régimen de guarda y custodia compartida entre los progenitores.

Es justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a Firma del Procurador/a
