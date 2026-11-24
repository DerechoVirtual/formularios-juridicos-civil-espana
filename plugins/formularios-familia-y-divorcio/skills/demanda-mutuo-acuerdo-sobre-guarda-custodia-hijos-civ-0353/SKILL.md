---
name: demanda-mutuo-acuerdo-sobre-guarda-custodia-hijos-civ-0353
description: "Demanda de mutuo acuerdo sobre guarda y custodia de hijos menores tras ruptura de unión de hecho. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de mutuo acuerdo sobre guarda y custodia de hijos menores tras ruptura de unión de hecho

> Formulario **CIV-0353** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda de mutuo acuerdo para que el tribunal homologue el convenio suscrito por los progenitores sobre guarda y custodia, régimen de comunicaciones y estancias de los hijos menores comunes tras la ruptura de una unión de hecho (pareja no casada), por el cauce del art. 777 LEC, con intervención del Ministerio Fiscal.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de mutuo acuerdo sobre guarda y custodia de hijos menores tras ruptura de unión de hecho» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de mutuo acuerdo sobre guarda y custodia de hijos menores tras ruptura de unión de hecho” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-mutuo-acuerdo-sobre-guarda-custodia-hijos-civ-0353`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] FECHA (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] DOMICILIO (2 veces)
- [ ] NOMBRE (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] PÁGINA (2 veces)
- [ ] TOMO (2 veces)
- [ ] AÑO
- [ ] COLEGIO
- [ ] DATOS Y CIRCUNSTANCIAS DE IDENTIFICACIÓN DE LOS PROGENITORES
- [ ] DÍA
- [ ] MES
- [ ] NOMBRE Y APELLIDOS DEL LETRADO/A
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº DE COLEGIADO
- [ ] Nº DE DOCUMENTOS
- [ ] NÚMERO
- [ ] OTROS HECHOS RELEVANTES, SI LOS HUBIERA.
- [ ] SEDE

## Normas que cita el formulario

- art. 6 LEC
- art. 154 CC
- art. 769.3 LEC
- art. 777 LEC
- art. 748.4.º LEC
- art. 777.1 LEC
- art. 770.5.ª LEC
- art. 750.2 LEC
- art. 159 Código Civil
- art. 92 CC
- art. 90 CC
- art. 749.2 LEC

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

AL TRIBUNAL DE INSTANCIA DE [SEDE]
SECCIÓN CIVIL
SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, que actúa en nombre y representación de D. [NOMBRE Y APELLIDOS] y Dña. [NOMBRE Y APELLIDOS] [DATOS Y CIRCUNSTANCIAS DE IDENTIFICACIÓN DE LOS PROGENITORES], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento n.º [Nº DE DOCUMENTO], bajo dirección del Letrado/a D./Dña. [NOMBRE Y APELLIDOS DEL LETRADO/A], colegiado/a n.º [Nº DE COLEGIADO] del Ilustre Colegio de Abogados de [COLEGIO], cuyo despacho se abre en [LOCALIDAD], calle [DOMICILIO], ante el Tribunal comparezco y, como mejor en Derecho proceda, DIGO:

Que por medio del presente escrito, siguiendo las instrucciones de mis mandantes, vengo a formular demanda de mutuo acuerdo sobre GUARDA Y CUSTODIA DE HIJOS MENORES, con base en los siguientes:

HECHOS

PRIMERO.– Doña [NOMBRE Y APELLIDOS] y Don [NOMBRE Y APELLIDOS] formaron familia natural desde la fecha [FECHA], en la que iniciaron su relación paramatrimonial con intención de permanencia y consolidación, y fruto de esta unión nacieron dos hijos: A [NOMBRE], nacido el [FECHA], inscrito en el Registro Civil de [LOCALIDAD], tomo [TOMO], página [PÁGINA]; y B [NOMBRE], nacido el [FECHA], inscrito en el Registro Civil de [LOCALIDAD], tomo [TOMO], página [PÁGINA], por consiguiente menores de edad. Ambos aparecen inscritos como hijos de los dos litigantes, según se demuestra con las certificaciones literales de nacimiento que se acompañan como documentos números [Nº DE DOCUMENTOS].

Esta convivencia lo ha sido con carácter paramatrimonial, en el sentido de relación afectiva semejante a la de las parejas casadas, estable y duradera, puesto que alcanzó [NÚMERO] años, apareciendo ante los vecinos, amigos, compañeros de trabajo y familiares como pareja, compartiendo techo, ingresos y vida sentimental, siendo el último domicilio común [DOMICILIO].

SEGUNDO.– Hace unos meses Doña [NOMBRE Y APELLIDOS] y Don [NOMBRE Y APELLIDOS] decidieron poner fin a la convivencia en pareja por desavenencias que no vienen al caso, suscribiendo un convenio en el que regulaban lo relativo a guarda, custodia y régimen de comunicaciones y estancias de los hijos comunes.

Se adjunta al presente escrito, como documento número [Nº DE DOCUMENTO], el convenio firmado por ambos progenitores para su homologación judicial.

TERCERO.– [OTROS HECHOS RELEVANTES, SI LOS HUBIERA.]

A los anteriores hechos son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

I.– CAPACIDAD.

Mis representados ostentan la capacidad procesal necesaria conforme a lo establecido en los arts. 6 y siguientes LEC.

II.– LEGITIMACIÓN.

La legitimación para intervenir en el procedimiento corresponde a ambos progenitores, habida cuenta de que son los que se hallan en la situación jurídica respectiva del derecho-deber de velar por los hijos menores no emancipados (art. 154 CCiv).

III.– JURISDICCIÓN.

Es competente la jurisdicción civil, conforme a lo dispuesto en los arts. 9.2 y 21.1 LOPJ.

IV.– COMPETENCIA.

Es competente el Tribunal al que nos dirigimos de conformidad con lo dispuesto en el art. 769.3 LEC, que fija como fuero de competencia territorial el correspondiente al del lugar del último domicilio común de los progenitores.

V.– PROCEDIMIENTO.

En cuanto al procedimiento a seguir, resulta de aplicación el trámite previsto en el art. 777 LEC, que regula el procedimiento de mutuo acuerdo, y ello en virtud de lo establecido en el art. 748.4.º LEC, al disponer que las disposiciones del título primero del libro IV serán aplicables, entre otros, a los procesos que versen exclusivamente sobre guarda y custodia de hijos menores, como es el objeto de la presente litis.

La extensión del cauce procedimental de mutuo acuerdo para pretender la guarda y custodia en las parejas de hecho, a pesar de los términos del art. 777.1 LEC, dimana de que la posibilidad de transformación del contencioso (art. 770.5.ª LEC) implica la posibilidad del recurso inicial al procedimiento consensual.

VI.– POSTULACIÓN.

Al amparo de lo dispuesto en el art. 750.2 LEC, para el caso de solicitudes de común acuerdo, se concurre con una sola defensa y representación.

VII.– FONDO DE LA PRETENSIÓN.

Son de aplicación los arts. 159 y siguientes del Código Civil, por cuanto en ellos se dispone lo relativo a la guarda, custodia y medidas personales de los hijos menores, en relación con el art. 90 y concordantes del mismo texto legal.

Es evidente que el beneficio e interés del menor debe ser el criterio principal a considerar a la hora de manifestarse acerca de la adopción de medidas en relación con los hijos y, por lo tanto, el órgano judicial debe proceder a valorar y decidir teniendo en cuenta las circunstancias que concurren en los hijos y progenitores, resolviendo según lo mejor para ellos y para el libre y correcto desarrollo de su formación y personalidad (arts. 92, 94, 103, 154, 156 y 159 CCiv). Y ello porque los principios rectores de la protección familiar definidos en el art. 39 CE («los poderes públicos aseguran la protección integral de los hijos») permiten al juzgador una mayor autonomía en aras de la búsqueda de la solución más equitativa y menos perjudicial para el menor. Este carácter indisponible recogido en la legislación española se acomoda a la Convención sobre los Derechos del Niño, aprobada por la Asamblea General de las Naciones Unidas el 20 de noviembre de 1989 y ratificada por España el 30 de noviembre de 1990, en cuyo articulado se parte de la premisa de que cualquier medida que se adopte respecto de ellos tendrá que basarse en su interés superior. Y en lo concerniente a las relaciones paternofiliales, el art. 18 reconoce el principio de que ambos progenitores tienen obligaciones comunes en lo que afecta a la crianza y desarrollo del niño. En consonancia con lo cual, tal criterio se desarrolla en la Ley Orgánica 1/1996, de 15 de enero, de Protección Jurídica del Menor, donde se insiste en la necesidad de proteger en primer lugar el interés superior del menor sobre cualquier otro interés legítimo que pudiera concurrir.

Dicho principio de «favor filii» conduce a resolver las cuestiones debatidas determinando cuáles van a ser las condiciones más propicias para el correcto desenvolvimiento de las facultades afectivas e intelectivas de los menores.

En definitiva, nos situaríamos, en lo que afecta a los hijos no matrimoniales, en el entorno por analogía del art. 90 CCiv, con el necesario control judicial de dichos acuerdos sobre el ejercicio de la patria potestad, custodia y comunicaciones, para aprobar los pactos que no perjudiquen a los descendientes y rechazarlos en caso contrario. Dicho convenio entre convivientes en la práctica ha venido operando inter partes para regular las consecuencias de la crisis convivencial aunque no sea vinculante para el Juez, quien lo evaluará teniendo en cuenta que la disponibilidad viene restringida por el principio del favor filii y la tutela judicial, sin olvidar que la ruptura de la convivencia de los progenitores no interrumpe ni elimina la obligación de asistencia de los padres hacia los hijos, sean o no matrimoniales.

Ninguno de los pactos que constan en el convenio referido es contrario a la normativa propia del Derecho de familia, como tampoco afecta ni es perjudicial a los intereses de los hijos menores de edad de los progenitores, por todo lo cual se solicita su aprobación y homologación judicial en su integridad, en aras a garantizar los derechos que les asisten a los hijos comunes de ambos.

VIII.– PROPUESTA DE CONVENIO REGULADOR.

Conforme a lo dispuesto en el apartado 2.º del art. 777 LEC, se aporta con el presente escrito la documentación exigida en el mismo y, por lo tanto, la propuesta de convenio regulador redactada con arreglo a lo establecido por la legislación civil y firmada por ambos progenitores.

IX.– INTERVENCIÓN DEL MINISTERIO FISCAL.

Con arreglo al art. 749.2 LEC, deberá ser parte el Ministerio Fiscal, por hacerse referencia a cuestiones en las que debe intervenir, dado que se trata de pactos del convenio relativos a medidas que afectan a menores.

X.– CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda no está sujeta al previo intento de resolución de controversias en vía no jurisdiccional de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia, por tratarse en sí de un acuerdo consensual y voluntario entre las partes, necesitando únicamente la homologación del mismo por parte del Tribunal, siendo que el convenio regulador (arts. 775.2 y 777.9 LEC y 90.3 CCiv) se entiende acreditativo de haber realizado esa actividad negociadora.

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito con los documentos que se acompañan y sus copias, se digne admitirlos, tenerme por comparecido y parte en la representación que ostento, entendiéndose conmigo las sucesivas diligencias, y previos los pertinentes trámites, los progenitores sean requeridos por el Letrado de la Administración de Justicia para que comparezcan y se ratifiquen por separado, con citación del Ministerio Fiscal, dictándose en su día sentencia por la que, estimando la presente DEMANDA SOBRE GUARDA Y CUSTODIA DE LOS HIJOS MENORES, se acuerde aprobar y homologar judicialmente en su integridad el convenio de fecha [FECHA], presentado de mutuo acuerdo.

Es justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a Firma del Procurador/a
