---
name: demanda-terceria-dominio-sobre-inmueble-aportado-civ-1691
description: "Demanda de tercería de dominio sobre inmueble aportado a una sociedad sin inscribir en el Registro. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de tercería de dominio sobre inmueble aportado a una sociedad sin inscribir en el Registro

> Formulario **CIV-1691** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Demanda de tercería de dominio en relación a un bien inmueble embargado, el cual fue aportado por la actora al capital social de la mercantil contra la que se dictó auto despachando ejecución decretándose el embargo de dicho inmueble.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de tercería de dominio sobre inmueble aportado a una sociedad sin inscribir en el Registro» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de tercería de dominio sobre inmueble aportado a una sociedad sin inscribir en el Registro” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:demanda-terceria-dominio-sobre-inmueble-aportado-civ-1691`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (10 veces)
- [ ] NÚMERO (6 veces)
- [ ] FECHA (5 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] AÑO (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] COLEGIO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DIRECCIÓN
- [ ] FOLIO
- [ ] IMPORTE
- [ ] IMPORTE EN CIFRA
- [ ] LIBRO
- [ ] LUGAR
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] SEDE
- [ ] TOMO

## Normas que cita el formulario

- art. 599 LEC
- art. 85.1 LOPJ
- art. 38 CC
- art. 595 LEC
- art. 600 LEC
- art. 253.1 LEC
- art. 251 LEC
- art. 595.3 LEC
- art. 597 LEC
- art. 596 LEC
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 601 LEC
- art. 603 LEC
- art. 348 CC
- art. 349 CC
- art. 538.3 LEC
- art. 71 LH
- art. 44 LH
- art. 1.923 CC
- art. 598.1 LEC
- art. 604 LEC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, que actúa en nombre y representación de [NOMBRE DEL REPRESENTADO/A], S.L., con domicilio en [LOCALIDAD], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], dirigido por el Letrado/a en ejercicio D./Dña. [NOMBRE Y APELLIDOS], colegiado n.º [NÚMERO] del Iltre. Colegio de Abogados de [COLEGIO], y despacho abierto en [LOCALIDAD], ante el Tribunal comparezco en autos de Ejecución de título judicial n.º [NÚMERO]/[AÑO], y como mejor en Derecho proceda, DIGO:

Que siguiendo instrucciones de mi mandante formulo demanda de tercería de dominio frente a D./Dña. [NOMBRE Y APELLIDOS], parte ejecutante en el proceso antes referido, que postula representado por el Procurador/a D./Dña. [NOMBRE Y APELLIDOS], siendo ejecutados D./Dña. [NOMBRE Y APELLIDOS], y otros, fundándola en los siguientes

HECHOS

PRIMERO.- Esta parte ha tenido conocimiento de que en la presente ejecución, por ese Tribunal al que me dirijo ha sido dictada diligencia de ordenación de [FECHA], por la que se acuerda sacar a pública subasta el inmueble que es finca urbana n.º [NÚMERO], inscrita al folio [FOLIO], del tomo [TOMO], libro [LIBRO] de [LOCALIDAD], en el Registro de la Propiedad n.º [NÚMERO] de

SEGUNDO.- Dicho procedimiento de apremio nace de que con fecha [FECHA], se dictó auto despachando ejecución frente a D./Dña. [NOMBRE Y APELLIDOS], y otros, como consecuencia de sentencia firme recaída en juicio verbal de oposición en juicio cambiario n.º [NÚMERO]/[AÑO], acordándose mediante decreto el embargo del bien que se saca a subasta.

TERCERO.- El expresado inmueble, que se halla en el Paseo de [DIRECCIÓN], n.º [NÚMERO] de [LOCALIDAD], es propiedad de mi representada [NOMBRE DEL REPRESENTADO/A], S.L., puesto que fue aportada por D./Dña. [NOMBRE Y APELLIDOS] en la constitución de dicha mercantil, mediante escritura pública de [FECHA], y que se inscribió en el Registro Mercantil de [LOCALIDAD], el

Se acompaña copia auténtica de la mencionada escritura pública de constitución como documento número [Nº DE DOCUMENTO].

CUARTO.- El embargo acordado por ese Tribunal a través de decreto de fecha [FECHA], se hizo para cubrir una deuda de D./Dña. [NOMBRE Y APELLIDOS] y de los otros codemandados en el juicio cambiario, y condenados solidariamente, que es ajena a la responsabilidad patrimonial de la S.L. mandante.

QUINTO.- El citado inmueble pertenecía a mi patrocinada con mucha anterioridad al citado embargo anotado en autos.

SEXTO.- Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

A los anteriores hechos son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA.

Corresponde el conocimiento de la presente demanda al Tribunal, conforme a lo dispuesto en el art. 599 LEC en relación con lo dispuesto en el art. 85.1º LOPJ, ya que la tercería de dominio ha de interponerse ante el tribunal que conozca de la ejecución, con lo cual se resuelve en una regla la competencia genérica, y específica objetiva, funcional y territorial.

II.- CAPACIDAD.

La entidad demandante es una sociedad mercantil, que goza de personalidad independiente y plena capacidad, tanto para ser parte como capacidad procesal, que se deriva de su regular constitución en escritura pública inscrita en el Registro Mercantil, compareciendo por medio del legal representante, administrador social único, con arreglo a los arts. 6.1.3.º y 7.4 LEC, en relación con los arts. 38 CCiv, y 20 y 33 LSC.

El demandado es persona física mayor de edad, con pleno ejercicio de derechos civiles, parte en la ejecución (arts. 6.1.1º, 7.1, y 538.1 LEC).

III.- LEGITIMACIÓN.

Puede interponer tercería de dominio, en forma de demanda, quien, sin ser parte en la ejecución, afirma ser dueño de un bien embargado como perteneciente al ejecutado y que no ha adquirido de éste una vez trabado el embargo (art. 595 LEC), por lo que mi representada está legitimada activamente por ser la propietaria del bien embargado y ser tercero en el proceso de ejecución del que dimana la traba.

La demanda de tercería se debe interponer frente al acreedor ejecutante y también frente al ejecutado cuando el bien al que se refiera haya sido por él designado (art. 600 LEC). No constando en autos que el inmueble embargado haya sido designado por D./Dña. [NOMBRE Y APELLIDOS], en el presente caso se ha demandado al ejecutante y no al ejecutado, sin perjuicio de la intervención procesal que le autoriza el precitado precepto.

IV.- POSTULACIÓN.

En cuanto a la postulación es preceptiva en el presente proceso la intervención de Abogado habilitado para ejercer su profesión en el tribunal que conozca del asunto, y Procurador igualmente habilitado para actuar en el tribunal que conozca del juicio (arts. 23.1, 31.1 y 539.1 párrafo 1.º LEC), acompañándose a este escrito la escritura de apoderamiento para pleitos y la identificación de los dichos profesionales.

V.- PROCEDIMIENTO.

El presente proceso habrá de sustanciarse por los trámites del juicio verbal, de acuerdo con lo que establece el art. 599 LEC, formándose pieza separada de la ejecución.

VI.- CUANTÍA.

Cumpliendo con el deber de fijación en la demanda del interés económico litigioso del art. 253.1 LEC, se manifiesta que la cuantía del juicio asciende a [IMPORTE] euros ([IMPORTE EN CIFRA] €), que se corresponde con el valor catastral de la finca consignado en el recibo del impuesto sobre bienes inmuebles del pasado ejercicio, y que se adjunta como documento número 2, siendo las reglas cuantificadoras las 2.ª y 3.ª del art. 251 LEC.

VII.- PRESUPUESTOS DE ADMISIÓN

Justificación. El art. 595.3 LEC exige que con la demanda de tercería de dominio se aporte un principio de prueba por escrito del fundamento de la pretensión del tercerista, como así se hace con la escritura de constitución de [DENOMINACIÓN SOCIAL], S.L. anexa.

La demandante no ha interpuesto tercería anterior sobre el mismo bien (art. 597 LEC).

Tiempo. Esta tercería de dominio se interpone tempestivamente, puesto que cupiendo desde que se haya embargado el bien a que se refiera, aunque el embargo sea preventivo, no se deduce con posterioridad al momento en que, de acuerdo con lo dispuesto en la legislación civil, se producirá la transmisión del bien al acreedor o al tercero que lo adquiera en pública subasta, que todavía no se ha celebrado, tal y como determina el art. 596 LEC.

VIII.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

IX.- FUNDAMENTO MATERIAL

Título de dominio. El objeto de la tercería de dominio es la pretensión del tercerista de que se alce el embargo del bien objeto de tercería (art. 601 LEC). El tribunal se pronunciará sobre la pertenencia del bien y la procedencia de su embargo a los únicos efectos de la ejecución en curso, sin que produzca efectos de cosa juzgada en relación con la titularidad del bien (art. 603 LEC).

Tal es doctrina ya consolidada [Sentencia del Tribunal Supremo, Sala Primera, de lo Civil, de 22 Jul. 1985, 2 de noviembre de 1987, Sentencia del Tribunal Supremo, Sala Primera, de lo Civil, de 8 Feb. 1991, Sentencia Tribunal Supremo, Sala Primera, de lo Civil, de 8 Feb. 1991, 24 de julio de 1992 y 2 de junio de 1994].

La pretensión ha de ser fundada en la titularidad del derecho de propiedad, u otro que, por disposición legal expresa, autorice a oponerse al embargo, o a la realización forzosa de un bien, como de pertenencia al ejecutado.

En el supuesto de esta demanda, se alega y prueba la propiedad del inmueble embargado por mi mandante, a través de negocio de aportación al capital social de la mercantil, que no puede desconocerse por el procedimiento de apremio, ya que es tal el derecho a gozar y disponer de una cosa sin más limitaciones que las establecidas en las leyes (art. 348 CCiv), y nadie puede ser privado de su propiedad, sino por autoridad competente y por causa justificada de utilidad pública, previa siempre la correspondiente indemnización, bajo amparo de los jueces (art. 349 CCiv).

Lo que debe probar como hechos constitutivos el demandante es la propiedad del bien embargado, la identidad con el trabado, y que el embargo se ha llevado a cabo para cubrir deudas ajenas.

Junto con el dominio del bien, y su identidad física y registral, se prueba que el embargo se hizo por deudas ajenas a la S.L., la que no figura como deudora en el título ejecutivo, de tal manera que no tampoco resulta de aplicación la extensión ejecutiva a tercero frente al que no se despacha la ejecución, que se contempla en el art. 538.3 LEC, y que procedería de una afectación de bienes ajenos a la obligación que se ejecuta.

Oponibilidad de la adquisición frente a la anotación preventiva de embargo.

Aunque la idea de que la anotación preventiva de embargo, sucesora de la hipoteca judicial, cerraba el Registro de la Propiedad a los actos de disposición o gravamen de la finca en que provisionalmente se publicaba el embargo, fue la auspiciada por el primer sistema hipotecario, en línea con la tradición —así lo resalta la alabada Exposición de Motivos de la Ley de 1861—, la jurisprudencia, primero, la configuración de la acción rescisoria por fraude pauliano en el CCiv, después, y la misma doctrina hipotecaria de fin del siglo XIX, al final, condujeron a reputar pacífica la interpretación del art. 71 LH, según la cual, si toda anotación preventiva permite la transmisión del bien sobre el que se practicó, pero "sin perjuicio del derecho de la persona a cuyo favor se haya hecho la anotación’, lo mismo cabe afirmar de la anotación que publican el embargo, siendo el derecho del anotante que se salva, por de pronto, el configurado en el art. 44 LH, y que es, explícitamente, una preferencia crediticia.

Preferencia crediticia que se concreta, por remisión, en el contenido del art. 1.923 CCiv, que en su ordinal 4º, clasifica entre los privilegios especiales inmobiliarios, uno, de fundamento formalista, que se gana con la anotación preventiva en el Registro de la Propiedad, matizando que procederá de venir de mandamiento de judicial de embargo, secuestro o ejecución de sentencia, y ‘ sólo en cuanto a créditos posteriores’.

Sabido es que la prenda o hipoteca judicial fue aborrecida por el movimiento liberal, y que los autores de la LH 1861, la describieron, al rebautizarla como anotación preventiva y restringirla, a modo de mero aseguramiento de los derechos reconocidos en sede judicial, a través de vedar la enajenación o gravamen de las cosas afectadas y la eventualidad de constitución del deudor en insolvencia, de forma que el protosistema hipotecario se quiso circunscribir a afirmar la publicidad de la propiedad y derechos reales en el campo inmobiliario, dejando en segundo plano la resolución de los conflictos prelativos y la configuración del crédito mediante la publicidad de los procesos de ejecución.

La jurisprudencia, desde un principio, se ha aplicado a negar eficacia ofensiva a la anotación preventiva de embargo, que sólo se admite otorga rango preferente sobre los actos dispositivos celebrados, y sobre los créditos contraídos con posterioridad a la fecha de la propia anotación, y no en cuanto a los actos de disposición ni tampoco sobre los créditos anteriores que tienen una preferencia sobre el anotado.

Huelga la cita de sentencias de la Sala I TS —y doctrina antigua de la DGRN: resoluciones de 16 de octubre y 13 de diciembre de 1974, 17 de diciembre de 1975, 5 de marzo de 1982 ó 12 de septiembre de 1983— que han sido machaconamente desfavorables a cualquier tipo de eficacia real de las anotaciones de embargo, y sobre la base de que otorgándose publicidad de un temporal poder directo e inmediato ‘erga omnes’ sobre bienes inscritos semejante al del derecho real, no se transforma en derecho real el crédito ejecutivo que garantizan, han auspiciado siempre la prelación por orden de antigüedad extrarregistral de los derechos.

A pesar de que se admite la existencia de una crítica de juristas con talla, que no es reciente, a propósito de la exigencia de un efecto real para la anotación preventiva de embargo, con el sentido de que se aplique una prelación por antigüedad registral en la concurrencia de situaciones crediticias o reales asentadas, no conoce eco jurisprudencial, ya que la jurisprudencia se mantiene en la tesis clásica acerca de la restricción de la preferencia por rango registral de la anotación de embargo al régimen de prelación de ‘prioridad civil’.

Suspensión.

De conformidad con el art. 598.1 LEC, procede acordar la suspensión del proceso de ejecución con respecto al bien inmueble que es propiedad de mi mandante, sin que se calibre razón para que se preste caución, al constar por certificación registral que la finca fue adquirida con anterioridad al embargo, y está inscrita, constando en todo caso la anotación preventiva en el folio real. El retardo que podría darse, si insospechadamente no se alzara el embargo, en sacar a subasta el inmueble, ya tiene su reparación con el devengo de intereses legales, y el valor de la finca supera con creces la deuda ejecutiva que se persigue.

Pronunciamientos.

Se pide, con arreglo al art. 604 LEC, que se alce el embargo, y la cancelación de la anotación preventiva en el Registro de la Propiedad, que se practicó para el aseguramiento de aquél.

X.- COSTAS PROCESALES.

Las costas de este proceso deberán ser impuestas al demandado, de conformidad con lo establecido en el art. 603 párrafo 2.º LEC, en relación con los arts. 394 y ss. LEC.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por interpuesta la presente demanda, junto con los documentos que se acompañan, se digne admitir uno y otras, teniéndome por comparecida y parte en la representación que ostento, entendiéndose conmigo las sucesivas actuaciones, y por formulada demanda de tercería de dominio contra D./Dña. [NOMBRE Y APELLIDOS], ejecutante en el proceso, y con suspensión de la ejecución respecto del bien a que se refiere la demanda hasta que se resuelva la tercería, y seguidos que sean los trámites legales de procedimiento, se dicte auto por el que, previa declaración de pertenencia a mi representada del inmueble objeto de esta demanda, se acuerde el alzamiento del embargo, así como la cancelación de la anotación preventiva del embargo practicada en el Registro de la Propiedad, con expresa imposición de las costas al demandado

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
