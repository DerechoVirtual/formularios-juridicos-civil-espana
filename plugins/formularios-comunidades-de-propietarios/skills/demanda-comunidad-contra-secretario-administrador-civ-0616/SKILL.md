---
name: demanda-comunidad-contra-secretario-administrador-civ-0616
description: "Demanda de la comunidad contra el secretario-administrador cesado para que entregue la documentación. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de la comunidad contra el secretario-administrador cesado para que entregue la documentación

> Formulario **CIV-0616** del plugin **Comunidades de propietarios** (`formularios-comunidades-de-propietarios`) · Civil › Propiedad horizontal · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario de una comunidad de propietarios, a través de su Presidente, contra el Secretario-Administrador cesado que se niega a entregar la documentación y los efectos de la comunidad (libro de actas, extractos bancarios, justificantes, llaves, etc.), alegando un supuesto derecho de retención por cantidades que dice se le adeudan.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de la comunidad contra el secretario-administrador cesado para que entregue la documentación» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de la comunidad contra el secretario-administrador cesado para que entregue la documentación” para mi caso». También puedes invocarla directamente con `/formularios-comunidades-de-propietarios:demanda-comunidad-contra-secretario-administrador-civ-0616`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-comunidades-de-propietarios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Comunidades de propietarios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº DE DOCUMENTO (8 veces)
- [ ] NOMBRE Y APELLIDOS DEL DEMANDADO/A (6 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] AÑO (3 veces)
- [ ] CALLE (3 veces)
- [ ] Nº (3 veces)
- [ ] CORREO ELECTRÓNICO (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] FECHA (2 veces)
- [ ] MES (2 veces)
- [ ] TELÉFONO (2 veces)
- [ ] COLEGIO
- [ ] DOMICILIO LABORAL
- [ ] DÍA
- [ ] FECHAS
- [ ] NOMBRE DEL NOTARIO
- [ ] NOMBRE Y APELLIDOS DEL LETRADO/A
- [ ] NOMBRE Y APELLIDOS DEL PRESIDENTE/A
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº DE COLEGIADO
- [ ] Nº DE DOCUMENTOS
- [ ] SEDE

## Normas que cita el formulario

- art. 24.1 LEC
- art. 399.1 LEC
- art. 85.1 LOPJ
- art. 50 LEC
- art. 253 LEC
- art. 249.1 LEC
- art. 13.3 LPH
- art. 35 CC
- art. 6.1.1.º LEC
- art. 7.1 LEC
- art. 25 LEC
- art. 23 LEC
- art. 5 Ley Orgánica 1/2025
- art. 1712.2 Código Civil
- art. 1733 Código Civil
- art. 20.e LPH
- art. 1.730 Código Civil
- art. 394 LEC
- art. 24.2 LEC
- art. 155.3 LEC

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

### Avisos de actualización (3) — se aplican en el texto, nunca se copian en el documento

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] QUE POR TURNO CORRESPONDA»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…ma Ley, en aplicación de lo dispuesto en el apartado tercero del art. 249.1 LEC.»: el original remitía al «apartado tercero de dicho precepto»; comprobar que la remisión corresponde al art. 249.1.8.º o 249.2 LEC según la redacción vigente.
- Junto a «…l principio consagrado en el artículo 1733 del Código Civil antes mencionado...»»: comprobar la numeración vigente de los apartados de los arts. 13 y 20 de la Ley de Propiedad Horizontal citados en esta cita jurisprudencial y en el resto del escrito, por las reformas posteriores a la sentencia citada.

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] QUE POR TURNO CORRESPONDA

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, que actúa en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS DEL PRESIDENTE/A], en su condición de Presidente/a de la Comunidad de Propietarios del edificio señalado con el n.º [Nº] de la calle [CALLE] de [LOCALIDAD], representación que acredito mediante escritura de poder otorgada a mi favor (el art. 24.1 LEC prevé tres formas de otorgar el apoderamiento al Procurador),

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— (Si el poder se otorga a través de la sede judicial electrónica).- mediante comparecencia electrónica, a través de la sede judicial electrónica e inscrito en el Registro Electrónico de Apoderamientos Judiciales; y a cuya justificación acompaño certificación de dicho Registro aportada como Documento n.º [Nº DE DOCUMENTO], y que se puede acreditar mediante consulta automatizada orientada al dato, por parte del órgano judicial al cual tengo el honor de dirigirme.

