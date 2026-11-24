---
name: contestacion-demanda-resolucion-subarriendo-falta-civ-0600
description: "Contestación a la demanda de resolución por subarriendo y falta de ocupación (vivienda, LAU 1994). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contestación a la demanda de resolución por subarriendo y falta de ocupación (vivienda, LAU 1994)

> Formulario **CIV-0600** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Modelo de contestación a la demanda por la que se solicita la resolución del contrato de arrendamiento de vivienda, fundada en el subarriendo y en la falta de ocupación de la vivienda arrendada ante la jubilación del arrendatario y la ocupación de la misma por su sobrina, que se aloja sin pago de cantidad alguna.

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contestación a la demanda de resolución por subarriendo y falta de ocupación (vivienda, LAU 1994)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contestación a la demanda de resolución por subarriendo y falta de ocupación (vivienda, LAU 1994)” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:contestacion-demanda-resolucion-subarriendo-falta-civ-0600`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] Nº DE DOCUMENTO (5 veces)
- [ ] IMPORTE (4 veces)
- [ ] FECHA (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] NOMBRE DE LA RESIDENCIA (2 veces)
- [ ] LUGAR
- [ ] NOMBRE DE LA FACULTAD
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] OTROS DATOS
- [ ] POSICIÓN SOBRE EL HECHO PRIMERO
- [ ] POSICIÓN SOBRE EL HECHO SEGUNDO

## Normas que cita el formulario

- art. 255 LEC
- art. 251 LEC
- art. 23 LEC
- art. 31 LEC
- art. 27.2.f LAU
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

### Avisos de actualización (0) — se aplican en el texto, nunca se copian en el documento

- Ninguno.

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

AL TRIBUNAL

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a. de los Tribunales, en nombre y representación de [NOMBRE DEL REPRESENTADO/A], según acredito mediante copia de la escritura de poder que acompaño para su unión a los autos por testimonio con devolución del original (o, en su caso, según apoderamiento otorgado «apud acta», que acompaño), dirigido por el Letrado abajo firmante D./Dña. [NOMBRE Y APELLIDOS], con despacho profesional en [LOCALIDAD], ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que mediante el presente escrito y dentro del término conferido, paso a contestar la demanda formulada de adverso, oponiéndome a la misma en base a los siguientes:

HECHOS

Esta parte niega los hechos alegados en la demanda, excepto los que expresamente se admitan en el presente escrito.

PRIMERO.- De conformidad con el hecho primero de contrario [POSICIÓN SOBRE EL HECHO PRIMERO]

SEGUNDO.- De conformidad con el hecho segundo de contrario [POSICIÓN SOBRE EL HECHO SEGUNDO]

TERCERO.- Se niega expresamente el correlativo de la demanda, puesto que la persona que ha podido ser vista en la vivienda, y que probablemente no conoce el actor ni la vecindad, es una sobrina de mi mandante que ha venido desde su pueblo a estudiar a la Facultad de [NOMBRE DE LA FACULTAD], de la Universidad de [LOCALIDAD], y que se aloja sin pago de cantidad alguna, por relación de parentesco y amistad.

Se adjunta certificado de empadronamiento de D./Dña. [NOMBRE Y APELLIDOS], en [LOCALIDAD], y de matriculación universitaria, como documentos nos. y [Nº DE DOCUMENTO].

CUARTO.- Se niega igualmente el hecho cuarto de los de la demanda [OTROS DATOS], puesto que lo ocurrido en el espacio de tiempo que va desde el [FECHA] hasta el [FECHA], ha sido que por el ingreso hospitalario de la esposa de mi poderdante en la Residencia de [NOMBRE DE LA RESIDENCIA], a causa de una grave enfermedad, para atenderla debidamente, aquél ha pasado a residir temporalmente en casa de su cuñada D./Dña. [NOMBRE Y APELLIDOS]

Se acompaña certificado médico de la residencia [NOMBRE DE LA RESIDENCIA], a acreditativo del ingreso referido (documento nº [Nº DE DOCUMENTO]).

QUINTO.- Se asume que no han fructificado gestiones amistosas que dice el hecho quinto correlativo, si por tales se entienden que mi mandante le entregara las llaves de la vivienda a la propiedad, lo que se le pidió en el requerimiento del documento nº [Nº DE DOCUMENTO] de la demanda, que se envió al provisional lugar en que se hallaba, al cuidado de su esposa enferma.

FUNDAMENTOS DE DERECHO

I, II.-

Conforme esta parte con la competencia y el tipo de procedimiento señalados por el actor en el correlativo de la demanda.

III, IV.-

De conformidad con los expuestos de contrario, acerca de la capacidad de las partes y su legitimación.

V.- A los efectos del art. 255 LEC, se impugna para decidirse en el acto de la audiencia previa la cuantía de la demanda fijada por el demandante.

La cuantía litigiosa no es de [IMPORTE] euros ( €), ya que de conformidad con lo establecido en la regla 9.ª del art. 251 LEC, en los juicios sobre arrendamientos de bienes, salvo cuando tengan por objeto reclamaciones de las rentas o cantidades debidas, la cuantía de la demanda será el importe de una anualidad de renta, que, en el caso presente, es de [IMPORTE] euros ( €), y no como quiere el demandante, utilizando la regla 3.ª.5.º del art. 251 LEC, el importe del valor catastral del inmueble, notablemente superior.

Se acompaña como documento nº [Nº DE DOCUMENTO] el contrato de arrendamiento en el que se estipuló una renta anual de [IMPORTE] euros ( €) pagaderos en doce mensualidades de ( €) euros cada una de ellas, y como documento nº [Nº DE DOCUMENTO] justificante del importe de la actualización anual, de lo que resulta que la renta mensual vigente al tiempo de interposición de la demanda es de [IMPORTE] euros ( €).

VI.- POSTULACIÓN Y DEFENSA

La parte está representada por el Procurador/a. [NOMBRE Y APELLIDOS], legalmente habilitado en el partido, según el art. 23 LEC,y defendida por el Letrado que consta en el encabezamiento (art. 31 LEC).

VII.- FUNDAMENTO LEGAL DE LA OPOSICIÓN

Uno de los fundamentos de la demanda está en el art. 27.2 c) de la vigente Ley de Arrendamientos Urbanos, LAU 1994, en cuanto que el arrendador puede resolver de pleno derecho el contrato de arrendamiento cuando se produce el subarriendo o la cesión inconsentida, y en el presente caso el arrendatario ciertamente no ha solicitado el consentimiento del arrendador a que se refiere el art. 8.2 del mismo Texto.

Pero el caso es que el subarriendo o cesión de contrato no se produce por el dato de que una persona, pariente del arrendatario y además sin vida independiente, sin pago de renta ni merced, se acoja en la vivienda, y que casualmente lo haga en el tiempo en que, de forma provisional, urgente y por desdicha personal, el arrendatario no ha podido permanecer en el domicilio que es habitual.

El segundo fundamento radica en el art. 27.2.f) LAU 1994, al señalar como causa de resolución de pleno derecho del arrendamiento cuando la vivienda deja de estar destinada a satisfacer la necesidad primaria y permanente de vivienda del arrendatario, lo que en definitiva es aban

D./Dña. [NOMBRE Y APELLIDOS] ar el destino permanente del tipo de contrato según art. 2, pero es evidente que la enfermedad grave, que supone cuidados en régimen interno por establecimientos sanitarios, con acompañamiento de familiares, es justa causa para que se pierda momentáneamente la satisfacción inmediata del destino domiciliario, lo que la jurisprudencia siempre consideró justa causa en términos de la denegación de prórroga forzosa de inquilinatos bajo imperio de LAU 1964, en razón de la causa 3ª del art. 62 de dicha ley locativa derogada.

VIII.- COSTAS

Las costas deberán serle impuestas, de conformidad con el artículo 394 LEC, a la parte actora, de ser desestimada su demanda.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito con los documentos y copias que le acompañan, admita uno y otras, y teniendo por contestada en tiempo y forma la demanda, y opuesta esta parte a la misma, previos los trámites que corresponden, se dicte en su día sentencia por la que se desestime la demanda presentada, absolviendo libremente de la misma al demandado, con expresa imposición de costas a la parte actora.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a./a

========================================================================
