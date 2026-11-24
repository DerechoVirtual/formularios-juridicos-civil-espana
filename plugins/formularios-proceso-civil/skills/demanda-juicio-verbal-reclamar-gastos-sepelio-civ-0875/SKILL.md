---
name: demanda-juicio-verbal-reclamar-gastos-sepelio-civ-0875
description: "Demanda de juicio verbal para reclamar los gastos del sepelio. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio verbal para reclamar los gastos del sepelio

> Formulario **CIV-0875** del plugin **Proceso civil: demandas, contestaciones, prueba y vista** (`formularios-proceso-civil`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio verbal para reclamar los gastos del sepelio» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio verbal para reclamar los gastos del sepelio” para mi caso». También puedes invocarla directamente con `/formularios-proceso-civil:demanda-juicio-verbal-reclamar-gastos-sepelio-civ-0875`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-proceso-civil:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso civil: demandas, contestaciones, prueba y vista) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] IMPORTE (4 veces)
- [ ] AÑO (2 veces)
- [ ] DÍA (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] MES (2 veces)
- [ ] CALLE
- [ ] CAUSA
- [ ] COLEGIO
- [ ] LUGAR
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº DE COLEGIADO/A
- [ ] Nº DE DOCUMENTO
- [ ] SEDE

## Normas que cita el formulario

- art. 85.1 LOPJ
- art. 6 LEC
- art. 250.2 LEC
- art. 251.1 LEC
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 1100 Código Civil
- art. 394.1 LEC
- art. 50.1 LEC
- art. 23 LEC
- art. 730 LEC
- art. 726 LEC
- art. 728.1 LEC
- art. 728.2 LEC
- art. 733.2 LEC
- art. 736.1 LEC
- art. 733 LEC

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

- Junto a «… SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE QUE POR TURNO DE REPARTO CORRESPONDA»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE QUE POR TURNO DE REPARTO CORRESPONDA

[NOMBRE Y APELLIDOS], Procuradora de los Tribunales y de [NOMBRE DEL REPRESENTADO/A], según acredito por certificación del registro electrónico de apoderamientos judiciales que acompaño (o mediante designación apud acta ante el Letrado de la Administración de Justicia de [SEDE]), bajo la dirección Letrada de [NOMBRE Y APELLIDOS], colegiado/a nº [Nº DE COLEGIADO/A] del Ilustre Colegio de Abogados de [COLEGIO] y con Despacho Profesional en [LOCALIDAD], calle [CALLE], ante el Tribunal comparezco y, como mejor proceda en Derecho, DIGO:

Que por medio del presente escrito y siguiendo instrucciones expresas de mi mandante formulo, DEMANDA DE JUICIO VERBAL SOBRE RECLAMACIÓN DE CANTIDAD, por un total de [IMPORTE] EUROS ( €) frente a la HERENCIA YACENTE DE D. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], calle

Todo ello en base a los siguientes,

HECHOS

PRIMERO D. [NOMBRE Y APELLIDOS], falleció el día [DÍA] de [MES] de [AÑO]

Se acompaña como documento número 1, el certificado de defunción de D. [NOMBRE Y APELLIDOS]

SEGUNDO Que mi mandante procedió a abonar los gastos de sepelio y enterramiento del finado.

Se adjunta como documento número 2, la factura acreditativa de los gastos y como documento número 3, justificante de la trasferencia de abono de los memos.

TERCERO Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

FUNDAMENTOS DE DERECHO

Jurisdicción y competencia

Es competente la jurisdicción civil, conforme a lo dispuesto en los artículos 9 y 21.1 de la Ley Orgánica del Poder Judicial, en relación con lo dispuesto en el art. 85.1º LOPJ.

Corresponde a los Tribunales de Instancia de esta ciudad en base al artículo 50.1 de la Ley de Enjuiciamiento Civil, por ser el del único domicilio conocido de la demandada.

Capacidad

