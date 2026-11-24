---
name: demanda-ejecutiva-sentencia-firme-division-cosa-comun-civ-1579
description: "Demanda ejecutiva de sentencia firme de división de cosa común sobre finca rústica. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda ejecutiva de sentencia firme de división de cosa común sobre finca rústica

> Formulario **CIV-1579** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Demanda ejecutiva al Tribunal de Instancia solicitando se cumpla la sentencia sobre declaración de indivisibilidad y venta de finca rústica en pública subasta, sentencia firme tras la desestimación del recurso de apelación por la Audiencia Provincial.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda ejecutiva de sentencia firme de división de cosa común sobre finca rústica» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda ejecutiva de sentencia firme de división de cosa común sobre finca rústica” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:demanda-ejecutiva-sentencia-firme-division-cosa-comun-civ-1579`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (10 veces)
- [ ] NÚMERO (5 veces)
- [ ] FECHA (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] LUGAR (2 veces)
- [ ] CALLE
- [ ] FOLIO
- [ ] Nº
- [ ] SECCIÓN
- [ ] SEDE
- [ ] TIPO DE PROCEDIMIENTO
- [ ] TOMO

## Normas que cita el formulario

- art. 545.1 LEC
- art. 538.1 LEC
- art. 539.1 LEC
- art. 517.2.1.º LEC
- art. 548 LEC
- art. 518 LEC
- art. 549 LEC
- art. 583 LEC
- art. 656 LEC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a. de los Tribunales, que actúa en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], según tengo acreditado, junto con la dirección letrada y las circunstancias personales, en los autos de Juicio ordinario n.º [NÚMERO], seguidos a instancias de D./Dña. [NOMBRE Y APELLIDOS] frente a D./Dña. [NOMBRE Y APELLIDOS], ante el Tribunal comparezco y, como mejor proceda en Derecho, DIGO:

Que mediante el presente escrito formulo DEMANDA EJECUTIVA de título judicial de sentencia de condena firme sobre declaración de indivisibilidad y venta de finca rústica en pública subasta, contra D./Dña. [NOMBRE Y APELLIDOS], domiciliado en esta ciudad, calle [CALLE], n.º [NÚMERO], cuyas circunstancias constan en los autos principales, donde se halla personada, fundamentando dicha pretensión en los siguientes:

HECHOS

PRIMERO.- El pasado día [FECHA] por el Tribunal al que me dirijo se dictó sentencia cuya parte dispositiva es del tenor literal siguiente: "FALLO: Que estimando la demanda formulada por D./Dña. [NOMBRE Y APELLIDOS], representado por el Procurador/a. Sr./a. [NOMBRE Y APELLIDOS], contra D./Dña. [NOMBRE Y APELLIDOS], representado por el Procurador/a. Sr./a. [NOMBRE Y APELLIDOS], debo declarar y declaro disuelta la comunidad de bienes o copropiedad existente entre las partes litigantes sobre la finca registral n.º [NÚMERO] del Registro de la Propiedad n.º [NÚMERO] de [LOCALIDAD], inscrita al tomo [TOMO], folio [FOLIO] y, siendo indivisible, debe procederse a su venta en pública subasta, con admisión de licitadores externos, debiendo repartirse el precio, una vez deducidos los gastos que se produzcan, a cargo de ambos partes, por mitad.".

SEGUNDO.- Dicha sentencia ha devenido firme tras la desestimación del recurso de apelación fallado por la Sección [SECCIÓN] de la Audiencia Provincial de [LOCALIDAD], habiendo transcurrido más de veinte días desde que se notificó la resolución de condena al demandado.

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA.

Corresponde la competencia para conocer de esta ejecución al Tribunal que nos dirigimos, conforme a la regla que aúna en la funcional, toda la demás específica, objetiva y territorial, determinada en el art. 545.1 LEC, puesto que fue el que dictó la sentencia que se ejecuta.

II.- CAPACIDAD Y LEGITIMACIÓN.

Se cumplen los requisitos de capacidad, en tanto que personas físicas ejecutante y ejecutado, que fueron partes en el proceso declarativo del que surge la ejecutoria, legitimadas conforme al art. 538.1 LEC.

III.- POSTULACIÓN.

Conforme a lo dispuesto en el art. 539.1 LEC, la demanda viene firmada por abogado y Procurador/a., ya que estamos ante la ejecución de una resolución dictada en un proceso en que es preceptiva la intervención de dichos profesionales.

IV.- TÍTULO DE EJECUCIÓN.

El art. 517.2.1.º LEC enumera como uno de los títulos que lleva aparejada ejecución la sentencia de condena firme, como la que sirve de fundamento a esta demanda.

V.- REQUISITOS TEMPORALES.

La resolución de condena se ha notificado al ejecutado hace más de veinte días (art. 548 LEC) y la demanda ejecutiva se ha interpuesto sin que hayan transcurrido los cinco años siguientes a la firmeza de la sentencia, que el art. 518 LEC fija como de caducidad de la acción ejecutiva.

VI.- REQUISITOS FORMALES.

La presente demanda contiene todos los requisitos enumerados en el art. 549 LEC, ya que se ha indicado cual es el título en que se funda, la tutela ejecutiva que se pretende y las personas frente a las que se interesa el despacho de la ejecución.

VII.- COSTAS.

En materia de imposición de costas resultan de aplicación los arts. 583, 394, 539 y 561 LEC que la prevén a cargo de la parte ejecutada., para el caso de que se opusiere a la ejecución interesada.

Por todo ello,

SUPLICO AL TRIBUNAL:

Que teniendo por presentado este escrito junto con su copia, se sirva admitirlo, ordenando se entiendan conmigo las sucesivas diligencias y en nombre de mi patrocinado se tenga por presentada demanda ejecutiva contra D./Dña. [NOMBRE Y APELLIDOS], y siendo firme la sentencia dictada en el juicio de [TIPO DE PROCEDIMIENTO] n.º [NÚMERO], se proceda a su ejecución forzosa, acordándose despachar ejecución en la forma ordenada por la Ley, una vez examinados los requisitos y presupuestos procesales, el título ejecutivo y los actos de ejecución que se solicitan, así como la propia competencia y, en consecuencia, proceder a la venta en pública subasta de la finca descrita en el hecho primero de la demanda, tal y como determina la sentencia dictada en los presentes autos, celebrándose dicha subasta de conformidad con los arts. 655 y ss. LEC. Todo ello con imposición de las costas al ejecutado que se opusiera.

Es Justicia de hacerse en [LUGAR], a [FECHA].

PRIMER OTROSÍ DIGO: Que conforme a lo dispuesto en el art. 656 LEC procede que el Tribunal libre mandamiento al Registro de la Propiedad de [LOCALIDAD], a fin de que remita al Tribunal certificación de dominio y cargas de la finca descrita en el hecho primero de la demanda.

SEGUNDO OTROSÍ DIGO: Que con arreglo a lo dispuesto en los arts. 666, y 637 y ss. LEC procede sea valorada la finca a subastar, debiendo ser nombrado, en su consecuencia, un PERITO TASADOR del inmueble referido.

De conformidad con lo anteriormente expuesto,

SUPLICO AL TRIBUNAL que, teniendo por hechas las anteriores manifestaciones, se sirva admitirlas, interesando, desde este momento, se practiquen tales diligencias, como es Justicia que reitero en lugar y fecha "ut supra".

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a

========================================================================
