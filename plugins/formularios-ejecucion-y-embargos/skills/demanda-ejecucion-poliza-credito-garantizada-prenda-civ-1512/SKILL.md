---
name: demanda-ejecucion-poliza-credito-garantizada-prenda-civ-1512
description: "Demanda de ejecución de póliza de crédito garantizada con prenda de acciones cotizadas. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de ejecución de póliza de crédito garantizada con prenda de acciones cotizadas

> Formulario **CIV-1512** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Demanda ejecutiva para exigir el pago de una deuda derivada de una póliza de crédito con garantía pignoraticia (acciones cotizadas en Bolsa).

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de ejecución de póliza de crédito garantizada con prenda de acciones cotizadas» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de ejecución de póliza de crédito garantizada con prenda de acciones cotizadas” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:demanda-ejecucion-poliza-credito-garantizada-prenda-civ-1512`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (11 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] Nº (5 veces)
- [ ] DENOMINACIÓN SOCIAL (3 veces)
- [ ] FECHA (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] CALLE
- [ ] DESCRIBIR
- [ ] LUGAR
- [ ] Nº DE CLÁUSULA
- [ ] PETICIÓN
- [ ] PORCENTAJE
- [ ] SEDE
- [ ] ÍNDICE DE REFERENCIA

## Normas que cita el formulario

- art. 681 LEC
- art. 684.1.4.º LEC
- art. 85.1 LOPJ
- art. 539.1 LEC
- art. 685.2 LEC
- art. 550 LEC
- art. 573 LEC
- art. 1.863 Código Civil
- art. 320 Código de Comercio
- art. 681.1 LEC
- art. 687 LEC
- art. 694 LEC

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.R.C.

D./Dña. [NOMBRE Y APELLIDOS] Procurador/a. de lo tribunales, en nombre y representación de la entidad [DENOMINACIÓN SOCIAL], como acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], ante el Tribunal comparezco y, como mejor proceda en derecho, DIGO:

Que en dicha representación, interpongo DEMANDA EJECUTIVA para exigir el pago de una deuda derivada de una póliza de crédito con garantía pignoraticia, contra D./Dña. [NOMBRE Y APELLIDOS], domiciliado en la calle [CALLE], de [LOCALIDAD]. La demanda se dirige contra el mismo, en su calidad de deudor, según se desprende del título ejecutivo indicado, y que luego se concretará, en reclamación de la cantidad de [IMPORTE] euros como principal, [IMPORTE] euros por intereses moratorios vencidos, más los intereses que puedan devengarse durante la ejecución y las costas del presente procedimiento. Todo ello en virtud de lo dispuesto en los artículos 681 y concordantes de la LEC y en los siguientes:

HECHOS:

PRIMERO.- El [FECHA], mi mandante [NOMBRE DEL REPRESENTADO/A] suscribió con el demandado [NOMBRE Y APELLIDOS] una póliza de crédito intervenida por el Notario D./Dña. [NOMBRE Y APELLIDOS] en tal fecha. En virtud de tal póliza resultó abierta una cuenta corriente de crédito a favor del demandado D./Dña. [NOMBRE Y APELLIDOS] por un importe de [IMPORTE] euros, de la cual podía libremente disponer en los términos convenidos en tal contrato.

Se acompañan como documentos nºy, ejemplar de la póliza de crédito en cuestión, así como certificación del Notario interviniente, que acredita la conformidad de la póliza con lo resultante de los libros de dicho fedatario.

SEGUNDO.- La mencionada póliza de crédito fue pactada, según resulta de su condicionado general, por el importe de principal citado y con un interés variable revisable anualmente del tipo publicado por [ÍNDICE DE REFERENCIA] incrementado en un [PORCENTAJE] %, además de las siguientes condiciones:

Interés de demora:

Plazo de devolución:

En garantía de la obligación de devolución del principal prestado y de los intereses remuneratorios por un total de [IMPORTE] euros (principal por importe de [IMPORTE] euros, e intereses remuneratorios de [Nº] años por importe de [IMPORTE] euros), se constituyó garantía pignoraticia sobre [DESCRIBIR] acciones de la entidad [DENOMINACIÓN SOCIAL], admitidas a cotización en las bolsas de valores de [LOCALIDAD]. Dichas acciones son de titularidad del deudor, están numeradas del [Nº] al [Nº], y se encuentra depositadas en la misma entidad que las emite.

El número de las mencionadas acciones fue concretado, tomando como referencia su valor de cotización el día de constitución de la prenda, computando un % del mismo, para compensar las eventuales oscilaciones que tal valor pudiera sufrir en bolsa. Asimismo, para el caso de que el valor de las acciones se redujera por debajo del % del valor de cotización, se fijaba un deber de reposición por parte del pignorante, que consistía en extender las garantías a un número de acciones adicional, determinado conforme a una fórmula matemática acordada en el contrato de mutuo acuerdo. Por último, se pactó expresamente que la entidad bancaria podía optar, en el caso de ejecución por apropiarse de las acciones pignoradas, o solicitar su realización.

TERCERO.- Vencida la póliza por impago de las cuotas pactadas, a fecha de presentación del presente escrito rector, el demandado adeuda a mi mandante la cantidad de [IMPORTE] euros en concepto de principal, así como [IMPORTE] euros como intereses pactados y vencidos a la fecha de la liquidación efectuada. Tales cantidades han sido calculadas de conformidad con lo acordado en la póliza y de conformidad con las siguientes operaciones:

Al respecto se acompañan los siguientes documentos:

— Como documento nº [Nº], el extracto de cuenta corriente de crédito de la que resulta el historial de disposiciones y abonos y cargos correspondientes a intereses liquidados, según lo previsto en la cláusula [Nº DE CLÁUSULA] de la póliza.
— Como documento nº [Nº DE DOCUMENTO] la certificación librada por mi principal, verificada y legitimada por Notario, en la que consta haberse practicado la liquidación en la forma fijada en la póliza cuya ejecución se pretende y, asimismo, que el saldo resultante coincide con el que aparece deudor en la cuenta abierta al ejecutado.

CUARTO.- Se ha intentado, infructuosamente, el cobro de las cantidades adeudadas por mi mandante, sin que haya quedado otra alternativa que solicitar el auxilio judicial mediante la interposición de la presente demanda ejecutiva conforme al título ejecutivo, el cual se adjunta en unión de los restantes documentos allí exigidos.

A los anteriores hechos les son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO:

I.- COMPETENCIA.

Conforme al art. 684.1.4.º de la LEC, en relación con lo dispuesto en el art. 85.1º LOPJ, para conocer de los procedimientos de ejecución sobre bienes pignorados será competente el Tribunal de Instancia al que las partes se hubieren sometido en la escritura o póliza de constitución de la garantía y, en su defecto, el del lugar en que los bienes se hallen, estén almacenados o se entiendan depositados

En el presente caso, ambos lugares coinciden, al haberse pactado expresamente el sometimiento a los tribunales del partido judicial del Tribunal al que me dirijo, siendo dicho partido aquel en donde se encuentra domiciliada la mencionada entidad depositaria.

II.- POSTULACIÓN.

Es preceptiva la intervención de abogado y procurador en este procedimiento, tal y como prescribe el art. 539.1 de la LEC.

III.- TÍTULO DE EJECUCIÓN.

El art. 685.2 de la LEC dispone que a la demanda se acompañará el título o títulos de crédito, revestidos de los requisitos que esta Ley exige para el despacho de la ejecución. Por lo tanto, de acuerdo con el artículo 517.2.4.º de la Ley Procesal, en relación con lo dispuesto en el artículo 17.1 párrafo 4.º de la Ley del Notariado, (el cual señala que a los efectos del mismo se considerará título ejecutivo aquella copia que el interesado solicite que se expida con tal carácter), se acompaña copia de la escritura de préstamo con garantía pignoraticia expedida con las características indicadas en el artículo 233 del Reglamento Notarial, en cumplimiento de lo legalmente establecido.

IV.- REQUISITOS FORMALES.

La escritura de constitución de la prenda determina el precio en que los interesados tasan las acciones pignoradas, por importe de [IMPORTE] euros.

Además, aparte de acompañar a la demanda el título ejecutivo, se aportan los demás documentos a que se refieren el art. 550 LEC (poder) y, en sus respectivos casos, los artículos 573 y 574 de la LEC (liquidación de la deuda).

V.- ASPECTOS SUSTANTIVOS.

La prenda sujeta directa e inmediatamente los bienes sobre los que se constituye, al cumplimiento de la obligación para cuya seguridad fue constituida; confiriendo derecho al acreedor pignoraticio para retener la cosa en su poder o en el de la tercera persona a quien hubiese sido entregada, hasta que se le pague el crédito.

De esta forma, conforme a la regulación clásica del derecho de prenda (artículos 1.863 y siguientes del Código Civil y artículos 320 y siguientes del Código de Comercio) mi mandante tiene derecho a retener la cosa en su poder, hacer suyos los intereses que se generen para compensar aquellos que se le deben, o incluso, imputar el exceso al capital o principal. Y, en caso de impago de la obligación garantizada, el acreedor podrá vender el bien pignorado. La venta se realizará conforme a las disposiciones contempladas en la Ley de Enjuiciamiento Civil, o a través del proceso extrajudicial, y para el caso (aquí concurrente) de que la prenda consistiere en valores cotizables, se venderán en la forma prevenida por el Código de Comercio, notificando a los organismos rectores del correspondiente mercado de valores.

Si bien, el legislador actual ha mejorado las posibilidades de ejecución del bien o bienes objeto de la prenda, configurando la posibilidad específica de apropiarse de aquel o aquellos. Así, el Real Decreto-ley 5/2005, de 11 marzo, de reformas urgentes para el impulso a la productividad y para la mejora de la contratación pública, el cual, al regular el régimen de los acuerdos de compensación contractual y de las garantías financieras, admite de forma expresa la licitud de la apropiación en el primer párrafo del artículo 11.1 :"Se considera como supuesto de ejecución un incumplimiento de obligaciones o cualquier hecho pactado entre las partes que en caso de producirse permita al beneficiario de la garantía, en virtud del acuerdo de garantía o de la Ley, realizar o apropiarse del objeto de dicha garantía; o que produce la aplicación de una cláusula de liquidación por compensación exigible anticipadamente, si tal cláusula estuviera prevista por el acuerdo de garantía". Opción que contempla el contrato que unió a las partes (en su estipulación nº [NÚMERO]), y cuya viabilidad queda confirmada por la STS 24 de junio de 2010, rec. 1798/2006.

VI.- SOBRE EJECUCIÓN DE BIENES PIGNORADOS.

El artículo 681.1 de la LEC determina que la acción para exigir el pago de deudas garantizadas por prenda podrá ejercitarse directamente contra los bienes pignorados, sujetando su ejercicio a lo dispuesto para la ejecución dineraria, con las especialidades que se establecen en los artículos 681 a 698 de la citada ley procesal. De esta forma, procederá que se requiera de pago al deudor, y, para el supuesto de que no abone la deuda que se ejecuta, se proceda por [PETICIÓN], mediante decreto del Letrado de la Administración de Justicia, a depositar las acciones pignoradas en poder de mi mandante, en virtud de lo dispuesto en el art. 687 LEC.

Como se ha dicho anteriormente, en el caso de que la deuda no resulte abonada, mi mandante podrá optar entre que las acciones le sean adjudicadas en pago de la deuda, a partir de la valoración fijada en la escritura o póliza de constitución de la prenda en su día firmada por las partes. O bien que, también conforme a dicha valoración; se proceda a su realización por el procedimiento de apremio, de conformidad con lo dispuesto en los artículos 694 y 635 LEC, oficiándose al Director General de la Sociedad Rectora de la Bolsa de [LOCALIDAD], para que proceda a la venta de las acciones en cuestión, e ingrese su importe en la cuenta de depósitos y consignaciones del Tribunal.

Por lo expuesto

SUPLICO AL TRIBUNAL

que se tenga por presentado este escrito junto con los documentos que se acompañan y, admitiéndolos, se me tenga por comparecido y parte en nombre y representación de [NOMBRE DEL REPRESENTADO/A], entendiéndose conmigo las sucesivas diligencias, y por promovido procedimiento de ejecución de garantía pignoraticia contra D./Dña. [NOMBRE Y APELLIDOS], respecto de las [Nº] acciones sometidas a cotización en bolsa de valores pignoradas con nº [NÚMERO] al [DENOMINACIÓN SOCIAL]. Y ello, con objeto de que, tras requerimiento de pago y demás trámites pertinentes, se acuerde por el Letrado de la Administración de Justicia el depósito de las acciones pignoradas en poder de mi mandante, para que, posteriormente, se le adjudiquen, o se realicen, y con el producto que se obtenga con su realización (o con los frutos derivados del depósito), se haga pago a mi poderdante de la cantidad de [IMPORTE] euros en concepto de principal, [IMPORTE] euros por intereses devengados hasta la fecha de la liquidación de la deuda, más los intereses que a los tipos pactados se devenguen computados desde el día [FECHA] hasta que se practique la liquidación definitiva, así como las costas de este procedimiento que deberán ser sufragadas por el demandado.

PRIMER OTROSÍ DIGO: No presentándose con este escrito acta notarial que acredite haberse requerido de pago al ejecutado con al menos diez días de antelación, a que se refiere el artículo 686 en relación con el 581.2 de la LEC

SE SOLICITA que en el mismo auto en que se despache ejecución se mande que se requiera de pago al deudor en el domicilio fijado en la póliza de crédito pactada.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
