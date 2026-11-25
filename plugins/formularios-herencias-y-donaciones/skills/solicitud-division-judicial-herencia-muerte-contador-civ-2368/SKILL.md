---
name: solicitud-division-judicial-herencia-muerte-contador-civ-2368
description: "Solicitud de división judicial de la herencia por muerte del contador-partidor y falta de acuerdo. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de división judicial de la herencia por muerte del contador-partidor y falta de acuerdo

> Formulario **CIV-2368** del plugin **Herencias, testamentos y donaciones** (`formularios-herencias-y-donaciones`) · Civil › Sucesiones y donaciones · normativa revisada el 25-11-2026.

## Qué es

Escrito presentado ante el Tribunal Instancia interesando la división judicial de la herencia, al haber fallecido el contador-partidor y no ponerse los herederos de acuerdo en cuanto a cómo debe realizarse aquella.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de división judicial de la herencia por muerte del contador-partidor y falta de acuerdo» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de división judicial de la herencia por muerte del contador-partidor y falta de acuerdo” para mi caso». También puedes invocarla directamente con `/formularios-herencias-y-donaciones:solicitud-division-judicial-herencia-muerte-contador-civ-2368`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-herencias-y-donaciones:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Herencias, testamentos y donaciones) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (20 veces)
- [ ] Nº DE DOCUMENTO (9 veces)
- [ ] CALLE (4 veces)
- [ ] COMPLETAR (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] FECHA (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] Nº (2 veces)
- [ ] FECHAS
- [ ] LUGAR
- [ ] NÚMERO DE LA CALLE
- [ ] SEDE

## Normas que cita el formulario

- art. 85.1 LOPJ
- art. 5 Ley Orgánica 1/2025

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) El procedimiento para la división de la herencia, trasunto del antañón «juicio de testamentaría», se ordena a la cabal ejecución de la voluntad testamentaria del causante, a medio de la partición del caudal entre los causahabientes del finado y la adjudicación de bienes a los mismos.

Aunque no lo diga explícitamente la norma, es requisito sine qua non de la pertinencia de este cauce la existencia de una disposición testamentaria. A su vez, y de acuerdo con el apdo. 1 de este precepto, es preciso que el reparto y liquidación no haya sido realizada judicial o extrajudicialmente de forma tempestiva —S.T.S., Sala Primera, de 20 de febrero de 1964—, debidamente justificada —S.T.S., de 19 de junio de 1950—, toda vez que el derecho de los causahabientes adolece de carácter subsidiario al del testador de hacer por sí o encomendar a contadores-partidores, albaceas u otros la partición (arts. 1057 y 1058 C.C.), sin otras limitaciones que las de no perjudicar las legítimas, sin menoscabo de que quienes se estimen perjudicados puedan ejercitar las acciones de que se crean asistidos en el cauce procedente —SS.T.S., Sala Primera, de 22 de marzo de 1899, 9 de noviembre de 1907, 15 de febrero de 1916, 31 de octubre de 1922, 3 de noviembre de 1943, 17 de octubre de 1960, 4 de noviembre de 1969, 9 de abril de 1990, entre otras—.

La LEC 1/2000 reconoce aptitud para promover este procedimiento, en principio, a los coherederos y a los legatarios de parte alícuota. El empleo de la expresión «coherederos» desvanece las incertidumbres que originaba la locución «herederos testamentarios» del art. 1038 LEC 1881 a propósito de si ostentaban dicha idoneidad los legitimarios en quienes no concurre, al propio tiempo, la calidad de legatarios de parte alícuota —por satisfacerse sus derechos de otro modo—, inclinándose la doctrina por la postura afirmativa (J.B. VALLET DE GOYTISOLO; DE CASTRO GARCÍA). La supresión del término «testamentarios» comprende de suyo a los voluntarios y a los forzosos, con la excepción representada por el art. 366, II de la 40/1991, de 30 de diciembre, de Sucesiones de Cataluña, para el cual «el derecho a la legítima no autoriza a promover el juicio de testamentaría...».

La LEC 1/2000 invierte lo que constituía regla en la LEC 1881, y en principio, no reconoce a los acreedores aptitud para interesar la división del caudal, sin perjuicio de las acciones que les asistan para la satisfacción de sus derechos. Únicamente, los que se encuentren reconocidos como tales en el testamento, o por los herederos, o los que tengan documentado su crédito en un título que tenga aparejada ejecución ex art. 517 LEC 1/2000, quienes —de acuerdo con lo previsto en el art. 1082 C.C.— podrán oponerse a la práctica de las operaciones divisorias hasta tanto se les afiance o satisfaga el importe de su crédito, con el límite temporal representado por la entrega material de los bienes a los respectivos adjudicatarios.

En todo caso, estos mismos acreedores podrán pedir la intervención del caudal hereditario (art. 792.2, en relación con el art. 791.2 LEC 1/2000). A su vez (apdo. 5), y al igual que establece el art. 1083 C.C., cualquier acreedor de algún coheredero podrá intervenir para evitar que por el modo en que se efectúe la partición ésta les pueda parar algún perjuicio.

Al igual que sucediera en el art. 1055 LEC 1881, el escrito inicial recibe la denominación de «solicitud», considerada por GUASP como «verdadera demanda». En contra, HERCE QUEMADA estima que este calificativo encuentra explicación en la naturaleza voluntaria del procedimiento.

