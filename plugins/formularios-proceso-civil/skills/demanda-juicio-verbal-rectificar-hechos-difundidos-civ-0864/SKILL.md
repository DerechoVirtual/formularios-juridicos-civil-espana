---
name: demanda-juicio-verbal-rectificar-hechos-difundidos-civ-0864
description: "Demanda de juicio verbal para rectificar hechos difundidos en un medio de comunicación. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio verbal para rectificar hechos difundidos en un medio de comunicación

> Formulario **CIV-0864** del plugin **Proceso civil: demandas, contestaciones, prueba y vista** (`formularios-proceso-civil`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 24-11-2026.

## Qué es

Demanda al Tribunal de Instancia en reclamación de rectificación por la afirmación, en una tertulia radiofónica, de que la sociedad demandante, empresa de derivados de hígado de ñandú, después de haberse lucrado de la subvención, había sido absorbida por una sociedad francesa, llegándose a expresar el precio abonado a los accionistas y formular diversas valoraciones.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio verbal para rectificar hechos difundidos en un medio de comunicación» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio verbal para rectificar hechos difundidos en un medio de comunicación” para mi caso». También puedes invocarla directamente con `/formularios-proceso-civil:demanda-juicio-verbal-rectificar-hechos-difundidos-civ-0864`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-proceso-civil:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso civil: demandas, contestaciones, prueba y vista) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] FECHA (5 veces)
- [ ] DENOMINACIÓN SOCIAL (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] NOMBRE DE LA CADENA (3 veces)
- [ ] NOMBRE DEL PROGRAMA (3 veces)
- [ ] Nº (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] LUGAR
- [ ] MES Y AÑO
- [ ] NOMBRE DE LA PARTE
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] SEDE

## Normas que cita el formulario

- art. 85.1 LOPJ
- art. 51.1 LEC
- art. 250.1.9.º LEC
- art. 217.2 LEC
- art. 217.7 LEC
- art. 394.3 LEC
- art. 437.1 LEC

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

D./Dña. [NOMBRE Y APELLIDOS] Procuradora de los Tribunales, que actúa en nombre y representación de la mercantil [NOMBRE DEL REPRESENTADO/A], domiciliada en [DOMICILIO], conforme acredito mediante la escritura de poder inscrito en el Registro Electrónico de Apoderamientos Judiciales, a cuya justificación aporto certificación de dicho Registro como documento nº [Nº DE DOCUMENTO], a quien asiste el Letrado en ejercicio abajo firmante D./Dña. [NOMBRE Y APELLIDOS], con despacho profesional en [LOCALIDAD], ante ese Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que por medio del presente escrito vengo a formular DEMANDA DE JUICIO VERBAL ESPECIAL EN RECLAMACIÓN DE RECTIFICACIÓN DE HECHOS INEXACTOS Y PERJUDICIALES frente a D./Dña. [NOMBRE Y APELLIDOS], director de la cadena [NOMBRE DE LA CADENA], domiciliada en [DOMICILIO] de [LOCALIDAD],con base en los siguientes:

HECHOS

PRIMERO.- Que sobre las [Nº] horas del día [FECHA], de [MES Y AÑO], en la tertulia radiofónica que se denomina [NOMBRE DEL PROGRAMA], y que emite la cadena [NOMBRE DE LA CADENA], propiedad de la mercantil [DENOMINACIÓN SOCIAL], y dirigida por D./Dña. [NOMBRE Y APELLIDOS], se difundió repetidamente, siendo manifestaciones del dicho director y de los otros tres que hablaban, la noticia de que mi principal, que es la primera empresa que ha procedido a producir y comercializar en España derivados de hígado de ñandú, y específicamente ‘foie’ entero y pernil curado, después de haber lucrado subvención de la Consejería de Industria de la Comunidad Autónoma de [LOCALIDAD], a cargo de los fondos del programa de promoción y desarrollo de zonas clasificadas en lista II de la Directiva comunitaria [Nº] /CEE, había sido absorbida por la sociedad francesa [DENOMINACIÓN SOCIAL], llegándose a expresar el precio abonado a los accionistas y formular diversas valoraciones, lo que es algo radicalmente incierto y cuya divulgación causado perjuicio evidente a los intereses que patrocino.

Se aporta cinta magnetofónica como medio de prueba instrumental, con transcripción escrita, doc. n.º [NÚMERO].

SEGUNDO.- Al quinto día siguiente a la emisión radiofónica, por conducto del Notario de [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS], se dirigió requerimiento al director de la cadena D./Dña. [NOMBRE Y APELLIDOS], a fin de que difundiera la rectificación del tenor que se consignaba, sin que en la diligencia entendida con el apoderado de la empresa que estuvo presente se formulara respuesta. A su demostración se adjunta copia del acta notarial en que aparecen los términos de la rectificación solicitada, doc. n.º [NÚMERO].

TERCERO.- Por el director de la entidad demandada, D./Dña. [NOMBRE Y APELLIDOS], se envió a esta parte misiva, recibida con fecha [FECHA], en que se anunciaba la rectificación en el mismo espacio de la tertulia [NOMBRE DEL PROGRAMA], para el día [FECHA] Se adjunta la carta original, doc. n.º [Nº DE DOCUMENTO]

