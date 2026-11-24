---
name: escrito-ejecutado-pidiendo-devolucion-sobrante-subasta-civ-1491
description: "Escrito del ejecutado pidiendo la devolución del sobrante de la subasta. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito del ejecutado pidiendo la devolución del sobrante de la subasta

> Formulario **CIV-1491** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Escrito del ejecutado solicitando devolución del sobrante de la subasta, una vez aplicado el remanente del precio del remate a satisfacer a los acreedores con derecho inscrito o anotado con posterioridad al del ejecutante y no estando afecta la finca a otras responsabilidades distintas

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito del ejecutado pidiendo la devolución del sobrante de la subasta» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito del ejecutado pidiendo la devolución del sobrante de la subasta” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:escrito-ejecutado-pidiendo-devolucion-sobrante-subasta-civ-1491`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (4 veces)
- [ ] FECHA (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] Nº (2 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] SEDE (2 veces)
- [ ] AÑO
- [ ] LUGAR

## Normas que cita el formulario

- art. 672.1 LEC
- art. 575 LEC
- art. 1911 CC

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

D./Dña. [NOMBRE Y APELLIDOS], Procurador de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS], cuya representación tengo acreditada en los autos de ejecución hipotecaria registrados con el número [Nº]/[AÑO], siguiendo instrucciones de mi mandante y como mejor proceda en derecho DIGO:

Que con fecha [FECHA] se puso en conocimiento en el procedimiento ejecutivo [Nº DE PROCEDIMIENTO] / [Nº DE PROCEDIMIENTO] seguido ante la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [NÚMERO], con derecho anotado en el Registro de la Propiedad, la existencia de un remanente de [IMPORTE] euros en la presente ejecución hipotecaria, habiéndose remitido ya la cantidad reclamada desde aquel ejecutivo, la de [IMPORTE] euros de principal y [IMPORTE] más en que se presupuestan intereses y costas.

Que según lo dispuesto en el art. 672.1 LEC el remanente del precio obtenido en la subasta de inmuebles, una vez satisfecho el ejecutante, se retendrá para el pago de quienes tengan su derecho inscrito o anotado con posterioridad al del ejecutante; y si satisfechos estos acreedores, aún existiere sobrante, se entregará al ejecutado o al tercer poseedor.

Que cuando la ley habla de pago y satisfacción se está refiriendo al total cumplimiento de la obligación, pero contemplado desde la perspectiva de la garantía que comporta el embargo del inmueble, oportunamente anotado en el Registro de la Propiedad. El art. 575 LEC dice que la ejecución se despachará por la cantidad que se reclame en la demanda ejecutiva en concepto de principal e intereses ordinarios y moratorios vencidos, incrementada en los intereses que se prevean y costas; es decir, se despachará por una cantidad líquida y determinada, aunque un componente de esa cantidad esté sujeto a liquidación. Cuando se embarga preventivamente se hace, precisamente, por esa cantidad líquida, y concretamente en cuanto al derecho del embargante en la ejecución hipotecaria, la garantía viene limitada a la cantidad líquida.

Que sentado que el despacho de ejecución es por cantidad líquida, queda claro que la garantía del inmueble embargado se limita, en cuanto derive de tal embargo, a esa cantidad y no a otra superior, sin perjuicio de la responsabilidad universal del deudor consagrada en el art. 1911 CCiv.

Que puesta de manifiesto en el presente procedimiento la existencia de un remanente en la ejecución, y reclamada desde dicho Tribunal n.º [NÚMERO] la suma de [IMPORTE] euros, una vez aplicado el remanente del juicio hipotecario a la satisfacción de la cantidad por la que se había despachado ejecución en el otro procedimiento, el embargo que garantizaba la deuda del ejecutivo pierde sentido al haber sido realizado ya el pago de la cantidad líquida de cuyo pago respondía el inmueble embargado; y por ello debe considerarse extinguida la garantía que el embargo comportaba -sin perjuicio de su cancelación registral- y, no estando afecta la finca a otras responsabilidades distintas, el remanente de la ejecución hipotecaria debe entregarse al ejecutado.

Por lo expuesto,

SOLICITO AL TRIBUNAL:

Que admita este escrito y acuerde que se haga entrega a la recurrente del remanente existente en la presente ejecución,

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a

========================================================================