Junto con aquélla, el solicitante ha de aportar el certificado de defunción que acredite el fallecimiento del causante, y la disposición testamentaria, cuya vigencia corrobore el Certificado del Registro General de Actos de Última Voluntad, de la que resulte la calidad invocada en la petición. Si no se presentaren todos los documentos, deberá concederse al instante un plazo para la subsanación de la falta; y si, de los aportados inicialmente o luego de ser completados, resultare que el solicitante carece de idoneidad subjetiva, se rechazará la solicitud por medio de auto.

Junto con la solicitud podrá interesarse la intervención del caudal hereditario y la práctica de inventario de los bienes, diligencias a las que se accederá por el órgano jurisdiccional si concurrieren los presupuestos de la Secc. 2.ª (arts. 790 a 796).

Luego de realizadas, en su caso, dichas operaciones, o en otro caso, admitida la solicitud, el Letrado de la Administración de Justicia ordenará convocar a los interesados —herederos, legatarios de parte alícuota y, en su caso, al cónyuge supérstite— a una Junta que habrá de celebrarse dentro de los diez días siguientes. De acuerdo con la doctrina (MANRESA, DE LA PLAZA, DE CASTRO GARCÍA), si al promoverse estas actuaciones se solicitase el spatium deliberandi o se hubiese aceptado la herencia a beneficio de inventario, habrá de observarse lo prevenido en el art. 1014 C.C., a cuyo tenor se llamará a todos los acreedores y legatarios, y no sólo a los legatarios de parte alícuota, con los cuales se practicará necesariamente el inventario.

La citación de los interesados que estuvieren personados en juicio se entenderá con el Procurador que ostente su representación causídica. En otro caso, y si tienen domicilio conocido, los actos de comunicación se entenderán en éstos. Si se ignorase su paradero, después de practicadas las diligencias de averiguación mencionadas en el art. 156 LEC 1/2000, o cuando así se acuerde en el caso del art. 157.2 LEC 1/2000, el letrado o letrada de la Administración de Justicia, consignadas estas circunstancias, mandará que se haga la comunicación, a través del Tablón Edictal Judicial Único, salvaguardando en todo caso los derechos e intereses de menores, así como otros derechos y libertades que pudieran verse afectados por la publicidad de los mismos.

La citación de los menores, incapacitados o declarados ausentes se entenderá con sus representantes legales —arts. 154.2.º, 181, 184, 185, 267, 271.4, 290 C.C.— si los tuvieren. En otro caso, lo mismo que si, teniéndolos, éstos tuvieren intereses incompatibles con los del representados, hasta el momento en que se les provea de defensor judicial —arts. 163 y 299.1 C.C.—, desempeñará la representación de los mismos el Ministerio Fiscal. La misma representación ejercerá respecto de los ausentes de hecho, que no se hallaren en el lugar del juicio, hasta tanto se presenten o puedan ser habidos.

Atendido el carácter potestativo y voluntario de la intervención en el procedimiento de los acreedores de los herederos, no se prevé su citación salvo en el caso de que hubieren comparecido en el procedimiento; en otro caso, se les admitirá si se personasen el día señalado para la Junta con los títulos representativos de sus créditos.


### Flujo

1. **Paso 0**: comprueba Jurisprudenciator (arriba).
2. Lee entero `assets/formulario.md` (el formulario que vas a rellenar, en la carpeta de esta skill) y la parte de `../indice/marco.md` que afecte al caso. Limítate a la materia de este formulario: no añadas contenido ajeno a él.
3. Pide los datos de la lista en una sola tanda. Si un dato aparece varias veces, aclara a qué persona o acto corresponde cada vez. Lo que el usuario no sepa se queda como hueco visible con su etiqueta (p. ej. [FECHA]).
4. Resuelve cada [ELEGIR …] y cada [OPCIONAL …] según los hechos, y sustituye cualquier indicación entre paréntesis del formulario («(se describirá…)», «(indicar…)») por el contenido que corresponda. Redacta las partes que dependen del caso (hechos, motivos, descripción de bienes).
5. Aplica los avisos de actualización en el lugar que indican. Comprueba con `buscar_articulo` cada norma citada; si alguna ha cambiado, usa la redacción vigente. Si citas jurisprudencia, localízala con `buscar_sentencias` o `buscar_por_cita` y léela con `leer_sentencias`.
6. Antes de entregarlo, pasa `verificar_escrito` con las frases que citan normas o sentencias y corrige lo que señale.
7. **Documento final = el formulario tal cual, rellenado y limpio.**
   - Empieza exactamente por la primera línea de `assets/formulario.md` y sigue su estructura y su orden hasta la firma.
   - No pongas en el documento título, nombre del formulario o de la skill, código, encabezados, «Para qué sirve», leyendas, avisos, notas de uso, comentarios ni explicaciones. Tampoco marcas [ELEGIR…] u [OPCIONAL…]: ya están resueltas.
   - Formato Word (.docx, con la skill de Word disponible): **Times New Roman 11 pt** en todo el documento, **interlineado 1,15**, **texto justificado**, márgenes de 2,5 cm. Los rótulos del formulario (REUNIDOS, CLÁUSULAS, HECHOS, SUPLICO…) en su propia línea y en negrita, sin cambiar su texto.
8. En el chat (nunca dentro del documento): datos pendientes, partes redactadas por ti, normas y sentencias comprobadas con Jurisprudenciator (y, si algún dato sale de internet, cuál y su enlace) y, si es un escrito judicial o administrativo, el plazo y el órgano ante el que se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.
