---
name: normas-regimen-interior-urbanizacion-civ-0637
description: "Normas de régimen interior de una urbanización. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Normas de régimen interior de una urbanización

> Formulario **CIV-0637** del plugin **Comunidades de propietarios** (`formularios-comunidades-de-propietarios`) · Civil › Propiedad horizontal · normativa revisada el 24-11-2026.

## Qué es

Reglamento de régimen interior para una urbanización o conjunto residencial sujeto a propiedad horizontal, que desarrolla las normas de convivencia, el uso de servicios comunes (calefacción, ascensores, piscinas, pistas de tenis, basuras), el régimen de sanciones y las obligaciones de ocupantes y arrendatarios. No regula las prohibiciones o limitaciones al derecho de propiedad, que corresponden a los Estatutos o a los acuerdos adoptados en Junta conforme a la Ley de Propiedad Horizontal.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Normas de régimen interior de una urbanización» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Normas de régimen interior de una urbanización” para mi caso». También puedes invocarla directamente con `/formularios-comunidades-de-propietarios:normas-regimen-interior-urbanizacion-civ-0637`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-comunidades-de-propietarios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Comunidades de propietarios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] HORA (6 veces)
- [ ] DÍA (4 veces)
- [ ] CALLE
- [ ] DENOMINACIÓN DE LA URBANIZACIÓN
- [ ] EDAD
- [ ] LOCALIDAD
- [ ] Nº
- [ ] PERIODO MÁXIMO DE USO

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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…y de las acciones previstas en el artículo 19 de la Ley de Propiedad Horizontal.»: comprobar el artículo de la Ley 49/1960, de 21 de julio, sobre propiedad horizontal, que regula en la redacción vigente las acciones frente a los incumplimientos (posiblemente el artículo 7.2); el original citaba el artículo 19.
- Junto a «… los requisitos mencionados. Artículo 13. Normas de uso de los espacios comunes.»: el original no traía el título de este artículo; se ha titulado conforme a su contenido.

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

REGLAMENTO DE RÉGIMEN INTERIOR DE LA URBANIZACIÓN [DENOMINACIÓN DE LA URBANIZACIÓN], SITA EN EL NÚMERO [Nº] DE LA CALLE [CALLE] DE [LOCALIDAD]

CAPÍTULO I. DISPOSICIONES GENERALES

Artículo 1. Carácter obligatorio del Reglamento.

El presente Reglamento es de obligado cumplimiento y los empleados de la Urbanización están facultados para hacerlo cumplir. Los derechos y obligaciones de los Estatutos y de este Reglamento afectan de idéntica forma a los ocupantes de las viviendas y locales, sean propietarios, usufructuarios, arrendatarios o usuarios por cualquier título de ocupación, o bien por simple cesión onerosa o gratuita del propietario.

El encargado de la Urbanización dará nota por escrito a la Junta Directiva de todo incumplimiento denunciado por los empleados de la misma, a efecto de darlo a conocer y adoptar las decisiones oportunas.

La Junta Directiva, a través del Secretario Administrador, dará cuenta por escrito al propietario del piso de la decisión tomada en relación con la falta cometida por él, sus familiares, invitados y personas dependientes. Cuando el piso o local lo ocupen terceras personas, de las que tenga constancia la Comunidad, las comunicaciones se harán también igualmente a los usuarios.

Artículo 2. Carácter ejecutivo de las decisiones de la Junta Directiva.

Las decisiones de la Junta Directiva serán ejecutivas y la persona sancionada podrá impugnarlas por escrito ante la Junta Directiva.

CAPÍTULO II. DE LAS SANCIONES A IMPONER

Artículo 3. Primera falta.

La comisión de la primera falta a las normas de la Comunidad dará lugar a una amonestación simple.

Artículo 4. Segunda falta.

La comisión de una segunda falta supondrá una segunda amonestación con la advertencia de que podrá ser privado, en la forma y tiempo que se establezca, de la utilización de servicios o elementos comunes.

Artículo 5. Tercera falta.

La comisión de una tercera falta podrá dar lugar a la privación del derecho a utilizar elementos y servicios comunes, sin perjuicio de la decisión que al respecto pueda adoptarse en la Junta General e independientemente de la reparación económica de los daños ocasionados y de las acciones previstas en el artículo 19 de la Ley de Propiedad Horizontal.

CAPÍTULO III. DE LAS NORMAS DE CONVIVENCIA

Artículo 6. Quejas, sugerencias y observaciones.

Todos los propietarios deberán exponer sus quejas, sugerencias y observaciones al Presidente o Administrador de su bloque, quien las hará llegar a la Junta Directiva para adoptar las decisiones oportunas.

