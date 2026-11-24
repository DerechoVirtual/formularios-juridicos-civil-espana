---
name: plan-parentalidad-mutuo-acuerdo-guarda-individual-civ-0162
description: "Plan de parentalidad de mutuo acuerdo con guarda individual. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Plan de parentalidad de mutuo acuerdo con guarda individual

> Formulario **CIV-0162** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Plan de parentalidad de mutuo acuerdo con guarda individual» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Plan de parentalidad de mutuo acuerdo con guarda individual” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:plan-parentalidad-mutuo-acuerdo-guarda-individual-civ-0162`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (3 veces)
- [ ] MES (3 veces)
- [ ] AÑO (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE DEL MENOR (2 veces)
- [ ] ACTIVIDADES EXTRAESCOLARES
- [ ] CALLE
- [ ] DÍA
- [ ] NOMBRE DEL CENTRO
- [ ] NOMBRE DEL PROGENITOR
- [ ] NOMBRE Y APELLIDOS
- [ ] NÚMERO DE LA CALLE

## Normas que cita el formulario

- art. 233 Código Civil

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

En la ciudad de [LOCALIDAD], a [DÍA] de [MES] de [AÑO]

MANIFIESTAN

Que los que suscriben contrajeron matrimonio en fecha [FECHA] y fruto de la convivencia son padres de dos hijos, ambos menores de edad: [NOMBRE DEL MENOR], nacido/a el día [FECHA], del mes de [MES], del año [AÑO]; y [NOMBRE DEL MENOR], nacida/o el día [FECHA], del mes de [MES], del año

El domicilio familiar está sito en la localidad de [LOCALIDAD], calle [CALLE], núm. [NÚMERO DE LA CALLE]

Siendo voluntad de ambas partes proceder a la separación/divorcio de mutuo acuerdo acuerdan la regulación del cuidado de sus hijos atribuyéndose la guarda individual a [NOMBRE DEL PROGENITOR], con el establecimiento del régimen de relaciones personales en favor del progenitor no guardador, de acuerdo con el presente PLAN DE PARENTALIDAD con el siguiente contenido según lo previsto en el artículo 233-9 del Código Civil de Cataluña:

PRIMERO ASPECTOS RELATIVOS A LA GUARDA Y AL LUGAR EN QUE VIVIRÁN HABITUALMENTE LOS HIJOS (Art. 233-9.2a)

Los padres acuerdan la atribución de la guarda indivual de los hijos comunes a la madre Dª [NOMBRE Y APELLIDOS], por ser más conveniente al interés de los hijos, dada la situación personal y laboral del padre.

La madre y los hijos residirán habitualmente en el domicilio familiar que figura en el encabezamiento.

SEGUNDO TAREAS DE QUE SE DEBE RESPONSABILIZAR CADA PROGENITOR EN RELACIÓN A LAS ACTIVIDADES COTIDIANAS DE LOS HIJOS (Art. 233-9.2b)

La madre se responsabilizará de las tareas correspondientes al cuidado de los hijos, entre ellas las domésticas, las de llevar y recoger a los hijos al colegio y actividades extraescolares, cuidar de sus estudios y alimentación y similares, y adoptará las decisiones necesarias en relación a las actividades cotidianas de los hijos.

En caso de no poderse responsabilizar personalmente, la madre se encargará de escoger las personas idóneas para hacerse cargo de estas actividades.

El padre cooperará a las tareas cotidianas en el caso de ser requerido para ello por la madre, debiendo realizarlas en todo caso en los periodos en que tenga en su compañía a los hijos según el régimen de estancias que se pacta en el presente Plan.

TERCERO FORMA EN QUE DEBEN REALIZARSE LOS CAMBIOS (Art. 233-9.2 c).

Los cambios de progenitor tendrán lugar en el domicilio habitual de la madre e hijos, al cual deberá acudir el padre para recoger y reintegrar a los hijos menores al inicio y finalización de cada periodo de estancia.

El padre se hará cargo de los costes que se generen.

CUARTO RÉGIMEN DE RELACIÓN Y COMUNICACIÓN CON LOS HIJOS (Art. 233- 9.2.d)

El padre podrá comunicarse con los hijos en el momento en que estime oportuno por cualquier medio, respetando en todo caso los periodos de estudio y descanso de los hijos.

En caso de desacuerdo y de forma subsidiaria, se fija el siguiente régimen de comunicación:

A) El padre podrá tener en su compañía a los hijos una tarde a la semana en que no realicen actividades extraescolares, desde la finalización de las horas lectivas hasta las 20.30 horas.

B) El padre podrá tener en su compañía a los hijos los fines de semana alternos, desde el viernes a las 20:00 horas hasta el domingo a las 20:00 horas.

QUINTO RÉGIMEN DE ESTANCIAS EN VACACIONES Y FECHAS ESPECIALMENTE SEÑALADAS (art. 233-9.2 e).

El padre podrá tener en su compañía a los hijos en los periodos vacacionales y fechas que convenga con la madre de forma flexible, si bien para el caso de que existan discrepancias se fijan con carácter subsidiario el siguiente régimen de estancias:

A) En cuanto a las vacaciones de Navidad, los hijos pasarán la mitad de las vacaciones escolares de Navidad con el padre, según elija éste en los años impares, eligiendo la madre en los pares. El primer período se iniciará el día siguiente a aquél en que finalicen las clases y finalizando el mismo, el día 31 de diciembre al mediodía. El segundo período comenzará el día 31 de diciembre al mediodía y finalizará el día inmediatamente anterior a aquél en que comiencen las clases.

B) En cuanto a las vacaciones de Semana Santa, los hijos pasarán la mitad de las vacaciones escolares de Semana Santa con el padre, según elija éste en los años impares, eligiendo la madre en los pares, iniciándose el primer período el día siguiente a aquél en que finalicen las clases y finalizando el mismo, el miércoles al mediodía. El segundo período comenzará el primer miércoles al mediodía y finalizará el día inmediatamente anterior a aquél en que comiencen las clases.

C) En cuanto a las vacaciones estivales, Julio y Agosto, los hijos pasarán un mes de sus vacaciones con el padre en los años impares, eligiendo la madre en los pares.

En los periodos vacacionales, los hijos podrán viajar tanto con el padre como con la madre siempre que éste lo comunique previamente al otro, obligándose ambos a facilitarse la documentación necesaria para que puedan llevar a cabo los viajes vacacionales.

D) En cuanto a los días señalados, los hijos pasarán el día del cumpleaños del padre o de la madre con éste, con respeto a su horario y obligaciones escolares y extraescolares.

El día del cumpleaños de los hijos, el padre podrá visitarlos y tenerlos en su compañía en la comida o cena, con respeto a las obligaciones y horario más adecuado para los hijos.

SEXTO TIPO DE EDUCACIÓN Y ACTIVIDADES EXTRAESCOLARES, FORMATIVAS Y DE TIEMPO LIBRE (Art. 233-9.2 f).

Los hijos recibirán su educación en el Centro [NOMBRE DEL CENTRO] donde se encuentran matriculados en la actualidad. El cambio de Centro deberá realizarse de mutuo acuerdo por ambos padres en interés de los hijos.

Los hijos cursarán las siguientes actividades extraescolares [ACTIVIDADES EXTRAESCOLARES] La modificación de las actividades extraescolares deberá realizarse de mutuo acuerdo por ambos padres en interés de los hijos.

La madre puede decidir sobre otras actividades formativas, sociales y de tiempo libre de los hijos en interés de éstos, comunicándolo al padre.

SÉPTIMO DEBERES DE INFORMACIÓN SOBRE LOS HIJOS (Art. 233-9.2 g)

Cada progenitor ha de informar al otro de los aspectos relativos a la salud, educación y bienestar de los hijos, facilitándose mutuamente el acceso a todos los documentos que tengan relación con estos aspectos.

La comunicación entre los padres ha de ser personal, sin que dicha información pueda realizarse por intermediación de terceros ni de los propios hijos.

OCTAVO DECISIONES RELATIVAS AL CAMBIO DE DOMICILIO Y A OTRAS CUESTIONES RELEVANTES (Art. 233-9.2 h)

La madre ha de comunicar la intención de cambio de domicilio con un preaviso mínimo de dos meses. En caso de que el cambio de domicilio sea del padre, debe observar el mismo periodo de preaviso.

Si el cambio de domicilio fuera incompatible con las medidas acordadas en el presente plan, ambos progenitores deberán revisarlo para adecuarlo a las necesidades de los hijos, comprometiéndose el progenitor que cambia de domicilio a asumir los mayores costes económicos que puedan generarse en concepto de desplazamientos o transportes derivados del cambio de domicilio.

Cualquiera de los progenitores podrá tomar cualquier decisión en caso de urgencia tales como enfermedad, accidente, hospitalización u otra circunstancia que afecte a la salud de los hijos, comunicándolo inmediatamente al otro progenitor.

NOVENO.- MODIFICACIÓN DEL PLAN Y MEDIACIÓN FAMILIAR (art. 233-9.3).

Los padres revisarán de mutuo acuerdo el Plan en el caso que sea necesario en interés de los hijos.

Los padres pactan que acudirán a la mediación familiar en relación a las diferencias que puedan producirse en la aplicación del presente Plan o si no se ponen de acuerdo en el caso que sea necesaria su revisión.

Y en prueba de conformidad, los comparecientes se ratifican en el contenido de todos y cada uno de los pactos que integran el presente documento, los cuales han sido redactados según sus propias instrucciones, firmándolo por duplicado y a un solo efecto en el lugar y fecha arriba indicados, quedando uno de ellos en poder de cada uno de los padres, quien pueden presentarlo en el caso de interposición de demanda de separación o divorcio.

Fdo.: Fdo.:

========================================================================
