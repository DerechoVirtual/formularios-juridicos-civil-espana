---
name: demanda-juicio-verbal-sobre-regimen-visitas-hijo-menor-civ-0360
description: "Demanda de juicio verbal sobre régimen de visitas con un hijo menor extramatrimonial. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio verbal sobre régimen de visitas con un hijo menor extramatrimonial

> Formulario **CIV-0360** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Modelo de demanda de juicio verbal solicitando la determinación de un régimen de comunicación y visita del demandante con su hijo menor de edad, fruto de una relación de pareja de hecho al haber resultado infructuosos todos los intentos pacíficos de conseguir un acuerdo sobre las visitas al hijo menor.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio verbal sobre régimen de visitas con un hijo menor extramatrimonial» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio verbal sobre régimen de visitas con un hijo menor extramatrimonial” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-juicio-verbal-sobre-regimen-visitas-hijo-menor-civ-0360`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] FECHA (3 veces)
- [ ] Nº (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] CALLE
- [ ] CORREO ELECTRÓNICO
- [ ] LUGAR
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] NOMBRE DEL MENOR
- [ ] Nº DE COLEGIADO/A
- [ ] Nº DE DOCUMENTO
- [ ] NÚMERO
- [ ] PLAZO
- [ ] SEDE
- [ ] TELÉFONO

## Normas que cita el formulario

- art. 24.1 LEC
- art. 437.1 LEC
- art. 85.1 LOPJ
- art. 50.1 LEC
- art. 749.2 LEC
- art. 250.1.13.º LEC
- art. 2 Ley 42/2003
- art. 23 LEC
- art. 5 Ley Orgánica 1/2025
- art. 154 CC
- art. 160.1 CC
- art. 94 CC
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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…FANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) A la hora de su acreditación, todos los poderes deben estar inscritos en el Registro Electrónico de Apoderamientos Judiciales (REAJ). Se supone que, para su acreditación, basta con la consulta (de dicho Registro) automatizada orientada al dato. Algo que está a disposición de cualquier Letrado de la Administración de Justicia. Sin embargo, dado que el art. 24.2 LEC, configura la certificación de dicha inscripción como vía subsidiaria de acreditación, para el caso de que el sistema no permita aquella consulta automatizada; se señala en el modelo que se acompaña certificación electrónica. El sistema permite emitir dicha certificación para quien inscribe el poder.

(2) El art. 155.3 LEC permite fijar expresar varios domicilios del demandado (el que aparezca en el padrón municipal o conste oficialmente a estos efectos; el que aparezca en Registro oficial o en publicaciones de colegios profesionales, si se trata de empresas o personas colegiadas; donde desarrolle su actividad profesional o laboral no ocasional; si es empresa mercantil, el domicilio de cualquiera de sus administradores, gerentes, o apoderados; o, si es asociación que consta en registro oficial; el domicilio del presidente, miembro o gestor de la Junta correspondiente). Cuando se señalen varios, indicará el orden a seguir para la notificación, con vistas al éxito de la misma.

(3) El art. 155.3 LEC configura una obligación adicional del demandante, consistente en aportar cuantos datos sean de utilidad para localizar al demandado: número de identificación fiscal o de extranjeros, nº [Nº] de teléfono o de fax, dirección de correo electrónico, o similares.

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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.C.

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], representación que acredito mediante escritura de poder otorgada a mi favor (existen tres posibilidades para otorgar el apoderamiento al Procurador de los Tribunales, conforme dispone el art. 24.1 LEC)

[OPCIONAL — opción en función de cómo se haya otorgado el poder]

[ELEGIR UNA OPCIÓN: Si el poder se otorga a través de la sede judicial electrónica / Si el poder se otorga mediante comparecencia apud acta / Si el poder se otorga ante Notario]

bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS], abogado/a en ejercicio, con despacho profesional abierto en [LOCALIDAD], colegiado nº [Nº DE COLEGIADO/A] del Ilustre Colegio de la Abogacía de [LOCALIDAD], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que mediante el presente escrito vengo a formular DEMANDA DE JUICIO VERBAL SOBRE DERECHO DE COMUNICACIÓN Y VISITAS DE UN PROGENITOR RESPECTO DE SU HIJO MENOR, contra D./Dña. [NOMBRE Y APELLIDOS], con domicilio, primero en [DOMICILIO]; y segundo, el domicilio laboral en [DOMICILIO]); con email [CORREO ELECTRÓNICO]; y con número de teléfono móvil [TELÉFONO]; debiéndose cursar traslado al Ministerio Fiscal, al venir interesado un menor.

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa, e, incluso, en una eventual fase de ejecución por medios telemáticos, en términos del art. 399.1 II con relación al art. 437.1, ambos LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y nº [Nº] de teléfono:

Sirvan a la presente demanda los siguientes:

HECHOS

PRIMERO.- Mi patrocinado y la hoy demandada D./Dña. [NOMBRE Y APELLIDOS], se conocieron en [LOCALIDAD], entablándose entre ellos una relación sentimental semejante a la de los casados, que arrancó desde [FECHA] hasta hace [Nº] años, cuando, por divergencias surgidas entre ambos, se puso amigablemente fin a la misma, habiendo convivido en relación afectiva semejante al de las parejas casadas en la vivienda sita en calle [CALLE] n.º [NÚMERO] de

SEGUNDO.- Al cabo de [PLAZO], nació el hijo menor de mi patrocinado y la demandada, al que se puso de nombre [NOMBRE DEL MENOR], y fue inscrito en el Registro Civil de [LOCALIDAD], reconocido por el padre dentro del plazo de práctica de la inscripción, según se demuestra con la certificación que se acompaña como documento n.º 1.

TERCERO.- La separación de la unión de hecho referida se produjo de manera civilizada, y la demandada pasó a residir con su hijo menor en [LOCALIDAD], donde se dirige la presente, pactándose que quedara la madre con la guarda y custodia, dadas las exigencias de trabajo de mi mandante, y hasta el momento, habiéndose cumplido sin problemas, un régimen de prestación de alimentos a cargo del progenitor no custodio.

La comunicación de padre con el hijo ha sido constante, en lo que permitía la crianza del menor y el trabajo del padre, tanto en casa de la madre como mediante estancias fuera de ella, cuando la edad del niño lo ha permitido, y dentro de la mayor flexibilidad y buen acuerdo de los progenitores.

CUARTO.- Sin embargo, desde [Nº] meses la madre estableció una relación con otro hombre, y fue paulatinamente oponiéndose a las visitas de mi poderdante, alegando actividades extraescolares que menguaban el tiempo libre del menor, y negando la posibilidad de pernocta del menor con el padre, aduciendo pretextativas razones de salud.

El [FECHA], la demandada ha contraído matrimonio, y ha prohibido el acceso a su casa a mi mandante, tanto como comunicar con el hijo, llegando a mantener la propuesta de que, a cambio de renunciar a la pensión alimenticia, el padre se debe mantener alejado de "su" hijo.

QUINTO.- Han resultando infructuosos todos los intentos pacíficos de conseguir un acuerdo sobre las visitas al hijo menor, aunque se haya ofrecido incrementar las aportaciones económicas por parte del padre para el sostenimiento y educación de éste, y no se discute la guarda y custodia.

Así, previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Para demostrarlo, se acompaña como documento nº [Nº DE DOCUMENTO]

A los anteriores hechos, son aplicables los siguientes

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA.

Radicando la competencia genérica en el orden civil de la jurisdicción, y siendo cuestión de estado indisponible, detenta la competencia objetiva y funcional la Sección Civil del Tribunal de Instancia, por aplicación de lo dispuesto en los arts. 85.1 LOPJ y 45 LEC, y puesto que no está prevenido un fuero preceptivo específico, resulta territorialmente competente el Tribunal a que me dirijo, puesto que es el del partido del lugar donde tiene su domicilio la demandada, que es el fuero general de las personas físicas ex art. 50.1 LEC.

II.- CAPACIDAD Y LEGITIMACIÓN.

Tanto mi mandante como la demandada son personas físicas en pleno ejercicio de sus derechos civiles, como lo son los mayores de edad que no están incapacitados, por lo que tiene capacidad para ser parte y capacidad procesal ex arts. 6.1.1.º y 7.1 LEC.

Corresponde la legitimación activa a mi mandante por encontrarse en la situación jurídica de titularidad de patria potestad compartida, y la legitimación pasiva corresponde a la demandada D./Dña. [NOMBRE Y APELLIDOS], puesto que es quien tiene la guarda del hijo común menor, y puede y debe tolerar el ejercicio del precitado derecho, como no hace de grado, y así se manifiesta.

Tiene intervención adhesiva de carácter preceptivo el Ministerio Fiscal de conformidad con el art. 749.2 LEC, a quien se deberá conceder traslado como impera el art. 753.

III.- PROCEDIMIENTO.

La presente demanda deberá sustanciarse por las normas del juicio verbal con cauce especial del capítulo I del Título I del Libro IV LEC, de conformidad con el art. 250.1.13.º LEC, que introdujo -con la referencia al ordinal 12.º- el art. 2º de la Ley 42/2003, de 21 de noviembre, de modificación del Código Civil y de la Ley de Enjuiciamiento Civil en materia de relaciones familiares de los nietos con los abuelos, siendo finalmente retocado con la reforma de la Ley 13/2009 de 3 de noviembre.

IV.- POSTULACIÓN.

Conforme a los arts. 23 y 31 LEC se formula esta demanda por medio de Procurador de los Tribunales con poder notarial para pleitos, y con dirección y firma de Letrado ejerciente habilitado ante el tribunal.

V.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VI.- FONDO DE LA CUESTIÓN CONTROVERTIDA.

Conforme al art. 39 CE está consagrada en nuestro ordenamiento la igualdad de los hijos ante la ley con independencia de su filiación, y el deber de los padres de prestar asistencia de toda clase a los hijos habidos dentro o fuera del matrimonio.

La patria potestad es el conjunto de derechos que la ley confiere a los padres sobre la persona y los bienes de los hijos menores no emancipados, para asegurar el cumplimiento de las cargas que les incumben respecto del sostenimiento y educación que pesan sobre tales padres, que incluye tenerlos en su compañía (art. 154 CCiv).

Cuando los padres viven separados, la patria potestad se ejercerá por aquel con quien el hijo conviva (art. 156, párrafo 5.º CCiv), y sin necesidad de solicitar mi patrocinado que se le atribuya judicialmente el ejercicio conjunto con el otro progenitor de la patria potestad, o la distribución de funciones, no dejan de detentar el derecho de relacionarse con sus hijos menores (art. 160.1 CCiv), lo cual no se configura realmente como un derecho del progenitor sino como derecho del hijo de contar con el contacto físico y anímico del progenitor en orden al desarrollo de su personalidad, "evitando la ruptura por falta de convivencia de los lazos de afecto que deben mediar entre ellos" [STS de 19 de octubre de 1992 ].

Este derecho de relación ha de hacer semejante al derecho de visitar, comunicar y tener en compañía al hijo menor referido por el art. 94 CCiv al supuesto de hijos matrimoniales y caso de crisis por nulidad, separación, y divorcio, en tanto que está subordinado al interés y beneficio del hijo (STS de 21 de julio de 1993, Rec. 3467/1990).

No habiendo sido posible el acuerdo de estabilizar y garantizar el acuerdo de manera extrajudicial, y no mediando motivos, por ninguna circunstancia excepcional, para limitar o suspenderlo, se propone un régimen de visitas tradicional de distribución por medias partes del tiempo libre extraescolar.

VII.- COSTAS.

Conforme al artículo 394 LEC las costas han de imponerse a la demandada, si se opone y resulta vencida.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que, habiendo por presentado este escrito de demanda con los documentos que lo acompañan y copias de uno y otros, se digne admitirlos y teniéndome por comparecido y parte en la representación que ostento, y por promovido juicio verbal frente a D./Dña. [NOMBRE Y APELLIDOS], acuerde emplazarla, así como al Ministerio Fiscal, para que, en su caso, comparezca y la conteste, y seguido que sea todo el pertinente procedimiento, se dicte en su día sentencia por la que estimando la demanda, se determine un régimen de comunicación y visita del demandante con su hijo menor, en las siguientes condiciones:

El padre podrá tener consigo a su hijo, recogiéndole y devolviéndole en el domicilio de la madre, un fin de semana de cada dos, de sábado a las diez horas hasta el domingo a las veinte horas; en vacaciones de Navidad, el hijo pasará una mitad de sus vacaciones escolares con el padre y la otra mitad con la madre, ésta la primera mitad los años pares, y dicha primera mitad el padre los años impares; en las de Semana Santa, el hijo pasará los años pares con la madre y los impares con el padre; y durante el período de vacaciones de verano escolares, pasará el hijo el mes de julio con la madre los años pares, y el mes de agosto con el padre, de modo que los años impares pase el hijo julio con el padre y agosto con la madre.

Asimismo, se condene a la demandada a estar y pasar por la antedicha declaración a todo efecto, con imposición de las costas del juicio a la parte demandada.

Es justicia de hacerse en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a