Artículo 7. Utilización incorrecta de servicios y elementos comunes.

La utilización de los servicios y elementos comunes de forma contraria a su destino está completamente prohibida.

Además de las sanciones previstas en los artículos 3, 4 y 5, la rotura o deterioro de un elemento común por uso indebido o contrario a su destino dará lugar a la exigencia económica del importe de la factura de reparación de dicho elemento común.

Artículo 8. Tendido de ropa.

Queda prohibido el tendido de ropa en las terrazas principales de las viviendas, debiendo hacerse exclusivamente en los sitios destinados al efecto de cada piso y de forma tal que no produzca molestias a las viviendas inferiores.

Artículo 9. Toldos.

Para la instalación de toldos en las terrazas exteriores se deberá guardar una homogeneidad con el resto de los ya instalados, debiendo ser, al menos, del mismo color, y en caso de que no hubiese instalado ninguno, deberá consultarse previamente a la Junta de Propietarios.

Artículo 10. Períodos de ausencia prolongados.

Los vecinos que se ausentaren durante largo tiempo dejarán las llaves de su vivienda a un familiar o conocido de confianza, o al portero de la finca, para que, en caso de emergencia o fuerza mayor de carácter intempestivo, no sea preciso entrar a la misma por la fuerza.

Artículo 11. Actividades ruidosas y molestas.

Queda prohibido desarrollar actividades que produzcan ruidos y molestias a los vecinos desde las 12 de la noche hasta las 10 de la mañana y de las [HORA] hasta las [HORA] horas (horario de siesta).

Artículo 12. Perros.

Los propietarios que tengan en la Urbanización perros deberán sujetarse a las siguientes normas, además de las reglas dictadas por la autoridad competente:

a) Los perros deberán ir siempre atados y con bozal.

b) Se evitará totalmente que los perros hagan sus necesidades fisiológicas en jardines y otras zonas comunes de la Urbanización.

c) Los perros deberán estar provistos de la correspondiente documentación sanitaria.

d) El propietario deberá evitar que se produzcan ladridos durante las horas de descanso establecidas en el artículo 11 de este Reglamento.

La Junta Directiva, además de imponer las sanciones que correspondan por incumplimiento de estas normas, avisará a los servicios municipales para la recogida de perros que no reúnan los requisitos mencionados.

Artículo 13. Normas de uso de los espacios comunes.

1. Queda prohibido pisar y pasar por lugares no previstos para el paso y especialmente por las zonas ajardinadas.

2. Los juegos de niños se desarrollarán exclusivamente en los lugares destinados al efecto.

3. El paseo en bicicleta se hará únicamente en los lugares donde no se moleste y a velocidad moderada.

4. Queda prohibido desarrollar reuniones y tertulias en voz alta en las plazas de la Urbanización, calles, portales y demás servicios comunes, fuera de las horas señaladas en el artículo 11.

CAPÍTULO IV. DEL SERVICIO DE CALEFACCIÓN

Artículo 14. Fechas y horarios.

El servicio de calefacción se dará en las fechas y horarios que cada año se acuerde por la Junta Directiva.

Como mínimo se tendrá ocho horas diarias desde el [DÍA] de noviembre al [DÍA] de marzo. Para ampliar el servicio bastará el voto de la mayoría de los Presidentes. Para reducirlo será necesaria la unanimidad.

Artículo 15. Conservación y mantenimiento de las instalaciones.

Cada propietario responderá de los defectos internos de su propia vivienda, de conducciones y radiadores, pero a su vez tiene el derecho de recibir un servicio correcto de la central térmica.

Aquellos que tengan defectos de calefacción lo comunicarán por escrito a la empresa de conservación del servicio, la cual tendrá obligación de subsanar el problema en el plazo máximo de tres días. De no ser posible técnicamente, se dará cuenta a la Junta Directiva y al propio interesado para hallar la solución adecuada; si el vicio viene de las instalaciones privativas, se informará al interesado, quien será responsable de esta reparación, cumpliendo exactamente las recomendaciones técnicas de la empresa de conservación.

Artículo 16. Obras en las instalaciones.

Ningún propietario puede hacer reformas de radiadores sin el permiso de la Junta Directiva. A tal fin, se comunicará a la misma el proyecto a realizar y, después de recabar la información técnica oportuna, esta Junta dará o no su aprobación, no pudiendo negar el permiso si las obras no suponen variación o perjuicio para otros copropietarios. Obtenida la autorización, las obras se realizarán ajustándose estrictamente a las recomendaciones técnicas, siendo responsable de ello el propietario.

