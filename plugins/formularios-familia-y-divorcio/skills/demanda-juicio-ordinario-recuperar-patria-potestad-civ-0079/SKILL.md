---
name: demanda-juicio-ordinario-recuperar-patria-potestad-civ-0079
description: "Demanda de juicio ordinario para recuperar la patria potestad. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio ordinario para recuperar la patria potestad

> Formulario **CIV-0079** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda sobre recuperación de la patria potestad; en cuanto al procedimiento a seguir, contempla la opción inicial por la regla del declarativo correspondiente, que reconduce al juicio ordinario, o si esa privación se hubiera acordado en un proceso matrimonial, o de relaciones paterno filiales, a través del procedimiento de modificación de medidas.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio ordinario para recuperar la patria potestad» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio ordinario para recuperar la patria potestad” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-juicio-ordinario-recuperar-patria-potestad-civ-0079`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] FECHA (3 veces)
- [ ] SEDE (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] EXPONER LOS HECHOS (2 veces)
- [ ] AÑO
- [ ] CORREO ELECTRÓNICO
- [ ] DESCRIBIR
- [ ] FECHA DE LA SENTENCIA
- [ ] LUGAR
- [ ] Nº
- [ ] Nº DE COLEGIADO/A
- [ ] NÚMERO
- [ ] PARTE DEMANDADA
- [ ] TELÉFONO
- [ ] TIPO DE PROCEDIMIENTO

## Normas que cita el formulario

- art. 24.1 LEC
- art. 399.1 LEC
- art. 36 LEC
- art. 85.1 LOPJ
- art. 769.1 LEC
- art. 10 LEC
- art. 23 LEC
- art. 249.2 LEC
- art. 250 LEC
- art. 4.1 LO 1/2025
- art. 154 CC
- art. 170 CC
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

- Junto a «…MILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], representación que acredito mediante escritura de poder otorgada a mi favor (existen tres posibilidades para otorgar el apoderamiento al Procurador de los Tribunales, conforme dispone el art. 24.1 LEC)

[OPCIONAL — opción en función de cómo se haya otorgado el poder]

[ELEGIR UNA OPCIÓN: Si el poder se otorga a través de la sede judicial electrónica / Si el poder se otorga mediante comparecencia apud acta / Si el poder se otorga ante Notario]

bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS], abogado/a en ejercicio, con despacho profesional abierto en [LOCALIDAD], colegiado nº [Nº DE COLEGIADO/A] del Ilustre Colegio de la Abogacía de [LOCALIDAD], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que mediante el presente escrito vengo a formular demanda de juicio ordinario para la recuperación de la patria potestad respecto a su hijo mayor de edad incapacitado [NOMBRE Y APELLIDOS], contra D./Dña. [NOMBRE Y APELLIDOS], con domicilio, primero en [DOMICILIO]; y segundo, el domicilio laboral en [DOMICILIO]); con email [CORREO ELECTRÓNICO]; y con número de teléfono móvil [TELÉFONO]; todo ello de conformidad con los hechos y fundamentos de derecho que se especificarán.

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa, e, incluso, en una eventual fase de ejecución por medios telemáticos, en términos del art. 399.1 II LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y nº [Nº] de teléfono:

HECHOS

PRIMERO.- Que [NOMBRE Y APELLIDOS] es hijo de mi representado/a, fruto de su matrimonio con D./Dña. [NOMBRE Y APELLIDOS], nacido el día [FECHA], según se acredita demuestra con la certificación registral que se presenta como documento n.º [NÚMERO].

SEGUNDO.- Que mediante Sentencia de fecha [FECHA DE LA SENTENCIA] la Sección Civil del Tribunal de Instancia de [SEDE] declaró la discapacidad de [LOCALIDAD], rehabilitando la patria potestad de sus progenitores sobre el mismo, al haber alcanzado a esa fecha su mayoría de edad.

TERCERO.- Que debido a las circunstancias y hechos ocurridos en las fechas [FECHA], según los cuales [EXPONER LOS HECHOS], la Sección Civil del Tribunal de Instancia de [SEDE] vino a dictar Sentencia en los autos de [LOCALIDAD] acordando la privación de la patria potestad de mi mandante sobre su hijo [NOMBRE Y APELLIDOS], razonando al efecto que

CUARTO.- Que habiendo superado ya mi representado/a la situación que motivó la anterior resolución, tal y como se acredita mediante la prueba que se acompaña, en virtud de la cual resulta que [EXPONER LOS HECHOS], existen motivos suficientes para que éste/a recupere la patria potestad sobre [DESCRIBIR] de la que fue privado.

A los anteriores hechos, son aplicables los siguientes

FUNDAMENTOS DE DERECHO

I. JURISDICCIÓN Y COMPETENCIA

Los arts. 36 y 45 LEC, en relación con lo dispuesto en el art. 85.1º LOPJ, que establecen que corresponde a las secciones civiles de los tribunales de instancia del orden jurisdiccional civil el conocimiento, en esa primera instancia, de todos los asuntos civiles no atribuidos a otros tribunales.

Por su parte, la competencia del Tribunal al cual tengo el honor de dirigirme viene determinada por el art. 769.1 LEC, al ser éste el que en su momento acordó la privación de la patria potestad mediante Sentencia de

II. CAPACIDAD Y LEGITIMACIÓN

La capacidad procesal de mi mandante para ser parte en este procedimiento viene reconocida en los arts. 6.1.1.º y 7.1 LEC, al ser persona física, mayor de edad, en pleno ejercicio de sus derechos civiles.

Asimismo, le corresponde la legitimación activa en virtud de lo dispuesto en el art. 10 LEC.

El Ministerio Fiscal ostenta la misma capacidad y legitimación, reconocida en el art. 6.1.6.º, debiendo intervenir con carácter preceptivo en este procedimiento a tenor de lo dispuesto en el art. 749.2.

III. POSTULACIÓN Y REPRESENTACIÓN

Resulta preceptiva la intervención de Procurador/a y Abogado en este procedimiento, cumpliéndose en este caso lo dispuesto en los arts. 23, 31 y 750 LEC.

IV. PROCEDIMIENTO

La sustanciación de la presente demanda se realizará conforme a los trámites de:

Opción 1.ª: Juicio ordinario (art. 249.2 LEC), si la privación de la patria potestad cuya recuperación se pretende fue adoptada mediante Sentencia dictada en procedimiento seguido por los mismos trámites con ese exclusivo objeto. Se trata de una materia que no viene expresamente establecida en el art. 250 LEC como propia del ámbito del juicio verbal, teniendo además cuantía inestimable.

Opción 2.ª: Mediante demanda de modificación de medidas (art. 775) si la privación de la patria potestad hubiera sido adoptada en procedimiento matrimonial o de menores regulado en los arts. 769 y ss (Capítulo IV, Título I, Libro IV).

Vid. STS de 3 de mayo de 2001, Rec. 962/1996.

V. CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda no está sujeta al previo intento de resolución de controversias en vía no jurisdiccional por tratarse de materia excluida del requisito de procedibilidad de acuerdo con el art. 4.1 II LO 1/2025, entre las cuales se encuentran los conflictos que afecten a derechos y obligaciones que no estén a disposición de las partes, en cuanto la decisión sobre recuperación de la patria potestad solo puede ser tomada por un juez.

VI. FONDO DE LA CUESTIÓN

a) De orden sustantivo-legal

El art. 170, párrafo 2.º, CCiv establece que "Los Tribunales podrán, en beneficio e interés del hijo, acordar la recuperación de la patria potestad cuando hubiere cesado la causa que motivó la privación".

El art. 154 CCiv sobre el contenido, deberes y facultades, de la patria potestad.

En relación con el principio del interés del menor:

Convención de las Naciones Unidas sobre los Derechos del Niño, de 1989, ratificada por España en 1990.

Carta europea de los Derechos del Niño del Parlamento Europeo (Resolución A 3-0172/92, de 8 julio).

Ley Orgánica 1/1996, de Protección Jurídica del Menor.

b) De orden jurisprudencial

La temporalidad de la medida de privación de la patria potestad es puesta de manifiesto, entre otras muchas resoluciones, en SSTS de 23 de julio de 1987, 5 de octubre de 1987, 30 de abril de 1991, 12 de julio de 2004, Rec. 4793/1999; y SSAP León de 15 de septiembre [AÑO]) y 7 de octubre de 1994, o Salamanca de 14 de julio de 2010 .

Y en aplicación de tal previsión general de temporalidad la STS, II, de 20 de diciembre de 1993, Rec. 11961/1992, declara que "tal privación no significa una extinción de aquel derecho-función ya que, como previene el párrafo 2.º del citado art. 170, podrá acordarse en el futuro la recuperación del mismo, siempre en beneficio del menor, acreditadas por el cambio de conducta de la madre la desaparición de las causas que han motivado esta privación".

En definitiva, la privación de la potestad paterna no tiene carácter irreversible, resultando que si la patria potestad es recuperable, tras el cese de la causa que la motivó, la procedencia de la medida en cuestión pasa por la pervivencia de la causa que la determina [STSJ Navarra de 14 de junio de 1995 ].

Atendida la previsión del párrafo 2.º del art. 170 CCiv, únicamente un Tribunal puede acordar la recuperación de la titularidad de la potestad paterna, bien respecto de uno sólo de los progenitores o respecto de ambos, en la hipótesis de que los dos hubieran sido privados de la potestad sobre el hijo (SAP Bizkaia de 18 de diciembre de 2008, Rec. 128/2008), cuando hubiere cesado la causa que motivó la privación, como expresamente subraya la STS de 5 de marzo de 1998, Rec. 506/1994, que, partiendo de la exigencia legal, manifiesta que tal previsión "implica mayor seguridad para el cumplimiento si se priva al progenitor de la patria potestad, dado que, si realmente tiene interés en cumplir sus deberes para con la niña, cumplirá, y de no ser así, parece ajustarse al interés de ésta que no ostente la tan aludida patria potestad".

En el mismo sentido, la SAP Zaragoza de 14 de febrero de 2005, Rec. 470/2004, declara que "[...] Siempre en beneficio e interés del hijo es posible la recuperación de la patria potestad; se requiere en todo caso, además de la cesación de la causa que motivó la privación, una nueva resolución judicial, que la deje sin efecto".

A la exigencia de intervención judicial como requisito legal (ex art. 170 CCiv) para la recuperación del derecho-función en que consiste la potestad paterna en los casos de privación también se refiere la STS, II, de 20 de diciembre de 1993, Rec. 11961/1992, cuando declara que "podrá acordarse en el futuro la recuperación del mismo", imponiendo pues la necesidad de un pronunciamiento judicial al respecto, sin el cual, obviamente, por constituir la intervención judicial una garantía de la efectiva desaparición de los motivos que justificaron la adopción de tan drástica medida, operante siempre en interés y protección del menor, no se podrá entender restablecido el ejercicio de la patria potestad.

VII. COSTAS PROCESALES

El art. 394 LEC, en cuanto establece el criterio objetivo del vencimiento.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que, habiendo por presentado este escrito de demanda, documentos acompañados y escritura de poder cuya devolución reitero, se sirva admitirlos y, en su virtud, tenga por formulada demanda de [TIPO DE PROCEDIMIENTO], contra [PARTE DEMANDADA], con citación del Ministerio Fiscal, para que, previos los trámites de la Ley, en su día se dicte Sentencia por la que estimando la demanda, se acuerde la recuperación de la patria potestad por parte de mi representado sobre su hijo [NOMBRE Y APELLIDOS], con expresa condena en costas a la demandada si se opusiera a dicha pretensión.

Es justicia de hacerse en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a
