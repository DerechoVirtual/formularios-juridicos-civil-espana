---
name: escrito-oposicion-demandado-demanda-desahucio-falta-civ-0540
description: "Escrito de oposición del demandado a la demanda de desahucio por falta de pago. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito de oposición del demandado a la demanda de desahucio por falta de pago

> Formulario **CIV-0540** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito de oposición del demandado a la demanda de desahucio por falta de pago» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito de oposición del demandado a la demanda de desahucio por falta de pago” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:escrito-oposicion-demandado-demanda-desahucio-falta-civ-0540`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (6 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] Nº DE DOCUMENTO (4 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] EXPONER EL MOTIVO
- [ ] FECHA
- [ ] LOCALIDAD
- [ ] MES
- [ ] MESES ADEUDADOS
- [ ] Nº
- [ ] SEDE

## Normas que cita el formulario

- art. 438.5 LEC
- art. 22.4 LEC

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

- Junto a «…r falta de pago núm. [Nº] A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

Juicio verbal de desahucio por falta de pago núm. [Nº]

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

Don [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en nombre y representación de Don [NOMBRE Y APELLIDOS] con domicilio en [LOCALIDAD], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], ante el Tribunal comparezco y DIGO:

Que habiendo sido requerido mi representado en fecha [FECHA] como parte demandada en el juicio de desahucio número [NÚMERO] arriba expresado, para que en el plazo de diez días desaloje el inmueble, pague o pretenda lo procedente sobre la enervación, por medio del presente escrito, y al amparo de lo prevenido en el artículo 438.5 de la LEC, paso a OPONERME a la demanda de desahucio alegando sucintamente los siguientes MOTIVOS:

PRIMERO.- [EXPONER EL MOTIVO]
SEGUNDO.- Nos oponemos a la demanda por cuanto que el demandante no está legitimado activamente, puesto que ni fue parte en el contrato de arrendamiento, careciendo de la condición de propietario o poseedor de la finca.

En efecto, el contrato se concertó con D. [NOMBRE Y APELLIDOS], como titular del inmueble, a quien se ha venido abonando la renta desde el inicio de la relación arrendaticia, desconociéndose en qué concepto actúa la sociedad [DENOMINACIÓN SOCIAL], ahora demandante, no justificando su condición de propietaria ni tampoco el título en virtud del cual ostenta la posesión de la finca arrendada, por lo que nos oponemos a la demanda interpuesta por dicha representación.

TERCERO.- El demandante ejercita la acción de desahucio reclamando el lanzamiento y el pago de la cantidad de [IMPORTE] euros que se corresponderían a la diferencias de renta abonadas por mi representado en los meses de [MESES ADEUDADOS], pretendiendo que la renta mensual arrendaticia era de [IMPORTE] euros.

Al respecto debemos oponernos rotundamente al importe de [IMPORTE] euros de renta fijado unilateralmente por el arrendador, en base a un supuesto incremento de la renta por gastos de comunidad, siendo que mi mandante ha venido abonando desde el inicio de la relación arrendaticia la cantidad de [IMPORTE] euros mensuales, tal como se acredita con los documentos [Nº DE DOCUMENTO], siendo modificada la cuantía de la renta por el arrendador inopinadamente, de forma unilateral y sin notificarlo a mi representado.

Por este motivo, nos oponemos a la acción de desahucio en base a que la cantidad reclamada por el demandante no se adeuda, por cuanto que si bien el desahucio no es el cauce adecuado para la determinación de la renta derivada del contrato, el éxito de la acción ejercitada en el mismo depende del impago, siendo que en este caso aportamos un principio de prueba creíble y fundado, consistente en los recibos de renta desde el inicio del arrendamiento hasta el mes de [MES], en orden que la renta satisfecha hasta entonces es distinta a la que se refiere la demanda rectora del juicio de desahucio.

Por tanto, nos oponemos a la demanda interpuesta de contrario, tal como se expondrá de forma extensa en el acto de la vista.

CUARTO.- El demandante ejercita la acción de desahucio reclamando el lanzamiento por no haberse abonado la cantidad de [IMPORTE] euros correspondiente a la renta arrendaticia del periodo comprendido entre los meses de

Al respecto debemos oponernos a la demanda alegando el puntual pago de la renta arrendaticia, por cuanto que mi representado ha venido abonando la renta, sin oposición alguna por el arrendador, mediante ingresos en metálico en la cuenta corriente número [NÚMERO], titularidad del arrendador, según se acredita con los recibos de renta que se acompañan como documentos [Nº DE DOCUMENTO] y que se incluyen el periodo reclamado.

En la demanda se alega un presunto deber de mi representado de abonar la renta en la cuenta de la sociedad [DENOMINACIÓN SOCIAL], titularidad del arrendador, pero lo cierto es que dicha pretensión es contraria a lo pactado por las partes en el contrato de arrendamiento y a los propios actos del demandante.

Por tanto, nos oponemos a la demanda interpuesta de contrario por pago de la renta.

QUINTO.- Nos oponemos a la demanda formulada por cuanto que, pese a lo indicado en la misma, en que se expresa que no es posible enervar la acción de desahucio, lo cierto es que se dan las circunstancias y condiciones para la enervación de la acción, según dispone el artículo 22.4 de la LEC.

El demandante pretende en su demanda que no puede darse la enervación con fundamento en el párrafo segundo del artículo 22.4 al haber requerido de pago a mi mandante con treinta días de antelación a la presentación de la demanda. Sin embargo, en ningún momento mi representado ha recibido dicho requerimiento que en todo caso habría de realizarse de forma fehaciente según el tenor del citado precepto, no cumpliéndose en este caso los requisitos del artículo 22.4 de la LEC, al haberse formulado el requerimiento mediante un burofax que no consta recibido, y en este sentido invocamos la interpretación que realizan la SAP Guipúzcoa (Sección 3ª) 13 abril 2005 y la SAP Murcia (Sección 4ª) 3 enero 2013.

Además, y tal como es de ver en el requerimiento que acompaña el demandante como documento [Nº DE DOCUMENTO], en el mismo sólo se indica que debe abonar la cantidad de [IMPORTE] euros en concepto de rentas, sin mayor precisión, por lo que no se dan los requisitos exigidos para exceptuar la facultad de enervación; en este sentido, como indica la SAP de Barcelona, Sección 13, de 21 de mayo de 2004, y en el mismo sentido las SSAP Palencia 15 septiembre 2006 y Segovia 24 septiembre 2009, la excepción a la facultad de enervación legalmente impuesta supone una limitación de derechos del arrendatario, debe ser interpretada restrictivamente, siendo necesario que se advierta al arrendatario de una manera clara y terminante de todas las consecuencias jurídicas inherentes a su impago, de tal modo que el inquilino comprenda el alcance y fines de la intimación, lo cual en modo alguno se ha realizado en este caso.

Por todo ello,

SUPLICO AL TRIBUNAL: Que tenga por presentado este escrito, con su copia y documentos que lo acompañan, que lo admita acordando su unión a los autos de su razón, y que me tenga por personado y parte en la representación que ostento de Don [NOMBRE Y APELLIDOS] en virtud de la copia electrónica del poder notarial de representación informática (o digitalizada) general para pleitos cuya devolución intereso, quedando en los autos copia testimoniada (o en virtud de apoderamiento apud acta) y me tenga por OPUESTO en tiempo y forma a la demanda de desahucio deducida de contrario, procediéndose a la celebración de la vista señalada (en su caso teniendo por acompañado el resguardo de consignación de las rentas adeudadas a efectos de enervación de la acción de desahucio.)

En

========================================================================
