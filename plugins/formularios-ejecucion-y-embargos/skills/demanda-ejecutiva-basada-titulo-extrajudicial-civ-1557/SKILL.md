---
name: demanda-ejecutiva-basada-titulo-extrajudicial-civ-1557
description: "Demanda ejecutiva basada en título extrajudicial. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda ejecutiva basada en título extrajudicial

> Formulario **CIV-1557** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda ejecutiva basada en título extrajudicial» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda ejecutiva basada en título extrajudicial” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:demanda-ejecutiva-basada-titulo-extrajudicial-civ-1557`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (6 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] IMPORTE (5 veces)
- [ ] TIPO DE INTERÉS (2 veces)
- [ ] CANTIDADES ADEUDADAS
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] ENTIDAD BANCARIA
- [ ] LOCALIDAD
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº
- [ ] Nº DE DOCUMENTO
- [ ] PLAZO
- [ ] PORCENTAJE
- [ ] SEDE
- [ ] TÍTULO EJECUTIVO

## Normas que cita el formulario

- art. 517.2.5 LEC
- art. 545.3 LEC
- art. 549.2 LEC
- art. 551 LEC
- art. 551.2.3 LEC
- art. 575.1 LEC
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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D. [NOMBRE Y APELLIDOS] Procurador de los Tribunales, en nombre y representación de [NOMBRE DEL REPRESENTADO/A], cuestión que acredito mediante la aportación de la copia electrónica del poder notarial de representación informática (o digitalizada) que acompaño, ante el Tribunal comparezco y como mejor proceda en Derecho DIGO:

Que en la representación que ostento INTERPONGO DEMANDA EJECUTIVA, con base en el título [TÍTULO EJECUTIVO], contra D. [NOMBRE Y APELLIDOS] en reclamación de cantidad de [IMPORTE] Euros correspondientes al préstamo concedido y no reembolsado por mi mandante al ejecutado, más la cantidad de [IMPORTE] euros en concepto de intereses devengados y no satisfechos, más los de demora que se hayan devengado, más la totalidad de gastos y costas que se vayan devengando hasta el cobro total de la deuda.

Fundamento esta demanda en los siguientes

HECHOS

PRIMERO.- En fecha [FECHA] la entidad financiera [ENTIDAD BANCARIA] a la que represento concedió póliza de préstamo personal a D. por la cantidad de [IMPORTE], formalizada ante el Notario de [LOCALIDAD] D. [NOMBRE Y APELLIDOS], aportándose Copia Simple de la misma como DOCUMENTO NÚM. 1.

SEGUNDO.- Tal y como consta en dicha póliza las condiciones pactadas son las siguientes:

1. El interés anual que devengará la cantidad objeto de préstamo será de [TIPO DE INTERÉS], más un porcentaje de comisión del [PORCENTAJE] sobre el capital, debiendo satisfacerse las cuotas por meses vencidos, debiendo realizarse el primer pago en fecha [FECHA].

2. El plazo de devolución de la cantidad prestada libremente pactado entre las partes es de [PLAZO] Las cuotas serán anuales a satisfacer por meses vencidos, siendo la fecha del primer pago [FECHA].

3. El tipo de interés de demora establecido es de [TIPO DE INTERÉS], siendo la fecha del primer pago [FECHA].

TERCERO.- Se procede a los efectos del artículo 517.2.5º LEC, a la aportación como DOCUMENTO NÚM. 2 de certificación expedida por el Notario interviniente relativa a la acreditación de la conformidad de la póliza con los asientos de su libro registro y la fecha de éstos.

CUARTO.- De acuerdo con la cláusula tercera del contrato de préstamo aportado como DOCUMENTO NÚM. 1, «la demora en el pago de los intereses o de cualquier amortización comportará la resolución inmediata del contrato y el vencimiento anticipado de la suma».

Teniendo en cuenta que el primer impago se produjo en fecha [FECHA], siendo requerido el deudor por la entidad financiera a la que represento, mediante requerimiento notarial de fecha [FECHA] que se aporta como DOCUMENTO NÚM. 2, sin que hasta la fecha se haya producido pago alguno en dicho concepto, procede el vencimiento anticipado previsto en la póliza y las cantidades adeudas a fecha de hoy son las siguientes: [CANTIDADES ADEUDADAS].

[NOMBRE Y APELLIDOS], aportándose certificación expedida por la entidad financiera a la que represento en la que consta acta elaborada por el Notario D. [NOMBRE Y APELLIDOS], que se aporta como DOCUMENTO NÚM. 3, en la que se relaciona la conformidad de la liquidación en los términos pactados por las partes en el título ejecutivo, coincidiendo el saldo con la deuda y como DOCUMENTO NÚM. 4 requerimiento notarial en el que se detalla al deudor la cantidad exigible y se le requiere de pago.

QUINTO.- Que designo como bienes a embargar del ejecutado, considerándolos suficientes al efecto de cubrir las cantidades reclamadas.

A los anteriores hechos le son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

PRIMERO.- COMPETENCIA.

Correspondiendo al Juez al que me dirijo por ser el competente, de acuerdo con lo establecido en el artículo 545.3 LEC, teniendo en cuenta el lugar de cumplimiento del contrato de préstamo objeto de la presente ejecución.

SEGUNDO.- PROCEDIMIENTO.

El Tribunal procederá a despachar ejecución cuando se presente demanda que reúna los requisitos establecidos en los artículos 549.2 y 550 LEC por los trámites de los artículos 551 a 554 LEC.

TERCERO.- TÍTULO EJECUTIVO.

El establecido en el artículo 517.2.5º LEC.

CUARTO.- COSTAS.

Artículo 539.2 LEC.

Por lo expuesto,

SUPLICO AL TRIBUNAL: Tenga por presentado este escrito con los documentos que lo acompañan y sus copias, teniéndome por comparecido y parte en la representación que ostento y por formulada DEMANDA EJECUTIVA contra D. [NOMBRE Y APELLIDOS], la admita y dicte auto conteniendo la orden general de ejecución y despachando la misma, en el que conforme al artículo 551.2.3º LEC fije la cantidad reclamada conforme a lo solicitado en la cantidad de [IMPORTE] Euros en concepto de principal, más la cantidad de [IMPORTE] Euros en concepto de intereses, gastos y costas (que no debe superar el 30% del principal, de acuerdo con el artículo 575.1 LEC), procediéndose por este órgano judicial a requerir de pago al ejecutado y para el caso de que no se verifique el pago inmediato se proceda a embargar los bienes [DESCRIPCIÓN DEL BIEN] para cubrir las indicadas responsabilidades en su totalidad.

OTROSÍ DIGO: Que, una vez dictado el auto general de ejecución, se solicita que por el Letrado de la Administración de Justicia responsable de la misma se dicte decreto procediéndose a requerir de pago al ejecutado por la cantidad indicada y, para el caso de que no se verifique el pago inmediato, se proceda a adoptar las medidas ejecutivas necesarias, acordando el embargo de los siguientes bienes del deudor de los que tiene conocimiento esta parte y que se estiman suficientes para cubrir las indicadas responsabilidades en su totalidad:

SUPLICO que se dicte decreto en el que se contengan las medidas que dejo interesadas.

OTROSÍ DIGO II: Que, al amparo de lo dispuesto en el art. 152.1.2º en relación con el art. 553 de la Ley de Enjuiciamiento Civil, esta parte solicita que la notificación al ejecutado del auto y decreto que se deriva de este trámite se practique a su costa por medio del Procurador de esta parte, que suscribe el presente escrito, asumiendo las responsabilidades prevenidas legalmente.

SUPLICO se acuerde practicar el acto de comunicación que deriva de este escrito por medio del Procurador de esta parte y a su costa, entregando los documentos correspondientes a esta representación para su diligenciamiento.

OTROSÍ DIGO III.- Que estando la presente demanda sujeta al abono de la tasa por el ejercicio de la potestad jurisdiccional fijada por la Ley 10/2012, de 20 de noviembre, modificada por RDL 3/2013 y Ley 25/2015, de 28 julio, y desarrollada por Orden HAP/2662/2012, de 13 de diciembre, siendo mi representada personas jurídica no exenta de su pago, se acompaña a la presente demanda como documento nº [Nº DE DOCUMENTO] la correspondiente autoliquidación con el ejemplar para la Administración de Justicia debidamente validado y en el que consta el pago de la cantidad de 200 euros correspondiente a la cuota fija, sin que se incluya la cuota variable prevista en el artículo 7.2 de la Ley 10/2012 al haber sido declarado inconstitucional y nulo por la STC 140/2016, de 21 de julio.

En virtud de lo anterior,

SUPLICO AL TRIBUNAL: que tenga por hecha la anterior manifestación a los efectos pertinentes y por acompañado el documento justificativo del abono de la tasa.

========================================================================
