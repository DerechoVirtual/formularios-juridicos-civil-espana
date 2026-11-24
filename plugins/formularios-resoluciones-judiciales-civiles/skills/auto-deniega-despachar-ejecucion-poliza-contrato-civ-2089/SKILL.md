---
name: auto-deniega-despachar-ejecucion-poliza-contrato-civ-2089
description: "Auto que deniega despachar ejecución de póliza de contrato mercantil por falta de firma del corredor. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Auto que deniega despachar ejecución de póliza de contrato mercantil por falta de firma del corredor

> Formulario **CIV-2089** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

Auto por el que se deniega el despacho de la ejecución solicitada con base en una póliza de contrato mercantil, por no haberse acompañado testimonio con efectos ejecutivos o copia autorizada de la póliza expedida a tal fin, ni acreditado la notificación previa al ejecutado de la cantidad exigible (arts. 517.2.5.º y 552.1 LEC).

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Auto que deniega despachar ejecución de póliza de contrato mercantil por falta de firma del corredor» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Auto que deniega despachar ejecución de póliza de contrato mercantil por falta de firma del corredor” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:auto-deniega-despachar-ejecucion-poliza-contrato-civ-2089`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] AÑO (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] IMPORTE EN LETRA (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] NOMBRE Y APELLIDOS / DENOMINACIÓN SOCIAL DEL EJECUTANTE (2 veces)
- [ ] DÍA
- [ ] FECHA
- [ ] MES
- [ ] NOMBRE Y APELLIDOS / DENOMINACIÓN SOCIAL DEL EJECUTADO
- [ ] Nº DE CUENTA
- [ ] Nº DE GRUPO
- [ ] Nº DE PROCEDIMIENTO

## Normas que cita el formulario

- art. 552.1 LEC
- art. 517.2 LEC
- art. 517.2.5.º LEC

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

AUTO

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Magistrado/a: [NOMBRE Y APELLIDOS]

ANTECEDENTES DE HECHO

ÚNICO.- Por el/la Procurador/a Sr./a. [NOMBRE Y APELLIDOS], actuando en nombre y representación de [NOMBRE Y APELLIDOS / DENOMINACIÓN SOCIAL DEL EJECUTANTE], se formuló demanda ejecutiva, que, turnada a este Tribunal, fue registrada con el número [Nº DE PROCEDIMIENTO] / [AÑO], frente a [NOMBRE Y APELLIDOS / DENOMINACIÓN SOCIAL DEL EJECUTADO], en reclamación de la cantidad de [IMPORTE EN LETRA] euros ([IMPORTE] €) en concepto de principal e intereses ordinarios y moratorios vencidos hasta la fecha, más otros [IMPORTE EN LETRA] euros ([IMPORTE] €) presupuestados provisionalmente para los intereses que, en su caso, puedan devengarse durante la ejecución y las costas de ésta.

FUNDAMENTOS DE DERECHO

ÚNICO.- El art. 552.1 LEC dispone que, si el tribunal entendiese que no concurren los presupuestos y requisitos legalmente exigidos para el despacho de la ejecución, dictará auto denegando el despacho de la ejecución.

En el presente caso nos encontramos con que no se ha acompañado por el ejecutante testimonio con efectos ejecutivos de la póliza, ni copia autorizada de la misma expedida al efecto de su ejecución, tal y como exige el ordinal 5.º del art. 517.2 LEC, omitiendo lo previsto en el párrafo séptimo del apartado primero del art. 17 de la Ley de 28 de mayo de 1862, del Notariado, en su redacción dada por la reforma llevada a cabo por la Ley 36/2006, de 29 de noviembre (1).

Además, no se ha acreditado haber notificado previamente al ejecutado la cantidad exigible resultante de la liquidación efectuada por el acreedor en la forma convenida por las partes en el propio título ejecutivo.

PARTE DISPOSITIVA

SE ACUERDA DENEGAR EL DESPACHO DE LA EJECUCIÓN interesado por la representación de [NOMBRE Y APELLIDOS / DENOMINACIÓN SOCIAL DEL EJECUTANTE].

Lo acuerdo, mando y firmo.

Por ser de justicia, lo pido en [LOCALIDAD], a [FECHA].

Firma del/de la Magistrado/a:

Contra esta resolución cabe recurso de apelación que se interpondrá ante este Tribunal en el plazo de 20 días contados desde el día siguiente de su notificación, sustanciándose sólo con el acreedor, aunque a su elección podrá intentar el recurso de reposición previo a la apelación en el plazo de 5 días.

Para interponer el recurso será necesaria la constitución de un depósito de 50 euros, sin cuyo requisito no será admitido a trámite. El depósito se constituirá consignando dicho importe en la Cuenta de Depósitos y Consignaciones que este Tribunal tiene abierta en el grupo [Nº DE GRUPO] con el número [Nº DE CUENTA], indicando en el campo concepto del resguardo de ingreso que se trata de un "Recurso" código 02-Apelación. La consignación deberá ser acreditada al interponer el recurso (disp. adic. 15.ª LOPJ).

No están obligados a constituir el depósito para recurrir los declarados exentos en la disposición citada y quienes tengan reconocido el derecho a la asistencia jurídica gratuita.

(1) Desde el 1 de diciembre de 2006, fecha de entrada en vigor de la Ley 36/2006, de 29 de noviembre, de medidas para la prevención del fraude fiscal, el Notario conservará en su Libro-Registro o en su protocolo ordinario el original de la póliza, en los términos que reglamentariamente se disponga, y, a los efectos de lo dispuesto en el art. 517.2.5.º LEC, se considerará título ejecutivo el testimonio expedido por el Notario del original de la póliza debidamente conservada en su Libro-Registro o la copia autorizada de la misma, contenida en su protocolo (art. 17.1, párrafo 7.º, Ley del Notariado), y desaparece, por tanto, la certificación a que se refería el art. 517.2.5.º LEC, pues es un contrasentido, en sí mismo, que expidiendo el Notario copia autorizada o testimonio del único original, además deba expedir certificación de que esa copia o testimonio coincide con el original (Instrucción de 29 de noviembre de 2006, de la Dirección General de los Registros y del Notariado, relativa a la conservación de la póliza y a la expedición de copia autorizada o de testimonio de la misma a efectos ejecutivos).