La realización de obras sin permiso, o su realización de manera distinta a la autorizada, darán lugar a restituir las cosas a su estado primitivo, sin perjuicio de lo establecido en los artículos 3, 4 y 5 de este Reglamento y de cualquier acción que corresponda a los comuneros, a cada Comunidad o a la Urbanización.

Artículo 17. Obligación de paso.

Todo propietario tiene obligación de permitir la entrada a su vivienda, tanto para comprobaciones técnicas como para las reparaciones que sean necesarias en su domicilio en orden al buen funcionamiento general de este servicio.

CAPÍTULO V. DEL USO DE ASCENSORES

Artículo 18. Condiciones técnicas.

Cada bloque tiene unos elevadores, tanto de subida como de bajada, que deberán reunir en cada momento los requisitos que establezcan las normas legales correspondientes, además de las siguientes cuando no sean contradictorias con las primeras.

Artículo 19. Condiciones de uso.

1. En ningún caso se podrá sobrepasar la capacidad indicada en cada uno de ellos, ni en peso total ni en número de personas, exigiéndose las responsabilidades correspondientes a que hubiera lugar en caso de uso abusivo de estos ascensores.

2. No podrán utilizar estos ascensores los menores de 14 años sin ir acompañados de personas mayores.

3. No se podrán transportar en ellos objetos, paquetes o bultos cuyo peso sobrepase el límite de capacidad o que por su tamaño y características sean susceptibles de causar daños o deterioros.

4. No podrán utilizarse los elevadores para transportes de materiales de obras y tampoco para hacer traslados de muebles. En ningún caso se podrá ocupar el ascensor de forma permanente o continuada, dejando sin servicio al resto de los vecinos.

Artículo 20. Cuidado y vigilancia de los ascensores.

Del cuidado y vigilancia de los ascensores se encargará exclusivamente el conserje o el encargado de la Urbanización, a los efectos de avisar a la empresa de conservación, dando cuenta al Presidente y Administrador de cada bloque de los problemas que puedan existir para la adopción de las medidas oportunas. Ningún propietario o inquilino podrá manipular en su mecanismo en caso de mal funcionamiento, debiendo avisar a dichos empleados y, en su caso, a la empresa de mantenimiento.

Artículo 21. Conservación y mantenimiento de los ascensores.

Para el buen cuidado de los ascensores y los debidos engrases periódicos se concertará el correspondiente contrato con una casa especializada en tal cometido.

CAPÍTULO VI. DE LA UTILIZACIÓN DE PISCINAS

Artículo 22. Calendario de apertura.

Las piscinas de la Urbanización se abrirán normalmente el [DÍA] de junio hasta el [DÍA] de septiembre.

La Junta Directiva está facultada para que, atendiendo a las opiniones recogidas y a la vista del tiempo existente, pueda atrasar o adelantar el periodo de funcionamiento, adoptando el acuerdo por régimen de mayoría.

Artículo 23. Horario de uso.

De la misma manera, por régimen de mayoría, se establecerá el horario de uso, el tiempo destinado a clases de natación, prácticas y campeonatos, así como otras actividades sociales.

Artículo 24. Condiciones de acceso.

Para la entrada en el recinto de la piscina será totalmente necesario, caso de así disponerlo la Junta Directiva por acuerdo mayoritario, presentar el carné, emblema o distintivo que para cada temporada se fije.

Estos distintivos se facilitarán a toda persona que conviva de forma continuada con el cabeza de familia (propietario o quien ocupe con consentimiento del mismo el piso o local), siempre que tengan más de 8 años o que vayan acompañados de personas mayores.

Para el cumplimiento de lo anterior, todo propietario facilitará a la Junta Directiva, a través del Presidente o Administrador de bloque, relación de personas, indicando parentesco, a fin de poder hacer para cada uno el distintivo correspondiente.

Para el acceso y permanencia en la piscina tendrá que llevarse ropa adecuada, concretamente se prohíbe utilizar otra ropa que no sea el traje de baño y camisa o similar y siempre con zapatillas de baño.

Artículo 25. Normas de uso.

En el interior del recinto de la piscina se tendrán en cuenta con carácter obligatorio las siguientes normas:

1. Es obligatorio el uso de gorro de baño para toda persona que tenga el cabello largo.

2. Queda prohibido celebrar juegos de pelota, balones y cualquier otro que lleve consigo molestias para el resto de los usuarios.

3. Queda prohibido consumir comidas y bebidas dentro del recinto de la piscina y, asimismo, depositar toda clase de desperdicios y objetos en la misma.

4. Se prohíbe la entrada de cualquier perro y otro animal en el recinto, aunque sea atado y con bozal.

5. Se atenderán en todo momento las instrucciones del socorrista de la piscina, el cual queda autorizado para expulsar del recinto a las personas que puedan ocasionar, con su comportamiento, problemas y peligros para el resto de usuarios.

