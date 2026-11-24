---
name: denuncia-judicial-extravio-pagare-civ-1163
description: "Denuncia judicial por extravío de un pagaré. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Denuncia judicial por extravío de un pagaré

> Formulario **CIV-1163** del plugin **Cobrar deudas: monitorio y cambiario** (`formularios-reclamar-deudas-monitorio`) · Civil › Monitorio y cambiario · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Denuncia judicial por extravío de un pagaré» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Denuncia judicial por extravío de un pagaré” para mi caso». También puedes invocarla directamente con `/formularios-reclamar-deudas-monitorio:denuncia-judicial-extravio-pagare-civ-1163`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-reclamar-deudas-monitorio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Cobrar deudas: monitorio y cambiario) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (10 veces)
- [ ] LOCALIDAD (8 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] ENTIDAD BANCARIA (2 veces)
- [ ] FECHA (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] LUGAR
- [ ] MES
- [ ] NOMBRE DE LA PARTE
- [ ] NOMBRE DE LA SUCURSAL
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº DE CLÁUSULA
- [ ] Nº DE COLEGIADO/A
- [ ] SEDE
- [ ] SERIE

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

A LA SECCIÓN DE LO MERCANTIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, actuando en nombre y representación de [NOMBRE DEL REPRESENTADO/A], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño a este escrito, bajo la dirección letrada de D. [NOMBRE Y APELLIDOS], Abogado del Iltre. Colegio de [LOCALIDAD], con número de colegiado [Nº DE COLEGIADO/A], ante el Tribunal comparezco y como mejor proceda en Derecho DIGO:

- Que en la representación que ostento, al amparo de lo dispuesto en los arts. 132 y siguientes de la Ley de Jurisdicción Voluntaria, por medio del presente escrito, formulo SOLICITUD DE EXPEDIENTE DE JURISDICCIÓN VOLUNTARIA POR EXTRAVÍO DE PAGARÉdel que es legítimo tenedor mi representado, solicitando que se dé traslado al firmante D. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], la cual fundo en los siguientes:

HECHOS

Mi representado es legítimo tenedor del pagaré emitido el pasado día [FECHA], en la localidad de [LOCALIDAD], cuyo firmante es D. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], por importe de [IMPORTE] euros, el cual vence el próximo día [FECHA] y cuyo pago debía efectuarse en la localidad de [LOCALIDAD], entidad bancaria [ENTIDAD BANCARIA], número de cuenta

El citado pagaré fue emitido como consecuencia de las relaciones comerciales entre mi representado y el firmante D. [NOMBRE Y APELLIDOS], en virtud de las cuales el firmante adeudaba la cantidad de [IMPORTE] euros, emitiéndose el pagaré con el número de serie [SERIE], del talonario emitido por la entidad bancaria [ENTIDAD BANCARIA], sucursal de [LOCALIDAD] (se acompaña como documentos número [Nº DE DOCUMENTO], copia del contrato de reconocimiento de deuda en cuya cláusula [Nº DE CLÁUSULA] consta la emisión del pagaré y copia del pagaré cuyo original se ha extraviado).

El original del citado pagaré estaba en poder de mi mandante, quien lo guardó con diferente documentación de su empresa, archivándolo para su cobro al vencimiento.

Aproximándose la fecha de cobro, mi representado tras revisar reiteradamente la documentación de su empresa, no ha podido encontrar el original del pagaré, estando en la certeza que el mismo se ha traspapelado con otra documentación, de manera que se ha producido su extravío, por lo que se ve en la obligación de acudir a esta vía para que se declare la amortización del título y se reconozca el derecho de mi representado a exigir el pago de su crédito.

A efectos de acreditar la veracidad de estos hechos, esta parte propone los medios de prueba indicados en el otrosí de este escrito, aportando como prueba documental copia del título extraviado y del contrato de reconocimiento de deuda (documentos [Nº DE DOCUMENTO]) y propondrá asimismo la testifical de D. [NOMBRE Y APELLIDOS], empleado de la empresa de mi representado, quien podrá dar razón del extravío de la letra y de las circunstancias en que se produjo, así como de D. [NOMBRE Y APELLIDOS], Director de la sucursal bancaria de domiciliación del pagaré, quien podrá dar cuenta de la efectiva existencia del mismo y de su importe.

FUNDAMENTOS DE DERECHO

COMPETENCIA. Son competentes los Jueces de lo Mercantil de esta ciudad por ser el lugar de pago, conforme dispone el art. 133.1 de la Ley de Jurisdicción Voluntaria.

PROCEDIMIENTO. Debe seguirse el procedimiento establecido en los artículos 132 a 135 de la Ley de Jurisdicción Voluntaria.

LEGITIMACIÓN Y POSTULACIÓN. El artículo 133.2 de la Ley de Jurisdicción Voluntaria establece la legitimación del poseedor legítimo que hubiere sufrido el extravío del título, compareciendo con Abogado y Procurador tal como establece el art. 133.3 de la Ley de Jurisdicción Voluntaria.

PROCEDENCIA DE LA ACCIÓN. Artículo 135 de la Ley de Jurisdicción Voluntaria, debiendo ser autorizado mi representado a la percepción del importe del pagaré, una vez cumplidos los trámites legales.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL: Tenga por presentado este escrito y demás documentos junto con las copias que se acompañan a las que se dará el curso legal, lo admita, me tenga por comparecido y parte en la representación que ostento de [NOMBRE DE LA PARTE], entendiéndose conmigo las sucesivas diligencias. Y tenga por formulada solicitud de expediente de jurisdicción voluntaria por extravío de pagaré descrito en el hecho primero, disponiendo la citación del firmante y dar publicidad al expediente, y tras los trámites legales, se dicte decreto disponiendo la suspensión del pago del crédito y, transcurrido el plazo legal, se dicte resolución autorizando a mi representado al cobro de su crédito en la fecha de vencimiento.

OTROSÍ PRIMERO DIGO: Que, para su práctica en la comparecencia, y sin perjuicio de las demás pruebas que se propondrán oportunamente, intereso la citación de los siguientes testigos: [NOMBRE Y APELLIDOS], propongo los siguientes medios de prueba:

- D. [NOMBRE Y APELLIDOS], empleado de la empresa [DENOMINACIÓN SOCIAL], con domicilio en [LOCALIDAD]

- D. [NOMBRE Y APELLIDOS], director de la sucursal [NOMBRE DE LA SUCURSAL] de la entidad [DENOMINACIÓN SOCIAL], con domicilio en [LOCALIDAD]

SUPLICO AL TRIBUNAL: Tenga por anunciada la proposición de los medios de prueba indicados, acordando la citación de los referidos testigos para la comparecencia.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma de Abogado y Procurador

========================================================================
