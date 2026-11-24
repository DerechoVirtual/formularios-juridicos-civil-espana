---
name: escrito-paralizar-ejecucion-hipotecaria-desahucio-civ-1444
description: "Escrito para paralizar la ejecución hipotecaria y el desahucio de la vivienda habitual. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito para paralizar la ejecución hipotecaria y el desahucio de la vivienda habitual

> Formulario **CIV-1444** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Escrito elaborado por el Consejo General de la Abogacía Española dirigido al órgano judicial competente para que acuerde la suspensión inmediata del desahucio de la vivienda sujeta al préstamo hipotecario.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito para paralizar la ejecución hipotecaria y el desahucio de la vivienda habitual» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito para paralizar la ejecución hipotecaria y el desahucio de la vivienda habitual” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:escrito-paralizar-ejecucion-hipotecaria-desahucio-civ-1444`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NÚMERO (3 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] C.P.
- [ ] DNI/NIE
- [ ] DOMICILIO A EFECTOS DE NOTIFICACIONES
- [ ] FECHA
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº
- [ ] SEDE

## Normas que cita el formulario

- art. 3.1 Código Civil
- art. 695 LEC

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

- Junto a «… [NÚMERO] A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) Escrito elaborado por la Abogacía Española y puesto a disposición de los ciudadanos afectados por desahucio para solicitar al tribunal competente la suspensión inmediata de la ejecución hipotecaria.

En el mismo se requiere al tribunal la paralización de la ejecución hipotecaria hasta la modificación de la ley procesal por el Gobierno y a raíz de la sentencia del Tribunal de Justicia de la UE sobre cláusulas abusivas.

Este escrito se ha puesto a disposición de los ciudadanos y asociaciones de consumidores en la web del CGAE (www.abogacia.es) y en los diferentes Colegios territoriales.

========================================================================


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

Tribunal de Instancia nº [NÚMERO]

Ejecución hipotecaria n.º [NÚMERO]

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

[OPCIONAL — incluir si procede]

(SI LO PRESENTA DIRECTAMENTE EL CIUDADANO)

D./Dña. [NOMBRE Y APELLIDOS], con DNI n.º [DNI/NIE], en su propio nombre y derecho, con domicilio a efectos de notificaciones en [DOMICILIO A EFECTOS DE NOTIFICACIONES], C.P. [C.P.], localidad de [LOCALIDAD], ante el Tribunal y como mejor proceda en Derecho, DIGO:

[OPCIONAL — incluir si procede]

(SI LO PRESENTA A TRAVÉS DE PROCURADOR)

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales y de [NOMBRE DEL REPRESENTADO/A], según tengo acreditado en el procedimiento de ejecución hipotecaria n.º [NÚMERO], ante el Tribunal y como mejor en Derecho proceda, DIGO:

Que mediante el presente escrito interesamos la suspensión inmediata de las presentes actuaciones, en base a las siguientes,

ALEGACIONES

PRIMERO. EMERGENCIA SOCIAL Y ALARMA SOCIAL

Es un hecho manifiesto y notorio que el presente procedimiento de ejecución hipotecaria se enmarca una situación de emergencia social causada por las más de 400.000 ejecuciones hipotecarias que se han producido en España desde 2007, como resultado de la actividad antisocial de las entidades financieras y de una legislación injusta.

La alarma social generada por esta situación se ha hecho aún más evidente en las últimas semanas, en las que el drama de las ejecuciones hipotecarias ha irrumpido con mayor fuerza en primera línea de la actualidad.

Esta situación de emergencia social ha sido reconocida por la propia Asociación Española de Banca, que en un comunicado hecho público el pasado día 12 de noviembre, se hace eco de la «alarma social generada por los desahucios hipotecarios», y expone el «compromiso de las entidades miembros de la AEB, por razones humanitarias y en el marco de su política de responsabilidad social, de paralizar los lanzamientos durante los dos próximos años, en aquellos casos en que concurran circunstancias de extrema necesidad». De igual modo la CECA ha acordado suspender la ejecución de desahucios de vivienda habitual de colectivos especialmente vulnerables hasta la entrada en vigor de la reforma normativa anunciada por las autoridades.

El presidente del Gobierno también ha reconocido el carácter extraordinario de la situación social generada por los procedimientos de ejecución hipotecaria, manifestando que «estamos viendo cosas terribles, inhumanas» y que estudia «paralizar los desahucios que afectan a las familias más vulnerables».

El sindicato de policía SUP ha expresado que apoyará y respaldará jurídicamente a los policías que se nieguen a participar en desahucios.

El presidente del Consejo General del Poder Judicial ha manifestado que los jueces pueden actuar para «suspender, paralizar, modificar o adaptar la decisión judicial al caso concreto» amparándose tanto en normativas comunitarias como en principios constitucionales o de derecho contractual, máxime cuando se trata de situaciones «de verdadera crispación o de atentado a un derecho fundamental como es el de la vivienda».

Jueces para la Democracia ha hecho un llamamiento a los jueces para que «suspendan automáticamente todos los desahucios».

Desde el Foro Judicial Independiente se «recomienda a los miembros de la carrera judicial con competencias en la materia la suspensión de todos los procedimientos de ejecución hipotecaria pendientes de tramitación en los juzgados de toda España».

Recientemente desde la Asociación Profesional de la Magistratura se afirmaba que «Las entidades han convertido los tribunales en sus oficinas recaudatorias» y que se trata de «de una situación preocupante y muy dolorosa. Un drama social».

Y el presidente del Consejo General de la Abogacía Española ha expuesto también su posición de una forma rotunda: «No más desahucios por impago de deudas hipotecarias».

Las anteriores manifestaciones son prueba de que existe una auténtica alarma social en materia de desahucios, alarma concretada en los 400.000 desahucios que se han producido en los años de la crisis económica, y en los miles que se están tramitando en los tribunales españoles; esta trágica situación ha de ser tenida en cuenta a la hora de interpretar las normas vigentes pues, de conformidad con lo establecido en el artículo 3.1 del Código Civil, las normas jurídicas han de interpretarse con arreglo «a la realidad social del tiempo en que de ser aplicadas», lo que en el tiempo presente exige una clara visión pro ciudadano.

SEGUNDO. VIOLACIÓN SISTEMÁTICA DE LOS DERECHOS HUMANOS: EL DERECHO A UNA VIVIENDA ADECUADA

Las Plataformas de Afectados por la Hipoteca y diferentes entidades de la sociedad civil han denunciado reiteradamente que los procedimientos de ejecución hipotecaria masivos constituyen una violación sistemática de derechos humanos puesto que sitúan a la persona ejecutada en una situación de absoluta indefensión.

Corresponde al juzgador interpretar las normas relativas a derechos fundamentales que la Constitución Española reconoce de conformidad con la Declaración Universal de Derechos Humanos y los tratados y acuerdos internacionales sobre las mismas materias ratificados por España (art. 10.2 CE). Los derechos humanos están llamados para que resulten efectivos y no meramente ilusorios.

La vulneración del derecho a la tutela judicial efectiva en las ejecuciones hipotecarias masivas llevadas a cabo por las entidades financieras también vulnera el derecho de las personas a disfrutar de una vivienda digna y adecuada (art. 47 CE). Se trata de un derecho humano consagrado en el Pacto Internacional de Derechos Económicos, Sociales y Culturales (PIDESC), ratificado por España y que forma parte del ordenamiento interno español (art. 96.1 CE), y que en su art. 11.1 establece que los Estados se comprometen a tomar las medidas necesarias para realizar «el derecho de toda persona a un nivel de vida adecuado para sí y su familia, incluso (...) vivienda adecuados, y a una mejora continua de las condiciones de existencia. Los Estados Partes tomarán medidas apropiadas para asegurar la efectividad de este derecho, reconociendo a este efecto la importancia esencial de la cooperación internacional fundada en el libre consentimiento.»

Las referidas ejecuciones hipotecarias masivas en el actual entorno de crisis económica-financiera y con alta tasa de desempleo que imposibilita a las personas costear la financiación de sus viviendas, conllevan a la práctica de desalojos forzosos, con igual carácter masivo, incompatibles con las normas del PIDESC y su realización conculca gravemente otros derechos fundamentales como «violaciones de derechos civiles y políticos, tales como el derecho a la vida, el derecho a la seguridad personal, el derecho a la no injerencia en la vida privada, la familia y el hogar, y el derecho a disfrutar en paz de los bienes propios», según indica en su Observación General n° 7 el Comité de Derechos, Económicos, Sociales y Culturales, que constituye el intérprete autorizado del Pacto homónimo en el plano internacional y cuya interpretación debe ser tenida en cuenta ya que comprende las «condiciones de vigencia» de este instrumento. La referida Observación general expresa que «el término «desalojos forzosos» se define como «el hecho de hacer salir a personas, familias y/o comunidades de los hogares y/o las tierras que ocupan, en forma permanente o provisional, sin ofrecerles medios apropiados de protección legal o de otra índole ni permitirles su acceso a ellos»

Según el Informe de la Relatora Especial sobre una vivienda adecuada, Raquel Rolnik (Naciones Unidas A/67/286 Asamblea General) de fecha 10 de agosto de 2012 «en España se han ejecutado más de 350.000 hipotecas desde 2007, y en 2011 tuvieron lugar aproximadamente 212 ejecuciones y 159 desalojos al día. La crisis ha afectado desproporcionadamente a los más pobres y vulnerables, que fueron los últimos en ingresar en los mercados hipotecarios y los primeros en sufrir las consecuencias de las crisis en razón de su escasa resiliencia a las conmociones económicas y su poca capacidad de pago. Algunas investigaciones recientes indican que la mayor parte (el 70%) de los impagos registrados en España guarda relación con la crisis del empleo y que el 35% de las propiedades ejecutadas pertenecen a migrantes.".

De acuerdo con los últimos datos del CGPJ en su informe «efectos de la crisis en los órganos judiciales» en el segundo semestre de 2012 se han iniciado más de 50.000 procesos de ejecución hipotecaria por lo que se superarán las 400.000 ejecuciones hipotecarias desde el inicio de la crisis.

La violación del derecho a la tutela judicial efectiva y a un procedimiento con todas las garantías sería a su vez constitutivo de una violación de derechos fundamentales de las personas de la que podría devenir responsabilidad del Estado por violación sistemática de los derechos humanos, puesto que la mencionada violación se deriva de la aplicación del derecho interno y por la aplicación masiva ante la que nos encontramos.

TERCERO. NORMATIVA DE CONSUMIDORES

La hipoteca que se ejecuta fue otorgada a una persona física para la adquisición de una vivienda por lo que goza de la condición de consumidor según establece el Art. 3 del Real Decreto Legislativo 1/2007, de 16 de noviembre, por el que se aprueba el texto refundido de la Ley General para la Defensa de los Consumidores y Usuarios y otras leyes complementarias (en adelante ROL 1/2007).

De la lectura del artículo 51 en relación con el 53.3 CE se concluye que la defensa de los consumidores y usuarios ha de considerarse un principio general informador del ordenamiento jurídico en un doble sentido: por una parte, obligando al legislador a adoptar las medidas normativas precisas y, por otra, atribuyendo a los órganos encargados de aplicarlas el deber de interpretar las normas en un sentido favorable a los legítimos intereses de los mismos. Y este principio se ve reforzado cuando los derechos del consumidor guardan relación directa con un bien o servicio de uso común, ordinario y generalizado, como es el caso de los préstamos con garantía hipotecaria y más cuando son otorgados con la garantía de la vivienda familiar. La defensa de los consumidores y usuarios es, en consecuencia, una de las exigencias que derivan del componente social de nuestro Estado de Derecho que, en palabras del Tribunal Constitucional en STC 123/1992, de 28 de septiembre, cuya tendencia siguen otras STC 98/1993 y STC 177/1993«...significa una acción tuitiva del más débil o desvalido cuando surge un conflicto en el cual la prepotencia del contrario le haría ser siempre el perdedor, para conseguir así la igualdad real o efectiva de individuos y grupos, a la cual encamina el artículo 9 de la Constitución y, con ella, la justicia.»

Debiendo señalar para finalizar que tal y como se indicó en la STC 12/1994, de 17 de enero, FJ 6, nuestro texto constitucional no consagra derechos meramente teóricos o ilusorios, sino reales y efectivos.

CUARTO. ALEGACIÓN NULIDAD DE CLÁUSULAS ABUSIVAS DE EJECUCIÓN HIPOTECARIA. APLICACIÓN SENTENCIA TJUE 14-03-2013.-

La regulación actual del procedimiento de ejecución hipotecaria español ha sido objeto de numerosas críticas desde múltiples sectores jurídicos, principalmente dada la indefensión en la que sitúa al ejecutado.

Estas dudas jurídicas se plantearon por el Tribunal Mercantil nº 3 de Barcelona ante el Tribunal de Justicia de la Unión Europea, a fin de que valorara si el sistema de ejecución hipotecario español respetaba los parámetros mínimos que exige la normativa comunitaria de tutela de consumidores y usuarios, y dio origen a la cuestión prejudicial C415/2011. La STJUE de 14 de marzo de 2013, C-415/2011, ha confirmado que la legislación española de ejecuciones hipotecarias, artículos 695 y siguientes de la LEC, vulnera la normativa comunitaria de protección de consumidores y usuarios al no permitir la alegación por el ejecutado de la existencia de cláusulas abusivas.

Se planteó al TJUE si el sistema de ejecución de títulos judiciales sobre bienes hipotecados o pignorados, establecido en el artículo 695 y siguientes de la Ley de Enjuiciamiento Civil, con sus limitaciones en cuanto a los motivos de oposición previsto en el ordenamiento procesal español, no sería sino una limitación clara de la tutela del consumidor por cuanto supone formal y materialmente una clara obstaculización al consumidor para el ejercicio de acciones o recursos judiciales que garanticen una tutela efectiva de sus derechos.

Asimismo, en la cuestión prejudicial se requería al Tribunal de Justicia de la Unión Europea a fin de que pudiera dar contenido al concepto de desproporción de la normativa de consumidores a la posibilidad de vencimiento anticipado en contratos proyectados en un largo lapso de tiempo por incumplimientos en un periodo muy concreto, a la fijación de intereses de demora abusivos, y a la fijación de mecanismos de liquidación de los intereses variables realizados unilateralmente por el prestamista vinculados a la posibilidad de ejecución hipotecaria, dado que no permiten al deudor ejecutado que articule su oposición a la cuantificación de la deuda en el propio procedimiento ejecutivo, remitiéndole a un procedimiento declarativo en el que cuando haya obtenido pronunciamiento definitivo la ejecución habrá concluido o, cuando menos, el deudor habrá perdido el bien hipotecado o dado en garantía, cuestión de especial trascendencia cuando el préstamo se solicita para adquirir una vivienda y la ejecución determina el desalojo del inmueble.

La Comisión Europea en su informe de febrero de 2012, aportado al procedimiento, advertía que la LEC no respeta el derecho comunitario si mantiene un sistema de oposición por cláusulas abusivas que sólo se puede activar una vez efectuado el lanzamiento al deudor, y si los Intereses moratorios que se pudieran aplicar al deudor fueran desproporcionados.

Las conclusiones de la Abogada General del TJUE, presentadas el 8 de noviembre de 2012, son contundentes al sostener que la normativa española sobre ejecuciones hipotecarias vulnera la normativa comunitaria, dado que es incompatible con la Directiva 93/13/CEE del Consejo, de 5 de abril de 1993, sobre las cláusulas abusivas en los contratos celebrados con consumidores. Estima que no supone una protección efectiva contra las cláusulas abusivas del contrato que el consumidor que pretende instar la nulidad de las cláusulas deba soportar sin posibilidad de defensa la ejecución hipotecaria, la subasta de la vivienda y el desalojo de la misma, y que solo con posterioridad esté legitimado para ejercitar la acción de daños y perjuicios. La Directiva europea exige que el consumidor disponga de un recurso legal eficaz para demostrar el carácter abusivo de las cláusulas del préstamo que permita detener la ejecución forzosa. Considera que la efectividad de los derechos reconocidos por la Directiva exige que el órgano judicial que conoce del procedimiento declarativo deba disponer de la posibilidad de suspender de forma provisional el procedimiento ejecutivo, con objeto de detener la ejecución forzosa, hasta que se haya comprobado el carácter abusivo de una cláusula contractual, de modo que se impida que el procedimiento ejecutivo cree en perjuicio del consumidor una situación como la pérdida de la vivienda que posteriormente sea de muy difícil o imposible reparación.

El Tribunal responde que la Directiva sobre las cláusulas abusivas se opone a una normativa nacional, como la española, que no permite al juez que conozca del proceso declarativo (el que tiene por objeto declarar el carácter abusivo de una cláusula) adoptar medidas cautelares, en particular la suspensión del procedimiento de ejecución, cuando sean necesarias para garantizar la plena eficacia de su decisión final.

En efecto, consta en autos que el sistema procesal español prohíbe al juez que conoce de un proceso declarativo vinculado al procedimiento de ejecución hipotecaria adoptar medidas cautelares que garanticen la plena eficacia de su decisión final, no sólo cuando aprecie el carácter abusivo, con arreglo al artículo 6 de la Directiva, de una cláusula contenida en un contrato celebrado entre un profesional y un consumidor, sino también cuando compruebe que esa cláusula resulta contraria a las normas nacionales de orden público, lo que le corresponde a él verificar.

(...)

Por consiguiente, procede declarar que un régimen procesal de este tipo, al no permitir que el juez que conozca del proceso declarativo, ante el que el consumidor haya presentado una demanda alegando el carácter abusivo de una cláusula contractual que constituye el fundamento del título ejecutivo, adopte medidas cautelares que puedan suspender o entorpecer el procedimiento de ejecución hipotecaria, cuando acordar tales medidas resulte necesario para garantizar la plena eficacia de su decisión final, puede menoscabar la efectividad de la protección que pretende garantizar la Directiva (véase, en este sentido, la sentencia de 13 de marzo de 2007, Unibet, C-432/05, Rec. p. I-2271, apartado 77).

(...)

Así ocurre con mayor razón cuando, como en el litigio principal, el bien que constituye el objeto de la garantía hipotecaria es la vivienda del consumidor perjudicado y de su familia, puesto que el mencionado mecanismo de protección de los consumidores, limitado al pago de una indemnización por daños y perjuicios, no es adecuado para evitar la pérdida definitiva e irreversible de la vivienda.

(...)

En estas circunstancias, procede declarar que la normativa española controvertida en el litigio principal no se ajusta al principio de efectividad, en la medida en que hace imposible o excesivamente difícil, en los procedimientos de ejecución hipotecaria iniciados a instancia de los profesionales y en los que los consumidores son parte demandada, aplicar la protección que la Directiva pretende conferir a estos últimos.

La sentencia dictada por el TJUE vincula a los demás tribunales que conozcan de un problema similar

El TJ considera que el régimen procesal español menoscaba la efectividad de la protección que pretende garantizar la Directiva, lo que sucede en todos casos en que la ejecución del inmueble se lleva a cabo antes de que el juez que conozca del proceso declarativo declare abusiva la cláusula contractual en la que se basa la hipoteca y, en consecuencia, la nulidad del proceso de ejecución, que sólo permitiría garantizar una protección al consumidor meramente indemnizatoria, a todas resultas incompleta e insuficiente pues no evitaría la pérdida definitiva e irreversible de la vivienda. Así, el TJ declara que la normativa española no se ajusta al principio de efectividad, en la medida en que hace imposible o excesivamente difícil, en los procedimientos de ejecución hipotecaria aplicar la protección que la Directiva confiere a los consumidores.

Por otro lado, el TJ al examinar el concepto de cláusula abusiva recuerda que el desequilibrio importante creado por éstas debe apreciarse teniendo en cuenta las normas aplicables en Derecho nacional cuando no exista un acuerdo de las partes en ese sentido.

En el presente caso, como consta en el declarativo interpuesto y pendiente ante el Tribunal se han instado la nulidad de las cláusulas de la escritura hipotecaria referentes a (Cláusula de intereses de demora. Cláusula relativa al vencimiento anticipado. Cláusula relativa a la liquidación unilateral de la deuda impagada), ya que si continuara la ejecución se produciría un perjuicio irreparable.

Procede entonces que declare la suspensión de la ejecución hipotecaria, como medida cautelar, hasta que decida sobre la consideración y, en su caso, la nulidad de las cláusulas de la hipoteca.

QUINTO. VULNERACIÓN DEL DERECHO DE TUTELA JUDICIAL EFECTIVA

A resultas de lo planteado, y habiendo sido el procedimiento de ejecución hipotecaria de España considerado por el TJUE contrario a la normativa sobre consumidores, se estaría vulnerando el derecho a la tutela judicial efectiva, al derecho de defensa de los deudores hipotecados y a la prohibición de indefensión, y es imperativa para el juzgador la protección de derechos fundamentales en el procedimiento y su actuación urgente.

Por todo ello,

SOLICITO AL TRIBUNAL:

Que tenga por presentado el escrito y por realizadas las manifestaciones contenidas en el cuerpo del mismo acordando la suspensión inmediata del mismo hasta en tanto en cuanto no se lleve a cabo la modificación en la Ley procesal que permita el planteamiento de motivos de oposición basado en la existencia de cláusulas abusivas o, subsidiariamente la declaración de nulidad de actuaciones y petición de retroacción al momento procesal de admisión de la demanda.

Por ser justicia que pido en [LUGAR], a [FECHA].

OTROSÍ DIGO PRIMERO: Que para el supuesto de que SSª considerara que este escrito debe ser presentado por Abogado/a y procurador me sea notificada dicha resolución, y sea igualmente suspendido el procedimiento a los efectos de solicitud de Justicia Gratuita o presentación por el letrado de oficio que pudiera representarme.

Por ello,

SOLICITO: Que tenga por hechas las manifestaciones anteriores, a los efectos oportunos y acuerde de conformidad.

OTROSÍ DIGO SEGUNDO: Que dado que la presente petición se formula amparándose en el incumplimiento del Estado español de una normativa comunitaria que en modo alguno me puede ser imputada, que en tanto en cuando se mantengan las causas de suspensión ello no me suponga mayores perjuicios derivados de la continuidad en el devengo de los intereses moratorios.

Por ello, nuevamente,

SOLICITO: Que tenga por hechas las manifestaciones anteriores, a los efectos oportunos y acuerde de conformidad.

Firma del solicitante	Firma de Procurador/a
