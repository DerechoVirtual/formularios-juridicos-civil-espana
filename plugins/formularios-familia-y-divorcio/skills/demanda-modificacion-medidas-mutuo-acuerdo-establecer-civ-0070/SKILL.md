---
name: demanda-modificacion-medidas-mutuo-acuerdo-establecer-civ-0070
description: "Demanda de modificación de medidas de mutuo acuerdo para establecer la custodia compartida. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de modificación de medidas de mutuo acuerdo para establecer la custodia compartida

> Formulario **CIV-0070** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda conjunta de ambos progenitores para modificar de mutuo acuerdo las medidas definitivas fijadas en una sentencia de divorcio o separación (guarda y custodia individual, pensión de alimentos y uso de la vivienda familiar) y sustituirlas por un régimen de guarda y custodia compartida, acompañada del convenio regulador de modificación (arts. 775.2 y 777 LEC).

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de modificación de medidas de mutuo acuerdo para establecer la custodia compartida» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de modificación de medidas de mutuo acuerdo para establecer la custodia compartida” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-modificacion-medidas-mutuo-acuerdo-establecer-civ-0070`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (10 veces)
- [ ] AÑO (9 veces)
- [ ] DÍA (9 veces)
- [ ] MES (9 veces)
- [ ] Nº (7 veces)
- [ ] Nº DE DOCUMENTO (6 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] DOMICILIO (4 veces)
- [ ] PISO Y PUERTA (4 veces)
- [ ] PROFESIÓN (4 veces)
- [ ] SEDE (4 veces)
- [ ] Nº DE ESTIPULACIÓN (3 veces)
- [ ] Nº DE PROCEDIMIENTO (3 veces)
- [ ] DNI/NIE (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] NOMBRE DEL HIJO/A (2 veces)
- [ ] Nº DE PÁGINA (2 veces)
- [ ] Nº DE TOMO (2 veces)
- [ ] COLEGIO
- [ ] DENOMINACIÓN DEL ÓRGANO
- [ ] IMPORTE EN LETRA
- [ ] NOMBRE Y APELLIDOS DEL HIJO/A
- [ ] NOMBRE Y APELLIDOS DEL LETRADO/A
- [ ] NOMBRE Y APELLIDOS DEL PRIMER CÓNYUGE
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] NOMBRE Y APELLIDOS DEL SEGUNDO CÓNYUGE
- [ ] TRANSCRIBIR LA ESTIPULACIÓN
- [ ] TRANSCRIBIR LA ESTIPULACIÓN QUE ATRIBUYE EL USO DE LA VIVIENDA FAMILIAR
- [ ] TRANSCRIBIR LA ESTIPULACIÓN QUE FIJA LA PENSIÓN DE ALIMENTOS

## Normas que cita el formulario

- art. 769 LEC
- art. 777.1 LEC
- art. 775.2 LEC
- art. 775 LEC
- art. 90 CC
- art. 749.2 LEC
- art. 750 LEC
- art. 90.2 CC
- art. 90.3 CC
- art. 91 CC
- art. 92.2 CC
- art. 92.6 CC
- art. 9.1 Ley Orgánica 1/1996
- art. 92.5 CC
- art. 93 CC
- art. 142 Código Civil
- art. 146 CC
- art. 147 CC
- art. 96 CC
- art. 142 CC

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

- Junto a «…O]. Firma y número de colegiado del/de la Letrado/a Firma del/de la Procurador/a»: requisito de procedibilidad (art. 5 LO 1/2025): antes de demandar hay que intentar un medio adecuado de solución de controversias y acreditarlo con la demanda, salvo las materias excluidas del art. 5.2. Al tratarse de una petición conjunta y de mutuo acuerdo, comprobar si resulta de aplicación alguna de las exclusiones del art. 5.2.

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

A LA SECCIÓN [ELEGIR: DE FAMILIA, INFANCIA Y CAPACIDAD / CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS DEL PRIMER CÓNYUGE], mayor de edad, de profesión [PROFESIÓN], con domicilio en [LOCALIDAD], calle [DOMICILIO], n.º [Nº], piso/puerta [PISO Y PUERTA], y de D./Dña. [NOMBRE Y APELLIDOS DEL SEGUNDO CÓNYUGE], mayor de edad, de profesión [PROFESIÓN], con domicilio en [LOCALIDAD], calle [DOMICILIO], n.º [Nº], piso/puerta [PISO Y PUERTA], cuya representación acreditaré mediante comparecencia apud acta cuando sea requerido para ello, comparezco en este TRIBUNAL con la asistencia del/de la Letrado/a D./Dña. [NOMBRE Y APELLIDOS DEL LETRADO/A], del Ilustre Colegio de Abogados de [COLEGIO], y DIGO:

Que por medio del presente escrito y en la representación que ostento, interpongo DEMANDA DE MODIFICACIÓN DE MEDIDAS DEFINITIVAS DE [ELEGIR: DIVORCIO / SEPARACIÓN], de mutuo acuerdo. La presente demanda se basa en los siguientes

HECHOS

PRIMERO.- En fecha [DÍA] de [MES] de [AÑO] se dictó por la Sección [ELEGIR: Civil / de Familia, Infancia y Capacidad] del Tribunal de Instancia de [SEDE], plaza n.º [Nº], sentencia de [ELEGIR: divorcio / separación], en el seno del procedimiento de [ELEGIR: divorcio / separación] de mutuo acuerdo n.º [Nº DE PROCEDIMIENTO], en la que se procedió a aprobar el Convenio regulador de fecha [DÍA] de [MES] de [AÑO], presentado por las partes.

En la estipulación [Nº DE ESTIPULACIÓN] del citado Convenio, judicialmente homologado, en la que se regula el régimen de cuidado y convivencia con los hijos, se estableció un régimen de guarda y custodia individual a favor de [ELEGIR: la madre / el padre], con régimen de visitas de [ELEGIR: el padre / la madre] sobre el/la hijo/a menor de la pareja, [NOMBRE DEL HIJO/A]. El tenor literal de la citada estipulación es el siguiente: [TRANSCRIBIR LA ESTIPULACIÓN].

En relación con la medida anterior, se fijó, en la estipulación [Nº DE ESTIPULACIÓN] del referido Convenio, una pensión alimenticia de [IMPORTE EN LETRA] euros ([IMPORTE] €) en favor del/de la hijo/a menor de la pareja, antes citado/a, de periodicidad mensual y actualizable anualmente de acuerdo con las variaciones que experimente el IPC, a cargo del progenitor no custodio. El tenor literal de la citada estipulación es el siguiente: [TRANSCRIBIR LA ESTIPULACIÓN QUE FIJA LA PENSIÓN DE ALIMENTOS].

Asimismo, en la estipulación [Nº DE ESTIPULACIÓN] del mismo Convenio se atribuyó el uso de la vivienda familiar al progenitor custodio y al/a la hijo/a menor, en interés de éste/a. El tenor literal de la citada estipulación es el siguiente: [TRANSCRIBIR LA ESTIPULACIÓN QUE ATRIBUYE EL USO DE LA VIVIENDA FAMILIAR].

Se acompaña, para acreditar los anteriores extremos, testimonio de la citada sentencia de [ELEGIR: divorcio / separación], en el que consta la firmeza de la misma, como DOCUMENTO N.º [Nº DE DOCUMENTO].

SEGUNDO.- Desde que se dictó la sentencia de [ELEGIR: divorcio / separación] se ha producido una alteración sustancial y estable de las circunstancias atendidas las cuales se acordó en su momento un régimen de guarda y custodia individual a favor de [ELEGIR: la madre / el padre], y la obligación de [ELEGIR: el padre / la madre] de satisfacer una pensión periódica de alimentos a su hijo/a, así como la atribución del uso de la vivienda habitual al progenitor custodio junto con el/la hijo/a menor, que justifican la modificación de tales medidas en el sentido que se expondrá.

En efecto, el/la menor ha alcanzado una edad y, como consecuencia de ella, un grado de madurez que hace aconsejable atender de modo razonable a sus preferencias, las cuales se decantan por la convivencia con ambos padres en un régimen de paridad.

Por otra parte, [ELEGIR: el padre / la madre] del/de la menor, que por razones profesionales residía en una ciudad distinta a la del otro progenitor, con quien el/la menor convive en la actualidad, ha trasladado su residencia, de modo definitivo, a la misma localidad y zona. Ambas residencias, dada su ubicación, permitirían al/a la menor asistir con comodidad a su colegio actual y seguir relacionándose con los mismos amigos y compañeros.

Debe subrayarse que el hecho de residir anteriormente en otra ciudad fue la única circunstancia por la que mis representados convinieron en su momento que [ELEGIR: la madre / el padre] quedara con la guarda y custodia individual.

Hay que tener en cuenta, además, que con posterioridad a la citada sentencia se produjo la reforma del Código Civil por Ley 15/2005, de 8 de julio, regulándose expresamente la posibilidad de establecer la custodia compartida de los hijos tras la nulidad, separación o divorcio de los progenitores. En concreto, el art. 92.5 dispone que "se acordará el ejercicio compartido de la guarda y custodia de los hijos cuando así lo soliciten los padres", encontrándose ambos padres de acuerdo, en el presente caso, en que el régimen de custodia compartida es el que mejor se ajusta en la actualidad al interés superior del hijo.

Estos hechos hacen conveniente la sustitución del régimen de guarda y custodia individual por otro de guarda y custodia compartida, en los términos que proponen mis representados de común acuerdo y que se contienen en el CONVENIO REGULADOR DE MODIFICACIÓN DE LAS MEDIDAS DEFINITIVAS ANTERIORES que se acompaña a la presente demanda como DOCUMENTO N.º [Nº DE DOCUMENTO].

TERCERO.- Asimismo, y en relación con lo anterior, mis representados convienen que se sustituya el pago de la actual pensión de alimentos a cargo de [ELEGIR: el padre / la madre], que sólo tenía sentido en relación con el régimen de guarda y custodia individual, por la obligación de cada progenitor de mantener al menor durante el tiempo que conviva con él, además de satisfacer por mitad los gastos extraordinarios, tal y como se detalla en el citado CONVENIO REGULADOR que se acompaña a la presente demanda como DOCUMENTO N.º [Nº DE DOCUMENTO].

CUARTO.- En relación con el uso de la vivienda familiar, que en la referida sentencia se atribuyó al progenitor custodio y al/a la hijo/a menor en coherencia con el régimen de custodia individual, se solicita igualmente la modificación de la medida. A tal efecto se propone que dicha medida, al igual que las anteriores, sea sustituida por la que se acuerda en el CONVENIO REGULADOR que se acompaña a la presente demanda como DOCUMENTO N.º [Nº DE DOCUMENTO].

FUNDAMENTOS DE DERECHO

I. COMPETENCIA.- Es competente el Tribunal al que me dirijo, de acuerdo con el art. 769 LEC y el art. 777.1 LEC, por remisión del art. 775.2 LEC.

II. LEGITIMACIÓN.- La de ambas partes deriva del art. 775 LEC y de los arts. 90 y 91 CC. Conforme al art. 749.2 LEC, debe intervenir el Ministerio Fiscal, por encontrarse interesados menores.

III. PROCEDIMIENTO.- Arts. 775.2 y 777 LEC.

IV. REPRESENTACIÓN Y DEFENSA.- Mis mandantes comparecen representados y defendidos, respectivamente, por el/la Procurador/a y el/la Letrado/a que constan en el encabezamiento de este escrito, de acuerdo con lo dispuesto en el art. 750 LEC, en relación con el art. 775.2 LEC.

V. DERECHO SUSTANTIVO.- El art. 775 LEC, según el cual los cónyuges podrán solicitar del tribunal la modificación de las medidas convenidas por ellos o de las adoptadas en defecto de acuerdo, "siempre que hayan variado sustancialmente las circunstancias tenidas en cuenta al aprobarlas o acordarlas". El mismo precepto añade, en su apartado 2, que "estas peticiones se tramitarán conforme a lo dispuesto en el artículo 770. No obstante, si la petición se hiciera por ambos cónyuges de común acuerdo o por uno con el consentimiento del otro y acompañando propuesta de convenio regulador, regirá el procedimiento establecido en el artículo 777". En el caso presente, la petición de modificación de medidas definitivas se realiza de mutuo acuerdo, acompañándose a este escrito el preceptivo convenio regulador como DOCUMENTO N.º [Nº DE DOCUMENTO].

El art. 90.2, primer inciso CC, en cuanto determina que "Los acuerdos de los cónyuges adoptados para regular las consecuencias de la nulidad, separación y divorcio presentados ante el órgano judicial serán aprobados por el Juez salvo si son dañosos para los hijos o gravemente perjudiciales para uno de los cónyuges". Si fueran gravemente perjudiciales para el bienestar de los animales de compañía, la autoridad judicial ordenará las medidas a adoptar, sin perjuicio del convenio aprobado.

El art. 90.3 CC, que dispone: "Las medidas que el Juez adopte en defecto de acuerdo o las convenidas por los cónyuges judicialmente, podrán ser modificadas judicialmente o por nuevo convenio aprobado por el Juez, cuando así lo aconsejen las nuevas necesidades de los hijos o el cambio de las circunstancias de los cónyuges". Asimismo, podrá modificarse el convenio o solicitarse modificación de las medidas sobre los animales de compañía si se hubieran alterado gravemente sus circunstancias, en relación con el art. 775 LEC, que regula la modificación de las medidas definitivas. En el mismo sentido, el art. 91 CC señala que las medidas judiciales "podrán ser modificadas cuando se alteren sustancialmente las circunstancias".

El art. 92.2 CC, que impone al Juez, cuando deba adoptar cualquier medida acerca de la custodia, el cuidado y la educación de los hijos menores, que vele por el cumplimiento de su derecho a ser oídos. Y el art. 92.6 CC en el mismo sentido. Ambos en relación con el art. 9.1 de la Ley Orgánica 1/1996, de 15 de enero.

El art. 92.5 CC, según el cual "se acordará el ejercicio compartido de la guarda y custodia de los hijos cuando así lo soliciten los padres en la propuesta de convenio regulador o cuando ambos lleguen a este acuerdo en el transcurso del procedimiento".

El art. 93 CC, conforme al cual el Juez asegurará la acomodación de las prestaciones de alimentos a favor de los hijos a las circunstancias económicas y necesidades de éstos en cada momento.

El art. 154, párrafo tercero, 1.º CC, en relación con los arts. 142 y siguientes del Código Civil; en especial, el art. 146 CC, según el cual la cuantía de los alimentos será proporcionada al caudal o medios de quien los da y a las necesidades de quien los recibe; y el art. 147 CC, en cuya virtud los alimentos se reducirán o aumentarán proporcionalmente según el aumento o disminución que sufran las necesidades del alimentista y la fortuna del que hubiese de satisfacerlos.

El art. 96 CC, en relación con la atribución del uso de la vivienda familiar.

De los hechos expuestos resulta una modificación objetiva, sustancial y permanente respecto de las circunstancias existentes en el momento de la adopción de las medidas cuya modificación se solicita. Esto, junto con el acuerdo alcanzado por las partes en relación con la citada modificación, que redunda en interés del hijo, justifica que se acuerde la misma.

VI. Iura novit curia y las demás normas que resulten procedentes.

Por lo expuesto,

SUPLICO AL TRIBUNAL:

Que, tras admitir este escrito con los documentos que lo acompañan y sus copias, me tenga por comparecido/a y parte en la representación que ostento, entendiéndose conmigo las sucesivas diligencias, tenga por interpuesta DEMANDA DE MUTUO ACUERDO DE MODIFICACIÓN DE MEDIDAS DEFINITIVAS DE [ELEGIR: DIVORCIO / SEPARACIÓN] y, previos los trámites legales que procedan, dicte sentencia por la que, estimando íntegramente la demanda, se modifiquen las medidas dictadas por la Sección [ELEGIR: Civil / de Familia, Infancia y Capacidad] del Tribunal de Instancia de [SEDE], plaza n.º [Nº], en la sentencia de [ELEGIR: divorcio / separación] de fecha [DÍA] de [MES] de [AÑO], relativas a los siguientes extremos: régimen de guarda y custodia y pensión de alimentos fijada en favor del hijo menor de los cónyuges, [NOMBRE Y APELLIDOS DEL HIJO/A], y atribución del uso de la vivienda familiar, resolviendo el paso a un régimen de guarda y custodia compartida con obligación de mantener cada uno de los progenitores al menor mientras esté en su compañía y reparto de los gastos extraordinarios, y la extinción de la atribución del uso de la vivienda familiar al progenitor hasta ahora custodio, conforme a lo estipulado en el CONVENIO REGULADOR que se acompaña a esta demanda como DOCUMENTO N.º [Nº DE DOCUMENTO], cuya homologación se solicita.

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma y número de colegiado del/de la Letrado/a Firma del/de la Procurador/a

CONVENIO REGULADOR DE MODIFICACIÓN DEL APROBADO POR SENTENCIA DE [ELEGIR: DIVORCIO / SEPARACIÓN] DE FECHA [DÍA] DE [MES] DE [AÑO], DICTADA POR EL TRIBUNAL [DENOMINACIÓN DEL ÓRGANO] EN AUTOS [Nº DE PROCEDIMIENTO]

En la ciudad de [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

REUNIDOS

De una parte, D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de profesión [PROFESIÓN], con domicilio en [LOCALIDAD], calle [DOMICILIO], n.º [Nº], piso/puerta [PISO Y PUERTA], con DNI/NIF [DNI/NIE].

Y de otra, D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de profesión [PROFESIÓN], con domicilio en [LOCALIDAD], calle [DOMICILIO], n.º [Nº], piso/puerta [PISO Y PUERTA], con DNI/NIF [DNI/NIE].

Intervienen ambos en su propio nombre y derecho, y se reconocen mutuamente la capacidad legal necesaria para otorgar el presente convenio regulador, a cuyo efecto

MANIFIESTAN

I.- Con fecha [DÍA] de [MES] de [AÑO], los comparecientes contrajeron matrimonio [ELEGIR: canónico / civil] en [LOCALIDAD], que se encuentra inscrito en el Registro Civil de [LOCALIDAD], Sección 2.ª, Tomo [Nº DE TOMO], Página [Nº DE PÁGINA].

II.- De dicho matrimonio ha nacido y vive un/a hijo/a, [NOMBRE DEL HIJO/A], nacido/a en [LOCALIDAD], el [DÍA] de [MES] de [AÑO], de conformidad con la inscripción obrante en el Registro Civil de [LOCALIDAD], Sección 1.ª, Tomo [Nº DE TOMO], Página [Nº DE PÁGINA], y, por tanto, menor de edad.

III.- El matrimonio quedó disuelto [ELEGIR: o separado] por sentencia de fecha [DÍA] de [MES] de [AÑO], dictada por la Sección [ELEGIR: Civil / de Familia, Infancia y Capacidad] del Tribunal de Instancia de [SEDE], plaza n.º [Nº], en los autos de procedimiento de [ELEGIR: divorcio / separación] de mutuo acuerdo n.º [Nº DE PROCEDIMIENTO], siendo ésta firme. En dicha sentencia se homologó el convenio regulador presentado por los cónyuges.

IV.- Desde que se dictó la sentencia de [ELEGIR: divorcio / separación] se ha producido una alteración sustancial y estable de las circunstancias atendidas las cuales se acordó en su momento un régimen de guarda y custodia individual a favor de [ELEGIR: la madre / el padre], y la obligación de [ELEGIR: el padre / la madre] de satisfacer una pensión periódica de alimentos a su hijo/a, así como la atribución del uso de la vivienda habitual al progenitor custodio junto con el/la hijo/a menor, que justifican la modificación de tales medidas de acuerdo con las siguientes

ESTIPULACIONES

PRIMERA.- Guarda y custodia compartida.

El/La hijo/a menor de edad quedará bajo la guarda y custodia compartida de ambos progenitores, por considerar este sistema el más adecuado para el buen desarrollo, educación y equilibrio emocional del hijo/a, lo que se llevará a efecto de conformidad con cuanto sigue:

1. El padre y la madre acuerdan expresamente que cuantas decisiones sean necesarias en cuestiones que afecten directa o indirectamente al/a la menor serán consultadas y decididas por ambos progenitores. En este sentido se fijan como de inexcusable consenso las medidas que conciernan al hijo/a referentes a elección de colegio, clases particulares, actividades extraescolares, cursos en el extranjero, viajes o salidas al extranjero en los que no vayan acompañados por algún progenitor, tratamientos médicos o intervenciones quirúrgicas, etc.

En virtud del derecho-deber que tienen los progenitores de velar por el/la hijo/a menor de edad, cuando se encuentre bajo la custodia de uno (guarda y custodia) u otro progenitor (régimen de visitas y estancias), deberán informarse mutuamente y de manera inmediata de cualquier circunstancia que acontezca respecto del/de la menor y que tenga carácter relevante, y muy especialmente de cualquier enfermedad, favoreciendo y facilitando el contacto. Igualmente, ambos progenitores tendrán derecho a estar informados del rendimiento escolar, para lo cual tendrán pleno derecho a asistir y recibir cuanta información requieran del Colegio donde asista el/la menor.

2.- La guarda y custodia se atribuye al padre y a la madre por periodos alternativos de una semana, comenzando por [ELEGIR: el padre / la madre]. No se computan los meses de julio y agosto, por corresponder a estancias vacacionales.

3.- En el periodo en que un progenitor tenga la guarda y custodia del/de la menor, se establece para el otro el siguiente régimen de visitas:

Durante la semana fuera de períodos vacacionales.

Fines de semana.

El/La menor estará con el progenitor que no tenga la guarda los domingos desde las 9 h, que lo recogerá en el domicilio del progenitor que tenga la guarda, y se encargará de llevarlo al colegio los lunes por la mañana.

De lunes a viernes.

El/La menor estará con el progenitor que no tenga la guarda un día entre semana -de no acordar otra cosa ambos progenitores, será el miércoles- desde la salida del colegio, o en su defecto las 17 horas, hasta las 21 horas, momento en el que será reintegrado/a en el domicilio del progenitor que tenga la guarda y custodia del/de la menor esa semana.

Días festivos y puentes escolares fuera de períodos vacacionales.

Se distribuirán por mitad entre el padre y la madre. En caso de desacuerdo sobre la concreta distribución, [ELEGIR: la madre / el padre] tendrá preferencia para elegir si el menor permanece con ella/él o con el otro progenitor el primer festivo o puente que se presente. En el siguiente, el/la menor permanecerá con el otro progenitor y, a partir de ahí, se irán alternando las estancias con uno y otro. Los puentes no se dividirán, salvo que ambos progenitores acuerden lo contrario.

Vacaciones de Navidad, Semana Santa y Verano.

Las vacaciones escolares de Navidad, Semana Santa y Verano serán repartidas por mitad entre los progenitores, correspondiendo a [ELEGIR: la madre / el padre] la primera mitad los años pares y la segunda los impares, y al otro progenitor a la inversa, salvo que ambos acuerden otro reparto diferente, haciéndose las siguientes puntualizaciones:

Primera. La recogida del/de la menor será a las 11 horas del primer día de vacaciones y finalizará a las 21 horas del último día que corresponda al que disfruta del primer periodo, o a las 21 horas del último día de las vacaciones escolares para el que disfrute del segundo periodo.

Segunda. En las vacaciones de Navidad, en todo caso, con independencia de a qué progenitor corresponda cada periodo, se considerarán aparte los siguientes días: Nochebuena, que corresponderá a [ELEGIR: el padre / la madre], y Navidad, que corresponderá al otro progenitor.

Tercera. Las vacaciones de verano comprenderán los meses de julio y agosto, y se distribuirán en cuatro quincenas, correspondiendo a [ELEGIR: el padre / la madre] elegir en los años impares las dos quincenas que estará con el/la menor, y al otro progenitor en los pares, pudiendo ser consecutivas las referidas quincenas.

Comunicaciones telefónicas.

Ambos progenitores podrán comunicarse telefónicamente con su hijo/a con total libertad, respetándose para este tipo de comunicación el horario de descanso o estudio del/de la menor. Para el caso de que en periodo de vacaciones escolares se marchara de viaje, ambos progenitores se facilitarán un teléfono de contacto o colaborarán en que el/la menor efectúe la pertinente llamada telefónica. Todo ello se llevará a efecto dentro de criterios de flexibilidad y atendiendo siempre, prioritariamente, al interés del/de la hijo/a.

SEGUNDA.- Alimentos en favor del hijo común.

Ambos progenitores se harán cargo de los gastos en concepto de alimentos, en sentido amplio, que necesite el/la hijo/a cuando esté bajo la respectiva custodia de uno y otro, según el régimen establecido en la estipulación anterior.

Los gastos de colegios, institutos, facultades o universidades de carácter público donde curse estudios el/la hijo/a, así como las matrículas, serán abonados por mitad por ambos progenitores. En el caso de centros privados, se sufragarán por mitad siempre que haya acuerdo por ambas partes. En caso de desacuerdo, el exceso que suponga sobre el centro público será sufragado por el progenitor que haya decidido que realice los estudios en el centro privado que finalmente haya elegido. Los relativos a gastos por clases extraordinarias de repaso y viajes escolares del/de la menor, tanto si se llevan a cabo en el mismo colegio como en un centro externo, serán a cargo, por mitad, de ambos progenitores, siempre que previamente hayan prestado su conformidad o así vengan recomendados por el centro escolar. En caso contrario, serán sufragados por el progenitor que haya decidido su realización.

Otros gastos extraordinarios, en concreto aquellos de naturaleza médica necesarios, no cubiertos por la Seguridad Social ni por cualquier otra mutualidad u organismo, serán abonados por mitad por ambos progenitores.

[OPCIONAL — incluir si procede]

Deberá imputarse a la mitad de gastos extraordinarios a cargo de D./Dña. [NOMBRE Y APELLIDOS] la cantidad de [IMPORTE] euros, que le corresponde en concepto de compensación económica por la atribución del uso de la vivienda familiar, de su exclusiva propiedad, al progenitor custodio y a su hijo/a.

Si, tras cumplir los dieciocho años, el hijo se encuentra todavía en período de formación y no puede mantenerse por sí mismo, ambos progenitores le prestarán los alimentos debidos de acuerdo con los arts. 142 y siguientes CC, en proporción a sus respectivos recursos.

TERCERA.- Atribución del uso de la vivienda familiar.

Se acuerda la extinción del uso de la vivienda familiar atribuido en la sentencia de [ELEGIR: divorcio / separación] al progenitor hasta ahora custodio.

Y, en prueba de conformidad, y para someterlo a la aprobación judicial, lo firman por triplicado los comparecientes en la ciudad y fecha indicados en el encabezamiento.

Fdo.: [NOMBRE Y APELLIDOS] Fdo.: [NOMBRE Y APELLIDOS]
