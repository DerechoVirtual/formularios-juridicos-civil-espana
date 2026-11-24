---
name: demanda-juicio-verbal-precario-sobre-finca-urbana-civ-0682
description: "Demanda de juicio verbal de precario sobre finca urbana. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio verbal de precario sobre finca urbana

> Formulario **CIV-0682** del plugin **Propiedad, posesión, servidumbres e hipotecas** (`formularios-propiedad-y-derechos-reales`) · Civil › Propiedad y derechos reales · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio verbal de precario en el que el propietario de una vivienda por herencia de su padre, solicita del Tribunal que condene al demandado precarista a dejar libre y a su disposición la misma. Adaptada a la STC 26/2025, de 29 de enero; y a la reforma procesal de la LO 1/2025.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio verbal de precario sobre finca urbana» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio verbal de precario sobre finca urbana” para mi caso». También puedes invocarla directamente con `/formularios-propiedad-y-derechos-reales:demanda-juicio-verbal-precario-sobre-finca-urbana-civ-0682`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-propiedad-y-derechos-reales:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Propiedad, posesión, servidumbres e hipotecas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] Nº DE DOCUMENTO (5 veces)
- [ ] FECHA (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] AÑO
- [ ] CALLE
- [ ] CORREO ELECTRÓNICO
- [ ] DESCRIPCIÓN DEL DOCUMENTO
- [ ] FECHAS
- [ ] IMPORTE
- [ ] IMPORTE EN CIFRA
- [ ] LUGAR
- [ ] MES
- [ ] Nº
- [ ] Nº DE COLEGIADO/A
- [ ] NÚMERO
- [ ] SEDE
- [ ] TELÉFONO

## Normas que cita el formulario

- art. 24.1 LEC
- art. 399.1 LEC
- art. 439.6 LEC
- art. 85.1 LOPJ
- art. 52.1.7.º LEC
- art. 250.1.2.º LEC
- art. 253.1 LEC
- art. 251 LEC
- art. 437 LEC
- art. 5 Ley Orgánica 1/2025
- art. 3 k) Ley 12/2023
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

- Junto a «… la LO 1/2025. A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.R.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Demanda de juicio verbal de precario en el que el propietario de una vivienda por herencia de su padre, solicita del Tribunal que condene al demandado precarista a dejar libre y a su disposición la misma. Adaptada a la STC 26/2025, de 29 de enero; y a la reforma procesal de la LO 1/2025.

Notas al pie del formulario original:
(1) A la hora de su acreditación, todos los poderes deben estar inscritos en el Registro Electrónico de Apoderamientos Judiciales (REAJ). Se supone que, para su acreditación, basta con la consulta (de dicho Registro) automatizada orientada al dato. Algo que está a disposición de cualquier Letrado de la Administración de Justicia. Sin embargo, dado que el art. 24.2 LEC, configura la certificación de dicha inscripción como vía subsidiaria de acreditación, para el caso de que el sistema no permita aquella consulta automatizada; se señala en el modelo que se acompaña certificación electrónica. El sistema permite emitir dicha certificación para quien inscribe el poder.

(2) El art. 155.3 LEC permite fijar expresar varios domicilios del demandado (el que aparezca en el padrón municipal o conste oficialmente a estos efectos; el que aparezca en Registro oficial o en publicaciones de colegios profesionales, si se trata de empresas o personas colegiadas; donde desarrolle su actividad profesional o laboral no ocasional; si es empresa mercantil, el domicilio de cualquiera de sus administradores, gerentes, o apoderados; o, si es asociación que consta en registro oficial; el domicilio del presidente, miembro o gestor de la Junta correspondiente). Cuando se señalen varios, indicará el orden a seguir para la notificación, con vistas al éxito de la misma.

(3) El art. 155.3 LEC configura una obligación adicional del demandante, consistente en aportar cuantos datos sean de utilidad para localizar al demandado: número de identificación fiscal o de extranjeros, nº [Nº] de teléfono o de fax, dirección de correo electrónico, o similares.

(4) Ha desaparecido la exigencia de requerimiento al precarista con un mes de anticipación del art. 1565.3.º LECiv 1881.

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.R.C.

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], representación que acredito mediante escritura de poder otorgada a mi favor (existen tres posibilidades para otorgar el apoderamiento al Procurador de los Tribunales, conforme dispone el art. 24.1 LEC)

[OPCIONAL — opción en función de cómo se haya otorgado el poder]

[ELEGIR UNA OPCIÓN: Si el poder se otorga a través de la sede judicial electrónica / Si el poder se otorga mediante comparecencia apud acta / Si el poder se otorga ante Notario]

bajo la dirección letrada de D./Dña [NOMBRE Y APELLIDOS], abogado/a en ejercicio, con despacho profesional abierto en [LOCALIDAD], colegiado nº [Nº DE COLEGIADO/A] del Ilustre Colegio de la Abogacía de [LOCALIDAD], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que mediante el presente escrito y en nombre de mi mandante formulo DEMANDA DE JUICIO VERBAL DE PRECARIO contra D./Dña. [NOMBRE Y APELLIDOS] con domicilio, primero en [DOMICILIO]; y segundo, el domicilio laboral en [DOMICILIO]); con email [CORREO ELECTRÓNICO]; y con número de teléfono móvil [TELÉFONO]; y todo ello de conformidad con los siguientes hechos y fundamentos de derecho.

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa, e, incluso, en una eventual fase de ejecución por medios telemáticos, en términos del art. 399.1 II LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y nº [Nº] de teléfono:

