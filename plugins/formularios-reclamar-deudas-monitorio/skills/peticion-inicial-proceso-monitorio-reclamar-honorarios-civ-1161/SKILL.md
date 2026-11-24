---
name: peticion-inicial-proceso-monitorio-reclamar-honorarios-civ-1161
description: "Petición inicial de proceso monitorio para reclamar honorarios de abogado. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Petición inicial de proceso monitorio para reclamar honorarios de abogado

> Formulario **CIV-1161** del plugin **Cobrar deudas: monitorio y cambiario** (`formularios-reclamar-deudas-monitorio`) · Civil › Monitorio y cambiario · normativa revisada el 24-11-2026.

## Qué es

Solicitud inicial de proceso monitorio (art. 812 LEC) presentada por un abogado para reclamar a su cliente los honorarios devengados por actuaciones judiciales y extrajudiciales, acompañando la minuta detallada y acreditando el intento previo de solución negociada.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Petición inicial de proceso monitorio para reclamar honorarios de abogado» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Petición inicial de proceso monitorio para reclamar honorarios de abogado” para mi caso». También puedes invocarla directamente con `/formularios-reclamar-deudas-monitorio:peticion-inicial-proceso-monitorio-reclamar-honorarios-civ-1161`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-reclamar-deudas-monitorio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Cobrar deudas: monitorio y cambiario) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (3 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] CALLE (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL DEUDOR (2 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] AÑO
- [ ] COLEGIO
- [ ] DESCRIBIR LOS ASUNTOS Y ACTUACIONES PROFESIONALES
- [ ] DNI/NIE
- [ ] DOMICILIO
- [ ] DÍA
- [ ] FECHA
- [ ] FECHAS
- [ ] FIRMA
- [ ] IMPORTE
- [ ] MES
- [ ] NOMBRE Y APELLIDOS DEL LETRADO/A
- [ ] Nº DE COLEGIADO
- [ ] SEDE
- [ ] TELÉFONO
- [ ] ÓRGANO JUDICIAL DE INSTANCIA
- [ ] ÓRGANO JUDICIAL DE RECURSO

## Normas que cita el formulario

- art. 812.1.2.ª LEC
- art. 5 Ley Orgánica 1/2025
- art. 35 LEC
- art. 12 LEC
- art. 812 LEC

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

D./Dña. [NOMBRE Y APELLIDOS DEL LETRADO/A], con DNI [DNI/NIE], Letrado/a perteneciente al Ilustre Colegio de la Abogacía de [COLEGIO], colegiado/a con el n.º [Nº DE COLEGIADO], con domicilio en [DOMICILIO], ante el Tribunal comparezco y DIGO (véase la nota explicativa final):

Que por medio del presente escrito formulo demanda de PROCESO MONITORIO en reclamación de [IMPORTE] euros contra D./Dña. [NOMBRE Y APELLIDOS DEL DEUDOR], quien podrá ser debidamente citado en su domicilio en [LOCALIDAD], calle [CALLE], número [NÚMERO] o, de no ser hallado en el mismo, en el lugar en que desarrolla su actividad profesional, igualmente en [LOCALIDAD], calle [CALLE], número [NÚMERO].

Asimismo, puede ser localizado en el teléfono número [TELÉFONO].

La presente solicitud se fundamenta en las siguientes

ALEGACIONES

El crédito que se reclama a D./Dña. [NOMBRE Y APELLIDOS DEL DEUDOR] tiene su origen en mi intervención profesional como Letrado/a en ejercicio, tanto de carácter extrajudicial como judicial, relativa a [DESCRIBIR LOS ASUNTOS Y ACTUACIONES PROFESIONALES].

Se aporta como documento n.º [Nº DE DOCUMENTO] minuta detallada en la que se relacionan pormenorizadamente los diversos conceptos cuyo pago se reclama.

Dichos documentos reúnen las características que requiere el art. 812.1.2.ª LEC, a los efectos de dar curso a la presente petición inicial de proceso monitorio.

Por otro lado, la parte actora manifiesta que, previo a la presentación de la presente demanda, se han llevado a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad exigido en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia, y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria, incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, envié un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, el cual fue contestado por el demandado por el mismo medio, [ELEGIR: rechazando el acuerdo / habiendo sido solo posible un acuerdo parcial], viéndome en la necesidad de acudir a la presente vía judicial, respecto a los extremos de la controversia en los que se mantiene la discrepancia.

Acompaño como documento nº [Nº DE DOCUMENTO] el requerimiento efectuado y como documento nº [Nº DE DOCUMENTO] la contestación del demandado.

Por lo expuesto,

SUPLICO AL TRIBUNAL:

Que teniendo por presentada esta solicitud junto al documento acompañado, con sus copias, se admita a trámite acordándose el trámite correspondiente.

Por ser de Justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del solicitante: [FIRMA]

NOTA EXPLICATIVA

La cuestión pudiera parecer dudosa, y se ha considerado en ocasiones un procedimiento inadecuado ante la existencia del procedimiento de jura de cuentas (en este sentido, el AAP Soria 53/2003, de 24 de abril de 2003, rec. 86/2003), pero la doctrina mayoritaria, desde la perspectiva del modelo de proceso monitorio de tipo documental diseñado por el legislador (AAP Madrid 19/2006, de 12 de enero de 2006, rec. 543/2005), se pronuncia en sentido favorable a la posibilidad de reclamación de honorarios de abogado por el cauce monitorio (AAP Málaga 173/2003, de 13 de junio de 2003, rec. 177/2003).

El presente escrito contempla el supuesto en el que se reclaman tanto los honorarios devengados por la realización de actuaciones judiciales como los honorarios devengados por actuaciones extrajudiciales (por ejemplo, asesoramiento, preparación de documentación), y precisamente esta circunstancia constituye un argumento más a favor de considerar adecuado el procedimiento monitorio, como no se quiera llegar a la conclusión, contraria al principio más elemental de economía procesal, de que el Letrado puede reclamar a través del juicio monitorio sus honorarios por su asesoramiento o actuación no judicial, pero no los correspondientes a actuaciones judiciales, que debería reclamar mediante el proceso de jura de cuentas. En este sentido, el AAP Burgos 2/2003, de 2 de enero de 2003, rec. 596/2002, argumenta:

«Ningún precepto de la nueva LEC exige que el Letrado reclame la minuta de sus honorarios a su propio cliente por un procedimiento concreto y específico, bien puede acudir al procedimiento privilegiado de jura de cuentas (artículo 35 de la LEC, con la diferencia sustancial respecto de la anterior regulación procesal, en el que ahora el Letrado es el que se dirige directamente contra el cliente y no el Procurador, como antes regulaba el artículo 12 LEC/1881), bien al procedimiento monitorio (artículo 812 de la LEC, siempre que concurran los requisitos exigidos en dicho artículo) o bien mediante el procedimiento declarativo que corresponda por la cuantía. La elección de uno u otro procedimiento corresponde al propio Letrado que, como acreedor, puede, dentro de su derecho a obtener la tutela judicial efectiva, optar por la vía procesal que considere más conveniente según las circunstancias del caso concreto. En este caso, además, el Letrado (...) justifica la elección del proceso monitorio, con fundamento en el artículo 818.1.2.ª y 2.1.º de la LEC, en lugar del juicio de jura de cuentas, dado que la reclamación económica por la labor profesional realizada no se limita a su actuación en [ÓRGANO JUDICIAL DE INSTANCIA] y en [ÓRGANO JUDICIAL DE RECURSO], en los autos [Nº DE PROCEDIMIENTO] y [Nº DE PROCEDIMIENTO], respectivamente, sino que alcanza a otras actuaciones extraprocesales que no tendrían cabida dentro del procedimiento regulado en el artículo 35 de la LEC.»
