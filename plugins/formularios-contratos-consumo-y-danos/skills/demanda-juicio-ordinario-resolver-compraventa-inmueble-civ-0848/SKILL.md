---
name: demanda-juicio-ordinario-resolver-compraventa-inmueble-civ-0848
description: "Demanda de juicio ordinario para resolver una compraventa de inmueble por impago e indemnizar daños. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio ordinario para resolver una compraventa de inmueble por impago e indemnizar daños

> Formulario **CIV-0848** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Demanda, dirigida al Tribunal de Instancia que por turno corresponda, de juicio ordinario sobre resolución de contrato de compraventa de bien inmueble por impago del precio y condena a pago de cantidad en concepto de daños y perjuicios por existencia de una cláusula penal en el contrato.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio ordinario para resolver una compraventa de inmueble por impago e indemnizar daños» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio ordinario para resolver una compraventa de inmueble por impago e indemnizar daños” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-juicio-ordinario-resolver-compraventa-inmueble-civ-0848`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (8 veces)
- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] NÚMERO (6 veces)
- [ ] FECHA (5 veces)
- [ ] IMPORTE EN CIFRA (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] Nº (4 veces)
- [ ] DOMICILIO (2 veces)
- [ ] Nº DE CLÁUSULA (2 veces)
- [ ] CORREO ELECTRÓNICO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] ENTIDAD BANCARIA
- [ ] FECHAS
- [ ] LUGAR
- [ ] MES
- [ ] Nº DE COLEGIADO/A
- [ ] Nº DE DOCUMENTO
- [ ] SEDE
- [ ] TELÉFONO

## Normas que cita el formulario

- art. 24.1 LEC
- art. 399.1 LEC
- art. 21 LOPJ
- art. 36 LEC
- art. 85 LOPJ
- art. 45 LEC
- art. 50 LEC
- art. 7.1 LEC
- art. 10 LEC
- art. 253.1 LEC
- art. 252.2.ª LEC
- art. 251.1.ª LEC
- art. 5 Ley Orgánica 1/2025
- art. 1.504 CC
- art. 1.124 CC
- art. 1.152 CC
- art. 394.1 LEC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.R.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.R.C.

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales y de la entidad [DENOMINACIÓN SOCIAL], con domicilio social en [LOCALIDAD], representación que acredito mediante escritura de poder otorgada a mi favor (existen tres posibilidades para otorgar el apoderamiento al Procurador de los Tribunales, conforme dispone el art. 24.1 LEC)

[OPCIONAL — opción en función de cómo se haya otorgado el poder]

[ELEGIR UNA OPCIÓN: Si el poder se otorga a través de la sede judicial electrónica / Si el poder se otorga mediante comparecencia apud acta / Si el poder se otorga ante Notario]

bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS], abogado/a en ejercicio, con despacho profesional abierto en [LOCALIDAD], colegiado nº [Nº DE COLEGIADO/A] del Ilustre Colegio de la Abogacía de [LOCALIDAD], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que mediante el presente escrito vengo a formular DEMANDA DE JUICIO ORDINARIO sobre resolución de contrato y condena a pago de cantidad, contra D./Dña. [NOMBRE Y APELLIDOS], con domicilio, primero en [DOMICILIO]; y segundo, el domicilio laboral en [DOMICILIO]); con email [CORREO ELECTRÓNICO]; y con número de teléfono móvil [TELÉFONO]; todo ello de conformidad con los hechos y fundamentos de derecho que se especificarán.

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa, e, incluso, en una eventual fase de ejecución por medios telemáticos, en términos del art. 399.1 II LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y nº [Nº] de teléfono:

HECHOS

PRIMERO.- Mi mandante es una sociedad de responsabilidad limitada constituida por tiempo indefinido en escritura autorizada por el Notario de esta localidad el día [FECHA], número [NÚMERO] de su protocolo, general corriente, cuyos datos registrales constan en la escritura de poder que acredita la representación procesal, y por el documento n.º 1 que se acompaña a la presente demanda, en que consta la cédula con CIF expedida por la Agencia Tributaria.

SEGUNDO.- Mi mandante y el demandado D./Dña. [NOMBRE Y APELLIDOS], suscribieron en documento privado de fecha [FECHA], que se aporta como documento n.º [Nº], la compraventa del inmueble, cuya descripción se transcribe a continuación:

« descripción, linderos, referencia registral» [DESCRIPCIÓN DEL BIEN].

TERCERO.- En el citado contrato quedó fijado en la cláusula [Nº DE CLÁUSULA] que el precio de la compraventa era de [IMPORTE] euros ([IMPORTE EN CIFRA] €), que se aplazaba mediante abonos mensuales de [IMPORTE] euros ([IMPORTE EN CIFRA] €), después de un inicial pago alzado de otros [IMPORTE] euros ([IMPORTE EN CIFRA] €). En la cláusula [Nº DE CLÁUSULA], también se recoge la forma de pago y se relacionan los recibos para su presentación al cobro en la entidad bancaria [ENTIDAD BANCARIA], en los que se documentó el precio aplazado.

CUARTO.- Mi mandante y el demandado, formalizaron en escritura pública ante el Notario de esta localidad, D./Dña. [NOMBRE Y APELLIDOS], el día [FECHA], bajo el número [NÚMERO] de su protocolo la citada compraventa, si bien la posesión de la finca ya la tenía con anterioridad el demandado desde la firma del contrato privado.

Se acompaña como documento n.º [NÚMERO] copia simple del referido instrumento público.

QUINTO.- Es el caso que, salvo la entrega inicial del precio, ninguno de los plazos fijados para el pago pleno, e instrumentados en recibos cuya domiciliación en cuenta de entidad bancaria suscribió el demandado, se han hecho efectivos.

Se acompañan los recibos presentados al cobro de meses de [MES], con el cajetín puesto por la entidad domiciliataria de incorriencia, como documento n.º [NÚMERO].

SEXTO.- La parte actora manifiesta que, previamente a la presentación de la presente demanda, se han llevado a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad, y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria; incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución (documentos números [Nº DE DOCUMENTO]).

Finalmente, con fecha [FECHA], después de agotados los intentos de solución pacífica del asunto, y consolidada la certeza de que el demandado no tenía voluntad de pago, se practicó requerimiento notarial ante D./Dña. [NOMBRE Y APELLIDOS], que lleva n.º [NÚMERO] de su protocolo general corriente, al cual el demandado no respondió, y en el que, además de exigir la devolución de la finca, por resolución debida al incumplimiento radical del pago del precio, se indicaba la aplicación de la entrega verificada de [IMPORTE] euros, como arras penales, en indemnización de daños y perjuicios, tan elementales como los derivados de estar privada mi mandante de su inmueble durante [Nº] meses.

Se acompaña el acta pública de requerimiento como documento n.º [NÚMERO].

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA.

Los arts. 21 y 22 LOPJ y art. 36 LEC atribuyen con carácter general a la jurisdicción de nuestro Estado y al orden civil, el conocimiento de una materia como la presente.

El art. 85 LOPJ y el art. 45 LEC, designan a las secciones civiles de los tribunales de instancia, como los órganos con la competencia específica objetiva y funcional para resolver estos pleitos.

Finalmente, el art 50 LEC fija que la competencia territorial general, en el caso de personas físicas, será del órgano del lugar de su domicilio.

II.- TRAMITACIÓN.

En aplicación de los arts. 248.3, 249.2 y 251 LEC, y en atención a la cuantía reclamada que asciende a [IMPORTE] EUROS, este pleito se tramitará por las normas de proceso declarativo llamado Juicio Ordinario.

III.- CAPACIDAD.

Conforme a los arts. 6.1.1.º y 3.º LEC tienen capacidad para ser parte las personas físicas y las jurídicas, y a tenor de los arts. 7.1 y 4 LEC, detentan capacidad de obrar procesal, aquéllas mayores de edad no incapacitadas, y éstas constituidas legalmente a través de sus representantes necesarios.

IV.- LEGITIMACIÓN.

E1 art. 10 LEC legitima para comparecer y actuar en juicio, a los titulares de la relación jurídica o del objeto litigioso. En el caso de autos, la entidad demandante y el demandado, son los sujetos titulares del contrato cuyo incumplimiento arraiga la acción resolutoria que se ejerce, existiendo, pues, legitimación directa ordinaria. La demandante es titular del crédito derivado del reintegro de la finca vendida y de los daños y perjuicios irrogados, habiendo cumplido su prestación. Está legitimado pasivamente el demandado por ser el comprador, deudor del pago del precio incumplido.

V.- POSTULACIÓN.

En aplicación de los arts. 23.1 y 31.1 LEC, las partes comparecerán representadas por Procurador/a de los Tribunales y asistidas por Letrado en ejercicio, ambos habilitados ante el Tribunal.

VI.- CUANTÍA.

Cumpliendo la exigencia del art. 253.1 LEC, se cifra la cuantía de la demanda en la cantidad de [IMPORTE] euros ([IMPORTE EN CIFRA] €).

Dicha cifra se obtiene de agregar, conforme al art. 252.2.ª LEC, al valor del inmueble que se vendiera, con arreglo a su valor catastral de [IMPORTE] euros (art. 251.2.ª párrafo 2.º LEC), dado que se pide la condena a su devolución, a la que se pide como indemnización por incumplimiento, de [IMPORTE] euros (art. 251.1.ª LEC).

VII.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VIII.- FUNDAMENTO MATERIAL

Facultad resolutoria especial.

La base de la demanda se constituye por el precepto contenido en el art. 1.504 CCiv, éste que resulta de mayor severidad que el genérico precepto sobre resolución en obligaciones recíprocas del art. 1.124, y determina la resolución, sin admitir apreciación de causas justificadas de incumplimiento y prohibiendo en forma expresa y absoluta la concesión de un nuevo término para cumplir la obligación.

En supuesto de impago del precio, como el del asunto, el comprador puede recurrir a la norma general del art. 1.124 CCiv, y ante la exigencia de la resolución, pedir sin duda como criterio de equidad que flexibiliza el automatismo que pueda cumplir o pagar aún después de expirado el término, o tras el vencimiento ya operado.

Se haya o no pactado esa posibilidad de pago tardío, en cierto modo, persiste en tanto en cuanto no se haya requerido en forma judicial o notarialmente a dicho comprador, si bien tras el requerimiento, no es posible conceder nuevo término o viabilizar cualquier otro pago "tardío".

Ni el requerimiento ni la eventualidad resolutoria, en materia de venta de inmuebles, para el caso de impago del precio, no precisan que previamente así lo hayan acogido las partes, puesto que opera por ministerio de la ley, ex art. 1.504 CCiv, sin que en caso alguno, en la venta de inmuebles quepa la discrecionalidad judicial de señalar nuevo plazo, que permite el penúltimo párrafo de susodicho art. 1.124 (STS de 26 de enero de 1996, Rec. 2126/1992).

De ello se deduce que en dicho artículo se configuran dos requisitos para que el mismo sea de aplicación, con arreglo a la jurisprudencia (SSTS de 7 de julio de 1998, Rec. 1149/1998, 28 de enero de 1999, Rec. 2348/1994, 25 de junio de 1999, Rec. 3609/1994, y 23 de julio de 1999, Rec. 3646/1994), a saber:

1.º) que por parte del comprador se haya producido un incumplimiento, no pudiendo ser otro que la falta de pago de algunas de las cantidades a las que en virtud del contrato de compraventa viene obligado; y
2.º) que se produzca por parte del vendedor una declaración expresa de su voluntad resolutoria.

Ambos requisitos concurren en el caso de autos ya que la demandada ha impagado todos los recibos girados, como resulta de la documental aportada y, por otra parte, mi representada notificó al demandado mediante requerimiento notarial su expresa voluntad de resolución en el domicilio de aquél.

Indemnización de daños y perjuicios.

En la estipulación [Nº] de la escritura de compraventa, así como el la cláusula del contrato privado, ambas partes, haciendo ejercicio de la autonomía privada en la contratación, estipularon que en el supuesto de resolución del contrato de compraventa la vendedora podría retener para sí las cantidades percibidas hasta ese momento en concepto de daños y perjuicios, como cláusula penal o pena convencional, por lo que haciendo uso de tal convención las cantidades entregadas hasta el momento de la resolución por la compradora han quedado retenidas por mi mandante, lo que fue puesto en conocimiento de la compradora en el requerimiento notarial.

Es aplicable el art. 1.152 CCiv, que establece que ‘en las obligaciones con cláusula penal, la pena sustituirá a la indemnización de daños y al abono de intereses en caso de falta de cumplimiento, si otra cosa no se hubiere pactado’, y la doctrina al respecto de las arras penales [STS de 17 de febrero de 1982].

IX.- COSTAS.

Las costas del presente procedimiento deberán ser impuestas a la parte demandada, con arreglo al art. 394.1 LEC, que recoge el principio objetivo del vencimiento en la materia por lo que respecta a los juicios declarativos en su primera instancia.

En atención a todo lo anterior es por lo que,

AL TRIBUNAL SUPLICO

que, teniendo por presentado este escrito de demanda junto con los documentos que se acompañan y copias simples de todo ello, se sirva admitir uno y otros, se me tenga por comparecida y parte, en la representación que ostento y con carácter de demandante, entendiéndose conmigo las ulteriores sucesivas diligencias, y por promovido juicio ordinario contra D./Dña. [NOMBRE Y APELLIDOS], se le confiera traslado emplazándole en legal forma de comparecencia, y eventual contestación y seguido que sea el oportuno procedimiento, en su día, se dicte sentencia en la que:

1. Se declare resuelto el contrato de compraventa concertado entre mi mandante y el demandado respecto del bien inmueble que se determina en el cuerpo de este escrito.
2. Se declare el reintegro de prestaciones, de modo que mi mandante permanezca propietaria del bien inmueble, pero sea indemnizada con la totalidad de las cantidades entregadas por el demandado hasta el momento del requerimiento, como pena convencional por el incumplimiento.
3. Se condene al demandado a estar y pasar por las anteriores declaraciones, y a que entregue de inmediato la posesión del inmueble a la sociedad actora.
4. Se dirija mandamiento al Registro de la Propiedad de [LOCALIDAD], que ordene reinscribir a nombre de mi mandante como dueño en pleno dominio la finca objeto del presente juicio.
5. Se condene al demandado al pago de las costas procesales.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a
