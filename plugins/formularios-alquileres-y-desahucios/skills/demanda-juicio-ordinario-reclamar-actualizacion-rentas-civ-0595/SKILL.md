---
name: demanda-juicio-ordinario-reclamar-actualizacion-rentas-civ-0595
description: "Demanda de juicio ordinario para reclamar la actualización de rentas, con acumulación subjetiva. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio ordinario para reclamar la actualización de rentas, con acumulación subjetiva

> Formulario **CIV-0595** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Modelo de demanda al Tribunal de Instancia que por turno corresponda, de Juicio Ordinario en reclamación relativa a contrato de arrendamiento inmobiliario contra los arrendatarios. Se ejercita por los arrendadores la pretensión de actualización de rentas debidas en contrato de arrendamiento de inmueble con destino a vivienda de la legislación especial locativa urbana .

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio ordinario para reclamar la actualización de rentas, con acumulación subjetiva» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio ordinario para reclamar la actualización de rentas, con acumulación subjetiva” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:demanda-juicio-ordinario-reclamar-actualizacion-rentas-civ-0595`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (16 veces)
- [ ] Nº DE DOCUMENTO (7 veces)
- [ ] NÚMERO (4 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] CALLE (2 veces)
- [ ] FECHA (2 veces)
- [ ] MES (2 veces)
- [ ] AÑO
- [ ] DIRECCIÓN
- [ ] DOMICILIO
- [ ] FECHAS
- [ ] PISO
- [ ] SEDE

## Normas que cita el formulario

- art. 9.2 LOPJ
- art. 45 LEC
- art. 68 LEC
- art. 52.7 LEC
- art. 5 Ley Orgánica 1/2025
- art. 1254 Código Civil
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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…objetiva y funcional (art. 45 LEC) la Sección Civil del Tribunal de Instancia de»: Un solo TI por partido judicial (art. 84.1 LOPJ): sobra «de los de». Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.C.

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a. de los Tribunales, que actúa en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], con D.N.I. nº [NÚMERO], D./Dña. [NOMBRE Y APELLIDOS], con D.N.I. nº [NÚMERO], y D./Dña. [NOMBRE Y APELLIDOS], con D.N.I. nº [NÚMERO], con domicilio en [LOCALIDAD], conforme acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], siendo dirigido por el Letrado ejerciente D./Dña. [NOMBRE Y APELLIDOS], con despacho profesional abierto en esta localidad, calle [CALLE], ante ese Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que por medio del presente escrito vengo a formular demanda de Juicio Ordinario en reclamación relativa a contrato de arrendamiento inmobiliario, contra D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS], domiciliados en [DOMICILIO], c./ [DIRECCIÓN] nº [NÚMERO],

Se ejercita pretensión de actualización de rentas debidas en contrato de arrendamiento de inmueble con destino a vivienda de la legislación especial locativa urbana, con base en los siguientes:

HECHOS

PRIMERO.- Mis representados son dueños proindiviso de la vivienda sita en el piso [PISO] de [LOCALIDAD], calle [CALLE] habiendo contratado verbalmente hace unos veinte años el arrendamiento especial urbano de tal finca para uso de vivienda, con D./Dña. [NOMBRE Y APELLIDOS], que actualmente parece haber subrogado a D./Dña. [NOMBRE Y APELLIDOS], con la que convive o convivía.

Se adjunta como Documento nº [Nº DE DOCUMENTO] escritura de manifestación y aceptación de herencia que es el título de dominio, y como Documento nos. y [Nº DE DOCUMENTO] recibos de pago de renta correspondientes a las mensualidades de [MES] y [MES] de [AÑO], el último de los que pagó D./Dña. [NOMBRE Y APELLIDOS] y el primero de los que paga D./Dña. [NOMBRE Y APELLIDOS]

SEGUNDO.- Por mi mandantes se requirió a los demandados mediante carta certificada con acuse de recibo, al cumplirse una anualidad de vigencia del contrato, comunicándoles el importe de la actualización, acompañando certificación del Instituto Nacional de Estadística expresiva de los índices que determinan la cantidad notificada.

En ella se ve que el porcentaje que resulta de lo dispuesto en la aplicación de las reglas de la Disposición Transitoria Segunda de la LAU 1994, es mayor que la renta que viene pagándose incrementada a las cantidades asimiladas a la renta.

Se acompaña como Documento nº [Nº DE DOCUMENTO] la carta, en la que se se expresa el certificado del INE, junto con el acuse de recibo firmado por D./Dña. [NOMBRE Y APELLIDOS]

TERCERO.- No obstante ello, girados los correspondientes recibos, el demandado se ha negado a pagar el aumento, siendo infructuosas las gestiones realizadas amistosamente para conseguirlo.

Se adjunta como Documento nº [Nº DE DOCUMENTO] carta remitida a los codemandados por el abogado suscrito en fecha [FECHA], en la que se insiste en el deber de abono de la renta actualizada con incremento, y se anuncia la interposición de esta demanda.

CUARTO.- La parte actora manifiesta que, previo a la presentación de la presente demanda, se han llevaron a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad, y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria; incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, mi representado envío un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por el demandado por el mismo medio, rechazando el acuerdo/ habiendo sido solo posible un acuerdo parcial, viéndonos en la necesidad de acudir a la presente vía judicial, respecto a los extremos de la controversia en los que se mantiene la discrepancia.

Acompaño como documento nº [Nº DE DOCUMENTO], el requerimiento efectuado y como documento nº [Nº DE DOCUMENTO], la contestación del demandado.

A los anteriores hechos son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA.

Sobre materia de la competencia genérica del orden civil de la jurisdicción (art. 9.2 LOPJ), tiene la competencia objetiva y funcional (art. 45 LEC) la Sección Civil del Tribunal de Instancia de esta población, que por turno de reparto corresponda (art. 68 LEC), y la territorial, puesto que el inmueble arrendado se halla sito en la población de [LOCALIDAD] (art. 52.7º LEC).

II.- PROCEDIMIENTO.

El juicio ordinario a que se refieren los arts. 248, 249.1.6º y 399 a 436 LEC.

III.- LEGITIMACIÓN.

La legitimación activa corresponde a los demandantes por ser los propietarios de la vivienda, y la pasiva la tienen los demandados en cuanto obligados solidariamente a lo que se pide como arrendatarios de la finca, el uno por haber concertado el contrato y la otra por ser quien abona los recibos de la renta desde hace años, conviviente con el primero.

IV. CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 de la LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

V.- FONDO DEL ASUNTO.

Citamos aquí la Disposición Transitoria Segunda, apartado D) de la Ley de Arrendamientos Urbanos de 1994, y los arts. 1254 y 1258 del Código Civil, en cuanto determinan que lo contratos obligan también a todas las consecuencias que, según su naturaleza, sean conformes a la buena fe, al uso y a la Ley.

Los demandados no han hecho uso de la facultad que le otorga el apartado 6.º de la Disposición Transitoria 2ª D) de la citada Ley en el plazo de treinta días naturales siguientes a la recepción del requerimiento que se les lanzó por carta, y tampoco se hallan incursos en el supuesto de la regla 7ª de dicha disposición.

VI.- COSTAS.

Conforme al art. 394 LEC, las costas procesales han de imponerse a la parte demandada, con la estimación de la demanda.

En virtud de lo anteriormente expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito con sus copias, se digne admitir uno y otras, formar juicio ordinario especial arrendaticio, en el que se tenga a quien comparece a través de mandatario procesal como parte legítima, entendiéndose con el dicho mandatario todas las actuaciones, y en mérito a lo alegado, seguido que sea todo el pertinente procedimiento, se venga a dictar en su día definitiva Sentencia que declare la renta debida del contrato de arrendamiento de la vivienda descrita en el cuerpo de la demanda actualizada para el año, en la cantidad mensual deeuros (€), y en su consecuencia, condene a que D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS] paguen conjunta y solidariamente a los actores las cantidades especificadas en el cuerpo de la demanda, incrementada en lo que represente el interés por mora en el pago, con todo lo demás que sea procedente en Justicia de hacerse en

OTROSÍ DIGO que, para el supuesto de que el demandado D./Dña. [NOMBRE Y APELLIDOS] se afirme que no convive con D./Dña. [NOMBRE Y APELLIDOS] en el domicilio indicado, que es el de la vivienda arrendada, y como se desconoce el que pudiera tener, hallándose en paradero desconocido, a menos que la codemandada facilite noticia de sus señas, interesa que, en el caso, se le notifique la demanda por medio de edictos; por lo que

SUPLICO AL TRIBUNAL se sirva acordar el emplazamiento de la parte demandada por vía edictal, el cual contendrá el texto íntegro de la demanda, librando y entregando a esta parte los correspondientes despachos para su diligenciamiento.

Es Justicia que reitero en lugar y fecha ‘ut supra’.

Firma el Abogado/a	Firma el Procurador/a

========================================================================
