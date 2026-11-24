---
name: auto-ejecutoria-penal-fija-lo-debido-pensiones-civ-1869
description: "Auto en ejecutoria penal que fija lo debido por pensiones impagadas fijadas en proceso civil. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Auto en ejecutoria penal que fija lo debido por pensiones impagadas fijadas en proceso civil

> Formulario **CIV-1869** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

Auto en ejecutoria penal que determina y actualiza la cantidad debida por pensiones fijadas en proceso civil matrimonial desde la sentencia recaída en éste hasta la condena penal.

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Auto en ejecutoria penal que fija lo debido por pensiones impagadas fijadas en proceso civil» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Auto en ejecutoria penal que fija lo debido por pensiones impagadas fijadas en proceso civil” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:auto-ejecutoria-penal-fija-lo-debido-pensiones-civ-1869`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (14 veces)
- [ ] FECHA (10 veces)
- [ ] IMPORTE (10 veces)
- [ ] AÑO (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] Nº (2 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] IMPORTE EN CIFRA
- [ ] LOCALIDAD
- [ ] OTROS DATOS

## Normas que cita el formulario

- art. 798.2 LEC
- art. 7.1 LOPJ

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

SECCIÓN PENAL DEL TRIBUNAL DE INSTANCIA Nº [NÚMERO]

Ejecutoria nº [NÚMERO] /

Procedimiento Abreviado nº [Nº DE PROCEDIMIENTO] /

Partes:

Número de Identificación General:

AUTO

Ilmo. Sr./a Magistrado- Juez D./Dña. [NOMBRE Y APELLIDOS]

En la Villa de [LOCALIDAD], a [FECHA].

ANTECEDENTES DE HECHO

PRIMERO.- Por esta Sección Penal del Tribunal de Instancia se dictó sentencia firme de fecha [FECHA], cuyo fallo disponía que el condenado Don [NOMBRE Y APELLIDOS] debía indemnizar a la denunciante Doña [NOMBRE Y APELLIDOS] en la cantidad que se determinara en ejecución de sentencia, con descuento de la cifra de 5.000 euros (cinco mil euros) correspondientes a un pago por pensiones atrasadas anterior a la denuncia.

SEGUNDO.- Mediante escrito de [FECHA], la Procurador/a Sr./a. [NOMBRE Y APELLIDOS], representación procesal de Doña [NOMBRE Y APELLIDOS], solicitó la determinación de la cantidad en concepto de indemnización civil, presentando sus cálculos, de lo que se concedió traslado a las demás partes, de conformidad con el art. 798.2ª LECrim, evacuando alegaciones el Procurador/a Sr./a [NOMBRE Y APELLIDOS], mandatario del condenado Don [NOMBRE Y APELLIDOS] y el Ministerio Fiscal.

RAZONAMIENTOS JURÍDICOS

PRIMERO.- La sentencia firme de [FECHA] defirió para la vía de ejecución la fijación de la cantidad que como responsabilidad civil derivada de la comisión de un delito de abandono de familia por impago de pensión alimenticia de hijo menor tiene obligación de indemnizar el condenado Don [NOMBRE Y APELLIDOS] a su ex esposa Doña [NOMBRE Y APELLIDOS].

Mantiene el ejecutado que el periodo que debe tenerse en cuenta para el cálculo de lo que se adeuda por el obligado a prestar alimentos en la ejecutoria tiene que detenerse en la denuncia que dio origen al proceso penal, y no extenderse hasta la sentencia de condena.

Así como la ejecutada, el Ministerio Fiscal, considera que la denunciante no se vería repuesta en el perjuicio patrimonial sufrido como consecuencia de los hechos enjuiciados si sólo se le indemnizara por las pensiones impagadas hasta la denuncia, incurriendo en defecto de economía procesal la fijación del perjuicio sólo hasta dicho momento, habida cuenta que no se alega que las pensiones posteriormente devengadas se hayan abonado por el condenado, existiendo una identidad de hechos y continuidad del ilícito.

Debe partirse, de datos constantes en las actuaciones donde surge el título -sentencia-, y no otros:

1.- La denuncia de Doña [NOMBRE Y APELLIDOS] que inicia el procedimiento preliminar judicial es de [FECHA], y se refiere al impago de cinco anualidades de pensión de alimentos para el hijo común con el denunciado, desde un convenio regulador de [FECHA], homologado como medida definitiva derivada del divorcio de mutuo acuerdo de los padres por sentencia de [FECHA].
2.- El Fiscal: formuló acusación en escrito de casi un año más tarde, el [FECHA], manteniendo que el acusado no había pagado pensión alguna desde la fecha de la sentencia hasta entonces, sin que en la conclusión relativa a la responsabilidad civil mencionara más que ‘ [OTROS DATOS] el importe de las prestaciones económicas impagadas que se determinará en ejecución de sentencia’, sin otra precisión temporal.
3.- La sentencia declara probado que el condenado Don [NOMBRE Y APELLIDOS] no había pagado desde la sentencia de divorcio hasta entonces cantidad alguna de la pensión alimenticia de 350 euros mensuales, revisables anualmente conforme al IPC, con excepción de un pago total de 5.000 euros por pensiones atrasadas efectuado antes de la denuncia.

SEGUNDO.- El asunto no tiene una solución unívoca en abstracto, puesto que el art. 227.3 CP, al establecer que la reparación del daño incluye siempre el pago de las cuantías adeudadas, ello referido a la responsabilidad civil dimanante de un delito que puede consistir en el impago de todas las sucesivas obligaciones periódicas de una prestación de alimentos instaurada por resolución judicial, permite variadas formulaciones apriorísticas, partiendo de un impago inaugural de la pensión matrimonial o parental, y de que el impago persista y se mantenga cuando se enjuicia.

En primer lugar, ha de entenderse que el crédito ejecutivo del perjudicado en el proceso penal sólo abarca la responsabilidad civil que tiene su origen en la conducta típica que se sanciona, de modo que el apartado 3 del dicho art. 227 CP es una norma de concreción absolutamente necesaria para un delito de simple omisión, y que no existía para la inicial versión del tipo de injusto (art. 487 bis) CP 1973). Así, cualquier impago anterior o posterior al comportamiento conminado en el proceso penal, al ser impune en el mismo, habrá de reclamarse en la pertinente vía civil. Por ejemplo, resulta claro que en el asunto hay pensiones probablemente impagadas antes de la sentencia de divorcio, en un espacio de casi cinco años desde [FECHA] hasta [FECHA], que, al no venir impuestas por convenio judicialmente aprobado, no cabe sean responsabilidad civil por delito.

¿Qué ocurre, pues, con las pensiones impagadas posteriormente a la denuncia? En realidad, por el contrario de lo que asevera el ejecutado, se consignan como deudas correspondientes a la omisión típica por la que se condena un determinado periodo, porque consta en los hechos probados ser las pensiones desde la fecha de la sentencia de divorcio hasta la fecha de la sentencia penal.

Puesto que el delito que nos ocupa es de permanencia en el tiempo, nada impide que los adeudos de concretas mensualidades impagadas que se expresen en la denuncia de la víctima se vean complementados, como elementos objetivos del tipo, con los que se generen hasta el momento de la concreta formulación de acusación en trámite de conclusiones definitivas. En caso contrario, al forzarse a la parte perjudicada a un rosario de procesos judiciales derivados de la misma causa, se contrariaría la evidente finalidad legislativa de colocar la tutela de un determinado derecho de crédito ejecutivo como un delito omisivo que no exige un resultado material, y existiendo éste, colocar su secuela civil en la ejecución penal, vulnerándose en dicho caso la efectividad de la tutela judicial de los derechos e intereses legítimos (art. 24.1 CE y art. 7.1 LOPJ). No cabe hablar en tales supuestos, como el que nos ocupa, de una indefensión del acusado deudor por motivo de la indeterminación final de su deuda, ya que es claro que, tanto la acusación como la pretensión civil se refieren en todo caso a unos hechos con idéntica configuración causal, respecto de las que no hay motivo que impida la defensa referida al periodo impagado de devengos hasta la liquidación, ni como comprendido dentro de los términos del art. 227 CP, motivo que impida dejar dicha liquidación para ejecución de sentencia, de conformidad con el art. 115 CP.

En conclusión, no es cierto que la denuncia marque el momento hasta el que puede determinarse la deuda civil exigible en el proceso por delito de impago de pensiones, en que el condenado es reo de una pena y a la vez deudor pecuniario, y nada excluye legalmente que pueda, secundando el fin del art. 227.3 CP, determinarse hasta la sentencia firme de condena, o incluso petición ejecutiva posterior a la misma, únicamente requiriéndose una pretensión civil en tal sentido y un fallo congruente.

TERCERO.- Así las cosas, corresponde acceder a la determinación indemnizatoria solicitada:

Año [AÑO]: Desde la sentencia civil: meses, a razón de 350 euros:

Año [AÑO]: Actualización al IPC de [IMPORTE], [IMPORTE] euros; meses, a razón de 350 euros + [Nº] meses hasta fin de año, a razón de [IMPORTE] euros:

Año [AÑO]: Actualización al IPC de [IMPORTE], [IMPORTE] euros; meses, a razón de [IMPORTE] euros + [Nº] meses hasta la sentencia penal, a razón de [IMPORTE] euros:

Total [IMPORTE] - 5.000 euros = [IMPORTE] euros

En su virtud,

PARTE DISPOSITIVA

Con estimación de la solicitud de Doña [NOMBRE Y APELLIDOS], representada por el Procurador/a de los Tribunales D./Dña. [NOMBRE Y APELLIDOS], se determina la indemnización que adeuda el condenado Don [NOMBRE Y APELLIDOS] a la solicitante en el presente procedimiento de ejecutoria nº [Nº DE PROCEDIMIENTO] /, dimanante de la causa nº [NÚMERO] /, en la cantidad de [IMPORTE] euros ([IMPORTE EN CIFRA] €), en concepto de pensiones impagadas hasta el dictado de la sentencia de condena.

Así lo acuerdo, mando y firmo:

Firma del Juez/a

Este auto es susceptible de recurso de apelación para ante la Audiencia Provincial (art. 798.2ª `in fine' LECrim.).

========================================================================
