---
name: escrito-oposicion-ejecucion-dineraria-clausulas-civ-1409
description: "Escrito de oposición a la ejecución dineraria por cláusulas abusivas. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito de oposición a la ejecución dineraria por cláusulas abusivas

> Formulario **CIV-1409** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Escrito de oposición a la ejecución dineraria común por existencia de cláusulas abusivas.

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito de oposición a la ejecución dineraria por cláusulas abusivas» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito de oposición a la ejecución dineraria por cláusulas abusivas” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:escrito-oposicion-ejecucion-dineraria-clausulas-civ-1409`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (9 veces)
- [ ] FECHA (3 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] LUGAR
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] NOMBRE DEL SOLICITANTE
- [ ] NOMBRE Y APELLIDOS
- [ ] Nº
- [ ] PORCENTAJE
- [ ] SEDE

## Normas que cita el formulario

- art. 561.2 LEC
- art. 21.1 LOPJ
- art. 61 LEC
- art. 557 LEC
- art. 517 LEC
- art. 538 LEC
- art. 539.1 LEC
- art. 557.2 LEC
- art. 561.3 LEC

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

D./Dña. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en nombre y representación de [NOMBRE DEL REPRESENTADO/A], según acredito con la escritura de poder inscrito en el Registro Electrónico de Apoderamientos Judiciales, a cuya justificación aporto certificación de dicho Registro como documento nº [Nº DE DOCUMENTO], ante el Tribunal comparezco y como mejor proceda en Derecho DIGO:

Que en nombre de mi poderdante me persono en los autos de ejecución seguidos a instancia de [NOMBRE DEL SOLICITANTE] y registrados con el número [NÚMERO], y por medio del presente escrito formulo OPOSICIÓN a la citada ejecución, dentro del plazo concedido al efecto, en virtud de los siguientes:

HECHOS

PRIMERO.- Por auto de fecha [FECHA] se despachó ejecución contra mi cliente en reclamación de la cantidad de [IMPORTE] euros ( [IMPORTE] €) en concepto de principal e intereses devengados hasta la fecha, más otros [IMPORTE] euros ( [IMPORTE] €) presupuestados provisionalmente para hacer frente a los intereses que, en su caso, puedan devengarse durante la ejecución y las costas de ésta, auto que le fue notificado el pasado día [FECHA], por lo que el presente escrito se ha presentado dentro del término de diez días concedido al efecto para formular oposición.

SEGUNDO.- La liquidación del ejecutante incluye la cantidad de [IMPORTE] euros en concepto de intereses moratorios, en aplicación de la cláusula número [NÚMERO] del contrato de préstamo, aportado por la parte ejecutante como documento número [Nº DE DOCUMENTO] de la demanda ejecutiva.

Dicha cláusula es nula de pleno derecho, por ser abusiva, puesto que fija el interés moratorio en el [PORCENTAJE] % anual, lo que supone más de cinco veces el interés legal del dinero.

En este sentido, SAP Tenerife de 26 de abril de 2006, rec. 118/2006; SAP Tarragona de 10 de abril de 2012, rec. 640/2011; o SAP Alicante de 26 de julio de 2012, rec. 345/2011.

TERCERO.- La nulidad de pleno derecho de la cláusula implica que deben excluirse de la deuda reclamada por la parte ejecutante la cantidad de [IMPORTE] euros en concepto de intereses de demora de conformidad a lo dispuesto en el art. 561.2 LEC por inaplicación de la cláusula abusiva.

Por lo tanto, mi representada no adeuda la cantidad que reclama el ejecutante, sino la de [IMPORTE] euros ( €), por principal e intereses remuneratorios, que se reconoce como debida, debiendo excluirse en todo caso los intereses de demora por abusivos.

CUARTO.- Esta parte pone a disposición del Tribunal, para su inmediata entrega al ejecutante, la cantidad de [IMPORTE] euros ( [IMPORTE] €), por reconocerla como debida, a efectos de la suspensión de la ejecución despachada contra mi mandante, acompañando justificante de ingreso en efectivo, realizado en tal concepto en la cuenta de depósitos y consignaciones de ese Tribunal, con identificación del presente procedimiento, el cual se une al presente escrito como documento número

A los anteriores hechos le son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA.

Corresponde a la jurisdicción civil, conforme a lo dispuesto en los arts. 21.1 LOPJ y 5 LEC.

La competencia funcional para conocer de la oposición corresponde al mismo Tribunal que ha despachado la ejecución (art. 61 LEC).

II.- PROCEDIMIENTO.

Dispone el art. 557 LEC que cuando se despache ejecución por los títulos previstos en los números 4.º, 5.º, 6.º y 7.º, así como por otros documentos con fuerza ejecutiva a que se refiere el n.º 9.º del apartado 2 del art. 517 LEC, el ejecutado sólo podrá oponerse a ella, en el tiempo y en la forma prevista en el artículo anterior (dentro de los diez días siguientes a la notificación del auto en que se despache ejecución y por escrito), si se funda en alguna de las causas que allí se establecen, constando como causa 7.ª, "Que el título contenga cláusulas abusivas".

Respecto de la sustanciación y resolución de la oposición, arts. 559 y ss. LEC.

III.- LEGITIMACIÓN.

Son parte en el proceso de ejecución la persona que pide y obtiene el despacho de la ejecución y la persona frente a las que ésta se despacha (art. 538 LEC).

IV.- REPRESENTACIÓN Y DEFENSA.

El ejecutado deberá estar dirigido por Letrado y representado por Procurador, salvo que se trate de la ejecución de resoluciones dictadas en procesos en que no sea preceptiva la intervención de dichos profesionales (art. 539.1 LEC).

V.- JURÍDICO MATERIALES

1) CAUSA DE LA OPOSICIÓN

Arts. 557.1.7.ª y 558 LEC fundada en la pluspetición. En cuanto a la oposición por abusividad, como indica la STJUE de 14 de marzo de 2013, C-415/2011, el Tribunal deberá determinar si la cláusula de intereses de demora es abusiva contrastando el tipo de interés pactado con el tipo de interés legal y verificando que es adecuado para garantizar la realización de los objetivos que el interés de demora persigue, siendo que en este caso su inclusión en el contrato por la parte ejecutante constituye un patente enriquecimiento injusto y un manifiesto abuso de derecho.

En este sentido, la finalidad del sistema de protección del consumidor contenido en la Directiva 93/13/CEE, como ha señalado la citada sentencia, "se basa en la idea de que el consumidor se halla en situación de inferioridad respecto al profesional, en lo referido tanto a la capacidad de negociación como al nivel de información".

2) SUSPENSIÓN DEL PROCEDIMIENTO EJECUTIVO

De acuerdo con lo establecido en los arts. 557.2 y 558 LEC, formulada la oposición y justificada la puesta a disposición del Tribunal para su inmediata entrega al ejecutante de la cantidad que se considera debida, se solicita la inmediata suspensión del curso de la ejecución dejando sin efecto los embargos y demás medidas de garantía acordadas.

VI.- COSTAS.

En materia de costas procesales, a tenor de lo preceptuado en el art. 561.3 LEC, deberán ser impuestas al ejecutante.

En virtud de todo lo expuesto,

SUPLICO AL TRIBUNAL:

Tenga por presentado este escrito con sus documentos y copias, sirviéndose admitirlos y unirlos a autos, teniendo por formulada, en tiempo y forma OPOSICIÓN A LA EJECUCIÓN instada de contrario y, previa su sustanciación, se proceda a la suspensión inmediata del procedimiento ejecutivo, dejando sin efecto los embargos, y se estime la oposición formulada, inaplicando la cláusula declarada abusiva y reintegrando a mi mandante en la situación anterior al despacho de la ejecución, condenando al ejecutante al pago de las costas procesales causadas.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
