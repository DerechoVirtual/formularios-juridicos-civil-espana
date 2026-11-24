---
name: solicitud-medida-cautelar-prohibicion-hacer-demandado-civ-1244
description: "Solicitud de medida cautelar de prohibición de hacer al demandado, sin audiencia y con caución. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de medida cautelar de prohibición de hacer al demandado, sin audiencia y con caución

> Formulario **CIV-1244** del plugin **Medidas cautelares y diligencias preliminares** (`formularios-medidas-cautelares-civiles`) · Civil › Medidas cautelares y diligencias preliminares · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de medida cautelar de prohibición de hacer al demandado, sin audiencia y con caución» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de medida cautelar de prohibición de hacer al demandado, sin audiencia y con caución” para mi caso». También puedes invocarla directamente con `/formularios-medidas-cautelares-civiles:solicitud-medida-cautelar-prohibicion-hacer-demandado-civ-1244`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-medidas-cautelares-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Medidas cautelares y diligencias preliminares) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] IMPORTE (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] AÑO
- [ ] DIRECCIÓN
- [ ] DÍA
- [ ] ENFERMEDAD O DISCAPACIDAD
- [ ] MES
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº DE DOCUMENTO
- [ ] SEDE

## Normas que cita el formulario

- art. 723.1 LEC
- art. 50 LEC
- art. 721 LEC
- art. 730.2 LEC
- art. 733.2 LEC
- art. 1908 CC
- art. 728.2 LEC
- art. 728.1 LEC
- art. 727.7.ª LEC
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

D. [NOMBRE Y APELLIDOS] Procurador de los Tribunales, actuando en representación de [NOMBRE DEL REPRESENTADO/A], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], por medio de la presente solicito medida cautelar de prohibición de realización de actividad a D. [NOMBRE Y APELLIDOS] con domicilio en [LOCALIDAD] en base a los siguientes:

HECHOS

ÚNICO.-Que mi mandante D. es titular del inmueble situado en [DIRECCIÓN] tal y como deriva de la escritura de compraventa que se adjunta como documento n.º [NÚMERO], siendo el futuro demandado D. [NOMBRE Y APELLIDOS] que es el titular del inmueble contiguo tal y como deriva de la certificación del Registro de la Propiedad que se adjunta como documento n.º [NÚMERO] Mi mandante está afecto de una [ENFERMEDAD O DISCAPACIDAD] tal y como consta en el certificado médico que se aporta no pudiendo sufrir un contacto directo con humos como los que se desprenden de la instalación que el futuro demandado tiene en su finca y que se acreditan por medio de las fotografías que se adjuntan a esta petición. El propósito de mi mandante es interponer una demanda para que se acuerde la prohibición definitiva del ejercicio de tal actividad.

FUNDAMENTOS DE DERECHO

PRIMERO.- Competencia.-Le corresponde al Tribunal al que me dirijo ya que es el competente para conocer de la demanda principal que se formule con fundamento en el art. 723.1 LEC al ser en ese partido en el que está domiciliado el demandado (art. 50 LEC).

SEGUNDO.- Legitimación.-Le corresponde a esta parte ante su condición de acreedor y con ello futuro actor de la demanda que se pretende interponer (art. 721 LEC).

TERCERO.- Procedimiento.-Es el previsto en el art. 730.2 LEC al interesarse la adopción de la medida cautelar son carácter previo a la interposición de la demanda y sin audiencia del demandado (art. 733.2 LEC) ya que concurren en este caso razones de urgencia pues el demandado continúa con las emisiones, mi mandante está pendiente de un análisis científico de las mismas y dada la enfermedad de la que está afectado su salud se ve seriamente comprometida.

CUARTO.- Apariencia de buen derecho.-Se deriva de la documentación adjunta a esta solicitud y en la que consta la existencia de la inmisión que se considera incorrecta a los efectos del art. 1908 CC (art. 728.2 LEC).

QUINTO.- Peligro de mora.-Se deriva de la propia situación en la que se encuentra la instalación del demandado que puede por el transcurso del tiempo hacer empeorar el estado de salud de mi mandante de modo que solamente con la medida cautelar que se interesa se garantiza la efectividad de una eventual sentencia favorable que se pudiere dictar en beneficio de mi mandante (art. 728.1 LEC).

SEXTO.- Medida interesada.-Es la de cese de una actividad por parte del demandado del art. 727.7.ª de la LEC.

SÉPTIMO.- Caución.-Con fundamento en el art. 732.3 LEC se solicita sea fijada ésta en [IMPORTE] Euros dadas las condiciones de derecho expuesto y los posibles perjuicios que se le pudieren generar por ello ante el cese de la actividad que se interesa.

En base a lo anterior,

SUPLICO AL TRIBUNAL: Que tenga por presentado escrito con los documentos a él anejos y copias, tenga por comparecido a esta parte y ordene a D. [NOMBRE Y APELLIDOS] con domicilio en [LOCALIDAD] para que proceda de forma inmediata a cesar en el desempeño de la actividad que desarrolla en el inmueble de su titularidad sito en [LOCALIDAD] y que perjudica a la salud de mi mandante. Esta medida cautelar se solicita se acuerde con carácter previo a la presentación de la demanda y sin audiencia del demandado al concurrir motivos de urgencia. De cara a la adopción de tal medida cautelar se solicita asimismo que se tenga por ofrecida una caución de [IMPORTE] Euros.

a [DÍA] de [MES] de [AÑO]

Firma Abogado	Firma Procurador

========================================================================