— (Si el poder se otorga mediante comparecencia apud acta).- mediante comparecencia personal apud acta ante el Tribunal Decano de [LOCALIDAD], posteriormente inscrito en el Registro Electrónico de Apoderamientos Judiciales; y a cuya justificación acompaño certificación de dicho Registro aportada como Documento n.º [Nº DE DOCUMENTO], y que se puede acreditar mediante consulta automatizada orientada al dato, por parte del órgano judicial al cual tengo el honor de dirigirme.

— (Si el poder se otorga ante Notario).- mediante escritura de poder otorgada a mi favor, ante el Notario/Notaria [NOMBRE DEL NOTARIO], con Notaría sita en [LOCALIDAD]. El poder se inscribió en el Registro Electrónico de Apoderamientos Judiciales; lo cual justifico mediante certificación de dicho Registro aportada como Documento n.º [Nº DE DOCUMENTO], y que se puede acreditar mediante consulta automatizada orientada al dato, por parte del órgano judicial al cual tengo el honor de dirigirme.

bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS DEL LETRADO/A], abogado/a en ejercicio, con despacho profesional abierto en [DOMICILIO], colegiado n.º [Nº DE COLEGIADO] del Ilustre Colegio de la Abogacía de [COLEGIO], ante el Tribunal comparezco y como mejor en Derecho proceda,

DIGO

Que mediante el presente escrito vengo a formular DEMANDA DE JUICIO ORDINARIO, contra D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO/A], Secretario-Administrador que lo fue de la citada Comunidad, con domicilio, primero, en [DOMICILIO] [OPCIONAL — si ha lugar: ; y segundo, el domicilio laboral en [DOMICILIO LABORAL]]; con email [CORREO ELECTRÓNICO]; y con número de teléfono móvil [TELÉFONO]; en reclamación de la ENTREGA DE LA DOCUMENTACIÓN DE LA FINCA, según se especificará en el cuerpo del escrito y en el suplico, y todo ello de conformidad con los siguientes hechos y fundamentos de derecho.

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa e, incluso, en una eventual fase de ejecución, por medios telemáticos, en términos del art. 399.1 II LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y n.º de teléfono: [CORREO ELECTRÓNICO] / [TELÉFONO].

HECHOS

PRIMERO.- Mi mandante es Presidente/a de la Comunidad de Propietarios del edificio señalado con el n.º [Nº] de la calle [CALLE], según consta en el acta de la Junta de Propietarios que se acompaña como documento n.º [Nº DE DOCUMENTO].

SEGUNDO.- El demandado, D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO/A], ejerció como Secretario-Administrador de esta Comunidad de Propietarios desde [FECHA] hasta el mes de [MES] de [AÑO], en que la citada Comunidad prescindió de sus servicios.

Se acompaña copia del acta como documento n.º [Nº DE DOCUMENTO].

TERCERO.- Cesado en dicha fecha, el Presidente se puso en contacto con D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO/A] para que le hiciera entrega de la documentación de la Comunidad, negándose el demandado a facilitar la misma, so pretexto de la falta de liquidación de determinadas cantidades.

CUARTO.- Finalmente, habiendo resultado infructuosas todas las gestiones amistosas intentadas por mi mandante frente a D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO/A], se requirió al demandado, mediante burofax con certificación de contenido, para que entregara la documentación y efectos de la comunidad que obraban en su poder, con advertencia de la interposición de la presente demanda, y con reserva de los perjuicios que se pudieran acabar ocasionando (documentos números [Nº DE DOCUMENTOS]).

El demandado contestó al citado requerimiento, condicionando su entrega al abono de una indemnización en concepto de daños y perjuicios que en ningún caso se acreditaba (documento n.º [Nº DE DOCUMENTO]).

QUINTO.- La actitud de D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO/A] no está justificada en modo alguno, ya que el demandado debió devolver toda la documentación de la comunidad cuando cesó del cargo que ostentaba, sin que pueda condicionar la entrega de la documentación de la comunidad al pago de una indemnización de daños y perjuicios supuestamente debidos.

SEXTO.- La Comunidad de Propietarios se encuentra privada de la documentación que debe obrar en su poder, lo que impide su normal funcionamiento y el cumplimiento correcto de sus obligaciones con terceros, con los consiguientes perjuicios de los que eventualmente será responsable el demandado, forzando la actual precisión de impetrar tutela judicial para solicitar la condena del demandado a la devolución del Libro de Actas de la Comunidad y demás documentación que obre en su poder propiedad de la misma.

