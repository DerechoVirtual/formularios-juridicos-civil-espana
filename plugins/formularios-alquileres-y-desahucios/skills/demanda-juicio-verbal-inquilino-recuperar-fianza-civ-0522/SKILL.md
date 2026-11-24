---
name: demanda-juicio-verbal-inquilino-recuperar-fianza-civ-0522
description: "Demanda de juicio verbal del inquilino para recuperar la fianza de vivienda (LAU 1994). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio verbal del inquilino para recuperar la fianza de vivienda (LAU 1994)

> Formulario **CIV-0522** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio verbal en reclamación por el arrendatario de la fianza entregada en su día al arrendador una vez finalizado el arrendamiento.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio verbal del inquilino para recuperar la fianza de vivienda (LAU 1994)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio verbal del inquilino para recuperar la fianza de vivienda (LAU 1994)” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:demanda-juicio-verbal-inquilino-recuperar-fianza-civ-0522`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] FECHA (6 veces)
- [ ] IMPORTE (6 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] NÚMERO (4 veces)
- [ ] DOMICILIO (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] CORREO ELECTRÓNICO
- [ ] DIRECCIÓN
- [ ] FECHAS
- [ ] LUGAR
- [ ] Nº
- [ ] Nº DE COLEGIADO/A
- [ ] SEDE
- [ ] TELÉFONO

## Normas que cita el formulario

- art. 24.1 LEC
- art. 437.1 LEC
- art. 21.1 LOPJ
- art. 36.1 LEC
- art. 85.1 LOPJ
- art. 45 LEC
- art. 52.1.7.º LEC
- art. 249.1.6.º LEC
- art. 250.2 LEC
- art. 10 LEC
- art. 253.1 LEC
- art. 251 LEC
- art. 32.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 36.4 LAU
- art. 36 LAU
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

Notas al pie del formulario original:
(1) A la hora de su acreditación, todos los poderes deben estar inscritos en el Registro Electrónico de Apoderamientos Judiciales (REAJ). Se supone que, para su acreditación, basta con la consulta (de dicho Registro) automatizada orientada al dato. Algo que está a disposición de cualquier Letrado de la Administración de Justicia. Sin embargo, dado que el art. 24.2 LEC, configura la certificación de dicha inscripción como vía subsidiaria de acreditación, para el caso de que el sistema no permita aquella consulta automatizada; se señala en el modelo que se acompaña certificación electrónica. El sistema permite emitir dicha certificación para quien inscribe el poder.

(2) El art. 155.3 LEC permite fijar expresar varios domicilios del demandado (el que aparezca en el padrón municipal o conste oficialmente a estos efectos; el que aparezca en Registro oficial o en publicaciones de colegios profesionales, si se trata de empresas o personas colegiadas; donde desarrolle su actividad profesional o laboral no ocasional; si es empresa mercantil, el domicilio de cualquiera de sus administradores, gerentes, o apoderados; o, si es asociación que consta en registro oficial; el domicilio del presidente, miembro o gestor de la Junta correspondiente). Cuando se señalen varios, indicará el orden a seguir para la notificación, con vistas al éxito de la misma.

(3) El art. 155.3 LEC configura una obligación adicional del demandante, consistente en aportar cuantos datos sean de utilidad para localizar al demandado: número de identificación fiscal o de extranjeros, nº [Nº] de teléfono o de fax, dirección de correo electrónico, o similares.

========================================================================


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

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], representación que acredito mediante escritura de poder otorgada a mi favor (existen tres posibilidades para otorgar el apoderamiento al Procurador de los Tribunales, conforme dispone el art. 24.1 LEC)

[OPCIONAL — opción en función de cómo se haya otorgado el poder]

[ELEGIR UNA OPCIÓN: Si el poder se otorga a través de la sede judicial electrónica / Si el poder se otorga mediante comparecencia apud acta / Si el poder se otorga ante Notario]

bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS], abogado/a en ejercicio, con despacho profesional abierto en [LOCALIDAD], colegiado nº [Nº DE COLEGIADO/A] del Ilustre Colegio de la Abogacía de [LOCALIDAD], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que mediante el presente escrito vengo a formular DEMANDA DE JUICIO VERBAL EN RECLAMACIÓN DE FIANZA DE ARRENDAMIENTO URBANO, contra D./Dña. [NOMBRE Y APELLIDOS], con domicilio, primero en [DOMICILIO]; y segundo, el domicilio laboral en [DOMICILIO]); con email [CORREO ELECTRÓNICO]; y con número de teléfono móvil [TELÉFONO].

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa, e, incluso, en una eventual fase de ejecución por medios telemáticos, en términos del art. 399.1 II con relación al art. 437.1, ambos LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y nº [Nº] de teléfono:

Todo ello de conformidad con los siguientes hechos y fundamentos de derecho:

HECHOS

PRIMERO

Mi mandante D./Dña. [NOMBRE Y APELLIDOS] ocupaba en concepto de inquilino la vivienda sita en [LOCALIDAD], hasta el pasado [FECHA], según consta en la copia del contrato de arrendamiento que se adjunta como documento n.º [NÚMERO].

En dicho contrato se pactó una renta anual de [IMPORTE] euros.

SEGUNDO

El demandado D./Dña. [NOMBRE Y APELLIDOS] es propietario y hasta la fecha indicada arrendador del referido inmueble, en virtud de arrendamiento concertado con mi mandante, en fecha [FECHA].

A la celebración del contrato, se prestó fianza en metálico, por importe de [IMPORTE] euros, cantidad equivalente a una mensualidad de la renta pactada.

TERCERO

El contrato de arrendamiento se resolvió con fecha [FECHA], de muto acuerdo entre las partes contratantes, haciendo entrega mi mandante de las llaves del piso objeto de arrendamiento al demandado.

Se adjunta como documento n.º [NÚMERO] el escrito firmado por ambas partes acreditativo del acuerdo alcanzado para poner fin a la vigencia del contrato y recepción de las llaves por la propiedad.

CUARTO

Tras haber transcurrido más de un mes desde la finalización del arriendo y entrega de llaves de la vivienda, el arrendador se niega a devolver a mi mandante el importe de la fianza entregada en su día, y que asciende a [IMPORTE] euros, a pesar de haber sido requerido para ello, por lo que mi mandante se ve obligada a solicitar el auxilio judicial, lo que, efectivamente, se hace por medio del presente escrito.

Acompaño certificado de burofax como documento n.º [NÚMERO], y contestación escrita de la propiedad como documento n.º [NÚMERO].

QUINTO

La parte actora manifiesta que, previo a la presentación de la presente demanda, se han llevaron a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad, y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria; incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, mi representado envío un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por el demandado por el mismo medio, rechazando el acuerdo/ habiendo sido solo posible un acuerdo parcial, viéndonos en la necesidad de acudir a la presente vía judicial, respecto a los extremos de la controversia en los que se mantiene la discrepancia.

Acompaño como documento nº [Nº DE DOCUMENTO], el requerimiento efectuado y como documento nº [Nº DE DOCUMENTO], la contestación del demandado.

A estos hechos son de aplicación, los siguientes,

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA

La jurisdicción ordinaria es la única competente para el conocimiento de los juicios que se susciten en territorio español con arreglo a lo establecido en los tratados y convenios internacionales en los que España sea parte, en las normas de la Unión Europea y en las leyes españolas (art. 21.1 LOPJ y art. 36.1 LEC).

La competencia objetiva corresponde a la Sección Civil del Tribunal de Instancia según lo dispuesto en el art. 85.1 LOPJ y art. 45 LEC, así como la territorial con arreglo al art. 52.1.7.º LEC, puesto que el tribunal competente es el del lugar en que está sita la finca.

II.- PROCEDIMIENTO

La presente demanda deberá sustanciarse por las normas del juicio verbal, a tenor de lo prevenido en el art. 249.1.6.º LEC, por tratarse de mera reclamación de cantidad inferior a 15.000 euros, en aplicación de lo dispuesto en el art. 250.2 LEC.

III.- LEGITIMACIÓN ACTIVA Y PASIVA

Corresponde la activa a mi mandante por ser el arrendatario del inmueble; y la pasiva al demandado en su condición de arrendador de la vivienda (art. 10 LEC).

IV.- CUANTÍA

Conforme al art. 253.1 LEC cifro la cuantía de la presente demanda en [IMPORTE] euros ( [IMPORTE] €), que es el importe de la cantidad que se reclama, según resulta de la interpretación combinada de las reglas 1.ª y 9.ª del art. 251 LEC.

V.- POSTULACIÓN Y DEFENSA

En aplicación de los arts. 23.2.1.º y 31.2.1.º LEC, las partes están excusadas de comparecer representadas por Procurador de los Tribunales y asistidas por Letrado en ejercicio, sin embargo de lo cual, esta parte comparece representada por Procurador de los Tribunales y dirigida por Letrado habilitado ante el tribunal, y así se hace constar a los efectos del art. 32.1 LEC, para conocimiento de la contraparte.

VI.- Cumplimiento de los requisitos de procedibilidad

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 de la LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VII.- FUNDAMENTOS DE DERECHO MATERIALES O SOBRE EL FONDO DEL ASUNTO

En la presente demanda se ejercita por la parte actora reclamación de cantidad en concepto de devolución de fianza que en su día entregó a la parte arrendadora, constituida al formalizar el contrato de arrendamiento sobre la vivienda sita [DIRECCIÓN], tras la extinción de la relación arrendaticia, en base al art. 36.4 LAU 1994.

La fianza se regula en el Título IV de la Ley de Arrendamientos Urbanos de 24 de noviembre de 1994, que es la de aplicación al caso dada la fecha de celebración del contrato (febrero de 2 ) y se presta una sola vez en el momento de la referida celebración, siendo su finalidad garantizar el estado de la cosa localizada, y debiendo ser restituido el saldo de la fianza al arrendatario al final del arriendo.

En este sentido, el art. 36 LAU 1994 dispone la devolución del saldo de la fianza constituida en el plazo de un mes finalizado el arriendo, desde la entrega de llaves y momento a partir del cual devengará el interés legal.

Si la fianza cumple efectivamente una función de garantía, lo cierto es que la vivienda se entregó en el mismo estado en que se recibió por el arrendatario, y el arrendador aceptó las llaves del inmueble sin objeción alguna poniéndolo nuevamente en alquiler. Debiendo recordar que como señala la SAP Madrid de 20 de julio de 2001, rec. 1284/1998, la devolución de la fianza se configura "como una obligación del arrendador, consecuencia de la terminación normal del arriendo sin existencia de conceptos, tales como daños en el inmueble localizado o débitos, a los que aplicar la garantía prestada inicialmente por el arrendatario, según su propia finalidad aseguradora y debiendo incardinarse, como tal obligación del pacto en su conjunto entendido".

En igual sentido se mantiene en la SAP Las Palmas de 19 de septiembre de 2005, rec. 425/2005, entre otras muchas.

VIII.- COSTAS

Conforme al art. 394 LEC las costas del procedimiento habrán de imponerse a la parte demandada.

En su virtud,

AL TRIBUNAL SUPLICO,

que teniendo por presentado este escrito de demanda, junto con los documentos al mismo acompañados y copia de todo ello, por el Letrado de la Administración de Justicia se admita y, en su virtud, una vez dado traslado del mismo al demandado y después de cumplidos los demás trámites procesales, por el tribunal se dicte en su día sentencia por la que se condene a D./Dña. [NOMBRE Y APELLIDOS], a restituir a mi mandante la cantidad de [IMPORTE] euros en concepto de fianza arrendaticia constituida en su día, más los intereses legales de dicha cantidad devengados desde la fecha [FECHA], y todo ello con expresa imposición de las costas del presente procedimiento.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a
