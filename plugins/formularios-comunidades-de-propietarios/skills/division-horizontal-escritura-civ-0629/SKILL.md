---
name: division-horizontal-escritura-civ-0629
description: "División Horizontal (escritura). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# División Horizontal (escritura)

> Formulario **CIV-0629** del plugin **Comunidades de propietarios** (`formularios-comunidades-de-propietarios`) · Civil › Propiedad horizontal · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «División Horizontal (escritura)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “División Horizontal (escritura)” para mi caso». También puedes invocarla directamente con `/formularios-comunidades-de-propietarios:division-horizontal-escritura-civ-0629`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-comunidades-de-propietarios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Comunidades de propietarios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] DESCRIPCIÓN DEL BIEN (12 veces)
- [ ] NÚMERO (11 veces)
- [ ] LINDEROS (9 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] Nº (4 veces)
- [ ] PORCENTAJE (3 veces)
- [ ] SUPERFICIE (3 veces)
- [ ] FECHA (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] CALLE
- [ ] CLASE
- [ ] COLEGIO
- [ ] MES
- [ ] NORMATIVA APLICABLE
- [ ] Nº DE PROTOCOLO
- [ ] OTROS DATOS
- [ ] SERIE
- [ ] TÍTULO DE ADQUISICIÓN

## Normas que cita el formulario

- art. 6 Ley Orgánica 3/2018

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

NÚMERO PROTOCOLO [Nº DE PROTOCOLO]

En [LOCALIDAD], mi residencia, a [FECHA]

Ante mí, Notario del Ilustre Colegio de [COLEGIO]

Intervienen

En su propio nombre y derecho. Me aseguro de su identidad por su reseñado documento y tienen a mi juicio, la capacidad legal necesaria, para formalizar la presente escritura de división horizontal.

Exponen

Que son propietarios del edificio sito en el nº [NÚMERO] de la calle [CALLE] de esta ciudad, que ocupa una superficie de [Nº] metros cuadrados, está distribuido en [Nº] plantas, inscrita en el Registro de la Propiedad nº [NÚMERO], de [LOCALIDAD], como consecuencia de haberla adquirido en virtud de [TÍTULO DE ADQUISICIÓN], con fecha [FECHA] de [MES] de

Consta de los siguientes servicios e instalaciones:

Sin cargas y con un valor catastral de [IMPORTE] de euros (euros)

Que siendo su voluntad proceder a la división de dicho inmueble en viviendas, de acuerdo con lo que dispone la Ley de Propiedad Horizontal, con el objeto de la oportuna inscripción en el Registro de la Propiedad, en los siguientes términos:

I.– Se inscribirán como fincas independientes en distinto folio registral, practicando la correspondiente segregación, sin perjuicio de la porción que a cada una corresponda en los elementos comunes, las siguientes:

[OPCIONAL — incluir si procede]

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

Elemento nº [NÚMERO]: Piso [DESCRIPCIÓN DEL BIEN] superficie [SUPERFICIE] descripción [DESCRIPCIÓN DEL BIEN] con los siguientes linderos Norte: [LINDEROS], Sur: [LINDEROS], Este: [LINDEROS], y Oeste:

[OPCIONAL — incluir si procede]

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

Elemento nº [NÚMERO]: Local [DESCRIPCIÓN DEL BIEN] superficie [SUPERFICIE] descripción [DESCRIPCIÓN DEL BIEN] con los siguientes linderos Norte: [LINDEROS], Sur: [LINDEROS], Este: [LINDEROS], y Oeste:

[OPCIONAL — incluir si procede]

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

Elemento nº [NÚMERO]: Trastero [DESCRIPCIÓN DEL BIEN] superficie [SUPERFICIE] descripción [DESCRIPCIÓN DEL BIEN] con los siguientes linderos Norte: [LINDEROS], Sur: [LINDEROS], Este: [LINDEROS], y Oeste:

II.– A los efectos prevenidos en el artículo 5 Ley de Propiedad Horizontal, se fija como cuota de participación para cada uno de los apartamentos mencionados, atendiendo a su superficie útil, en relación con el valor total del inmueble, emplazamiento interior o exterior, situación y uso que se puede presumir va a efectuarse de los servicios y elementos comunes, la siguiente:

