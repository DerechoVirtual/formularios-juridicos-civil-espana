---
name: resolucion-consular-deniega-inscripcion-matrimonio-civ-0054
description: "Resolución consular que deniega la inscripción de un matrimonio. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Resolución consular que deniega la inscripción de un matrimonio

> Formulario **CIV-0054** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Resolución consular que deniega la inscripción de un matrimonio» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Resolución consular que deniega la inscripción de un matrimonio” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:resolucion-consular-deniega-inscripcion-matrimonio-civ-0054`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (6 veces)
- [ ] FECHA (4 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] MES (2 veces)
- [ ] AÑO
- [ ] DIRECCIÓN
- [ ] DÍA
- [ ] LUGAR
- [ ] Nº DE PROCEDIMIENTO
- [ ] REGISTRO CIVIL

## Normas que cita el formulario

- art. 74 Código Civil

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

DENEGACIÓN DE INSCRIPCIÓN DE MATRIMONIO

Consulado General de España en [LOCALIDAD]

Expediente nº [Nº DE PROCEDIMIENTO]/20

A LA DIRECCIÓN GENERAL DE REGISTRO Y DEL NOTARIADO

Ministerio de Justicia

D. Dª., con nº DNI, y con domicilio a efecto de notificaciones en [DIRECCIÓN] en la C/, ante este organismo comparece para formular

RECURSO DE APELACIÓN

contra la resolución del registro civil consular del Consulado General de España en [LOCALIDAD], copia de la cual se adjunta como documento nº 1, y con número de expediente citado “ut supra”.

Recurso que formulo en base a los siguientes,

HECHOS

Primero.— Que en fecha [FECHA] se presentó ante el Registro Civil Consular del Consulado General de España en [LOCALIDAD] solicitud con objeto de inscribir matrimonio civil entre el recurrente y D. Dª., cual se celebró el día [FECHA] en la ciudad de

En prueba de ello se adjunta como documento nº 2 copia del certificado del Registro Civil de matrimonio.

Segundo.— Que la inscripción del matrimonio fue denegada, según se desprende de la escueta resolución recurrida por entender que era un matrimonio de los denominados “de complacencia” sobre la base de las audiencias reservadas realizadas a los contrayentes.

A los anteriores hechos son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

I

Según lo establecido en el artículo 355 del Reglamento del Registro Civil, este recurso se presenta ante la Dirección General de Registros y del Notariado dentro del plazo de 15 días hábiles para ello.

II

En cuanto al fondo del asunto, debemos expresar nuestra disconformidad con la resolución recurrida por considerar que la misma se encuentra falta de motivación:

Y ello porque la resolución denegatoria se limita a exponer una fórmula estereotipada de carácter genérico, como es

“se informa que se deniega la práctica de la misma al considerarse un matrimonio de complacencia sobre la base de las audiencias reservadas realizadas a los contrayentes.”

De dicha cláusula resulta imposible deducir cuales son los aspectos concretos de dichas audiencias reservadas que llevaron a concluir que el matrimonio era de los considerados “de complacencia”, lo que debe considerarse causa de indefensión toda vez que no permite conocer los verdaderos motivos de la denegación, lo que no permite impugnarlos o aportar prueba que desvirtúe dichos motivos.

En este sentido se pronuncia la resolución DGRN (6.ª) de 30 de mayo de 2007, sobre cancelación de inscripción de nacimiento, considerando que la necesidad de motivación jurídica suficiente es una expresión del principio de «interdicción de la arbitrariedad de los poderes públicos» que rige también en el ámbito registral.

En dicha resolución se expresa que:

“Así lo impone la necesidad de evitar que se genere una situación de indefensión al interesado, para lo cual se hace necesario que la resolución contenga los extremos básicos que permitan a aquél conocer y evaluar cuales han sido los presupuestos en los que la autoridad que ha dictado el auto, en este caso el Encargado del Registro Civil Consular, ha apoyado y encontrado fundamento para su decisión. Nos encontramos aquí, pues, ante la necesidad de motivación jurídica suficiente como expresión del principio de «interdicción de la arbitrariedad de los poderes públicos», que ha encontrado consagración constitucional en el artículo 9.3 de nuestro Carta Magna, toda vez que, como ha señalado el Tribunal Supremo, los actos no motivados se tienen por arbitrarios (vid. Sentencias de 30 de junio de 1982 y 15 de octubre y 29 de noviembre de 1985).

La motivación es, pues, una garantía del derecho de defensa mediante el cual se puede comprobar que la resolución dada al caso es consecuencia de una exigencia racional del Ordenamiento jurídico, y no fruto de la arbitrariedad (vid. Sentencia del Tribunal Constitucional de 165/1993). Esta necesidad de motivación de las decisiones jurídicas se incrementa en relación con los actos que limiten los derechos subjetivos o los intereses legítimos de los ciudadanos cualquiera sea el procedimiento en que se dicten y constituyen, además, una exigencia formal y material de los autos denegatorios, según se desprende de los artículos 208.2 y 209.3.ª de la Ley de Enjuiciamiento Civil, aplicable a este ámbito registral en razón de la aplicabilidad supletoria de las normas procesales civiles que ordena el artículo 16 del Reglamento del Registro Civi l.”

Debe recordarse que la motivación es un medio técnico de control de la causa del acto, es decir, que no se trata de un simple requisito meramente formal, sino de fondo, que no se cumple mediante el empleo de cualquier fórmula convencional, sino que ha de ser suficiente, esto es, ha de dar razón plena al proceso lógico y jurídico determinante de la decisión (así lo estableció la S.T.C. de 17-7-1981), lo que no ha ocurrido en este caso.

Por lo expuesto, para considerarse motivada la resolución, debería haberse razonado cuales son los aspectos concretos de las audiencias personales que llevan a concluir que el matrimonio era de los denominados “de complacencia”, y el razonamiento lógico que lleva a tal conclusión.

Al no haberse hecho así, se ha incurrido en causa de anulabilidad de la resolución recurrida.

II

Debemos recordar en este caso, que la propia Dirección General de los Registros y del Notariado, dictó una Instrucción de 31 de enero de 2006, (BOE núm 41 de 17 febrero 2006) en la que se establecieron unas reglas de funcionamiento para poder inferir que existe un consentimiento simulado.

Así, dicha Instrucción establece que:

I. Los datos básicos de los que cabe inferir la simulación del consentimiento matrimonial son dos: a) el desconocimiento por parte de uno o ambos contrayentes de los «datos personales y/o familiares básicos» del otro y b) la inexistencia de relaciones previas entre los contrayentes. En cuanto a la valoración de ambos elementos se han de tomar en cuenta los siguientes criterios prácticos1:

1. La Instrucción DGRN establece varios criterios, por lo que habrá que ver cual es el que puede ajustarse mejor al caso concreto. Aquí citamos uno a modo de ejemplo.

4.ª En su caso el «desconocimiento» de los datos personales y familiares básicos de un contrayente respecto del otro debe ser claro, evidente y flagrante. Por tanto, el desconocimiento de un solo, singular y aislado dato personal o familiar básico del otro contrayente no es relevante para inferir automáticamente la existencia de un matrimonio simulado.

Debe, por tanto, llevarse a cabo una valoración de conjunto del conocimiento o desconocimiento de un contrayente respecto del otro.

En el presente caso, resulta evidente que no se ha realizado ninguna “valoración conjunta”, o si se ha hecho, no existe forma de conocerla del tenor literal de la resolución denegatoria.

Posteriormente se establece también que

Aun cuando los contrayentes puedan desconocer algunos «datos personales y familiares básicos recíprocos», ello puede resultar insuficiente a fin de alcanzar la conclusión de la existencia de la simulación, si se prueba que los contrayentes han mantenido relaciones antes de la celebración del matrimonio, bien personales, o bien por carta, teléfono o Internet que por su duración e intensidad no permita excluir toda duda sobre la posible simulación

La mencionada Instrucción, finalmente, establece las siguientes reglas de funcionamiento adicionales de las «presunciones»:

1.º Tanto por la presunción general de buena fe como porque el «ius nubendi» es un derecho fundamental de la persona, es necesario que el Encargado del Registro Civil alcance una «certeza moral plena» de hallarse en presencia de un matrimonio simulado para acordar la denegación de la autorización del matrimonio o de su inscripción.

En efecto, si bien no puede exigirse evidencia total» -imposible en el ámbito de las presunciones, ya que con ellas el Juez, en este caso el Encargado del Registro, no tiene un conocimiento directo ni indirecto del objeto de la prueba (hecho presunto), sino que deduce ese conocimiento de la prueba de otro hecho distinto (hecho base o indicio) con él unido de forma precisa y directa, «según las reglas del criterio humano que no son otras que las del raciocinio lógico» (vid. Sentencia del Tribunal Supremo de 25 de octubre de 1986)-, sí es necesario que el Encargado del Registro alcance un convencimiento o convicción plena en el sentido de concluir la valoración del conjunto de la prueba y de las audiencias practicadas (vid. Sentencia del Tribunal Supremo de 8 de noviembre de 1986) con un juicio conclusivo de probabilidad cualificada en grado de «certeza moral plena» sobre la veracidad del hecho de haber mediado un consentimiento simulado, descartando los casos de mera verosimilitud y los de duda o simple probabilidad. Y todo ello con arreglo a los criterios de la sana crítica, esto es, con arreglo a criterios valorativos racionales y a las máximas de experiencia común. Por ello, si la convicción de la simulación no que el Encargado adquiera una conciencia de «verdad material absoluta» o « es plena, el matrimonio deberá autorizarse o, en su caso, inscribirse.

En tales casos, como antes se ha recordado, queda siempre la posibilidad de que, si surgen posteriormente más datos o hechos que hagan dudar de la existencia y autenticidad del consentimiento matrimonial, se inste judicialmente la nulidad del matrimonio, a través del proceso judicial correspondiente (art. 74 Código Civil) por el Ministerio Fiscal, los cónyuges o cualquier persona con interés directo y legítimo (vid. Resolución de 6 de julio de 1998, Consulta DGRN 1 de junio de 2004, Consulta DGRN 28 de octubre de 2004).

2.º En todo caso, el Encargado del Registro Civil que aplica las presunciones judiciales debe incluir en su resolución, de modo expreso, el razonamiento en virtud del cual dicha Autoridad ha establecido la presunción, evitando la utilización de modelos formularios que, por su generalidad y falta de referencia a las concretas circunstancias particulares del caso concreto, no alcanzan a llenar el requisito imprescindible de la motivación de la resolución (cfr.art. 386 n.º 2 LEC).

3.º Frente a la formulación de una presunción judicial, cualquiera de los contrayentes u otra persona legitimada puede practicar una prueba en contrario, la cual puede estar dirigida a demostrar la inexistencia del indicio tomado en cuenta por la Autoridad española y/o demostrar la inexistencia del nexo de inferencia entre tal indicio y la situación de matrimonio simulado (art. 386.3 y 385.2 LEC).

En el caso que nos ocupa, vemos que no resulta posible practicar prueba en contrario pues los interesados no pueden conocer “el indicio tomado en cuenta por la Autoridad española” para inferir la existencia de un matrimonio simulado.

III

En el presente caso debe recordarse, además, que en los interesados se daban las siguientes circunstancias, que fueron expuestas en las audiencias reservadas, y acreditadas documentalmente2:

2. En este punto habrá que exponer todas las circunstancias del caso que acreditan la autenticidad de la relación afectiva, (se adjunta algunas a modo de ejemplo) así como citar los documentos aportados y aportar nueva documentación, como pueden ser fotografías, envío de cartas o correos electrónicos, billetes de avión que demuestren viajes de uno o ambos miembros de la pareja, documentación conjunta (cuentas bancarias, empadronamiento, titularidad conjunta de bienes, envíos de dinero de uno a otro miembro de la pareja, estudios que se hayan realizado conjuntamente, estancias hoteleras, etc).

Recordemos que la Instrucción DGRN establece que el hecho probado de que los contrayentes conviven juntos en el momento presente o tienen un hijo común es un dato suficiente para acreditar la existencia de "relaciones personales", por lo que esta circunstancia, caso de darse, debe ser especialmente remarcada y acreditada.

- D. y D.ª [NOMBRE Y APELLIDOS] tienen una relación afectiva desde ....

-Se conocieron en [LOCALIDAD] en (exponer las circunstancias de dicho encuentro).

-Desde esa fecha han mantenido una relación a través de teléfono, correo e internet.

-Dª. viajó a [LOCALIDAD] posteriormente en varias ocasiones.

-El día [FECHA] nació en [LOCALIDAD] el hijo de ambos, cuyo nacimiento fue inscrito en [REGISTRO CIVIL].

En resumen, todas estas circunstancias constituyen una evidencia de la existencia de una relación afectiva de tal entidad que para desvirtuarla haría falta algo más que unas meras contradicciones u omisiones como las que se pueden haber producido en las audiencias reservadas a los interesados, por lo que en este caso debería prevalecer sin género de dudas el “ius nubendi” como derecho fundamental de los mismos.

Por todo lo expuesto,

SUPLICO A LA DIRECCIÓN GENERAL DE REGISTRO Y NOTARIADO, del Ministerio de Justicia, que tenga por presentado este escrito, sirva admitirlo, así como la documentación que se adjunta y, una vez evaluados los trámites necesarios, dicte resolución anulando la resolución de fecha [FECHA] de [MES] de 20 del Registro Civil Consular de España en y, en consecuencia, apruebe la autorización de la inscripción del matrimonio civil entre D./Dª [NOMBRE Y APELLIDOS] y D./Dª [NOMBRE Y APELLIDOS]

Por ser Justicia que pido en [LUGAR], a [DÍA] de [MES] de [AÑO].

Fdo.

========================================================================
