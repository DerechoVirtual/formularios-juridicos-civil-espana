---
name: escrito-solicitante-laj-requiera-exhibicion-persona-civ-1199
description: "Escrito del solicitante para que el LAJ requiera la exhibición a la persona obligada. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito del solicitante para que el LAJ requiera la exhibición a la persona obligada

> Formulario **CIV-1199** del plugin **Medidas cautelares y diligencias preliminares** (`formularios-medidas-cautelares-civiles`) · Civil › Medidas cautelares y diligencias preliminares · normativa revisada el 24-11-2026.

## Qué es

Escrito del solicitante para que se requiera por el Letrado de la Administración de Justicia a la persona obligada a la exhibición

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito del solicitante para que el LAJ requiera la exhibición a la persona obligada» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito del solicitante para que el LAJ requiera la exhibición a la persona obligada” para mi caso». También puedes invocarla directamente con `/formularios-medidas-cautelares-civiles:escrito-solicitante-laj-requiera-exhibicion-persona-civ-1199`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-medidas-cautelares-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Medidas cautelares y diligencias preliminares) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] AÑO (4 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] FECHA (3 veces)
- [ ] TÍTULO DEL APARTADO (2 veces)
- [ ] DENOMINACIÓN SOCIAL
- [ ] LUGAR
- [ ] OTROS DATOS
- [ ] SEDE

## Normas que cita el formulario

- art. 116 Ley 15/2015
- art. 115.1 LJV
- art. 116 LJV

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

Notas al pie del formulario original:
(1) La exigencia de abogado y procurador para plantear expediente de jurisdicción voluntaria variará, según el art. 3.2 LJV, en función del expediente de que se trate, y la exigencia legal al respecto. En todo caso, aun cuando no sea necesario, las partes que lo deseen podrán actuar asistidas o representadas por Abogado y Procurador, respectivamente. En el supuesto específico del presente escrito el art. 113.2 LJV exige de manera preceptiva la intervención de Abogado y Procurador para la solicitud en análisis.


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

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en nombre y representación de la entidad [DENOMINACIÓN SOCIAL] SL [OTROS DATOS], según acredito mediante copia fehaciente de la escritura de poderes, que acompaño para su unión a los autos por copia testimoniada con devolución de aquélla, como mejor proceda en derecho comparezco y DIGO:

Que por medio del presente escrito, y de conformidad con el art. 116 de la Ley 15/2015, de 2 de julio, de la Jurisdicción Voluntaria (en lo sucesivo, LJV), solicito requerimiento del Letrado de la Administración de Justicia en relación a D./Dña. [NOMBRE Y APELLIDOS]. Todo ello, en base a los siguientes

Hechos y consideraciones jurídicas:

1ª [TÍTULO DEL APARTADO])

Que mi mandante planteó ante el Tribunal al cual tengo el honor de dirigirme expediente de jurisdicción voluntaria, en solicitud de exhibición de libros contables por parte de D./Dña. [NOMBRE Y APELLIDOS]. El expediente tramitado con número terminó con auto dictado el [FECHA] en el cual se le ordenaba la presentación en el Tribunal, en el plazo de diez días, del soporte informático relativo al libro de inventario y cuentas anuales correspondiente a los ejercicios de [AÑO] y [AÑO]. Dicha resolución judicial no fue recurrida, deviniendo, por ello, firme.

2ª [TÍTULO DEL APARTADO])

Que transcurrido el plazo ordenado para ello, donde ha cumplido con la orden dada, y no ha presentado ante el órgano judicial soporte informático alguno, incumpliendo el deber de colaboración exigido en el art. 115.1 LJV.

3º) En consecuencia, y en virtud de lo dispuesto en el art. 116 LJV, solicito que por el Letrado de la Administración de Justicia se proceda a requerir al citado comerciante para que aporte la documentación señalada, absteniéndose de reiterar el quebrantamiento, con apercibimiento de imposición de multa y de incurrir en un delito de desobediencia a la autoridad judicial. Y para el caso, de que persista en tal incumplimiento se impongan multas coercitivas en el importe que se estime conveniente, en atención a las circunstancias del hecho y los graves perjuicios que se puedan ocasionar a mi mandante.

Por todo lo expuesto, al amparo del art. 116 LJV,

SOLICITO AL TRIBUNAL

Que teniendo por presentado este escrito, se proceda por el Letrado de la Administración de Justicia a requerir a D./Dña. [NOMBRE Y APELLIDOS] para que aporte de manera inmediata soporte informático relativo al libro de inventario y cuentas anuales correspondiente a los ejercicios de [AÑO] y [AÑO], ordenado en auto dictado en fecha [FECHA], absteniéndose de reiterar el quebrantamiento, con apercibimiento de imposición de multa y de incurrir en un delito de desobediencia a la autoridad judicial. Y para el caso, de que persista en tal incumplimiento se impongan multas coercitivas en el importe que se estime conveniente, en atención a las circunstancias del hecho y los graves perjuicios que se puedan ocasionar a mi mandante.

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a
