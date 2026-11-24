---
name: contrato-ejecucion-obra-civ-0797
description: "Contrato de ejecución de obra. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de ejecución de obra

> Formulario **CIV-0797** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de ejecución de obra» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de ejecución de obra” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:contrato-ejecucion-obra-civ-0797`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (8 veces)
- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] IMPORTE (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] DNI/NIE (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] FECHA
- [ ] FOLIO
- [ ] LIBRO
- [ ] LUGAR
- [ ] MES
- [ ] Nº DE FINCA
- [ ] Nº REGISTRAL
- [ ] PERIODICIDAD
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

Reunidos

De una parte:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con DNI núm. [DNI/NIE]

De otra:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con DNI núm. [DNI/NIE]

Intervienen

[ELEGIR UNA OPCIÓN: En representación / Nombre propio]

Exponen

Primero.– Que EL COMITENTE es propietario en régimen de plena propiedad y dominio de la finca sita en el término municipal de [LOCALIDAD], con una superficie de [Nº] metros cuadrados, lindando a la izquierda con la finca propiedad de D./Dña. [NOMBRE Y APELLIDOS], a la derecha con la finca propiedad de D./Dña. [NOMBRE Y APELLIDOS], e inscrita en el Registro de la Propiedad de [LOCALIDAD] en el Tomo [TOMO], Libro [LIBRO], Folio [FOLIO], Finca [Nº DE FINCA], inscripción núm. [Nº REGISTRAL]

Segundo.– Que en tal terreno desea construir una vivienda cuyas características técnicas y materiales se adjuntan al presente escrito, así como los planos de planta y alzado para cuya realización ha recurrido a los servicios del CONTRATISTA.

Tercera.– Como quiera que ambas partes se encuentran interesadas en ello, ambas partes de común acuerdo llevan a efecto el presente contrato con arreglo a las siguientes:

Cláusulas

Objeto.–

Que EL CONTRATISTA se compromete a la realización de las obras descritas en el presupuesto de fecha [FECHA] y conforme a las calidades indicadas, presupuesto que se une a este contrato como anexo I.

Precio.–

El precio, conforme al presupuesto aceptado, es de [IMPORTE] euros, más el IVA vigente en el momento de pago.

Dicha cantidad constituye un precio cerrado, corriendo EL CONTRATISTA con todos los posibles incrementos que se originen, e incluye las tasas por certificaciones de obra y todos cuantos documentos sean precisos para llevar a cabo la obra que se solicita y se hará efectivo de la siguiente forma:

- % en el momento de la firma del presente contrato.
- % contra la recepción de las correspondientes certificaciones de obra.
- % a la finalización de la obra.

Asimismo, y como contrapartida, el constructor deberá acreditar con una periodicidad de [PERIODICIDAD] las certificaciones de obras que vaya realizando.

Plazo.–

El plazo para la realización de la obra se pacta en [Nº] días, contabilizados a partir del momento en que se concedan las licencias municipales oportunas.

Si llegado dicho término la obra no se hubiese terminado, salvo causas de fuerza mayor no imputables al CONTRATISTA, se establece una cláusula penal consistente en una indemnización de [IMPORTE] euros ( €) por día, descontándose de esta forma del precio total que quede por pagar por parte de D./Dña. [NOMBRE Y APELLIDOS]

Un retraso superior a [Nº] meses podrá ser considerado por EL COMITENTE como incumplimiento definitivo a los efectos de la resolución del contrato, con la consiguiente indemnización adicional de daños y perjuicios.

No se considerará fuerza mayor todos los fenómenos atmosféricos que acaezcan durante la realización de la obra, sin embargo son casos de fuerza mayor: los incendios causados por la electricidad atmosférica; los fenómenos naturales de efectos catastróficos, como maremotos, terremotos, inundaciones u otros semejantes; y los destrozos ocasionados por robos tumultuosos o alteraciones graves del orden público. En estos supuestos, y siempre que no exista actuación imprudente por parte del CONTRATISTA, éste tendrá derecho a una indemnización por los daños y perjuicios que se le hubieren producido.

Aportación de materiales propios.–

EL COMITENTE podrá aportar elementos o materiales cuya adquisición pueda haber gestionado directamente, con la condición de advertir previamente al CONTRATISTA, con una anticipación de [Nº] días/meses sobre la fecha prevista en el calendario de trabajo para la introducción o colocación de dichos materiales en la obra.

En ningún caso esta aportación de materiales por EL COMITENTE podrá superar el 20 % del presupuesto y conllevará una reducción proporcional del presupuesto. La valoración de las posibles aportaciones por EL COMITENTE se realizará por la Dirección Facultativa

Obligaciones del contratista.–

Seguro

EL CONTRATISTA se compromete a correr con todos los gastos derivados de la contratación de los seguros multirriesgos, debiendo no obstante tener como valor inicial asegurado al menos el de [IMPORTE] euros ( €) durante los primeros [Nº] meses, y siendo suficiente el valor de [IMPORTE] euros ( €) el resto del tiempo que reste por cumplir.

Sujeción a proyecto y presupuesto

Las obras se ejecutarán con estricta sujeción al contenido del proyecto y al presupuesto estipulado que sirve de base al contrato y conforme a las instrucciones que en interpretación técnica de éste diere al contratista el director técnico de la obra.

Licencias y permisos

EL CONTRATISTA se compromete a solicitar cuantas autorizaciones o licencias sean precisas para la construcción de la vivienda unifamiliar que queda descrita en los anexos de este contrato, obligándose a firmar cuantos documentos se requieran por parte de los Organismos a los que se dirija.

Vicios y defectos constructivos

No obstante, aún recibida definitivamente la obra y transcurrido el término de garantía, EL CONTRATISTA responderá de los vicios ocultos de la construcción si los mismos aparecen en el plazo de diez años contados desde que concluyó la construcción. En igual responsabilidad incurrirá el arquitecto o director técnico de la obra.

En el supuesto de incidencias surgidas en la ejecución del contrato de obras que puedan determinar, si no son resueltas, la imposibilidad de continuar la ejecución, podrá modificarse el presente contrato, a voluntad del contratista, y mediante la propuesta del director técnico de la obra.

Plazo de garantía.–

En relación con lo anterior, y sin perjuicio de la obligación del CONTRATISTA de realizar la obra en las debidas condiciones, de lo que debe responder en los términos legalmente establecidos, se pacta una garantía adicional de [Nº] meses durante los cuales atenderá cualquier reparación sin cargo alguno por sustitución de piezas defectuosas, y mano de obra y desplazamientos, siempre y cuando las averías no se deban a manipulaciones ajenas a su servicio técnico, inadecuado funcionamiento o causas imprevisibles como fallos en el suministro de energía eléctrica, incendios, inundaciones, etc.

Retención de cantidades.–

EL COMITENTE retendrá el % del precio final de la obra hasta transcurrido el plazo de [Nº] días/meses desde la recepción definitiva como garantía por posibles vicios ocultos o demora en la entrega de la obra.

Resolución del contrato.–

En caso de resolución del presente contrato, habrá lugar a una comprobación y liquidación de las obras realizadas con arreglo al proyecto, fijando los saldos pertinentes a favor o en contra del contratista.

Jurisdicción competente y ley aplicable.–

Para cuantas cuestiones o divergencias pudieran suscitarse en relación con el presente contrato, la competencia de los Tribunales que deban conocer del asunto se determinará de conformidad con los criterios de competencia objetiva, funcional y territorial legalmente aplicables.

El presente contrato tiene exclusivamente carácter civil y se regirá por sus propias cláusulas, y en lo en ellas no dispuesto, por lo previsto en el Código Civil y, demás leyes especiales.

Sumisión a tribunales.–

[ELEGIR UNA OPCIÓN: Sin cláusula penal / Con cláusula penal]

Sumisión a arbitraje.–

[ELEGIR UNA OPCIÓN: Sin cláusula penal / Con cláusula penal]

Notificaciones.–

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Generalidades.–

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este Contrato.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [Nº] folios del presente CONTRATO DE OBRA, extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

El/La Contratista	El/La Comitente

Fdo. D./Dña. [NOMBRE Y APELLIDOS]: Fdo. D./Dña. [NOMBRE Y APELLIDOS]:

========================================================================
