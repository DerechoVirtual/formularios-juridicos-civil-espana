---
name: contestacion-demanda-resolucion-alquiler-vivienda-civ-0597
description: "Contestación a demanda de resolución de alquiler de vivienda por necesidad (contrato previo a 1985). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contestación a demanda de resolución de alquiler de vivienda por necesidad (contrato previo a 1985)

> Formulario **CIV-0597** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Contestación a la demanda por la que se solicita la resolución del contrato de alquiler de la vivienda, por causa de necesidad de la misma, ya que el demandante ha pasado a residir en la de la vivienda arrendada como domicilio habitual. Además, no ha habido rechazo por el arrendatario de indemnización alguna porque no ha habido el ofrecimiento de las indemnizaciones a que se refiere el art. 66 LAU 1964, ni ha transcurrido el plazo de un año desde el requerimiento notarial efectuado.

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contestación a demanda de resolución de alquiler de vivienda por necesidad (contrato previo a 1985)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contestación a demanda de resolución de alquiler de vivienda por necesidad (contrato previo a 1985)” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:contestacion-demanda-resolucion-alquiler-vivienda-civ-0597`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (4 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] FECHA
- [ ] LUGAR
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] OTROS DATOS
- [ ] POSICIÓN SOBRE EL HECHO CUARTO
- [ ] POSICIÓN SOBRE EL HECHO PRIMERO
- [ ] POSICIÓN SOBRE EL HECHO SEGUNDO

## Normas que cita el formulario

- art. 66 LAU
- art. 23 LEC
- art. 31 LEC
- art. 62.1 LAU
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

AL TRIBUNAL

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a. de los Tribunales, en nombre y representación de [NOMBRE DEL REPRESENTADO/A], según acredito mediante copia de la escritura de poder que acompaño para su unión a los autos por testimonio con devolución del original (o, en su caso, según apoderamiento otorgado «apud acta», que acompaño), dirigido por el Letrado abajo firmante D./Dña. [NOMBRE Y APELLIDOS], con despacho profesional en [LOCALIDAD], ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que mediante el presente escrito y dentro del término conferido, paso a contestar la demanda formulada de adverso, oponiéndome a la misma en base a los siguientes:

HECHOS

Esta parte niega los hechos alegados en la demanda, excepto los que expresamente se admitan en el presente escrito.

PRIMERO.- De conformidad con el hecho primero de contrario [POSICIÓN SOBRE EL HECHO PRIMERO]

SEGUNDO.- De conformidad con el hecho segundo de contrario [POSICIÓN SOBRE EL HECHO SEGUNDO]

TERCERO.- Se niega expresamente el correlativo de la demanda, [OTROS DATOS] en el sentido de que, como se acredita con certificación del Registro de la Propiedad (Documento nº [Nº DE DOCUMENTO]), en la localidad de [LOCALIDAD], que se halla a cuatro km, es titular en pleno dominio el demandante de un piso, cuya descripción resulta la siguiente

CUARTO.- Respecto del ordinal cuarto de adverso [POSICIÓN SOBRE EL HECHO CUARTO] debe hacerse constar que, si bien es plenamente cierto (así diligencia del Acta notarial, que aporto como documento nº [Nº DE DOCUMENTO]), que se entendió con mi mandante y éste contestó no aceptando la denegación de prórroga, ni hubo rechazo de indemnización alguna, porque no hubo ofrecimiento de las indemnizaciones a que se refiere el art. 66 LAU 1964, ni ha transcurrido el plazo de un año desde el requerimiento notarial.

QUINTO.- Todos los intentos de mi representado por alcanzar una solución amistosa han sido ineficaces, a cuya demostración se adjuntan las misivas enviadas al demandante por el abogado que suscribe (documentos nos. y [Nº DE DOCUMENTO]).

FUNDAMENTOS DE DERECHO

I, II.-

Conforme esta parte con la competencia y el tipo de procedimiento señalados por el actor en el correlativo de la demanda.

III, IV y V.-

De conformidad con los expuestos de contrario, acerca de la capacidad de las partes y su legitimación, siempre que se entienda la legitimación pasiva ‘ad proccesum’.

VI.- POSTULACIÓN Y DEFENSA

La parte está representada por el Procurador/a. [NOMBRE Y APELLIDOS], legalmente habilitado en el partido, según el art. 23 LEC,y defendida por el Letrado que consta en el encabezamiento (art. 31 LEC).

VII.- FUNDAMENTOS DE FONDO DE LA OPOSICIÓN

La pretensión de la demanda se funda en el art. 62.1 LAU 1964, en cuanto dispone que el inquilino o arrendatario no tendrá derecho a la prórroga legal cuando el arrendador necesite para sí la vivienda.

Pero no se ha cumplido regularmente por la parte contraria el requisito del art. 65 de la misma Ley ya que la denegación de la prórroga forzosa a instancia de mi poderdante, aunque se ha verificado mediante requerimiento fehaciente en el que consta el nombre de la persona que necesita la vivienda, la causa de necesidad y las circunstancias de posposición concurrentes en los demás inquilinos, no se ha practicado con un año de antelación a la demanda, puesto que debe tenerse en cuenta, no la fecha de comparecencia del actor en la notaría, sino la de aceptación y realización del requerimiento, en la medida de que no se trata de una interpelación con base a datos del contrato, ni de interrumpir plazo prescriptivo, sino de poner en conocimiento de esta parte uno hechos, y a favor del arrendatario.

Asimismo se ha in cumplido el requisito del art. 66 LAU 1964, sobre ofrecimiento de indemnización.

Por otra parte, no media justa causa, habida cuenta que el arrendador, muy por el contrario de lo que asevera en su demanda, sí cuenta con una vivienda para su uso, en razón del traslado al que dice haberse visto obligado por su empleo, que si bien no se encuentra exactamente en el centro de esta población (por otro lado, tampoco la que disfruta mi principal), está a escasos cuatro kilómetros, en el barrio de [LOCALIDAD], siendo un puro formalismo que pertenezca al municipio limítrofe de [LOCALIDAD], motivo para considerar abusiva la pretensión de desalojo.

VIII.- COSTAS

Las costas deberán serle impuestas, de conformidad con el artículo 394 LEC, a la parte actora, de ser desestimada su demanda.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito con los documentos y copias que le acompañan, admita uno y otras, y teniendo por contestada en tiempo y forma la demanda, y opuesta esta parte a la misma, previos los trámites que corresponden, se dicte en su día sentencia por la que se desestime íntegramente la demanda presentada, absolviendo libremente de la misma al demandado, con expresa imposición de costas a la parte actora.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a./a

========================================================================