SÉPTIMO.- A los efectos de cumplir el requisito de procedibilidad para la iniciación de la vía jurisdiccional, la parte actora manifiesta que, previamente a la presentación de la presente demanda, se han llevado a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria; incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, mi representado envió un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por el demandado por el mismo medio, [ELEGIR: rechazando el acuerdo / habiendo sido solo posible un acuerdo parcial], viéndonos en la necesidad de acudir a la presente vía judicial, respecto a los extremos de la controversia en los que se mantiene la discrepancia.

Acompaño como documento n.º [Nº DE DOCUMENTO] el requerimiento efectuado y como documento n.º [Nº DE DOCUMENTO] la contestación del demandado.

A los anteriores hechos son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA

Radicando la competencia genérica en el orden civil de la jurisdicción, detenta la competencia objetiva y funcional la Sección Civil del Tribunal de Instancia, por aplicación de lo dispuesto en los arts. 85.1 LOPJ y 45 LEC, y puesto que no está prevenido un fuero preceptivo específico, resulta territorialmente competente el Tribunal a que me dirijo, puesto que es el del partido del lugar donde tiene su domicilio el demandado, que es el fuero general de las personas físicas (art. 50 LEC).

II.- CUANTÍA Y PROCEDIMIENTO

Conforme al art. 253 LEC, no es posible determinar, ni siquiera de manera relativa, la cuantía, atendiendo a la pretensión ejercitada en la presente demanda, sin reclamación de daños y perjuicios, cuya posibilidad se reserva mi mandante. Por todo ello, el procedimiento ajustado a derecho será el del juicio declarativo ordinario regulado en los arts. 399 a 436 de la misma Ley, en aplicación de lo dispuesto en el apartado tercero del art. 249.1 LEC.

III.- LEGITIMACIÓN ACTIVA Y PASIVA

En cuanto a la activa, corresponde a mi mandante, a tenor del art. 13.3 LPH; y en cuanto a la legitimación pasiva, corresponde al demandado, por estar en su poder la documentación que se reclama.

IV.- CAPACIDAD Y REPRESENTACIÓN

Mi mandante es el representante legal de la entidad sin personalidad que es la Comunidad de propietarios del edificio señalado con el n.º [Nº] de la calle [CALLE] de [LOCALIDAD], por lo que, detentando capacidad para ser parte por ministerio de la ley dicha comunidad, la capacidad procesal, o para comparecer en juicio, corresponde a su Presidente (arts. 6.1.5.º y 7.6 LEC).

La Comunidad carece de personalidad, pero corresponde a una entidad compleja que se asemeja a las personas jurídicas civiles conforme al art. 35 CC, más allá de los meros actos de conjunto (STS de 14 de mayo de 1992), que actúa mediante representación cuasiorgánica, en la que el Presidente sustituye formalmente la voluntad de la entidad, en los asuntos que le afectan.

El demandado es persona física, mayor de edad, respecto de la que no consta limitación de ejercicio de derechos civiles, por lo que detenta capacidad para ser parte (art. 6.1.1.º LEC) y capacidad procesal, o de obrar en este concreto juicio (art. 7.1 LEC), siempre que cumpla los oportunos requisitos de postulación para oponerse a la presente demanda.

V.- POSTULACIÓN Y DEFENSA

El actor ha otorgado poder notarial al Procurador/a de los Tribunales que encabeza este escrito, habilitado en el partido del Tribunal, cuya copia auténtica se ha aportado, general para pleitos (art. 25 LEC), siendo redactada y firmada la demanda por el abogado ejerciente colegiado que dirige el asunto y se identifica en el encabezamiento, según resulta preceptivo conforme a los arts. 23 y 31 LEC.

VI.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4.º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VII.- FUNDAMENTOS MATERIALES