Las partes poseen capacidad para interponer la presente demanda, según lo establecido en los artículos 6 y siguientes de la LEC.

[ELEGIR UNA OPCIÓN: Representación y postulación / Opción 1ª: Cuantía superior a 2.000 € / Opción 2ª: Cuantía inferior a 2.000 €]

Legitimación activa y pasiva

Corresponde legitimación activa a mi mandante por ser a quien se le adeuda la cantidad reclamada y la pasiva a la masa que conforma la Herencia Yacente, titular de los derechos y obligaciones del causante.

Procedimiento y cuantía

A tenor del artículo 250.2º de la LEC, al no exceder el valor de la reclamación de 15.000 euros, el procedimiento correspondiente es el del juicio declarativo verbal.

Cuantía del procedimiento

Atendiendo al artículo 251.1º de la LEC, se fija la cuantía del presente procedimiento en [IMPORTE] EUROS ( €).

Cumplimiento de los requisitos de procedibilidad

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

Fondo

Intereses

Respecto a los intereses, se devengaran los legales, desde la interposición de la presente demanda judicial, atendiendo a lo dispuesto en los artículos 1100, 1101 y 1108 del Código Civil.

Costas

Deberán ser impuestas a la parte cuyas pretensiones resulten totalmente desestimadas de acuerdo con lo dispuesto en el artículo 394.1 de la LEC.

En su virtud,

SOLICITO AL TRIBUNAL: Que teniendo por presentado la presente demanda junto con los documentos que la acompañan y sus copias, los admita y tenga por interpuesta DEMANDA DE JUICIO VERBAL de reclamación de cantidad y seguido el juicio por sus trámites legales, dicte en su día sentencia estimatoria de la demanda condenando a la demandada a abonar la suma total de [IMPORTE] EUROS ( €), todo ello con condena al abono de los intereses legales y costas.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

OTROSÍ PRIMERO DIGO: Que habiéndose aportado el poder general para pleitos, que se precisa para otros usos, intereso su devolución, previa unión a los autos de copia testimoniada.

OTROSÍ SEGUNDO DIGO: Interesa a esta parte, para asegurar la efectividad de la tutela judicial que pudiera otorgarse en la sentencia estimatoria que pudiera recaer en el referido procedimiento, la adopción de medidas cautelares que después se dirán, basadas en los siguientes,

HECHOS

PRIMERO: Se solicita la adopción de la medida cautelar consistente en el embargo preventivo de los saldos de las cuentas corrientes conocidas del causante, con el fin de poder asegurar el cumplimiento de una posible futura sentencia estimatoria de las pretensiones de esta parte.

FUNDAMENTOS DE DERECHO

Jurisdicción

Es competente la jurisdicción civil, conforme a lo dispuesto en los artículos 9 y 21.1 de la Ley Orgánica del Poder Judicial.

Competencia territorial

En aplicación del artículo 50.1 de la LEC y del artículo 723.1 del mismo cuerpo legal, es competente para conocer este asunto el Tribunal de Instancia al que me dirijo.

Capacidad

Las partes poseen capacidad para interponer la presente demanda, según lo establecido en los artículos 6 y siguientes de la LEC.

Representación y postulación

La representación de la actora y la postulación a la presente demanda es la procedente conforme lo establecido en los artículos 23 y siguientes de la LEC.

Legitimación

Corresponde legitimación activa a mi mandante por ser a quien se le adeuda la cantidad reclamada y la pasiva a la masa que conforma la Herencia Yacente, titular de los derechos y obligaciones del causante.

Procedimiento

El previsto en el artículo 730 de la LEC.

Fondo

CARACTERÍSTICAS DE LAS MEDIDAS CAUTELARES:

I.- Para que proceda la adopción de una determinada medida cautelar son varias las características que debe reunir, características que aparecen reguladas en el artículo 726 LEC, y que se concretan en:

