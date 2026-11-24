---
name: contestacion-demanda-alegando-nulidad-compraventa-civ-0855
description: "Contestación a la demanda alegando nulidad de la compraventa de vivienda por dolo. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contestación a la demanda alegando nulidad de la compraventa de vivienda por dolo

> Formulario **CIV-0855** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Contestación a la demanda, dirigida al Tribunal de Instancia, alegando nulidad del contrato de compraventa de vivienda por consentimiento viciado por dolo.

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contestación a la demanda alegando nulidad de la compraventa de vivienda por dolo» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contestación a la demanda alegando nulidad de la compraventa de vivienda por dolo” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:contestacion-demanda-alegando-nulidad-compraventa-civ-0855`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] FECHA (5 veces)
- [ ] IMPORTE (3 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] CREENCIA ERRÓNEA
- [ ] ENGAÑO PADECIDO
- [ ] HECHO QUE SE NIEGA
- [ ] IMPORTE EN CIFRA
- [ ] LUGAR
- [ ] NÚMERO
- [ ] PARENTESCO
- [ ] SEDE
- [ ] ÓRGANO O PERSONA

## Normas que cita el formulario

- art. 23 LEC
- art. 31 LEC
- art. 1.261 CC
- art. 1.265 CC
- art. 1.269 CC
- art. 394 LEC

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

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en nombre y representación de [NOMBRE DEL REPRESENTADO/A], según acredito mediante escritura de poder inscrito en el Registro Electrónico de Apoderamientos Judiciales, a cuya justificación aporto certificación de dicho Registro como documento nº [Nº DE DOCUMENTO], dirigido por el Letrado abajo firmante D./Dña. [NOMBRE Y APELLIDOS], con despacho profesional en [LOCALIDAD], ante el Tribunal comparezco y como mejor proceda en Derecho DIGO:

Que mediante el presente escrito y dentro del término conferido, paso a contestar la demanda formulada de adverso, oponiéndome a la misma en base a los siguientes:

HECHOS

PRIMERO.- Cierto que en fecha [FECHA] mi representado y el demandante suscribieron contrato privado de compraventa, en virtud del cual, éste adquiría la propiedad de la vivienda sita en la calle

Pero oculta el demandante que la causa que determinó en mi representado la decisión de firmar el contrato no fue producto de un libre concurso de voluntades obtenido con la consiguiente buena fe que debe presidir toda contratación, sino que en virtud de engaños que se prolongan durante varios meses se logró obtener el consentimiento de mi patrocinado.

Mi mandante se encuentra en precario estado físico e intelectual; esta circunstancia adquiere más relevancia si cabe en este caso, por su escasa instrucción, máxime en una persona de avanzada edad y residente en ámbito rural. Se acompaña como DOCUMENTO NÚM. dictamen pericial médico forense acerca de la disminución de capacidad de D./Dña. [NOMBRE Y APELLIDOS] al momento de concertar el contrato, estando limitada su capacidad intelectiva y volitiva, lo que favoreció sin duda las maquinaciones engañosas de la demandante.

Esta parte desea dejar constancia de los siguientes hechos que determinaron a mi mandante, por engaño, a prestar su consentimiento:

Con fecha [FECHA], el demandante le remite una carta en que manifiesta que el inmueble va a ser expropiado y se adjunta documentación, al parecer pública, en la que consta este extremo. Naturalmente dicha expropiación nunca tuvo lugar. Se acompañan como DOCUMENTOS NÚMEROS

Con fecha [FECHA] el demandante le escribe nuevamente y le señala que el agua y la luz va a ser cortada por razones de necesidad pública y dos días después recibe asimismo un escrito con presunta firma del Alcalde de la villa de [LOCALIDAD] en el que se le comunica esta circunstancia. Se acompañan como DOCUMENTOS NÚMEROS

En fecha [FECHA], mi principal fue llamado con urgencia por [NOMBRE Y APELLIDOS] y firmó el contrato de compraventa, convencido por engaño de que [ENGAÑO PADECIDO] Se acompaña como DOCUMENTO NÚMERO [Nº DE DOCUMENTO], copia del contrato de fecha

Debe significarse igualmente que entre los litigantes existen lazos de consanguinidad ya que mi mandante, quien actualmente cuenta con 89 años de edad, es [PARENTESCO] de [NOMBRE Y APELLIDOS] Adjunto como DOCUMENTO NÚM. certificación literal de nacimiento.

Pues bien, mi patrocinado, de edad avanzada y confiado en lo que se le manifestaba y en el hecho de que el demandante es un familiar cercano, prestó su asentimiento. En consecuencia, debe concluirse que el consentimiento prestado por [NOMBRE Y APELLIDOS] se halla viciado por dolo determinante de su nulidad.

SEGUNDO.- Cierto que el precio de la compraventa quedó fijado en la cantidad de [IMPORTE] euros ([IMPORTE EN CIFRA] €). Pero debe acogerse el hecho de que figurando en el contrato un valor de los inmuebles objeto de la venta de [IMPORTE] euros, según el dictamen pericial que se aporta como DOCUMENTO NÚM. [NÚMERO], su valor real es de cerca de [IMPORTE] de euros; diferencia de precio entre el consignado y el real, que, aunque no decisivo para acordar la nulidad del contrato, sí ha de ser tenido en cuenta en unión del resto de los hechos.

TERCERO.- No es cierto el correlativo de la demanda en el sentido de que [HECHO QUE SE NIEGA], como se desprende de los documentos números [Nº DE DOCUMENTO] que se adjuntan.

En consecuencia, mi mandante prestó su consentimiento a dicho contrato en la creencia de que [CREENCIA ERRÓNEA], sin saber que le estaban engañando.

FUNDAMENTOS DE DERECHO

I, II.-

Conforme esta parte con la competencia y el tipo de procedimiento señalados por el actor en el correlativo de la demanda.

III, IV, V.-

De conformidad con los expuestos de contrario.

VI.- POSTULACIÓN Y DEFENSA

La parte esta representada por el Procurador/a [NOMBRE Y APELLIDOS], legalmente habilitado según el art. 23 LEC y defendida por el Letrado que consta en el encabezamiento, art. 31 LEC.

VII.- NULIDAD DEL CONTRATO DE COMPRAVENTA

El art. 1.261 CCiv dispone que "No hay contrato sino cuando concurren los requisitos siguientes: 1.º Consentimiento de los contratantes. ()"

La conducta de la otra parte, tiene evidente transcendencia en el vicio del consentimiento producido, por la maquinación creada para llamar a engaño a mi mandante.

En línea de lo anterior, el art. 1.265 CCiv dice que "Será nulo el consentimiento prestado por error, violencia, intimidación o dolo."

Definido en el art. 1.269 CCiv el dolo como vicio del consentimiento contractual, comprensivo no solo de la insidia directa o inductora de la conducta errónea del otro contratante sino también la reticencia dolosa del que calla o no advierte a la otra parte en contra del deber de informar que exige la buena fe, tal concepto legal exige la concurrencia de dos requisitos; el empleo de maquinaciones engañosas, conducta insidiosa del agente que puede consistir tanto en una actuación positiva como en una abstención u omisión, y la inducción que tal comportamiento ejerce sobre la voluntad de la otra parte para determinarle a realizar el negocio que de otra forma no hubiera realizado, y en este sentido se pronuncia unánime la jurisprudencia del TS cuya sentencia de 12 de junio de 2003, rec. 3172/1997, afirma que los requisitos comúnmente exigidos por la doctrina científica son los siguientes: a) una conducta insidiosa, intencionada o dirigida a provocar la declaración negocial, utilizando para ello las palabras o maquinaciones adecuadas; b) que la voluntad del declarante quede viciada por hacerse emitido sin la natural libertad y conocimiento a causa del engaño, coacción u otra insidiosa influencia; c) que dicha conducta sea determinante de la declaración; d) que sea grave si se trata de anular el contrato; y e) que no haya sido causado por un tercero, ni empleado por las dos partes contratantes.

Todas estas circunstancias concurren en este supuesto donde el dolo fue grave, causa del contrato y directo por lo que debe concluirse que el consentimiento prestado por [NOMBRE Y APELLIDOS] se halla viciado por dolo determinante de su nulidad.

VIII.- COSTAS

Las costas deberán serle impuestas, de conformidad con el art. 394 LEC, a la parte actora, de ser desestimada su demanda.

Por lo expuesto,

SUPLICO AL TRIBUNAL.

Que tenga por presentado este escrito con sus documentos y copias y escritura de poder, se sirva admitirlo y por comparecido al Procurador/a [NOMBRE Y APELLIDOS], en representación de [NOMBRE DEL REPRESENTADO/A], entendiéndose conmigo las sucesivas diligencias; por opuesto y contestada la demanda de juicio declarativo ordinario formulada por [ÓRGANO O PERSONA], y, seguido el juicio por todos sus trámites, se dicte sentencia absolviendo a mi principal de todos los pedimentos deducidos en la demanda, con expresa imposición de costas a la parte demandante.

Es justicia debe hacerse en [LUGAR], a [FECHA].

Firma del Abogado	Firma del Procurador/a

========================================================================
