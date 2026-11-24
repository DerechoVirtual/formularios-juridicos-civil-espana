---
name: demanda-desahucio-precario-contra-quien-usa-vivienda-civ-0048
description: "Demanda de desahucio por precario contra quien usa la vivienda familiar por sentencia matrimonial. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de desahucio por precario contra quien usa la vivienda familiar por sentencia matrimonial

> Formulario **CIV-0048** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio verbal de desahucio por precario con la que el propietario que cedió gratuitamente una vivienda a un hijo/a para hogar familiar reclama su recuperación frente al cónyuge a quien una sentencia de separación o divorcio atribuyó el uso de la vivienda, según la doctrina del Tribunal Supremo que considera precarista al adjudicatario una vez rota la convivencia.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de desahucio por precario contra quien usa la vivienda familiar por sentencia matrimonial» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de desahucio por precario contra quien usa la vivienda familiar por sentencia matrimonial” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-desahucio-precario-contra-quien-usa-vivienda-civ-0048`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (4 veces)
- [ ] AÑO (3 veces)
- [ ] DÍA (3 veces)
- [ ] MES (3 veces)
- [ ] NOMBRE Y APELLIDOS DEL DEMANDADO (3 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] CALLE (2 veces)
- [ ] DNI/NIE (2 veces)
- [ ] FIRMA (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] PUERTA (2 veces)
- [ ] SEDE (2 veces)
- [ ] COLEGIO
- [ ] DESCRIPCIÓN DE LA VIVIENDA Y DATOS REGISTRALES
- [ ] DOCUMENTO QUE ACREDITA EL INTENTO DE SOLUCIÓN NEGOCIADA
- [ ] IMPORTE
- [ ] IMPORTE EN LETRA
- [ ] NOMBRE Y APELLIDOS DEL ABOGADO/A
- [ ] NOMBRE Y APELLIDOS DEL DEMANDANTE
- [ ] NOMBRE Y APELLIDOS DEL HIJO/A DEL DEMANDANTE
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº
- [ ] Nº DE PROCEDIMIENTO
- [ ] PROFESIÓN
- [ ] TÍTULO DE ADQUISICIÓN

## Normas que cita el formulario

- art. 68 LEC
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 1749 Código Civil
- art. 348 Código Civil
- art. 394.1 LEC
- art. 253 LEC
- art. 251.2.º LEC

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

### Avisos de actualización (3) — se aplican en el texto, nunca se copian en el documento

- Junto a «…MILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.
- Junto a «…C, por remisión del art. 251.3.º, en [IMPORTE EN LETRA] euros ([IMPORTE] euros).»: el original citaba «art. 251.3.º.5»; comprobar el apartado exacto del art. 251 LEC aplicable al cálculo de la cuantía del precario.

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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDANTE], mayor de edad, de profesión [PROFESIÓN], con domicilio en [LOCALIDAD], calle [CALLE], nº [NÚMERO], puerta [PUERTA], y DNI núm. [DNI/NIE], cuya representación acreditaré mediante comparecencia apud acta cuando sea requerido para ello, comparezco en este TRIBUNAL con la asistencia del Letrado/a D./Dña. [NOMBRE Y APELLIDOS DEL ABOGADO/A], del Ilustre Colegio de la Abogacía de [COLEGIO], y DIGO:

Que por medio del presente escrito y en la representación que ostento, interpongo DEMANDA DE JUICIO VERBAL DE DESAHUCIO POR PRECARIO, contra D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO], mayor de edad, con domicilio en [LOCALIDAD], calle [CALLE], nº [NÚMERO], puerta [PUERTA] y DNI núm. [DNI/NIE]. La presente demanda se basa en los siguientes

HECHOS

Mi representado/a es propietario/a de la siguiente vivienda: [DESCRIPCIÓN DE LA VIVIENDA Y DATOS REGISTRALES]. La adquirió por título de [TÍTULO DE ADQUISICIÓN]. Se acredita esta circunstancia mediante certificación literal expedida por el Registro de la Propiedad nº [Nº] de [LOCALIDAD], que se acompaña como DOCUMENTO Nº [Nº DE DOCUMENTO].

En fecha [DÍA] de [MES] de [AÑO], el/la demandado/a contrajo matrimonio con D./Dña. [NOMBRE Y APELLIDOS DEL HIJO/A DEL DEMANDANTE], hijo/a de mi representado/a, el cual cedió la vivienda a su citado hijo/a para que la ocupara junto con su cónyuge, sin contraprestación alguna, como vivienda familiar.

En fecha [DÍA] de [MES] de [AÑO], la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia de [SEDE] dictó sentencia de [ELEGIR: divorcio / separación] del hijo/a de mi mandante y su cónyuge, en el seno del procedimiento núm. [Nº DE PROCEDIMIENTO]. En dicha sentencia se atribuyó al/a la demandado/a, D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO], el uso de la citada vivienda. Sin embargo, ello no altera la circunstancia de que, una vez rota la convivencia conyugal, el demandado/la demandada siga ocupando la vivienda como mero precarista.

Se acompaña, como DOCUMENTO N.º [Nº DE DOCUMENTO], testimonio de la citada sentencia, en la que consta su firmeza.

Habiendo resultado infructuosas las gestiones negociadoras con la parte demandada para que dejara libre la vivienda, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial, se interpone la presente demanda de desahucio en precario. En concreto, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO: negociación directa entre abogados / mediación / conciliación / otro], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO] [DOCUMENTO QUE ACREDITA EL INTENTO DE SOLUCIÓN NEGOCIADA].

Resultan aplicables a los citados hechos los siguientes:

FUNDAMENTOS DE DERECHO

Jurisdicción

Es competente la jurisdicción civil, de acuerdo con lo establecido en los arts. 9.2, 21.1, 22 a) y 86.5 a) de la Ley Orgánica del Poder Judicial, en relación con los arts. 36 y 45 de la Ley de Enjuiciamiento Civil.

Competencia

Es competente el Tribunal de la localidad en que está sita la finca, en virtud de lo establecido en el art. 68 LEC, en relación con el artículo 52.1.7.º de la Ley de Enjuiciamiento Civil.

Procedimiento

La presente demanda debe sustanciarse por los trámites del juicio verbal, establecidos en los arts. 437 y siguientes de la Ley de Enjuiciamiento Civil, en virtud de lo dispuesto en el artículo 250.1.2.º de la misma Ley, siendo igualmente aplicables las Disposiciones Comunes a los Procesos Declarativos previstas en el Título I del Libro II de la misma Ley.

Capacidad

Ambas partes tienen capacidad para serlo, conforme a lo dispuesto en los artículos 6 y siguientes de la Ley de Enjuiciamiento Civil.

Legitimación

Están legitimados activa y pasivamente el/la demandante y el/la demandado/a, conforme a los arts. 10 y 250.1.2.º de la Ley de Enjuiciamiento Civil. El/La primero/a, como propietario/a de la vivienda cuyo desalojo y recuperación solicita y, el/la segundo/a, como ocupante en precario de la misma.

Representación y defensa

El/La demandante comparece representado/a y defendido/a, respectivamente, por el Procurador/a y el Letrado/a que constan en el encabezamiento de este escrito, de acuerdo con lo dispuesto en los artículos 23.1 y 31.1 de la Ley de Enjuiciamiento Civil.

Cumplimiento de los requisitos de procedibilidad

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4.º y 399.3 LEC en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

Derecho sustantivo

Se ejercita acción de desahucio por precario con el fin de recuperar la posesión efectiva de la vivienda propiedad de mi representado/a, descrita en el hecho primero de la presente demanda.

Es precarista, de acuerdo con la jurisprudencia, aquel que posee un bien sin título (o en virtud de título nulo o que haya perdido su validez), por tolerancia o inadvertencia del propietario, sin que medie renta o pago de contraprestación, dependiendo de la sola voluntad del propietario poner fin a dicha situación [SSTS de 2 de junio y 17 de noviembre de 1961, de 6 de abril de 1962, de 23 de mayo de 1989 o de 31 de diciembre de 1992, entre otras]. La calificación de precarista es aplicable al/a la demandado/a en este procedimiento, como resulta de lo que a continuación se expone.

El Tribunal Supremo ha consolidado a través de diversas sentencias (STS de 26 de diciembre de 2005, rec. 1551/1999 y, a partir de ella, entre muchas otras, las SSTS de 2 de octubre de 2008, rec. 1745/2003, y de 29 de octubre de 2008, rec. 234/2004; de 30 de junio de 2009, rec. 1738/2004; 22 de octubre de 2009, rec. 2302/2005; de 14 de enero de 2010, rec. 5806/2000; 18 de enero de 2010, rec. 1994/2005; 14 de julio de 2010, rec. 1741/2005, y 22 de noviembre de 2010, rec. 39/2007, o de 18 de marzo de 2011, rec. 86/2008) la doctrina jurisprudencial según la cual procede la reclamación por su propietario de la vivienda que ha cedido sin título concreto y de forma gratuita a un hijo o descendiente, para su uso como hogar conyugal o familiar, cuando posteriormente el vínculo conyugal se rompe y el uso y disfrute de la vivienda se atribuye por resolución judicial a uno de los cónyuges, lo cual no obsta a que el mismo posea como precarista.

Resulta paradigmática la citada sentencia de 29 de octubre de 2008, rec. 234/2004, que declara: «la controversia se ciñe, ante todo, a la concreción del título que legitima al hijo o hija para poseer el inmueble, y se complica con la determinación de la eficacia de la resolución judicial que confiere, una vez roto el vínculo conyugal, el derecho de uso y disfrute de la vivienda, como domicilio familiar, a uno de los cónyuges, que opone dicho derecho frente al demandante del desahucio por precario.

Se ha de tener a la vista la fundamentación jurídica y el fallo de la Sentencia de esta Sala de fecha 2 de octubre de 2008, en donde se fija la doctrina jurisprudencial con arreglo a la cual ha de decidirse la controversia. Conforme a la misma, la cuestión controvertida debe resolverse, ante todo, mediante la comprobación de la existencia de un contrato entre las partes, y particularmente, de un contrato de comodato, caracterizado por la cesión gratuita de la cosa por un tiempo determinado o para un uso concreto y determinado, que faculta al comodante para reclamar la cosa prestada únicamente cuando ha transcurrido dicho plazo o ha concluido el uso para el que se prestó, excepción hecha de los casos en que tuviere la urgente necesidad de ella (artículo 1749 del Código Civil). Si existe el préstamo de uso, han de aplicarse las normas reguladoras de la figura negocial; de lo contrario, se ha de considerar que la situación jurídica es la propia de un precario, estando legitimado el propietario o titular de la cosa cedida para reclamarla a su voluntad. Ciertamente, en la cesión de una vivienda a un hijo para que constituya en él el hogar conyugal o familiar, pueden apreciarse las notas caracterizadoras del préstamo de uso; pero para ello es preciso que tales elementos (la concreción y determinación del uso al que se destina el inmueble, en ese caso, para subvenir las necesidades familiares y facilitar un lugar destinado a servir de vivienda o domicilio conyugal y familiar) aparezcan con claridad, y que los hechos sean reveladores de que el uso para el que se cede la cosa se encuentra definido más allá del que es propio de la cosa genérica, e incluso específicamente considerada (in casu, servir de morada o residencia), lo que no empece a que puedan inferirse de las circunstancias fácticas del caso (Sentencias de 26 de diciembre de 2005 y de 2 de octubre de 2008). Paralelamente, se debe considerar que cuando desaparece el uso concreto y determinado al que se ha destinado la cosa (lo que puede suceder cuando se rompe la convivencia conyugal), y el propietario o titular de la cosa no la reclama, la situación de quien la posee es la propia de un precarista (Sentencias de 26 de diciembre de 2005 y de 2 de octubre de 2008); y, en fin, que la atribución por resolución judicial del derecho de uso y disfrute de la vivienda no sirve para hacer desaparecer la situación de precario, ni para enervar la acción de desahucio, en la medida en que no constituye un título jurídico hábil para justificar la posesión que resulte oponible a terceros ajenos a las relaciones surgidas por el matrimonio y por el procedimiento matrimonial, ni permite reconocer al beneficiario una posición jurídica y una protección posesoria de vigor jurídico superior al que la situación de precario proporciona a la familia, pues ello entrañaría subvenir necesidades familiares, desde luego muy dignas de protección, con cargo a extraños al vínculo matrimonial y titulares de un derecho que posibilita la cesión del uso de la vivienda (Sentencia de 31 de diciembre de 1994, cuya doctrina se recoge en las de 26 de diciembre de 2005 y de 2 de octubre de 2008).»

Así pues, la atribución del uso en procedimiento de separación o divorcio es oponible en el ámbito de las relaciones entre los cónyuges, pero no puede afectar a terceros ajenos al matrimonio, aunque se trate de familiares próximos que cedieron el uso en atención a la relación de la pareja. La atribución del uso en sentencia de nulidad o divorcio a uno de los cónyuges no da nacimiento a un derecho nuevo, antes inexistente, ni permite reconocer al adjudicatario mayor protección posesoria de la que antes derivaba de la ocupación.

Cuando se rompe la convivencia familiar, el adjudicatario se considera que ocupa la vivienda en precario, sin que pueda oponer frente a terceros un eventual comodato (aunque pudiera defenderse que éste existía antes de la crisis matrimonial), ni la atribución judicial del uso del inmueble. Así lo expresa, entre muchas otras, la STS de 29 de octubre de 2008, rec. 234/2004: «Si bien es posible reconocer en las circunstancias en que se produjo la cesión los elementos característicos de un préstamo de uso, delimitado precisamente por la asignación del destino de servir de morada familiar y de subvenir de ese modo las necesidades de la familia, se ha de convenir, empero, en línea con el criterio jurisprudencial expuesto, que este elemento caracterizador ha desaparecido al romperse la convivencia conyugal, encontrándose quien posee el inmueble desde entonces en la situación de precarista, que es la que, en cualquier caso, se da cuando, por cesar la convivencia conyugal, desaparece el uso concreto y determinado al que eventualmente pudiera considerarse que fue destinada la vivienda cedida. Y esta situación no se ve afectada por la atribución judicial a la esposa demandada del derecho de uso y disfrute de la vivienda en su condición de vivienda familiar, pues, tal y como se ha indicado, semejante declaración jurisdiccional no conforma un derecho nuevo, ni confiere mayor vigor jurídico que el correspondiente al precario, que pueda oponerse eficazmente frente a un tercero en la relación y en el proceso matrimonial que pretende, contando con título jurídico bastante para ello, la recuperación posesoria del inmueble.»

O como dicen la STS de 18 de enero de 2010, rec. 1994/2005, y la de 18 de marzo de 2011, rec. 86/2008, «la solución a estos conflictos debe ser dada desde el punto de vista del Derecho de propiedad y no desde los parámetros del Derecho de familia, porque las consecuencias del divorcio o la separación de los cónyuges nada tienen que ver con los terceros propietarios».

Por todo ello, procede el ejercicio de la presente acción de desahucio por precario, que debe ser estimada a la vista de los hechos expuestos, sustancialmente coincidentes con los de los casos resueltos por las sentencias antes citadas, con base en el derecho de propiedad de mi mandante (arts. 348 y 349 del Código Civil).

Costas

Procede imponerlas a la parte cuyas pretensiones hubieran sido totalmente rechazadas, en virtud de lo dispuesto en el art. 394.1 LEC.

Por lo expuesto,

SUPLICO AL TRIBUNAL:

Que tras admitir este escrito con los documentos que lo acompañan y sus copias, me tenga por comparecido/a y parte en la representación que ostento, entendiéndose conmigo las sucesivas diligencias, y tenga por interpuesta DEMANDA EN JUICIO VERBAL DE DESAHUCIO POR PRECARIO, contra D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO] y, previos los trámites legales que proceda, dicte sentencia por la que se estime la demanda y se condene a la parte demandada a desalojar la vivienda descrita en el hecho primero, dejándola libre y a disposición de mi representado/a en el plazo legalmente establecido, con apercibimiento de que, de no realizarlo así, se procederá al lanzamiento a su costa; con imposición de las costas procesales de este procedimiento al/a la demandado/a, en virtud de lo dispuesto en el art. 394.1 LEC.

OTROSÍ DIGO.- En cumplimiento de lo dispuesto en el art. 253 LEC, esta parte fija la cuantía del procedimiento, calculada de acuerdo con lo dispuesto en el art. 251.2.º LEC, por remisión del art. 251.3.º, en [IMPORTE EN LETRA] euros ([IMPORTE] euros).

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma y número de colegiado del Letrado/a: [FIRMA] Firma del Procurador/a: [FIRMA]
