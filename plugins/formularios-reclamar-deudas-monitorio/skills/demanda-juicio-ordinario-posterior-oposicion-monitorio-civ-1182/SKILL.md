---
name: demanda-juicio-ordinario-posterior-oposicion-monitorio-civ-1182
description: "Demanda de juicio ordinario posterior a la oposición en monitorio por precio de suministro. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio ordinario posterior a la oposición en monitorio por precio de suministro

> Formulario **CIV-1182** del plugin **Cobrar deudas: monitorio y cambiario** (`formularios-reclamar-deudas-monitorio`) · Civil › Monitorio y cambiario · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio ordinario posterior a la oposición en monitorio por precio de suministro» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio ordinario posterior a la oposición en monitorio por precio de suministro” para mi caso». También puedes invocarla directamente con `/formularios-reclamar-deudas-monitorio:demanda-juicio-ordinario-posterior-oposicion-monitorio-civ-1182`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-reclamar-deudas-monitorio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Cobrar deudas: monitorio y cambiario) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] FECHA (5 veces)
- [ ] Nº DE DOCUMENTO (4 veces)
- [ ] Nº DE PROCEDIMIENTO (3 veces)
- [ ] Nº (2 veces)
- [ ] AÑO
- [ ] DOMICILIO
- [ ] DÍA
- [ ] IMPORTE
- [ ] LUGAR
- [ ] MES
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] SEDE
- [ ] ÓRGANO

## Normas que cita el formulario

- art. 813 LEC
- art. 818.2 LEC
- art. 399 LEC
- art. 1500 CC
- art. 1.100 CC
- art. 394 LEC

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

D. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, actuando en representación de la mercantil [NOMBRE DEL REPRESENTADO/A], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], por medio de la presente formulo demanda de juicio ordinario derivada de la existencia de oposición en el procedimiento monitorio núm. [Nº DE PROCEDIMIENTO] seguido ante ese mismo Tribunal habiéndose dado a esta parte traslado de la oposición el [FECHA]. Tal demanda se interpone frente a D./Dª [NOMBRE Y APELLIDOS], domiciliados en [DOMICILIO] y en reclamación de 20.000 Euros.

HECHOS

PRIMERO.- La petición inicial origen del proceso monitorio núm. [Nº DE PROCEDIMIENTO] seguido ante ese mismo Tribunal deriva del impago de los suministros que por parte de la mercantil demandante [ÓRGANO] se hicieron a D./Dª [NOMBRE Y APELLIDOS] en el período comprendido entre el [FECHA] y el [FECHA] ascendiendo su importe a 20.000 Euros que es la cantidad que fue objeto del proceso monitorio antecedente de la presente ejecución. Tal cantidad se indicó en su oposición que fue abonada por medio de la transferencia bancaria que indicaba adjuntando una certificación de la misma.

No obstante lo anterior, por medio de tal certificación se hizo frente al pago de otras deudas que D./Dª [NOMBRE Y APELLIDOS] tenía con mi mandante según deriva del extracto de la cuenta abierta en los registros de mi representada que se acompaña como documento núm. [Nº], motivo por el que no cabe entender abonada la cantidad que fue objeto del proceso monitorio antecedente del presente y que se reclama por medio de esta demanda.

Para justificar el importe de la deuda se acompañaron a la petición inicial los albaranes de entrega firmados por la empresa deudora y las facturas correspondientes a los suministros impagados, como documentos número 1 a [Nº DE DOCUMENTO] de nuestro escrito de petición inicial, los cuales justifican la existencia e importe de la deuda, interesando desde este momento que se incorporen al presente proceso.

SEGUNDO.- Requerido de pago el deudor, presentó escrito oponiéndose al requerimiento alegando que la cantidad reclamada había sido abonada por medio de la transferencia bancaria que indicaba, adjuntando una certificación de la misma.

No obstante lo anterior, por medio de tal transferencia se hizo frente al pago de otras deudas que D/Dª [NOMBRE Y APELLIDOS]. tenía con mi mandante según deriva del extracto de la cuenta abierta en los registros de mi representada que se acompaña a este escrito de demanda como documento nº [Nº DE DOCUMENTO], motivo por el que no cabe entender abonada la cantidad que fue objeto del proceso monitorio antecedente del presente y que se reclama por medio de esta demanda.

Concretamente, el pago abonado por el deudor responde a los suministros de un periodo anterior, desde el [FECHA] al [FECHA], tal como se acredita mediante certificación de los asientos contables de mi representada y con las facturas que acompañamos como documentos [Nº DE DOCUMENTO], las cuales corresponden al pago alegado por el deudor.

TERCERO.- Por tanto, adeudando el demandado la cantidad reclamada, y ante su oposición al requerimiento de pago, nos vemos en la obligación de interponer la presente demanda de juicio ordinario, en reclamación de [IMPORTE] euros con más los intereses correspondientes.

FUNDAMENTOS DE DERECHO

PRIMERO.- Jurisdicción y competencia. Se acepta la del Tribunal al que me dirijo con fundamento en el art. 813 LEC.

SEGUNDO.- Demanda y procedimiento. Se interpone ante ese Tribunal y dentro del plazo de un mes desde el traslado del escrito de oposición que fija el art 818.2 LEC tramitándose por las normas que para el juicio ordinario se establecen en los arts 399 ss LEC, debiendo dictarse decreto poniendo fin al proceso monitorio, admitiendo la demanda y dando traslado de ella al demandado conforme a lo previsto en los artículos 404 y ss. de la LEC.

TERCERO.- Cumplimiento de los requisitos de procedibilidad. La presente demanda no está sujeta al intento previo de MASC como requisito de procedibilidad, en cuanto que, acreditado al presentar la petición inicial del monitorio, no es necesario volver a realizarlo para el juicio ordinario o verbal que derive de la oposición, ya que el requisito ya se entiende satisfecho para ese objeto de litigio.

CUARTO.- Fondo de la reclamación. Se trata de reclamar el precio de un suministro, lo que es exigible con fundamento en el art. 1500 y concordantes del CC al ser aplicables análogamente a los contratos de suministro las previsiones establecidas para la compraventa.

En cuanto a los intereses se solicitan los de demora desde la interpelación judicial en el procedimiento monitorio antecedente del presente con fundamento en el art. 1.100 CC.

QUINTO.- Costas. Se solicita su condena al demandado con fundamento en el art. 394 LEC.

En base a lo anterior,

SUPLICO AL TRIBUNAL: Se tenga por presentada esta demanda con sus documentos, se sirva admitirla y tener por formulada demanda de juicio ordinario derivada de la oposición al proceso monitorio [Nº DE PROCEDIMIENTO] seguido ante ese mismo Tribunal frente a D./Dª [NOMBRE Y APELLIDOS] en reclamación de 20.000 Euros y tras la adecuada tramitación se dicte sentencia por la que se condene al demandado al pago a mi principal de la cantidad de 20.000 Euros más intereses desde la interpelación del proceso monitorio antecedente del presente y costas del procedimiento.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

El Letrado	El Procurador

========================================================================
