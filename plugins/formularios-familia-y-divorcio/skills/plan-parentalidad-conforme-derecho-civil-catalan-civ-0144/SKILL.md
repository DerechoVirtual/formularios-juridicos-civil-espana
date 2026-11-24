---
name: plan-parentalidad-conforme-derecho-civil-catalan-civ-0144
description: "Plan de parentalidad conforme al Derecho civil catalán. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Plan de parentalidad conforme al Derecho civil catalán

> Formulario **CIV-0144** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Plan de parentalidad conforme al Derecho civil catalán» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Plan de parentalidad conforme al Derecho civil catalán” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:plan-parentalidad-conforme-derecho-civil-catalan-civ-0144`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] OTROS DATOS (19 veces)
- [ ] NOMBRE DEL PROGENITOR (12 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] DNI/NIE (3 veces)
- [ ] FECHA (3 veces)
- [ ] NOMBRE DEL CENTRO (3 veces)
- [ ] Nº (2 veces)
- [ ] TELÉFONO (2 veces)
- [ ] CALIDAD EN QUE ACTÚA
- [ ] HORA
- [ ] PLAZO

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

Firmas
Anexo
Decisiones relativas a la guarda y el lugar en el que vivirán habitualmente (art. 233-9.2a)
Tareas de las que se debe responsabilizar cada progenitor en relación con las actividades cotidianas de los hijos (art. 233-9.2b)
Forma de la que se deben hacer los cambios en la guarda (art. 233-9.2c)
Régimen de relación y de comunicación con los hijos durante los períodos en que un progenitor no los tenga con él (art. 233-9.2d)
Régimen de estancias de los hijos con cada uno de los progenitores en períodos festivos, de vacaciones y en fechas especialmente señaladas para los hijos, para los progenitores o para su familia (art. 233-9.2e)
Decisiones relativas a la educación y a las actividades extraescolares, formativas y de ocio (art. 233-9.2f)
Deberes de información y consulta entre los progenitores en relación con los hijos (art. 233-9.2g)
Decisiones relativas al cambio de domicilio y otras cuestiones relevantes para los hijos (art. 233-9.2h)
Modificaciones, revisión del plan y recurso a la mediación familiar

Plan de parentalidad relativo a las cuestiones principales que afectan al hijo o los hijos comunes en caso de ruptura familiar, preceptivo en los procedimientos de separación, divorcio o nulidad a los que sea de aplicación el Derecho civil especial de Cataluña.

D./Dña. [NOMBRE Y APELLIDOS], con DNI [DNI/NIE], como [CALIDAD EN QUE ACTÚA] con domicilio en [LOCALIDAD] y teléfono [TELÉFONO].

D./Dña. [NOMBRE Y APELLIDOS], con DNI [DNI/NIE], como con domicilio en [LOCALIDAD] y teléfono [TELÉFONO].

En relación a sus hijos:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

1. [NOMBRE Y APELLIDOS], con DNI [DNI/NIE], nacido el día [FECHA], en [LOCALIDAD].

EL RÉGIMEN de GUARDA CON ESTABLECIMIENTO DEL RÉGIMEN DE LAS RELACIONES PERSONALES [OTROS DATOS].

Y, para su mejor ejercicio,

el presente PLAN DE PARENTALIDAD según lo que establece el artículo 233-9 del Código civil catalán en [LOCALIDAD], en fecha [FECHA],

Firmado	Firmado
D./Dña. [NOMBRE Y APELLIDOS] D./Dña. [NOMBRE Y APELLIDOS]

A) Decisiones relativas a la guarda y el lugar en el que vivirán habitualmente (art. 233-9.2a)

□ Los padres acuerdan la guarda compartida del/de los hijo/s común/nes, cuya distribución se llevará a cabo por períodos de:

□ Semanas

□ Meses

□ Intervalos de seis meses

□ Otros: [OTROS DATOS].

□ El/Los hijo/s vivirá/n en el domicilio de cada uno de los progenitores según el período establecido.

□ El/Los hijo/s estará/n bajo la guarda del progenitor [NOMBRE DEL PROGENITOR] y en el domicilio de este, sin perjuicio del carácter compartido de las responsabilidades parentales.

□ El/Los hijo/s vivirá/n habitualmente en el hogar del progenitor [NOMBRE DEL PROGENITOR], dado que es quien tiene la guarda.

□ Otros: [OTROS DATOS].

B) Tareas de las que se debe responsabilizar cada progenitor en relación con las actividades cotidianas de los hijos (art. 233-9.2b)

□ Mientras no se acuerde lo contrario, los progenitores son los principales responsables del cuidado del/de los hijo/s común/nes.

□ Cada progenitor se hará cargo, por él mismo o mediante las personas que designe, de las tareas domésticas generadas por el cuidado del/de los hijo/s mientras lo/s tenga en su compañía, con la colaboración del/de los hijo/s desde que tenga/n la madurez suficiente.

□ Cada progenitor se hará cargo, por si mismo o mediante otras personas que designe, de llevar el/los hijo/s a la escuela y a las actividades extraescolares, así como de recogerlo/s, mientras esté/n en su compañía.

□ Cada progenitor puede escoger las personas adecuadas para que cuiden a los hijos mientras no se puedan hacer cargo.

□ Otros: [OTROS DATOS].

Durante el ejercicio de la guarda:

□ Cada progenitor puede tomar las decisiones cotidianas relativas a los hijos mientras estos se encuentren en su compañía.

□ Cada progenitor se responsabiliza de las decisiones siguientes: [OTROS DATOS].

□ Otros:

C) Forma de la que se deben hacer los cambios en la guarda (art. 233-9.2c)

□ Los intercambios tendrán lugar:

□ En la vivienda del progenitor que tenga la guarda en cada momento.

□ En la vivienda del otro progenitor.

□ En la escuela, al inicio o fin de la jornada escolar.

□ Otros: [OTROS DATOS].

□ Los intercambios se deben llevar a cabo dentro del horario [HORA].

□ El progenitor que reciba el/los hijo/s en guarda o con el fin de hacer efectivo el régimen de relaciones personales es el encargado de transportarlos.

□ El progenitor [NOMBRE DEL PROGENITOR] es el responsable de transportar el/los hijo/s en los cambios de la guarda o cuando tenga lugar el régimen de relaciones personales.

□ Si un progenitor, por cualquier causa, no puede hacer efectiva la guarda que tiene asignada, es responsable de encontrar un sistema alternativo de guarda para el/los hijo/s.

□ El progenitor que solicite un cambio en la guarda es responsable de cualquier gasto adicional de cuidado o transporte del/de los hijo/s que pueda resultar del cambio.

D) Régimen de relación y de comunicación con los hijos durante los períodos en que un progenitor no los tenga con él (art. 233-9.2d)

□ El progenitor que no tenga la guarda del/de los hijo/s común/nes podrá tenerlos en su compañía en los intervalos siguientes:

□ Fines de semana alternos:

□ Desde viernes a lunes por la mañana.

□ Otros: [OTROS DATOS].

□ Fines de semana alternos, más los días intersemanales siguientes: [OTROS DATOS].

□ Otros: [OTROS DATOS].

□ El progenitor con quien no esté/n el/los hijo/s podrá comunicarse con él/ellos por cualquier medio siempre que lo considere oportuno. En caso de comunicación telefónica, se deberá respetar el horario de descanso de los hijos, del otro progenitor y, si es el caso, del resto de su familia.

□ Otros: [OTROS DATOS].

E) Régimen de estancias de los hijos con cada uno de los progenitores en períodos festivos, de vacaciones y en fechas especialmente señaladas para los hijos, para los progenitores o para su familia (art. 233-9.2e)

1) Vacaciones de verano

□ Con independencia del progenitor a quien pueda corresponder la guarda del/de los hijo/s, cada progenitor podrá tenerlo/s la mitad de los períodos de vacaciones escolares de verano. En defecto de acuerdo entre los progenitores, el progenitor [NOMBRE DEL PROGENITOR] los tendrá el primer período los años pares y el progenitor [NOMBRE DEL PROGENITOR] los impares.

□ Los progenitores fijan la forma en que se producirá.

□ Otros períodos: [OTROS DATOS].

□ Después del período vacacional el reinicio habitual del [régimen de guarda][régimen de semana alterna].

□ Le corresponderá al progenitor que no haya estado con sus hijos en el último período de vacaciones.

□ Otros: [OTROS DATOS].

2) Vacaciones de Navidad

□ Cada progenitor tendrá el/los hijo/s la mitad de los períodos de vacaciones escolares de Navidad. A falta de acuerdo de los progenitores, el progenitor [NOMBRE DEL PROGENITOR] los tendrá el primer período los años pares y el progenitor [NOMBRE DEL PROGENITOR] los años impares.

□ Otros: [OTROS DATOS].

□ Después del período vacacional el reinicio habitual del régimen de [guarda][fines de semana alternos]

□ Le corresponderá al progenitor que no haya estado con sus hijos en el último período de vacaciones.

□ Otros: [OTROS DATOS].

3) Vacaciones de invierno

□ El/Los hijo/s podrán estar en compañía de cada progenitor por partes iguales. En este caso, el progenitor [NOMBRE DEL PROGENITOR] tendrá el/los hijo/s la primera parte de la semana los años pares, mientras que el otro los tendrá la primera parte de la semana en los años impares.

□ El progenitor [NOMBRE DEL PROGENITOR] tendrá el/los hijo/s toda la semana en los años pares, mientras que el otro los tendrá toda la semana en los años impares.

4) Vacaciones de Semana Santa

□ Cada progenitor tendrá el/los hijo/s la mitad de las vacaciones escolares de Semana Santa. A falta de acuerdo de los progenitores, decidirá el progenitor [NOMBRE DEL PROGENITOR] los años pares y el otro los impares.

□ Otros: [OTROS DATOS].

5) Días señalados

□ Los progenitores acuerdan que el día [FECHA] el régimen será el siguiente: [OTROS DATOS].

□ En las fechas de aniversario de los menores o de los progenitores, prevalecerá el acuerdo de los progenitores y, a falta de acuerdo, se aplicará el régimen de comunicación y relaciones previsto con carácter general.

□ Durante el aniversario del/de los hijo/s, este/estos estarán en compañía del progenitor [NOMBRE DEL PROGENITOR] los años pares y del progenitor [NOMBRE DEL PROGENITOR] los años impares.

□ Aunque no le corresponda, el día de su cumpleaños cada progenitor podrá tener el/los hijo/s en su compañía durante [Nº] horas, siempre que informe al otro progenitor con [PLAZO], como mínimo, [Nº] días de antelación.

6) Vacaciones y viajes con el/los hijo/s

□ Cada progenitor puede viajar con el/los hijo/s durante el tiempo en el que el/los tenga bajo su guarda comunicándolo previamente al otro progenitor.

□ El progenitor que tenga el pasaporte o documento adecuado del/de los hijo/s tendrá que facilitar al otro progenitor.

F) Decisiones relativas a la educación y a las actividades extraescolares, formativas y de ocio (art. 233-9.2f)

□ La educación que recibirán los hijos será:

□ Pública. Especificar centro, si es el caso: [NOMBRE DEL CENTRO].

□ Privada. Especificar centro, si es el caso [NOMBRE DEL CENTRO].

□ Concertada. Especificar centro, si es el caso: [NOMBRE DEL CENTRO].

□ Mientras entre el/los hijo/s residan con él, cada progenitor podrá autorizar que participen en las actividades que no requieran organización previa, así como en las actividades sociales.

□ Se requiere el acuerdo de los padres para inscribir a los hijos en actividades deportivas u otras que requieran un entrenamiento especial mientras el/los hijo/s están con el otro progenitor.

□ Otros: [OTROS DATOS].

G) Deberes de información y consulta entre los progenitores en relación con los hijos (art. 233-9.2g)

□ Cada progenitor debe informar al otro de los aspectos relativos a la salud, educación y ocio de sus hijos.

□ Los dos progenitores se deberán intercambiar y tendrán acceso a los documentos relevantes de sus hijos.

□ Toda información relativa al/a los hijo/s se deberá intercambiar entre los progenitores, que en ningún caso pueden utilizar el/los hijo/s como mensajero/s parar transmitir información, plantear cuestiones o proponer cambios.

H) Decisiones relativas al cambio de domicilio y otras cuestiones relevantes para los hijos (art. 233-9.2h)

□ Cada progenitor deberá comunicar al otro, con un preaviso mínimo de 30 días, su intención de cambiar de domicilio.

□ Si el cambio de domicilio de un progenitor es incompatible con el régimen de guarda o visitas establecido, los progenitores deberán revisar el acuerdo del plan de parentalidad para alcanzar otro que se adapte lo mejor posible a las necesidades del/de los hijo/s.

□ El/Los hijo/s deberán estar con el progenitor que permanezca en el domicilio inicial hasta que los progenitores alcancen un acuerdo alternativo.

□ Si un progenitor tiene conocimiento de cualquier enfermedad, accidente, hospitalización o cualquier otra circunstancia que afecta a la salud del hijo, debe comunicarlo inmediatamente al otro progenitor.

□ Otros: [OTROS DATOS].

I) Modificaciones, revisión del plan y recurso a la mediación familiar

□ Los progenitores acuerdan el recurso a la mediación familiar en caso de que la aplicación del plan provoque diferencias entre los progenitores o haya que modificar el contenido para adaptarlo a las necesidades de las diferentes etapas de la vida de los hijos o a las nuevas circunstancias de los progenitores.

□ Otras circunstancias relevantes [OTROS DATOS] para modificar los aspectos del plan.

Modelo elaborado, con carácter meramente indicativo, y facilitado por la Dirección General de Derecho y Entidades Jurídicas de la Generalitat de Cataluña, en cumplimiento de la Disposición adicional 9.ª de la Ley 25/2010, de 29 de julio, del Libro II del Código civil de Cataluña, relativo a la persona y a la familia.

El Plan de parentalidad es el instrumento diseñado por el Código civil de Cataluña para ordenar las cuestiones principales que pueden afectar al hijo o hijos comunes en caso de ruptura familiar, que debe presentarse tanto si el proceso es de mutuo acuerdo como si es contencioso para determinar cómo se ejercerán las responsabilidades parentales (arts. 233-8.2 y 233.9 CCCat).

========================================================================
