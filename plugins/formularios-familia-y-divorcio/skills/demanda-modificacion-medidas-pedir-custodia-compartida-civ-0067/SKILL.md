---
name: demanda-modificacion-medidas-pedir-custodia-compartida-civ-0067
description: "Demanda de modificación de medidas para pedir custodia compartida (ley valenciana de 2011). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de modificación de medidas para pedir custodia compartida (ley valenciana de 2011)

> Formulario **CIV-0067** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de modificación de medidas para pedir custodia compartida (ley valenciana de 2011)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de modificación de medidas para pedir custodia compartida (ley valenciana de 2011)” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-modificacion-medidas-pedir-custodia-compartida-civ-0067`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] Nº DE DOCUMENTO (5 veces)
- [ ] AÑO (4 veces)
- [ ] DÍA (4 veces)
- [ ] MES (4 veces)
- [ ] NÚMERO (4 veces)
- [ ] SEDE (3 veces)
- [ ] CALLE (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] Nº DE ESTIPULACIÓN (2 veces)
- [ ] COLEGIO
- [ ] DATOS DEL PROCEDIMIENTO
- [ ] DESCRIPCIÓN DE LA MEDIDA
- [ ] FECHA
- [ ] LUGAR
- [ ] Nº
- [ ] OTROS DATOS
- [ ] PROFESIÓN

## Normas que cita el formulario

- art. 92 CC
- art. 142 CC
- art. 769 LEC
- art. 85.1 LOPJ
- art. 775 LEC
- art. 749.2 LEC
- art. 750 LEC
- art. 775.2 LEC
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 90.3 CC
- art. 91 CC
- art. 92.2 CC
- art. 92.6 CC
- art. 9.1 LO 1/1996
- art. 92.8 CC
- art. 146 CC
- art. 147 CC
- art. 96 CC
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

### Avisos de actualización (3) — se aplican en el texto, nunca se copian en el documento

- Junto a «…MILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Denominación legal: Sección de Familia, Infancia y Capacidad. Si no existe en el partido, conoce la Sección Civil o la Única (art. 86.3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «… [MES] de [AÑO], se dictó por el Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).
- Junto a «…curador ========================================================================»: requisito de procedibilidad del art. 5 LO 1/2025 — antes de presentar la demanda hay que intentar un medio adecuado de solución de controversias (MASC) y acreditarlo con la demanda (arts. 264.4.º y 399.3 LEC), salvo las materias excluidas del art. 5.2. Fuente: LO 1/2025, arts. 5 a 7 (BOE-A-2025-76).

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

D./Dª [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en nombre y representación de D./Dª [NOMBRE Y APELLIDOS], mayor de edad, de profesión [PROFESIÓN], con domicilio en [LOCALIDAD], calle [CALLE], nº [NÚMERO], pta., cuya representación acreditaré mediante comparecencia apud acta cuando sea requerido para ello (o representación que acredito mediante copia de poder para pleitos que ruego me sea devuelta una vez testimoniada en autos por necesitarla para otros usos), comparezco en este Tribunal con la asistencia del Letrado D./Dª [NOMBRE Y APELLIDOS], del Ilustre Colegio de Abogados de [COLEGIO], y DIGO:

Que por medio del presente escrito y en la representación que ostento, interpongo DEMANDA DE MODIFICACIÓN DE MEDIDAS DEFINITIVAS DE DIVORCIO O SEPARACIÓN, en el sentido que se expresa en el suplico de esta demanda, contra D./Dª [NOMBRE Y APELLIDOS], mayor de edad, con domicilio en [LOCALIDAD], calle [CALLE], nº [NÚMERO], pta. La presente demanda se basa en los siguientes

HECHOS

En fecha [DÍA] de [MES] de [AÑO], se dictó por el Tribunal de Instancia de [SEDE], plaza n.º [Nº] [OTROS DATOS], sentencia de divorcio o de separación, en el seno del procedimiento de Divorcio o de Separación de mutuo acuerdo [DATOS DEL PROCEDIMIENTO], en la que se procedió a aprobar el Convenio regulador de fecha [DÍA] de [MES] de [AÑO], presentado por las partes.

Se acompaña testimonio de la citada sentencia, como DOCUMENTO Nº [Nº DE DOCUMENTO]

En la estipulación [Nº DE ESTIPULACIÓN] del citado Convenio, en la que se regula el régimen de cuidado y convivencia con los hijos, se estableció un régimen de guarda y custodia individual a favor de la madre/del padre con régimen de visitas del padre/de la madre sobre el hijo menor de la pareja, [DESCRIPCIÓN DE LA MEDIDA] El tenor literal de la citada estipulación es el siguiente:

En relación con la medida anterior, se fijó, en la estipulación [Nº DE ESTIPULACIÓN] del referido Convenio, una pensión alimenticia de [IMPORTE] euros ( €) en favor del hijo menor de la pareja, antes citado, de periodicidad mensual y actualizable anualmente de acuerdo con las variaciones que experimente el IPC, a cargo del padre/madre, progenitor no custodio. El tenor literal de la citada estipulación es el siguiente:

Desde que se dictó la sentencia de divorcio/separación se ha producido una alteración sustancial y estable de las circunstancias atendidas las cuales se acordó en su momento un régimen de guarda y custodia individual a favor de la madre/padre, y la obligación del padre/madre de satisfacer una pensión periódica de alimentos a su hijo/a, que justifican la modificación de tales medidas en el sentido que se expondrá.

En efecto, el/la menor ha alcanzado una edad y, como consecuencia de ella, un grado de madurez que hace aconsejable atender de modo razonable a sus preferencias, las cuales se decantan por la convivencia con ambos padres en un régimen de paridad.

Por otra parte, el/la padre/madre del/de la menor, que por razones profesionales residía en una ciudad distinta a la del progenitor custodio, ha trasladado su residencia, de modo definitivo, a la misma localidad y zona. Ambas residencias, dada su ubicación, permitirían al menor asistir con comodidad a su colegio actual y seguir relacionándose con los mismos amigos y compañeros.

Debe subrayarse que el hecho de residir anteriormente en otra ciudad fue la única circunstancia por la que mi representado/a estuvo de acuerdo, en su momento, en convenir que la/el madre/padre quedara con la guarda y custodia individual.

La limitada relación que el actual régimen de visitas permiten al/a la menor con su padre/madre, ha generado en aquél, cuyo interés debe prevalecer sobre cualquier otro, un cuadro de ansiedad que se acredita con el informe médico que se acompaña como DOCUMENTO Nº [Nº DE DOCUMENTO], emitido por el Dr., que ha atendido al menor desde [FECHA], tal y como resulta del mismo informe. Este estado de frustración y ansiedad repercute negativamente en el desarrollo personal y afectivo del/de la menor.

Se aporta, igualmente, como DOCUMENTO Nº [Nº DE DOCUMENTO], informe emitido por el psicólogo D. [NOMBRE Y APELLIDOS], en el que se manifiesta la conveniencia de un régimen de convivencia igualitaria con ambos progenitores.

Hay que tener en cuenta que la reforma del Código civil regula expresamente la posibilidad de establecer la custodia compartida de los hijos tras la nulidad, separación o divorcio de los progenitores, en la misma línea que otras legislaciones forales, tal como se recogía en la Ley de la Comunidad Valenciana 5/2011, que mantuvo su aplicación a las situaciones jurídicas consolidadas, hasta su declaración de inconstitucionalidad por la STC 192/2016, de 16 de noviembre.

En este sentido, como indica la citada STC 192/2016, la fijación de un determinado régimen de guardia y custodia para los hijos menores se funda en la recta aplicación del principio que rige esta materia que no es otro que el del beneficio y protección del interés del menor, y en este sentido se prescribe el régimen de custodia compartida en los términos establecidos en el art. 92 del CC cuando, como en este caso, es el régimen en el que se protege adecuadamente el interés superior del menor.

En el caso presente, el menor es un adolescente que prefiere convivir igualitariamente con ambos progenitores; los domicilios de estos se encuentran cercanos, lo que permite al menor mantener el mismo entorno social y escolar; y mi representado/a tiene, al menos, la misma capacidad o aptitud para atender de modo adecuado a su hijo/a. Por ello no existe ningún motivo que justifique la denegación del régimen de convivencia compartida.

Los anteriores hechos hacen conveniente la sustitución del régimen de guarda y custodia individual por otro de custodia compartida, en los términos que se proponen a continuación:

Asimismo y en relación con lo anterior, procede sustituir el pago de la actual pensión de alimento a cargo del padre, que sólo tenía sentido en relación con el régimen de guarda y custodia individual, por la obligación de cada progenitor de mantener al menor durante el tiempo que conviva con él, además de satisfacer por mitad los gastos extraordinarios, tal y como se detalla a continuación:

"Ambos progenitores se harán cargo de los gastos en concepto de alimentos, en sentido amplio, que necesite el/la hijo/a mientras convivan con él, según el anterior régimen establecido.

Los gastos de colegios, institutos, facultades o universidades de carácter Público donde curse estudios el/la hijo/a, así como las matrículas, serán abonados por mitad por ambos progenitores. En el caso de Centros Privados, se sufragarán por mitad siempre que haya acuerdo por ambas partes. En caso de desacuerdo, el exceso que suponga sobre el Centro Público será sufragado por el progenitor que haya decidido que realicen los estudios en el Centro Privado que finalmente haya elegido. Los relativos a gastos por clases extraordinarias de repaso, viajes escolares de las menores, tanto si se llevan a cabo en el mismo colegio o en un centro externo, serán a cargo, por mitad, de ambos progenitores, siempre que previamente hayan prestado su conformidad o así vengan recomendados por el centro escolar. Caso contrario, serán sufragados por el progenitor que haya decidido su realización.

Otros gastos extraordinarios, en concreto aquellos de naturaleza médica necesarios, no cubiertos por la Seguridad Social ni por cualquier otra mutualidad u organismo, serán abonados por mitad por ambos progenitores.

Deberá imputarse a la mitad de gastos extraordinarios a cargo de D./Dª [NOMBRE Y APELLIDOS], la cantidad de [IMPORTE] euros, que le corresponde en concepto de compensación económica por la atribución del uso de la vivienda familiar, de su exclusiva propiedad, al progenitor custodio y a su hijo/a.

Si, tras cumplir los dieciocho años, el hijo se encuentra todavía en período de formación y no pueda mantenerse por sí mismo, ambos progenitores le prestarán los alimentos debidos de acuerdo con los arts. 142 y ss CC en proporción a sus respectivos recursos."

En relación con el uso de la vivienda familiar, que en la citada sentencia de divorcio/separación se atribuyó al progenitor custodio y al hijo menor en coherencia con el régimen de custodia individual, se solicita, igualmente la modificación de la medida. A tal efecto se propone que dicha medida sea sustituida por la siguiente:

Debe tenerse en cuenta que ambos progenitores cuentan con ingresos equiparables, de lo que resulta que no puede predicarse de ninguno de ellos la existencia de un interés más débil, que pueda determinar la atribución del uso de la vivienda familiar a su favor en el contexto de un régimen de custodia compartida. Se adjunta, para acreditar este extremo, como DOCUMENTOS Nº [Nº DE DOCUMENTO] y Nº [Nº DE DOCUMENTO] los siguientes:

La presente demanda se interpone tras haber intentado llegar a un acuerdo, sin éxito, con la otra parte, lo que se acredita con los siguiente DOCUMENTOS, que se acompañan bajo el Nº [NÚMERO] y

Resultan aplicables a los citados hechos los siguientes

FUNDAMENTOS DE DERECHO

COMPETENCIA.- Es competente el Tribunal al que me dirijo, de acuerdo con el artículo 769 LEC, en relación con lo dispuesto en el art. 85.1º LOPJ.

LEGITIMACIÓN.- La de ambas partes deriva del artículo 775 LEC. Conforme al art. 749.2 LEC, debe intervenir el Ministerio Fiscal, por encontrarse interesados menores de edad no emancipados.

PROCEDIMIENTO.- Arts. 775.2 y 770 LEC.

REPRESENTACIÓN Y DEFENSA.- El/La demandante comparece representado y defendido, respectivamente, por el Procurador y el Letrado que constan en el encabezamiento de este escrito, de acuerdo con lo dispuesto en el artículo 750 LEC, en relación con los artículos 775.2 y 770 LEC.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

DERECHO SUSTANTIVO.- El art. 775 LEC, según el cual los cónyuges podrán solicitar del tribunal la modificación de las medidas convenidas por ellos o de las adoptadas en defecto de acuerdo, "siempre que hayan variado sustancialmente las circunstancias tenidas en cuenta al aprobarlas o acordarlas".

El art. 90.3 CC, que dispone: “Las medidas que el Juez adopte en defecto de acuerdo o las convenidas por los cónyuges judicialmente, podrán ser modificadas judicialmente o por nuevo convenio aprobado por el Juez, cuando así lo aconsejen las nuevas necesidades de los hijos o el cambio de las circunstancias de los cónyuges”, "Asimismo, podrá modificarse el convenio o solicitarse modificación de las medidas sobre los animales de compañía si se hubieran alterado gravemente sus circunstancias" en relación con el art. 775 LEC, que regula la modificación de las medidas definitivas. En el mismo sentido, el art. 91 CC, señala que las medidas judiciales “podrán ser modificadas cuando se alteren sustancialmente las circunstancias”.

El art. 92.2 CC, que impone al Juez, cuando deba adoptar cualquier medida acerca de la custodia, el cuidado y la educación de los hijos menores, que vele por el cumplimiento de su derecho a ser oídos. Y el art. 92.6 CC en el mismo sentido. Ambos en relación con el art. 9.1 LO 1/1996, de 15 de enero.

El art. 92.8 CC que, aun en defecto de acuerdo de los padres, permite al Juez establecer la guarda y custodia compartida a instancia de uno de ellos cuando considere que solo de esta forma se protege adecuadamente el interés superior del menor.

El art. 14 CE, que prohíbe la discriminación por razón de sexo, de modo que este criterio no puede ser determinante a la hora de establecer el régimen de convivencia y relaciones de los progenitores con los hijos menores. En este sentido puede citarse, entre otras, la sentencia del Tribunal Constitucional, Sala 1ª. De 14 de julio de 2003, rec. 5559/2000. Las normas anteriores deben interpretarse a la luz del principio del favor filii, que resulta determinante en esta materia, y encuentra sustento, entre otras normas en el art. 39.2 CE, que consagra el principio de protección integral de los hijos. En este sentido, entre muchas otras, la STS, Civil, Sala 1a, de 1 de octubre de 2010, rec. 681/2007, señala que "la medida de la guarda y custodia compartida debe acordarse siempre en interés del menor, que es el criterio fundamental a tener en cuenta para tomar esta decisión, criterio que es independiente de las opiniones de quien deba adoptar dicha medida y que debe basarse en razones objetivas".

El art. 154.III.1 CC, en relación con los arts. 142 y ss. del Código civil; en especial, el art. 146 CC, según el cual, la cuantía de los alimentos será proporcionada al caudal o medios de quien los da y a las necesidades de quien los recibe; el art. 147 CC, en cuya virtud, los alimentos se reducirán o aumentarán proporcionalmente según el aumento o disminución que sufran las necesidades del alimentista y la fortuna del que hubiese de satisfacerlos.

El art. 96 CC en relación con la atribución del uso de la vivienda familiar. Según este precepto, el uso de la vivienda se atribuirá al progenitor custodio o al que presente el interés más digno de protección. Como ya se ha argumentado, al solicitarse la custodia compartida no tendría efecto el primero de los criterios, sin que ninguno de los cónyuges/ex cónyuges se encuentre en una posición de desigualdad económica que justifique basar en ella la atribución del uso de la vivienda.

De los hechos expuestos resulta una modificación objetiva, sustancial y permanente respecto de las circunstancias existentes en el momento en que se dictó la sentencia de divorcio/separación y se adoptaron las medidas cuya modificación se solicita, que hace conveniente que aquéllas se sustituyan, en interés del hijo, por las que se proponen en este escrito.

COSTAS.- Procede imponer al/a la demandado/a el pago de las costas, en virtud de lo dispuesto en el art. 394 LEC, en la medida en que se oponga a la presente demanda.

Iura novit curia y las demás normas que resulten procedentes.

Por lo expuesto

SUPLICO AL TRIBUNAL:

Que tras admitir este escrito con los documentos que lo acompañan y sus copias, me tenga por comparecido y parte en la representación que ostento, entendiéndose conmigo las sucesivas diligencias, y tenga por interpuesta DEMANDA DE MODIFICACIÓN DE MEDIDAS DEFINITIVAS DE DIVORCIO o de separación, que habrá de sustanciarse por los trámites del juicio verbal, contra D./Dª [NOMBRE Y APELLIDOS]; y, previos los trámites legales que procedan, dicte sentencia por la que, estimando íntegramente la demanda, se modifiquen las medidas dictadas por el Tribunal de Instancia de [SEDE], plaza n.º [NÚMERO], en la sentencia de divorcio o de separación de fecha [DÍA] de [MES] de [AÑO], relativas a los siguientes extremos: Régimen de custodia y relaciones de los progenitores con el/la hijo/a menor [NOMBRE Y APELLIDOS], y pensión de alimentos fijada en favor éste, resolviendo el paso a un régimen de custodia compartida con obligación de mantener cada uno de los progenitores al menor mientras esté en su compañía y reparto de los gastos extraordinarios en los términos detallados en los HECHOS CUARTO Y QUINTO de esta demanda. A saber: Así mismo, se solicita la modificación de la medida relativa a la atribución del uso de la vivienda familiar, que será sustituida por la propuesta en el HECHO SEXTO de esta demanda, del tenor siguiente: Todo ellos con expresa imposición de costas al/la demandado/a si se opusiere a la presente demanda.

OTROSÍ PRIMERO DIGO que se acompaña en anexo relación de documentos presentados con esta demanda, debidamente foliados y con índice electrónico, para su debida localización y consulta.

SUPLICO AL TRIBUNAL tenga hecha esta manifestación a los efectos oportunos y por aportados los documentos relacionados en el anexo.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma y número del Letrado	Firma del Procurador

========================================================================
