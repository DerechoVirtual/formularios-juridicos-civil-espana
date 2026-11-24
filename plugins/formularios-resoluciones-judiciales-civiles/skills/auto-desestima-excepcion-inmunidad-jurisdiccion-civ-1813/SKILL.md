---
name: auto-desestima-excepcion-inmunidad-jurisdiccion-civ-1813
description: "Auto que desestima la excepción de inmunidad de jurisdicción alegada por una parte. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Auto que desestima la excepción de inmunidad de jurisdicción alegada por una parte

> Formulario **CIV-1813** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Auto que desestima la excepción de inmunidad de jurisdicción alegada por una parte» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Auto que desestima la excepción de inmunidad de jurisdicción alegada por una parte” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:auto-desestima-excepcion-inmunidad-jurisdiccion-civ-1813`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] LOCALIDAD
- [ ] MES
- [ ] NOMBRE Y APELLIDOS
- [ ] SEDE

## Normas que cita el formulario

- art. 65 LEC
- art. 64 LEC
- art. 36.2 LEC
- art. 21 LOPJ
- art. 66.2 LEC
- art. 452 LEC

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

Tribunal de Instancia de [SEDE]

Autos de procedimiento [Nº DE PROCEDIMIENTO]

En los Autos reseñados se ha dictado

AUTO

Magistrado- Juez Sr.- [NOMBRE Y APELLIDOS]

En la ciudad de [LOCALIDAD] a [DÍA] de [MES] de [AÑO].

ANTECEDENTES DE HECHO

Primero.- Que presentada demanda de juicio [Nº DE PROCEDIMIENTO] por la parte actora y admitida a trámite, fue presentado escrito de declinatoria por la parte demandada en el plazo legalmente previsto, alegando falta de Jurisdicción por causa de concurrir inmunidad de jurisdicción.

Segundo.- Siguiendo la tramitación prevista en el artículo 65 LEC, y con suspensión del procedimiento, se dio traslado del mismo a la parte actora quien se opuso a la declinatoria alegando lo que estimó por conveniente.

FUNDAMENTOS DE DERECHO

Primero.- La parte demandada interpuso incidente de declinatoria por falta de jurisdicción, adjuntando a su escrito los documentos que acreditan la pretensión de la excepción procesal planteada. La interposición del incidente conlleva la suspensión de las actuaciones de conformidad con el artículo 64 LEC. Frente a la pretensión de la declinatoria de inmunidad de Jurisdicción, la parte actora principal interesó la desestimación del incidente por entender que no concurren los presupuestos de la excepción procesal solicitada.

Segundo.- El artículo 36.2 LEC expresa que "Los tribunales civiles españoles se abstendrán de conocer de los asuntos que se les sometan cuando concurra en ellos alguna de las circunstancias siguientes: 1.ª Cuando se haya formulado demanda o solicitado ejecución respecto de sujetos o bienes que gocen de inmunidad de jurisdicción o de ejecución de conformidad con la legislación española y las normas del Derecho Internacional Público (...)". Según el citado precepto, de concurrir inmunidad de jurisdicción del demandado, se carece de jurisdicción, o en expresión de la LEC, se carece de "competencia internacional" y por tanto, los tribunales españoles, y por ende este Tribunal, no pueden conocer del asunto objeto del litigio.

Tercero.- La excepción de inmunidad de jurisdicción debe apreciarse según indica el artículo 21 LOPJ: "2. No obstante, no conocerán de las pretensiones formuladas respecto de sujetos o bienes que gocen de inmunidad de jurisdicción y de ejecución de conformidad con la legislación española y las normas de Derecho Internacional Público". En consecuencia, son las normas del Derecho internacional público las que refieren si la actuación del demandado queda al amparo de la excepción de inmunidad de jurisdicción. Por no ser aplicable en el presente asunto ninguno de los Convenios internacionales que regulan la inmunidad de jurisdicción de los que España es parte, su concurrencia o no debe ser apreciada de conformidad con las reglas establecidas por el Derecho Internacional Público general.

En este sentido, desde una regla de inmunidad de jurisdicción absoluta, fundada en la igual soberanía de los Estados y expresada por el adagio par in parem imperium non habet, donde la jurisdicción quedaba excluida por la mera presencia de un sujeto o un bien con una determinada cualidad soberana, el ordenamiento internacional ha evolucionado hacia una inmunidad de jurisdicción relativa, de aplicación restrictiva. La relativización de la excepción distingue entre actuación iure imperii o iure gestionis de tal manera que los Tribunales nacionales pueden ejercer su jurisdicción respecto de aquellos sujetos demandados o sus bienes siempre que su actuación no se realice en el ejercicio de su potestad de imperium, sino con sujeción a las reglas ordinarias del tráfico privado (actuación iure gestionis). Es por tanto, el carácter soberano o no de la actuación enjuiciada el criterio que determina la apreciación o no de la excepción de inmunidad de jurisdicción y ejecución. Esta distinción puede ser considerada como norma de Derecho Internacional general y es seguida por la Jurisprudencia tanto del Tribunal Constitucional (STC, Sala 2ª, 107/1992 de 1 julio 1992; STC, Sala 1ª, 292/1994 de 27 octubre 1994) como del Tribunal Supremo (STS de 1 diciembre 1986, STS de 10 de febrero de 1986) y la doctrina de las Audiencias Provinciales (SAP Madrid de 20 enero 1994, SAP Madrid 8 octubre 1996 y SAP Almería 15 julio 2004).

Esta jurisprudencia estima, básicamente, que la inmunidad de jurisdicción y ejecución son privilegios jurisdiccionales que no deben operar "cuando se trata de simples actos de gestión, en los que el Estado actúa como un particular o de acuerdo con las normas de Derecho privado" (STS, Sala 6ª, de 1 diciembre 1986).

En las presentes actuaciones, de un examen pormenorizado del principio de prueba aportado por la demandada se deduce que no concurren los presupuestos para estimar la excepción de declinatoria de jurisdicción planteada por la parte demandada. En efecto, es claro que el sujeto demandado presuntamente protegido por este privilegio jurisdiccional, operó a título meramente particular y no como representante de un Estado extranjero. La compraventa de los bienes a los que se refieren estas actuaciones recaen sobre unos vehículos destinados a su uso particular y de recreo y no a representación oficial de dicho Estado extranjero.

Cuarto.- En consecuencia, con lo anterior y conforme con el artículo 36.2 LEC, no procede que los tribunales españoles se abstengan de conocer del presente asunto, debiendo rechazar toda falta de jurisdicción planteada en virtud de las conclusiones irrefutables a las que nos lleva la prueba practicada. Por ello, alzándose la suspensión, deben continuar las actuaciones solicitadas por la parte actora, siguiendo todos los trámites inherentes al procedimiento solicitado, hasta la resolución sobre el fondo del asunto.

Vistos todos los preceptos citados y demás de general y correspondiente aplicación

PARTE DISPOSITIVA

Se desestima el incidente de declinatoria por excepción de inmunidad de jurisdicción planteado por la parte demandada, declarándose que en el presente asunto no concurre inmunidad de jurisdicción en la parte demandada por lo que procede la continuación de las actuaciones previo alzamiento de la suspensión acordada.

Notifíquese la presente resolución a las partes, advirtiéndoles que con arreglo al artículo 66.2 LEC, "Contra el auto por el que se rechace la falta de competencia internacional, de jurisdicción o de competencia objetiva, sólo cabrá recurso de reposición, sin perjuicio de alegar la falta de esos presupuestos procesales en la apelación contra la sentencia definitiva", que se habrá de interponer ante este Tribunal en el plazo de cinco días computados desde el día siguiente al de su notificación, de conformidad con el artículo 452 LEC el cual, no obstante, no suspenderá el curso de las actuaciones.

Así lo manda y firma S.S. Doy fe.

Firma del Magistrado-Juez

Firma del Letrado de la Administración de Justicia

========================================================================
