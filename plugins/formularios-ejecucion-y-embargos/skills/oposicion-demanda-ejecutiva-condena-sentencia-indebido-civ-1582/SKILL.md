---
name: oposicion-demanda-ejecutiva-condena-sentencia-indebido-civ-1582
description: "Oposición a la demanda ejecutiva de condena en sentencia por indebido tipo de interés moratorio. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Oposición a la demanda ejecutiva de condena en sentencia por indebido tipo de interés moratorio

> Formulario **CIV-1582** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Escrito de oposición del ejecutado a la ejecución de una sentencia de condena al pago de intereses del art. 20 de la Ley de Contrato de Seguro, cuando el ejecutante ha liquidado los intereses moratorios vencidos aplicando un tipo indebido (pluspetición). Se usa cuando el ejecutado acepta el principal, lo consigna y discute solo la cuantía de los intereses.

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Oposición a la demanda ejecutiva de condena en sentencia por indebido tipo de interés moratorio» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Oposición a la demanda ejecutiva de condena en sentencia por indebido tipo de interés moratorio” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:oposicion-demanda-ejecutiva-condena-sentencia-indebido-civ-1582`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (10 veces)
- [ ] Nº DE DÍAS (8 veces)
- [ ] FECHA INICIAL (4 veces)
- [ ] FECHA (3 veces)
- [ ] FECHA FINAL (3 veces)
- [ ] IMPORTE DEL PRINCIPAL (3 veces)
- [ ] IMPORTE EN LETRA (3 veces)
- [ ] Nº DE SECCIÓN (3 veces)
- [ ] 365 O 366 (2 veces)
- [ ] AÑO (2 veces)
- [ ] DÍA (2 veces)
- [ ] FECHA DEL SINIESTRO (2 veces)
- [ ] FIRMA (2 veces)
- [ ] MES (2 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] TIPO LEGAL INCREMENTADO EN UN 50 % (2 veces)
- [ ] AÑOS
- [ ] DENOMINACIÓN SOCIAL DE LA ASEGURADORA
- [ ] FECHA DE CONSIGNACIÓN
- [ ] FECHA DE LIQUIDACIÓN
- [ ] FECHA EN QUE SE CUMPLEN LOS DOS AÑOS
- [ ] IMPORTE DE LOS INTERESES VENCIDOS A LA SOLICITUD DE EJECUCIÓN
- [ ] IMPORTE DIARIO
- [ ] IMPORTE TOTAL DE INTERESES
- [ ] IMPORTE TOTAL DE INTERESES VENCIDOS
- [ ] LOCALIDAD
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº DE ROLLO
- [ ] PERIODO DE DEVENGO
- [ ] PROVINCIA
- [ ] SEDE
- [ ] SUMA DE LOS IMPORTES ANTERIORES
- [ ] TIPO INCREMENTADO
- [ ] TIPO LEGAL

## Normas que cita el formulario

- art. 20 LCS
- art. 20.4.º LCS
- art. 558 LEC
- art. 575.2 LEC
- art. 219 LEC
- art. 576.2 LEC
- art. 20.6.º LCS
- art. 563 LEC
- art. 712 LEC

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

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales y de la entidad aseguradora [DENOMINACIÓN SOCIAL DE LA ASEGURADORA], S.A., como acredito con copia de poder que ya consta en el JUICIO ORDINARIO n.º [Nº DE PROCEDIMIENTO], en autos de EJECUCIÓN DE TÍTULO JUDICIAL n.º [Nº DE PROCEDIMIENTO], en los mismos comparezco y como mejor proceda en Derecho, DIGO:

Que dentro del plazo legal que se concede en el auto de despacho de ejecución de fecha [DÍA] de [MES] de [AÑO], paso a formalizar la OPOSICIÓN contra la liquidación de la cuantía ejecutiva, y ello en base a los siguientes

HECHOS

PRIMERO.– El motivo de la oposición es la equivocada liquidación de los intereses moratorios que se practica en la demanda ejecutiva, lo cual constituye pluspetición, contradice el título ejecutivo o, en todo caso, es infracción del correcto acto liquidatorio.

Pretende la parte actora la ejecución de la sentencia dictada en el juicio ordinario de que dimanan estos autos ejecutivos. Y dicha sentencia establecía un principal a favor de los actores de [IMPORTE DEL PRINCIPAL] euros y los intereses recogidos en el art. 20 de la Ley de Contrato de Seguro (LCS) en caso de la compañía aseguradora.

Pues bien, esta representación no se opone a la obligación de pago del importe del principal (importe que está consignado en la cuenta del Tribunal), pero sí al importe recogido como intereses moratorios vencidos.

La parte actora ha aplicado incorrectamente el art. 20 LCS, según el siguiente cálculo:

— PRINCIPAL: [IMPORTE DEL PRINCIPAL]
— FECHA DEL SINIESTRO: [FECHA DEL SINIESTRO]
— FECHA DE LIQUIDACIÓN: [FECHA DE LIQUIDACIÓN]
— PERIODO DE DEVENGO: [PERIODO DE DEVENGO]
— INTERÉS DIARIO al 20 % anual: [IMPORTE]
— INTERESES DEVENGADOS según la parte actora: [IMPORTE]

Dicho precepto establece que, desde la fecha del siniestro y durante los dos primeros años, el interés devengado es igual al legal del dinero incrementado en un cincuenta por ciento, y que a partir de los dos años no podrá ser inferior al 20 % anual.

Por tanto, los intereses vencidos a la fecha de la solicitud de la ejecución ascienden a [IMPORTE EN LETRA] euros ([IMPORTE]), desglosados de la siguiente manera:

* Intereses desde la fecha del siniestro, [FECHA DEL SINIESTRO], hasta [FECHA EN QUE SE CUMPLEN LOS DOS AÑOS], en que se rebasaron los dos años desde el siniestro.

— [FECHA INICIAL] a [FECHA FINAL] = [Nº DE DÍAS] días: (PRINCIPAL x [TIPO LEGAL INCREMENTADO EN UN 50 %] x [Nº DE DÍAS]) / (100 x [365 O 366]) = [IMPORTE]
— [FECHA INICIAL] a [FECHA FINAL] = [Nº DE DÍAS] días: (PRINCIPAL x [TIPO LEGAL INCREMENTADO EN UN 50 %] x [Nº DE DÍAS]) / (100 x [365 O 366]) = [IMPORTE]

El interés legal del dinero ascendió al [TIPO LEGAL] % anual según las Leyes de Presupuestos Generales del Estado para los años [AÑOS], por lo que, incrementado en un cincuenta por ciento, ascendió al [TIPO INCREMENTADO] %. (Repítase el cálculo por cada año natural con su tipo legal.)

* Intereses desde el día siguiente al cumplimiento de los dos años hasta el día en que se presenta la solicitud de ejecución (20 %).

— [FECHA INICIAL] a [FECHA FINAL] = [Nº DE DÍAS] días: (PRINCIPAL x 20 x [Nº DE DÍAS]) / (100 x 365) = [IMPORTE]

TOTAL: [SUMA DE LOS IMPORTES ANTERIORES] = [IMPORTE TOTAL DE INTERESES VENCIDOS]

La doctrina de la Audiencia Provincial sobre la interpretación del art. 20.4.º LCS es clara, así:

— La sentencia dictada por la Sección [Nº DE SECCIÓN] de la Audiencia Provincial de [PROVINCIA], de fecha [FECHA], en el rollo de apelación n.º [Nº DE ROLLO], dice: «[CITA LITERAL: la aplicación por tramos es la interpretación más correcta del art. 20 LCS en la redacción dada por la Ley 30/1995]».

— El auto de fecha [FECHA] de la Sección [Nº DE SECCIÓN] establece: «[CITA LITERAL: el devengo del interés legal incrementado en un 50 % en los dos primeros años a partir de la fecha del siniestro y el 20 % anual a partir del segundo año hasta la consignación o pago]».

— Asimismo, el auto de fecha [FECHA], dictado por la Sección [Nº DE SECCIÓN] en incidente de liquidación de intereses, establece: «[CITA LITERAL: los intereses se devengan por días, incluso cuando haya transcurrido más de dos años desde la producción del siniestro, con la sola particularidad de que en este último caso el cálculo del interés legal incrementado en un 50 por ciento no puede ser inferior a ese 20 %; el interés del 20 % anual solo puede aplicarse transcurridos dos años desde la producción del siniestro]».

Y ha sido definida por la jurisprudencia en la STS (Sala 1.ª), Pleno, de 1 de marzo de 2007, rec. 2302/2001, en uno de los pocos ejemplos de acceso a la casación de esta materia, que interpreta que el art. 20.4.º LCS apunta literal o gramaticalmente al cálculo del doble tramo: «el interés de demora a satisfacer al lesionado por la aseguradora recurrente debe calcularse, durante los dos primeros años siguientes al siniestro, al tipo legal más su 50 % y, a partir de ese momento, al tipo del 20 % si aquel no resulta superior».

Por tanto, nos encontramos en un supuesto de PLUSPETICIÓN.

SEGUNDO.– Los intereses desde la fecha de la solicitud de ejecución hasta la consignación por parte de mi representada ascienden a [IMPORTE EN LETRA] euros ([IMPORTE]), desglosados de la siguiente manera:

* [FECHA INICIAL] a [FECHA DE CONSIGNACIÓN] = [Nº DE DÍAS] días: PRINCIPAL x 20 % / 365 = [IMPORTE DIARIO] euros/día x [Nº DE DÍAS] = [IMPORTE]

Sumados a los [IMPORTE DE LOS INTERESES VENCIDOS A LA SOLICITUD DE EJECUCIÓN] euros, corridos hasta la fecha en que se instó la ejecución, hacen [IMPORTE TOTAL DE INTERESES].

TERCERO.– Esta representación considera como cantidad debida por principal e intereses moratorios hasta el pago pleno la de [IMPORTE EN LETRA] euros ([IMPORTE]), resultante de la suma del principal ([IMPORTE DEL PRINCIPAL]) y los intereses liquidados según los cálculos de esta representación.

Habiendo consignado el dinero en la cuenta del Tribunal, mi mandante solicita la entrega de la cantidad citada de [IMPORTE] euros a los acreedores, suspendiéndose la ejecución hasta que se resuelva el motivo de oposición citado.

FUNDAMENTOS DE DERECHO

I.– Nada que oponer en cuanto a la jurisdicción, competencia (funcional, objetiva y territorial), clase de juicio, capacidades, legitimación o representación.

II.– PLUSPETICIÓN.

Conforme al art. 558 LEC, resulta aplicable la excepción de PLUSPETICIÓN, y ello por el motivo alegado en los antecedentes.

El art. 575.2 LEC dispone la imposibilidad de que el Tribunal deniegue el despacho de ejecución porque considere indebido, como es el caso, el cálculo de la cantidad por la que pide ejecución el acreedor, sin perjuicio de que se alegue la pluspetición.

Bien es cierto que dicha oposición de fondo al despacho ejecutivo no está prevista explícitamente para la derivada de títulos judiciales o asimilados, como es la sentencia, pero resulta inaceptable que, siendo la liquidación de intereses una operación técnica con arreglo a datos del título, pueda efectuarla la parte ejecutante desentendiéndose de tales datos, sin posible repulsa del órgano ejecutor y sin control de la parte deudora afectada.

III.– CONTRADICCIÓN DEL TÍTULO.

Se trata el título ejecutivo de una sentencia que establece la aplicación de los intereses del art. 20 LCS, sin especificar el «dies a quo» del devengo ni el tipo anual utilizable, por lo que no sienta las bases para liquidar, como derivaría de cumplir con lo preceptuado en el art. 219 LEC, siendo que el tipo y el tiempo de devengo son los parámetros que determinan la liquidez de una deuda de intereses (art. 576.2 LEC).

Los actores han solicitado la ejecución, fijando un cálculo a su favor, sin enterar a esta parte del crédito que estimaban ostentar en tal punto, y en lugar de haber esperado a la conformidad de pago y, en su caso, solicitar luego la liquidación de intereses cuando las cuentas de esta parte no le satisficieran.

Por consiguiente, es necesario un acto de liquidación, a fin de que se establezcan los parámetros de la cuantía correcta de la condena por intereses de mora y, sin discusión el día inicial, conforme al art. 20.6.º LCS, el tipo ha de fijarse en proceso liquidatorio.

No haberlo efectuado, y despachar ejecución por una cifra arbitraria, es un evidente acto ejecutivo que contradice el título y puede combatirse mediante la vía de recurso, conforme al art. 563 LEC, lo cual se aduce a fin de que se conceda tal carácter, subsidiariamente, a este escrito.

La irrecurribilidad del auto se refiere al despacho mismo, y no al acto ejecutivo de liquidación informal e indebida de intereses.

IV.– FONDO (exégesis del art. 20.4.º LCS).

Nos reiteramos en las apreciaciones jurídicas acerca del tipo o rédito aplicable, que se han expuesto en el hecho PRIMERO. Esta representación considera que, según el tenor literal del apartado 4 del art. 20 LCS, durante los dos años siguientes al siniestro la cantidad debida devengará intereses cuyo tipo será el legal incrementado en un 50 % y solo a partir de los dos años el tipo a aplicar será el del 20 %.

V.– COSTAS.

Deben imponerse al ejecutante de conformidad con lo recogido en los arts. 394, 539 y 561.3 LEC.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que, habiendo por presentado este escrito con los documentos que se acompañan, de los que se ha dado traslado por copia a la representación procesal de los ejecutantes, se sirva admitirlo, teniendo por formalizada la oposición en nombre de mi mandante y, en méritos de lo expuesto, dicte en su día resolución que ordene la reducción de la cuantía de ejecución en los términos alegados, con imposición de costas a la parte ejecutante, con todo lo demás que sea de hacer en justicia, que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

OTROSÍ DIGO: Que al derecho de esta parte interesa hacer constar que ha consignado en la cuenta del Tribunal la cantidad que ha sido objeto de despacho de ejecución y no se discute; solicito que se levanten los embargos acordados sobre bienes y derechos de mi representada, entregándose de inmediato a los ejecutantes dicha cantidad.

SUPLICO AL TRIBUNAL que, teniendo por hecha la antecedente manifestación a los efectos oportunos, se digne proveer en consecuencia, según es justo, en lugar y fecha ut supra.

Firma del Abogado/a: [FIRMA] Firma del Procurador/a: [FIRMA]

NOTA EXPLICATIVA

El cálculo o cuenta de intereses de mora puede producirse en dos momentos del proceso de declaración y en dos del de ejecución. Al ejercerse una pretensión declarativa de condena, se cuantificarán los vencidos al momento de interponer la demanda, fijándose las bases de los que están por correr, y luego se cuantificarán hasta el dictado de la sentencia estimatoria en esta, estando fijadas legalmente las bases de los que corren a partir de entonces. Al ejercerse la pretensión de ejecución derivada, se calculan los vencidos hasta el momento de la demanda ejecutiva, estando legalmente fijadas las bases de los que corren desde entonces, y luego se cuantificarán hasta el pago definitivo cuando este se produzca. En principio, son operaciones que no requieren de un genuino proceso de liquidación de los arts. 712 y siguientes LEC. Pero si falta algún dato en la sentencia, no parece que pueda prescindirse de un trámite liquidatorio. Es la opción del modelo, como fórmula de conceder salida al problema de que el ejecutado que paga discuta la cuantificación del ejecutante en la demanda ejecutiva, que no está previsto en la norma.
