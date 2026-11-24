---
name: medidas-cautelares-previas-proceso-ante-tribunal-otro-civ-1216
description: "Medidas cautelares previas a un proceso ante tribunal de otro Estado de la Unión Europea. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Medidas cautelares previas a un proceso ante tribunal de otro Estado de la Unión Europea

> Formulario **CIV-1216** del plugin **Medidas cautelares y diligencias preliminares** (`formularios-medidas-cautelares-civiles`) · Civil › Medidas cautelares y diligencias preliminares · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Medidas cautelares previas a un proceso ante tribunal de otro Estado de la Unión Europea» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Medidas cautelares previas a un proceso ante tribunal de otro Estado de la Unión Europea” para mi caso». También puedes invocarla directamente con `/formularios-medidas-cautelares-civiles:medidas-cautelares-previas-proceso-ante-tribunal-otro-civ-1216`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-medidas-cautelares-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Medidas cautelares y diligencias preliminares) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (7 veces)
- [ ] Nº DE DOCUMENTO (5 veces)
- [ ] NÚMERO (4 veces)
- [ ] DENOMINACIÓN SOCIAL (3 veces)
- [ ] IMPORTE (2 veces)
- [ ] AÑO
- [ ] DIRECCIÓN
- [ ] DOMICILIO
- [ ] DÍA
- [ ] FINCA
- [ ] LUGAR
- [ ] MES
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] NOMBRE Y APELLIDOS
- [ ] SEDE

## Normas que cita el formulario

- art. 721 LEC
- art. 730.2 LEC
- art. 733.2 LEC
- art. 728.2 LEC
- art. 728.1 LEC
- art. 727.1 LEC
- art. 629 LEC
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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D. [NOMBRE Y APELLIDOS] Procurador de los Tribunales, actuando en representación de [NOMBRE DEL REPRESENTADO/A] según se acredita mediante copia electrónica del poder notarial de representación informática (o digitalizada) que se acompaña y se solicita sea devuelta una vez testimoniada (o en virtud de apoderamiento apud acta que se otorgará ante la Secretaría de ese Tribunal) por medio de la presente solicito embargo preventivo de bienes de la mercantil [DENOMINACIÓN SOCIAL] con domicilio en [LOCALIDAD] en base a los siguientes:

HECHOS

PRIMERO.- Que mi mandante D. suministró a la mercantil [DENOMINACIÓN SOCIAL], domiciliada en [DOMICILIO] y en la fábrica de la misma ubicada en [DIRECCIÓN] diversas entregas de material de construcción tal y como resulta de los albaranes que se adjuntan como documentos nº [Nº DE DOCUMENTO] elaborándose las pertinentes facturas que se aportan como documentos nº [Nº DE DOCUMENTO] y que han resultado impagadas no atendiéndose la reclamación previa que al efecto se interpuso y que se acredita como documento nº [Nº DE DOCUMENTO], teniendo intención mi mandante de interponer una demanda a este respecto.

SEGUNDO.- La mercantil demandada se encuentra en una situación de dificultad económica tal y como se deriva de los procedimientos planteados contra la misma y en los que esta situación se ha acreditado tal y como resulta del documento nº [Nº DE DOCUMENTO] que se une a esta solicitud. Aún cuando para conocer de la demanda que se va a interponer por estos hechos la competencia corresponde a los tribunales franceses, ello no obstante, constándole a esta parte la titularidad por parte de la demandada de una finca ubicada en este partido judicial, se interesa la adopción de medidas cautelares en cuanto a la misma. Dicha finca es la que resulta de la nota simple del Registro de la Propiedad nº [NÚMERO] de [LOCALIDAD] que se adjunta como documento nº [Nº DE DOCUMENTO]

FUNDAMENTOS DE DERECHO

Competencia

Aún cuando la competencia para conocer de la demanda objeto de las presentes actuaciones corresponde a los tribunales de [LOCALIDAD] con fundamento en el art. 5 del Reglamento 1215/2012, se interpone esta petición de medidas cautelares ante el Tribunal al que me dirijo con fundamento en el art. 35 de ese mismo Reglamento dada la ubicación de los bienes y a los solos efectos de obtener la tutela cautelar, sin perjuicio de la ulterior interposición de la demanda principal ante los tribunales de [LOCALIDAD]. Este es el criterio competencial que asimismo se estima aplicable en cuanto a la competencia territorial.

Legitimación

Le corresponde a esta parte ante su condición de acreedor y con ello futuro actor de la demanda de reclamación de cantidad que se pretende interponer (art. 721 LEC).

Procedimiento

Es el previsto en el art. 730.2 LEC al interesarse la adopción de la medida cautelar son carácter previo a la interposición de la demanda y sin audiencia del demandado (art. 733.2 LEC) pues concurren en este caso razones de urgencia ya que ante la situación de iliquidez de la mercantil frente a la que se solicitan las medidas cautelares en cualquier momento puede deshacerse de sus bienes y desaparecer del tráfico con el perjuicio que ello ocasionaría a mi mandante que no vería satisfecho el importe de su crédito.

Apariencia de buen derecho

Se deriva de la documentación adjunta a esta solicitud y en la que consta el crédito del que es titular esta parte (art. 728.2 LEC).

Peligro de mora

Se deriva de la situación económica en la que se encuentra la mercantil frente a la que se va a interponer la demanda ya que solamente con la medida cautelar solicitada se podrá garantizar la efectividad de una eventual sentencia favorable que se pudiere dictar en beneficio de mi mandante (art. 728.1 LEC).

Medida interesada

Es la del embargo preventivo de inmuebles fijada en el art. 727.1ª de la LEC sobre la finca nº [NÚMERO] del Registro de la Propiedad nº [NÚMERO] de [LOCALIDAD], interesándose asimismo la anotación preventiva de éste con fundamento en el art. 629 LEC.

Caución

Con fundamento en el art. 732.3 LEC se solicita sea fijada ésta en [IMPORTE] € dadas las condiciones del crédito expuesto, la situación de la mercantil y los posibles perjuicios que se le pudieren generar por ello.

En base a lo anterior,

SUPLICO AL TRIBUNAL que tenga por presentado escrito con los documentos a él anejos y copias, tenga por comparecido a esta parte y acuerde el embargo preventivo de la finca [FINCA] inscrita en el Registro de la Propiedad nº [NÚMERO] titularidad de [DENOMINACIÓN SOCIAL], mercantil frente a la que se tiene intención de interponer demanda ante los tribunales de [LOCALIDAD] en el plazo legalmente previsto para ello desde la adopción de la medida cautelar solicitando que se acuerde la misma con carácter previo a la presentación de la demanda y sin audiencia del demandado al concurrir motivos de urgencia. Asimismo se interesa que en caso de decretarse se acuerde la anotación preventiva del embargo decretado dirigiendo el pertinente mandamiento al Registro de la Propiedad de [LOCALIDAD] De cara a la adopción de tal medida cautelar se solicita asimismo que se tenga por ofrecida una caución de [IMPORTE] euros.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

========================================================================