HECHOS

PRIMERO.- Mi mandante es propietario de una vivienda sita en esta ciudad, calle [CALLE], número [NÚMERO], por herencia de su padre. Se acompaña el título de propiedad, escritura de operaciones particionales, como documento número [Nº DE DOCUMENTO].

SEGUNDO.- El demandado D./Dña.- ocupa dicha vivienda desde el mes de [MES] de [AÑO] cuando, manifestando que acudía a la misma, a la muerte de D./Dña. [NOMBRE Y APELLIDOS], quien era al parecer su tía segunda, por parte de madre, y a fin de retirar los muebles y enseres de la finada, la cual era inquilina en virtud de contrato verbal de hace más de treinta años, se viene negando a desalojar.

TERCERO.- Mi mandante requirió al demandado mediante burofax que fue recibido en fecha [FECHA], para que dejara libre y expedita la vivienda en cuestión, lo que se demuestra adjuntando el contenido y acuse de recibo, como documento número [Nº DE DOCUMENTO], ello sin perjuicio de remitirme, en su caso, a los archivos del departamento oportuno de Correos, sin que el demandado haya mostrado más disposición que responder que carece de otra vivienda para trasladarse y estar gestionando la búsqueda.

CUARTO.- A los efectos del art. 439.6 LEC se hace constar expresamente los siguientes hechos:

1.- Consta a esta parte que la vivienda sobre la que versa la demanda es la vivienda habitual de la demandada.

2.- No concurre en la parte demandante la condición de gran tenedora de vivienda de acuerdo con la definición contenida en la Ley 12/2023, de 24 de mayo, por el derecho a la vivienda, a cuya acreditación se adjuntar a la demanda certificación del Registro de la Propiedad en el que consten la relación de propiedades a nombre de la parte actora (documento nº [Nº DE DOCUMENTO]).

QUINTO.- La parte actora manifiesta que, previo a la presentación de la presente demanda, se han llevado a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad, y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria; incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, mi representado envío un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por el demandado por el mismo medio, rechazando el acuerdo/ habiendo sido solo posible un acuerdo parcial, viéndonos en la necesidad de acudir a la presente vía judicial, respecto a los extremos de la controversia en los que se mantiene la discrepancia.

Acompaño como documento nº [Nº DE DOCUMENTO], el requerimiento efectuado y como documento nº [Nº DE DOCUMENTO], la contestación del demandado.

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA.

Es competente el Tribunal de Instancia, Sección Civil, de los de esta población, que por turno de reparto corresponda, por ser el lugar de situación de la finca, conforme a al art. 85.1º LOPJ y art. 52.1.7.º LEC.

II.- PROCEDIMIENTO.

Es procedente el trámite del juicio verbal por razón de la materia, en razón del art. 250.1.2.º LEC.

III.- PARTES.

Está legitimado activamente para pretender la recuperación de la plena posesión de una finca cedida en precario, el titular en concepto de dueño, y pasivamente el que la disfruta sin pagar renta ni merced, y sin que detente un derecho a poseer, por lo que se acredita el título de dominio, se identifica el inmueble, se afirma la posesión del demandado, y se niega la contraprestación.

Tratándose de un juicio verbal por razón de la materia y no por razón de la cuantía, conforme a los arts. 23.1 y 31.1 LEC, es preceptiva la intervención de procurador de los tribunales y de abogado en ejercicio, ambos habilitados ante el Tribunal, estando identificados representante y director letrado en el encabezamiento de la demanda.

IV.- CUANTÍA DE LA DEMANDA.

La cuantía de la demanda, se justifica a los efectos del art. 253.1 LEC, en la cantidad de [IMPORTE] euros ([IMPORTE EN CIFRA] €), que es el precio corriente de mercado que fija el valor actual de la vivienda, conforme a la regla 2.ª del art. 251 LEC. A su justificación se presenta [DESCRIPCIÓN DEL DOCUMENTO] como documento número 3.

V.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC en relación con el art. 437 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VI.- EXIGENCIAS LEGALES DE LA ACCIÓN DE DESAHUCIO EJERCITADA

Tal y como se ha hecho constar en los hechos de la presente demanda, se cumplen con los requisitos exigidos en el art. 439.6 LEC. En primer lugar, mi mandante tiene constancia de que la vivienda arrendada constituye la vivienda habitual de la parte demandada.

En segundo lugar, la demandante no ostenta la condición de gran tenedora de viviendas, según el art. 3 k) de la Ley 12/2023, de 24 de mayo, por el derecho a la vivienda.

VII.- COSTAS.

Las costas procesales se han de imponer al demandado por principio del vencimiento del art. 394 LEC.

Por lo expuesto,

SUPLICO AL TRIBUNAL,

que teniendo por presentado este escrito con los documentos que lo acompañan y sus copias, tenga por interpuesta frente a D./Dña. [NOMBRE Y APELLIDOS] demanda de juicio verbal por precario, acuerde dar traslado al demandado para que comparezca y la conteste, y seguido el juicio por sus trámites, dicte sentencia por la que, estimando la demanda, condene al demandado a dejar libre y a disposición del actor la vivienda que viene ocupando en precario, con expresa imposición de las costas del juicio.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a
