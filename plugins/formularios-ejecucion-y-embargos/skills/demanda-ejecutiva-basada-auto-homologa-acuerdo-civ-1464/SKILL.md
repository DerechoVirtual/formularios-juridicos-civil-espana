---
name: demanda-ejecutiva-basada-auto-homologa-acuerdo-civ-1464
description: "Demanda ejecutiva basada en el auto que homologa un acuerdo de mediación. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda ejecutiva basada en el auto que homologa un acuerdo de mediación

> Formulario **CIV-1464** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Demanda ejecutiva de auto que homologa acuerdo adoptado en procedimiento de mediación, con previo proceso judicial abierto suspendido

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda ejecutiva basada en el auto que homologa un acuerdo de mediación» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda ejecutiva basada en el auto que homologa un acuerdo de mediación” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:demanda-ejecutiva-basada-auto-homologa-acuerdo-civ-1464`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (9 veces)
- [ ] NÚMERO (6 veces)
- [ ] IMPORTE (3 veces)
- [ ] Nº (3 veces)
- [ ] AÑO (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] CALLE
- [ ] DENOMINACIÓN SOCIAL
- [ ] FOLIO
- [ ] LIBRO
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] NOMBRE DE LA INSTITUCIÓN DE MEDIACIÓN
- [ ] NOMBRE DE LA PARTE
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº DE PROCEDIMIENTO
- [ ] SEDE

## Normas que cita el formulario

- art. 415.1 LEC
- art. 517.1 LEC
- art. 545.1 LEC
- art. 19 LEC
- art. 538.1 LEC
- art. 539.1 LEC
- art. 549 LEC
- art. 548 LEC
- art. 576 LEC

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

D./Dña. [NOMBRE Y APELLIDOS] Procurador/a. de los Tribunales, que actúa en nombre y representación de [NOMBRE DEL REPRESENTADO/A], tal y como acreditaré mediante apoderamiento "apud acta" en el momento en que sea requerido por el Tribunal, ante tal Tribunal comparezco y como mejor proceda en derecho, DIGO:

Que en la representación que ostento formulo DEMANDA EJECUTIVA contra la entidad [DENOMINACIÓN SOCIAL], con domicilio en [LOCALIDAD], calle [CALLE], en reclamación de la cantidad de [IMPORTE] euros en concepto de principal, más la de [IMPORTE] euros en concepto de intereses moratorios procesales y costas de la ejecución, presupuestadas provisionalmente, con base en los siguientes:

HECHOS

PRIMERO.- Mediante decreto dictado por el Letrado de la Administración de Justicia en fecha [FECHA], en el marco del procedimiento de juicio ordinario n.º [Nº DE PROCEDIMIENTO]/[AÑO], tras petición conjunta de mi mandante y la parte demandada en la audiencia previa celebrada el [FECHA], se suspendió el indicado procedimiento declarativo, de conformidad con el artículo 415.1 LEC.

SEGUNDO.- En el subsiguiente procedimiento de mediación n.º [Nº]/[AÑO], iniciado tras dicha suspensión, desarrollado ante la Institución [NOMBRE DE LA INSTITUCIÓN DE MEDIACIÓN] y dirigido por el mediador D./Dña. [NOMBRE Y APELLIDOS], se alcanzó por las partes un acuerdo para decidir las consecuencias de la resolución de un contrato de permuta, recogido en el acta final firmada el [FECHA], del siguiente tenor: y [NOMBRE DE LA PARTE] ponen fin a sus diferencias en relación con el contrato de permuta firmado entre ambos el [FECHA], y resuelto el [FECHA]; acordando que la primera abonará a las segunda la cantidad de [IMPORTE] euros en el plazo de un mes desde la homologación judicial del acuerdo.

Se acompaña copia del acta, como documento n.º [NÚMERO].

TERCERO.- Con fecha [FECHA], se presentó por las partes el acuerdo para su homologación, dictándose auto por el órgano judicial a quien tengo el honor de dirigirme el [FECHA], mediante el cual se puso fin al procedimiento declarativo indicado, siendo dicha resolución firme. Se acompaña testimonio de dicho auto como documento n.º [NÚMERO].

CUARTO.- Han transcurrido más de veinte días desde el [Nº], mes posterior a la homologación judicial, habiéndose intentado por mi representada infructuosamente percibir de parte contraria la cantidad pactada, viéndose obligado a interponer la correspondiente demanda.

QUINTO.- Mi mandante tiene conocimiento de que la entidad ejecutada es titular del siguiente bien susceptible de embargo, que se considera suficiente para el fin de la ejecución:

- Finca n.º [NÚMERO] inscrita en el Registro de la Propiedad n.º [NÚMERO] de Madrid, el [FECHA], en el libro [LIBRO], folio [FOLIO], inscripción ª.

A los anteriores hechos resultan de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

PRIMERO.- Conforme al art. 517.1 LEC la acción ejecutiva deberá fundarse en un título que tenga aparejada ejecución, encontrándose entre éstos, como dispone el art. 517.2.3.º del mismo texto legal, los autos de homologación judicial de acuerdos.

SEGUNDO.- El Tribunal a que me dirijo es el tribunal competente, según lo establecido por los arts. 545.1 LEC y 26 párrafo 1.º de la Ley 5/2012, de 6 de julio, de mediación en asuntos civiles y mercantiles; por ser el órgano judicial que homologó el acuerdo alcanzado conforme a lo dispuesto en los arts. 19 LEC y 25.4 de la mencionada legislación especial.

TERCERO.- Las partes en este concreto proceso de ejecución, ejecutante y ejecutado, quedan determinadas mediante legitimación ordinaria directa, con arreglo al art. 538.1 LEC como acreedor y deudor que figuran en el título ejecutivo, siendo mi mandante titular de crédito pecuniario de la cantidad indicada frente a la sociedad demandada.

CUARTO.- Conforme a lo dispuesto en el art. 539.1 V LEC, la demanda viene firmada por el abogado que dirige la pretensión, y Procurador/a. que representa a la parte, ya que es preceptiva la intervención de dichos profesionales por rebasar la cantidad reclamada los 2.000 euros.

QUINTO.- La presente demanda contiene todos los requisitos enumerados en el art. 549 LEC, ya que se ha indicado cuál es el título en que se funda, la tutela ejecutiva que se pretende y la entidad frente a la que se interesa el despacho de la ejecución, así como los bienes del ejecutado susceptibles de embargo conocidos por mi poderdante. Así, se adjunta a la demanda ejecutiva la documentación necesaria: el acuerdo de mediación homologado incorporado al acta final (doc. n.º [NÚMERO]), y el auto de homologación, como título ejecutivo (documento n.º [NÚMERO]). Asimismo, se ha superado con creces el plazo de espera de 20 días del art. 548 LEC, desde la homologación en sí, dado que ha transcurrido el plazo del mes específicamente previsto en el acuerdo de mediación que aquí se pretende ejecutar.

SEXTO. Procede la imposición del pago del interés por mora procesal del art. 576 LEC, dado que si el auto resulta ejecutable por los trámites establecidos para la ejecución forzosa en la Ley de Enjuiciamiento Civil, y el establecimiento de una obligación de pago de suma en aquél se hace equivalente a una condena firme de cantidad líquida, tal y como se dispone en el apartado tercero de aquel precepto legal.

SEPTIMO.- En virtud de lo dispuesto en el art. 539.2, párrafo 2.º en relación con el 583.2 LEC, las costas de la ejecución serán a cargo del ejecutado, puesto que no es preciso ninguna imposición expresa.

Por lo anteriormente expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito con los documentos que se acompañan, y sus copias, se sirva admitirlo, ordenando se entiendan conmigo las sucesivas diligencias y en nombre de mi patrocinado se me tenga por comparecido y parte, y por presentada demanda ejecutiva, se digne, previo el traslado legal, despachar ejecución frente a, por el importe de la cantidad de dieciocho mil euros (€) en concepto de principal, más otros seis mil euros (€) presupuestados provisionalmente para los intereses que puedan generarse durante la ejecución y las costas de ésta, procediéndose, mediante decreto del Letrado de la Administración de Justicia, al embargo de la finca designada en el ordinal 5.º de los hechos de esta demanda, que deberá asegurarse mediante mandamiento dirigido al Registrador de la Propiedad de Madrid, como es justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a

========================================================================
