---
name: demanda-juicio-verbal-resolver-arrendamiento-bienes-civ-0781
description: "Demanda de juicio verbal para resolver un arrendamiento de bienes muebles. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio verbal para resolver un arrendamiento de bienes muebles

> Formulario **CIV-0781** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio verbal para resolver un arrendamiento de bienes muebles» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio verbal para resolver un arrendamiento de bienes muebles” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-juicio-verbal-resolver-arrendamiento-bienes-civ-0781`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] Nº DE DOCUMENTO (6 veces)
- [ ] FECHA (4 veces)
- [ ] IMPORTE (4 veces)
- [ ] MARCA/MODELO (4 veces)
- [ ] DESCRIPCIÓN DEL VEHÍCULO (3 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] MATRÍCULA (2 veces)
- [ ] MES (2 veces)
- [ ] MESES ADEUDADOS (2 veces)
- [ ] PLAZO (2 veces)
- [ ] AÑO
- [ ] CALLE
- [ ] DENOMINACIÓN SOCIAL
- [ ] DÍA
- [ ] LUGAR
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] Nº
- [ ] Nº DE BASTIDOR
- [ ] Nº DE CLÁUSULA
- [ ] PROVINCIA
- [ ] SEDE

## Normas que cita el formulario

- art. 250 LEC
- art. 50.1 LEC
- art. 85.1 LOPJ
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 1543 Código Civil
- art. 394 LEC
- art. 441.4 LEC

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

Don [NOMBRE Y APELLIDOS] Procurador de los Tribunales, en nombre y representación de la entidad [DENOMINACIÓN SOCIAL], con domicilio social en la calle [CALLE], de la localidad de [LOCALIDAD], provincia de [PROVINCIA], según acredito con la copia de copia electrónica del poder notarial de representación informática (o digitalizada) que se acompaña y cuya devolución solicito previa unión de testimonio a los autos, comparezco ante este Tribunal y DIGO:

Que en la representación que ostento formulo demanda de juicio verbal con la pretensión de que el Tribunal resuelva, con carácter sumario, sobre el incumplimiento de un contrato de arrendamiento de bienes muebles, al amparo del número 11º del apartado primero del art. 250 de la LEC, contra Don [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], la cual baso en los siguientes:

HECHOS

PRIMERO.- Mi representado, en fecha [FECHA], concertó con el demandado D. contrato de arrendamiento del camión de su propiedad [DESCRIPCIÓN DEL VEHÍCULO] marca [MARCA/MODELO] modelo [MARCA/MODELO] nº [Nº] de identificación [Nº DE BASTIDOR], matrícula [MATRÍCULA] por un periodo de [PLAZO] y pactándose una renta de [IMPORTE] euros mensuales, que debía abonarse por meses anticipados.

Este contrato fue formalizado ante el Notario de esta ciudad D. [NOMBRE Y APELLIDOS], en fecha [FECHA] acompañando copia auténtica del referido contrato.

SEGUNDO.- En la misma fecha de celebración del contrato mi mandante efectuó la entrega del vehículo a la parte demandada para su uso como arrendatario, quien cumplió con sus obligaciones hasta que el pasado mes de [MES] dejó de satisfacer la renta convenida, incumplimiento que se ha mantenido hasta la fecha de interposición de esta demanda, estando en adeudar un total de [IMPORTE] euros (acompaño como documentos números [Nº DE DOCUMENTO] recibos de renta adeudados correspondientes a los meses de [MESES ADEUDADOS]).

TERCERO.- Ante dicho incumplimiento mi representada, con intervención del Notario de esta ciudad Don [NOMBRE Y APELLIDOS], requirió de pago al demandado por plazo de [PLAZO], manifestando su voluntad de resolver el contrato por incumplimiento y reclamándole la restitución del camión arrendado en el lugar pactado en la cláusula [Nº DE CLÁUSULA] del contrato, concretamente el domicilio de mi representado (acompaño como documento número [Nº DE DOCUMENTO] acta notarial de requerimiento).

Transcurrido el plazo indicado, el demandado no ha efectuado el pago ni entregado el bien cedido en arrendamiento, tal como consta en la diligencia expedida por el Notario D. [NOMBRE Y APELLIDOS] en fecha [FECHA] que acompaño como documento número [Nº DE DOCUMENTO], por lo que nos vemos en la obligación de interponer la presente acción resolutoria del contrato pretendiendo exclusivamente la inmediata entrega del bien arrendado.

CUARTO.- Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

FUNDAMENTOS DE DERECHO

Competencia

Son competentes los Tribunales de Instancia de esta ciudad, por ser el lugar del domicilio del deudor, al amparo del art. 50.1 de la LEC, en relación con lo dispuesto en el art. 85.1º LOPJ.

Procedimiento

Teniendo en cuenta que se pretende que el Tribunal resuelva, con carácter sumario, sobre el incumplimiento de un contrato de arrendamiento de bienes muebles, el juicio deberá seguirse por los trámites del juicio verbal, al amparo del número 11º del apartado primero del art. 250 de la LEC, en su redacción por Ley 37/2011, de 10 de octubre.

Legitimación

El demandante tiene legitimación activa por ser el arrendador del vehículo [DESCRIPCIÓN DEL VEHÍCULO] y el demandado está legitimado pasivamente por ostentar la cualidad de arrendatario tal como consta en el contrato aportado como documento núm. [Nº DE DOCUMENTO]

Cumplimiento de los requisitos de procedibilidad

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

Motivos de fondo: Resolución del contrato

El contrato de arrendamiento de bienes muebles ha quedado resuelto por el impago de la renta por parte del arrendatario, tal como se establece en el artículo 1543 del Código Civil en relación con los artículos 1124 y concordantes del mismo texto legal. Conforme a estos preceptos, mi representado está facultado para resolver el contrato ante el incumplimiento del demandado quien ha dejado de abonar la renta los meses de [MESES ADEUDADOS], lo cual realiza mediante la presente acción en juicio sumario encaminada exclusivamente a obtener la inmediata entrega del bien a mi representado. Por su parte, el apartado 7 de la disposición adicional primera de la Ley de Venta a Plazos de Bienes Muebles 28/1998, de 12 de julio, redactado por Ley 37/2011, establece que lo previsto en los apartados 2 a 5 de la citada disposición será de aplicación a los contratos de arrendamiento de bienes muebles.

Costas

Al amparo del artículo 394 de la LEC, las costas deben imponerse a la parte cuyas pretensiones sean totalmente desestimadas.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL: Tenga por presentado este escrito, la copia electrónica del poder notarial de representación informática (o digitalizada) y demás documentos junto con las copias que se acompañan a las que se dará el curso legal, lo admita, me tenga por comparecido y parte en la representación que ostento de D [NOMBRE Y APELLIDOS], entendiéndose conmigo las sucesivas diligencias. Y tenga por formulada demanda de juicio verbal civil contra Don [NOMBRE Y APELLIDOS], cuyas demás circunstancias personales constan en el encabezamiento de este escrito, la admita y tras los trámites procedentes dicte sentencia por la que se declare resuelto el contrato suscrito entre las partes en fecha [FECHA], y se ordene al demandado la inmediata entrega de la camión [DESCRIPCIÓN DEL VEHÍCULO], marca [MARCA/MODELO] modelo [MARCA/MODELO] matrícula [MATRÍCULA] que fue cedida en arrendamiento por mi representado al demandado en el lugar indicado en el contrato; todo ello con imposición al demandado de las costas del proceso.

OTROSÍ PRIMERO DIGO: Que al amparo del art. 441.4 de la LEC, solicito al Tribunal que al admitir la demanda acuerde el depósito del bien cuya entrega se reclama, del cual se hará cargo mi representada, con dispensa de prestar fianza para conseguir la efectividad de la adopción de dicha medida y sin admitir oposición del demandado a la medida cautelar.

Por lo que SUPLICO AL TRIBUNAL ordene el inmediato depósito del bien cuya entrega se reclama.

OTROSÍ SEGUNDO DIGO: Que la cuantía del pleito se fija en [IMPORTE] euros.

Por lo que SUPLICO AL TRIBUNAL tenga por hecha esta manifestación.

OTROSÍ TERCERO DIGO.- Que estando la presente demanda sujeta al abono de la tasa por el ejercicio de la potestad jurisdiccional fijada por la Ley 10/2012, de 20 de noviembre, modificada por Real Decreto Ley 3/2013, de 22 de febrero, y Ley 25/2015, de 28 julio, y por Orden HAP/861/2015, de 7 de mayo, siendo mi representada persona jurídica no exenta, se acompaña a la presente demanda como documento nº [Nº DE DOCUMENTO] la correspondiente autoliquidación con el ejemplar para la Administración de Justicia debidamente validado y en el que consta el pago de la cantidad de 150 euros correspondiente a la cuota fija, más la cantidad de [IMPORTE] euros por la aplicación a la base imponible de la escala prevista en el artículo 7.2 de la citada Ley

En virtud de lo anterior,

SUPLICO AL TRIBUNAL que tenga por hecha la anterior manifestación a los efectos pertinentes y por acompañado el documento justificativo del abono de la tasa.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma Abogado: Firma Procurador:

========================================================================
