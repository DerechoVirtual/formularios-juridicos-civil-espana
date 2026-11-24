---
name: otrosi-pide-anotacion-preventiva-demanda-como-medida-civ-1228
description: "Otrosí que pide la anotación preventiva de la demanda como medida cautelar. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Otrosí que pide la anotación preventiva de la demanda como medida cautelar

> Formulario **CIV-1228** del plugin **Medidas cautelares y diligencias preliminares** (`formularios-medidas-cautelares-civiles`) · Civil › Medidas cautelares y diligencias preliminares · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Otrosí que pide la anotación preventiva de la demanda como medida cautelar» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Otrosí que pide la anotación preventiva de la demanda como medida cautelar” para mi caso». También puedes invocarla directamente con `/formularios-medidas-cautelares-civiles:otrosi-pide-anotacion-preventiva-demanda-como-medida-civ-1228`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-medidas-cautelares-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Medidas cautelares y diligencias preliminares) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NÚMERO (4 veces)
- [ ] IMPORTE (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] FINCA (2 veces)
- [ ] NOMBRE DE LA PARTE (2 veces)
- [ ] DENOMINACIÓN SOCIAL
- [ ] DÍA
- [ ] MES
- [ ] Nº DE DOCUMENTO

## Normas que cita el formulario

- art. 727.5 LEC
- art. 42.1 LH
- art. 723.1 LEC
- art. 721 LEC
- art. 733 LEC
- art. 733.2 LEC
- art. 34 LH
- art. 728.2 LEC
- art. 728.1 LEC
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

OTROSÍ DIGO.-Que según se ha expuesto en la presente demanda, la misma tiene por objeto la rescisión del contrato por el que se constituye la hipoteca a favor de la entidad codemandada [DENOMINACIÓN SOCIAL] de la finca [FINCA] inscrita a nombre del otro codemandado [NOMBRE DE LA PARTE] en el Registro de la Propiedad de [LOCALIDAD] con el nº [NÚMERO] tal y como resulta de la certificación adjunta como documento nº [Nº DE DOCUMENTO] Es por ello que se solicita la medida cautelar de anotación preventiva de la demanda prevista en el art. 727.5ª LEC y art. 42.1 LH.

FUNDAMENTOS DE DERECHO

PRIMERO.- Competencia.- Le corresponde al Tribunal al que me dirijo ya que es aquel ante el que se ha presentado la demanda principal (art. 723.1 LEC).

SEGUNDO.- Legitimación.- Le corresponde a esta parte ante su condición de demandante en las presentes actuaciones (art. 721 LEC).

TERCERO.- Procedimiento.- Es el previsto en el art. 733 LEC, solicitando que la medida se adopte sin audiencia del demandado (art. 733.2 LEC), ya que la misma puede comprometer el buen fin de la medida cautelar que se solicita, al poder el demandado disponer, en el periodo que mediare entre el conocimiento de la pendencia del proceso y la adopción de la medida cautelar, del bien reclamado a favor de un tercero que pudiere ostentar la condición de tercero de buena fe a los efectos del art. 34 LH, lo que haría el bien irreivindicable, no pudiendo por ello ver mi principal satisfechos sus legítimos derechos en el caso de estimarse la demanda que se presenta.

CUARTO.- Apariencia de buen derecho.- Se deriva de la documentación adjunta a esta solicitud, en la que consta un principio de prueba suficiente de la rescisión pretendida (art. 728.2 LEC).

QUINTO.- Peligro de mora.- Se deriva de la falta de otros bienes en poder del deudor y de la posibilidad de que se ejecute la hipoteca, ya que solamente con la medida cautelar solicitada se podrá garantizar la efectividad de una eventual sentencia favorable que se pudiere dictar en beneficio de mi mandante (art. 728.1 LEC).

SEXTO.- Medida interesada.- Es la de anotación preventiva de demanda fijada en el art. 727.5ª de la LEC y 42.1 LH sobre la finca nº [NÚMERO] del Registro de la Propiedad nº [NÚMERO] de [LOCALIDAD].

SÉPTIMO.- Caución.- Con fundamento en el art. 732.3 LEC, se solicita sea fijada ésta en [IMPORTE] €, dado el valor del inmueble acordado en la venta, la situación de la mercantil demandada y los posibles perjuicios que se le pudieren generar por ello.

En base a lo anterior,

SUPLICO AL TRIBUNAL que acuerde la anotación preventiva de la demanda presentada sobre la finca [FINCA] inscrita en el Registro de la Propiedad nº [NÚMERO] titularidad de [NOMBRE DE LA PARTE] frente a la que se interpone la presente demanda que se interesa se acuerde sin audiencia del demandado. De cara a la adopción de tal medida cautelar se solicita asimismo que se tenga por ofrecida una caución de [IMPORTE] €.

OTROSÍ DIGO.-Se fija la cuantía del presente procedimiento en [IMPORTE] €.

Con base en lo anterior

SUPLICO AL TRIBUNAL se tenga por efectuada la anterior manifestación a los efectos pertinentes.

Es justicia que insto en la localidad de [LOCALIDAD], a [DÍA], de [MES] del año

========================================================================