CUARTO.- El día [FECHA], indicado en la comunicación de la demandada, mentándose en el espacio radiofónico la cuestión, en absoluto se respetó, no ya la integridad de la rectificación solicitada, sino que se desvirtuó nuevamente el dato.

Se acompaña cinta magnetofónica como medio de prueba instrumental, con transcripción escrita, doc. n.º [NÚMERO].

QUINTO.- La información difundida es falsa, tanto en cuanto a la absorción de la sociedad que represento, como en cuanto a que se haya lucrado subvención de ningún tipo, por lo que se deduce esta demanda, ya que aunque se ha notificado que la rectificación se produciría, no se ha producido y se ha insistido en divulgar el dato inveraz.

FUNDAMENTOS DE DERECHO

I.- Es competente el Tribunal a que me dirijo puesto que en esa localidad tiene domicilio social la sociedad propietaria del medio y radica la dirección (art. 4 LO 2/84 de 26 de marzo, reguladora del derecho de rectificación, en relación con el art. 85.1º LOPJ), lo que es cohoneste con el principio del art. 51.1 LEC

II.- El proceso adecuado es el juicio verbal por razón de la materia, conforme al art. 250.1.9.º LEC, por lo que corresponde el trámite de arts. 437 y ss. LEC con las especialidades contempladas en los arts. 5, 6, 7 y 8 de LO 2/84.

III.- Tiene legitimación mi mandante como persona jurídica que afirma que en el medio de comunicación social que explota la demandada se han difundido hechos que le aluden y que considera inexactos, y cuya divulgación puede causarle perjuicio, ejercitándose la acción del art. 1 LO 2/84 por el representante legal de [NOMBRE DE LA PARTE], contra el director de la cadena [NOMBRE DE LA CADENA], de la entidad [DENOMINACIÓN SOCIAL], que es respecto de quien se sostiene la obligación de rectificar.

Tratándose de un juicio verbal por razón de la materia y no por razón de la cuantía, conforme a los arts. 23.1 y 31.1 LEC, es preceptiva la intervención de procurador de los tribunales y de abogado en ejercicio, ambos habilitados ante el Tribunal, estando identificados representante y director letrado en el encabezamiento de la demanda.

IV.- Entiende esta parte que no es necesario acudir a un MASC antes de presentar una demanda ejercitando la acción de rectificación, en cuanto el derecho de rectificación es un procedimiento que tiene como finalidad la tutela de los derechos fundamentales y, por lo tanto, está excluido de cumplir el requisito de procedibilidad. Así se ha pronunciado el AAP Cantabria 226/2025, de 28 de noviembre de 2025.

V.- El fondo de la pretensión consiste en la reconstrucción de la información veraz, que por cualquier medio de difusión, es el derecho fundamental de comunicar y recibir ex art. 20.1.d) CE. La veracidad es lo que legitima el ejercicio del derecho y fija su límite.

En el caso, no se persigue excluir una opinión divulgada, sino la afirmación del hecho o dato histórico en que se funda.

Si la prueba de los hechos ordinariamente constitutivos de la pretensión pesa sobre quien agita (art. 217.2 LEC), mas la prueba de los hechos negativos, por su inviabilidad contraria a la tutela judicial efectiva, en tanto que indisponible para la parte o de máxima dificultad (art. 217.7 LEC), al contrariar el deber de colaboración con la Justicia del art. 118 CE, si no prueba el dato positivo que se niega la parte demandada, y el principio de que no puede aprovechar la propia torpeza procesal, conducirán al éxito de la demanda, al margen del éxito en acopiar por la actora documentos o testigos.

VI.- Las costas procesales deben ser impuestas a la parte demandada, por criterio del íntegro vencimiento, si no fueran en todo caso por la temeridad de oponerse a la demanda, con la limitación del art. 394.3 LEC, y en tanto que mi mandante tiene domicilio en lugar distinto a esta circunscripción.

Y demás normas y jurisprudencia de general y pertinente aplicación.

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito con sus copias y documentos adjuntados, se digne admitir uno y otros, tener por formulada demanda de juicio verbal especial en los términos manifestados, y en mérito a ellos, seguido que sea el pertinente procedimiento, se dicte Sentencia por la que se condene a la entidad [DENOMINACIÓN SOCIAL], a difundir la rectificación que consta en el documento número dos, en la tertulia radiofónica denominada [NOMBRE DEL PROGRAMA], dentro término del tercer día contado desde la notificación, o en la forma atenida al art. 3 de LO 2/84 de 26 de marzo, con pago de las costas procesales por la demandada, y todo los demás que proceda en

OTROSÍ DIGO

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa, e, incluso, en una eventual fase de ejecución por medios telemáticos, en términos del art. 399.1 II en relación al art. 437.1, ambos LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y nº [Nº] de teléfono:

Por lo expuesto,

AL TRIBUNAL NUEVAMENTE SUPLICO que, teniendo por hecha la anterior manifestación anteriores, se admita y provea en consecuencia.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a
