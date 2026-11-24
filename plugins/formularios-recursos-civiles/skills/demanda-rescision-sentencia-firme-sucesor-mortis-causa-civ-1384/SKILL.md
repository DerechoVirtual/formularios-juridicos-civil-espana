---
name: demanda-rescision-sentencia-firme-sucesor-mortis-causa-civ-1384
description: "Demanda de rescisión de sentencia firme por el sucesor mortis causa del rebelde, con edictos. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de rescisión de sentencia firme por el sucesor mortis causa del rebelde, con edictos

> Formulario **CIV-1384** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 24-11-2026.

## Qué es

Modelo de demanda de juicio de rescisión de sentencia firme dictada en rebeldía por la causa 3ª del art. 501 LEC, por el sucesor del condenado rebelde.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de rescisión de sentencia firme por el sucesor mortis causa del rebelde, con edictos» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de rescisión de sentencia firme por el sucesor mortis causa del rebelde, con edictos” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:demanda-rescision-sentencia-firme-sucesor-mortis-causa-civ-1384`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (17 veces)
- [ ] NOMBRE Y APELLIDOS (17 veces)
- [ ] AÑO (11 veces)
- [ ] FECHA (9 veces)
- [ ] MES (8 veces)
- [ ] DÍA (6 veces)
- [ ] NÚMERO (6 veces)
- [ ] CITA JURISPRUDENCIAL (2 veces)
- [ ] LUGAR (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] AÑOS
- [ ] CALLE
- [ ] COLEGIO
- [ ] DESCRIPCIÓN DE LOS BIENES
- [ ] DOMICILIO
- [ ] FOLIO
- [ ] IMPORTE
- [ ] NOMBRE DE LA VÍA
- [ ] NOMBRE DEL NOTARIO
- [ ] Nº DE APARTADO
- [ ] Nº DE PROCEDIMIENTO
- [ ] PROVINCIA
- [ ] SEDE
- [ ] TOMO
- [ ] TÉRMINO MUNICIPAL
- [ ] ÓRGANO

## Normas que cita el formulario

- art. 501 LEC
- art. 9.2 LOPJ
- art. 504.2 LEC
- art. 253.1 LEC
- art. 251 LEC
- art. 502.1.2.º LEC
- art. 503 LEC
- art. 777 LEC
- art. 501.3.º LEC
- art. 506.2 LEC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…rador/a ========================================================================»: requisito de procedibilidad del art. 5 LO 1/2025 — antes de presentar la demanda hay que intentar un medio adecuado de solución de controversias (MASC) y acreditarlo con la demanda (arts. 264.4.º y 399.3 LEC), salvo las materias excluidas del art. 5.2. Fuente: LO 1/2025, arts. 5 a 7 (BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

Don/Doña [NOMBRE Y APELLIDOS], Procurador de los Tribunales, que actúa en nombre y representación de Don [NOMBRE Y APELLIDOS], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], a quien asiste el Letrado en ejercicio Don/Doña [NOMBRE Y APELLIDOS], colegiado n.º [NÚMERO] del Iltre. Colegio de Abogados de [COLEGIO], con despacho abierto en esta localidad, calle [CALLE] de [LOCALIDAD], ante el Tribunal comparezco y como mejor proceda en Derecho DIGO:

Que, en la representación que ostento, vengo a interponer demanda de juicio de rescisión de la sentencia firme dictada elen autos de Juicio Ordinario n.º [Nº DE PROCEDIMIENTO]/[AÑO], frente a Don/D.ª [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD],

Se ejercita en la presente demanda la acción de rescisión de sentencias firmes dictadas en rebeldía por causa 3.ª del art. 501 LEC.

Fundamento la misma en los siguientes hechos y consideraciones jurídicas:

HECHOS

PRIMERO

Mi representado es único hijo de Don/Doña [NOMBRE Y APELLIDOS], que falleció en [LOCALIDAD], el [FECHA], y su sucesor como heredero universal, según acredito mediante certificado de defunción expedido por el Registro Civil de [LOCALIDAD], que acompaño como documento n.º 1, certificado del Registro Central de Actos de Última Voluntad (documento n.º 2), y copia auténtica del testamento otorgado ante el Notario de [LOCALIDAD], Don [NOMBRE DEL NOTARIO], el [DÍA] de [MES] de [AÑO], n.º [NÚMERO] de su protocolo general corriente (documento n.º 3).

SEGUNDO

El finado Don/Doña [NOMBRE Y APELLIDOS] era natural y fue vecino de esta población, hasta el año [AÑO], donde tenía varias propiedades, y al volver mi mandante en recientes fechas a este pueblo de sus mayores, a fin de resolver gestiones de su herencia, ha sido enterado de que existió proceso ante el Tribunal al que honro en dirigirme, por el que se dictó sentencia que condenaba al difunto, y que éste ignoraba, a entregar a la demandada Don/D.ª [NOMBRE Y APELLIDOS], los siguientes montes maderables:, y [DESCRIPCIÓN DE LOS BIENES], en el término de [TÉRMINO MUNICIPAL] (son pertenecidos de la finca registral n.º [NÚMERO], al folio [FOLIO], tomo [TOMO], del libro de [LOCALIDAD], Registro de la Propiedad de [LOCALIDAD]).

Se acompaña como documento n.º 4, copia testimoniada de la sentencia, de fecha [FECHA]

TERCERO

El proceso de donde surge la sentencia fue Juicio Ordinario n.º [NÚMERO]/[AÑO], en que fue demandante Don/D.ª [NOMBRE Y APELLIDOS], siendo demandado mi causante Don/Doña [NOMBRE Y APELLIDOS], que fue intentado emplazar en domicilio de Vía [NOMBRE DE LA VÍA], n.º [NÚMERO], como se indicaba en la demanda, y se efectuó en dicho piso que el finado tenía en esta población, una diligencia fallida de emplazamiento, ya que, al cumplimentar el trámite, el agente se encontró con que, según informaciones de la portera del inmueble, "el Sr/Sra [NOMBRE Y APELLIDOS] ya no vivía en dicho domicilio, sino en [LOCALIDAD], pero desconocía la dirección, por lo que concluye el agente, no se ha podido llevar a cabo dicho emplazamiento"; el [DÍA] de [MES] del mismo año, en diligencia de ordenación, se manda sacar fotocopia del frustrado emplazamiento, dándole traslado a la actora para que a la vista del mismo inste lo que a su derecho convenga, por diligencia de ordenación que se notifica a la demandante el [ÓRGANO], ante lo cual, la parte demandada, sin más prefirió la cómoda y contraria a Derecho solución de solicitar que se le emplazase por vía edictal, y sin más averiguaciones, se emplazó por edictos colocados en el tablón de anuncios de la Oficina Judicial y publicados en el Boletín Oficial de [PROVINCIA], siendo declarado el demandado en rebeldía procesal en diligencia de ordenación de [FECHA] de [MES] de

Por el mismo conducto edictal fue notificada la sentencia condenatoria, que apareció en el predicho Boletín el día [DÍA] de [MES] de [AÑO]

Se adjunta testimonio de particulares del indicado juicio, como documento n.º 5.

CUARTO

El causante de mi patrocinado estuvo domiciliado en [DOMICILIO], desde el mes de [MES] del año [AÑO], según se ha dicho, e ininterrumpidamente.

Se aporta certificado del Padrón Municipal del Ayuntamiento de [LOCALIDAD] -documento n.º 6- que acredita que Don/Doña [NOMBRE Y APELLIDOS] causó alta en dicho padrón, es decir, fue inscrito como domiciliado en dicha ciudad el [FECHA], permaneciendo en esta situación hasta el [DÍA] de [MES] de [AÑO], en que causó baja por fallecimiento.

Igualmente se aporta certificado de la Compañía Telefónica de [LOCALIDAD], conforme al que Don [NOMBRE Y APELLIDOS], tuvo designado su teléfono en [LOCALIDAD], durante los años [AÑOS], constando en todos ellos en los sucesivos ‘listines’ (documento n.º 7).

QUINTO

Teniendo en cuenta, pues, que la demanda del Juicio Ordinario n.º [NÚMERO]/[AÑO] se presentó el [FECHA], resulta evidente, pues, que en esa fecha, no estaba domiciliado D [NOMBRE Y APELLIDOS] en el lugar donde se le emplazó, y teniendo su domicilio en [LOCALIDAD], de forma fehaciente, se le emplazó por edictos, como si se tratase de una persona de domicilio desconocido e incierto, lo cual es contrario a derecho, siendo continua su situación de rebeldía injusta.

A los anteriores hechos, son aplicables los siguientes

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA

A) JURISDICCIÓN

La potestad jurisdiccional se ejerce por los Jueces y Tribunales determinados por las leyes, según las normas de competencia y procedimiento que las mismas establezcan (art. 117.3 CE), siendo los tribunales del orden civil los que conocen, además de las materias que les son propias, de todas aquellas que no estén atribuidas a otro orden jurisdiccional (art. 9.2 LOPJ), no existiendo en el presente asunto, por su carácter procesal e instrumental de cara a conseguir un juicio rescisorio, de posibilidad de elemento ninguno de extranjería, o sujeción a arbitraje.

B) COMPETENCIA

En una sola regla de competencia funcional, contenida en el art. 501, párrafo 1.º LEC, se resuelve toda competencia específica, ya que la rescisión de la sentencia firme dictada en rebeldía debe pretenderse ante el tribunal que la hubiere dictado, ante el que tengo el honor de dirigirme.

II.- PROCEDIMIENTO

Conforme al art. 504.2 LEC el procedimiento se sustanciará por los trámites establecidos para el juicio ordinario, regulado en los arts. 399 a 436 de la misma Ley.

III.- CAPACIDAD Y REPRESENTACIÓN

Mi mandante es mayor de edad, en pleno disfrute de sus derechos civiles, por lo que detentan capacidad para ser parte por sí, y capacidad procesal, o para comparecer en juicio, siendo también mayor de edad las demandada, respecto de las que se ignora exista limitación alguna de capacidad (arts. 6.1.1.º y 7.1 LEC).

IV.- LEGITIMACIÓN

Corresponde al demandante la legitimación activa ordinaria derivada, por sucesión ‘mortis causa’, ya que es heredero universal testamentario de Don/Doña [NOMBRE Y APELLIDOS], por afirmarse titular, por sucesión hereditaria, del objeto litigioso en posición pasiva en el proceso cuya sentencia se pretende rescindir, y por lo tanto, sucesor procesal del demandado que ha permanecido constatemente en rebeldía en dicho proceso (art. 501, párrafo 1.º LEC), y tiene acción para reclamar la tutela judicial rescindente, y la legitimación pasiva corresponde a la demandada porque fue la demandante en el proceso previo.

V.- POSTULACIÓN Y DEFENSA

Conforme a lo previsto en los arts. 23.1 y 31.1 LEC, se presenta la demanda por medio de Procurador de los Tribunales con poder general para pleitos, legalmente habilitado ante el Tribunal, y bajo dirección de Letrado en ejercicio colegiado, cuyo nombre y apellido se consignan, que redacta y firma la misma.

VI.- CUANTÍA

Debe entenderse que la cuantía de la demanda, que ha de determinarse conforme al art. 253.1 LEC, se corresponde con la de la que dio lugar al juicio cuya sentencia firme se pretende rescindir, dado que ésta responde a una primera fase, rescindente, cuyo objeto es dar paso a otra segunda, rescisoria, en que se vuelva replantear el objeto de cara a la resolución definitiva del mismo asunto. Y la cuantía del proceso cuya sentencia se ataca ascendía según la documentación valorativa de los predios reivindicados, con arreglo a la regla 2.ª del art. 251 LEC, en base a la demanda inicial, al importe de [IMPORTE] euros.

VII.- REQUISITO DE ADMISIBILIDAD

Se acompaña a este escrito resguardo acreditativo del pago del depósito que exige la disposición adicional 15.ª LOPJ.

VIII.- CUESTIÓN DE FONDO

PRESUPUESTOS

Temporales. La demanda se presenta dentro de los cuatro meses contados a partir de la publicación de la sentencia firme, que nunca se notificó personalmente (art. 502.1.2.º LEC).

Causales. La sentencia firme recaída tiene efectos de cosa juzgada material, al resolver una acción reivindicatoria en juicio ordinario, siempre plenario (art. 503 LEC).

CAUSA LEGAL DE RESCISIÓN

Se invoca como causa legal la del n.º 3 del art. 501 LEC, por haber sido desconocedor el causante del actor de la demanda y el pleito, cuando fue demandado rebelde, emplazado por edictos, mientras que estuvo ausente del lugar en que se siguió el proceso, la ciudad de [LOCALIDAD], así como de cualquier otro lugar de la Comunidad Autónoma de [LOCALIDAD], en cuyo Boletín Oficial se hubiesen publicado aquéllos.

La doctrina constitucional tiene establecido que el derecho a la defensa y a la bilateralidad que, como fundamental consagra el art. 24.1 CE, contiene un mandato dirigido al legislador y al intérprete, en el sentido de promover la contradicción, resultando conculcado cuando los titulares de derechos e intereses legítimos se ven imposibilitados de hacer uso de los medios legales necesarios para su defensa, correspondiendo en estos casos al órgano judicial suplir, mediante una interpretación posible y favorable al ejercicio de la acción impugnativa, el imperfecto, y muchas veces erróneo, cumplimiento de los requisitos formales impuestos por la ley procesal, asegurando así la primacía del mencionado derecho fundamental (SSTC de 20 de junio de 1986, rec. 121/1985 y 10 de diciembre de 1986, rec.591/1985).

La LEC trata con criterio diferenciado las rebeldías del demandado procedentes de situaciones de domicilio desconocido, en las que el emplazamiento se ha efectuado mediante edictos (art. 501.3.º), y aquellas otras procedentes de notificaciones personales y por cédula (art. 501.2.º), no exigiendo en las primeras la justificación de inimputabilidad, es decir, abstrayendo el obstáculo que les hubiera impedido comparecer, presumiendo "iuris tantum" que ignoraban la existencia del procedimiento, y creando en definitiva una "rebeldía ficta", con la sola prueba de la ausencia constante del lugar en el que se siguió el juicio, y de los lugares de los Boletines Oficiales donde se publicaron los edictos; o dicho de otro modo, habrá lugar a la audiencia con la sola acreditación del hecho en sí, prescindiendo de la voluntariedad o involuntariedad del mismo; y todo ello sin perjuicio de no privar a la parte contraria de la posible justificación de una conducta que lo contradiga [STS de 5 de junio de 1990].

Por su parte, la STS de 10 de diciembre de 1990, refiriéndose al art. 777 de la LECiv 1881, semejante al art. 501.3.º LEC, establece que "lo que tal precepto considera no es la estancia esporádica temporal del ausente en el pueblo en que se ha seguido el juicio, sino que hubiere estado en él durante el período de tiempo comprendido desde que fue emplazado hasta la publicación de la sentencia [CITA JURISPRUDENCIAL] " y " [CITA JURISPRUDENCIAL] bajo otro aspecto, porque esa estancia temporal esporádica tampoco pone de manifiesto que lo estuvier a precisamente al tiempo de publicarse los edictos de emplazamiento, a que se alude en la circunstancia tercera del precitado art. 777 [Nº DE APARTADO] ".

Aplicando la anterior doctrina al caso que nos ocupa, resulta que, si la interpretación ha de ser favorable al principio de defensa y bilateralidad y el estar constantemente fuera del pueblo en que se ha seguido el juicio desde el emplazamiento por edictos hasta la publicación de la sentencia, ha de apreciarse la causa invocada, ya que es un hecho indiscutible que Don/Doña [NOMBRE Y APELLIDOS], tenía el año [AÑO], su domicilio en [LOCALIDAD], tal y como aparece en el documento [Nº DE DOCUMENTO],es decir, se demuestra como domiciliado en esa ciudad desde [FECHA], permaneciendo en esta situación hasta el [FECHA], en que causó baja por fallecimiento, por lo que, en consecuenci,a habiéndose presentado la demanda el [DÍA] de [MES] de [AÑO], resulta evidente, pues, y por las circunstancias que han quedado anteriormente expuestas, no pudo ser emplazado en su real domicilio, sino que, lo fue, en donde originariamente tenía en [LOCALIDAD], y además, según diligencia de [FECHA], se manifestó por la portera del inmueble, que ya no vivía allí, desconociéndose el domicilio en [LOCALIDAD], al practicar la diligencia de emplazamiento, por lo que la parte demandada, fue la que, sin más, instó el procedimiento por vía edictal.

IX.- COSTAS

Conforme al art. 506.2 LEC las costas habrán de imponerse a la demandada, puesto que se tendrá que dictar sentencia que estime procedente la rescisión, y ante la evidencia de la pretensión de esta parte, resistirla equivale a temeraridad procesal.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que, habiendo por presentado este escrito de demanda con los documentos que lo acompañan y copias de uno y otros, los admita y me tenga por comparecido y parte en la representación que ostento, y por promovido juicio ordinario en rescisión de sentencia firme por el sucesor del condenado rebelde, se sirva darle el curso señalado en la ley y, en su día, venga a dictar sentencia en la que, estimando íntegramente la demanda, declare haber lugar a oir a Don [NOMBRE Y APELLIDOS], a fin de exponga y pida lo que a su derecho convenga en la forma prevenida para la contestación de la demanda, con lo demás que entonces proceda, todo ello con imposición de las costas del juicio a la parte demandada, D.ª/Doña [NOMBRE Y APELLIDOS], si se opusiera a la demanda, por su temeridad.

Es de Justicia que pido en [LUGAR], a [DÍA] de [MES] de [AÑO].

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a

========================================================================
