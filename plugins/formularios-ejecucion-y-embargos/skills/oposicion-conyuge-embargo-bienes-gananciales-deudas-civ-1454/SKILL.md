---
name: oposicion-conyuge-embargo-bienes-gananciales-deudas-civ-1454
description: "Oposición del cónyuge al embargo de bienes gananciales por deudas del consorte (art. 541.2 LEC). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Oposición del cónyuge al embargo de bienes gananciales por deudas del consorte (art. 541.2 LEC)

> Formulario **CIV-1454** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Oposición del cónyuge al embargo de bienes gananciales por deudas del consorte (art. 541.2 LEC)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Oposición del cónyuge al embargo de bienes gananciales por deudas del consorte (art. 541.2 LEC)” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:oposicion-conyuge-embargo-bienes-gananciales-deudas-civ-1454`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] AÑO (5 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] DÍA (3 veces)
- [ ] MES (3 veces)
- [ ] Nº (3 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] CALLE
- [ ] COLEGIO
- [ ] DESCRIPCIÓN DE LOS DOCUMENTOS
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] NÚMERO
- [ ] SEDE

## Normas que cita el formulario

- art. 541.2 LEC
- art. 541 LEC
- art. 1373 CC
- art. 560 LEC
- art. 539.1 LEC
- art. 1365 CC
- art. 539.2.I LEC
- art. 541.3 LEC

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

### Avisos de actualización (3) — se aplican en el texto, nunca se copian en el documento

- Junto a «…Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).
- Junto a «…2666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.

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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D./Dª [NOMBRE Y APELLIDOS], Procurador de los Tribunales y de D./Dª [NOMBRE Y APELLIDOS], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], bajo la dirección técnica de D./Dª [NOMBRE Y APELLIDOS], Letrado del Ilustre Colegio de [COLEGIO], con despacho profesional en [LOCALIDAD], calle [CALLE], nº [NÚMERO], pta., ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que por medio del presente escrito, siguiendo instrucciones de mi representado/a, planteo OPOSICIÓN A LA EJECUCIÓN SOBRE BIENES GANANCIALES decretada en el procedimiento de Ejecución de Título Judicial o título ejecutivo que corresponda nº [Nº]/[AÑO], seguido contra D./Dª [NOMBRE Y APELLIDOS], cónyuge de mi representado/a, con base en los siguientes

HECHOS

En fecha [DÍA] de [MES] de [AÑO], se notificó a mi representado/a el embargo de bienes gananciales trabado en el procedimiento de Ejecución de Título Judicial o título ejecutivo que corresponda nº [Nº]/[AÑO], seguido contra su cónyuge, D./Dª [NOMBRE Y APELLIDOS], dándole traslado del auto que despachó la ejecución, de fecha [DÍA] de [MES] de [AÑO], y de la demanda ejecutiva, en cumplimiento del artículo 541.2 LEC y advirtiéndole de las posibilidades de actuación en el proceso conforme a lo dispuesto en el art. 541 LEC, fijándose el plazo de diez días para su eventual oposición a la ejecución.

Por el presente escrito mi representado se opone al citado embargo por ser la deuda privativa o propia del ejecutado, su cónyuge, en cuyo exclusivo interés fue contraída sin que pueda incardinarse en ninguno de los supuestos de deudas consorciales regulados por el Código civil, y sin que, por tanto, deba responderse de la misma con los bienes gananciales más allá de la participación que en los mismos corresponde al deudor ejecutado. Por ello y conforme a lo dispuesto en el artículo 1373 CC, solicita que en la traba se sustituyan los bienes comunes por la parte que ostenta el cónyuge deudor en la sociedad conyugal, a cuyo efecto se disolverá y liquidará ésta, siguiendo el embargo sobre los bienes que finalmente sean adjudicados a título privativo al deudor ejecutado.

Resultan aplicables a los anteriores hechos, los siguientes

FUNDAMENTOS DE DERECHO

TRAMITACIÓN DE LA OPOSICIÓN.- Se trata de una oposición de fondo a la ejecución en sentido técnico, basada en no ser la deuda consorcial, sino privativa o propia del deudor ejecutado, conforme a lo dispuesto en el art. 541.2 LEC, en relación con el art. 1373 CC.

El art. 541.2 LEC añade el citado motivo de oposición a la ejecución, a los contemplados en ños arts. 556 y ss. LEC.

La oposición se sustanciará por los trámites del incidente de oposición a la ejecución regulado en los arts. 556 y ss. LEC, atendiendo en especial a lo dispuesto en los arts. 560 y 561 LEC, sobre oposición de fondo a la ejecución, no afectando la resolución de este incidente a la existencia ni subsistencia de la deuda, ni a la procedencia de su ejecución, sino tan solo a la afección de los bienes que han de ser objeto de la traba y del apremio.

CAPACIDAD.- Ambas partes tienen capacidad para serlo, conforme a lo dispuesto en los artículos 6 y ss. LEC.

LEGITIMACIÓN.- Está legitimado mi representado, como cónyuge del ejecutado, conforme al art. 541.2 LEC.

REPRESENTACIÓN Y DEFENSA.- El/La demandante comparece representado y defendido, respectivamente, por el Procurador y el Letrado que constan en el encabezamiento de este escrito, de acuerdo con lo dispuesto en el art. 539.1 LEC.

DERECHO SUSTANTIVO.- Las deudas contraídas por un cónyuge han de considerarse privativas del mismo, mientras no quede probado en el procedimiento su carácter consorcial, recayendo la carga de la prueba en el acreedor demandante, según resulta, del art. 541.2 LEC, que dispone: "Cuando la ejecución se siga a causa de deudas contraídas por uno de los cónyuges, pero de las que deba responder la sociedad de gananciales, la demanda ejecutiva podrá dirigirse únicamente contra el cónyuge deudor, pero el embargo de bienes gananciales habrá de notificarse al otro cónyuge, dándole traslado de la demanda ejecutiva y del auto que despache ejecución a fin de que, dentro del plazo ordinario, pueda oponerse a la ejecución. La oposición a la ejecución podrá fundarse en las mismas causas que correspondan al ejecutado y, además, en que los bienes gananciales no deben responder de la deuda por la que se haya despachado la ejecución.

Cuando la oposición se funde en esta última causa, corresponderá al acreedor probar la responsabilidad de los bienes gananciales. Si no se acreditara esta responsabilidad, el cónyuge del ejecutado podrá pedir la disolución de la sociedad conyugal conforme a lo dispuesto en el apartado siguiente".

Acoge este precepto la tesis que se había extendido anteriormente en un importante sector doctrinal y de la que se hizo eco la DGRN en numerosas ocasiones. Pueden citarse, entre otras muchas, las RRDGRN de 16 de febrero de 1987, 24 de noviembre de 1987, 4 de junio de 1991 o 18 de julio de 1991.

Así pues, mientras no se demuestre el carácter consorcial de la deuda, cosa que no ha sucedido en el procedimiento que culmina con la ejecución a que se opone mi representado, aquélla deberá ser tratada como privativa, por lo que los bienes gananciales sólo responderán de modo subsidiario y en los términos del art. 1373 CC, tal y como reconoce el citado art. 541 LEC. En efecto, el art. 541 LEC señala en el último inciso del apartado 2 que si el acreedor no acredita el carácter consorcial de la deuda, el cónyuge del ejecutado podrá pedir la disolución de la sociedad conyugal conforme a lo dispuesto en el apartado siguiente. El apartado siguiente, el 3, dedicado a la ejecución de deudas propias o privativas de uno de los cónyuges, determina: "Si la ejecución se siguiere a causa de deudas propias de uno de los cónyuges y se persiguiesen bienes comunes a falta o por insuficiencia de los privativos, el embargo de aquéllos habrá de notificarse al cónyuge no deudor. En tal caso, si éste optare por pedir la disolución de la sociedad conyugal, el tribunal, oídos los cónyuges, resolverá lo procedente sobre división del patrimonio y, en su caso, acordará que se lleve a cabo con arreglo a lo dispuesto en esta Ley, suspendiéndose entre tanto la ejecución en lo relativo a los bienes comunes".

Por otra parte, aunque la carga de la prueba no corresponde a mi representado, según lo que acaba de exponerse, lo cierto es que la deuda, contraída por su cónyuge, ejecutado en este procedimiento, tiene carácter privativo, al no poder inscribirse en ninguno de los supuestos regulados en los arts. 1365, 1366 y 1368 CC. Se justifica lo anterior con mayor detalle, según el tipo de deuda, aludiendo a las circunstancias del caso

Se acompañan como Documentos nos, [Nº DE DOCUMENTO] y [Nº DE DOCUMENTO] los siguientes: [DESCRIPCIÓN DE LOS DOCUMENTOS], de los que resulta el carácter privativo de la deuda, según lo antes expuesto.

Por ello, de acuerdo con lo establecido en el art. 541.2 y 3 LEC, en relación con el art. 1373 CC, debe darse a mi representado la oportunidad de pedir la disolución de la sociedad conyugal.

COSTAS.- Procede imponer al/a la ejecutante el pago de las costas, en virtud de lo dispuesto en el art. 561.2, y en el art. 539.2.I, ambos de la LEC.

Iura novit curia

En su virtud:

SUPLICO AL TRIBUNAL: Que teniendo por presentado este escrito en tiempo y forma con los documentos que se acompañan y justificante de haber entregado copia de todo ello a los Procuradores de ejecutante y ejecutado, se sirva admitirlo, se me tenga por personado, entendiéndose conmigo las ulteriores diligencias, tenga por interpuesto INCIDENTE DE OPOSICIÓN A LA EJECUCIÓN, y tras los trámites legales oportunos, dicte resolución en la que se declare el carácter privativo de la deuda ejecutada y se acuerde proceder a la disolución de la sociedad conyugal y a su liquidación por los cauces legales, conforme a lo establecido en el art. 541.3 LEC, sustituyéndose el embargo practicado sobre los bienes gananciales por el de los que sean adjudicados al deudor ejecutado como consecuencia de la liquidación de la sociedad de gananciales, suspendiéndose, entre tanto, la ejecución en lo relativo a los bienes comunes, con imposición de las costas de la ejecución al/la ejecutante.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma y número del Letrado	Firma del Procurador

========================================================================
