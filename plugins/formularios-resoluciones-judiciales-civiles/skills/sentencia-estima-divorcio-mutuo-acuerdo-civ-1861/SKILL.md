---
name: sentencia-estima-divorcio-mutuo-acuerdo-civ-1861
description: "Sentencia que estima el divorcio de mutuo acuerdo. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Sentencia que estima el divorcio de mutuo acuerdo

> Formulario **CIV-1861** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

Sentencia que declara disuelto por divorcio el matrimonio en un procedimiento de mutuo acuerdo o a petición de uno de los cónyuges con el consentimiento del otro (art. 777 LEC), sin hijos menores ni hijos con discapacidad con medidas de apoyo, y aprueba el convenio regulador.

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Sentencia que estima el divorcio de mutuo acuerdo» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Sentencia que estima el divorcio de mutuo acuerdo” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:sentencia-estima-divorcio-mutuo-acuerdo-civ-1861`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] AÑO (3 veces)
- [ ] DÍA (3 veces)
- [ ] MES (3 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL CÓNYUGE (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL SOLICITANTE (2 veces)
- [ ] FECHA
- [ ] FIRMA
- [ ] HECHOS ALEGADOS

## Normas que cita el formulario

- art. 86 CC
- art. 777 LEC
- art. 81.1.º CC
- art. 90 CC
- art. 777.4 LEC

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

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

SENTENCIA

ANTECEDENTES DE HECHO

PRIMERO.– Por el/la Procurador/a Sr./Sra. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], obrando en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS DEL SOLICITANTE], mediante escrito con fecha [FECHA], que por turno de reparto correspondió a este Tribunal, formuló solicitud de divorcio respecto del matrimonio contraído por dicho/a representado/a con D./Dña. [NOMBRE Y APELLIDOS DEL CÓNYUGE], alegando los hechos en que basa su solicitud: [HECHOS ALEGADOS]; invocó el art. 86 CC y terminó suplicando se dictara sentencia estimatoria en la que se decretase la disolución por divorcio del matrimonio, adjuntando convenio regulador.

SEGUNDO.– Por auto de fecha [DÍA] de [MES] de [AÑO] se admitió a trámite la demanda, acordándose la ratificación por separado de los cónyuges, que fue verificada, y no habiendo en el matrimonio hijos menores ni hijos con discapacidad con medidas de apoyo, y estimándose suficiente la documentación aportada e innecesaria la práctica de ninguna otra prueba, quedaron los autos pendientes de dictar sentencia por diligencia de ordenación de [DÍA] de [MES] de [AÑO].

TERCERO.– En la tramitación del presente juicio, seguida conforme al art. 777 LEC, se han observado todas las prescripciones formales de la Ley.

FUNDAMENTOS DE DERECHO

PRIMERO.– No existiendo causas materiales para la extinción del matrimonio por divorcio, al margen de la libre voluntad de los cónyuges, según la remisión del art. 86 CC al régimen del art. 81.1.º CC, en afirmación de la libertad como valor superior de nuestro ordenamiento jurídico, que se proyecta no solo al derecho subjetivo constitucionalizado en el art. 32 CE a contraer matrimonio, sino también al derecho legalizado a no continuar casado, siendo esta última la opción de los solicitantes en este procedimiento, procede acceder al divorcio solicitado, no existiendo otro interés protegible en la Ley que pueda enervarlo.

SEGUNDO.– En punto a las medidas definitivas acerca de la situación derivada de la disolución vincular, que se corresponden con un estado de cosas disímil del de la separación precedente, debe homologarse el nuevo convenio regulador propuesto y ratificado por las partes, toda vez que recoge los extremos a que debe extender su contenido conforme a la Ley, y no se observa que pueda ocasionar grave perjuicio a ninguno de los cónyuges, ni son menester garantías adicionales a las que lleva consignadas, en armonía con el art. 90 CC y el art. 777.4 LEC.

Vistos los preceptos y jurisprudencia citados y demás de general y pertinente aplicación, ejerciendo la potestad jurisdiccional que emana de la soberanía popular,

FALLO

Estimando la solicitud formulada por el/la Procurador/a de los Tribunales [NOMBRE Y APELLIDOS DEL PROCURADOR/A], en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS DEL SOLICITANTE], con el consentimiento de D./Dña. [NOMBRE Y APELLIDOS DEL CÓNYUGE], declaro disuelto por divorcio el matrimonio de dichos cónyuges, y apruebo como medidas definitivas las consignadas en el convenio regulador propuesto.

Firme que sea esta sentencia, líbrese oficio al Encargado del Registro Civil de [LOCALIDAD], al que se acompañará testimonio de ella, a fin de que proceda a anotar su parte dispositiva en la correspondiente inscripción de matrimonio.

Poniendo en las actuaciones certificación, inclúyase la presente en el Libro de Sentencias.

Contra esta sentencia no cabe interponer recurso alguno.

Así, por esta mi sentencia, definitivamente juzgando, lo pronuncio, mando y firmo.

Firma del Juez/a: [FIRMA]