Aunque la naturaleza de la relación jurídica que liga al administrador con la Comunidad es una cuestión controvertida, si se trata de un contrato de arrendamiento de servicios o de un mandato, la tesis que prospera conforme a la doctrina mayoritaria consiste en hibridar las categorías, y afirmar que participa de ciertos rasgos del arrendamiento de servicios sobre la figura del contrato de mandato, a fin de caracterizar su condición de mandato sui generis de los arts. 1709 y ss. CC, en razón, como dice la SAP Málaga de 9 de enero de 2006, rec. 792/2005, «principalmente, de la similitud del contenido del artículo 13.7 de la Ley de Propiedad Horizontal —los designados podrán ser removidos de su cargo antes de la expiración del mandato por acuerdo de la Junta de propietarios, convocada en sesión extraordinaria— con los artículos 1732 —el mandato se acaba por su revocación— y 1733, ambos del Código Civil, en el que se hace constar que el mandante puede revocar el mandato a su voluntad y compeler al mandatario a la devolución del documento en que consiste el mandato; en razón a que dentro de la generalidad de los términos en que queda redactado el mencionado artículo 1709, se comprenden dos figuras distintas, el mandato representativo y el mandato de gestión (SSTS 16 febrero 1935 y 8 abril 1991), modalidad esta última que fácilmente puede llegar a confundirse con el arrendamiento de servicios del que se distingue acudiendo a diversos criterios, uno de los cuales es la sustituibilidad, porque no es obligatorio que se encomiende la administración a un ajeno a la comunidad a tenor de lo establecido en el artículo 13, párrafo quinto, de la Ley de Propiedad Horizontal, es decir, sus funciones se ejercen por el presidente de la comunidad si no acuerdan elegir a otras personas para el desempeño de este cargo, que a su vez podrá recaer en una misma persona, y este elemento lo explica la Sentencia del Tribunal Supremo de 14 marzo 1986: "...en orden a la distinción del mandato con el arrendamiento de servicios, es básico el criterio de la sustituibilidad, no confundible con el de la representación, de tal manera que sólo pueden ser objeto posible de mandato aquellos actos en que quepa la sustitución, o sea, los que el que solicita la gestión realizaría normalmente por sí mismo, que pertenecen a la esfera propia de su misma actividad y que nada impide poderlos realizar por medio de otra persona, pues cuando así no es, o lo que es lo mismo, cuando se encomienda a otra persona la prestación de servicios que normalmente no pueden ser realizados ni son de la propia actividad de la persona que los encomienda a otro, que precisamente necesita acudir a él para que lleve a cabo la actividad que aquél no podía utilizar, estaremos en presencia de un arrendamiento de servicios"; y en razón a que las actividades ejecutivas que se recogen en el artículo 20 de la Ley de Propiedad Horizontal vienen a ser meramente accesorias, inherentes e indispensables para el ejercicio de una función gestora característica del mandato, que desempeña no solamente en el ámbito interno de la Comunidad, sino en proyección externa, cuando contrata con terceros y practica gestiones en nombre de su mandante, aunque lo haga en nombre propio, ya que en tal supuesto entraría en juego el artículo 1712.2 del Código Civil, puesto que contrataría sobre cosas propias de la comunidad de propietarios. En este sentido, al igual que ocurre con el cargo de presidente o con el de secretario, la duración del administrador, según el mencionado artículo 13.7 de la Ley de Propiedad Horizontal, durará un año, prorrogable tácitamente por períodos iguales, salvo que los Estatutos de la comunidad de propietarios establezcan otra cosa, no obstante lo cual, cabe también la posibilidad de que el administrador sea removido de su cargo mediante acuerdo adoptado en Junta general extraordinaria convocada al efecto, en observancia al principio consagrado en el artículo 1733 del Código Civil antes mencionado...»

De la referida doctrina se deduce que la relación del Administrador para con la Comunidad es de mandato y no de arrendamiento de servicios o de depósito, por lo que no se le puede facultar para retener documentación; pero por si ello fuese poco, el art. 20.e) LPH establece una expresa excepción a la facultad excepcional de retención, cual es la obligación que tiene de poner a disposición de los comuneros la referida documentación de la comunidad, obrante en su poder por razón del cargo, con lo cual nunca podría retenerla al no tener cobertura legal para ello, pues la puesta a disposición es incompatible con la retención.

De este modo, el Administrador destituido está obligado a entregar al Presidente toda la documentación relacionada con la Comunidad de Propietarios, no pudiendo retenerla en su poder hasta que la Comunidad abone las cantidades que le adeuda, como se pronuncia la SAP Barcelona de 15 de abril de 1999, rec. 381/1998:

