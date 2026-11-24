---
name: decreto-aprueba-remate-inmuebles-postura-inferior-70-civ-2054
description: "Decreto que aprueba el remate de inmuebles por postura inferior al 70 y superior al 50 por 100. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Decreto que aprueba el remate de inmuebles por postura inferior al 70 y superior al 50 por 100

> Formulario **CIV-2054** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

Auto aprobando el remate de los bienes inmuebles embargados por una postura inferior al 70 por 100 pero superior al 50 por 100 del valor de tasación, al haber vencido los plazos legalmente previstos para que el ejecutado presente tercero que mejore la postura y para que el ejecutante pida la adjudicación de los bienes.

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Decreto que aprueba el remate de inmuebles por postura inferior al 70 y superior al 50 por 100» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Decreto que aprueba el remate de inmuebles por postura inferior al 70 y superior al 50 por 100” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:decreto-aprueba-remate-inmuebles-postura-inferior-70-civ-2054`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (4 veces)
- [ ] IMPORTE EN CIFRA (4 veces)
- [ ] FECHA (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] LUGAR (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] GRUPO
- [ ] LOCALIDAD

## Normas que cita el formulario

- art. 670.3 LEC
- art. 652 LEC

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

DECRETO DEL LETRADO DE LA ADMINISTRACIÓN DE JUSTICIA

En [LUGAR], a [FECHA].

ANTECEDENTES DE HECHO

PRIMERO.- El pasado día [FECHA] se dictó auto despachando ejecución contra los bienes de D./Dña. [NOMBRE Y APELLIDOS], en reclamación de la cantidad de [IMPORTE] euros ([IMPORTE EN CIFRA] €) en concepto de principal e intereses devengados hasta la fecha, más otros [IMPORTE] euros ([IMPORTE EN CIFRA] €) presupuestados provisionalmente para hacer frente a los intereses que, en su caso, puedan devengarse durante la ejecución y las costas de ésta.

SEGUNDO.- Como consecuencia de dicha resolución, mediante decreto, se embargó/aron el/los siguiente/s bien/es inmueble/s propiedad del ejecutado:

TERCERO.- Una vez justipreciado/s el/los bien/es inmueble/s embargado/s, se sacó/aron a subasta, anunciándose mediante edictos que se fijaron en el Portal dependiente de la Agencia Estatal Boletín Oficial del Estado, en el tablón de anuncios de la oficina judicial (en su caso, añadir la publicidad adicional acordada).

CUARTO.- Celebrada la subasta señalada se anunció como mejor postura la de D./Dña. [NOMBRE Y APELLIDOS], por importe de [IMPORTE] euros ([IMPORTE EN CIFRA] €), quien previamente había manifestado conocer las condiciones generales y particulares de la subasta. Tal postura era inferior al 70 por 100 del valor de tasación.

QUINTO.- Han transcurrido los plazos fijados en la LEC, para que el ejecutado presente tercero que mejorara la postura, sin que haya ejercitado tal facultad.

FUNDAMENTOS DE DERECHO

PRIMERO.- Conforme al párrafo cuarto del art. 670.3 LEC, cuando el ejecutado no haga uso de la facultad de mejora a que se refiere el párrafo primero, se aprobará el remate del bien en favor del mejor postor, aunque se haya subastado conjuntamente con otros bienes, siempre que la cantidad que se ofrezca por él sea igual o superior al 50 por ciento de su valor de subasta.

En el presente caso, nos encontramos ante una postura inferior al 70 por 100 pero superior al 50 por 100 del valor de tasación, por lo que vencidos los plazos legalmente previstos para que el ejecutado presente tercero que mejore la postura y para que el ejecutante pida la adjudicación de los bienes, procede aprobar el remate a favor del mejor postor.

SEGUNDO.- Aprobado el remate, procede devolver las cantidades depositadas por los postores excepto la que corresponda al mejor postor, la cual se reservará en depósito como garantía del cumplimiento de su obligación y, en su caso, como parte del precio de la venta (art. 652 LEC).

PARTE DISPOSITIVA

SE ACUERDA APROBAREL REMATE de los bienes inmuebles embargados cuya descripción consta en el antecedente de hecho segundo de esta resolución a favor de D. [NOMBRE Y APELLIDOS], con D.N.I. número [NÚMERO] y domicilio en [LOCALIDAD], por la cantidad de [IMPORTE] euros ([IMPORTE EN CIFRA] €). Devuélvanse a los restantes licitadores las cantidades depositadas para poder participar en la subasta.

Contra esta resolución cabe interponer recurso de revisión, mediante escrito ante el Tribunal que se presenta dentro de los cinco días hábiles siguientes al de notificación, y en el que deberá indicarse la infracción cometida a juicio del recurrente, y sin perjuicio del cual se llevará a efecto lo acordado.

Para interponer el recurso será necesario la constitución de un depósito de 25 euros, sin cuyo requisito no será admitido a trámite. El depósito se constituirá consignando dicho importe en la Cuenta de Depósitos y Consignaciones que este Tribunal tiene abierta en el grupo [GRUPO] con el número [NÚMERO], indicando en el campo concepto del resguardo de ingreso que se trata de un "Recurso" código 01-Revisión. La consignación deberá ser acreditada al interponer el recurso (disp. adic. 15.ª de la LOPJ).

Están exentos de constituir el depósito para recurrir los incluidos en el apartado 5 de la disposición citada y quienes tengan reconocido el derecho a la asistencia jurídica gratuita.

Así lo acuerdo y firmo.

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma del Letrado de la Administración de Justicia

========================================================================