1ªSer exclusivamente conducente a hacer posible la efectividad de la tutela judicial que pudiere otorgarse en una eventual sentencia estimatoria, de modo que no pueda verse impedida o dificultada por situaciones producidas durante la pendencia del proceso correspondiente.

2ªNo ser susceptible de sustitución por otra medida igualmente eficaz, a los efectos del apartado precedente, pero menos gravosa o perjudicial para el demandado.

II."PERICULUM IN MORA"O PELIGRO POR LA MORA PROCESAL: La concurrencia de este requisito viene exigida por el artículo 728.1 LEC, precepto que establece que:

"Sólo podrán acordarse medidas cautelares si quien las solicita justifica, que, en el caso de que se trate, podrían producirse durante la pendencia del proceso, de no adoptarse las medidas solicitadas, situaciones que impidieren o dificultaren la efectividad de la tutela que pudiere otorgarse en una eventual sentencia estimatoria".

Pues bien, el tenor literal de este precepto permite sostener una interpretación amplia del periculum in mora, y ello porque, a diferencia de la anterior Ley de Enjuiciamiento Civil, la actual redacción no previene una forma o modo concreto de acreditar la concurrencia del peligro, sino que exige tan sólo que el solicitante "justifique" la situación que amenaza la efectividad de la sentencia.

III."FUMUS BONI IURIS"O APARICENCIA DE BUEN DERECHO: El artículo 728.2 LEC establece que:

"El solicitante de medidas cautelares también habrá de presentar los datos, argumentos y justificaciones documentales que conduzcan a fundar, por parte del tribunal, sin prejuzgar el fondo del asunto, un juicio provisional e indiciario favorable al fundamento de su pretensión. En defecto de justificación documental, el solicitante podrá ofrecerla por otros medios".

IV. MEDIDA CAUTELAR INAUDITA PARTE: La audiencia previa al demandado es un presupuesto general que admite excepciones cuando se acreditan razones de urgencia. Así lo dispone el artículo 733.2 LEC:

"...cuando el solicitante así lo pida y acredite que concurren razones de urgencia o que la audiencia previa puede comprometer el buen fin de la medida cautelar, el tribunal podrá acordarla sin más trámites mediante auto, en el plazo de cinco días, razonando por separado sobre la concurrencia de los requisitos de la medida cautelar y las razones que han aconsejado acordarla sin oír al demandado".

La grave situación de [CAUSA], hace que esta parte considere que concurre una situación de urgencia justificada suficiente para legitimar la adopción de la medida cautelar inaudita parte.

La adopción de esta medida no causaría una situación de indefensión a la demandada, puesto que los artículos 739 y ss. LEC le brindan los medios de oposición necesarios para que se alce la medida cautelar adoptada en el supuesto de que la oposición fuera estimada.

[ELEGIR UNA OPCIÓN: Caución / Opción 728.3 de la LEC / Opción 737 de la LEC]

Costas

Se deberán imponer a la contraparte atendiendo al artículo 736.1 de la LEC en relación con el 394 del mismo cuerpo legal.

Por todo ello,

SOLICITO AL TRIBUNAL: Se sirva tener por presentado este escrito junto con los documentos y copias que se acompañan, por interpuesta SOLICITUD DE MEDIDAS CAUTELARES frente a y, en su virtud, al amparo de lo dispuesto en el artículo 733 LEC, acuerde, sin dar audiencia a la mercantil demandada o, subsidiariamente, previa celebración de los trámites legalmente oportunos, sin constitución previa de caución alguna o, de 100 €, o en su caso, previa la caución que el Tribunal estime suficiente, la adopción de la medida cautelar consistente en el embargo preventivo de las cuentas corrientes señaladas de la demandada hasta cubrir la cuantía de [IMPORTE] EUROS ( €).

En fecha y lugar "ut supra"

Fdo.:

Abogada

Fdo.:

Procuradora

========================================================================