«No existiendo derecho alguno del actor de ser reembolsado por razón del mandato que le unía al demandado, aquel no tiene derecho alguno a retener la documentación de la Comunidad en base a lo dispuesto en el art. 1.730 del Código Civil ("El mandatario podrá retener en prenda las cosas que son objeto del mandato hasta que el mandante realice la indemnización y reembolso de que tratan los dos arts. anteriores"), además de que tal documentación no es propiamente objeto del mandato (este es la representación y administración de la comunidad y como tal mandatario "está obligado a dar cuenta de sus operaciones y a abonar al mandante cuanto haya recibido en virtud del mandato, aun cuando lo recibido no se debiera al segundo", según dice el art. 1.720 del Cuerpo legal tantas veces citado)»

En este sentido, el demandado viene afirmando una suerte de derecho de retención de lo requerido hasta que obtenga el pago de la indemnización exigida, lo cual es jurídicamente inadmisible, ya que, de un lado, si no se renovó el cargo en el año [AÑO], esa actuación comunitaria es plenamente legítima, pues el mandato para el que había sido nombrado terminaba en ese momento, y la Comunidad podía decidir, como lo hizo, no volver a reelegir al demandado, careciendo en consecuencia el administrador de derecho a exigir indemnización, pues ésta sólo procede cuando se le cesa sin motivo antes del transcurso del plazo para el que fue nombrado, lo que en este caso no concurre.

En todo caso, la documentación comunitaria es propiedad del inmueble y sólo está depositada de forma temporal y provisional en el Secretario-Administrador, a quien siempre se le puede exigir, incluso aunque no estuviera cesado.

Por todo ello, se realiza un último intento para recuperar la documentación comunitaria, reservándonos la acción para reclamar los daños y perjuicios que se irrogarán, sin lugar a dudas, en el caso de que la negativa se mantenga, u otras acciones que pudieran corresponder.

VIII.- COSTAS

El total vencimiento de la parte demandada, unido a su temeridad y mala fe, determina, según el art. 394 LEC, que ésta deba satisfacer todas las costas del presente procedimiento.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito, junto con los documentos que se acompañan, se admita la demanda y se emplace a la parte demandada, siguiendo la correspondiente tramitación procesal, a fin de que en su día se dicte sentencia condenando a D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO/A] a la ENTREGA INMEDIATA DE TODA LA DOCUMENTACIÓN DE LA COMUNIDAD, y en especial la siguiente: a) Libro de actas; b) Extractos bancarios; c) Justificantes de ingresos y gastos; d) Cuanta documentación disponga en relación a la comunidad (contratos, pólizas de seguro, listado de propietarios con domiciliaciones bancarias, relación de pagos pendientes y relación de deudores, etc.); e) Cualesquiera efectos que posea de la comunidad (llaves, talonarios de cheques, etc.); y f) Cualquier otra documentación y/o efectos que obre en su poder, así como al pago de las costas procesales causadas.

Es justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a Firma del Procurador/a

NOTAS DE AYUDA

(1) Acreditación del poder: todos los poderes deben estar inscritos en el Registro Electrónico de Apoderamientos Judiciales (REAJ). Para su acreditación basta, en principio, la consulta automatizada orientada al dato de dicho Registro, que está a disposición de cualquier Letrado de la Administración de Justicia. Dado que el art. 24.2 LEC configura la certificación de la inscripción como vía subsidiaria, para el caso de que el sistema no permita aquella consulta, el modelo prevé que se acompañe certificación electrónica, que el sistema permite emitir a quien inscribe el poder.

(2) El art. 155.3 LEC permite expresar varios domicilios del demandado (el que aparezca en el padrón municipal o conste oficialmente a estos efectos; el que aparezca en registro oficial o en publicaciones de colegios profesionales, si se trata de empresas o personas colegiadas; donde desarrolle su actividad profesional o laboral no ocasional; si es empresa mercantil, el domicilio de cualquiera de sus administradores, gerentes o apoderados; o, si es asociación que consta en registro oficial, el domicilio del presidente, miembro o gestor de la Junta correspondiente). Cuando se señalen varios, se indicará el orden a seguir para la notificación, con vistas al éxito de la misma.

(3) El art. 155.3 LEC configura una obligación adicional del demandante, consistente en aportar cuantos datos sean de utilidad para localizar al demandado: número de identificación fiscal o de extranjeros, n.º de teléfono, dirección de correo electrónico o similares.