CAPÍTULO VII. DE LA UTILIZACIÓN DE LAS PISTAS DE TENIS

Artículo 26. Calendario de apertura y horario de uso.

Las pistas de tenis estarán abiertas durante todo el año y con el siguiente horario: de [HORA] a [HORA] horas.

Artículo 27. Condiciones de acceso.

Tienen derecho a su utilización los propietarios o usuarios de las viviendas y locales, así como sus familiares. Podrán jugar con personas ajenas a la Urbanización, en calidad de invitados, siempre y cuando, como mínimo, la mitad de los jugadores tengan la condición de residentes en la Urbanización.

Los niños menores de [EDAD] años no podrán utilizar las pistas sin estar acompañados de mayores, salvo en aquellos momentos en que no haya peticiones previas y se encuentren vacías.

Cada propietario tendrá derecho a solicitar la utilización de la pista [PERIODO MÁXIMO DE USO] al día como máximo, salvo que las instalaciones estén libres.

El encargado de las pistas, que será un empleado de la Urbanización, dispondrá de una lista con el consiguiente cuadro de horarios a fin de que puedan inscribirse los interesados que deseen jugar.

CAPÍTULO VIII. DE LOS EMPLEADOS DE LA URBANIZACIÓN

Artículo 28. Dirección y control de los empleados.

El poder de dirección y control de los empleados será ejercido por la Junta Directiva. Queda prohibido todo tipo de discusión o queja directamente a los empleados, siendo el sistema el de dar cuenta al Presidente o Administrador del bloque, conforme al artículo 6 de este Reglamento.

Será la Junta Directiva, a través de sus órganos, quien dará instrucciones, reconocimientos o sanciones a las personas contratadas.

CAPÍTULO IX. DEL SERVICIO DE BASURAS

Artículo 29. Horarios de recogida.

El horario de bajada de basuras individuales a los cubos existentes será de [HORA] a [HORA] horas, estando fuera de este horario cerrados dichos cuartos y quedando prohibido bajar los desperdicios en horario distinto o depositar bolsas u otro tipo de recipientes fuera del lugar destinado al efecto.

Atendiendo al horario de recogida por los servicios municipales, la Junta Directiva queda facultada para cambiar estos horarios por acuerdo mayoritario.

Artículo 30. Condiciones de depósito de la basura.

Las basuras individuales deberán ser bajadas siempre en bolsas de plástico cerradas u otro sistema similar, quedando prohibido utilizar otros recipientes que no reúnan las características de seguridad y cerramiento, depositándolas únicamente dentro de los cubos colectivos.

CAPÍTULO X. DE LA UTILIZACIÓN DE SERVICIOS COMUNES POR INVITADOS

Artículo 31. Condiciones de uso.

Para la utilización de servicios y elementos comunes por invitados de los propietarios u ocupantes de viviendas o locales deberá tenerse en cuenta, como regla principal, que este disfrute estará siempre supeditado a que sea posible y que no prive en ningún momento de los derechos de todos y cada uno de los propietarios o residentes en la Urbanización.

La Junta Directiva fijará cada año, por mayoría, las normas para invitados, número posible de cada servicio, máximo por cada propietario, etc., notificándose a los comuneros por escrito.

CAPÍTULO XI. DE LAS VIVIENDAS Y LOCALES QUE SON ARRENDADOS O CEDIDOS

Artículo 32. Comunicación de datos.

Reiterando en su totalidad las obligaciones de los propietarios que vienen reflejadas en los Estatutos de la Comunidad, cada propietario estará obligado a dar cuenta al Presidente o Administrador de su bloque de la persona y demás datos del arrendatario o cesionario del piso o local, pues, de no mediar esta comunicación, el ocupante carecerá de derecho para el uso y disfrute de los servicios y elementos comunes.

En esta comunicación, que el Presidente o Administrador del bloque trasladará a la Junta Directiva, el arrendatario o cesionario hará constar que conoce y acepta los Estatutos de la Urbanización, los de su propio bloque y este Reglamento de Régimen Interior, comprometiéndose a su cumplimiento, sin perjuicio de las acciones que, en su caso, deriven contra el propietario por la Comunidad.

Artículo 33. Responsabilidad.

La Urbanización, a través de los órganos representativos de la Comunidad, podrá exigir a los ocupantes los daños y perjuicios ocasionados e imponer las sanciones previstas en este Reglamento, sin perjuicio de la responsabilidad directa del propietario conforme a lo previsto en los Estatutos y, naturalmente, ejercitar las acciones previstas en la Ley de Propiedad Horizontal, el Código Civil y demás normas legales.
