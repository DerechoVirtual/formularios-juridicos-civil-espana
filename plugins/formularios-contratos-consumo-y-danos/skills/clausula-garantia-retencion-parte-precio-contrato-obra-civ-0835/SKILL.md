---
name: clausula-garantia-retencion-parte-precio-contrato-obra-civ-0835
description: "Cláusula de garantía y retención de parte del precio en un contrato de obra de vivienda. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Cláusula de garantía y retención de parte del precio en un contrato de obra de vivienda

> Formulario **CIV-0835** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Contrato de cláusula de garantía y retención en un contrato de obra de vivienda unifamiliar, de determinada cantidad al constructor hasta la recepción definitiva de la obra como garantía por posibles vicios ocultos o demora en la entrega de la obra.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Cláusula de garantía y retención de parte del precio en un contrato de obra de vivienda» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Cláusula de garantía y retención de parte del precio en un contrato de obra de vivienda” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:clausula-garantia-retencion-parte-precio-contrato-obra-civ-0835`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (6 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] Nº (5 veces)
- [ ] IMPORTE EN CIFRA (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] NÚMERO (4 veces)
- [ ] CALLE (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] FOLIO
- [ ] LIBRO
- [ ] LUGAR
- [ ] MES
- [ ] MUNICIPIO
- [ ] Nº DE FINCA
- [ ] Nº REGISTRAL
- [ ] PERIODICIDAD
- [ ] PROFESIÓN
- [ ] TOMO

## Normas que cita el formulario

- No cita artículos concretos; Claude localizará las normas aplicables con Jurisprudenciator si el documento las necesita.

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

En [LUGAR], a [DÍA] de [MES] de [AÑO].

REUNIDOS

DE UNA PARTE:

D. [NOMBRE Y APELLIDOS], mayor de edad, estado civil [ESTADO CIVIL], profesión [PROFESIÓN] con domicilio en [LOCALIDAD], calle [CALLE] nº [NÚMERO] y con N.I.F. nº [NÚMERO]

Y DE OTRA:

D. [NOMBRE Y APELLIDOS], mayor de edad, estado civil [ESTADO CIVIL], de profesión constructor, con domicilio en [LOCALIDAD], calle [CALLE] nº [NÚMERO], y con N.I.F. nº [NÚMERO]

Intervienen ambos en su propio nombre y derecho, reconociéndose la mutua capacidad legal necesaria para otorgar el presente contrato, de acuerdo con las siguientes:

ESTIPULACIONES

PRIMERA: Que D. es propietario de la finca sita en el término municipal de [MUNICIPIO], con una superficie de [Nº] metros cuadrados, lindando a la izquierda con la finca propiedad de D [NOMBRE Y APELLIDOS], a la derecha con la finca propiedad de D [NOMBRE Y APELLIDOS], e inscrito en el Registro de la Propiedad de [LOCALIDAD] al Tomo [TOMO], Libro [LIBRO], Folio [FOLIO], Finca [Nº DE FINCA] e inscripción nº [Nº REGISTRAL]

SEGUNDA: Que en tal terreno desea construir una vivienda unifamiliar cuyas características técnicas y materiales se adjuntan al presente escrito, así como los planos de planta y alzada, para lo cual ha recurrido a los servicios de D. [NOMBRE Y APELLIDOS] como profesional en estos temas.

TERCERA: Que D. acepta tal construcción y obras anexas a la misma, en un precio total de [IMPORTE] euros ([IMPORTE EN CIFRA] €), precio que se considera desde este momento como cerrado, corriendo el contratista con todos los posibles incrementos que origine dicha obra, así como los materiales o la mano de obra utilizada. Que D. ha aceptado previamente el presupuesto presentado por aquél y cuya copia se anexiona al presente contrato.

CUARTA: Que la obra se realizará con los materiales aceptados comúnmente, o en su defecto, otros de calidades semejantes.

QUINTA: El precio total pactado es de [IMPORTE] euros ([IMPORTE EN CIFRA] €), cantidad que incluye las tasas por certificaciones de obra y todos cuantos documentos sean precisos para llevar a cabo la obra que se solicita. Dicha cantidad se hará efectiva al constructor en el momento de la recepción provisional de la misma, excepto la cantidad de [IMPORTE] euros ([IMPORTE EN CIFRA] €), que serán retenidas por D. hasta transcurrido el plazo de [Nº] días desde la recepción definitiva como garantía por posibles vicios ocultos o demora en la entrega de la obra.

SEXTA: Asímismo, y como contrapartida, el constructor deberá acreditar con una periodicidad de [PERIODICIDAD] las certificaciones de obras que vaya realizando.

SÉPTIMA: El constructor se compromete a solicitar cuantas autorizaciones o licencias sean precisas para la construcción de la vivienda unifamiliar que queda descrita en los anexos de este contrato, obligándose a firmar cuantos documentos se requieran por parte de los Organismos a los que se dirija.

OCTAVA: El plazo para la realización de la obra se pacta en [Nº] días, contabilizados a partir del momento en que se concedan las licencias municipales oportunas. Si llegado dicho término la obra no se hubiese terminado, salvo causas de fuerza mayor no imputables al contratista, se establece una cláusula penal consistente en una indemnización de [IMPORTE] euros ([IMPORTE EN CIFRA] €) como días de retraso conlleve la ultimación de la misma, descontándose de esta forma del precio total que quede por pagar por parte de D. [NOMBRE Y APELLIDOS]

NOVENA: No se considerará fuerza mayor todos los fenómenos atmosféricos que acaezcan durante la realización de la obra, sin embargo son casos de fuerza mayor: los incendios causados por la electricidad atmosférica; los fenómenos naturales de efectos catastróficos, como maremotos, terremotos, inundaciones u otros semejantes; y los destrozos ocasionados por robos tumultuosos o alteraciones graves del orden público. En estos supuestos, y siempre que no exista actuación imprudente por parte del contratista, éste tendrá derecho a una indemnización por los daños y perjuicios que se le hubieren producido.

DÉCIMA: El contratista se compromete a correr con todos los gastos derivados de la contratación de los seguros multiriesgos, debiéndo no osbstante tener como valor inicial asegurado al menos el de [IMPORTE] durante los primeros [Nº] meses, y siendo suficiente el valor de [IMPORTE] el resto del tiempo que reste por cumplir.

UNDÉCIMA: Las obras se ejecutarán con estricta sujeción al contenido del proyecto y al presupuesto estipulado que sirve de base al contrato y conforme a las instrucciones que en interpretación técnica de éste diere al contratista el director técnico de la obra.

DUODÉCIMA: En el supuesto de incidencias surgidas en la ejecución del contrato de obras que puedan determinar, si no son resueltas, la imposibilidad de continuar la ejecución, podrá modificarse el presente contrato, a voluntad del contratista, y mediante la propuesta del director técnico de la obra.

DECIMOTERCERA: Como plazo de garantía se establece el de [Nº] meses entre la recepción provisional de las obras y la definitiva.

DECIMOCUARTA: No obstante, aún recibida definitivamente la obra y transcurrido el término de garantía, el constructor responderá de los vicios ocultos de la construcción si los mismos aparecen en el plazo de diez años contados desde que concluyó la construcción. En igual responsabilidad incurrirá el arquitecto o director técnico de la obra.

DECIMOQUINTA: En caso de resolución del presente contrato, habrá lugar a una comprobación y liquidación de las obras realizadas con arreglo al poryecto, fijando los saldos pertinentes a favor o en contra del contratista.

DECIMOSEXTA: Ambas partes, con renuncia de su fuero propio si lo tuvieren, se someten expresamente a los Tribunales de [LOCALIDAD] para la interpretación o cualquier cuestión litigiosa que derive de este contrato.

Y leído el presente documento, ambas partes lo firman en prueba de su conformidad, a un solo efecto y por duplicado, en el lugar y fecha ‘ut supra’.

========================================================================
