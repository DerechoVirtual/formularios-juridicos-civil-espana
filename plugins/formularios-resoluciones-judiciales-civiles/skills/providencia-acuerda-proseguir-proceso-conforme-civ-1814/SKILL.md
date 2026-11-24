---
name: providencia-acuerda-proseguir-proceso-conforme-civ-1814
description: "Providencia que acuerda proseguir el proceso conforme al artículo 15 del Convenio de La Haya de 1965. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Providencia que acuerda proseguir el proceso conforme al artículo 15 del Convenio de La Haya de 1965

> Formulario **CIV-1814** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Providencia que acuerda proseguir el proceso conforme al artículo 15 del Convenio de La Haya de 1965» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Providencia que acuerda proseguir el proceso conforme al artículo 15 del Convenio de La Haya de 1965” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:providencia-acuerda-proseguir-proceso-conforme-civ-1814`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] ACTO O RESOLUCIÓN (2 veces)
- [ ] FECHA (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] AÑO
- [ ] DOMICILIO
- [ ] DÍA
- [ ] LOCALIDAD
- [ ] MES
- [ ] NOMBRE DE LA PARTE
- [ ] NÚMERO
- [ ] PLAZO

## Normas que cita el formulario

- art. 451 LEC

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

SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA N.º [NÚMERO]

PROVIDENCIA

Magistrado/Juez D. [NOMBRE Y APELLIDOS]

En la ciudad de [LOCALIDAD] a [DÍA] de [MES] de [AÑO]

Dada cuenta del estado de los presentes Autos, este Tribunal acuerda proseguir la tramitación del procedimiento de conformidad con los siguientes

HECHOS

Primero.- Que por la parte actora, D. [NOMBRE Y APELLIDOS], se presentó escrito de demanda de Juicio [Nº DE PROCEDIMIENTO] contra [ACTO O RESOLUCIÓN] domiciliado en [DOMICILIO], que fue admitida a trámite mediante Auto de fecha [FECHA], acordándose emplazar a la parte demandada, por término de [PLAZO].

Segundo.- Que con fecha de [FECHA] consta petición de notificación o traslado al U.S. Department of Justice, Civil Division. Office of International Judicial Assistance (Autoridad Central de Estados Unidos de América), conforme a la fórmula modelo anexa al Convenio de La Haya sobre notificación o traslado al extranjero de documentos judiciales y extrajudiciales en materia civil o comercial de 15 de noviembre de 1965, organismo competente al que se refiere el artículo 3 del citado Convenio.

Tercero.- Este Tribunal no ha recibido comunicación o certificación acreditativa de la notificación o traslado y habiéndose interesado información de la Autoridad Central de Estados Unidos de América, ésta no ha podido obtener certificación de la realización de la notificación o traslado. La razón por la que la notificación no ha sido efectiva es que el sujeto a notificar ha rechazado recibir la comunicación.

RAZONAMIENTOS JURÍDICOS

Primero.- El párrafo 2.º del artículo 15 del Convenio de La Haya sobre notificación o traslado al extranjero de documentos judiciales y extrajudiciales en materia civil o comercial de 15 de noviembre de 1965 establece que «Cada Estado contratante tiene la facultad de declarar que sus jueces, no obstante las disposiciones del párrafo primero, podrán proveer a pesar de no haberse recibido comunicación alguna acreditativa, bien de la notificación o traslado, bien de la entrega, si se dan los siguientes requisitos:

a) El documento ha sido remitido según alguno de los modos previstos por el presente Convenio;
b) Ha transcurrido, desde la fecha de envío del documento, un plazo que el Juez apreciará en cada caso particular y que será, al menos, de seis meses, y
c) No obstante las diligencias oportunas ante las autoridades competentes del Estado requerido, no ha podido obtener certificación alguna».

Segundo.- Aplicando lo anteriormente expuesto al caso de autos, se cumplen todos los requisitos establecidos en el artículo mencionado. En primer lugar, el Estado español declaró, en relación con este artículo que «1) El Estado español declara que sus Jueces, no obstante las disposiciones del párrafo 2, podrán proveer a pesar de no haber recibido notificación alguna acreditativa de la notificación o de la remisión de documentos si se dan los requisitos previstos en el citado artículo 15, párrafo 2». En segundo lugar, el documento ha sido remitido para su notificación o traslado según el modo previsto en el artículo 3 del Convenio, a la Autoridad Central de los Estados Unidos. En tercer lugar, se han realizado por este Tribunal las diligencias oportunas ante la autoridad competente del Estado requerido y no ha podido obtener certificación alguna. Por último, ha transcurrido, desde la fecha de envío del documento, un plazo superior a 6 meses.

Nota: Dependiendo del país donde se realiza la notificación, ésta procede en aplicación del Reglamento (UE) 2020/1784 del Parlamento Europeo y del Consejo de 25 de noviembre de 2020 relativo a la notificación y traslado en los Estados miembros de documentos judiciales y extrajudiciales en materia civil o mercantil. En este Reglamento existe un artículo paralelo (artículo 22.2) al del Convenio que permite continuar el procedimiento si se dan los requisitos allí previstos (prácticamente los mismos que los que aquí se relacionan).

PARTE DISPOSITIVA

Se acuerda continuar con el Procedimiento de Demanda de Juicio [Nº DE PROCEDIMIENTO] promovido por [NOMBRE DE LA PARTE] contra [ACTO O RESOLUCIÓN] hasta dictar la correspondiente Sentencia.

Contra esta resolución y de acuerdo con el artículo 451 de la LEC, se podrá interponer recurso de reposición ante este Tribunal en el plazo de cinco días desde la notificación del mismo. No obstante, se llevará a efecto lo acordado.

Lo manda y firma Su Señoría, de lo que Doy fe.

DILIGENCIA. Seguidamente se cumple lo ordenado y se notifica. Doy fe.

El/la MAGISTRADO-JUEZ El/la LETRADO DE LA ADMINISTRACIÓN DE JUSTICIA

========================================================================
