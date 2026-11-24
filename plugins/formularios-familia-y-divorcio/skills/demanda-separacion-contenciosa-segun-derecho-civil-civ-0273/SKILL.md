---
name: demanda-separacion-contenciosa-segun-derecho-civil-civ-0273
description: "Demanda de separación contenciosa según el Derecho civil de Cataluña. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de separación contenciosa según el Derecho civil de Cataluña

> Formulario **CIV-0273** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda de separación contenciosa conforme al Derecho Civil especial de Cataluña.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de separación contenciosa según el Derecho civil de Cataluña» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de separación contenciosa según el Derecho civil de Cataluña” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-separacion-contenciosa-segun-derecho-civil-civ-0273`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (9 veces)
- [ ] LOCALIDAD (8 veces)
- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] Nº (6 veces)
- [ ] NÚMERO (5 veces)
- [ ] CALLE (4 veces)
- [ ] FECHA (4 veces)
- [ ] NOMBRE DEL HIJO/A 2 (4 veces)
- [ ] Nº DE CUENTA (IBAN) (4 veces)
- [ ] NOMBRE DEL HIJO/A 1 (3 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] PISO (2 veces)
- [ ] BENEFICIARIO
- [ ] COLEGIO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DOMICILIO
- [ ] LUGAR
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] PORCENTAJE
- [ ] SEDE

## Normas que cita el formulario

- art. 233 CC
- art. 232 CC
- art. 770 LEC
- art. 6.1.1.º LEC
- art. 750.1 LEC
- art. 81.2.º CC
- art. 749.2 LEC
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 236 CC
- art. 394 LEC
- art. 773.1 LEC
- art. 771 LEC
- art. 773.3 LEC

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

Notas al pie del formulario original:
(1) Existe una guía y un modelo del plan de parentalidad, elaborados, con carácter meramente indicativo, y facilitados por la Dirección General de Derecho y Entidades Jurídicas de la Generalitat de Cataluña, en cumplimiento de la Disposición adicional 9.ª de la Ley 25/2010, de 29 de julio, del Libro II del Código civil de Cataluña, relativo a la persona y a la familia, que está disponible en la web del ICAB (véase modelo de plan de parentalidad).

(2) Los requisitos para que surja el derecho a compensación económica al amparo del art. 232.5 CCC son: a) la existencia de una situación de separación, nulidad o divorcio; b) que uno de los cónyuges haya trabajado para la casa sustancialmente más que el otro, o para el otro cónyuge, sin retribución o con retribución insuficiente; y c) que en el momento de la extinción del régimen el otro haya obtenido un incremento patrimonial superior.

En este sentido, la nueva regulación abandona toda referencia a la compensación como remedio sustitutorio de un enriquecimiento injusto, prescinde de la idea de sobre contribución a los gastos familiares, implícita en la formulación del art. 41 del Código de familia, y se fundamenta, sencillamente, en el desequilibrio que produce entre las economías de los cónyuges el hecho de que uno realice una tarea que no genera excedentes acumulables y el otro realice otra que sí que los genera. Por ello, basta con acreditar que uno de los dos se ha dedicado a la casa sustancialmente más que el otro.

En cuanto al criterio legal respecto a la determinación cuantitativa de la compensación económica por razón del trabajo el art. 232.5 CCC explicita que para determinar la cuantía de la indemnización se ha de tener en cuenta la duración y la intensidad de la dedicación, en base a los años de convivencia, y, concretamente, en el caso de trabajo doméstico, el hecho de la crianza de hijos o la atención personal a otros miembros de la familia que convivan con los cónyuges. Tal compensación tendrá como límite la cuarta parte de la diferencia entre los incrementos patrimoniales de los cónyuges, según cálculo del art. 232.6, salvo que de acreditarse una mayor contribución pueda la autoridad judicial incrementar tal cuantía.

En caso de nulidad del matrimonio, separación o divorcio, la compensación económica por razón de trabajo debe reclamarse en el proceso que causa la extinción del régimen, y en el caso de resoluciones o decisiones eclesiásticas, en el proceso dirigido a obtener su eficacia civil. Como cuestión previa, la sentencia matrimonial puede pronunciarse sobre el régimen vigente si las partes hacen cuestión de él (art. 232-11.1 CCC).

La cuantía de la compensación económica concedida vía art. 232-5 CCC, es perfectamente compatible con la prestación compensatoria por desequilibrio económico del art. 233-14 del mismo texto legal, si concurren los presupuestos legales de esta última, si bien ha de ser tenida en cuenta aquélla para determinar ésta (art. 232-10 CCC).

La compensación debe satisfacerse en metálico, salvo acuerdo entre las partes o si la autoridad judicial, por causa justificada y a petición de cualquiera de las partes o de los herederos del cónyuge deudor, ordena el pago total o parcial con bienes. A petición del cónyuge deudor o de sus herederos, la autoridad judicial puede aplazar el pago de la compensación u ordenar que se haga a plazos, con un vencimiento máximo de tres años y el devengo del interés legal a contar del reconocimiento. La autoridad judicial puede, en este caso, ordenar la constitución de garantías a favor del cónyuge acreedor (art. 232-8 CCC).

Con relación a las especialidades procesales, se ofrece en la disposición adicional 3.ª CCC una vía procesal para canalizar la reclamación de la compensación económica por razón de trabajo e incentivar que en el proceso correspondiente se presente toda la documentación relevante.

========================================================================


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

D./Dña. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, que actúa en nombre y representación de Dña. [NOMBRE Y APELLIDOS], provista de D.N.I. n.º [NÚMERO], con domicilio en [LOCALIDAD], calle [CALLE], a virtud de poder para pleitos cuya copia acompaño para su unión a los autos mediante testimonio bastante, con ruego de devolución de la copia autorizada por necesitarla a otros usos, bajo dirección de la Letrada D.ª [NOMBRE Y APELLIDOS], colegiada n.º [NÚMERO] del Iltre. Colegio de Abogados de [COLEGIO], cuyo despacho se abre en [LOCALIDAD], calle [CALLE], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que por medio del presente escrito, siguiendo la instrucción de mi mandante, vengo a formular DEMANDA CONTENCIOSA DE SEPARACIÓN frente a su esposo D. [NOMBRE Y APELLIDOS], con domicilio actual en [DOMICILIO], con base a los siguientes datos y argumentos:

HECHOS

PRIMERO.- Mi mandante contrajo matrimonio canónico con D. [NOMBRE Y APELLIDOS], en [LOCALIDAD], el día [FECHA] Se acompaña la correspondiente certificación de matrimonio expedida por el Registro Civil de [LOCALIDAD] (DOCUMENTO N.º [NÚMERO]).

De dicha unión nacieron dos hijos que son menores de edad, de nombre [NOMBRE DEL HIJO/A 1] y [NOMBRE DEL HIJO/A 2], nacidos el [FECHA], y el [FECHA]

Se adjuntan las correspondientes certificaciones de nacimiento que ha emitido el Registro Civil de [LOCALIDAD] (DOCUMENTOS NÚMEROS [Nº] y [Nº]).

SEGUNDO.- Como consecuencia de las desavenencias entre los cónyuges, sin que mi representada tenga por el momento deseo de disolver el vínculo, está persuadida de lo adecuado de su decisión de separación matrimonial.

TERCERO.- El régimen económico del matrimonio es el de separación de bienes, ya que por residencia y lugar de celebración del matrimonio la vecindad de los cónyuges es la catalana, no habiéndose otorgado nunca capitulaciones matrimoniales, por lo que no corresponde realizar liquidación alguna del referido régimen económico matrimonial.

CUARTO.- En la actualidad, mi mandante ocupa junto a los dos hijos habidos del matrimonio el domicilio conyugal, perteneciente en plena propiedad y por mitades indivisas a ambos cónyuges.

Adjunto certificado de empadronamiento y escritura pública de propiedad de la vivienda familiar, donde consta que es propiedad indivisa de ambos por partes iguales (DOCUMENTOS NÚMEROS [Nº] y [Nº]).

Por su parte, el Sr./a. tiene su residencia en casa de sus padres, sita en [LOCALIDAD], que es el domicilio arriba reseñado.

QUINTO.- Los hijos menores de edad han estado siempre en compañía de la madre, mi mandante, y es lo conveniente que queden bajo la guarda individual o exclusiva de ella, que ha sido quien ha dedicado toda su vida al cuidado del hogar; y asimismo debe atribuírsele el uso de la vivienda familiar por razón de la guarda de los hijos.

De acuerdo con lo establecido en el art. 233-8.2 del Libro II del Código Civil de Cataluña aprobado por Ley 25/2010 de 29 de julio (en adelante, CCC), se acompaña propuesta de plan de parentalidad para el ejercicio de las responsabilidades parentales con respecto a la guarda, cuidado y educación de los hijos comunes, conforme al art. 233-9 CCC, como DOCUMENTO NÚMERO [Nº DE DOCUMENTO].

SEXTO.- El demandado percibe unos ingresos de [IMPORTE] euros mensuales como trabajador de la empresa [DENOMINACIÓN SOCIAL], mientras que mi representada carece de cualificación profesional de cualquier tipo, por haber dedicado su vida, desde su matrimonio, al cuidado de la casa y de la familia, habiendo tenido que recurrir a la realización de trabajos de empleada de hogar, en forma discontinua, que le han permitido atender las necesidades vitales de sus hijos y los gastos de la casa, con la ayuda de sus padres. Se adjunta, al objeto de demostrar las rentas de la unidad familiar, copias de la declaración -conjunta- del I.R.P.F. del año pasado y el anterior, como DOCUMENTOS NÚMEROS [Nº] y [Nº].

Por ello, dado el desequilibrio que la ruptura de la convivencia provocará en mi mandante, procede que se acuerde, como prestación compensatoria en forma de pensión, la cantidad de [IMPORTE] € mensuales, sin que se solicite compensación económica al amparo del art. 232-5 CCC.

Esta pensión se pagará por meses anticipados, dentro de los cinco primeros días de cada mes, mediante ingreso en [Nº DE CUENTA (IBAN)] Para su actualización, deberá estarse a las variaciones que experimenten los índices de precio al consumo, según el Instituto Nacional de Estadística u organismo que le sustituya, y a los posibles aumentos de sueldo que obtuviera el demandado.

SÉPTIMO.- Los gastos que ocasionan la manutención, vestido y educación de los hijos ascienden, aproximadamente, a [IMPORTE] € mensuales.

Conforme a lo dicho, procede fijar en la cantidad de [IMPORTE] € mensuales la pensión alimenticia que corresponde pagar al demandado, estando a lo ya dicho respecto a la prestación compensatoria a efectos del pago y de actualizaciones.

OCTAVO.- Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN.

Es competente la jurisdicción civil, según lo establecido en los arts. 9.2 y 21.1 de la LOPJ.

II.- COMPETENCIA.

Es competente el Tribunal de Instancia del lugar del domicilio del demandado, que es el criterio alternativo, a elección del demandante, conforme al art. 769.1, párrafo 1.º LEC.

III.- PROCEDIMIENTO.

El procedimiento adecuado es el del art. 770 LEC para conocer de las demandas de separación contenciosas.

IV.- CAPACIDAD.

Mi mandante ostenta capacidad procesal suficiente, conforme al art. 6.1.1.º LEC.

V.- POSTULACIÓN.

Comparece representada por Procurador debidamente habilitado para actuar en el territorio de este Tribunal, y asistido por Abogado, conforme a lo establecido en el art. 750.1 LEC.

VI.- LEGITIMACIÓN.

Tiene la demandante legitimación activa ordinaria por hallarse en la situación jurídica de relación conyugal, como detenta la pasiva su marido demandado (arts. 81.2.º CCiv y 10, párrafo 1.º LEC), siendo el objeto del proceso principal la pretensión de separación conyugal y la adopción de medidas definitivas derivadas de la misma.

VII.- INTERVENCIÓN DEL MINISTERIO FISCAL.

Dada la presencia de hijos menores del matrimonio, es preceptiva la intervención del Ministerio Fiscal, según lo establecido en el art. 749.2 LEC.

VIII.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

IX.- PETICIÓN DE SEPARACIÓN.

El fondo de la pretensión consiste en la declaración de separación conyugal sin consenso de los cónyuges, a instancia de uno solo de ellos (art. 81.2.º CCiv), sin necesidad de invocar ni demostrar causa legal alguna, por más de ser evidente que el demandado no ha cumplido cabalmente sus deberes conyugales, ni con los hijos comunes, fundándose en el derecho subjetivo constitucionalizado a contraer matrimonio, sin renuncia mínima al libre desarrollo de la personalidad, sin que sea preciso exteriorizar motivos materiales para poner fin a la convivencia.

X.- MEDIDAS QUE HAN DE REGULAR LOS EFECTOS DE LA SEPARACIÓN.

En relación a las medidas a adoptar el art. 233-4 CCC dispone que "1. Si un cónyuge solicita la nulidad del matrimonio, el divorcio o la separación judicial sin consentimiento del otro, o si ambos cónyuges no llegan a un acuerdo sobre el contenido del convenio regulador, la autoridad judicial debe adoptar las medidas definitivas pertinentes sobre el ejercicio de las responsabilidades parentales, incluidos el deber de alimentos... 2. Si alguno de los cónyuges lo solicita, la autoridad judicial debe adoptar las medidas pertinentes respecto al uso de la vivienda familiar y su ajuar, la prestación compensatoria, la compensación económica por razón del trabajo si el régimen económico es el de separación de bienes, la liquidación del régimen económico matrimonial y la división de los bienes comunes o en comunidad ordinaria indivisa".

Son de aplicación el art. 233-14 CCC en relación a la existencia de desequilibrio económico por parte de la esposa; el art. 236-8 CCC sobre la potestad parental del padre y de la madre; el art. 236-17.1 CCC relativo a las pensiones de los hijos; y el art. 233-20.2 con referencia a la atribución de la vivienda familiar.

También resulta de aplicación el art. 233-8.1 CCC, que al referirse al carácter compartido de las responsabilidades parentales, precisa que deberán ejercerse conjuntamente "en la medida de lo posible", sin olvidar que el art. 233-10.2 CCC otorga al Juez la posibilidad de atribuir la guarda exclusiva "si conviene más al interés del hijo", sin hacer especial mención a la preferencia sobre la guarda compartida.

En cualquier caso, entiende esta parte que con independencia de que la regulación de esta materia establezca una preferencia por uno u otro sistema de guarda, conjunta o exclusiva de uno de los progenitores, la decisión judicial no debe ser sometida a la preferencia de la Ley sino únicamente al interés superior del menor, y en ningún caso puede obviarse lo dispuesto en el art. 39 CE y los arts. 1 y 2 y 11.2 de la Ley Orgánica 1/1996, 15 de enero, de Protección Jurídica del Menor.

En definitiva, en opinión de esta representación, el beneficio de los menores exige la atribución de la guarda exclusiva a mi mandante, destacando los arts. 233-11.1.a), d) y e) CCC como criterio para determinar la guarda individual la vinculación especial de los hijos con uno de los progenitores, la dedicación a los hijos que la madre o el padre hayan tenido antes de la ruptura, y la propia opinión expresada por los hijos, sin perjuicio de garantizar el régimen de relación y comunicación con los hijos para el progenitor que no tenga la guarda.

XI.- COSTAS.

No hay ninguna razón para excluir la aplicación del principio del vencimiento en punto a laa costas procesales (art. 394 LEC), debiéndose condenar al demandado que se oponga, dado que el obtener la razón precisando de un proceso no ha de suponer una merma patrimonial del que tiene razón.

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito con los documentos que se acompañan y sus copias, se digne admitirlos, tenerme por comparecida y parte en la representación que ostento, entendiéndose conmigo las sucesivas diligencias y por formulada demanda de separación legal, de modo que seguido que sea el pertinente procedimiento, con citación del Ministerio Fiscal, se dicte en su día sentencia por la que estimando la presente demanda:

1.º) DECLARE la separación del matrimonio por causa legal entre D. y Dña. [NOMBRE Y APELLIDOS], oficiándose al Registro Civil de [LOCALIDAD] para la anotación de su parte dispositiva en la inscripción del matrimonio.
2.º) ACUERDE las siguientes medidas definitivas, que se podrán modificar si se alteraren sustancialmente las circunstancias:
1.- Atribución de la guarda individual de los hijos menores [NOMBRE DEL HIJO/A 1] y [NOMBRE DEL HIJO/A 2] a la demandante, conforme al plan de parentalidad para el ejercicio de las responsabilidades parentales propuesto por esta parte.
2.- Atribución del uso exclusivo de la vivienda familiar sita en la calle [CALLE], n.º [NÚMERO], piso [PISO], a la demandante y los dos hijos, así como del ajuar doméstico en ella existente.
3.- Establecimiento de una pensión compensatoria a favor de la demandante de [IMPORTE] euros mensuales ( [IMPORTE] €), y sendas pensiones alimenticias, a favor de [BENEFICIARIO] y de [NOMBRE DEL HIJO/A 2] de [IMPORTE] euros mensuales ( [IMPORTE] €), todas ellas a cargo del demandado D. [NOMBRE Y APELLIDOS], pagaderas por meses anticipados, mediante ingreso en la cuenta corriente [Nº DE CUENTA (IBAN)], y actualizables anualmente conforme a las variaciones que experimente el Índice de Precios al Consumo que publique el Instituto Nacional de Estadística, u organismo oficial que lo sustituya.

(En su caso, si procede: "3.º) DECLARE el derecho de la demandante a percibir una compensación económica al amparo del art. 232-5 CCC que se cuantifica eneuros, atendiendo a todas las circunstancias, pagaderos por la parte adversa en el plazo máximo de tres años desde la fecha de la sentencia, con el devengo desde entonces, hasta su total pago de los intereses legales" )

En todo caso, se pronuncie el reintegro de las costas con cargo a la parte demandada, si se opusiere.

Es Justicia de hacerse en (lugar y fecha).

OTROSÍ DIGO: Que por necesitar para otros usos la copia de escritura de poder acreditativa de la representación del suscrito Procurador, intereso y

SUPLICO AL TRIBUNAL. Se sirva acordar su desglose y devolución a esta parte, dejando en autos testimonio de la misma.

SEGUNDO OTROSÍ DIGO: Que al amparo del art. 773.1 LEC, no habiéndose adoptado con anterioridad, se solicitan mediante el presente escrito MEDIDAS PROVISIONALES coetáneas a la admisión de la demanda, en base a los siguientes:

HECHOS

PRIMERO.- Los dos hijos menores comunes del matrimonio han permanecido siempre en compañía de la madre, y es lo conveniente que continúen con ella, habida cuenta de la edad de los hijos y las circunstancias que rodean a la presente ruptura, pareciendo suficiente la comunicación y estancia sin pernocta del padre, en casa de los abuelos donde éste reside, los sábados de todas las semanas, por lo menos hasta la resolución definitiva.

SEGUNDO.- Puesto que el interés familiar más necesitado de protección es el de los hijos en potestad, tanto ellos como mi representada deben continuar en el uso de la vivienda familiar.

TERCERO.- Como quiera que mi representada carece de ingresos estables o de bienes rentables, constituyendo las fuentes del activo familiar el sueldo como trabajador por cuanta ajena del demandado, es necesaria su aportación con el [PORCENTAJE] % para hacer frente a los gastos familiares, toda vez que el demandado vive con sus padres, que gozan de asentada posición.

La dicha cantidad debiera ser directamente ingresada en la cuenta bancaria [Nº DE CUENTA (IBAN)], habida cuenta que todos los datos apuntan que el cumplimiento voluntario no es verosímil que se produzca, y en evitación de dilaciones y diligencias ejecutivas inútiles.

FUNDAMENTOS DE DERECHO

I.- El cónyuge que solicita la separación está legitimado para pedir con la demanda medidas provisionales del art. 233-1 CCC.

II.- El procedimiento adecuado es el del art. 771 LEC para medidas previas, conforme remisión del art. 773.3 LEC.

III.- Esta pretensión consiste en la adopción de los efectos "ope legis" del art. 233-1.5 CCC y medidas del art. 233-1.1 CCC, de cognición judicial, derivados de la tutela cautelar por la lesión que, de no adoptarse, pueden padecer las partes y los hijos menores, por la duración del proceso.

En su virtud,

SUPLICO AL TRIBUNAL

que, teniendo por causadas las precedentes manifestaciones a los efectos oportunos, y por deducida solicitud de adopción de medidas provisionales, seguido que sea su pertinente trámite, se dicte Auto por el que se aprueben las siguientes:

a) Asignación a la madre actora de la guarda de los dos hijos menores en potestad parental [NOMBRE DEL HIJO/A 1] y [NOMBRE DEL HIJO/A 2]
b) Fijación de un derecho provisional de comunicación del demandado con sus hijos todos los sábados de cada semana de diez a veinte horas.
c) Atribución del uso exclusivo de la vivienda familiar sita en la calle [CALLE], n.º [NÚMERO], piso [PISO], a la solicitante y los dos hijos, así como del ajuar doméstico en ella existente. Para la constancia de dicho derecho de uso, expedirá mandamiento por duplicado el Tribunal junto con testimonio del Auto que la acuerde, a fin de que el Registro de la Propiedad de [LOCALIDAD] publique la afectación de la finca.
d) Fijación de la cantidad de [IMPORTE] euros mensuales en concepto de contribución a los gastos familiares, que será ingresada, en cumplimiento de oficio del Tribunal, por meses anticipados, dentro de los cinco primeros días de cada mes en la cuenta bancaria [Nº DE CUENTA (IBAN)] Dicha cantidad se actualizará anualmente, con efectos de primero de enero de cada año, en proporción a las variaciones que experimenten los índices de precio al consumo, según el Instituto Nacional de Estadística u organismo que le sustituya.

Reitero Justicia en lugar y fecha "ut supra".

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a