[OPCIONAL — incluir si procede]

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

Elemento nº [NÚMERO]: Piso [DESCRIPCIÓN DEL BIEN] participación con [PORCENTAJE] centésimas de participación en los elementos comunes.

[OPCIONAL — incluir si procede]

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

Elemento nº [NÚMERO]: Local [DESCRIPCIÓN DEL BIEN] participación con [PORCENTAJE] centésimas de participación en los elementos comunes.

[OPCIONAL — incluir si procede]

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

Elemento nº [NÚMERO]: Trastero [DESCRIPCIÓN DEL BIEN] participación con [PORCENTAJE] centésimas de participación en los elementos comunes.

Total:100 centésimas

III.– Se adjudicarán los distintos apartamentos en la forma siguiente

[OPCIONAL — incluir si procede]

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

Elemento nº [NÚMERO]: Piso [DESCRIPCIÓN DEL BIEN] a Don /Doña [NOMBRE Y APELLIDOS]

[OPCIONAL — incluir si procede]

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

Elemento nº [NÚMERO]: Local [DESCRIPCIÓN DEL BIEN] a Don /Doña [NOMBRE Y APELLIDOS]

[OPCIONAL — incluir si procede]

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

Elemento nº [NÚMERO]: Trastero [DESCRIPCIÓN DEL BIEN] a Don /Doña [NOMBRE Y APELLIDOS]

IV.– A efectos fiscales valoran la división horizontal en este acto efectuada en la suma de [IMPORTE].

[OPCIONAL — incluir si procede]

V.- En virtud de la facultad otorgada por el artículo 5 la Ley de Propiedad Horizontal, se

transcriben a continuación una serie de reglas de constitución y disposiciones no prohibidas por la mencionada Ley en orden al uso o destino del edificio, sus diferentes pisos o locales, instalaciones y servicios, gastos, administración y gobierno, seguros, conservación y reparaciones, formando los siguientes

ESTATUTOS

Esta propiedad horizontal se regirá por [NORMATIVA APLICABLE].

1.– División, agrupación y segregación:

Todas las fincas resultantes de esta división horizontal, podrán, sin consentimiento de la Junta de Propietarios, ser divididas, segregadas, agrupadas, agregadas con otras colindantes del mismo o distinto inmueble, vertical u horizontalmente (modificando las cuotas de participación de los departamentos afectados por suma o distribución de sus cuotas), manteniendo, en su caso, la seguridad de los elementos comunes de ambas fincas.

También podrán ser desvinculados los anejos de sus elementos privativos.

2.– Régimen específico para los locales

Los propietarios de los locales comerciales (), podrán establecer en los mismos todo tipo de negocios, previas las correspondientes licencias municipales, siempre que no sean inmorales o peligrosos, según lo previsto por las Ordenanzas Municipales.

Estos departamentos no contribuirán a los gastos de limpieza, alumbrado y conservación del portal, ascensor, y escalera por no utilizarlos.

También podrán colocar rótulos, incluso luminosos u opacos, que no sobrepasen la altura de la planta baja, sin otra limitación que la que fijen las Ordenanzas Municipales.

Realizar todo tipo y clase de obras, y en todo tiempo, en el interior de dichos locales, con las correspondientes Licencias Municipales.

Modificar la fachada en la parte del local, efectuando cerramientos, colocando elementos como recubrimiento de pilares, Caja nocturna, rótulos luminosos o no, horizontales en la parte correspondiente a los locales de planta baja, y todo ello siempre que no contravengan las Ordenanzas Municipales.

Podrán ocupar, sin consentimiento de la comunidad de propietarios ni contraprestación de clase alguna, aquellos elementos comunes del edificio que no sean de uso privativo, para la instalación de instalaciones eléctricas, refrigeración, calefacción, aire acondicionado, y ventilación (incluso chimeneas o tubos para la extracción de humos y ventilación) que desde el local lleguen a los elementos de cierre de la finca por arriba, con la única limitación de que su instalación deberá ser realizada con arreglo a las Ordenanzas, y en lo que respecta a las paredes donde tienen que apoyarse, lo será de forma que no afecten a ventanas ni a las fachadas, y con la autorización y bajo la supervisión de los Arquitectos Directores de la obra y los de la Entidad Promotora, en su caso.

