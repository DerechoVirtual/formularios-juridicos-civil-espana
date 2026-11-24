---
name: demanda-ejecutiva-sentencia-extranjera-conforme-civ-1394
description: "Demanda ejecutiva de sentencia extranjera conforme al Reglamento (UE) nº 1215-2012. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda ejecutiva de sentencia extranjera conforme al Reglamento (UE) nº 1215-2012

> Formulario **CIV-1394** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Demanda de ejecución de título judicial extranjero en reclamación de cantidad, al amparo del Reglamento (UE) no 1215/2012 del Parlamento Europeo y del Consejo, de 12 de diciembre de 2012, relativo a la competencia judicial, el reconocimiento y la ejecución de resoluciones judiciales en materia civil y mercantil.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda ejecutiva de sentencia extranjera conforme al Reglamento (UE) nº 1215-2012» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda ejecutiva de sentencia extranjera conforme al Reglamento (UE) nº 1215-2012” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:demanda-ejecutiva-sentencia-extranjera-conforme-civ-1394`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (8 veces)
- [ ] IMPORTE (6 veces)
- [ ] FECHA (4 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] LUGAR (2 veces)
- [ ] NOMBRE DE LA PARTE (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] AÑO
- [ ] COLEGIO
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] NIF
- [ ] Nº
- [ ] Nº DE DOCUMENTO
- [ ] PARTE DEMANDADA
- [ ] PAÍS
- [ ] SEDE
- [ ] ÓRGANO JUDICIAL
- [ ] ÓRGANO O PERSONA

## Normas que cita el formulario

- art. 545.3 LEC
- art. 523.1 LEC
- art. 517.2.1.º LEC
- art. 539.1 LEC
- art. 550.1.2.º LEC
- art. 549 LEC
- art. 576 LEC
- art. 539.2 LEC
- art. 589 LEC
- art. 549.1.3.º LEC
- art. 551.3.1.º LEC
- art. 590 LEC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: Un solo TI por partido judicial (art. 84.1 LOPJ): sobra «de los de». Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) Respecto al reconocimiento y ejecución de títulos ejecutivos extranjeros, el Reglamento 1215/2012 solo es aplicable a aquellas solicitudes de reconocimiento o ejecución de resoluciones extranjeras dictadas en procedimientos judiciales iniciados con posterioridad al 10 de enero de 2015. Para la ejecución de sentencias extranjeras dictadas en un procedimiento iniciado con anterioridad a dicha fecha, se sigue aplicando el Reglamento 44/2001, del Consejo, de 22 de diciembre de 2000, relativo a la competencia judicial, el reconocimiento y la ejecución de resoluciones judiciales en materia civil y mercantil.


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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.C.

D./Dña. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], con D.N.I. n.º [NÚMERO] y domicilio en [LOCALIDAD], según acredito con la escritura de poder que acompaño, solicitando que se me devuelva una vez testimoniada en Autos, por ser poder general para pleitos y necesitarlo para otros usos, y bajo la dirección del Letrado/a [NOMBRE Y APELLIDOS], colegiado n.º [NÚMERO] del Ilustre Colegio de Abogados de [COLEGIO], con despacho profesional en [LOCALIDAD], ante el Tribunal comparezco y, como mejor proceda en Derecho, DIGO:

Que mediante el presente escrito vengo a formular DEMANDA EJECUTIVA contra [PARTE DEMANDADA], con N.I.F [NIF], y domicilio en [LOCALIDAD], con base en sentencia extranjera dictada por la Corte de [LOCALIDAD] del Estado miembro de [PAÍS] con fecha [FECHA], al amparo del Reglamento (UE) nº 1215/2012 del Parlamento Europeo y del Consejo, de 12 de diciembre de 2012, relativo a la competencia judicial, el reconocimiento y la ejecución de resoluciones judiciales en materia civil y mercantil (en adelante, Reglamento de Bruselas I bis), en reclamación de la cantidad de [IMPORTE] EUROS (€) en concepto de principal, [IMPORTE] EUROS (€) en concepto de intereses vencidos, así como de otros [IMPORTE] EUROS (€) presupuestados inicialmente para los intereses que puedan devengarse durante la ejecución y las costas de ésta.

Fundamento la presente demanda de ejecución dineraria en los siguientes

HECHOS

PRIMERO.- El pasado día [FECHA], por [ÓRGANO JUDICIAL], en autos de acción ordinaria n.º [Nº]/[AÑO], se dictó sentencia que en su parte dispositiva decía lo siguiente:

Acompaño como documentos números [Nº DE DOCUMENTO] copia auténtica de la resolución y certificado expedido conforme al artículo 53 del Reglamento de Bruselas I bis.

SEGUNDO.- En dicho proceso fueron parte actora [NOMBRE DE LA PARTE], y parte demandada [NOMBRE DE LA PARTE], ambas comparecidas ante el tribunal de [LOCALIDAD], que se declaró competente por razón de la nacionalidad, de la materia, y de la jerarquía.

TERCERO.- Dado que hasta la fecha no se han abonado por la condenada las cantidades fijadas en la sentencia dictada en el reseñado proceso, me veo en la necesidad de formular demanda ejecutiva, a la que son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA INTERNACIONAL.

Resulta de aplicación el Reglamento de Bruselas I bis.

Conforme al art. 39 del citado Reglamento, las resoluciones dictadas en un Estado miembro que tengan fuerza ejecutiva en él gozarán también de esta en los demás Estados miembros sin necesidad de una declaración de fuerza ejecutiva, siendo competente el Estado requerido al tratarse del lugar de ejecución en el que tiene el domicilio el ejecutado.

II.- COMPETENCIA TERRITORIAL.

Es competente el Tribunal al que me dirijo, por ser el domicilio del deudor, de conformidad con lo previsto en los arts. 545.3, 50 y 51 LEC.

III.- EJECUCIÓN DE SENTENCIAS EXTRANJERAS.

De conformidad con lo dispuesto en el art. 523.1 LEC, para que las sentencias firmes y demás títulos ejecutivos extranjeros lleven aparejada ejecución en España se estará a lo dispuesto en los Tratados internacionales y a las disposiciones legales sobre cooperación jurídica internacional.

El art. 2.a) del Reglamento Bruselas I bis, dentro del sentido del término resolución, comprende cualquier decisión adoptada por un tribunal de un Estado miembro con independencia de la denominación que recibiere, tal como auto, sentencia, providencia o mandamiento de ejecución, así como el acto por el cual el Letrado de la Administración de Justicia liquidare las costas del proceso.

IV.- TÍTULO Y LEGITIMACIÓN.

Se solicita el despacho de ejecución por quien aparece como acreedor en el título ejecutivo, y frente a quien aparece como deudor en el mismo título, que es sentencia firme de condena (art. 517.2.1.º LEC, en relación con el art. 523 del mismo cuerpo legal), como se concluye de la lectura de la parte dispositiva de la sentencia dictada por [ÓRGANO O PERSONA].

V.- PRESUPUESTOS FORMALES.

Las modalidades de presentación de la solicitud se determinarán con arreglo a la ley del Estado miembro en el que se solicitare la ejecución (art. 40.1 del Reglamento Bruselas I bis).

El procedimiento de ejecución de las resoluciones dictadas en otro Estado miembro se regirá por el Derecho del Estado miembro requerido. Las resoluciones dictadas en un Estado miembro que tengan fuerza ejecutiva en el Estado miembro requerido serán ejecutadas en este en las mismas condiciones que si se hubieran dictado en el Estado miembro requerido (art. 41.1 del Reglamento Bruselas I bis).

Conforme a lo dispuesto en el art. 539.1 LEC, la demanda viene firmada por abogado en ejercicio, y a la ejecutante representa procurador de los tribunales habilitado ante el tribunal, con aportación del poder (art. 550.1.2.º LEC), ya que no estamos ante la ejecución de una resolución dictada en un proceso en que, por excepción, no sea preceptiva la intervención de dichos profesionales.

La presente demanda contiene todos los requisitos enumerados en el art. 549 LEC, ya que se indica cual es el título en que se funda, la tutela ejecutiva que se pretende y las personas frente a las que se interesa el despacho de la ejecución, los bienes del ejecutado susceptibles de embargo conocidos por mi poderdante, así como las medidas de localización e investigación de otros bienes del ejecutado, dada la insuficiencia de los reseñados.

Por último, en cumplimiento de lo establecido en el art. 37 del Reglamento Bruselas I bis, se aporta una copia de la resolución, que reúne los requisitos necesarios para ser considerada auténtica, así como certificado expedido conforme a lo dispuesto en el art. 53 del citado Reglamento, acreditativo de que la resolución tiene fuerza ejecutiva y que recoge un extracto de la resolución, así como la información pertinente sobre las costas impuestas en el procedimiento y el cálculo de los intereses.

VI.- INTERESES.

Conforme a lo establecido en el art. 576 LEC, desde que fuere dictada sentencia en primera instancia, toda sentencia o resolución que condene al pago de una cantidad de dinero líquida determinará, a favor del acreedor, el devengo de un interés anual igual al del interés legal del dinero incrementado en dos puntos o el que corresponda por pacto de las partes o por disposición especial de la ley.

VII.- COSTAS.

En virtud de lo dispuesto en el art. 539.2 LEC en relación con el 583, las costas de esta ejecución deberán ser impuestas al ejecutado, ya que ha sido quien ha originado la necesidad de este procedimiento al no haber cumplido voluntariamente con lo establecido en la sentencia recaída en las presentes actuaciones.

Por lo expuesto,

SUPLICO AL TRIBUNAL:

Que se sirva tenerme por comparecido y parte en la representación que ostento, tener por presentado este escrito de DEMANDA DE EJECUCIÓN DE TÍTULOS JUDICIALES con los documentos que se acompañan y sus prevenidas copias, se digne admitirlo a trámite, y

DICTE auto despachando la ejecución solicitada por el importe de la cantidad de [IMPORTE] EUROS (€), en concepto de principal, [IMPORTE] EUROS (€) en concepto de intereses devengados hasta la fecha, más otros [IMPORTE] EUROS (€) presupuestadas provisionalmente para los intereses que puedan generarse durante la ejecución y las costas de ésta, y

REQUIERA de pago al deudor por el importe antes indicado por el que se ha despachado la ejecución, y mediante resoluciones del Letrado de la Administración de Justicia

REQUIERA al deudor, mediante diligencia de ordenación, para que, de conformidad con lo previsto en el art. 589 LEC, manifieste bienes suficientes para el buen fin de la ejecución, con los apercibimientos legales, y

ACUERDE, mediante decreto, el embargo de bienes en cantidad suficiente para cubrir las mencionadas cantidades hasta hacer completo pago a mi representado, con imposición al demandado de las costas del procedimiento.

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a

PRIMER OTROSÍ DIGO: A efectos de lo dispuesto en el art. 549.1.3.º LEC, se señalan como bienes del deudor susceptibles de embargo los siguientes: [DESCRIPCIÓN DEL BIEN].

Por lo expuesto,

SUPLICO AL TRIBUNAL: Que conforme a lo previsto en el art. 551.3.1.º LEC, acuerde, mediante decreto del Letrado de la Administración de Justicia, el embargo de los bienes concretamente señalados y, a tal efecto, libre los siguientes oficios: haciéndoseme entrega de los despachos para cuidar de su diligenciamiento.

SEGUNDO OTROSÍ DIGO: Que entendiendo esta parte que los bienes señalados para su embargo no son suficientes para el buen fin de la ejecución, interesamos, de conformidad con el art. 590 LEC, que por el Letrado/a de la Administración de Justicia se acuerde librar los siguientes despachos:

- Al Tribunal Decano de [LOCALIDAD], Oficina de Averiguación Patrimonial para que comunique los bienes o derechos que le consten respecto del deudor.
- A la oficina de Renta y Patrimonio del Excmo. Ayuntamiento de [LOCALIDAD], a fin de que, por quien corresponda, sea expedida certificación acreditativa de los conceptos por los que el deudor figure como contribuyente al mismo, con indicación en su caso de la entidad bancaria y número de cuenta donde consten domiciliados los pagos, y demás datos patrimoniales que tengan respecto de la parte demandada.
- A la Delegación Provincial de la Tesorería General de la Seguridad Social de [LOCALIDAD], para que indique su concepto de afiliación y los datos de la empresa u organismo para el que se encuentra prestando sus servicios, o bien las prestaciones que perciba del sistema.
- A la Agencia Estatal de la Administración Tributaria, para que se expida y remita a ese Tribunal certificación acreditativa de los bienes muebles, inmuebles, y medios de fortuna que le sean conocidos por dicho Organismo a la parte deudora; y
- Al Servicio de Índices del Colegio de Registradores de la Propiedad y Mercantiles de España, sito en la c/, a fin de que informe de los derechos que les consten inscritos a su favor.

Por lo expuesto,

SUPLICO AL TRIBUNAL: Que teniendo por realizadas las anteriores manifestaciones acuerde según se ha dejado interesado, haciéndoseme entrega de los despachos para cuidar de su diligenciamiento.

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a
