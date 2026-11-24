---
name: demanda-divorcio-contencioso-segun-derecho-civil-civ-0064
description: "Demanda de divorcio contencioso según el Derecho civil catalán pidiendo la custodia compartida. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de divorcio contencioso según el Derecho civil catalán pidiendo la custodia compartida

> Formulario **CIV-0064** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda de divorcio contencioso (sin acuerdo entre los cónyuges) sujeta al Derecho civil de Cataluña (Libro II del Código Civil de Cataluña), en la que se pide como medida principal la guarda y custodia compartida del hijo menor común, con solicitud de medidas provisionales coetáneas a la admisión de la demanda.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de divorcio contencioso según el Derecho civil catalán pidiendo la custodia compartida» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de divorcio contencioso según el Derecho civil catalán pidiendo la custodia compartida” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-divorcio-contencioso-segun-derecho-civil-civ-0064`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº DE DOCUMENTO (12 veces)
- [ ] IMPORTE (10 veces)
- [ ] LOCALIDAD (9 veces)
- [ ] DENOMINACIÓN SOCIAL (4 veces)
- [ ] APELLIDOS DEL CÓNYUGE (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL DEMANDADO/A (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL DEMANDANTE (2 veces)
- [ ] APELLIDOS DEL TITULAR
- [ ] AÑO
- [ ] COLEGIO
- [ ] DESCRIPCIÓN DE LA JORNADA Y EMPRESA
- [ ] DESCRIPCIÓN DE LA JORNADA Y HORARIO
- [ ] DNI/NIE
- [ ] DOMICILIO DEL DEMANDADO/A
- [ ] DOMICILIO DEL DESPACHO
- [ ] DÍA
- [ ] EDAD
- [ ] FECHA
- [ ] FECHA DE NACIMIENTO
- [ ] MES
- [ ] NOMBRE DEL CENTRO ESCOLAR
- [ ] NOMBRE DEL HIJO/A
- [ ] NOMBRE Y APELLIDOS DEL CÓNYUGE
- [ ] NOMBRE Y APELLIDOS DEL LETRADO/A
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº DE COLEGIADO
- [ ] SEDE

## Normas que cita el formulario

- art. 233 Código Civil
- art. 233 CC
- art. 770 LEC
- art. 6.1.1.º LEC
- art. 750.1 LEC
- art. 86 CC
- art. 749.2 LEC
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 81.2.º CC
- art. 394 LEC
- art. 773.1 LEC
- art. 771 LEC
- art. 773.3 LEC

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

A LA SECCIÓN [ELEGIR: DE FAMILIA, INFANCIA Y CAPACIDAD / CIVIL / ÚNICA, DE CIVIL Y DE INSTRUCCIÓN] DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, que actúa en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDANTE], provisto/a de D.N.I. n.º [DNI/NIE], con domicilio en [LOCALIDAD], calle [DOMICILIO], según acredito mediante [ELEGIR: certificación del Registro Electrónico de Apoderamientos Judiciales / escritura de poder] que acompaño como documento n.º [Nº DE DOCUMENTO], bajo la dirección del/de la Letrado/a D./Dña. [NOMBRE Y APELLIDOS DEL LETRADO/A], colegiado/a n.º [Nº DE COLEGIADO] del Ilustre Colegio de Abogados de [COLEGIO], cuyo despacho se abre en [LOCALIDAD], calle [DOMICILIO DEL DESPACHO], ante el Tribunal comparezco y, como mejor en Derecho proceda, DIGO:

Que por medio del presente escrito, siguiendo las instrucciones de mi mandante, vengo a formular DEMANDA CONTENCIOSA DE DIVORCIO frente a su [ELEGIR: esposa / esposo] D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO/A], con domicilio actual en [LOCALIDAD], calle [DOMICILIO DEL DEMANDADO/A], con base en los siguientes datos y argumentos:

HECHOS

PRIMERO.- Mi mandante contrajo matrimonio [ELEGIR: canónico / civil] con D./Dña. [NOMBRE Y APELLIDOS DEL CÓNYUGE], en [LOCALIDAD], el día [FECHA]. Se acompaña la correspondiente certificación de matrimonio expedida por el Registro Civil de [LOCALIDAD] (DOCUMENTO N.º [Nº DE DOCUMENTO]).

De dicha unión nació un hijo, menor de edad, de nombre [NOMBRE DEL HIJO/A], nacido el [FECHA DE NACIMIENTO]. Se adjunta la correspondiente certificación de nacimiento emitida por el Registro Civil de [LOCALIDAD] (DOCUMENTO N.º [Nº DE DOCUMENTO]).

SEGUNDO.- Como consecuencia de las desavenencias entre los cónyuges, mi representado/a está persuadido/a de lo adecuado de su decisión de disolver el vínculo matrimonial mediante divorcio, sin que haya sido posible tramitarlo de mutuo acuerdo, por lo que se interpone la presente demanda contenciosa.

TERCERO.- El régimen económico del matrimonio es el de separación de bienes, ya que por residencia y lugar de celebración del matrimonio la vecindad civil de los cónyuges es la catalana, no habiéndose otorgado nunca capitulaciones matrimoniales, por lo que no corresponde realizar liquidación alguna del referido régimen económico matrimonial.

CUARTO.- La disolución del vínculo no produce desequilibrio económico para ninguno de los cónyuges, por lo que no se solicita la prestación compensatoria prevista en el art. 233-14 del Libro II del Código Civil de Cataluña, aprobado por Ley 25/2010, de 29 de julio (en adelante, CCC), ni compensación económica alguna de las reguladas en el art. 232-5 del citado texto legal.

QUINTO.- En la actualidad, mi mandante tiene su residencia en [ELEGIR: la casa de sus padres / otra vivienda], sita en [LOCALIDAD], calle [DOMICILIO], que es el domicilio arriba señalado.

Por su parte, [ELEGIR: el Sr. / la Sra.] [APELLIDOS DEL CÓNYUGE] ocupa el que ha sido domicilio conyugal, perteneciente en plena propiedad a [ELEGIR: el Sr. / la Sra.] [APELLIDOS DEL TITULAR].

Adjunto certificado de empadronamiento y escritura pública de propiedad de la vivienda familiar (DOCUMENTOS N.º [Nº DE DOCUMENTO] y [Nº DE DOCUMENTO]).

SEXTO.- El hijo común, de [EDAD] años de edad a la fecha de la demanda, tiene una muy buena relación con su [ELEGIR: padre / madre], quien está plenamente capacitado/a para su cuidado y atención, siendo un progenitor plenamente implicado y preocupado por el bienestar de su hijo, que desea compartir con él el mayor tiempo posible.

El/La demandante tiene plena disponibilidad laboral para poder ejercer la guarda y custodia en semanas alternas, ya que trabaja de [DESCRIPCIÓN DE LA JORNADA Y HORARIO]. Se adjunta certificado de la empresa para la que trabaja, expresivo de los turnos y horarios de trabajo del/de la demandante (DOCUMENTO N.º [Nº DE DOCUMENTO]).

El/La progenitor/a demandante reside en una vivienda próxima a la que fue vivienda familiar, debiendo considerarse irrelevante que comparta dicha vivienda con sus padres, abuelos del menor, habida cuenta de que la misma es adecuada, pues cuenta con espacio suficiente para que el menor pueda tener su propia habitación, lo que, además, facilita el contacto de éste con sus abuelos.

[ELEGIR: La madre / El padre] del menor trabaja, [DESCRIPCIÓN DE LA JORNADA Y EMPRESA], y ambos progenitores han venido alternándose el cuidado de su hijo, incluso en el último periodo en el que han decidido la ruptura y realizaban vidas separadas.

El menor estudia en el Colegio [NOMBRE DEL CENTRO ESCOLAR], habiendo ingresado en dicho colegio por voluntad conjunta de ambos progenitores.

De acuerdo con lo establecido en el art. 233-8.2 CCC, se acompaña propuesta de plan de parentalidad (1) para el ejercicio de las responsabilidades parentales con respecto a la guarda, cuidado y educación de los hijos comunes, conforme al art. 233-9 CCC, como DOCUMENTO N.º [Nº DE DOCUMENTO].

SÉPTIMO.- Los gastos que ocasionan la manutención, vestido y educación del hijo ascienden, aproximadamente, a [IMPORTE] euros mensuales.

El/La demandante percibe unos ingresos de [IMPORTE] euros mensuales como trabajador/a de la empresa [DENOMINACIÓN SOCIAL], mientras que [ELEGIR: el Sr. / la Sra.] [APELLIDOS DEL CÓNYUGE] percibe unos ingresos de [IMPORTE] euros mensuales como trabajador/a de la empresa [DENOMINACIÓN SOCIAL]. Se adjuntan, al objeto de demostrar las rentas de la unidad familiar, copias de las declaraciones del IRPF del último ejercicio y del anterior (DOCUMENTOS N.º [Nº DE DOCUMENTO] y [Nº DE DOCUMENTO]).

Conforme a lo dicho, y teniendo en cuenta la similitud de los ingresos de ambos progenitores, se entiende que no procede fijar pensión alimenticia alguna, de manera que las cargas serán atendidas por mitad.

En cuanto a la manutención diaria, cada progenitor soportará los gastos del hijo cuando lo tenga en su compañía y, para atender los gastos ordinarios de escolaridad y sanidad, cada uno de ellos ingresará en una cuenta común la cantidad de [IMPORTE] euros mensuales. Esta cuenta será administrada por [ELEGIR: el padre / la madre], que deberá llevar la oportuna referencia contable, de la que pasará nota al otro progenitor al vencimiento de cada semestre.

Los gastos extraescolares (que deberán ser concertados de común acuerdo) y los extraordinarios (necesarios, no periódicos e imprevisibles) serán soportados al 50 %. Se solicita la atribución de la administración a [ELEGIR: el padre / la madre], puesto que la atención directa de las necesidades escolares viene siendo ejercida por él/ella, sin perjuicio de que comunique al otro progenitor cualquier circunstancia relevante en este campo.

OCTAVO.- Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO: MEDIACIÓN, NEGOCIACIÓN ENTRE LETRADOS, ETC.], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento n.º [Nº DE DOCUMENTO].

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN.

Es competente la jurisdicción civil, según lo establecido en los arts. 9.2 y 21.1 LOPJ.

II.- COMPETENCIA.

Es competente el Tribunal de Instancia del lugar del domicilio de la parte demandada, que es el último domicilio conyugal común, conforme al art. 769.1, párrafo 1.º LEC.

III.- PROCEDIMIENTO.

El procedimiento adecuado es el del art. 770 LEC para conocer de las demandas de divorcio contenciosas.

IV.- CAPACIDAD.

Mi mandante ostenta capacidad procesal suficiente, conforme al art. 6.1.1.º LEC.

V.- POSTULACIÓN.

Comparece representado/a por Procurador/a debidamente habilitado/a para actuar en el territorio de este Tribunal, y asistido/a por Abogado/a, conforme a lo establecido en el art. 750.1 LEC.

VI.- LEGITIMACIÓN.

Tienen legitimación ordinaria, por hallarse en la situación jurídica de relación matrimonial, ambos cónyuges (arts. 86 CC y 10, párrafo 1.º LEC), siendo el objeto del proceso principal la pretensión de disolución del vínculo por divorcio y la adopción de medidas definitivas derivadas de la misma.

VII.- INTERVENCIÓN DEL MINISTERIO FISCAL.

Dada la presencia de hijos menores del matrimonio, es preceptiva la intervención del Ministerio Fiscal, según lo establecido en el art. 749.2 LEC.

VIII.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4.º y 399.3 en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

IX.- PETICIÓN DE DIVORCIO.

El fondo de la pretensión consiste en la declaración de divorcio, a fin de la disolución del matrimonio, a instancia de uno de los cónyuges, de conformidad con el art. 81.2.º CC, por remisión del art. 86 CC, sin que pueda oponer el otro cónyuge ninguna causa de oposición material, al fundarse en la voluntad de no permanecer casado, como corolario legal del derecho a contraer matrimonio del art. 32 CE.

X.- MEDIDAS QUE HAN DE REGULAR LOS EFECTOS DEL DIVORCIO.

En relación con las medidas a adoptar, el art. 233-4 CCC dispone que "1. Si un cónyuge solicita la nulidad del matrimonio, el divorcio o la separación judicial sin consentimiento del otro, o si ambos cónyuges no llegan a un acuerdo sobre el contenido del convenio regulador, la autoridad judicial debe adoptar las medidas definitivas pertinentes sobre el ejercicio de las responsabilidades parentales, incluidos el deber de alimentos. 2. Si alguno de los cónyuges lo solicita, la autoridad judicial debe adoptar las medidas pertinentes respecto al uso de la vivienda familiar y su ajuar, la prestación compensatoria, la compensación económica por razón del trabajo si el régimen económico es el de separación de bienes, la liquidación del régimen económico matrimonial y la división de los bienes comunes o en comunidad ordinaria indivisa".

El art. 233-8 dice, en su apartado 1, que "la nulidad del matrimonio, el divorcio o la separación judicial no alteran las responsabilidades que los progenitores tienen hacia sus hijos de acuerdo con el artículo 236-17.1. En consecuencia, estas responsabilidades mantienen el carácter compartido y, en la medida de lo posible, deben ejercerse conjuntamente".

El apartado 2 añade que "los cónyuges, para determinar cómo deben ejercerse las responsabilidades parentales, deben presentar sus propuestas de plan de parentalidad, con el contenido establecido por el artículo 233-9".

El apartado 3 finaliza diciendo que "la autoridad judicial, en el momento de decidir sobre las responsabilidades parentales de los progenitores, debe atender de forma prioritaria al interés del menor".

Desde el punto de vista de los Tribunales, en lo referente a la guarda y custodia conjunta, cabe reseñar el criterio señalado por el TSJC en su sentencia de 20 de diciembre de 2010, rec. 108/2010: "La jurisprudencia de esta Sala ha declarado -SSTSJC 29/2008, de 31 de julio, 24/2009, de 25 de junio, 9/2010, de 3 de marzo y 10/2010, de 8 de marzo, entre otras- que es el interés superior de los hijos el criterio preferente a examinar y resolver en la atribución de la guarda y custodia compartida, siendo que su aplicación debe ser extremadamente cuidadosa y subordinada a la protección jurídica de la persona y de los derechos de personalidad de los menores afectados; procurando su implantación cuando resulta beneficiosa para los menores de tal modo que ni la guarda y custodia compartida constituye una situación excepcional frente a la custodia monoparental o que haya de primar una de ellas, en cualquier caso, frente a la otra pues es el interés del menor el criterio preferente". Y en la sentencia de 8 de marzo de 2010, rec. 47/2009, manifiesta para casos de conflictividad entre los padres que "no significa que deba desecharse frente a cualquier grado de conflictividad y que no deba procurarse su implementación cuando resulta beneficiosa para los menores, aunque sea imponiendo en determinados casos la mediación familiar o terapias educativas (art. 79.2 C.F.), teniendo en cuenta la edad de los hijos, el horario laboral o profesional de los progenitores, la proximidad del lugar de residencia de ambos progenitores, la disponibilidad por éstos de una residencia adecuada para tener consigo a los hijos, el tiempo libre o de vacaciones, la opinión de los menores al respecto, u otras circunstancias similares, teniendo siempre presente el preferente interés de los menores".

La doctrina general sobre la custodia de los hijos tras la separación o el divorcio es la recogida por el Tribunal Supremo en su sentencia de 8 de octubre de 2009, rec. 1471/2006. Esta resolución, unificadora de los criterios dispersos hasta ese momento, marca un punto de inflexión en la materia desde que entrara en vigor la Ley 15/2005, que introdujo la custodia compartida en el ordenamiento español, y destaca que el punto de vista esencial para determinar la modalidad de ejercicio de la guarda ha de ser el del superior interés del menor, recogido en los arts. 2 y 3 de la Ley Orgánica de Protección Jurídica del Menor y en los sucesivos textos legales que han desplazado las consideraciones de otra índole, ante el esencial eje de toda decisión administrativa o jurisdiccional en la materia.

Las SSTS de 8 de octubre de 2009, rec. 1471/2006; 1 de octubre de 2010, rec. 681/2007 y 11 de marzo de 2010, rec. 54/2008, en la misma línea, señalan los diversos criterios que han de servir de base a la decisión, y la STS de 22 de julio de 2011, rec. 813/2009, añade la consideración de que el ejercicio conjunto de todas las responsabilidades parentales tras la ruptura de la relación entre los progenitores no ha de ser excepcional, sino que debe ser la norma cuando se dan las condiciones de idoneidad en los menores y es posible establecerlo atendida la actitud y aptitud de quienes han de ejercerla.

La jurisprudencia del TSJ de Cataluña, en sus sentencias de 31 de julio de 2008, rec. 72/2007, 5 de septiembre de 2008, rec. 134/2007 y 3 de marzo de 2010, rec. 152/2008, entre otras, y la línea jurisprudencial que se ha consolidado en esta materia, viene delimitando sus requisitos, basados esencialmente en el análisis de la realidad de cada caso concreto, y teniendo en cuenta fundamentalmente la propia dinámica de la familia anterior a la crisis, los deseos de los menores, el respeto mutuo, el cumplimiento de las obligaciones por los progenitores o la ubicación de los domicilios.

A favor del reconocimiento de la guarda y custodia compartida, y en aplicación del derecho civil de Cataluña, se han pronunciado, entre otras, la sentencia de la Audiencia Provincial de Girona, Sección 1.ª, de 29 de junio de 2012, rec. 304/2012, y de 20 de junio de 2012; la sentencia de la Audiencia Provincial de Barcelona, Sección 12.ª, de 19 de junio de 2012, y la sentencia de la Audiencia Provincial de Tarragona, Sección 1.ª, de 28 de marzo de 2012, rec. 45/2012.

En cualquier caso, entiende esta parte que, con independencia de que la regulación de esta materia establezca una preferencia por uno u otro sistema de guarda, conjunta o exclusiva de uno de los progenitores, la decisión judicial no debe ser sometida a la preferencia de la Ley sino únicamente al interés superior del menor, y en ningún caso puede obviarse lo dispuesto en el art. 39 CE y en los arts. 1, 2 y 11.2 de la Ley Orgánica 1/1996, de 15 de enero, de Protección Jurídica del Menor.

En definitiva, en opinión de esta representación, el beneficio del menor exige la atribución de la guarda y custodia compartida, ya que en este caso concurren los requisitos exigidos en los arts. 233-11.1.a), d) y e) CCC: el menor tiene una vinculación afectiva igual con ambos progenitores, la dedicación al hijo del demandante tras la ruptura es incuestionable, y la propia opinión expresada por el hijo es favorable a pasar todo el tiempo posible con su padre y con su madre; todo ello, sin perjuicio de que se garantice el régimen de relación y comunicación con el hijo durante el tiempo en que el menor se encuentre con el progenitor que no tenga la guarda.

XI.- COSTAS.

No hay ninguna razón para excluir la aplicación del principio del vencimiento (art. 394 LEC), debiéndose condenar a la parte demandada que se oponga, dado que el obtener la razón precisando de un proceso no ha de suponer una merma patrimonial para quien la tiene.

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito con los documentos que se acompañan y sus copias, se digne admitirlos, tenerme por comparecido/a y parte en la representación que ostento, entendiéndose conmigo las sucesivas diligencias, y por formulada demanda de disolución del matrimonio por divorcio, de modo que, seguido que sea el pertinente procedimiento, con citación del Ministerio Fiscal, se dicte en su día sentencia por la que, estimando la presente demanda:

1.º) DECLARE disuelto el vínculo matrimonial por causa de divorcio entre D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDANTE] y D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO/A], oficiándose al Registro Civil de [LOCALIDAD] para la anotación de su parte dispositiva en la inscripción del matrimonio.

2.º) ACUERDE las siguientes medidas definitivas, que se podrán modificar si se alteraren sustancialmente las circunstancias:

1.- La atribución de la guarda y custodia compartida del hijo menor, conforme al plan de parentalidad para el ejercicio de las responsabilidades parentales propuesto por esta parte, sin perjuicio de que eventualmente pueda llegarse a un acuerdo conjunto con el otro progenitor sobre cualquiera de los puntos recogidos en el plan que se adjunta.

2.- En relación con las cargas alimenticias, y teniendo en cuenta la similitud de los ingresos de ambos progenitores, que no procede fijar pensión alimenticia alguna, de manera que serán atendidas por mitad, conforme a la siguiente distribución:

- En cuanto a la manutención diaria, cada progenitor soportará los gastos del hijo cuando lo tenga en su compañía y, para atender los gastos ordinarios de escolaridad y sanidad, cada uno de ellos ingresará en una cuenta común la cantidad de [IMPORTE] euros mensuales. Cantidad que será actualizable anualmente conforme a las variaciones que experimente el Índice de Precios al Consumo que publique el Instituto Nacional de Estadística, u organismo oficial que lo sustituya. Esta cuenta será administrada por [ELEGIR: el padre / la madre], que deberá llevar la oportuna referencia contable, de la que pasará nota al otro progenitor al vencimiento de cada semestre.

- Los gastos extraescolares (que deberán ser concertados de común acuerdo) y los extraordinarios (necesarios, no periódicos e imprevisibles) serán soportados al 50 %. Se atribuirá la administración a [ELEGIR: el padre / la madre], puesto que la atención directa de las necesidades escolares viene siendo ejercida por él/ella, sin perjuicio de que comunique al otro progenitor cualquier circunstancia que sea relevante en este campo.

En todo caso, se pronuncie el reintegro de las costas con cargo a la parte demandada, si se opusiere.

Es justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

OTROSÍ DIGO: Que al amparo del art. 773.1 LEC, no habiéndose adoptado con anterioridad, se solicitan mediante el presente escrito MEDIDAS PROVISIONALES coetáneas a la admisión de la demanda, en base a los siguientes:

HECHOS

PRIMERO.- Dado que ambos padres han venido alternándose el cuidado de su hijo menor de edad desde que decidieron la ruptura y comenzaron a realizar vidas separadas, la guarda y custodia debe concederse conjuntamente a ambos progenitores, quienes la ejercerán en semanas alternas ([CONCRETAR LAS CIRCUNSTANCIAS EN QUE DEBA EJERCERSE ESA GUARDA Y CUSTODIA, QUE, NORMALMENTE, COINCIDIRÁN CON LAS PREVISTAS EN EL PLAN DE PARENTALIDAD QUE SE ADJUNTE CON LA DEMANDA]).

SEGUNDO.- Los gastos que ocasionan la manutención, vestido y educación del hijo ascienden, aproximadamente, a [IMPORTE] euros mensuales.

El/La demandante percibe unos ingresos de [IMPORTE] euros mensuales como trabajador/a de la empresa [DENOMINACIÓN SOCIAL], mientras que [ELEGIR: el Sr. / la Sra.] [APELLIDOS DEL CÓNYUGE] percibe unos ingresos de [IMPORTE] euros mensuales como trabajador/a de la empresa [DENOMINACIÓN SOCIAL]. Se adjuntan, al objeto de demostrar las rentas de la unidad familiar, copias de las declaraciones del IRPF del último ejercicio y del anterior (DOCUMENTOS N.º [Nº DE DOCUMENTO] y [Nº DE DOCUMENTO]).

En relación con las cargas alimenticias, y teniendo en cuenta la similitud de los ingresos de ambos progenitores, no procede fijar pensión alimenticia alguna, de manera que serán atendidas por mitad.

En cuanto a la manutención diaria, cada progenitor soportará los gastos del hijo cuando lo tenga en su compañía y, para atender los gastos ordinarios de escolaridad y sanidad, cada uno de ellos ingresará en una cuenta común la cantidad de [IMPORTE] euros mensuales. Esta cuenta será administrada por [ELEGIR: el padre / la madre], que deberá llevar la oportuna referencia contable, de la que pasará nota al otro progenitor al vencimiento de cada semestre.

Los gastos extraescolares (que deberán ser concertados de común acuerdo) y los extraordinarios (necesarios, no periódicos e imprevisibles) serán soportados al 50 %. Se solicita la atribución de la administración a [ELEGIR: el padre / la madre], puesto que la atención directa de las necesidades escolares viene siendo ejercida por él/ella, sin perjuicio de que comunique al otro progenitor cualquier circunstancia que sea relevante en este campo.

FUNDAMENTOS DE DERECHO

I.- El cónyuge que solicita el divorcio está legitimado para pedir con la demanda las medidas provisionales del art. 233-1 CCC.

II.- El procedimiento adecuado es el del art. 771 LEC para medidas previas, conforme a la remisión del art. 773.3 LEC.

III.- Esta pretensión consiste en la adopción de los efectos "ope legis" del art. 233-1.5 y de las medidas del art. 233-1.1, de cognición judicial, derivados de la tutela cautelar frente a la lesión que, de no adoptarse, pueden padecer las partes y los hijos menores por la duración del proceso.

En su virtud,

SUPLICO AL TRIBUNAL

que, teniendo por causadas las precedentes manifestaciones a los efectos oportunos, y por deducida solicitud de adopción de medidas provisionales, seguido que sea su pertinente trámite, se dicte Auto por el que se aprueben las siguientes:

1.- La atribución de la guarda y custodia compartida del hijo menor ([CONCRETAR LAS CIRCUNSTANCIAS EN QUE DEBA EJERCERSE ESA GUARDA Y CUSTODIA, QUE, NORMALMENTE, COINCIDIRÁN CON LAS PREVISTAS EN EL PLAN DE PARENTALIDAD QUE SE ADJUNTE CON LA DEMANDA]).

2.- En relación con los alimentos del menor, y teniendo en cuenta la similitud de los ingresos de ambos progenitores, no procede fijar pensión alimenticia alguna, de manera que serán atendidas por mitad, conforme a la siguiente distribución:

- En cuanto a la manutención diaria, cada progenitor soportará los gastos del hijo cuando lo tenga en su compañía y, para atender los gastos ordinarios de escolaridad y sanidad, cada uno de ellos ingresará en una cuenta común la cantidad de [IMPORTE] euros mensuales. Cantidad que será actualizable anualmente conforme a las variaciones que experimente el Índice de Precios al Consumo que publique el Instituto Nacional de Estadística, u organismo oficial que lo sustituya. Esta cuenta será administrada por [ELEGIR: el padre / la madre], que deberá llevar la oportuna referencia contable, de la que pasará nota al otro progenitor al vencimiento de cada semestre.

- Los gastos extraescolares (que deberán ser concertados de común acuerdo) y los extraordinarios (necesarios, no periódicos e imprevisibles) serán soportados al 50 %. Se atribuirá la administración a [ELEGIR: el padre / la madre], puesto que la atención directa de las necesidades escolares viene siendo ejercida por él/ella, sin perjuicio de que comunique al otro progenitor cualquier circunstancia que sea relevante en este campo.

[Lugar y fecha]

Firma del Abogado/a Firma del Procurador/a

(1) Existe una guía y un modelo del plan de parentalidad, elaborados con carácter meramente indicativo y facilitados por la Dirección General de Derecho y Entidades Jurídicas de la Generalitat de Cataluña, en cumplimiento de la Disposición adicional 9.ª de la Ley 25/2010, de 29 de julio, del Libro II del Código civil de Cataluña, relativo a la persona y a la familia, y que está disponible en la web del Ilustre Colegio de la Abogacía de Barcelona (ICAB).
