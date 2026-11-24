---
name: divorcio-contencioso-sin-separacion-judicial-previa-civ-0284
description: "Divorcio contencioso sin separación judicial previa (demanda). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Divorcio contencioso sin separación judicial previa (demanda)

> Formulario **CIV-0284** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda de divorcio contencioso presentada por uno de los cónyuges sin separación judicial previa (art. 86 CC), con petición de medidas definitivas (guarda y custodia, alimentos de los hijos y pensión compensatoria) tras una separación de hecho o pactada extrajudicialmente, y adaptada al requisito de procedibilidad de la LO 1/2025.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Divorcio contencioso sin separación judicial previa (demanda)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Divorcio contencioso sin separación judicial previa (demanda)” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:divorcio-contencioso-sin-separacion-judicial-previa-civ-0284`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº DE DOCUMENTO (12 veces)
- [ ] AÑO (10 veces)
- [ ] LOCALIDAD (8 veces)
- [ ] IMPORTE EN LETRA (7 veces)
- [ ] NOMBRE DEL HIJO/A (6 veces)
- [ ] DÍA (5 veces)
- [ ] MES (5 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] PORCENTAJE (3 veces)
- [ ] CORREO ELECTRÓNICO (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] FIRMA (2 veces)
- [ ] IMPORTE EN NÚMERO (2 veces)
- [ ] Nº DE TELÉFONO (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] ACTIVIDAD
- [ ] DENOMINACIÓN DE LA ASEGURADORA
- [ ] DENOMINACIÓN SOCIAL
- [ ] DESCRIBIR LAS LESIONES O PATOLOGÍAS
- [ ] DOMICILIO LABORAL
- [ ] DOMICILIO PROFESIONAL
- [ ] EDAD
- [ ] EMPLEADOR
- [ ] FECHA
- [ ] FECHAS
- [ ] JORNADA
- [ ] NOMBRE DEL NOTARIO
- [ ] NOMBRE Y APELLIDOS DEL ABOGADO/A
- [ ] NOMBRE Y APELLIDOS DEL CÓNYUGE
- [ ] NOMBRE Y APELLIDOS DEL DEMANDADO
- [ ] NOMBRE Y APELLIDOS DEL DEMANDANTE
- [ ] NOMBRE Y APELLIDOS DEL PERITO
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº DE COLEGIADO
- [ ] NÚMERO DE AÑOS
- [ ] SEDE

## Normas que cita el formulario

- art. 24.1 LEC
- art. 399.1 LEC
- art. 769.1 LEC
- art. 770 LEC
- art. 86 CC
- art. 10.1 LEC
- art. 251 LEC
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 81.2.º CC
- art. 81 CC
- art. 97 CC
- art. 93 CC
- art. 142 CC
- art. 143 CC
- art. 151 CC
- art. 147 CC
- art. 146 CC
- art. 144 CC
- art. 149 CC
- art. 394 LEC
- art. 24.2 LEC
- art. 155.3 LEC

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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Junto a «…cluyendo recíprocas concesiones, y nada indica que deba desaparecer o reducirse.»: art. 97 CC en su redacción vigente; comprobar la numeración de las circunstancias del precepto tras las reformas posteriores a la Ley 15/2005.

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

AL TRIBUNAL DE INSTANCIA
SECCIÓN CIVIL – SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDANTE], con domicilio en [DOMICILIO], representación que acredito mediante escritura de poder otorgada a mi favor [ELEGIR UNA DE LAS TRES FORMAS DE OTORGAMIENTO DEL PODER, conforme al art. 24.1 LEC]:

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]
— mediante comparecencia electrónica, a través de la sede judicial electrónica, e inscrito en el Registro Electrónico de Apoderamientos Judiciales; y a cuya justificación acompaño certificación de dicho Registro aportada como Documento n.º [Nº DE DOCUMENTO], y que se puede acreditar mediante consulta automatizada orientada al dato, por parte del órgano judicial al cual tengo el honor de dirigirme.
— mediante comparecencia personal apud acta ante el Tribunal de Instancia de [LOCALIDAD], posteriormente inscrito en el Registro Electrónico de Apoderamientos Judiciales; y a cuya justificación acompaño certificación de dicho Registro aportada como Documento n.º [Nº DE DOCUMENTO], y que se puede acreditar mediante consulta automatizada orientada al dato, por parte del órgano judicial al cual tengo el honor de dirigirme.
— mediante escritura de poder otorgada a mi favor ante el Notario/Notaria [NOMBRE DEL NOTARIO], con Notaría sita en [LOCALIDAD]. El poder se inscribió en el Registro Electrónico de Apoderamientos Judiciales; lo cual justifico mediante certificación de dicho Registro aportada como Documento n.º [Nº DE DOCUMENTO], y que se puede acreditar mediante consulta automatizada orientada al dato, por parte del órgano judicial al cual tengo el honor de dirigirme.

Actúo bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS DEL ABOGADO/A], abogado/a en ejercicio, con despacho profesional abierto en [DOMICILIO PROFESIONAL], colegiado/a n.º [Nº DE COLEGIADO] del Ilustre Colegio de la Abogacía de [LOCALIDAD]. Ante el Tribunal comparezco y, como mejor en Derecho proceda, DIGO:

Que mediante el presente escrito vengo a formular DEMANDA DE DIVORCIO contra D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO], con domicilio, en primer lugar, en [DOMICILIO] [OPCIONAL — si ha lugar: y, en segundo lugar, el domicilio laboral en [DOMICILIO LABORAL]]; con correo electrónico [CORREO ELECTRÓNICO] y número de teléfono móvil [Nº DE TELÉFONO]; todo ello de conformidad con los hechos y fundamentos de derecho que se especificarán.

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa e, incluso, en una eventual fase de ejecución, por medios telemáticos, en los términos del art. 399.1, párrafo segundo, LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y número de teléfono: [CORREO ELECTRÓNICO] y [Nº DE TELÉFONO].

HECHOS

PRIMERO.– Mi mandante/mi mandante contrajo matrimonio [ELEGIR: canónico / civil] con D./Dña. [NOMBRE Y APELLIDOS DEL CÓNYUGE], en [LOCALIDAD], el día [DÍA] de [MES] de [AÑO]. Se acompaña la correspondiente certificación de matrimonio expedida por el Registro Civil de [LOCALIDAD] como DOCUMENTO N.º [Nº DE DOCUMENTO].

De dicha unión nacieron [NÚMERO] hijos que son menores de edad, de nombre [NOMBRE DEL HIJO/A] y [NOMBRE DEL HIJO/A], nacidos el [DÍA] de [MES] de [AÑO] y el [DÍA] de [MES] de [AÑO]. Se adjuntan las correspondientes certificaciones de nacimiento emitidas por el Registro Civil de [LOCALIDAD] como DOCUMENTOS n.os [Nº DE DOCUMENTO] y [Nº DE DOCUMENTO].

SEGUNDO.– Los casados cesaron efectivamente su convivencia conyugal desde hace [NÚMERO DE AÑOS] años, desde que convinieron en separarse de hecho, y como dato indudable que lo sustenta consta la escritura notarial de fecha [DÍA] de [MES] de [AÑO], que instauró la separación pactada personal, estableció convenio regulador y disolvió y liquidó el régimen de bienes, sin que haya existido ulterior reanudación de la convivencia (se aportan copia de la escritura pública y certificado de empadronamiento como DOCUMENTOS n.os [Nº DE DOCUMENTO] y [Nº DE DOCUMENTO]). Ahora es voluntad de mi mandante/mi mandante la disolución del vínculo mediante divorcio.

TERCERO.– No hay cuestión sobre que la guarda y custodia de los hijos menores se atribuya a mi mandante/mi mandante, y el patrimonio postconyugal ya se ha dividido, pero el demandado viene pidiendo la determinación de alimentos en cuantía inferior a la pactada para los hijos comunes y la eliminación de la pensión para el cónyuge demandante, razón por la que desde hace meses viene incumpliendo sus obligaciones.

Se pide aquí la ratificación de las condiciones de la separación extrajudicial pactada en el año [AÑO], es decir, [DESCRIBIR EL REPARTO PACTADO DE LOS INGRESOS DEL OBLIGADO ENTRE ALIMENTOS DE LOS HIJOS Y PENSIÓN AL CÓNYUGE, por ejemplo, la mitad de la nómina para alimentos de los hijos y la otra mitad para el cónyuge], lo que se ha venido cumpliendo hasta fechas recientes.

CUARTO.– Mi mandante/mi mandante se incorporó al mercado laboral en el año [AÑO], mediante contratos a tiempo parcial, en actividades de [ACTIVIDAD], y en la actualidad, aunque trabaja para [EMPLEADOR], carece de una real estabilidad, habiendo percibido [IMPORTE EN LETRA] euros brutos ([IMPORTE EN LETRA] euros líquidos) en el año [AÑO], y [IMPORTE EN LETRA] euros brutos ([IMPORTE EN LETRA] euros líquidos) en los [NÚMERO] primeros meses del año corriente, en labores de [JORNADA]. Se adjunta certificación de haberes como DOCUMENTO N.º [Nº DE DOCUMENTO].

Sin embargo, mi mandante/mi mandante padece [DESCRIBIR LAS LESIONES O PATOLOGÍAS] que, aunque no la incapacitan, llevan a asegurar que su vida laboral está limitada, como techo, a una actividad horaria y de sedentarización semejante a la que desarrolla; de modo que, habiendo realizado el esfuerzo de incorporación al mundo laboral, por lo que el desfase económico respecto a su situación de casada lógicamente tendería a desaparecer, no lo consigue por su estado de salud, sino que, en realidad, su penuria económica se convierte en irrecuperable, más allá del esfuerzo antedicho.

Se aporta dictamen del/la especialista Dr./Dra. [NOMBRE Y APELLIDOS DEL PERITO], que se propondrá como perito médico (PRUEBA PERICIAL).

QUINTO.– Para determinar los ingresos del demandado, debe admitirse que ha abandonado la empresa [DENOMINACIÓN SOCIAL], donde trabajaba desde antes de casarse, pero ello no disminuye su renta, al contrario de lo que sostiene.

Tal salida proviene de un plan de prejubilación conforme al cual, agotada la prestación contributiva de desempleo, pasa a percibir la asistencial para trabajadores mayores de cincuenta y dos años, hasta que cumpla la edad de [EDAD] años y se prejubile con el [PORCENTAJE] % de su base reguladora. Pero como complemento de dicha prestación, que le sirve para cotizar en un convenio especial de la Seguridad Social, la entidad [DENOMINACIÓN DE LA ASEGURADORA], en virtud de póliza de seguro colectivo que concertó la empresa que extinguió la relación laboral del demandado, abonará, el año [AÑO], hasta el [PORCENTAJE] % del neto mensual que constituye su sueldo de calificación, por lo que la pensión del demandado en los años venideros incluso estará ligeramente por encima de su salario actual, si se tiene en cuenta el tratamiento fiscal del complemento de pensión como renta irregular devengada a lo largo de los años de antigüedad de la relación laboral que se extingue hasta la cifra de capitalización de la indemnización legal.

Se acompaña copia de la información sindical difundida en la empresa que ha tenido ocasión de conseguir mi mandante/mi mandante (DOCUMENTO N.º [Nº DE DOCUMENTO]).

SEXTO.– La parte actora manifiesta que, previamente a la presentación de la presente demanda, se han llevado a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron conforme a los principios de buena fe, con la intención de alcanzar una solución satisfactoria; incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, mi representado/a envió un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por el demandado por el mismo medio, [ELEGIR: rechazando el acuerdo / habiendo sido solo posible un acuerdo parcial], viéndonos en la necesidad de acudir a la presente vía judicial respecto a los extremos de la controversia en los que se mantiene la discrepancia.

Acompaño como documento n.º [Nº DE DOCUMENTO] el requerimiento efectuado y como documento n.º [Nº DE DOCUMENTO] la contestación del demandado.

A estos hechos les son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

I.– Es competente el Tribunal de Instancia del lugar del domicilio del demandado, que es el criterio alternativo, a elección del demandante, conforme al art. 769.1, párrafo primero, LEC.

II.– El procedimiento adecuado es el del art. 770 LEC para conocer de las demandas de divorcio contenciosas.

III.– Tienen legitimación ordinaria, por hallarse en la situación jurídica de relación matrimonial, ambos cónyuges (art. 86 CC y art. 10.1 LEC), siendo el objeto de la pretensión la disolución vincular por divorcio.

IV.– Se fija la cuantía de la demanda, en lo que tiene de estimable, por razón de la pretensión de medidas que incluye reclamaciones de pensiones periódicas, acumulada a la disolución vincular, en [IMPORTE EN LETRA] euros, en armonía con la regla 7.ª del art. 251 LEC.

V.– La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4.º y 399.3 LEC en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VI.– El fondo de la pretensión consiste en la declaración de divorcio, a fin de la disolución del matrimonio, a instancia de uno de los cónyuges, de conformidad con el art. 81.2.º CC, por remisión del art. 86 CC, sin que pueda oponerse por el otro cónyuge ninguna causa de oposición material, al fundarse en la voluntad de no permanecer casado, como corolario legal del derecho del art. 32 CE a contraer matrimonio.

VII.– Aunque las medidas que prevé el art. 81, in fine, CC, al que reenvía el art. 86 CC, parecen ser las adoptadas en el seno de un proceso de separación o divorcio, y no las contratadas extrajudicialmente, al mismo resultado de ponderar la situación económica actual de los esposos, entre sí y con relación a sus hijos, conduce establecer unas medidas ex novo, o entender que se modifican las previamente acordadas por alteración sustancial de las circunstancias.

La pensión compensatoria que se pide, y que la demandante disfruta, a tenor de la naturaleza de la pensión del art. 97 CC, aunque articule una deuda duradera de cumplimiento periódico, tiene como evidente finalidad evitar que la ruptura del vínculo matrimonial suponga para uno de los casados un descenso en el nivel de vida efectivamente gozado durante el matrimonio; y no debe confundirse con una aportación al levantamiento de las cargas de una institución que viene a desaparecer definitivamente, ni tampoco con la obligación de alimentos.

Teniendo en cuenta los criterios legales, ha de resaltarse: 1.º) existe el acuerdo (art. 97 CC) a que llegaron los cónyuges en el año [AÑO], en el que el cónyuge acreedor recibía una pensión del [PORCENTAJE] % de los salarios del otro, en el seno de un convenio que además disolvía la comunidad matrimonial de bienes y liquidaba el patrimonio familiar; 2.º) el estado de salud del actor es deficiente y compromete su futuro laboral, limitándolo, en la expectativa actual de trabajo, a una actividad a tiempo parcial y sedentaria; 3.º) las necesidades del mantenimiento del nivel sociofamiliar, por lo que, hasta ahora, se ha aceptado esta medida de pensión, incluyendo recíprocas concesiones, y nada indica que deba desaparecer o reducirse.

La contribución de cada progenitor a los alimentos debidos a los hijos, que prevé el art. 93 CC, remite a los arts. 142 y siguientes CC. La finalidad de estos preceptos es diferente, y consiste en suministrar a una persona los medios necesarios para atender a su subsistencia, desenvolviendo una obligación basada en la relación de parentesco. Obligación también de tracto sucesivo, pero recíproca (art. 143 CC), irrenunciable, no transmisible, no compensable (salvo las pensiones atrasadas, ex art. 151 CC), que presupone, además del vínculo parental, un estado de necesidad en el alimentista (art. 147 CC) y la posibilidad económica en el obligado (arts. 146, 147 y 152 CC).

La prestación alimenticia para los hijos comunes, si se contempla desde la economía del progenitor custodio, necesariamente debe proceder, en tanto no se modifiquen las actuales circunstancias, de sus escasos ingresos salariales y de la pensión compensatoria que intenta equilibrar su situación económica en relación con la que gozaba casado/a, y que se confundirán con los alimentos debidos a los hijos desde la economía del otro progenitor, en tanto que, conviviendo con ellos, será el gestor y administrador de las cargas de la familia postmatrimonial.

Si conforme a los arts. 144 y 145 CC la obligación alimenticia (ya se ha dicho, moderada) es de ambos padres, un cónyuge prestaría alimentos de forma directa, a través de la atención directa y proporcionando vivienda, ex art. 149 CC, y sin asignación de cuota, del dinero de su salario y de la pensión compensatoria; y el otro, a través de una pensión de determinada cifra en metálico, que se sumará a la compensatoria, y que se debe mantener en su porcentaje, que arroja un cálculo aproximado de las cantidades que se solicitan.

VIII.– No hay ninguna razón para excluir la aplicación del principio del vencimiento en punto a las costas procesales (art. 394 LEC), debiéndose condenar al demandado que se oponga, dado que obtener la razón precisando de un proceso no ha de suponer una merma patrimonial del que tiene razón.

Y demás normas y jurisprudencia de general y pertinente aplicación.

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito con los documentos que se acompañan y sus copias, se digne admitirlos, tenerme por comparecido/a y parte en la representación que ostento, entendiéndose conmigo las sucesivas diligencias, y por formulada demanda de disolución del matrimonio por divorcio, de modo que, seguido que sea el pertinente procedimiento, se dicte en su día sentencia por la que se declare el divorcio de los esposos D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS], oficiándose al Registro Civil de [LOCALIDAD] para la anotación de su parte dispositiva en la inscripción del matrimonio, y se acuerden las siguientes medidas definitivas, que se podrán modificar si se alteraren sustancialmente las circunstancias:

1.– Atribución de la guarda y custodia de los hijos menores [NOMBRE DEL HIJO/A] y [NOMBRE DEL HIJO/A] al/a la demandante, en cuya compañía conviven, pudiendo comunicar con ellos el progenitor demandado como hasta la actualidad.

2.– Establecimiento de una pensión compensatoria a favor del/de la demandante de [IMPORTE EN LETRA] euros ([IMPORTE EN NÚMERO] €) mensuales, y sendas pensiones alimenticias a favor de [NOMBRE DEL HIJO/A] y de [NOMBRE DEL HIJO/A] de [IMPORTE EN LETRA] euros ([IMPORTE EN NÚMERO] €) mensuales, todas ellas a cargo del demandado D./Dña. [NOMBRE Y APELLIDOS], pagaderas por meses anticipados, mediante el sistema que se establezca en ejecución, si fuere menester, y actualizables anualmente conforme a las variaciones que experimente el Índice de Precios al Consumo que publique el Instituto Nacional de Estadística u organismo oficial que lo sustituya.

Es Justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a: [FIRMA] Firma del Procurador/a: [FIRMA]

NOTAS DE AYUDA

(1) A la hora de su acreditación, todos los poderes deben estar inscritos en el Registro Electrónico de Apoderamientos Judiciales (REAJ). Se supone que, para su acreditación, basta con la consulta automatizada orientada al dato de dicho Registro, que está a disposición de cualquier Letrado de la Administración de Justicia. Sin embargo, dado que el art. 24.2 LEC configura la certificación de dicha inscripción como vía subsidiaria de acreditación, para el caso de que el sistema no permita aquella consulta automatizada, se señala en el modelo que se acompaña certificación electrónica. El sistema permite emitir dicha certificación a quien inscribe el poder.

(2) El art. 155.3 LEC permite expresar varios domicilios del demandado (el que aparezca en el padrón municipal o conste oficialmente a estos efectos; el que aparezca en un registro oficial o en publicaciones de colegios profesionales, si se trata de empresas o personas colegiadas; donde desarrolle su actividad profesional o laboral no ocasional; si es empresa mercantil, el domicilio de cualquiera de sus administradores, gerentes o apoderados; o, si es asociación que consta en registro oficial, el domicilio del presidente, miembro o gestor de la Junta correspondiente). Cuando se señalen varios, se indicará el orden a seguir para la notificación, con vistas al éxito de la misma.

(3) El art. 155.3 LEC configura una obligación adicional del demandante, consistente en aportar cuantos datos sean de utilidad para localizar al demandado: número de identificación fiscal o de extranjeros, número de teléfono, dirección de correo electrónico o similares.
