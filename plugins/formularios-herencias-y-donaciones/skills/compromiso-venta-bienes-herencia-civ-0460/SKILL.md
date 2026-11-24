---
name: compromiso-venta-bienes-herencia-civ-0460
description: "Compromiso de venta de bienes de la herencia. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Compromiso de venta de bienes de la herencia

> Formulario **CIV-0460** del plugin **Herencias, testamentos y donaciones** (`formularios-herencias-y-donaciones`) · Civil › Sucesiones y donaciones · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Compromiso de venta de bienes de la herencia» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Compromiso de venta de bienes de la herencia” para mi caso». También puedes invocarla directamente con `/formularios-herencias-y-donaciones:compromiso-venta-bienes-herencia-civ-0460`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-herencias-y-donaciones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Herencias, testamentos y donaciones) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] AÑO (3 veces)
- [ ] DÍA (3 veces)
- [ ] FRACCIÓN (TERCERAS / CUARTAS PARTES...) (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] MES (3 veces)
- [ ] IMPORTE (2 veces)
- [ ] Nº (2 veces)
- [ ] CALLE
- [ ] LETRA
- [ ] LUGAR
- [ ] Nº DE HIJOS
- [ ] Nº DE INMOBILIARIAS
- [ ] PISO

## Normas que cita el formulario

- No cita artículos concretos; Claude localizará las normas aplicables con Jurisprudenciator si el documento las necesita.

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

### Avisos de actualización (0) — se aplican en el texto, nunca se copian en el documento

- Ninguno.

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

COMPROMISO DE VENTA DE BIENES HEREDITARIOS

En [LUGAR], a [DÍA] de [MES] de [AÑO].

INTERVIENEN

Todas las partes en su propio nombre y derecho, así mismo con la capacidad y legitimación para contratar que recíprocamente se reconocen, los comparecientes han convenido otorgar el presente COMPROMISO DE VENTA DE BIENES HEREDITARIOS, y a tal efecto y de común acuerdo,

EXPONEN

I.- Que los comparecientes forman la herencia yaciente de D.. [NOMBRE Y APELLIDOS]

II.- Que D. [NOMBRE Y APELLIDOS], falleció el [DÍA] de [MES] de [AÑO], habiendo manifestado su última voluntad otorgando testamento abierto ante el Iltre. Notario de [LOCALIDAD], D. [NOMBRE Y APELLIDOS], en virtud del cual declara herederos universales, por [FRACCIÓN (TERCERAS / CUARTAS PARTES...)] e iguales partes a sus [Nº DE HIJOS] hijos, quienes suscriben el presente documento privado.

III.-Que a la fecha de su fallecimiento, D. [NOMBRE Y APELLIDOS], era propietaria de los siguientes bienes:

• Un bien inmueble, concretamente la vivienda sita en la calle [CALLE] número de portal [Nº] piso [PISO], letra [LETRA] del municipio de [LOCALIDAD], con la salvedad que a continuación se expresará.

CLÁUSULAS

Objeto

Que los herederos de común acuerdo han decido poner la vivienda mencionada en el exponiendo III a la venta, atribuyendo la venta a [Nº DE INMOBILIARIAS] inmobiliarias del término municipal de [LOCALIDAD], previa consulta del precio a las referidas inmobiliarias, al fin de ajustar el precio de la venta al valor real del mercado.

Fijación del precio

El precio de salida del inmueble se fija en [IMPORTE] EUROS ( €), autorizando los comparecientes al letrado D. [NOMBRE Y APELLIDOS] para negociar el precio definitivo con los posibles futuros adquirentes con el límite del valor mínimo de venta de [IMPORTE] euros ( €), no admitiéndose en este acto, y por el momento, cantidad inferior alguna a esta última reseñada. Que en el supuesto que el valor de mercado atribuido por la consulta sea inferior a 198.334 euros, este último será el precio inicial de venta.

Terceros compradores

Si alguno de los comparecientes presentase a un tercero interesado en la compraventa, siempre que el precio ofrecido se encontrase dentro de los límites referidos en el pacto I y no hubiese mejor oferta que lo superase, el presentado tendrá la preferencia para dicha adquisición según el orden de llegada (caso de ser varios), quedando los comparecientes obligados a la escritura traslativa correspondiente.

Transmisión

La transmisión se efectuará libre de toda carga y/o gravamen y al corriente de pago de IBI y de inscripción, siendo todos los gastos de la transmisión de cuenta de la parte compradora, excepto el impuesto sobre el incremento de val valor de los terrenos de naturaleza urbana, si lo hubiere, que será de cuenta y cargo de la parte vendedora. Que delegan las gestiones a realizar con dichas inmobiliarias en los Despachos Profesionales de los Letrados Inmaculada Larrinaga y Fernando San José, como representantes de los tres herederos, la primera de José Luis y el segundo de Ernesto Ángel y Francisco Javier.

Gastos e impuestos

Que los gastos de la valoración inmobiliaria y los que pudieran surgir de las gestiones de venta realizadas por las inmobiliarias se sufragarán por [FRACCIÓN (TERCERAS / CUARTAS PARTES...)] e iguales partes entre los herederos.

Que los herederos acuerdan sufragar por [FRACCIÓN (TERCERAS / CUARTAS PARTES...)] e iguales partes los impuestos y plusvalías que deriven de la venta del inmueble, así como los impuestos y gastos que de la vivienda hayan tenido origen, desde el fallecimiento de la causante, previa exhibición de justificantes de los mismos.

Depósito de llaves

Que con anterioridad a depositar las llaves de la vivienda en dichas inmobiliarias, los herederos convienen en retirar y disponer cada uno de los bienes del ajuar y mobiliario que les han sido adjudicados que igualmente firman en prueba de conformidad, con anterioridad al [DÍA] de [MES] de [AÑO], al fin de facilitar la labor de las inmobiliarias y evitar cualquier tipo de pérdida o deterioro de los bienes.

Apoderamiento

Que los comparecientes acuerdan conferir poder suficiente al Letrado D. [NOMBRE Y APELLIDOS] para que en su nombre y representación firme cuantos documentos públicos o privados sean necesarios para proceder a la venta del inmueble en los términos convenidos en la estipulación segunda y tercera del presente contrato, sin necesidad de previo acuerdo entre las partes.

Duración

El presente compromiso de venta tiene una duración de [Nº] años.

Notificaciones

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje

[ELEGIR UNA OPCIÓN: Sumisión a Tribunales / Sin cláusula penal en caso de no ejecución voluntaria de la sentencia / Notificaciones / — y además elegir: Sumisión a arbitraje / Sin cláusula penal en caso de no ejecución voluntaria del laudo / Con cláusula penal en caso de no ejecución voluntaria del laudo]

Generalidades

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este Contrato.

Y en prueba de conformidad, firman las partes el presente contrato por triplicado y a un solo efecto en el lugar y fecha expresados en el encabezamiento.

========================================================================
