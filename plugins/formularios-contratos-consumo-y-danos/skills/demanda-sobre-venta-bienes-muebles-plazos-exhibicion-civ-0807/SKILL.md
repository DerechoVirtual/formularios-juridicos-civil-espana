---
name: demanda-sobre-venta-bienes-muebles-plazos-exhibicion-civ-0807
description: "Demanda sobre venta de bienes muebles a plazos con exhibición de los bienes y depositario. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda sobre venta de bienes muebles a plazos con exhibición de los bienes y depositario

> Formulario **CIV-0807** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda sobre venta de bienes muebles a plazos con exhibición de los bienes y depositario» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda sobre venta de bienes muebles a plazos con exhibición de los bienes y depositario” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-sobre-venta-bienes-muebles-plazos-exhibicion-civ-0807`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (9 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] MARCA/MODELO (4 veces)
- [ ] CALLE (2 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] Nº (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] DIRECCIÓN
- [ ] FECHA
- [ ] LOCALIDAD
- [ ] LUGAR Y FECHA
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] MES
- [ ] Nº DE INSCRIPCIÓN
- [ ] Nº DE SERIE
- [ ] PROVINCIA
- [ ] SEDE

## Normas que cita el formulario

- art. 250 LEC
- art. 250.1.10 LEC
- art. 52.2 LEC
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 439.4 LEC
- art. 1100 CC
- art. 394 LEC
- art. 441.4 LEC
- art. 7.2 Ley 10/2012

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

Que en la representación que ostento formulo demanda de juicio verbal con la pretensión de que el Tribunal resuelva con carácter sumario, sobre el incumplimiento de un contrato de financiación para la venta de bienes muebles a plazos, al amparo del número 10º del apartado primero del art. 250 de la LEC, contra Don [NOMBRE Y APELLIDOS] con domicilio en la calle [CALLE] de esta ciudad, la cual baso en los siguientes:

HECHOS

Primero.- Mi representada es una entidad mercantil que se dedica a la venta de material informático, en especial ordenadores y demás bienes de equipo y accesorios.

Segundo.- En fecha [FECHA] mi representada suscribió con el demandado un contrato de compraventa de bienes muebles a plazos, cuyo objeto era un ordenador, marca [MARCA/MODELO] modelo [MARCA/MODELO] nº [Nº] de identificación [Nº DE SERIE] y una pantalla marca [MARCA/MODELO] modelo [MARCA/MODELO] nº [Nº] de identificación, provisto también del correspondiente teclado de la misma marca, y demás accesorios que constan en el contrato, cuyo precio total era de [IMPORTE] euros.

Tercero.- En virtud del citado contrato, el deudor se comprometió a abonar a mi representada el precio convenido de [IMPORTE] euros mediante el pago de 12 cuotas mensuales que vencían el primer día de cada mes. El pago aplazado en cuotas mensuales de [IMPORTE] euros debía hacerse mediante domiciliación bancaria en los términos que resulta de la cláusula 10ª del contrato.

Cuarto.- El contrato se formalizó en modelo oficial y fue inscrito en el Registro de Venta de Bienes Muebles a Plazos [Nº DE INSCRIPCIÓN].

Quinto.- No obstante el demandado dejó de satisfacer los dos plazos correspondientes a los meses de [MES] y, por lo que mi representada a través del Notario de esta ciudad Don [NOMBRE Y APELLIDOS] requirió al comprador para que pagara la totalidad de la cantidad que se reclama, que asciende a [IMPORTE] euros, más los intereses de demora pactados en la cláusula 14ª.

También se expresó en el requerimiento que la causa del vencimiento de la obligación derivaba de la cláusula 16ª del contrato, conforme a la cual el impago de dos o más mensualidades hacía perder al comprador el beneficio del plazo y facultaba al vendedor a dar por vencida la obligación, constituyendo una causa de vencimiento que facultaba al vendedor a exigir la totalidad de las cuotas pendientes de pago.

Asimismo se apercibió al comprador de que si no atendía a su pago se procedería contra los bienes adquiridos a plazos en la forma establecida en el art. 16 de la misma ley, a cuyos efectos se le indicaba que podía hacer entrega voluntaria de los bienes adquiridos para su realización, entrega que debía hacerse en el establecimiento del demandante sito en esta ciudad [DIRECCIÓN], lugar en el que el demandado efectuó la compraventa; en este caso se procedería a la enajenación en pública subasta mediante intervención de Notario y con cuyo producto se reintegraría el vendedor; todo ello sin perjuicio de que, una vez satisfechos los gastos de la subasta, si existiera algún sobrante se entregaría al comprador.

Por último, se advertía de que, en caso de no efectuar el pago ni entregar voluntariamente los bienes, se ejercitaría la acción prevista en el art. 250.1.10ª de la LEC.

Sexto.- El deudor dejó transcurrir el plazo establecido en la ley sin efectuar el pago ni entregar los bienes, tal como queda acreditado por el acta notarial y la diligencia del fedatario expresiva del impago y de la no entrega del bien (acompaño acta original como documento nº 3).

Séptimo.- Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

FUNDAMENTOS DE DERECHO PROCESAL

COMPETENCIA

Es competente el Tribunal de Instancia de esta ciudad, al ser de aplicación el artículo 52.2 de la LEC.

PROCEDIMIENTO

Teniendo en cuenta la clase de pretensión que se ejercita y que se ampara en la Ley 28/1998, de 13 de julio, el proceso deberá seguirse por los trámites del juicio verbal (artículo 250.1.10º de la LEC).

CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

FUNDAMENTOS DE DERECHO SUSTANTIVO

Primero.- El Tribunal al que me dirijo es competente, al amparo del art. 52.2 de la LEC, dado el domicilio del comprador.

Segundo.- El artículo 250.1.10º de la LEC permite que el Tribunal resuelva, con carácter sumario, sobre el incumplimiento por el comprador de las obligaciones derivadas de los contratos inscritos en el Registro de Venta de Bienes Muebles a Plazos, formalizados en el modelo establecido al efecto, al objeto de obtener una sentencia condenatoria que permita dirigir la ejecución exclusivamente sobre el bien o bienes adquiridos a plazos.

Tercero.- Mi representado está legitimado activamente para el ejercicio de la acción ya que vendió los artículos objeto del contrato de compraventa y el demandado está legitimado pasivamente por ser el comprador.

Cuarto.- La suma exigible, por no existir pacto en contrario, es la especificada en la certificación expedida por mi representada, al resultar acreditado, por fedatario público, haberse practicado la liquidación, en la forma pactada por las partes en el contrato y que el saldo coincide con el que aparece en la cuenta abierta al deudor, al amparo del art. 16.2.a) de la LVPBM.

Quinto.- Al amparo del art. 439.4 de la LEC, acompaño a esta demanda el documento que acredita haber requerido de pago al deudor, con diligencia expresiva del impago y de la no entrega del bien que fue llevado a cabo, en los términos que establece el art. 16 de la Ley de Venta de Bienes Muebles a Plazos y certificación de la inscripción de los bienes en el Registro de VPBM.

Sexto.- Con arreglo al art. 16 de la LVPBM, el acreedor podrá recabar el cumplimiento de las obligaciones derivadas de los contratos regulados por dicha ley mediante el ejercicio de las acciones que correspondan, siendo una de ellas, este proceso de ejecución que permite, una vez acreditada la deuda, dirigirse directa y exclusivamente contra los bienes adquiridos a plazos; todo ello sin perjuicio de que, si a consecuencia de la enajenación resultare un sobrante, se reintegre al deudor.

Séptimo.- Asimismo procede la pretensión de intereses de demora en los términos que establece el art. 1100 del CC en relación con la cláusula 9ª del contrato, y que al tiempo de interponer la demanda ascendían a [IMPORTE] euros.

COSTAS

Al amparo del artículo 394 de la LEC, las costas deben imponerse a la parte cuyas pretensiones sean totalmente desestimadas.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL: Tenga por presentado este escrito, la copia electrónica del poder notarial de representación informática (o digitalizada) y demás documentos junto con las copias que se acompañan a las que se dará el curso legal, lo admita, me tenga por comparecido y parte en la representación que ostento de la entidad [DENOMINACIÓN SOCIAL] entendiéndose conmigo las sucesivas diligencias. Y tenga por formulada demanda de juicio verbal civil contra el demandado Don [NOMBRE Y APELLIDOS] cuyas demás circunstancias personales constan en el encabezamiento de este escrito, la admita y tras los trámites que procedan dicte sentencia en la que se estime la demanda, se declare que el demandado adeuda la cantidad de [IMPORTE] comprensiva de las cuotas vencidas y no satisfechas y los intereses correspondientes, así como que se acuerde proceder a la ejecución que se dirigirá exclusivamente sobre los bienes muebles adquiridos a plazos objeto del contrato y financiados por mi representada con el fin de que mi principal se reintegre de la cantidad adeudada de [IMPORTE] euros, más los intereses que se cuantifican en [IMPORTE] Todo ello con imposición de las costas causadas en esta instancia al demandado.

OTROSÍ PRIMERO DIGO: Que al amparo del art. 441.4 de la LEC solicito al Tribunal que al admitir la demanda acuerde la exhibición de los bienes a su poseedor, bajo apercibimiento de incurrir en desobediencia a la autoridad judicial, y su inmediato embargo preventivo, que se asegurará mediante depósito, con arreglo a lo previsto en la LEC.

A dichos efectos designo como depositario a Don [NOMBRE Y APELLIDOS], el cual también deberá ser dispensado de prestar fianza una vez acepte el cargo.

OTROSÍ SEGUNDO DIGO: Que fijo la cuantía del pleito en [IMPORTE] euros que resultan del principal que se reclama y los intereses de demora ya vencidos.

OTROSÍ TERCERO.-Que estando la presente demanda sujeta al abono de la tasa por el ejercicio de la potestad jurisdiccional fijada por la Ley 10/2012, de 20 de noviembre, modificada por Real Decreto Ley 3/2013, de 22 de febrero, y Ley 25/2015, de 28 julio, y por Orden HAP/861/2015, de 7 de mayo, siendo mi representada persona jurídica no exenta, se acompaña a la presente demanda como documento nº [Nº DE DOCUMENTO] la correspondiente autoliquidación con el ejemplar para la Administración de Justicia debidamente validado y en el que consta el pago de la cantidad de 150 euros correspondiente a la cuota fija, sin que se incluya la cuota variable prevista en el artículo 7.2 de la Ley 10/2012 al haber sido declarado inconstitucional y nulo por la STC 140/2016, de 21 de julio.

En virtud de lo anterior,

SUPLICO AL TRIBUNAL: que tenga por hecha la anterior manifestación a los efectos pertinentes y por acompañado el documento justificativo del abono de la tasa.

En [LUGAR Y FECHA].

========================================================================
