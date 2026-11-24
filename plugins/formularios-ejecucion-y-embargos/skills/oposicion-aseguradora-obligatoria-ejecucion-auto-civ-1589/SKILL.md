---
name: oposicion-aseguradora-obligatoria-ejecucion-auto-civ-1589
description: "Oposición de la aseguradora obligatoria a la ejecución de auto de cuantía máxima por accidente. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Oposición de la aseguradora obligatoria a la ejecución de auto de cuantía máxima por accidente

> Formulario **CIV-1589** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Escrito de oposición de la aseguradora al procedimiento de proceso de ejecución por auto de cuantía máxima por accidente de circulación, alegando motivos procesales y de fondo.

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Oposición de la aseguradora obligatoria a la ejecución de auto de cuantía máxima por accidente» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Oposición de la aseguradora obligatoria a la ejecución de auto de cuantía máxima por accidente” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:oposicion-aseguradora-obligatoria-ejecucion-auto-civ-1589`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (14 veces)
- [ ] NOMBRE DE LA CARRETERA (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] AÑO (2 veces)
- [ ] FECHA (2 veces)
- [ ] MOTIVO (2 veces)
- [ ] Nº (2 veces)
- [ ] SEDE (2 veces)
- [ ] CALLE
- [ ] COLEGIO
- [ ] DENOMINACIÓN SOCIAL
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] MATRÍCULA
- [ ] Nº DE COLEGIADO/A
- [ ] Nº DE DOCUMENTO
- [ ] TIPO Y Nº DE PROCEDIMIENTO

## Normas que cita el formulario

- art. 559 LEC
- art. 559.1.3.º LEC
- art. 559.1.2.º LEC
- art. 556.3 LEC
- art. 556.3.1.ª LEC
- art. 557.1.3.ª LEC
- art. 20.8.º LCS
- art. 557 LEC
- art. 561.3 LEC
- art. 394 LEC
- art. 560 LEC
- art. 337.1 LEC
- art. 337.2 LEC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…de la Sección de Instrucción del Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, que actúa en nombre y representación de SEGUROSS.A., según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], a fin de que conste en autos de ETJ n.° [Nº]/[AÑO], con la asistencia del Letrado en ejercicio D./Dña. [NOMBRE Y APELLIDOS], colegiado número [Nº DE COLEGIADO/A] del Iltre. Colegio de Abogados de [COLEGIO], y despacho abierto en [LOCALIDAD], calle [CALLE], n.º [NÚMERO], ante cuyo Tribunal comparezco y, comparezco y como mejor en derecho proceda, DIGO:

Que a medio del presente escrito, de conformidad con los arts. 559 y 560 LEC, me persono y muestro parte en el presente procedimiento de proceso de ejecución por auto de cuantía máxima, para OPONERME A LA EJECUCIÓN, lo que hago en tiempo y forma, tanto por motivos procesales como de fondo, en base a los siguientes hechos y fundamentos de Derecho.

HECHOS

PREVIO.- Negación de los hechos.

Con carácter general y expreso, negamos los aducidos de contrario, en cuanto se opongan, modifiquen o contradigan a los que aquí pasamos a establecer.

PRIMERO.- Hechos controvertidos.

En fecha [FECHA], D./Dña. [NOMBRE Y APELLIDOS] conducía el vehículo de su propiedad, asegurado por mi representada, por la carretera [NOMBRE DE LA CARRETERA], cuando fue colisionado por el vehículo matrícula [MATRÍCULA] conducido por el ejecutante D./Dña. [NOMBRE Y APELLIDOS], propiedad de [NOMBRE Y APELLIDOS] y asegurado en AUTOASEGURADORA [DENOMINACIÓN SOCIAL] S.A., como consecuencia de incorporarse a la citada carretera [NOMBRE DE LA CARRETERA] sin respetar la preferencia de paso del vehículo propiedad de mi representada.

Pese a ello, además, el ejecutante presentó denuncia contra D./Dña. [NOMBRE Y APELLIDOS] dándose lugar a los autos de juicio por delitos leves n.º [NÚMERO]/[AÑO] de la Sección de Instrucción del Tribunal de Instancia de [SEDE], plaza n.º [Nº] [TIPO Y Nº DE PROCEDIMIENTO], recayendo sentencia absolutoria.

Nos remitimos a efectos probatorios a los autos del juicio por delito leve, del que, de todas formas, se acompaña testimonio de la sentencia como documento n.º [NÚMERO].

SEGUNDO.- Oposición fundada en defectos procesales (arts. 559 y concordantes LEC).

La oposición que formalizamos en este plano se basa en:

1.º) La nulidad del título ejecutivo (art. 559.1.3.º LEC) en base a que el auto de cuantía máxima contiene defectos intrínsecos.

Conforme al art. 13, párrafo 3.º TRLRCSCVM el auto de cuantía máxima debe contener ‘la descripción del hecho y la indicación de las personas y vehículos que intervinieron y de los aseguradores de cada uno de éstos". Está, pues, aquejado de nulidad el auto ejecutivo al que nos oponemos que, sin respetar los requisitos legales de contenido, omite la descripción del accidente, y no identifica el vehículo asegurado por quien se ejecuta, sin que valga acudir, sin expresión de reenvío a lo que consta en el proceso penal en que fue dictado.

2.º) Falta de legitimación activa del actor, en tanto que carece del carácter o representación con que demanda (art. 559.1.2.º LEC), habida cuenta que D./Dña. [NOMBRE Y APELLIDOS] reclama daños materiales en el vehículo que no es de su propiedad, sino de

Se acompañan como documentos nos. 2 y 3 notas de tráfico sobre la titularidad del vehículo que conducía el ejecutante.

TERCERO.- Oposición por motivos de fondo (arts. 556.3 y 560 LEC).

En este otro frente, la oposición se funda en:

3.º) La excepción específica de culpa exclusiva del propio perjudicado del art. 556.3.1.ª LEC.
El hecho se produjo únicamente por culpa o negligencia de la propia parte ejecutante, D./Dña. [NOMBRE Y APELLIDOS], que resultó lesionado, sin existir la más leve culpa, descuido o negligencia por parte de la conductora del vehículo asegurado en la entidad que represento, Doña LUISA [NOMBRE Y APELLIDOS], al incorporarse el primero a la carretera [NOMBRE DE LA CARRETERA] desde un carril de aceleración con obligación de ceder el paso a los vehículos que, como el asegurado en esta entidad, circulaban por la dicha carretera con clara preferencia, como así resulta tanto por las normas generales de circulación como por la marca vial existente en la calzada, según se observa en el croquis que se aporta, como ya se aportó en la documentación del juicio de faltas ya indicado (documento n.º 4).
4.º) Subsidiariamente, se invoca la concurrencia de culpas delart. 556.3.3.ª LEC, como concurso causal de la acción de la ejecutante a la producción de sus propios males, aplicándose como factor de minoración de las indemnizaciones básicas del Baremo del Anexo al TRLRCSCVM.
5.º) También se resiste la cuantía de indemnización por pluspetición del art. 557.1.3.ª LEC, tanto de las lesiones personales como de los daños en las cosas, que se ha cuantificado con notorio exceso, con arreglo a las siguientes alegaciones:
A) [MOTIVO]
B) [MOTIVO]

CUARTO.- Intereses moratorios.

Para el improbable caso de que se estimase la existencia de concurrencia de culpas, no habría lugar a acceder a la petición de intereses moratorios solicitados por la parte ejecutante, toda vez que se trata de uno de los supuestos jurisprudenciales de aplicación de la exoneración de intereses en virtud de lo dispuesto en el art. 20.8.º LCS 50/1980, dado que la ausencia de consignación judicial o pago del importe mínimo está fundada en una causa justificada, siendo evidente que en el presente caso la asegurada de la mercantil a la que representamos, Doña LUISA [NOMBRE Y APELLIDOS], está arropada incluso por una sentencia absolutoria en la jurisdicción penal, lo que pone de manifiesto la lógica de su tesis exculpatoria.

FUNDAMENTOS DE DERECHO

I

Se aceptan los de la demanda en cuanto a competencia.

II

Por lo que hace al procedimiento, la ejecución del auto de cuantía máxima, pero con algunas especialidades, que se justifican en la especial naturaleza de este título, que es judicial, aunque no jurisdiccional, en el sentido de que no se forma en un proceso, sino que se emite sin cognición judicial previa, mediante una simple constatación de hechos por el Juez al que legalmente se le encomienda.

En lo tocante a la oposición a la ejecución, las especialidades se ciñen a que, sobre las causas de oposición a la ejecución para los títulos ejecutivos no judiciales en el art. 557 LEC, además de los motivos procesales (art. 559 LEC), puede basarse en unas causas específicas de fondo (art. 556.3 LEC); y la oposición por motivos de fondo tiene efectossuspensivo el curso de dicha ejecución, hasta que dicha oposición sea desestimada por resolución firme (art. 561.3 LEC).

III

Se alegan los fundamentos de derecho de la demanda ejecutiva en sentido contrario, los arts. 4, 5 y 6 TRLRCSCVM y concordantes del Reglamento del Seguro Obligatorio, y los preceptos invocados de la LEC sobre el proceso de ejecución y sus especialidades.

Hay que advertir que esta ejecución se despacha desde un ‘tertium genus’ de resolución judicial (auto) dictada por un órgano del orden jurisdiccional penal, que nada ha juzgado, ni decidido sobre los elementos de los que depende la relación jurídica de crédito a la reparación, ni sobre su titularidad activa, ni sobre la existencia de la obligación del responsable o del asegurador, el cual se quiere llevar a la prestación indemnizatoria forzosa por un órgano del orden jurisdiccional civil.

IV

Se alegan los arts. 559.2 y 561.2 de la LEC en cuanto a costas, que se remiten al sistema de imposición cuasiobjetivo para declarativos de instancia del art. 394 LEC.

En su virtud,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito, documentos que se acompañan y copia de todo ello, se sirva admitir uno y otros, tener por formulada la oposición a la ejecución instada de contrario y, suspendiendo el curso del procedimiento de ejecución, se conceda a estos autos el trámite legal correspondiente, recibiéndolos a prueba y previas las actuaciones procesales pertinentes, se sirva dictar auto por el que, estimando los motivos alegados, se declare:

1. La estimación de la oposición por motivos procesales, dejando sin efecto la ejecución despachada con imposición de costas a la parte ejecutante.
2. Alternativamente, la estimación de la oposición planteada por motivos de fondo, declarándose la improcedencia de la continuación de la ejecución, y reintegrándose a mi representada a la situación anterior al despacho de la ejecución.

Todo con imposición de costas a la ejecutante.

Es de Justicia que pido en [LUGAR], a [FECHA].

OTROSÍ PRIMERO DIGO: Que de conformidad con lo dispuesto en el art. 560 LEC, intereso la celebración de vista, la que habrá de desarrollarse conforme a lo prevenido para el juicio verbal, interesándose la citación por el Tribunal de las siguientes personas en su calidad de testigos:

1.- [NOMBRE Y APELLIDOS]
2.- [NOMBRE Y APELLIDOS]

OTROSÍ SEGUNDO DIGO: Para combatir expresamente el dictamen pericial emitido por el médico especialista en valoración del daño corporal Dr./a. [NOMBRE Y APELLIDOS], que se documenta y acompaña con la demanda ejecutiva, se anuncia la presentación por esta parte de su dictamen médico, que se ha encomendado al Dr./a. [NOMBRE Y APELLIDOS], pero no ha podido ser elaborado en el fugaz plazo de oposición.

De acuerdo con lo dispuesto en el art. 337.1 LEC, se aportará el dictamen anunciado en cuanto se disponga del mismo, y en todo caso antes de la vista, y si no se celebrara, previamente a que deba resolver el Tribunal. Y conforme al art. 337.2 LEC, interesa al derecho de esta parte manifestar que desea la convocatoria del perito a la vista que se celebre, a fin de que exponga o explique su dictamen, y responda a las preguntas, objeciones o propuestas de rectificación que se le planteen.

Por lo expuesto,

AL TRIBUNAL SUPLICO que, teniendo por hechas las afirmaciones anteriores a los efectos oportunos, y por anunciada la prueba pericial y la proposición de aclaraciones del perito, de cara a la vista, se sirva proceder como queda interesado.

Es Justo en el mismo lugar y fecha arriba indicados.

Firma del Abogado/a	Firma del Procurador/a

========================================================================
