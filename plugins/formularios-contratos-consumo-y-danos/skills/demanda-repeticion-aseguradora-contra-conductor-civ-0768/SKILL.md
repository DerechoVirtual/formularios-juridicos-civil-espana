---
name: demanda-repeticion-aseguradora-contra-conductor-civ-0768
description: "Demanda de repetición de la aseguradora contra el conductor condenado por delito vial. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de repetición de la aseguradora contra el conductor condenado por delito vial

> Formulario **CIV-0768** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario en que la aseguradora, una vez efectuado el pago de la indemnización, ejercita la facultad de repetición contra el conductor del vehículo causante del daño debido a la conducción bajo la influencia de bebidas alcohólicas, condenado por delito contra la seguridad vial.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de repetición de la aseguradora contra el conductor condenado por delito vial» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de repetición de la aseguradora contra el conductor condenado por delito vial” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-repeticion-aseguradora-contra-conductor-civ-0768`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] FECHA (6 veces)
- [ ] IMPORTE (6 veces)
- [ ] MARCA/MODELO (6 veces)
- [ ] CALLE (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] MATRÍCULA (3 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] ASEGURADORA
- [ ] FECHAS
- [ ] LUGAR
- [ ] Nº
- [ ] PENA IMPUESTA
- [ ] SEDE

## Normas que cita el formulario

- art. 85.1 LOPJ
- art. 45 LEC
- art. 52.1 LEC
- art. 6.1.3.º LEC
- art. 7.4 LEC
- art. 10 LEC
- art. 253.1 LEC
- art. 23 LEC
- art. 399 LEC
- art. 5 Ley Orgánica 1/2025
- art. 576 LEC
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

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en nombre y representación de la Entidad Aseguradora [ASEGURADORA], con domicilio en [LOCALIDAD], calle [CALLE], como acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], a quien asiste el Letrado en ejercicio abajo firmante D./Dña. [NOMBRE Y APELLIDOS], con despacho profesional en [LOCALIDAD], ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que mediante el presente escrito formulo DEMANDA DE JUICIO ORDINARIO contra D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], calle [CALLE], en reclamación de la cantidad de [IMPORTE] euros más intereses legales y costas procesales, en base a los siguientes:

HECHOS

PRIMERO.- El día [FECHA] sobre las [Nº] horas el demandado D./Dña. [NOMBRE Y APELLIDOS] conducía el vehículo de su propiedad marca [MARCA/MODELO], modelo [MARCA/MODELO], matrícula [MATRÍCULA], por la calle [CALLE] de esta ciudad, haciéndolo bajo influencia de bebidas alcohólicas, cuando al llegar al cruce con la calle [CALLE], colisionó por alcance al no percatarse de que el conductor que lo precedía se había detenido ante un semáforo en ámbar, contra el vehículo marca [MARCA/MODELO], modelo [MARCA/MODELO], matrícula [MATRÍCULA], propiedad de D./Dña. [NOMBRE Y APELLIDOS], en el que viajaba como ocupante D./Dña. [NOMBRE Y APELLIDOS], quien tras el impacto, sufrió lesiones consistentes en

SEGUNDO.- Como consecuencia de estos hechos se siguieron actuaciones penales y el demandado fue condenado en sentencia firme de fecha [FECHA], con expresa mención a la relación entre la colisión y limitación de las facultades psico-físicas causada por la ingesta de bebidas alcohólicas, como autor responsable criminal de un delito contra la seguridad vial previsto y penado en el art. 379 CP en concurso con un delito de lesiones por imprudencia grave, previsto y penado en el art. 152.1.1.º, a la pena de [PENA IMPUESTA] y a indemnizar a D./Dña. [NOMBRE Y APELLIDOS], ocupante, con la cantidad de [IMPORTE] Euros y a D./Dña. [NOMBRE Y APELLIDOS], como propietario del vehículo marca [MARCA/MODELO], modelo [MARCA/MODELO], matrícula [MATRÍCULA], en la cantidad de [IMPORTE] euros, con declaración de la responsabilidad civil directa de la compañía aseguradora

En ejecución de sentencia penal mi representada abonó a los perjudicados los daños y lesiones causados, por importe total de [IMPORTE] euros, cantidad que con los intereses y costas reclama en la presente demanda.

Se acompaña como documento n.º [NÚMERO] testimonio de actuaciones penales.

TERCERO.- La parte actora manifiesta que, previo a la presentación de la presente demanda, se han llevado a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad, y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria; incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución (documentos números [Nº DE DOCUMENTO]).

Finalmente, con anterioridad a la presentación de la demanda se ha requerido de pago al demandado, mediante burofax de fecha [FECHA], que se acompaña como documento n.º [NÚMERO], sin que la reclamación haya sido atendida hasta la fecha, lo que fuerza acudir a la vía judicial.

A estos hechos le son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA.

Radicando la competencia genérica en el orden civil de la jurisdicción, detenta la competencia objetiva y funcional la Sección Civil del Tribunal de Instancia, por aplicación de lo dispuesto en los arts. 85.1 LOPJ y art. 45 LEC.

Conforme a lo dispuesto en el ordinal 9.º del art. 52.1 LEC es territorialmente competente el Tribunal de [LOCALIDAD] por ser el del lugar en el que tuvo lugar el siniestro.

II.- PROCEDIMIENTO.

La presente demanda deberá sustanciarse por las normas del juicio ordinario, a tenor de lo prevenido en los arts. 248 y 249.2 LEC, toda vez que el criterio de atribución preferente de la materia objeto del proceso resulta inaplicable, al carecer de especialidad típica la de éste, y cumplir entonces el criterio de cuantía, que rebasa con creces los quince mil euros.

III.- CAPACIDAD Y LEGITIMACIÓN.

Mi mandante es persona jurídica mercantil, sociedad anónima con capacidad para ser parte (art. 6.1.3.º LEC) por su constitución en documento público inscrito en el Registro Mercantil, que goza de capacidad procesal a través de la actuación de sus representantes orgánicos o necesarios (art. 7.4 LEC), y el demandado es persona física, mayor de edad, en pleno ejercicio de sus derechos civiles, por lo que tiene capacidad para ser parte y capacidad procesal ex arts. 6.1.1.º y 7.1 LEC.

IV.- LEGITIMACIÓN.

El art. 10 LEC legitima para comparecer y actuar en juicio, a los titulares de la relación jurídica o del objeto litigioso, lo cual es legitimación ordinaria, detentando la activa originaria la demandante, por su condición de aseguradora del vehículo causante de los daños, en cuanto es titular de un derecho subjetivo de carácter legal derivado del hecho de la circulación y del seguro obligatorio de responsabilidad civil que permite la repetición del coste de los daños al conductor de vehículo, que ostenta la legitimación pasiva correlativa, como causante de daños y perjuicios a terceros como consecuencia de la conducción de un vehículo a motor bajo la influencia de bebidas alcohólicas; daños a cuya indemnización y pago se ha visto obligada mi mandante como consecuencia de una sentencia penal condenatoria firme.

V.- CUANTÍA DE LA DEMANDA.

La cuantía de la demanda a los efectos de lo dispuesto en el art. 253.1 LEC es la de [IMPORTE] euros, en aplicación de la regla 1.ª del art. 251, según el cual si se reclama una cantidad de dinero determinada, la cuantía de la demanda estará representada por dicha cantidad.

VI.- POSTULACIÓN Y DEFENSA.

Conforme a los arts. 23 y 31 LEC se deduce esta demanda por medio de Procurador/a de los Tribunales con poder notarial para pleitos, y con dirección y firma de Letrado habilitado ante el tribunal. Asimismo se cumplen los requisitos formales del art. 399 LEC.

VII. Cumplimiento de los requisitos de procedibilidad

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VIII.- FONDO DEL ASUNTO.

El art. 10 a) del Texto Refundido de la Ley sobre responsabilidad civil y seguro en la circulación de vehículos a motor, aprobado por Real Decreto Legislativo 8/2004, de 29 de octubre, reconoce a mi representada, una vez efectuado el pago de la indemnización, la facultad de repetición contra el conductor del vehículo, si el daño causado fuera debido a la conducción bajo la influencia de bebidas alcohólicas.

IX.- INTERESES.

Deben reconocerse a mi patrocinada los intereses moratorios de los arts. 1.100, 1.101 y 1.108 CCiv desde la interpelación extrajudicial de fecha [FECHA], con devengo al tipo legal del dinero hasta el dictado de sentencia, y a partir de entonces, rindiendo los intereses procesales del art. 576 LEC, ya que la cantidad reclamada es líquida previamente a la constitución en mora, y no deuda de valor.

X.- COSTAS.

Conforme al art. 394 LEC, las costas han de imponerse a la demandada por el vencimiento.

En virtud de lo expuesto,

AL TRIBUNAL SUPLICO,

que habiendo por presentado este escrito, con el poder que acredita la representación procesal, y los documentos acompañados, y copias de todo ello, se sirva admitir uno y otros, tener por formulada demanda de juicio ordinario, en nombre de quien comparezco, contra D./Dña. [NOMBRE Y APELLIDOS], y seguidos que sean los trámites legales, dicte sentencia por la que estimando íntegramente esta demanda, se condene al demandado a abonar a mi representada la suma de [IMPORTE] euros, más los intereses correspondientes al tipo legal desde el día [FECHA], fecha de la reclamación extrajudicial de la deuda, pronunciando las costas del presente procedimiento a cargo del demandado.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
