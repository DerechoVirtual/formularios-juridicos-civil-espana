---
name: demanda-resolucion-arrendamiento-vivienda-subarriendo-civ-0566
description: "Demanda de resolución de arrendamiento de vivienda por subarriendo inconsentido (posterior a 1995). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de resolución de arrendamiento de vivienda por subarriendo inconsentido (posterior a 1995)

> Formulario **CIV-0566** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario del arrendador para que se declare resuelto el contrato de arrendamiento de vivienda, celebrado después del 1 de enero de 1995 (LAU 1994), por subarriendo realizado por el arrendatario sin consentimiento del arrendador (arts. 8 y 27.2.c LAU), y se condene al demandado a desalojar la vivienda.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de resolución de arrendamiento de vivienda por subarriendo inconsentido (posterior a 1995)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de resolución de arrendamiento de vivienda por subarriendo inconsentido (posterior a 1995)” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:demanda-resolucion-arrendamiento-vivienda-subarriendo-civ-0566`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº DE DOCUMENTO (5 veces)
- [ ] NOMBRE Y APELLIDOS DEL DEMANDADO (4 veces)
- [ ] AÑO (2 veces)
- [ ] DNI/NIE (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] DÍA (2 veces)
- [ ] FECHA (2 veces)
- [ ] FIRMA (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] MES (2 veces)
- [ ] DOMICILIO DE LA VIVIENDA
- [ ] DOMICILIO DEL DESPACHO
- [ ] FECHAS
- [ ] IMPORTE EN LETRA
- [ ] NOMBRE Y APELLIDOS DEL ABOGADO/A
- [ ] NOMBRE Y APELLIDOS DEL DEMANDANTE
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº DE DOCUMENTOS
- [ ] SEDE

## Normas que cita el formulario

- art. 21.1 LOPJ
- art. 36.1 LEC
- art. 85.1 LOPJ
- art. 45 LEC
- art. 52.1.7.º LEC
- art. 249.1.6.º LEC
- art. 10 LEC
- art. 253.1 LEC
- art. 251 LEC
- art. 23 LEC
- art. 399 LEC
- art. 5 Ley Orgánica 1/2025
- art. 394 LEC
- art. 25 LAU

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, en nombre y representación de [NOMBRE Y APELLIDOS DEL DEMANDANTE], con DNI/NIE [DNI/NIE] y domicilio en [DOMICILIO], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento n.º [Nº DE DOCUMENTO]; dirigido por el Abogado D./Dña. [NOMBRE Y APELLIDOS DEL ABOGADO/A], que redacta y firma el presente escrito, con despacho profesional abierto en [LOCALIDAD], [DOMICILIO DEL DESPACHO], ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que por medio del presente escrito deduzco DEMANDA DE JUICIO ORDINARIO EN ASUNTO RELATIVO A CONTRATO DE ARRENDAMIENTO URBANO, contra D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO], con DNI/NIE [DNI/NIE] y domicilio en [DOMICILIO], ejercitando la acción de resolución de contrato de arrendamiento de vivienda por subarriendo inconsentido, en base a los siguientes

HECHOS

PRIMERO.– Mi mandante es propietario de la vivienda sita en [DOMICILIO DE LA VIVIENDA]. Se acompaña el título de propiedad como documento n.º [Nº DE DOCUMENTO].

SEGUNDO.– El demandado D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO] ocupa la vivienda en concepto de inquilino en virtud de contrato de arrendamiento celebrado en fecha [DÍA] de [MES] de [AÑO]. Se acompaña dicho contrato como documento n.º [Nº DE DOCUMENTO], siendo la renta inicialmente convenida la de [IMPORTE] euros mensuales.

TERCERO.– El demandado D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO], desde la fecha aproximada de [FECHA], ha introducido en la casa a una tercera persona, cuyos datos personales por ahora se desconocen, a la cual ha hecho subarriendo de una de las habitaciones de la vivienda, constituyendo su domicilio habitual.

En acreditación de ello se acompañan los documentos números [Nº DE DOCUMENTOS].

CUARTO.– La parte actora manifiesta que, previo a la presentación de la presente demanda, se han llevado a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria, incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, mi representado/a envió un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por el demandado por el mismo medio, [ELEGIR: rechazando el acuerdo / habiendo sido solo posible un acuerdo parcial], viéndonos en la necesidad de acudir a la presente vía judicial, respecto a los extremos de la controversia en los que se mantiene la discrepancia.

Acompaño como documento n.º [Nº DE DOCUMENTO] el requerimiento efectuado y como documento n.º [Nº DE DOCUMENTO] la contestación del demandado.

A los anteriores hechos son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

I.– JURISDICCIÓN Y COMPETENCIA.

La jurisdicción ordinaria es la única competente para el conocimiento de los juicios que se susciten en territorio español con arreglo a lo establecido en los tratados y convenios internacionales en los que España sea parte, en las normas de la Unión Europea y en las leyes españolas (art. 21.1 LOPJ y art. 36.1 LEC).

La competencia objetiva corresponde a la Sección Civil del Tribunal de Instancia según lo dispuesto en el art. 85.1 LOPJ y el art. 45 LEC, así como la territorial con arreglo al art. 52.1.7.º LEC, puesto que el Tribunal competente es el del lugar en que está sita la finca.

II.– PROCEDIMIENTO.

El art. 249.1.6.º LEC dice que se decidirá en juicio ordinario las demandas que versen sobre cualesquiera asuntos relativos a arrendamientos urbanos, salvo excepciones que no comprenden el presente supuesto.

III.– LEGITIMACIÓN ACTIVA Y PASIVA.

Corresponde la activa a mi mandante por ser el arrendador en el contrato cuya resolución determina la recuperación de la posesión inmediata, detentando la real mediata a título de dueño.

La legitimación pasiva corresponde al demandado en su condición de arrendatario (art. 10 LEC) (véase la nota explicativa).

IV.– CUANTÍA.

Conforme al art. 253.1 LEC cifro la cuantía de la presente demanda en [IMPORTE EN LETRA] euros ([IMPORTE]), importe de una anualidad de renta, según resulta de la regla 9.ª del art. 251 LEC.

V.– POSTULACIÓN Y DEFENSA.

Conforme a los arts. 23 y 31 LEC se formula esta demanda por medio de Procurador/a con poder para pleitos, y con dirección y firma de Letrado habilitado. Asimismo se cumplen los requisitos formales del art. 399 LEC.

VI.– CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4.º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VII.– FUNDAMENTOS DE DERECHO MATERIALES O SOBRE EL FONDO DEL ASUNTO.

El fundamento de esta demanda está en el art. 27.2.c) de la vigente Ley de Arrendamientos Urbanos, en cuanto que el arrendador puede resolver de pleno derecho el contrato de arrendamiento cuando se produce el subarriendo o la cesión inconsentida. En el presente caso el arrendatario ha incumplido la exigencia del consentimiento del arrendador a que se refiere el art. 8.2 del mismo texto.

VIII.– COSTAS.

Conforme al art. 394 LEC, las costas del procedimiento habrán de imponerse al demandado.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito de demanda junto con los documentos que se acompañan y copias de todo ello, se sirva admitirlo a trámite, me tenga por comparecido y parte demandante y por formulada la demanda de juicio ordinario contra D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO], acordando conferir traslado de la misma a dicho demandado, emplazándole para que comparezca y la conteste, y seguido el juicio por sus trámites, se dicte sentencia por la que, estimando íntegramente la demanda, se declare la resolución del contrato de arrendamiento de la vivienda descrita, condenando al demandado a que desaloje la misma, bajo apercibimiento de ser lanzado, con expresa imposición de costas procesales al demandado.

Es justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a: [FIRMA] Firma del Procurador/a: [FIRMA]

NOTA EXPLICATIVA

Sobre la existencia de litisconsorcio pasivo necesario y la posibilidad de demandar al tercero ocupante deben hacerse las siguientes precisiones. Es doctrina constante que, a diferencia de lo que ocurre en los casos de resolución por cesión de vivienda, para los que el art. 25 de la LAU de 1964, aplicable a los contratos anteriores al 1 de enero de 1995, impone que la demanda se dirija también contra el cesionario, en este caso no se precisa demandar al tercer ocupante. No obstante, puede resultar necesario traer al proceso al tercero ocupante cuando la sentencia pudiera tener efectos directos e inmediatos sobre esa situación, porque es esa situación misma el objeto de discusión en el proceso arrendaticio y pudiera alegar algún derecho propio frente al arrendador.

Aun cuando la citada doctrina litisconsorcial es recogida en la unánime jurisprudencia de la Sala Primera del Tribunal Supremo, son de citar, entre las sentencias que condicionan la necesidad del litisconsorcio pasivo a la concurrencia de una relación jurídico-material a la que son ajenos los terceros o extraños al contrato, las de fechas 23 de febrero de 1988 y 13 de abril de 1989, y por lo que respecta a las situaciones concretas de subarriendo, cesión y traspaso, son de mencionar, además de otras, las SSTS de 22 de abril de 1991, 11 de junio de 1991, 9 de junio de 1992, 14 de junio de 1994 y muy especialmente la de 27 de noviembre de 1996, rec. 182/1993, que declaran la innecesariedad de demandar a la persona del cesionario o subarrendatario. En definitiva, la STC 58/1988, de 6 de abril, resume la doctrina posteriormente desarrollada en el mismo sentido, en los siguientes puntos: a) No es contrario al principio de contradicción del art. 24 CE el que una decisión judicial pueda tener efectos que repercutan en sujetos que no han participado en el proceso y que no han sido llamados a él y que, por tanto, no figuren como condenados en la sentencia; b) El principio constitucional de contradicción no se opone a que una sentencia pronunciada frente al arrendatario pueda ser oponible y tener efectos indirectos o reflejos también frente al subarrendatario, pese a no haber sido este parte del proceso principal, pero ello siempre que ese subarrendatario haya permanecido legítimamente extraño al procedimiento cuando no pudiera alegar ningún derecho propio frente al arrendador, en cuyo caso la sentencia no podría tener efectos directos e inmediatos sobre su derecho, aunque repercutiera en su situación jurídica; y c) Pero cuando la sentencia pudiera tener efectos directos e inmediatos sobre esa situación, porque es esa situación misma el objeto de discusión en el proceso arrendaticio y pudiera alegar algún derecho propio frente al arrendador, resulta cuestionable la legitimidad de la no llamada al proceso. En consecuencia, es exigible, a la luz del art. 24 CE, la llamada al subarrendatario o cesionario cuando lo que se discute es la legitimidad de tal subarriendo.
