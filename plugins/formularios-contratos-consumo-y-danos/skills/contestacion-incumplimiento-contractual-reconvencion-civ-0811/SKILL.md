---
name: contestacion-incumplimiento-contractual-reconvencion-civ-0811
description: "Contestación por incumplimiento contractual con reconvención de resolución e indemnización. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contestación por incumplimiento contractual con reconvención de resolución e indemnización

> Formulario **CIV-0811** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contestación por incumplimiento contractual con reconvención de resolución e indemnización» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contestación por incumplimiento contractual con reconvención de resolución e indemnización” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:contestacion-incumplimiento-contractual-reconvencion-civ-0811`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] IMPORTE (3 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] AÑO (2 veces)
- [ ] DESCRIBIR
- [ ] DÍA
- [ ] FECHA
- [ ] MES
- [ ] Nº
- [ ] Nº DE PROCEDIMIENTO
- [ ] SEDE
- [ ] TIPO DE PROCEDIMIENTO
- [ ] ÓRGANO

## Normas que cita el formulario

- art. 249.2 LEC
- art. 1544 CC
- art. 1124 CC
- art. 394 LEC
- art. 406 LEC
- art. 1121 CC
- art. 1100 CC
- art. 7.2 Ley 10/2012

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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…TO]/[AÑO] A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

Juicio [TIPO DE PROCEDIMIENTO] n.º [Nº DE PROCEDIMIENTO]/[AÑO]

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D. [NOMBRE Y APELLIDOS] Procurador de los Tribunales, actuando en representación de D. [NOMBRE Y APELLIDOS], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], comparezco en el presente procedimiento en el que se emplazó a mi representada el pasado [FECHA] y por medio de la presente paso a contestar a la demanda interpuesta contra mi principal en base a los siguientes:

HECHOS

PRIMERO.- Se rechazan los distintos hechos invocados en la demanda salvo aquellos que sean objeto de un reconocimiento expreso.

SEGUNDO.- Se reconoce la existencia de una relación contractual entre las partes por medio de la que mi principal encargó a la demandante la colocación de un parquet de tarima en la vivienda de la que es titular. Asimismo se reconoce el abono de un 50% del importe de tal instalación, así como la falta de abono del resto del precio a consecuencia de las deficiencias apreciadas en el mismo a las que solamente se les puede dar solución mediante la recolocación de nuevo del parquet. Tales deficiencias resultan del acta notarial al efecto levantada y que se aporta como documento n.º [NÚMERO] y el análisis de las mismas se hace en el informe elaborado por D. [NOMBRE Y APELLIDOS] que se adjunta como documento n.º [Nº DE DOCUMENTO]

FUNDAMENTOS DE DERECHO

PRIMERO.- Procedimiento.-Se acepta la tramitación de la causa por los trámites del juicio ordinario con fundamento en el art. 249.2 LEC y asumiendo las alegaciones en este sentido vertidas en el escrito de demanda.

SEGUNDO.- Fondo de la reclamación.-Se estima improcedente la misma ante el incumplimiento de las obligaciones derivadas del contrato de arrendamiento de obra del art. 1544 CC por parte del demandante, al haber llevado a cabo la instalación del parquet con unas imperfecciones de tal naturaleza que lo hace inidóneo para la finalidad del mismo debiéndose proceder a su total sustitución lo que supone que se ha entregado un aliud pro alio concurriendo la causa de resolución del art. 1124 CC, resolución que por vía de reconvención se va a interesar.

TERCERO.- En materia de costas el art. 394 LEC.

En base a lo anterior,

SUPLICO AL TRIBUNAL que tenga por presentado este escrito junto con sus copias, teniendo a esta parte por personada en las presentes actuaciones entendiéndose conmigo las siguientes diligencias y por contestada a la demanda interpuesta contra mi principal y tras la pertinente tramitación se sirva dictar sentencia por la que se desestime la demanda presentada contra mi principal con imposición de costas al demandante.

RECONVENCIÓN

HECHOS

ÚNICO.-Que como se ha indicado en la contestación de la demanda, el parquet que el Sr. frente al que se interpone la presente reconvención es manifiestamente inidóneo para la finalidad que se pretendía con su colocación ante las deficiencias apreciables en el acta notarial y que detalla el perito Sr. [NOMBRE Y APELLIDOS] en el informe que se adjunta como documento n.º [NÚMERO] y consistentes en [DESCRIBIR], siendo completamente imposible una reparación del parquet al ser la única solución a adoptar la de proceder a una nueva instalación. Ello hace que con esta demanda reconvencional se solicite además de la resolución, la restitución de las prestaciones que consisten en las cantidades abonadas por mi principal y que ascienden a [IMPORTE] como reconoce el actor en su demanda y resultan de los documentos n.º [NÚMERO] de esta reconvención. A ello se añade el coste no de una nueva instalación de parquet mas sí de la de desmontaje del actualmente existente que es algo únicamente imputable al reconvenido y que asciende a [IMPORTE] Euros. Ello hace que el total de la presente reconvención sea de

FUNDAMENTOS DE DERECHO

PRIMERO.- Competencia.-La tiene el Tribunal al que me dirijo al ser el que está conociendo del asunto en el que el litigio se ha suscitado con fundamento en los arts. 406 y 407 LEC.

SEGUNDO.- Fondo de la reclamación.-Lo es el art. 1121 CC que determina que ante un incumplimiento de las obligaciones se tiene la facultad de resolverlas con indemnización de daños y perjuicios.

TERCERO.- En cuanto a los intereses se solicitan los mismos desde la presente reconvención al cumplirse con ella los requisitos de la mora con fundamento en el art. 1100 CC.

CUARTO.- En materia de costas el art. 394 LEC.

En base a lo anterior,

SUPLICO AL TRIBUNAL, se tenga por presentado este escrito y documentos al mismo adjuntos y por formulada demanda reconvencional contra el demandante [ÓRGANO], se sirva admitirla y tras la adecuada tramitación se dicte sentencia por la que se condene al reconvenido a abonar a mi principal la cantidad de [IMPORTE] Euros intereses desde la presente reconvención y costas.

OTROSÍ DIGO.-Que estando la presente demanda sujeta al abono de la tasa por el ejercicio de la potestad jurisdiccional fijada por la Ley 10/2012, de 20 de noviembre, modificada por RDL 3/2013 y Ley 25/2015, de 28 julio, y desarrollada por Orden HAP/2662/2012, de 13 de diciembre, siendo mi representada personas jurídica no exenta de su pago, se acompaña a la presente demanda como documento nº [Nº DE DOCUMENTO] la correspondiente autoliquidación con el ejemplar para la Administración de Justicia debidamente validado y en el que consta el pago de la cantidad de 300 euros correspondiente a la cuota fija, sin que se incluya la cuota variable prevista en el artículo 7.2 de la Ley 10/2012 al haber sido declarado inconstitucional y nulo por la STC 140/2016, de 21 de julio.

En virtud de lo anterior,

SUPLICO AL TRIBUNAL: que tenga por hecha la anterior manifestación a los efectos pertinentes y por acompañado el documento justificativo del abono de la tasa.

a [DÍA] de [MES] de [AÑO]

Firma Abogado	Firma Procurador

========================================================================
