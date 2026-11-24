---
name: demanda-contra-declaracion-no-idoneidad-adoptar-civ-0137
description: "Demanda contra la declaración de no idoneidad para adoptar. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda contra la declaración de no idoneidad para adoptar

> Formulario **CIV-0137** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Al Tribunal Comparecencia, representación y asistencia letrada Interposición de demanda de oposición a la declaración de inidoneidad HECHOS FUNDAMENTOS DE DERECHO Suplico Otrosí digo Lugar y fecha Firmas

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda contra la declaración de no idoneidad para adoptar» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda contra la declaración de no idoneidad para adoptar” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-contra-declaracion-no-idoneidad-adoptar-civ-0137`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] MES (8 veces)
- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] AÑO (6 veces)
- [ ] DÍA (6 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] ÓRGANO ADMINISTRATIVO (3 veces)
- [ ] CALLE (2 veces)
- [ ] FECHA (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] COLEGIO
- [ ] LUGAR
- [ ] Nº
- [ ] ÓRGANO O PERSONA

## Normas que cita el formulario

- art. 779 LEC
- art. 780.1 LEC
- art. 779.I LEC
- art. 750.1 LEC
- art. 780 LEC
- art. 753 LEC
- art. 3.2 LO 1/2025
- art. 176 CC
- art. 176.3 CC
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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…CIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA NÚMERO DE [LOCALIDAD]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.

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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA NÚMERO DE [LOCALIDAD]

D./Dª [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en nombre y representación de D./Dª [NOMBRE Y APELLIDOS], cuya representación acreditaré cuando sea requerido para ello mediante comparecencia apud acta (o bien: representación que acredito mediante copia de poder especial para pleitos que presento, la cual solicito me sea devuelta tras su testimonio inicial en autos, por necesitarla para otros usos), bajo la dirección técnica de D./Dª [NOMBRE Y APELLIDOS], Letrado del Ilustre Colegio de [COLEGIO], con despacho profesional en calle [CALLE], ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que por medio del presente escrito, siguiendo instrucciones expresas de mi representado/a y dentro del plazo de veinte días concedido mediante diligencia de ordenación de fecha [DÍA] de [MES] de [AÑO], interpongo, con base en lo dispuesto en los arts. 779 y 780 LEC, DEMANDA DE OPOSICIÓN A LA RESOLUCIÓN ADMINISTRATIVA dictada en fecha [DÍA] de [MES] de [AÑO] por [ÓRGANO ADMINISTRATIVO] de la Comunidad Autónoma de [LOCALIDAD] por la que se declara la no idoneidad de mi representado/a en el expediente de adopción nacional/internacional número [NÚMERO], conforme a los siguientes

HECHOS

PRIMERO.- En fecha [DÍA] de [MES] de [AÑO] por [ÓRGANO ADMINISTRATIVO] de la Comunidad Autónoma de [LOCALIDAD] se dictó resolución en el expediente de adopción nacional/internacional número [NÚMERO], en el que se declaró la inidoneidad de mi representado/a, por no ser su motivación la adecuada para la adopción de acuerdo con los informes psicosociales recabados por el citado organismo. La citada resolución fue notificada a mi representado en fecha [FECHA] de [MES] de

Se acompaña como Documento Nº [Nº DE DOCUMENTO], testimonio de la citada resolución.

SEGUNDO.- Mediante escrito de fecha [FECHA] de [MES] dentro del plazo de dos meses desde la notificación de la resolución, mi representado/a presentó ante este Tribunal un escrito inicial en el que sucintamente expresaba su pretensión de oponerse a la citada declaración, conforme a lo establecido en el art. 780.1 y 2 LEC.

TERCERO.- Recibido testimonio completo del expediente administrativo, del que se dio traslado a mi representado/a, el Letrado de la Administración de Justicia lo/la emplazó para que antes de que transcurrieran veinte días presentara la correspondiente demanda, lo que efectúa mediante el presente escrito.

CUARTO.- Mi representado/a se opone a dicha declaración de inidoneidad con base en que no se encuentra en absoluto justificada.

En el informe psicosocial emitido por D./Dª [NOMBRE Y APELLIDOS] y D./Dª [NOMBRE Y APELLIDOS], psicólogo y trabajador social, respectivamente, en fecha [DÍA] de [MES] de [AÑO], que tuvo presente la resolución administrativa impugnada, se señala que la motivación de mi representado/a para la adopción no estaba correctamente fundamentada, minimizando las dificultades que puede conllevar y orientando la adopción a cubrir un vació personal.

Por otra parte, se incurre, en el mismo, en las siguientes contradicciones:

QUINTO.- Al estar mi representado/a totalmente en desacuerdo con dicha valoración, solicitó, por iniciativa propia, asesoramiento e informe a otro gabinete privado, que ha valorado favorablemente su aptitud para la adopción.

Se acompaña, como DOCUMENTO Nº [Nº DE DOCUMENTO], informe favorable a su idoneidad para la adopción, y se ofrece, para su práctica en el momento oportuno, de considerarlo conveniente el Juez, prueba testifical de las personas que han elaborado el citado informe: D./Dª [NOMBRE Y APELLIDOS] y D./Dª [NOMBRE Y APELLIDOS], con domicilio profesional en [LOCALIDAD], calle [CALLE], núm. [Nº], puerta

Resultan aplicables a los anteriores hechos, los siguientes

FUNDAMENTOS DE DERECHO

I. COMPETENCIA.- La competencia corresponde a este Tribunal, conforme al art. 779.II LEC.

II. LEGITIMACIÓN.- Ostenta legitimación activa mi representado/a, declarado/a inidóneo/a para la adopción, y legitimación pasiva, la entidad pública que dictó la resolución en que se contiene dicha declaración.

III. REPRESENTACIÓN Y DEFENSA.- El/La demandante se halla debidamente representado/a y asistido/a por el Procurador y Letrado señalados al inicio, tal y como exige el art. 750.1 LEC.

IV. PROCEDIMIENTO. De acuerdo con el artículo 780 LEC, en relación con el artículo 753 LEC, la presente oposición debe sustanciarán por los trámites del juicio verbal.

Dispone el art. 780 LEC: “1. No será necesaria reclamación previa en vía administrativa para formular oposición, ante los Tribunales civiles, a las resoluciones administrativas en materia de protección de menores. La oposición a las mismas podrá formularse en el plazo de dos meses desde su notificación.

Estarán legitimados para formular oposición a las resoluciones administrativas en materia de protección de menores, siempre que tengan interés legítimo y directo en tal resolución, los menores afectados por la resolución, los progenitores, tutores, acogedores, guardadores, el Ministerio Fiscal y aquellas personas que expresamente la ley les reconozca tal legitimación. Aunque no fueran actores podrán personarse en cualquier momento en el procedimiento, sin que se retrotraigan las actuaciones.

Los menores tendrán derecho a ser parte y a ser oídos en el proceso conforme a lo establecido en la Ley Orgánica de Protección Jurídica del Menor. Ejercitarán sus pretensiones en relación a las resoluciones administrativas que les afecten a través de sus representantes legales siempre que no tengan intereses contrapuestos a los suyos, o a través de la persona que se designe como su defensor para que les represente.

2. El proceso de oposición a una resolución administrativa en materia de protección de menores se iniciará mediante la presentación de un escrito inicial en el que el actor sucintamente expresará la pretensión y la resolución a que se opone.

En el escrito consignará expresamente la fecha de notificación de la resolución administrativa y manifestará si existen procedimientos relativos a ese menor.

3. El Letrado de la Administración de Justicia reclamará a la entidad administrativa un testimonio completo del expediente, que deberá ser aportado en el plazo de veinte días.

4. Recibido el testimonio del expediente administrativo, el Letrado de la Administración de Justicia emplazará al actor por veinte días para que presente la demanda, que se tramitará con arreglo a lo previsto en el artículo 753.

5. Si el Ministerio Fiscal, las partes o el Juez competente tuvieren conocimiento de la existencia de más de un procedimiento de oposición a resoluciones administrativas relativas a la protección de un mismo menor, pedirán los primeros y dispondrá el segundo, incluso de oficio, la acumulación ante el Tribunal que estuviera conociendo del procedimiento más antiguo.

Acordada la acumulación, se procederá según dispone el artículo 84, con la especialidad de que no se suspenderá la vista que ya estuviera señalada si fuera posible tramitar el resto de procesos acumulados dentro del plazo determinado por el señalamiento. En caso contrario, el Letrado de la Administración de Justicia acordará la suspensión del que tuviera la vista ya fijada, hasta que los otros se hallen en el mismo estado, procediendo a realizar el nuevo señalamiento para todos con carácter preferente y, en todo caso, dentro de los diez días siguientes.

Contra el auto que deniegue la acumulación podrán interponerse los recursos de reposición y apelación sin efectos suspensivos. Contra el auto que acuerde la acumulación no se dará recurso alguno.”

El art. 753 LEC, por su parte, se remite a los trámites del juicio verbal, con las especialidades que el mismo precepto establece.

De conformidad con lo dispuesto en el art. 779.I de la LEC, el procedimiento que se insta tiene carácter preferente.

Conforme a lo dispuesto en el art. 3.2 LO 1/2025, la presente demanda no está sujeta al requisito de MASC, en cuanto se dirige contra una entidad pública como lo es en este caso [ÓRGANO ADMINISTRATIVO].

V. DERECHO SUSTANTIVO.- Establece el artículo 176 CC que la adopción se constituye por resolución judicial, que tendrá en cuenta siempre el interés del adoptando y la idoneidad del adoptante o adoptantes para el ejercicio de la patria potestad. Es con base en ese interés superior del menor que debe valorarse si procede revisar la resolución administrativa que concluye la falta de idoneidad.

Los aspectos que han de ponderarse para considerar a una persona idónea para la adopción y la finalidad que se persigue con dicho proceso, se dirigen a determinar si el sujeto o familia tiene capacidad para procurar el desarrollo integral del menor y una aptitud educadora adecuada, garantizar la cobertura de las necesidades del menor y el cumplimiento de las obligaciones establecidas legalmente y más específicamente la de asegurar que la persona o familia pueda ofrecer al menor la estabilidad, el cuidado y el respeto a sus señales de identidad que permitan su desarrollo integral. En concreto, el art. 176.3 CC establece: “Se entiende por idoneidad la capacidad, aptitud y motivación adecuadas para ejercer la responsabilidad parental, atendiendo a las necesidades de los menores a adoptar, y para asumir las peculiaridades, consecuencias y responsabilidades que conlleva la adopción.

La declaración de idoneidad por la Entidad Pública requerirá una valoración psicosocial sobre la situación personal, familiar, relacional y social de los adoptantes, así como su capacidad para establecer vínculos estables y seguros, sus habilidades educativas y su aptitud para atender a un menor en función de sus singulares circunstancias. Dicha declaración de idoneidad se formalizará mediante la correspondiente resolución.

No podrán ser declarados idóneos para la adopción quienes se encuentren privados de la patria potestad o tengan suspendido su ejercicio, ni quienes tengan confiada la guarda de su hijo a la Entidad Pública.

Las personas que se ofrezcan para la adopción deberán asistir a las sesiones informativas y de preparación organizadas por la Entidad Pública o por Entidad colaboradora autorizada”.

Con el contenido de los informes psicológicos que se aportan, no puede afirmarse que dichas aptitudes y funciones no puedan ser desarrolladas de forma adecuada por el/la demandante.

Se presentan, para acreditarlo así, informes periciales alternativos a los que tuvo en cuenta la Administración demandada.

Tal y como establece, entre otras, la SAP Barcelona (Sección 18ª), núm. 708/2005, de 7 noviembre, los informes tenidos en cuenta por la Administración para dictar su resolución, “pueden ser perfectamente discutidos y confrontados con otros en un proceso judicial, en el que las partes pueden aportar informes de otros equipos psicológicos o incluso solicitar un informe de asesoramiento del Equipo de Asesoramiento Técnico, y si la Juzgadora, después de valorar el contenido de todos los informes que se aporten a las actuaciones y resto de las pruebas practicadas, llega a una conclusión contraria a la de la Administración, en absoluto puede entenderse que vulnera precepto alguno de atribución de competencias, sino que está dando perfecto cumplimiento a la función jurisdiccional que tiene encomendada por Ley y efectividad al derecho de tutela judicial de todo ciudadano ante la Administración.”

La resolución administrativa impugnada alude a una inadecuada motivación del/de la solicitante para la adopción, pues persigue colmar una necesidad personal.

En relación con este extremo, hay que decir que, con carácter general, como señala la SAP Barcelona (Sección 18ª), núm. 708/2005 de 7 noviembre, “las motivaciones para solicitar la adopción normalmente son muy complejas, entremezclándose la necesidad de cubrir determinadas carencias a nivel personal y la de satisfacer las necesidades de los demás”, sin que en el caso de mi representado/a pueda entenderse acreditado que sus motivaciones no sean legítimas.

Como argumenta la SAP Ciudad Real (Sección 1ª), núm. 250/2005, de 11 octubre, “considerar como un concepto negativo que la adopción suponga una forma de cubrir necesidades de la pareja, no es sino una valoración muy subjetiva, puesto que el cubrir esas necesidades, por un lado, no es incompatible con el deseo de tener un hijo atendiendo todas las necesidades de éste, desde las puramente materiales a las afectivas, y, por otro, es una motivación que formulada de forma tan genérica nos la encontramos en casi todas las parejas, pues el desarrollo personal o de pareja a través de la maternidad o paternidad no es incompatible, antes al contrario, con las atenciones a los hijos para el correcto desarrollo de estos. La primacía en el interés del menor no choca con la voluntad de desarrollo de pareja a través de la maternidad.” Estas mismas consideraciones son válidas cuando el adoptante es una sola persona y no una pareja.

Por otra parte, es cierto, que mi representado/a manifestó una preferencia de sexo, pero esta preferencia es perfectamente legítima mientras no sea excluyente y en este caso es obvio que no lo es, en tanto no condicionó el resultado de la adopción a la elección del sexo.

En apoyo de los anteriores argumentos pueden citarse, además de las reseñadas, las siguientes sentencias:

Debe citarse, además, si la hay, la normativa autonómica aplicable al caso.

VII. COSTAS.- Procede imponer las costas a la entidad pública demandada, conforme al art. 394 LEC, de cuya aplicación no está exenta.

VIII. Iura novit curia y los demás que en Derecho procedan.

En su virtud:

SUPLICO AL TRIBUNAL: Que teniendo por presentado este escrito, en tiempo y forma, con los documentos que se acompañan, se sirva admitirlo, tenga por interpuesta DEMANDA DE OPOSICIÓN A LA DECLARACIÓN DE INIDONEIDAD PARA LA ADOPCIÓN EFECTUADA POR RESOLUCIÓN ADMINISTRATIVA de fecha [DÍA] de [MES] de [AÑO] dictada por [ÓRGANO O PERSONA] (organismo que corresponda según la Comunidad Autónoma de que se trate) de la Comunidad Autónoma de [LOCALIDAD] y, estimando lo que en él se solicita y previos los trámites legales oportunos, declare nula y sin efecto la citada resolución, por no resultar ajustada a Derecho, y declare la obligación de la Administración demandada de expedir el correspondiente certificado de idoneidad de D./Dª [NOMBRE Y APELLIDOS] para la adopción nacional/internacional de un menor, con expresa condena en costas si se opone a esta demanda, conforme al art. 394 LEC.

OTROSÍ DIGO: La cuantía del procedimiento resulta inestimable, por carecer su objeto de interés económico.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma y número del Letrado

Firma del Procurador

========================================================================
