---
name: demanda-mutuo-acuerdo-parejas-hecho-hijos-menores-civ-0083
description: "Demanda de mutuo acuerdo de parejas de hecho con hijos menores. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de mutuo acuerdo de parejas de hecho con hijos menores

> Formulario **CIV-0083** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de mutuo acuerdo de parejas de hecho con hijos menores» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de mutuo acuerdo de parejas de hecho con hijos menores” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-mutuo-acuerdo-parejas-hecho-hijos-menores-civ-0083`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (20 veces)
- [ ] Nº (8 veces)
- [ ] Nº DE DOCUMENTO (7 veces)
- [ ] CALLE (5 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] PISO (4 veces)
- [ ] FECHA (3 veces)
- [ ] AÑO (2 veces)
- [ ] Nº DE COLEGIADO (2 veces)
- [ ] PUERTA (2 veces)
- [ ] C.P.
- [ ] COLEGIO
- [ ] COLEGIO DE ABOGADOS
- [ ] DOMICILIO
- [ ] DÍA
- [ ] EDAD
- [ ] EXPONER LOS HECHOS
- [ ] LUGAR
- [ ] MES
- [ ] Nº DE COLEGIADO/A
- [ ] Nº DE FAX
- [ ] Nº DE PROCEDIMIENTO
- [ ] Nº DE PROTOCOLO
- [ ] PROFESIÓN
- [ ] RÉGIMEN ECONÓMICO
- [ ] SEDE
- [ ] TELÉFONO

## Normas que cita el formulario

- art. 85.1 LOPJ

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
- Junto a «…l Poder Judicial. b) De los concursos de persona natural que no sea empresario».»: el texto legal citado entre comillas es la redacción anterior a la LO 1/2025; hoy esas competencias corresponden a la Sección Civil del Tribunal de Instancia. Fuente: LO 1/2025 (BOE-A-2025-76).
- Junto a «…EGIADO] ========================================================================»: requisito de procedibilidad del art. 5 LO 1/2025 — antes de presentar la demanda hay que intentar un medio adecuado de solución de controversias (MASC) y acreditarlo con la demanda (arts. 264.4.º y 399.3 LEC), salvo las materias excluidas del art. 5.2. Fuente: LO 1/2025, arts. 5 a 7 (BOE-A-2025-76).

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

Don/doña [NOMBRE Y APELLIDOS], Procurador de los Tribunales con número de colegiado [Nº DE COLEGIADO/A] y de Don/doña [NOMBRE Y APELLIDOS], mayor de edad, con DNI núm. [Nº], y con domicilio personal en [DOMICILIO], calle [CALLE], núm. [Nº], piso [PISO] puerta [PUERTA], código postal [C.P.], teléfono [TELÉFONO], fax [Nº DE FAX]; según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño a este escrito, asistido por el/la Letrado/a del Ilustre Colegio de Abogados de [COLEGIO], don/doña [NOMBRE Y APELLIDOS] núm. [Nº] de colegiación [COLEGIO DE ABOGADOS] como mejor proceda en Derecho comparezco y digo:

Que mediante el presente escrito insto JUICIO ORDINARIO EN SOLICITUD DE HOMOLOGACIÓN DE LOS ACUERDOS DE LA RUPTURA CONVIVENCIAL de la unión estable entre mi mandante don [NOMBRE Y APELLIDOS], y doña [NOMBRE Y APELLIDOS], mayor de edad, de profesión [PROFESIÓN], con domicilio en la C./ [CALLE] núm. [Nº] de [LOCALIDAD], DNI y NIF núm. [Nº]; teléfono núm. [Nº], fax núm. [Nº]; dirección de correo electrónico

Al presente escrito se acompaña documento privado que recoge los acuerdos a los que han llegado, con objeto de que se apruebe judicialmente, que se acompaña como documento número 2.

Solicitud que se fundamenta en los siguientes:

HECHOS

PRIMERO Doña [NOMBRE Y APELLIDOS] y don [NOMBRE Y APELLIDOS] iniciaron una relación sentimental [o paramatrimonial] en fecha [FECHA] con intención de permanencia y consolidación, es decir, en análoga relación de afectividad que el matrimonio.

- Se adjunta como documento núm. [Nº DE DOCUMENTO]: certificado de empadronamiento en la vivienda sita en [LOCALIDAD], calle [CALLE] núm. piso [PISO] puerta [PUERTA]

- Se adjunta como documento núm. [Nº DE DOCUMENTO]: contrato de arrendamiento en el que consta como titular don [NOMBRE Y APELLIDOS] y doña [NOMBRE Y APELLIDOS]

- Se adjunta como documento núm. [Nº DE DOCUMENTO].

SEGUNDO De la relatada unión [EXPONER LOS HECHOS]

- Se aportan [Nº DE DOCUMENTO] en extracto de nacimiento, de los Registros Civiles correspondientes.

- Se adjunta como documento núm. [Nº DE DOCUMENTO]: Libro de familia correspondiente.

TERCERO El último domicilio convivencial estuvo situado en la calle [CALLE] núm. piso [PISO], de [LOCALIDAD], donde residen en la actualidad doña [NOMBRE Y APELLIDOS] y [EDAD] de edad. Ambos convivientes conviniendo de mutuo acuerdo que don [NOMBRE Y APELLIDOS] abandonara dicho domicilio, residiendo éste en la actualidad y desde entonces en [LOCALIDAD] calle [CALLE] núm. [Nº], piso [PISO] puerta

- Se acompaña como documentos núms. y [Nº DE DOCUMENTO]: Certificados de empadronamiento del año [AÑO], en el que figuran inscritos mi representada con [NOMBRE Y APELLIDOS], por un lado; y don [NOMBRE Y APELLIDOS] en el nuevo domicilio indicado.

CUARTO Habiendo surgido dificultades en la convivencia que no son del caso relatar, ambos convivientes han decidido solicitar la declaración de ruptura judicialmente.

QUINTO En cuanto al régimen económico de la pareja, ésta ha venido rigiéndose por un régimen [RÉGIMEN ECONÓMICO], establecido mediante escritura pública de fecha [FECHA] otorgada ante el Notario de esta ciudad Don [NOMBRE Y APELLIDOS] (núm. Protocolo [Nº DE PROTOCOLO]) [o bien, por contrato privado entre ambos convivientes, estando ambos conformes en la forma y términos de su liquidación].

SEXTO Y siendo el interés de ruptura expresado, de ambos convivientes, interpone mi representado/a la presente solicitud de declaración de ruptura y aprobación de los efectos, con el consentimiento de don/doña [NOMBRE Y APELLIDOS], adjuntando a tal efecto propuesta de convenio regulador firmado por ambos, que interesa sea aprobado como medidas definitivas.

- Se adjunta como documento núm. [Nº DE DOCUMENTO]: Original de la propuesta de acuerdos alcanzados por los convivientes en fecha [FECHA] por triplicado ejemplar a un solo efecto.

A estos hechos son de aplicación los siguientes,

A) FUNDAMENTOS DE DERECHO PROCESAL

Capacidad de las partes

- Art. 6 LECiv: «Capacidad para ser parte. 1. Podrán ser parte en los procesos ante los tribunales civiles: 1. Las personas físicas».

En consecuencia, tienen capacidad para ser parte tanto los solicitantes en el presente proceso.

Representación procesal

- Art. 23 LECiv: «Intervención de Procurador. 1. La comparecencia en juicio será por medio de Procurador legalmente habilitado para actuar en el tribunal que conozca del juicio [Nº DE PROCEDIMIENTO]».

Representación de las partes

- Art. 7 LECiv: «Comparecencia en juicio y representación.

1. Sólo podrán comparecer en juicio los que estén en el pleno ejercicio de sus derechos civiles.

2. Las personas físicas que no se hallen en el caso del apartado anterior habrán de comparecer mediante la representación o con la asistencia, la autorización, la habilitación o el defensor exigidos por la ley».

Defensa letrada

- Art. 31 LECiv: «Intervención de abogado. 1. Los litigantes serán dirigidos por abogados habilitados para ejercer su profesión en el tribunal que conozca del asunto. No podrá proveerse a ninguna solicitud que no lleve la firma de Abogado».

Intervención del Ministerio Fiscal

- Art. 749.2 LECiv: « En los demás procesos a que se refiere este Título será preceptiva la intervención del Ministerio Fiscal, siempre que alguno de los interesados en el procedimiento sea menor, incapacitado o esté en situación de ausencia legal».

Jurisdicción

- Art. 5 LECiv: « Se podrá pretender de los tribunales la condena a determinada prestación, la declaración de la existencia de derechos y de situaciones jurídicas, la constitución, modificación o extinción de estas últimas, la ejecución, la adopción de medidas cautelares y cualquier otra clase de tutela que esté expresamente prevista por la ley. 2. Las pretensiones a que se refiere el apartado anterior se formularán ante el tribunal que sea competente y frente a los sujetos a quienes haya de afectar la decisión pretendida».

Competencia objetiva

- Art. 45 LECiv: «Competencia de los Juzgados de Primera Instancia. Corresponde a los Juzgados de Primera Instancia el conocimiento, en primera instancia, de todos los asuntos civiles que por disposición legal expresa no se hallen atribuidos a otros Tribunales. Conocerán, asimismo, dichos Juzgados a) De los asuntos, actos, cuestiones y recursos que les atribuye la Ley Orgánica del Poder Judicial. b) De los concursos de persona natural que no sea empresario».

Por otro lado, el art. 85.1º LOPJ, tras la reforma de la LO 1/2025, establece que los Tribunales de Instancia son los órganos judiciales de base en el ámbito civil, asumiendo las competencias que antes tenían los Tribunales de Instancia (Sección Civil).

En consecuencia, corresponde conocer del presente asunto a los Tribunales de Instancia, en tanto que no se haya atribuido a otros tribunales.

Competencia funcional

- Art. 61 LECiv: «Competencia funcional por conexión. Salvo disposición legal en otro sentido, el Tribunal que tenga competencia para conocer de un pleito, la tendrá también para resolver sobre sus incidencias, para llevar a efecto las providencias y autos que dictare, y para la ejecución de la sentencia o convenios y transacciones que aprobare».

- Art. 62 LECiv: «Apreciación de oficio de la competencia para conocer de los recursos. 1. No serán admitidos a trámite los recursos dirigidos a un tribunal que carezca de competencia funcional para conocer de los mismos. No obstante lo anterior, si admitido un recurso el tribunal al que se haya dirigido entiende que no tiene competencia funcional para conocer del mismo, dictará auto absteniéndose de conocer previa audiencia de las partes personadas por plazo común de diez días. 2. Notificado el auto a que se refiere el apartado anterior, los litigantes dispondrán de un plazo de cinco días para la correcta interposición o anuncio del recurso, que se añadirán al plazo legalmente previsto para dichos trámites. Si sobrepasaren el tiempo resultante sin recurrir en forma, quedará firme la resolución de que se trate».

- Art. 769.2 LECiv: Aplicación por analogía « En el procedimiento de separación o divorcio de mutuo acuerdo a que se refiere el artículo 777, será competente el Juez del último domicilio común, o el del domicilio de cualquiera de los solicitantes».

En consecuencia, la tiene este Tribunal al que me dirijo por ser el del último domicilio común de los convivientes.

Clase de juicio

-El trámite a seguir será el señalado en la ley procesal civil en los artículos 399 y siguientes.

Legitimación activa y pasiva

- Art. 10 LECiv: «Condición de parte procesal legítima. Serán considerados partes legítimas quienes comparezcan y actúen en juicio como titulares de la relación jurídica u objeto litigioso».

B) FUNDAMENTOS DE DERECHO SUSTANTIVO O LEGAL

Constitución Española

- Art. 10 CE: «1. La dignidad de la persona, los derechos inviolables que le son inherentes, el libre desarrollo de la personalidad, el respeto a la ley y a los derechos de los demás son fundamento del orden político y de la paz social.

2. Las normas relativas a los derechos fundamentales y a las libertades que la Constitución reconoce, se interpretarán de conformidad con la Declaración Universal de Derechos humanos y los tratados y acuerdos internacionales sobre las mismas materias ratificados por España».

- Art. 14 CE: «Los españoles son iguales ante la ley, sin que pueda prevalecer discriminación alguna por razón de nacimiento, raza, sexo, religión, opinión o cualquier otra condición o circunstancia personal o social».

- Art. 24 CE: «Todas las personas tienen derecho a obtener la tutela efectiva de los jueces y tribunales en el ejercicio de sus derechos e intereses legítimos, sin que, en ningún caso, pueda producirse indefensión».

- Art. 39 CE: «1. Los poderes públicos aseguran la protección social, económica y jurídica de la familia.

2. Los poderes públicos aseguran, asimismo, la protección integral de los hijos, iguales éstos ante la ley con independencia de su filiación, y de las madres, cualquiera que sea su estado civil. La ley posibilitará la investigación de la paternidad.

3. Los padres deben prestar asistencia de todo orden a los hijos habidos dentro o fuera del matrimonio, durante su minoría de edad y en los demás casos en que legalmente proceda.

4. Los niños gozarán de la protección prevista en los acuerdos internacionales que velan por sus derechos».

Código Civil

En base a la jurisprudencia que se cita en el punto siguiente.

- Art. 90. «El convenio regulador deberá referirse, al menos, a los siguientes extremos:

A) El cuidado de los hijos sujetos a la patria potestad de ambos, el ejercicio de ésta y, en su caso, el régimen de comunicación y estancia de los hijos con el progenitor que no viva habitualmente con ellos.

B) Si se considera necesario, el régimen de visitas y comunicación de los nietos con sus abuelos, teniendo en cuenta, siempre, el interés de aquéllos.

B)bis El destino de los animales de compañía, en caso de que existan, teniendo en cuenta el interés de los miembros de la familia y el bienestar del animal; el reparto de los tiempos de convivencia y cuidado si fuere necesario, así como las cargas asociadas al cuidado del animal.

C) La atribución del uso de la fivienda y ajuar familiar.

D) La contribución a las cargas del matrimonio y alimentos, así como sus bases de actualización y garantías en su caso, E) La liquidación, cuando proceda del régimen económico del matrimonio. F) La pensión que conforme al artículo 97 correspondiere satisfacer, en su caso, a uno de los cónyuges.

- Art. 92 CC: «1. La separación, la nulidad y el divorcio no eximen a los padres de sus obligaciones para con los hijos.

2. El juez, cuando deba adoptar cualquier medida sobre la custodia, el cuidado y la educación de los hijos menores, velará por el cumplimiento de su derecho a ser oídos.

3. En la sentencia se acordará la privación de la patria potestad cuando en el proceso se revele causa para ello.

4. Los padres podrán acordar en el convenio regulador o el Juez podrá decidir, en beneficio de los hijos, que la patria potestad sea ejercida total o parcialmente por uno de los cónyuges».

- Art. 93 CC: «El Juez, en todo caso, determinará la contribución de cada progenitor para satisfacer los alimentos y adoptará las medidas convenientes para asegurar la efectividad y acomodación de las prestaciones a las circunstancias económicas y necesidades de los hijos en cada momento.

Si convivieran en el domicilio familiar hijos mayores de edad o emancipados que carecieran de ingresos propios, el Juez, en la misma resolución, fijará los alimentos que sean debidos conforme a los artículos 142 y siguientes de este Código».

- Art. 96 CC: «En defecto de acuerdo de los cónyuges aprobado por el Juez el uso de la vivienda familiar y de los objetos de uso ordinario en ella corresponden a los hijos y al cónyuge en cuya compañía queden.

Para disponer de la vivienda y bienes indicados cuyo uso corresponda al cónyuge no titular se requerirá el consentimiento de ambas partes o, en su caso, autorización judicial».

- Art. 1255 CC: «Los contratantes pueden establecer los pactos, cláusulas y condiciones que tengan por conveniente, siempre que no sean contrarios a las leyes, a la moral, ni al orden público».

C) Doctrina jurisprudencial

Sentencia del Tribunal Supremo de fecha 18 de mayo de 1992: Las uniones libres aunque están carentes de precisa normativa, no son desconocidas por nuestro ordenamiento jurídico: la Constitución no las prevé, pero tampoco expresamente las prohíbe (art. 32 en relación al 39), que proyecta la protección de la familia en forma genérica, es decir, como núcleo creado tanto por el matrimonio, como por la unión de hecho; y legislativamente: arts. 101, 107, 108 y 320.1 CC; arts. 11 y 18 CP que equipara al cónyuge, la persona que se halla obligada de forma permanente por análoga relación de afectividad; art. 3 de la Ley Orgánica reguladora de procedimiento de Habeas Corpus; legitima para instarlo, no sólo al cónyuge del detenido, sino también aquella persona unida por análoga razón de afectividad; la disp. adic. 10ª Ley de 7 de julio de 1981, en el ámbito de la SS, contempla el percibo de pensiones, así como el derecho a las prestaciones sanitarias que, con carácter excepcional, acordó dispensar la Resolución de la Secretaría General de la Seguridad Social, con apoyo en razones de equidad.

El empleo de la analogía viene impuesto, pues, no obstante tratarse de una operación jurídica muy delicada que exige mesura, ponderación, meditado y cuidado uso (STC de 14 de julio de 1988, rec. 864/1987), ante el problema de anomia que el tema presenta, al no ser el ordenamiento jurídico previsor, la analogía evidentemente es la técnica adecuada ante una realidad social que se presenta dinámica y con profusión en los tiempos actuales y exige respuesta judicial.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL: Que teniendo por presentado este escrito con los documentos que se acompañan y sus copias, se sirva admitirlo y, en su virtud, de conformidad con las manifestaciones que contiene, tenga por comparecido a don/doña [NOMBRE Y APELLIDOS], y en su nombre tener por instada JUICIO ORDINARIO EN SOLICITUD DE HOMOLOGACIÓN DE LOS ACUERDOS DE LA RUPTURA CONVIVENCIAL y previos los trámites legales pertinentes, dicte sentencia que:

1º Declare la ruptura de la unión estable de pareja de hecho constituida entre [NOMBRE Y APELLIDOS] y [NOMBRE Y APELLIDOS] [esta declaración no es necesaria en derecho común, pero útil] y la revocación de los poderes que se hubieren otorgado mutuamente.

2º Acuerde la ratificación de ambos convivientes de la propuesta de acuerdos r suscritos y presentados con la demanda.

3º Se apruebe judicialmente los acuerdos de la ruptura convivencial con las medidas que contienen.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Fdo. Letrado [NOMBRE Y APELLIDOS]

Colegiado núm. [Nº DE COLEGIADO]

Fdo. Procurador/a [NOMBRE Y APELLIDOS]

Colegiado núm. [Nº DE COLEGIADO]

========================================================================
