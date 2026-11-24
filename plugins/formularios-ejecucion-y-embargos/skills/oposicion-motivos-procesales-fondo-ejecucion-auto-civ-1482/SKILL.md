---
name: oposicion-motivos-procesales-fondo-ejecucion-auto-civ-1482
description: "Oposición por motivos procesales y de fondo a la ejecución de un auto de cuantía máxima. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Oposición por motivos procesales y de fondo a la ejecución de un auto de cuantía máxima

> Formulario **CIV-1482** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Escrito por el que la aseguradora ejecutada se opone, por motivos procesales y de fondo, a la ejecución de un auto de cuantía máxima dictado en un proceso penal por accidente de circulación (art. 13 del texto refundido de la Ley sobre responsabilidad civil y seguro en la circulación de vehículos a motor). Alega la nulidad del título (falta de audiencia e indeterminación de la cantidad) y, en cuanto al fondo, culpa exclusiva de la víctima o, subsidiariamente, concurrencia de culpas. Adáptense los hechos al caso.

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Oposición por motivos procesales y de fondo a la ejecución de un auto de cuantía máxima» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Oposición por motivos procesales y de fondo a la ejecución de un auto de cuantía máxima” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:oposicion-motivos-procesales-fondo-ejecucion-auto-civ-1482`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (6 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] SEDE (5 veces)
- [ ] FECHA (4 veces)
- [ ] PORCENTAJE (4 veces)
- [ ] DENOMINACIÓN SOCIAL DE LA ASEGURADORA (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] MATRÍCULA (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL EJECUTANTE (2 veces)
- [ ] ADAPTAR ESTE RELATO A LOS HECHOS DEL CASO CONCRETO.
- [ ] AÑO
- [ ] DÍA
- [ ] EL VEHÍCULO CONDUCIDO POR EL CAUSANTE DE LA PARTE EJECUTANTE
- [ ] IZQUIERDA
- [ ] LOCALIDAD
- [ ] MES
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº DE PROCEDIMIENTO

## Normas que cita el formulario

- art. 556.3 LEC
- art. 13 Real Decreto Legislativo 8/2004
- art. 559 LEC
- art. 556.3.1.º LEC
- art. 559.1.3.º LEC
- art. 556.3.2.º LEC
- art. 1.2 Real Decreto Legislativo 8/2004
- art. 560 LEC
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

### Avisos de actualización (3) — se aplican en el texto, nunca se copian en el documento

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…TAJE] %, debiendo indemnizar mi representada el [PORCENTAJE] % a ella imputable.»: comprobar la redacción vigente del art. 1.2 del texto refundido tras la reforma de la Ley 35/2015 antes de transcribir el precepto.
- Junto a «…aber sido declarada inconstitucional y nula por la STC 140/2016, de 21 de julio.»: comprobar si la oposición a la ejecución está sujeta a la tasa y su cuantía vigente.

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, en representación de [DENOMINACIÓN SOCIAL DE LA ASEGURADORA], según acredito mediante apoderamiento apud acta otorgado ante el Letrado/a de la Administración de Justicia de [SEDE], en autos de ejecución n.º [Nº DE PROCEDIMIENTO], seguidos a instancia de [NOMBRE Y APELLIDOS DEL EJECUTANTE] contra [DENOMINACIÓN SOCIAL DE LA ASEGURADORA], ante el Tribunal comparezco y, como mejor proceda en derecho, DIGO:

1) Que en el proceso penal n.º [Nº] seguido ante la Sección de Instrucción del Tribunal de Instancia de [SEDE] se dictó auto de sobreseimiento, sin declaración de responsabilidad, por fallecimiento de D./Dña. [NOMBRE Y APELLIDOS], dictándose seguidamente auto de cuantía máxima a percibir por los perjudicados D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS] a cuenta de la compañía aseguradora [DENOMINACIÓN SOCIAL DE LA ASEGURADORA], titular de la póliza de seguro obligatorio del vehículo matrícula [MATRÍCULA].

2) Que por parte de la representación de los perjudicados se instó la ejecución del referido auto de cuantía máxima ante el Tribunal al que me dirijo, procediendo éste a despachar ejecución en virtud de auto de fecha [FECHA].

3) Que, al amparo de lo dispuesto en los artículos 556.3 y 559 de la LEC, y dentro del plazo legalmente establecido, procedo a formular OPOSICIÓN A LA EJECUCIÓN POR MOTIVOS PROCESALES Y POR MOTIVOS DE FONDO, ello en base a los siguientes

HECHOS

PRIMERO.– En fecha [FECHA] se iniciaron diligencias previas n.º [Nº] en la Sección de Instrucción del Tribunal de Instancia de [SEDE], habiéndose dictado auto de archivo sin declaración de responsabilidad, firme, en fecha [FECHA].

SEGUNDO.– Descripción del título y motivos de nulidad. Por auto de fecha [FECHA], adjuntado a la demanda, se fijó la cuantía líquida máxima que podía reclamar el perjudicado, adoleciendo dicha resolución de los siguientes defectos:

1) La resolución fue dictada sin que existiera oferta motivada ni respuesta motivada y sin convocar comparecencia, de manera que no se dio audiencia a la aseguradora que represento.

2) La cantidad fijada es indeterminada al remitirse a una cantidad que debía determinarse en ejecución de sentencia, sin fijar ningún tipo de base para su cuantificación.

3) La existencia de tales defectos esenciales implica la nulidad radical del título ejecutivo por cuanto no cumple los requisitos establecidos en el artículo 13 del Real Decreto Legislativo 8/2004, al haber sido dictado sin la preceptiva audiencia de esta parte y al no contener la determinación de la cantidad máxima que puede reclamarse, defectos éstos insubsanables, que deben dar lugar a dejar sin efecto el despacho de ejecución conforme a lo que dispone el artículo 559 de la LEC.

TERCERO.– Descripción del accidente y alegación de culpa exclusiva. En cuanto al fondo, concurre la causa establecida en el artículo 556.3.1.º de la LEC de culpa exclusiva de la víctima, puesto que en el relato fáctico realizado en el auto de cuantía máxima se pone de manifiesto que fue [EL VEHÍCULO CONDUCIDO POR EL CAUSANTE DE LA PARTE EJECUTANTE] el que embistió al vehículo matrícula [MATRÍCULA], propiedad del asegurado de mi representada, colisionando con la parte trasera [IZQUIERDA] del turismo, que se encontraba detenido en la calzada, en lugar habilitado para realizar el giro y habiendo señalizado con suficiente antelación la maniobra.

Todos estos hechos constan en el atestado y fueron presenciados por los testigos reseñados en el mismo, anunciándose desde este momento la intención de esta parte de proponerlos en la vista, de todo lo cual se concluye que la culpa del accidente es la única y exclusiva conducta del ejecutante.

[ADAPTAR ESTE RELATO A LOS HECHOS DEL CASO CONCRETO.]

CUARTO.– Alegación de concurrencia de culpas. De forma subsidiaria, y para el caso de no estimarse la culpa exclusiva de la víctima, se alega la culpa concurrente del perjudicado, lo cual debe determinar equitativa moderación de la responsabilidad y reparto en la cuantía de la indemnización, atendida la respectiva entidad de las culpas concurrentes, siendo indudable que la conducta del perjudicado en todo caso contribuyó de forma relevante y esencial a la causación del daño, siendo la misma de mayor entidad que la del conductor asegurado, tal como se ha descrito en los anteriores expositivos, de manera que se produciría una concurrencia de culpas en la producción del evento dañoso, siendo imputable al ejecutante una culpa que podría concretarse en un porcentaje del [PORCENTAJE] %, debiendo indemnizar mi representada por el [PORCENTAJE] % imputable a su asegurado.

A los anteriores hechos les son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

I.– PROCEDIMIENTO.

Artículos 559, 560 y 561 de la LEC.

II.– OPOSICIÓN POR MOTIVOS PROCESALES.

Al amparo de lo dispuesto en el artículo 559.1.3.º de la LEC se alega la nulidad radical del despacho de ejecución por no cumplir el documento presentado los requisitos legales exigidos para llevar aparejada ejecución.

El artículo 13 del Real Decreto Legislativo 8/2004, de 29 de octubre, por el que se aprueba el texto refundido de la Ley sobre responsabilidad civil y seguro en la circulación de vehículos a motor, establece que en el auto de cuantía máxima se determinará la cantidad líquida máxima que puede reclamarse como indemnización de los daños y perjuicios sufridos por cada perjudicado, amparados por el seguro de suscripción obligatoria y según la valoración que corresponda con arreglo al sistema de valoración de la ley, y contendrá la descripción del hecho, la indicación de las personas y vehículos que intervinieron y de los aseguradores de cada uno; en tanto que el párrafo cuarto del citado precepto establece que, en todo caso, antes de dictarse el auto, si en las actuaciones no consta oferta motivada o respuesta motivada según las prescripciones de esta ley, el juez convocará a los perjudicados y posibles responsables y sus aseguradores, incluido, en su caso, el Consorcio de Compensación de Seguros, a una comparecencia en el plazo de cinco días, a fin de que pueda aportarse la oferta o la respuesta motivada, o hacerse las alegaciones que consideren convenientes.

En el presente caso, el auto fue dictado sin audiencia de mi representada y no determina la cantidad líquida que puede reclamarse por el ejecutante, puesto que únicamente se remite a un eventual trámite de ejecución de sentencia, sin liquidar las cantidades con cargo al seguro obligatorio.

III.– OPOSICIÓN A LA EJECUCIÓN POR MOTIVOS DE FONDO.

1) CULPA EXCLUSIVA DE LA VÍCTIMA (art. 556.3.1.º LEC). La culpa del perjudicado es única y exclusiva, reuniendo los requisitos que determinan la exoneración de responsabilidad en el ámbito del seguro obligatorio, puesto que la conducta de la víctima reúne los requisitos de unicidad, totalidad o carácter excluyente y exclusividad en el origen del daño, al no existir participación negligente de otro o, cuando menos, por cuanto su acción anula o impide la apreciación de otras conductas culposas de otros intervinientes.

2) Subsidiariamente, se alega concurrencia de culpas al amparo del artículo 556.3.2.º de la LEC, en relación con el artículo 1.2 del Real Decreto Legislativo 8/2004, que establece que «sin perjuicio de que pueda existir culpa exclusiva de acuerdo con el apartado 1, cuando la víctima capaz de culpa civil sólo contribuya a la producción del daño se reducirán todas las indemnizaciones, incluidas las relativas a los gastos en que se haya incurrido en los supuestos de muerte, secuelas y lesiones temporales, en atención a la culpa concurrente hasta un máximo del setenta y cinco por ciento. Se entiende que existe dicha contribución si la víctima, por falta de uso o por uso inadecuado de cinturones, casco u otros elementos protectores, incumple la normativa de seguridad y provoca la agravación del daño». De no estimarse la anterior alegación de culpa exclusiva, es indudable que la conducta del perjudicado contribuyó decisivamente al resultado lesivo, por lo que se pretende, de forma subsidiaria, que se aprecie una culpa concurrente del perjudicado que se concreta en un [PORCENTAJE] %, debiendo indemnizar mi representada el [PORCENTAJE] % a ella imputable.

IV.– COSTAS.

Artículos 559.2 y 561.2 LEC, debiendo imponerse al ejecutante.

Por lo expuesto,

SUPLICO AL TRIBUNAL: Tenga por presentada en tiempo y forma la presente oposición a la demanda ejecutiva formulada por [NOMBRE Y APELLIDOS DEL EJECUTANTE] contra mi mandante y, previa su tramitación con suspensión de la ejecución, se dicte resolución por la que se estime la oposición y se deje sin efecto la ejecución despachada. Subsidiariamente, se proceda a estimar parcialmente la oposición, despachando ejecución por la cantidad de [IMPORTE] euros por culpa concurrente del perjudicado. Imponiendo en ambos casos las costas al ejecutante.

OTROSÍ PRIMERO DIGO: De conformidad con el artículo 560 de la LEC se solicita la celebración de vista pública a fin de que se realice la prueba que a continuación se detalla:

1) DOCUMENTAL: se tengan por reproducidos los documentos adjuntos a este escrito y, además, se remita exhorto a la Sección de Instrucción del Tribunal de Instancia n.º [Nº] de [SEDE] para que remita testimonio de los siguientes documentos:

A.– Parte de declaración amistosa de accidente.

B.– Atestado levantado por la Guardia Civil de Tráfico en relación con este siniestro.

C.– Copia del documento justificativo de los rendimientos económicos anuales del ejecutante.

D.– Informe del Médico Forense.

E.– Testimonio íntegro de los autos de las diligencias previas n.º [Nº] seguidos ante la Sección de Instrucción del Tribunal de Instancia.

2) TESTIFICAL: a fin de que los testigos que a continuación se relacionan sean examinados en el acto de la vista:

D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [DOMICILIO].

D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [DOMICILIO].

SUPLICO AL TRIBUNAL: Se proceda a la celebración de la vista pública solicitada al efecto de la práctica de la totalidad de la prueba propuesta.

OTROSÍ SEGUNDO DIGO: [OPCIONAL — incluir si la parte es persona jurídica no exenta de la tasa y el escrito está sujeto a ella] Que, estando el presente escrito sujeto al abono de la tasa por el ejercicio de la potestad jurisdiccional fijada por la Ley 10/2012, de 20 de noviembre, y desarrollada por la Orden HAP/2662/2012, de 13 de diciembre, siendo mi representada persona jurídica no exenta de su pago, se acompaña como documento n.º [Nº] la correspondiente autoliquidación, con el ejemplar para la Administración de Justicia debidamente validado y en el que consta el pago de la cantidad de [IMPORTE] euros correspondiente a la cuota fija, con la bonificación por la utilización de medios telemáticos que proceda, sin que se incluya la cuota variable prevista en el artículo 7.2 de la Ley 10/2012, al haber sido declarada inconstitucional y nula por la STC 140/2016, de 21 de julio.

En virtud de lo anterior, SUPLICO AL TRIBUNAL que tenga por hecha la anterior manifestación a los efectos pertinentes y por acompañado el documento justificativo del abono de la tasa.

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a Firma del Procurador/a
