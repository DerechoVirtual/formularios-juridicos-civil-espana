---
name: oposicion-ejecucion-no-notificar-saldo-deudor-poliza-civ-1492
description: "Oposición a la ejecución por no notificar el saldo deudor de una póliza mercantil. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Oposición a la ejecución por no notificar el saldo deudor de una póliza mercantil

> Formulario **CIV-1492** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Escrito de oposición a la ejecución de carácter procesal por falta de notificación al ejecutado de la cantidad líquida exigible resultante de la liquidación en póliza de contrato mercantil

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Oposición a la ejecución por no notificar el saldo deudor de una póliza mercantil» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Oposición a la ejecución por no notificar el saldo deudor de una póliza mercantil” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:oposicion-ejecucion-no-notificar-saldo-deudor-poliza-civ-1492`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (4 veces)
- [ ] IMPORTE (4 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] NÚMERO (2 veces)
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] NOMBRE DEL SOLICITANTE
- [ ] Nº DE CLÁUSULA
- [ ] Nº DE DOCUMENTO
- [ ] SEDE

## Normas que cita el formulario

- art. 1467 LEC
- art. 572.2 LEC
- art. 1435 LEC
- art. 573 LEC
- art. 573.1.3.º LEC
- art. 559.1.3.º LEC
- art. 559.2 LEC

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

D./Dña. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD] y D.N.I. número [NÚMERO], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], ante el Tribunal comparezco y como mejor proceda en derecho DIGO:

Que en nombre de mi poderdante me persono en los autos de ejecución seguidos a instancia de [NOMBRE DEL SOLICITANTE] y registrados con el número [NÚMERO], y por medio del presente escrito formulo OPOSICIÓN a la citada ejecución, dentro del plazo concedido al efecto, en virtud de los siguientes,

HECHOS

Negamos los hechos alegados por el ejecutante en su escrito de demanda, en tanto se opongan a los que a continuación se relatan.

PRIMERO.- Por auto de fecha [FECHA] se despachó ejecución contra mi cliente en reclamación de la cantidad de [IMPORTE] euros ( [IMPORTE] €) en concepto de principal e intereses devengados hasta la fecha, más otros [IMPORTE] euros ( [IMPORTE] €) presupuestados provisionalmente para hacer frente a los intereses que, en su caso, puedan devengarse durante la ejecución y las costas de ésta, sirviendo como título al efecto póliza de crédito suscrita entre las partes, e intervenida por Corredor de Comercio colegiado, de fecha [FECHA], auto que le fue notificado el pasado día [FECHA], por lo que el presente escrito se ha presentado dentro del término de diez días concedido al efecto para formular oposición.

SEGUNDO.- Mi patrocinado no está conforme con lo relatado por la ejecutante en su escrito de demanda puesto que no ha sido notificado previamente al ejecutado la cantidad resultante de la liquidación practicada por el acreedor, ni se ha aportado documentación alguna que acredite este hecho.

FUNDAMENTOS DE DERECHO

I.- Negamos que sean de aplicación al presente caso los fundamentos de derecho alegados por el ejecutante.

II.- Establece el art. 559 de nuestra Ley Adjetiva la posibilidad de oposición a la ejecución por defectos procesales y de entre ellos se solicitará la "nulidad radical del despacho de ejecución por no cumplir el documento presentado los requisitos legales exigidos para llevar aparejada la ejecución" (artículo que se correspondería con el antiguo art. 1467 LECiv 1881) y a tenor del art. 572.2 LEC (se correspondería con el art. 1435 LECiv 1881) "también podrá despacharse ejecución por el importe del saldo resultante de operaciones derivadas de contratos formalizados enpóliza intervenida por corredor de comercio colegiado, siempre que se haya pactado en el título que la cantidad exigible en caso de ejecución será la resultante de la liquidación efectuada por el acreedor en la forma convenida por las partes en el propio título ejecutivo. En este caso, sólo se despachará la ejecución si el acreedor acredita haber notificado previamente al ejecutado y al fiador, si lo hubiere, la cantidad exigible resultante de la liquidación".

Siendo determinados en el art. 573 LEC los documentos que han de acompañarse a la demanda ejecutiva por saldo de cuenta, debiendo acompañarse en los casos a que se refiere el apartado segundo del artículo anterior, además del título ejecutivo y de los documentos a que se refiere el art. 550:

1.º El documento o documentos en que se exprese el saldo resultante de la liquidación efectuada por el acreedor, así como el extracto de las partidas de cargo y abono y las correspondientes a la aplicación de intereses que determinan el saldo concreto por el que se pide el despacho de la ejecución.
2.º El documento fehaciente que acredite haberse practicado la liquidación en la forma pactada por las partes en el título ejecutivo.
3.º El documento que acredite haberse notificado al deudor y al fiador, si lo hubiere, la cantidad exigible.

Así, el art. 572.2 LEC traslada a la nueva Ley Procesal los requisitos que contenía el art. 1435 LECiv 1881, y alude a los contratos mercantiles en los que se hubiera convenido que la cantidad exigible en caso de ejecución sea la especificada en la certificación expedida por la entidad acreedora que conste en documento fehaciente que acredite haberse practicado la liquidación en la forma pactada por las partes en el título ejecutivo y que el saldo coincida con el que aparece en la cuenta abierta al deudor. Pero para que sea necesario el pacto de liquidez al que se refiere el precepto, es preciso que en razón de la naturaleza del contrato haya de liquidarse previamente la deuda pendiente.

En este sentido, la conocida STC 14/1992 de 10 de febrero de 1992, sobre la constitucionalidad del penúltimo párrafo del art. 1435 LECiv 1881, ya decía que "el precepto restringe su alcance a aquellos contratos mercantiles que, además de documentarse mediante forma que garantice su autenticidad, implican la existencia de una situación de cuenta corriente entre las partes, único contexto en el que cobra sentido la regulación de operaciones de liquidación y certificación del saldo". Situación de cuenta corriente que se caracteriza por las distintas partidas de cargo y abono que se compensan aisladamente, caso por caso, con posibilidad de exigir en cualquier momento el saldo que resulte, lo que ocurre en la presente litis.

Luego, el título ejecutivo se integrará por dicha póliza, intervenida por Corredor de Comercio colegiado, junto con la certificación de saldo deudor, confeccionada por la entidad acreedora, y el documento fehaciente de que la liquidación se ha realizado en la forma pactada (cláusula [Nº DE CLÁUSULA] de la póliza de crédito) y, finalmente, la notificación del saldo deudor, a fin de cumplir el requisito de procedibilidad; todo lo cual viene exigido con arreglo al pacto de liquidez, y en este caso no resulta acreditado en los documentos aportados con la demanda.

Resulta patente, pues, que la notificación del saldo al ejecutado es requisito ineludible, y debe referirse obviamente al momento en que el acreedor formula su reclamación, momento en que debiera haberse practicado notificación, resultando sorpresivo el despacho ejecutado.

Por otro lado, en cuanto al requisito de la notificación al deudor, y dado que no precisa la forma en que debe hacerse la notificación, las interpretaciones jurisprudenciales son dispares.

La dicción actual del art. 572.2, párrafo segundo, LEC exige claramente que se acredite la recepción de la comunicación, no solo la emisión de la notificación al deudor. Efectivamente la actual legislación, quizás con el fin de salvaguardar la protección del consumidor junto con la seguridad jurídica, exige la acreditación de la notificación, lo cual implica no sólo que se justifique el envío o remisión de la comunicación, sino su recepción por el destinatario. Ello impone que en los casos de comunicación por correo deberá adjuntarse la tarjeta o certificado de correos justificativo de que se ha efectuado la entrega de la notificación; y en caso de fax, burofax o telegrama el documento que acredite la recepción u otro medio análogo. En definitiva, la nueva Ley de Enjuiciamiento Civil parece introducir realmente un cambio en esta materia no sólo en el aspecto literal del precepto, sino sustancialmente al exigir la acreditación de la recepción de la comunicación por el destinatario "ejecutado y al fiador, si lo hubiere, la cantidad exigible resultante de la liquidación".

No obstante, no desconoce esta parte que el criterio de la mayoría de las Audiencias Provinciales considera que: a) la notificación no debe ser formalista, ni "sacramental", pues su única finalidad es dar a conocer al deudor el riesgo inminente de que contra él se plantee una demanda ejecutiva; b) aunque la norma nada dice, parece razonable entender que debe mediar un cierto tiempo entre la notificación del saldo y la presentación de la demanda ejecutiva; c) en principio, sea válido para llevar a cabo la notificación cualquiera de los medios admitidos en Derecho; d)para la notificación el acreedor debe poner una mínima y elemental diligencia, pero no es preciso que realice una "investigación policial", pues no exige que la notificación sea fehaciente; basta con que el medio elegido sea idóneo para que la notificación de la cantidad exigible llegue efectivamente a conocimiento del deudor.

La forma de notificación más frecuente, como en este supuesto, es la realizada mediante telegrama —con acuse de recibo— remitido al domicilio del deudor que figure en la póliza, y en relación a la validez y requisitos a que está sometida la validez de este específico medio de notificación, la doctrina de apelación es contradictoria, si bien la más antigua y extendida dirección jurisprudencial, entiende suficientemente cumplido el requisito del art. 573.1.3.º LEC si el ejecutante acredita que envió el telegrama al domicilio de la póliza.

En el presente supuesto, en cualquier caso, no se aporta documentación alguna que acredite ni siquiera que la notificación fue correctamente intentada en el domicilio pactado en la póliza, puesto que el requerimiento no se libró al domicilio señalado por el deudor en el título que se ejecuta, sin que haya existido cambio de domicilio notificado al acreedor, por lo que concurre motivo de oposición de carácter procesal al amparo del art. 559.1.3.º LEC, por no acreditar la actora haber notificado previamente al ejecutado la cantidad líquida exigible resultante de la liquidación.

III.- En materia de costas procesales, a tenor de lo preceptuado en el art. 559.2, párrafo segundo, LEC deberán ser impuestas al ejecutante.

En virtud de todo lo expuesto,

SUPLICO AL TRIBUNAL:

que tenga por presentado este escrito con sus copias y me tenga por comparecido y parte en la representación que ostento de D./Dña. [NOMBRE Y APELLIDOS] en el expresado procedimiento de ejecución y mandar que se entiendan conmigo las actuaciones que a partir de este momento se realicen, teniendo por formulada en tiempo y forma oposición a la ejecución despachada para que, tras la correspondiente tramitación, y con estimación de la causa de oposición fundada en defecto procesal se dicte auto dejando sin efecto la ejecución despachada, con imposición de las costas al ejecutante.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