Los propietarios de los citados DEPARTAMENTOS podrán sin consentimiento de la Comunidad de Propietarios y previo las licencias municipales correspondientes cambiar el uso o destino de los mismos, dividirlos, segregarlos, agruparlos o agregarlos con fincas colindantes del mismo o distinto inmueble, vertical u horizontalmente (modificando las cuotas de participación de los departamentos afectados por suma o distribución de sus cuotas), manteniendo, en su caso, la seguridad de los elementos comunes de ambas fincas.

3.– Gastos del portal

Los gastos de limpieza, alumbrado y conservación del ascensor, vestíbulo y escalera serán sufragados exclusivamente por los propietarios de las viviendas [ELEGIR: por partes iguales / con arreglo a su coeficiente de participación].

4.– Otros gastos:

Los gastos de reparación de los elementos comunes cuyo uso se encuentra individualizado o atribuido de forma exclusiva a algún departamento, se satisfarán con arreglo a las siguientes normas:

a) Los de mera conservación y mantenimiento, por el usuario.
b) Los originados por reparaciones extraordinarias, por todos los propietarios del edificio, [ELEGIR: por partes iguales / con arreglo a su coeficiente de participación].
c) Los originados por daños debidos a culpa o negligencia de los usuarios, por el causante del daño, tanto si son ordinarios como extraordinarios.

5.– Toldos, marquesinas y tendederos:

No podrá colocarse ningún tipo de toldo y/o marquesina en las terrazas del edificio de color, dimensiones y características diferentes a las que haya aprobado la Junta de Propietarios.

Asimismo queda totalmente prohibida la colocación de tendederos a los propietarios de las viviendas en las fachadas del edificio.

6.– Antenas parabólicas:

Queda totalmente prohibida la colocación de antenas parabólicas a los propietarios de los departamentos que componen el edificio en las fachadas del mismo.

7.– Rótulos informativos o de publicidad:

La promotora se reserva la facultad de colocar en el edificio rótulos informativos o de publicidad para la promoción y venta de las fincas resultantes de esta división, sin consentimiento de la comunidad de propietarios ni contraprestación de clase alguna, pudiendo mantenerlos hasta la finalización de las ventas de la totalidad de aquellas.

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

.– [OTROS DATOS]

Autorización

Así lo dicen y otorgan, después de hechas las reservas y advertencias legales pertinentes.

De conformidad con el art. 6º de la Ley Orgánica 3/2018, de 5 de diciembre, de Protección de Datos Personales y garantía de los derechos digitales, se entiende por consentimiento del afectado toda manifestación de voluntad libre, específica, informada e inequívoca por la que éste acepta, ya sea mediante una declaración o una clara acción afirmativa, el tratamiento de datos personales que le conciernen. Cuando se pretenda fundar el tratamiento de los datos en el consentimiento del afectado para una pluralidad de finalidades será preciso que conste de manera específica e inequívoca que dicho consentimiento se otorga para todas ellas. No podrá supeditarse la ejecución del contrato a que el afectado consienta el tratamiento de los datos personales para finalidades que no guarden relación con el mantenimiento, desarrollo o control de la relación contractual.

La finalidad de esta incorporación es facilitar la tramitación y seguimiento de esta escritura, es responsable del fichero, de su seguridad y confidencialidad el Notario titular de esta notaría.

Advierto también sobre la incorporación de datos a los ficheros automatizados regulados en la Orden del Ministerio de Justicia 484/2003, de 19 de febrero.

Permito a la Señora compareciente la lectura de esta escritura, porque así lo solicita después de advertida de la opción del artículo 193 del Reglamento Notarial.

Enterada, según dice, por la lectura que ha practicado y por mis explicaciones verbales, la señora compareciente hace constar libremente su consentimiento al contenido de la escritura. Y la firma. Y yo el Notario, del contenido de este instrumento público, extendido [Nº] folios de papel timbrado de la clase [CLASE], serie [SERIE], números [Nº].

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
Fdo. D./Dña. [NOMBRE Y APELLIDOS]: Fdo. D./Dña. [NOMBRE Y APELLIDOS]

========================================================================
