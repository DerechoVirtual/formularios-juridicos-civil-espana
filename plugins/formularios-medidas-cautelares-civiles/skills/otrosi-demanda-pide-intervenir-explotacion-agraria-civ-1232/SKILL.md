---
name: otrosi-demanda-pide-intervenir-explotacion-agraria-civ-1232
description: "Otrosí de demanda que pide intervenir una explotación agraria como cautelar (art. 727.2 LEC). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Otrosí de demanda que pide intervenir una explotación agraria como cautelar (art. 727.2 LEC)

> Formulario **CIV-1232** del plugin **Medidas cautelares y diligencias preliminares** (`formularios-medidas-cautelares-civiles`) · Civil › Medidas cautelares y diligencias preliminares · normativa revisada el 24-11-2026.

## Qué es

FUNDAMENTOS DE DERECHO

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Otrosí de demanda que pide intervenir una explotación agraria como cautelar (art. 727.2 LEC)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Otrosí de demanda que pide intervenir una explotación agraria como cautelar (art. 727.2 LEC)” para mi caso». También puedes invocarla directamente con `/formularios-medidas-cautelares-civiles:otrosi-demanda-pide-intervenir-explotacion-agraria-civ-1232`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-medidas-cautelares-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Medidas cautelares y diligencias preliminares) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FINCA (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] OBJETO DEL CONTRATO

## Normas que cita el formulario

- art. 727.2.ª LEC
- art. 723.1 LEC
- art. 721 LEC
- art. 733 LEC
- art. 728.2 LEC
- art. 732.3 LEC

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

OTROSÍ DIGO: Que, según se ha expuesto en la presente demanda, la misma tiene por objeto la reivindicación de la finca [FINCA] en la que la mercantil demandada explota el cultivo de la cebada, al no haber sido entregada en la forma convenida por el contrato privado de [OBJETO DEL CONTRATO], adjunto como documento n.º [NÚMERO], una vez abonado por mi principal su importe, según resulta de los documentos n.º [NÚMERO]. Es por ello que se solicita la medida cautelar de intervención en la administración de la finca prevista en el art. 727.2.ª LEC, con la finalidad de controlar el ejercicio de las labores agrícolas, de modo que se verifiquen éstas en forma adecuada y sin perjuicio de reservarse esta parte el derecho de solicitar la constitución de una administración judicial en el caso de constatarse de la inidoneidad de la labor ejecutada.

FUNDAMENTOS DE DERECHO

PRIMERO.- Competencia.-Le corresponde al Tribunal al que me dirijo ya que es aquel ante el que se ha presentado la demanda principal (art. 723.1 LEC).

SEGUNDO.- Legitimación.- Le corresponde a esta parte ante su condición de demandante en las presentes actuaciones (art. 721 LEC).

TERCERO.- Procedimiento.- Es el previsto en el art. 733 LEC, interesando que la medida se acuerde con audiencia de la mercantil demandada, procediendo en la misma comparecencia, en caso de estimarse pertinente la medida cautelar, a la determinación de la persona que va a actuar como interventor.

CUARTO.- Apariencia de buen derecho.- Se deriva de la documentación adjunta a esta solicitud, en la que consta el crédito del que se estima es titular esta parte (art. 728.2 LEC).

QUINTO.- Peligro de mora.- Se deriva del mismo bien que es objeto de reclamación (una finca agrícola en plena explotación), que se solicita continúe en adecuada forma ante las consecuencias perniciosas que pudiere tener un abandono de la producción por parte de la mercantil demandada, ante el conocimiento de la pendencia del presente proceso.

SEXTO.- Medida interesada.- Es la de la intervención en la administración fijada en el art. 727.2.ª de la LEC, solicitando que la misma recaiga, de ser ello posible, en la persona de [NOMBRE Y APELLIDOS].

SÉPTIMO.- Caución.- Con fundamento en el art. 732.3 LEC, se solicita sea fijada ésta en [IMPORTE] euros, dado el valor del inmueble acordado en la venta y los posibles perjuicios que se le pudieren generar por ello.

En base a lo anterior,

SUPLICO AL TRIBUNAL: Que, previos los trámites pertinentes, tenga a bien acordar la medida cautelar de intervención en la administración de la finca [FINCA] propiedad de la mercantil frente a la que se interpone la presente demanda y en la que se lleva a cabo una explotación de cebada, interesando la designación como interventor de D. [NOMBRE Y APELLIDOS]. De cara a la adopción de tal medida cautelar, se solicita asimismo que se tenga por ofrecida una caución de [IMPORTE] euros.

========================================================================
