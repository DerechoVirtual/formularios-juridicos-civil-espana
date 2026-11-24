---
name: demanda-ejecucion-laudo-arbitral-consumo-civ-1486
description: "Demanda de ejecución de un laudo arbitral de consumo. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de ejecución de un laudo arbitral de consumo

> Formulario **CIV-1486** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Modelo de demanda ejecutiva solicitando se despache ejecución del laudo arbitral dictado por el Colegio Arbitral de la Junta Arbitral de Consumo de la Comunidad Autónoma correspondiente.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de ejecución de un laudo arbitral de consumo» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de ejecución de un laudo arbitral de consumo” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:demanda-ejecucion-laudo-arbitral-consumo-civ-1486`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (7 veces)
- [ ] IMPORTE (6 veces)
- [ ] FECHA (4 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] AÑO
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] DÍA
- [ ] LUGAR
- [ ] MES
- [ ] Nº
- [ ] NÚMERO
- [ ] OTROS DATOS
- [ ] SEDE

## Normas que cita el formulario

- art. 548 LEC
- art. 85.1 LOPJ
- art. 550 LEC
- art. 517 LEC
- art. 551.2.3 LEC
- art. 551.3.1 LEC
- art. 590 LEC
- art. 551.3.2 LEC
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

- Junto a «…Proceso número [NÚMERO] A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

Proceso número [NÚMERO]

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D. [NOMBRE Y APELLIDOS] Procurador de los Tribunales en representación de D. según consta acreditado en los Autos arriba expresados ante el Tribunal comparezco y como mejor en derecho proceda DIGO:

Que por medio de la presente demanda y en la meritada representación solicito la ejecución del laudo de fecha [FECHA] dictado por la Corte de Arbitraje de [LOCALIDAD], en reclamación de la suma de [IMPORTE] euros en concepto de principal e intereses vencidos, con más la cantidad de [IMPORTE] euros, que se presupuesta en concepto de intereses que se pueden devengar en la presente ejecución y costas, la cual dirijo contra D [NOMBRE Y APELLIDOS] con base en los siguientes:

HECHOS

Que el ejecutante y el ejecutado se sometieron a la Corte de Arbitraje de [LOCALIDAD] para la resolución de los conflictos derivados del contrato de fecha [FECHA], en virtud de convenio arbitral que se acompaña como documento

Seguido el procedimiento arbitral de forma contradictoria y por los trámites prevenidos legalmente, por el árbitro se dictó laudo en fecha [FECHA], cuya parte dispositiva es la siguiente:

El laudo fue notificado a las partes el día [FECHA]

(se acompañan como documentos [Nº DE DOCUMENTO] laudo arbitral y copias de las diligencias de notificación a las partes).

Que habiendo transcurrido el plazo prevenido en el artículo 548 de la LEC sin que se haya hecho efectiva la deuda por la parte condenada al pago, es por lo que se interesa su ejecución.

FUNDAMENTOS DE DERECHO

Competencia

Artículo 545.2 de la LEC, en relación con lo dispuesto en el art. 85.1º LOPJ: Es competente el Tribunal al que me dirijo por cuanto el título es un laudo arbitral, siendo competente para denegar o autorizar la ejecución y el correspondiente despacho el Tribunal de Instancia del lugar en que se hubiera dictado.

Procedimiento

Artículo 548, procediéndose a despachar ejecución de la sentencia dentro de los veinte días posteriores a aquél en que la condena haya sido notificada al ejecutado.

Artículo 549 LEC en relación con el que debe ser el contenido de la demanda ejecutiva y artículo 550 de la LEC en cuanto a los documentos a aportar, estableciendo que cuando el título sea un laudo arbitral, se acompañará, además, el convenio arbitral y los documentos justificativos de la notificación del laudo a las partes.

Artículos 551 a 554 LEC en relación al despacho de ejecución.

Título ejecutivo

Artículo 517.2.2 de la LEC: "Los laudos o resoluciones arbitrales y los acuerdos de mediación, debiendo estos últimos haber sido elevados a escritura pública de acuerdo con la Ley de mediación en asuntos civiles y mercantiles".

Tutela ejecutiva

Se interesa el despacho de ejecución por la cantidad de [IMPORTE] euros, que se condenó a pagar al ejecutado en el laudo arbitral que se ejecuta, con más la de [IMPORTE] euros presupuestadas para intereses y costas, conforme al artículo 517 LEC, en relación con los artículos 571 y ss. para la ejecución dineraria.

Costas

Artículo 539.2 LEC.

Por todo ello,

SUPLICO AL TRIBUNAL: Que teniendo por presentado este escrito con los documentos que lo acompañan y sus copias, se acuerde, sin necesidad de previo requerimiento al deudor, se dicte auto conteniendo la orden general de ejecución y despachando la misma, en el que conforme al artículo 551.2.3º LEC fije la cantidad reclamada conforme a lo solicitado en la cantidad de [IMPORTE] euros en concepto de principal, más la cantidad de [IMPORTE] euros en concepto de intereses, gastos y costas.

OTROSÍ DIGO: Que, una vez dictado el auto general de ejecución y de conformidad con el art. 551.3.1º de la LEC, se solicita que por el Letrado de la Administración de Justicia responsable de la misma se dicte decreto procediéndose al embargo, sin previo requerimiento de pago del ejecutado por la cantidad indicada, de los siguientes bienes que se estiman suficientes para cubrir las indicadas responsabilidades en su totalidad:

(se designarían bienes en su caso [DESCRIPCIÓN DEL BIEN])

Por lo que, SUPLICO que se dicte decreto en el que se contengan las medidas que dejo interesadas.

OTROSÍ DIGO II: Que desconociendo esta parte bienes que puedan ser objeto de embargo por parte de este Tribunal, al amparo de lo dispuesto en el artículo 590 LEC, esta parte solicita que, una vez dictado el auto general de ejecución y de conformidad con el art. 551.3.2º de la LEC, el Tribunal proceda a dirigirse a los efectos de determinación de la relación de bienes muebles e inmuebles, así como depósitos o imposiciones a plazo fijo que el ejecutado pueda tener a su nombre a los siguientes organismos:

1. Gerencia Territorial del Catastro de [LOCALIDAD]

2. Delegación Territorial de la Agencia Tributaria de [LOCALIDAD]

3. Registro de la Propiedad núm. [Nº] de [LOCALIDAD]

4. Jefatura Provincial de Tráfico de [LOCALIDAD]

5. Caja de Ahorros Provincial de [LOCALIDAD]

Por lo que, SUPLICO que se dicte decreto procediéndose a adoptar las medidas de localización y averiguación de bienes solicitadas.

OTROSÍ DIGO III.- Que estando la presente demanda sujeta al abono de la tasa por el ejercicio de la potestad jurisdiccional fijada por la Ley 10/2012, de 20 de noviembre, modificada por RDL 3/2013 y Ley 25/2015, de 28 julio, y desarrollada por Orden HAP/2662/2012, de 13 de diciembre, siendo mi representada personas jurídica no exenta de su pago, se acompaña a la presente demanda como documento nº [Nº DE DOCUMENTO] la correspondiente autoliquidación con el ejemplar para la Administración de Justicia debidamente validado y en el que consta el pago de la cantidad de 200 euros correspondiente a la cuota fija [OTROS DATOS], sin que se incluya la cuota variable prevista en el artículo 7.2 de la Ley 10/2012 al haber sido declarado inconstitucional y nulo por la STC 140/2016, de 21 de julio.

En virtud de lo anterior,

SUPLICO AL TRIBUNAL: que tenga por hecha la anterior manifestación a los efectos pertinentes y por acompañado el documento justificativo del abono de la tasa.

Es justicia que pido en [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma Abogado y Procurador

========================================================================
