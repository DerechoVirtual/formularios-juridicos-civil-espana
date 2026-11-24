---
name: recurso-directo-revision-contra-decreto-laj-deniega-civ-1526
description: "Recurso directo de revisión contra el decreto del LAJ que deniega la mejora de embargo. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Recurso directo de revisión contra el decreto del LAJ que deniega la mejora de embargo

> Formulario **CIV-1526** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **recursos**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Recurso directo de revisión contra el decreto del LAJ que deniega la mejora de embargo» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Recurso directo de revisión contra el decreto del LAJ que deniega la mejora de embargo” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:recurso-directo-revision-contra-decreto-laj-deniega-civ-1526`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (4 veces)
- [ ] IMPORTE (2 veces)
- [ ] DÍA
- [ ] FUNDAMENTOS
- [ ] LOCALIDAD
- [ ] MES
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] NOMBRE Y APELLIDOS
- [ ] Nº
- [ ] Nº DE PROCEDIMIENTO
- [ ] SEDE

## Normas que cita el formulario

- art. 612 LEC
- art. 612.3 LEC

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

- Junto a «…ejecución A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
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

Proceso de ejecución

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D. [NOMBRE Y APELLIDOS], Procurador de los Tribunales y de [NOMBRE DEL REPRESENTADO/A], según tengo acreditado en los autos de proceso civil [Nº DE PROCEDIMIENTO] arriba referenciados, ante el Tribunal comparezco y como mejor proceda en derecho DIGO:

Que habiendo sido notificado a esta representación el decreto de fecha [FECHA], dictado por el Letrado de la Administración de Justicia del órgano al que me dirijo, por el que se deniega la mejora de embargo solicitada por esta parte, al amparo del art. 454 bis y 551.5 de la LEC, interpongo recurso directo de revisión de la mencionada resolución citando como infringido el mismo artículo 612 de la Ley de Enjuiciamiento Civil en base a los siguientes motivos:

MOTIVOS

El decreto recurrido deniega la mejora de embargo interesada por esta parte, con lo que se infringe lo dispuesto en el artículo 612 de la LEC, por cuanto se han producido nuevas circunstancias que hacen dudar de la suficiencia de los bienes embargados en relación con la exacción de responsabilidad del ejecutado.

Tal como se exponía en nuestro escrito de solicitud de mejora de embargo, las nuevas circunstancias que hacen dudar de la suficiencia de los bienes consisten en que se constató que se había anotado previamente otro embargo en cuanto al piso titularidad del ejecutado, lo cual se constató con posterioridad a decretarse el embargo, al expedir la certificación el Registro de la Propiedad en fecha [FECHA], tal como consta en autos.

Habida cuenta del importe del que debe responder el inmueble por la anotación anterior, es evidente que prácticamente cubre todo el valor del inmueble, siendo fácilmente pronosticable que no existirá sobrante o que, si lo hay, será muy escaso.

Ello supone una manifiesta insuficiencia del embargo trabado, por cuanto el resto de los bienes embargados apenas cubren una mínima parte de la deuda, quedando prácticamente sin posibilidad de realizarse el bien de mayor valor, que era el piso del ejecutado, por haberse anotado anteriormente otro embargo, preferente, que cubre todo su valor.

En consecuencia, entendemos que concurren los requisitos del art. 612 de la LEC para decretar la mejora del embargo, puesto que los hechos manifestados justifican la necesidad de ampliar el embargo, dándose el supuesto de hecho prevenido en el referido art. 612 por cuanto, en la sustanciación de este proceso de ejecución, se ha producido un cambio de las circunstancias que permite dudar de la suficiencia de los bienes embargados en relación con la exacción de responsabilidad del ejecutado, tal como se ha expuesto.

Por ello solicitamos que se revise el decreto recurrido, acordando en su lugar la mejora de embargo instada por esta parte.

El decreto recurrido deniega la mejora de embargo interesada por esta parte, con lo que se infringe lo dispuesto en el artículo 612.3 de la LEC en relación con los artículos 578.3 y 613.4 de la LEC.

La mejora de embargo es procedente por cuanto por auto de fecha [FECHA] se dio lugar la ampliación de la ejecución por vencimiento de nuevos plazos de la deuda en virtud de la cual se proceda, con lo cual se incrementó el montante de la ejecución en la cantidad de [IMPORTE] euros por principal y [IMPORTE] euros por intereses, no siendo suficientes los bienes embargados inicialmente para cubrir dichos importes.

Asimismo, la mejora de embargo es procedente puesto que ha existido un aumento de la cantidad prevista para intereses y costas, tal como se justificaba en nuestro escrito de petición de mejora, y debido a la dilación de este proceso de ejecución y a los distintos trámites contradictorios que se han venido siguiendo, en los que han sido impuestas las costas al ejecutado, que ha incrementado notablemente la cantidad correspondiente a estas partidas, tal como justificábamos en la documentación aportada.

Por ello solicitamos también por estos motivos que se revise el decreto recurrido, acordando en su lugar la mejora de embargo instada por esta parte.

El decreto impugnado infringe lo dispuesto en el art. de la Ley de Enjuiciamiento Civil por cuanto [FUNDAMENTOS]

En consecuencia, se solicita también por este motivo revocar el Decreto impugnado y en su lugar acordar de conformidad a lo interesado por esta parte en su solicitud de mejora de embargo.

En su virtud,

SUPLICO AL TRIBUNAL que teniendo por presentado este escrito, con justificante de traslado, se sirva admitirlo, tener por interpuesto recurso directo de revisión contra el decreto dictado por el Letrado de la Administración de Justicia de ese órgano de fecha [FECHA] y, tras los trámites legales, se dicte por el Tribunal auto por el que se revoque y deje sin efecto el Decreto impugnado, ordenando en su lugar que se decrete la mejora de embargo solicitada por esta representación.

OTROSÍ DIGO que, de conformidad con lo dispuesto en los apartados 4 y 6 de la disposición adicional decimoquinta de la LOPJ acompaño a este escrito resguardo de consignación en la cuenta de Depósitos y Consignaciones abierta a nombre del Tribunal del depósito exigido para interponer el recurso por importe de 25 euros.

Por lo que SUPLICO AL TRIBUNAL que tenga por constituido el depósito, dejando interesada desde este momento su devolución para el caso de estimación total o parcial del recurso

En [LOCALIDAD], a [DÍA], de [MES] del año

========================================================================
