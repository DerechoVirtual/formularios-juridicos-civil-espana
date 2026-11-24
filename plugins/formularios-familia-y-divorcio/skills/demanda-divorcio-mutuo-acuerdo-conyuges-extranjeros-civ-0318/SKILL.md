---
name: demanda-divorcio-mutuo-acuerdo-conyuges-extranjeros-civ-0318
description: "Demanda de divorcio de mutuo acuerdo de cónyuges extranjeros comunitarios. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de divorcio de mutuo acuerdo de cónyuges extranjeros comunitarios

> Formulario **CIV-0318** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda conjunta de divorcio de mutuo acuerdo (art. 777 LEC) de cónyuges extranjeros de la Unión Europea con residencia habitual en España y con hijos menores, que incluye los fundamentos de competencia internacional (Reglamento (UE) 2019/1111) y de ley aplicable al divorcio, al régimen económico, a las relaciones paternofiliales y a los alimentos, y a la que se acompaña propuesta de convenio regulador.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de divorcio de mutuo acuerdo de cónyuges extranjeros comunitarios» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de divorcio de mutuo acuerdo de cónyuges extranjeros comunitarios” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-divorcio-mutuo-acuerdo-conyuges-extranjeros-civ-0318`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (8 veces)
- [ ] DOMICILIO (4 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] NOMBRE (3 veces)
- [ ] AÑO (2 veces)
- [ ] DÍA (2 veces)
- [ ] EDAD (2 veces)
- [ ] ESTADO CUYA LEY SE ELIGE (2 veces)
- [ ] FECHA (2 veces)
- [ ] FIRMA (2 veces)
- [ ] MES (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] NOMBRE DEL HIJO/A (2 veces)
- [ ] DOMICILIO PROFESIONAL
- [ ] NOMBRE DE LA SECCIÓN SEGÚN EL TRIBUNAL DE INSTANCIA
- [ ] NOMBRE Y APELLIDOS DE UN CÓNYUGE
- [ ] NOMBRE Y APELLIDOS DEL ABOGADO/A
- [ ] NOMBRE Y APELLIDOS DEL OTRO CÓNYUGE
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº DE COLEGIADO
- [ ] Nº DE DOCUMENTO
- [ ] NÚMERO
- [ ] SEDE

## Normas que cita el formulario

- art. 9.2 CC
- art. 777 LEC
- art. 36.1 LEC
- art. 9.2 LOPJ
- art. 45 LEC
- art. 85.1 LOPJ
- art. 86 LOPJ
- art. 769 LEC
- art. 10 LEC
- art. 750 LEC
- art. 9.4 CC
- art. 281 LEC
- art. 749.2 LEC

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

- Junto a «…erior a la celebración, esto es, la ley [ELEGIR: española / OTRA LEY APLICABLE].»: para matrimonios celebrados desde el 29 de enero de 2019 puede resultar aplicable el Reglamento (UE) 2016/1103 sobre régimen económico matrimonial; comprobar la norma aplicable según la fecha del matrimonio.

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

AL TRIBUNAL DE INSTANCIA
SECCIÓN CIVIL – SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, que actúa en nombre y representación de los esposos D./Dña. [NOMBRE Y APELLIDOS DE UN CÓNYUGE], vecino/a de [LOCALIDAD], con domicilio en [DOMICILIO], y D./Dña. [NOMBRE Y APELLIDOS DEL OTRO CÓNYUGE], vecino/a de [LOCALIDAD], con domicilio en [DOMICILIO], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento n.º [Nº DE DOCUMENTO], bajo dirección del/de la Letrado/a D./Dña. [NOMBRE Y APELLIDOS DEL ABOGADO/A], colegiado/a n.º [Nº DE COLEGIADO] del Ilustre Colegio de la Abogacía de [LOCALIDAD], cuyo despacho se abre en [DOMICILIO PROFESIONAL], ante el Tribunal comparezco y, como mejor en Derecho proceda, DIGO:

Que por medio del presente escrito y siguiendo instrucciones de mis mandantes, vengo a formular demanda de DIVORCIO DE MUTUO ACUERDO de los cónyuges arriba indicados, con base en los siguientes:

HECHOS

PRIMERO.– D./Dña. [NOMBRE Y APELLIDOS], de nacionalidad [NACIONALIDAD], y D./Dña. [NOMBRE Y APELLIDOS], de nacionalidad [NACIONALIDAD], contrajeron matrimonio [ELEGIR: canónico / civil] en [LOCALIDAD], el día [DÍA] de [MES] de [AÑO], a cuya acreditación se acompaña certificación expedida por el Registro Civil de [LOCALIDAD], como documento n.º 1.

SEGUNDO.– Del referido matrimonio nacieron y viven [NÚMERO] hijos, de nombres [NOMBRE DEL HIJO/A] y [NOMBRE DEL HIJO/A], menores de edad, que tienen [EDAD] y [EDAD] años de edad, respectivamente, como se demuestra con sendas certificaciones registrales que hacen documentos n.os 2 y 3.

TERCERO.– El régimen económico del matrimonio es el de [RÉGIMEN ECONÓMICO MATRIMONIAL, por ejemplo, gananciales], en aplicación de la cláusula general del Derecho internacional privado español del art. 9.2 CC, conforme a la que los efectos del matrimonio, a falta de elección de las partes sobre la ley aplicable, se rigen por la ley de la residencia habitual común inmediatamente posterior a la celebración, esto es, la ley [ELEGIR: española / OTRA LEY APLICABLE].

CUARTO.– El matrimonio fijó el domicilio conyugal en la calle [DOMICILIO] de [LOCALIDAD], en vivienda en régimen de [ELEGIR: alquiler / propiedad]. Se acompaña como documento n.º 4 el [TÍTULO DE LA VIVIENDA, por ejemplo, contrato de arrendamiento concertado por D./Dña. [NOMBRE] en fecha [FECHA]].

Desde [FECHA] el matrimonio decidió hacer vidas separadas e independientes, encontrándose desde entonces separados de hecho. Actualmente ambos residen en el municipio de [LOCALIDAD], en distintos domicilios: D./Dña. [NOMBRE] sigue residiendo en el que había sido el domicilio familiar junto con sus hijos menores de edad y D./Dña. [NOMBRE] reside desde entonces en la calle [DOMICILIO], conforme acredito con certificados de empadronamiento que se acompañan como documentos n.os 5 y 6.

QUINTO.– Por razones debidamente sopesadas, es voluntad de los dos cónyuges no solo poner fin a su vida en común, sino proceder también a la extinción del vínculo mediante divorcio por mutuo acuerdo y adopción de medidas correlativas.

SEXTO.– Conforme a lo exigido por el apartado 2.º del art. 777 LEC, se adjunta al presente escrito, como documento n.º 7, propuesta de convenio regulador firmada por ambos cónyuges.

A los anteriores hechos son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

I.– JURISDICCIÓN Y COMPETENCIA

Competencia internacional.

La resolución de la pretensión de divorcio pertenece a la jurisdicción y, a tenor del art. 36.1 LEC, la extensión y límites de la jurisdicción de los tribunales civiles españoles se determinará por lo dispuesto en la Ley Orgánica del Poder Judicial y en los tratados y convenios internacionales en los que España sea parte.

Dicha normativa viene constituida por el Reglamento (UE) 2019/1111 del Consejo, de 25 de junio de 2019, relativo a la competencia, el reconocimiento y la ejecución de resoluciones en materia matrimonial y de responsabilidad parental, y sobre la sustracción internacional de menores, que deroga, con efectos desde el 1 de agosto de 2022, el Reglamento (CE) n.º 2201/2003.

En materia de matrimonio, el art. 3.a).i) del Reglamento atribuye competencia para resolver las cuestiones relativas al divorcio, la separación judicial o la nulidad del matrimonio de los cónyuges a los órganos jurisdiccionales del Estado miembro en cuyo territorio se encuentre la residencia habitual de los cónyuges.

Respecto a la responsabilidad parental y guarda y custodia de los hijos comunes, los tribunales españoles son competentes en virtud de lo dispuesto en el art. 7.1 del Reglamento, aplicable a las materias civiles relativas «a la atribución, el ejercicio, la delegación, la restricción o la finalización de la responsabilidad parental» (art. 1.1.b), que establece que «Los órganos jurisdiccionales de un Estado miembro serán competentes en materia de responsabilidad parental respecto de un menor que resida habitualmente en dicho Estado miembro en el momento en que se acuda al órgano jurisdiccional».

Competencia genérica.

Está atribuida al orden civil de jurisdicción, conforme al art. 9.2 LOPJ.

Competencia objetiva.

Por lo tocante a la competencia objetiva, corresponde a los Tribunales de Instancia (art. 45 LEC en relación con el art. 85.1 LOPJ) y, con arreglo a la especialización ex art. 86 LOPJ, a las Secciones de Familia, Infancia y Capacidad que hay en esta ciudad. [NOMBRE DE LA SECCIÓN SEGÚN EL TRIBUNAL DE INSTANCIA]

Competencia territorial interna.

Se asigna desde el art. 769 LEC a los Tribunales del último domicilio del matrimonio.

II.– LEGITIMACIÓN

Ostentan las partes legitimación ordinaria por ocupar la posición de cónyuges en la situación jurídica de relación matrimonial (art. 10, párrafo primero, LEC), siendo el objeto de la pretensión la disolución vincular por divorcio.

III.– REPRESENTACIÓN Y POSTULACIÓN

Conforme al art. 750 LEC, mis representados se valen de una sola defensa y representación.

IV.– PROCEDIMIENTO

La acción debe tramitarse conforme a lo establecido en el art. 777 LEC, que es el procedimiento adecuado para conocer de las peticiones de divorcio de mutuo acuerdo, o de un cónyuge con el consentimiento del otro.

V.– CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD

La presente demanda no está sujeta al previo intento de resolución de controversias en vía no jurisdiccional de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia, por tratarse en sí de un acuerdo consensual y voluntario entre las partes, necesitando únicamente la homologación del mismo por parte del Tribunal, siendo que el convenio regulador (arts. 775.2 y 777.9 LEC y 90.3 CC) se entiende acreditativo de haber realizado esa actividad negociadora.

VI.– FONDO DEL ASUNTO

Ley sustantiva aplicable

AL DIVORCIO

Se invoca la aplicación de la legislación de [ESTADO CUYA LEY SE ELIGE], al haberse convenido como ley aplicable al divorcio, como habilita el art. 5 del Reglamento (UE) n.º 1259/2010 del Consejo, de 20 de diciembre de 2010, por el que se establece una cooperación reforzada en el ámbito de la ley aplicable al divorcio y a la separación judicial.

Se adjunta como documento n.º 8 convenio de elección de la ley aplicable al divorcio celebrado por los cónyuges, conforme al art. 7 del citado Reglamento.

AL RÉGIMEN ECONÓMICO MATRIMONIAL

En aplicación del art. 9.2 CC, resulta de aplicación la ley [ELEGIR: española / OTRA LEY APLICABLE], al ser la ley de la residencia habitual común inmediatamente posterior a la celebración del matrimonio.

A LAS RELACIONES PATERNOFILIALES

Deberá aplicarse el derecho del foro según el art. 15 del Convenio de La Haya de 19 de octubre de 1996 relativo a la competencia, la ley aplicable, el reconocimiento, la ejecución y la cooperación en materia de responsabilidad parental y de medidas de protección de los niños.

El citado precepto incorpora la máxima lex fori in foro propio, estableciendo que las autoridades de los Estados contratantes aplicarán su propia ley cuando resulten internacionalmente competentes de conformidad con las disposiciones del Capítulo II del Convenio.

Ahora bien, dado que los menores respecto de los cuales se interesan las medidas definitivas de la situación derivada del divorcio residen habitualmente en España, la competencia judicial internacional viene determinada no por los foros de competencia judicial internacional del dicho Capítulo II del Convenio de La Haya de 1996, sino por las disposiciones del Reglamento (UE) 2019/1111 del Consejo, de 25 de junio de 2019, de conformidad con lo previsto en el art. 97.1.a) del propio Reglamento, que en materia de responsabilidad parental (art. 7.1) otorga competencia a los órganos jurisdiccionales del Estado miembro de la residencia habitual del menor en el momento en el que se presenta el asunto ante dicho órgano jurisdiccional.

De este modo, una interpretación estricta del art. 15.1 del Convenio de La Haya de 1996 podría inducir a pensar que en supuestos como el que nos ocupa no resultaría de aplicación la norma de conflicto convencional, debiendo, entonces, acudirse a la norma de conflicto de producción interna, es decir, al art. 9.4 CC. No obstante lo dicho, de conformidad con acreditada doctrina científica, debe entenderse que si, como es el caso, el foro del Reglamento 2019/1111 en el cual el órgano jurisdiccional fundamenta su competencia judicial internacional, en tanto que incorpora idéntico criterio de atribución de competencia, es equivalente a uno de los que contempla el Convenio de La Haya de 1996, nada impide al Tribunal aplicar las normas de conflicto previstas en el citado Convenio. Dicha solución resulta conforme con el «espíritu conflictual» del Convenio, puesto que lleva a aplicar el Derecho material del Estado contratante cuyas autoridades resultan competentes en virtud de uno de los foros previstos en la propia norma convencional, cual es el de la residencia habitual del menor, incorporado en el art. 5.1 del Convenio de La Haya de 1996 (en este sentido, SAP Zaragoza de 20 de abril de 2012, rec. 146/2012).

A LOS ALIMENTOS A MENORES

Resulta de aplicación la ley española, por disposición del art. 15 del Reglamento (CE) n.º 4/2009 del Consejo, de 18 de diciembre de 2008, relativo a la competencia, la ley aplicable, el reconocimiento y la ejecución de las resoluciones y la cooperación en materia de obligaciones de alimentos, que establece que se determinará de acuerdo con el Protocolo de La Haya de 23 de noviembre de 2007, cuyo art. 3 también fija el criterio de la residencia del menor, como ya hacía el art. 4 del Convenio de La Haya de 2 de octubre de 1973, al que ha venido a sustituir, como expresamente se establece en su art. 18.

Pretensiones ejercibles

El fondo de la pretensión consiste en la declaración de divorcio, causa de disolución del matrimonio, a instancia de ambos cónyuges, lo cual procede por aplicación de lo dispuesto en los arts. 86, por relación al 81 in fine, y 90 CC y 774 LEC: el Tribunal deberá homologar el convenio regulador que se aporta, como medidas definitivas de la situación derivada del divorcio, puesto que no es gravemente perjudicial para ninguno de los cónyuges ni dañoso para los hijos y, en su caso, aplicar las garantías adicionales que procedan.

Acreditación

De conformidad con el art. 281 LEC, además de los hechos relativos a la tutela judicial solicitada en el proceso, es objeto de prueba la costumbre y el derecho extranjero, el cual deberá ser probado en lo que respecta a su contenido y vigencia, pudiendo valerse el tribunal de cuantos medios de averiguación estime necesarios para su aplicación.

Se aporta como documento n.º 9 traducción al español de la legislación de [ESTADO CUYA LEY SE ELIGE] en vigor.

VII.– INTERVENCIÓN DEL MINISTERIO FISCAL

Con arreglo al art. 749.2 LEC, deberá ser parte el Ministerio Fiscal, por hacerse referencia a cuestiones en las que debe intervenir, dado que se trata de pactos del convenio relativos a medidas que afectan a menores.

VIII.– COMUNICACIÓN A LOS REGISTROS PÚBLICOS

La sentencia de divorcio dictada por este Tribunal se comunicará de oficio al Registro Civil donde figura inscrito el matrimonio, de conformidad con lo preceptuado en la normativa que lo rige.

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito con los documentos que se acompañan y sus copias, se digne admitirlos, y se tenga por formulada DEMANDA DE DIVORCIO DE MUTUO ACUERDO entre los cónyuges D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS], entendiéndose conmigo las sucesivas diligencias y, previos los pertinentes trámites, los cónyuges sean requeridos por el Letrado de la Administración de Justicia para que comparezcan y se ratifiquen por separado, con intervención del Ministerio Fiscal, dictándose en su día Sentencia por la que se declare la disolución del matrimonio por divorcio, con todos los efectos legales inherentes a esta declaración, aprobándose el convenio regulador aportado como medidas definitivas en cuanto a los efectos de dicho divorcio.

OTROSÍ DIGO: Que, por necesitar para otros usos la copia de escritura de poder acreditativa de la representación del suscrito Procurador, intereso y

SUPLICO AL TRIBUNAL se sirva acordar su desglose y devolución a esta parte, dejando en autos testimonio de la misma.

Es justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a: [FIRMA] Firma del Procurador/a: [FIRMA]
