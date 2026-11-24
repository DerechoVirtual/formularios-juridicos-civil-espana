---
name: demanda-resolver-compra-vivienda-construccion-reclamar-civ-0749
description: "Demanda para resolver la compra de vivienda en construcción y reclamar lo entregado al banco. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda para resolver la compra de vivienda en construcción y reclamar lo entregado al banco

> Formulario **CIV-0749** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda para resolver la compra de vivienda en construcción y reclamar lo entregado al banco» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda para resolver la compra de vivienda en construcción y reclamar lo entregado al banco” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-resolver-compra-vivienda-construccion-reclamar-civ-0749`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (9 veces)
- [ ] Nº DE DOCUMENTO (9 veces)
- [ ] IMPORTE (8 veces)
- [ ] DENOMINACIÓN SOCIAL (7 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] ENTIDAD BANCARIA (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] AÑO
- [ ] DENOMINACIÓN DEL EDIFICIO
- [ ] DÍA
- [ ] LUGAR
- [ ] MES
- [ ] Nº DE CLÁUSULA
- [ ] Nº DE CUENTA (IBAN)
- [ ] PARTE DEMANDADA
- [ ] PISO
- [ ] PUERTA
- [ ] SEDE

## Normas que cita el formulario

- art. 1124 Código Civil
- art. 1.822 Código Civil
- art. 51 LEC
- art. 85.1 LOPJ
- art. 72 LEC
- art. 10 LEC
- art. 249.2 LEC
- art. 1258 Código Civil
- art. 394 LEC
- art. 251 LEC
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

D/Dña. [NOMBRE Y APELLIDOS] Procurador/a de los Tribunales en representación de D/Dña. [NOMBRE Y APELLIDOS], según acredito por certificación del registro electrónico de apoderamientos judiciales que acompaño o mediante designación apud acta otorgado ante el/la Letrado/a de la Administración de Justicia de [LOCALIDAD] que acompaño [Nº DE DOCUMENTO] bajo la dirección letrada de D/Dña. [NOMBRE Y APELLIDOS], Abogado/a del Iltre. Colegio de [LOCALIDAD], ante el Tribunal comparezco y como mejor en derecho proceda formulo demanda de juicio ordinario en ejercicio de la acción de resolución del contrato de compraventa suscrito en fecha [FECHA], la cual dirijo contra la promotora [DENOMINACIÓN SOCIAL], con domicilio en [LOCALIDAD], acumulando la acción de reclamación de cantidad contra la entidad [DENOMINACIÓN SOCIAL], con domicilio en [LOCALIDAD], en base a los siguientes:

HECHOS

PRIMERO En fecha [FECHA], mi representado, en su condición de comprador, suscribió la promotora demandada [DENOMINACIÓN SOCIAL] contrato privado de compraventa de vivienda y parking en la promoción del edificio [DENOMINACIÓN DEL EDIFICIO] sito en [LOCALIDAD], en concreto, piso [PISO], puerta [PUERTA], con tres dormitorios, dos baños, cocina, lavadero, salón y terraza, y una plaza de aparcamiento con el número [NÚMERO], fijándose como precio [IMPORTE], euros, más el % de IVA, [IMPORTE] euros, en total [IMPORTE] euros (acompaño como documento número [Nº DE DOCUMENTO] copia simple del citado contrato de compraventa)

En la cláusula [Nº DE CLÁUSULA] del citado contrato se estableció el modo de pago fraccionado desde la reserva hasta la escritura pública, en cuatro plazos que debían abonarse en la cuenta especial [Nº DE CUENTA (IBAN)] abierta en la entidad bancaria [ENTIDAD BANCARIA], conviniéndose que las cantidades entregadas serían garantizadas con aval bancario solidario de la citada entidad, y se fijó como fecha de finalización de las obras el día [FECHA], con obligación de entrega al comprador.

SEGUNDO En cumplimiento del citado contrato, mi representado abonó cuatro pagos parciales por importe de [IMPORTE] euros cada uno, los cuales fueron ingresados en la cuenta especial número [NÚMERO] de la entidad bancaria codemandada, por un total de [IMPORTE] euros (acompaño como documentos [Nº DE DOCUMENTO] justificante de las transferencias bancarias).

TERCERO Una vez llegada la fecha de entrega de la vivienda, y ante la total ausencia de noticias de la vendedora codemandada, mi representado pudo constatar que el día [FECHA] todavía no se habían iniciado las obras, tal como se recoge en el acta notarial de presencia de fecha [FECHA] que se acompaña como documento [Nº DE DOCUMENTO], pudiendo comprobarse en las fotografías que tan solo se había rebajado el suelo para construir el aparcamiento del edificio y levantado algunos pilares.

CUARTO Ante la evidencia del incumplimiento de la vendedora, mi representado remitió burofax a la citada codemandada por el que dio por resuelto el contrato y solicitó la devolución de las cantidades entregadas con más los intereses legales (acompaño como documento número [Nº DE DOCUMENTO] copia del burofax donde consta la recepción por la codemandada en fecha [FECHA])

Asimismo, mi representado requirió a la entidad bancaria codemandada para que le fueran devueltas las cantidades avaladas con más los intereses correspondiente por medio de burofax que se acompaña como documento

QUINTO Ante la falta de respuesta de los codemandados esta parte se ve en la obligación de instar la resolución del contrato por medio de la presente demanda, en aplicación de lo dispuesto en el art. 1124 del Código Civil, puesto que se ha producido un incumplimiento grave y culpable de la promotora vendedora, quien a fecha de hoy aun no ha dado inicio a las obras, cuando el plazo de entrega había vencido varios meses atrás. Es decir, que no estamos frente a un supuesto de mora, sino que se ha producido un total y absoluto incumplimiento de la obligación principal del contrato de compraventa, de mala fe, que debe determinar la resolución del contrato con las consecuencias establecidas en el citado artículo 1124 del Código Civil, debiendo la vendedora indemnizar a mi representado en los daños y perjuicios causados, esto es, con devolución de las cantidades entregadas a cuenta con más los intereses.

SEXTO De forma acumulada la acción se dirige contra la entidad bancaria [ENTIDAD BANCARIA], en su condición de avalista solidaria del contrato, siendo de aplicación la Disposición Adicional Primera, apartado Cuatro de la Ley 38/1999, de 5 de noviembre, que establece que una vez expirado el plazo de iniciación de las obras o de entrega de la vivienda sin que una u otra hubiesen tenido lugar, el cesionario, en este caso mi representado, puede rescindir el contrato, con derecho a la devolución de las cantidades entregadas a cuenta, pudiendo incluso optar la vía procesal ejecutiva, por lo que es patente que puede dirigir la acción en el juicio declarativo como se realiza mediante la presente demanda.

Por tanto, de conformidad con lo preceptuado en la disposición adicional primera de la Ley 38/1999, de 5 de noviembre, y en relación con los artículos 1.822 y siguientes del Código Civil, interesamos la condena de la entidad bancaria codemandada en virtud del aval otorgado por la misma a la vendedora en fecha [FECHA]. que se acompaña como documento número [Nº DE DOCUMENTO], debiendo abonar, de forma conjunta y solidaria con la otra condemandada, la cantidad entregada a cuenta de [IMPORTE] euros, con más los intereses correspondientes.

SÉPTIMO.- Mi representado envío un requerimiento fehaciente a las demandadas con fecha [FECHA], que fue contestado por las entidades [DENOMINACIÓN SOCIAL], en los siguientes términos

Acompaño como documentos números [Nº DE DOCUMENTO], los requerimientos efectuados y como documentos números [Nº DE DOCUMENTO], las contestaciones de las codemandadas.

FUNDAMENTOS DE DERECHO

Competencia

Corresponde a los Tribunales de [LOCALIDAD] conforme a lo que dispone el art. 51 de la LEC, en relación con lo dispuesto en el art. 85.1º LOPJ.

Acumulación de acciones

Es de aplicación el art. 72 de la LEC al ser conexas las acciones ejercitadas simultáneamente contra los codemandados.

Legitimación

Le corresponde a esta parte la activa ante la condición de comprador del contrato cuya resolución se interesa y la pasiva a la promotora codemandada en su condición de vendedora, así como a la entidad bancaria en su condición de avalista de las cantidades entregadas a cuenta (art. 10 LEC).

Procedimiento

Es el juicio ordinario con fundamento en el artículo 249.2º LEC al exceder la cuantía de este proceso de 15.000 euros.

Cumplimiento de los requisitos de procedibilidad.

La presente demanda cumple con el requisito de procedibilidad exigido por la disp. adic. 7ª de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

Acción resolutoria

Se ejercita en primer lugar la acción de resolución del contrato de compraventa por incumplimiento del vendedor, siendo de aplicación lo dispuesto en los artículos 1124 del Código Civil en relación con los artículos 1258 y 1461 del Código Civil.

Acción acumulada de reclamación de cantidad

Se ejercita de forma acumulada la acción de reclamación de cantidad contra la entidad bancaria codemandada fundada la misma en la Disposición Adicional Primera, apartado Cuatro de la Ley 38/1999, de 5 de noviembre.

Efectos

Son de aplicación los artículos 1124 del Código Civil y la Disposición Adicional Primera, apartado Cuatro de la Ley 38/1999, de 5 de noviembre, debiendo declararse resuelto el contrato y condenando a las codemandadas a abonar, conjunta y solidariamente, a mi representado las cantidades entregadas a cuenta con los intereses correspondientes desde su entrega.

En materia de costas, es de aplicación el artículo 394 LEC debiendo imponerse a las demandadas.

En base a lo anterior,

SUPLICO al Tribunal que tenga por presentada la presente demanda con los documentos a ella adjuntos y por parte en la representación que ostento se tenga por formulada demanda de acción de resolución de contrato de compraventa y acumulada de reclamación de cantidad frente a [PARTE DEMANDADA] y a [DENOMINACIÓN SOCIAL] y, en su virtud se dicte sentencia por la que por la que se declare resuelto y sin efecto el contrato de compraventa suscrito entre las partes en fecha [FECHA], condenando solidariamente a las codemandadas [DENOMINACIÓN SOCIAL] y [DENOMINACIÓN SOCIAL] a la devolución de las cantidades entregadas a cuenta, que ascienden en su totalidad a [IMPORTE] euros, con más los intereses correspondientes, todo ello con imposición de costas a las citadas demandadas.

OTROSÍ DIGO I que, de conformidad con lo dispuesto en los arts. 251 y 252 de la LEC se fija la cuantía del presente proceso en [IMPORTE] euros.

OTROSÍ DIGO.-Que estando la presente demanda sujeta al abono de la tasa por el ejercicio de la potestad jurisdiccional fijada por la Ley 10/2012, de 20 de noviembre, modificada por RDL 3/2013 y Ley 25/2015, de 28 julio, y desarrollada por Orden HAP/2662/2012, de 13 de diciembre, siendo mi representada personas jurídica no exenta de su pago, se acompaña a la presente demanda como documento nº [Nº DE DOCUMENTO] la correspondiente autoliquidación con el ejemplar para la Administración de Justicia debidamente validado y en el que consta el pago de la cantidad de 300 euros correspondiente a la cuota fija, sin que se incluya la cuota variable prevista en el artículo 7.2 de la Ley 10/2012 al haber sido declarado inconstitucional y nulo por la STC 140/2016, de 21 de julio.

En virtud de lo anterior,

SUPLICO AL TRIBUNAL que tenga por hechas las anteriores manifestaciones a los efectos pertinentes y por acompañado el documento justificativo del abono de la tasa.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma Abogado y Procurador

========================================================================
