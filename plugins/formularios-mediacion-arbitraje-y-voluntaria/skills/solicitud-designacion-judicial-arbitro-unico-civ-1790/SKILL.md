---
name: solicitud-designacion-judicial-arbitro-unico-civ-1790
description: "Solicitud de designación judicial de árbitro único. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de designación judicial de árbitro único

> Formulario **CIV-1790** del plugin **Mediación, MASC, arbitraje y jurisdicción voluntaria** (`formularios-mediacion-arbitraje-y-voluntaria`) · Civil › Jurisdicción voluntaria, MASC, mediación y arbitraje · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de designación judicial de árbitro único» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de designación judicial de árbitro único” para mi caso». También puedes invocarla directamente con `/formularios-mediacion-arbitraje-y-voluntaria:solicitud-designacion-judicial-arbitro-unico-civ-1790`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-mediacion-arbitraje-y-voluntaria:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Mediación, MASC, arbitraje y jurisdicción voluntaria) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NÚMERO (6 veces)
- [ ] FECHA (4 veces)
- [ ] DENOMINACIÓN SOCIAL (3 veces)
- [ ] IMPORTE (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] ACTO O RESOLUCIÓN
- [ ] CALLE
- [ ] DOMICILIO
- [ ] LUGAR
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº

## Normas que cita el formulario

- art. 15 Ley 60/2003

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

Escrito solicitando la designación judicial de árbitro.

A LA SALA DE LO CIVIL DEL TRIBUNAL SUPERIOR DE JUSTICIA DE LA COMUNIDAD AUTÓNOMA DE [LOCALIDAD]

D./DÑA. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales y de [NOMBRE DEL REPRESENTADO/A], como acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], y con la dirección del Letrado D./DÑA. [NOMBRE Y APELLIDOS], colegiado n.º [NÚMERO] del Itre. Colegio de Abogado/as de [LOCALIDAD], ante la Sala comparezco, y como mejor en Derecho proceda, DIGO:

Que al amparo del art. 15 de la Ley 60/2003 de 23 de diciembre, de Arbitraje (LA), vengo a solicitar en la representación que ostento la designación judicial de árbitro frente a la entidad [DENOMINACIÓN SOCIAL], domiciliada en [DOMICILIO], calle [CALLE], n.º [NÚMERO], con C.I.F. n.º [NÚMERO], con base en los siguientes:

HECHOS

PRIMERO.- Con fecha [FECHA], mi representada suscribió un contrato de ejecución de obra con [DENOMINACIÓN SOCIAL] y en la cláusula tercera de dicho contrato se acordó que el pago se efectuaría por unidad de obra o medida, y ello conforme a los criterios establecidos en el anexo n.º [Nº]

En la cláusula decimoctava del contrato las partes acordaron textualmente lo siguiente:

‘Para la solución de cualquier cuestión controvertida que pueda surgir de la interpretación o aplicación del presente contrato, las partes se someten a arbitraje de equidad según lo establecido en la Ley de Arbitraje. En caso de conflicto, las partes designarán de común acuerdo a un Arquitecto Técnico del Colegio de Arquitectos Técnicos y Aparejadores de ‘.

En prueba de las anteriores afirmaciones se acompaña, como documento n.º [NÚMERO], copia del contrato de ejecución de obra suscrito entre las partes.

SEGUNDO.-Con fecha [FECHA], nuestra representada comunicó a [DENOMINACIÓN SOCIAL]., la terminación de las obras contratadas, remitiendo también la última certificación, con el visto bueno de la dirección facultativa de la obra. Dichas certificaciones ascienden a la cantidad de [IMPORTE] euros ( €). Asimismo fue citada dicha entidad para levantar la correspondiente acta de recepción provisional de obra, denegando aquélla la recepción, puesto que discrepa de las mediciones totales de obra ejecutada, sosteniendo que el precio de la obra ejecutada ya ha sido pagado, y una serie de deficiencias indefinidas.

Se acompañan, como docs. n.º [NÚMERO] y [Nº DE DOCUMENTO], la última certificación de obra remitida a .., y copia de ‘burofax’ de fecha [FECHA], por el que se citaba en la obra, junto con la dirección facultativa, al objeto de levantar la correspondiente acta de recepción provisional.

TERCERO.- Al no verse ninguna voluntad de acuerdo por la contraparte respecto a pago del precio que resta, por esta parte se dirigió a .. mediante burofax una carta en que se le urgía a prestar su conformidad a la designación de Arquitecto Técnico de entre un número de doce del listado del Colegio de Arquitectos Técnicos y Aparejadores de [LOCALIDAD], o proponer otra fórmula de llegar a un acuerdo para nombrar otro, sin que hasta el momento se haya recibido ninguna respuesta.

Se aporta como doc. n.º [NÚMERO] copia de la carta y acuse de recibo.

Por consiguiente, no queda más remedio que recurrir a lo tribunales a fin de que se designe el árbitro que dirima en equidad el conflicto surgido.

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA.

Es competente el Tribunal a que me dirijo, como Sala de lo Civil, puesto que es el Tribunal Superior de Justicia de la Comunidad Autónoma del lugar del arbitraje, por hallarse situada la obra ejecutada y ser el Colegio profesional del árbitro designado en el convenio arbitral de esta Comunidad Autónoma, con arreglo al art. 8.1 LA.

II.- PARTES.

Ostentan legitimación las partes que suscribieron el contrato, pasivamente la promotora/propietaria/vendedora, reclamada, y activamente, la constructora, que represento, y postula con representación de Procurador y asistencia letrada.

III.- PROCEDIMIENTO.

Con arreglo al art. 15.4 LA, las pretensiones que se ejerciten en relación con lo previsto para la designación judicial de árbitros se sustanciarán por los cauces del juicio verbal.

La cuantía de la demanda se fija en [IMPORTE] euros ( €).

IV.- ACCIÓN.

La solicitud se funda en el convenio arbitral, que resulta presupuesto del procedimiento y única razón su falta de documentación para rechazarla (art. 15.5 LA), y procede de que no habiendo en aquél un método específico de designación del árbitro único previsto, ni habiéndose podido alcanzar el acuerdo ‘ad hoc’, ese tribunal competente debe designarlo a solicitud de cualquiera de las partes [art. 15.2.a) LA].

La negativa al pago de [IMPORTE], hace que la correlativa denegación de la designación de Arquitecto Técnico que arbitre, como es el compromiso contractual, resulte únicamente una maniobra dilatoria, bien para que esta parte inicie acciones judiciales que se enerven con declinatoria por sumisión a arbitraje, o deba tener que recurrir a este trámite.

Por todo lo expuesto,

SUPLICO A LA SALA

que, teniendo por presentado este escrito con los documentos acompañados, y copia de todo ello, admita la designación judicial de árbitro frente a [ACTO O RESOLUCIÓN], y se proceda por el Letrado de la Administración de Justicia a citar al acto de la vista de juicio verbal para que, seguido el legal procedimiento, se dicte Auto que designe Árbitro conforme a la Ley, con lo demás que proceda

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a

========================================================================
