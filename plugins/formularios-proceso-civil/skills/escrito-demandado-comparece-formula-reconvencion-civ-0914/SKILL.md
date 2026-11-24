---
name: escrito-demandado-comparece-formula-reconvencion-civ-0914
description: "Escrito del demandado que comparece y formula reconvención en juicio verbal. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito del demandado que comparece y formula reconvención en juicio verbal

> Formulario **CIV-0914** del plugin **Proceso civil: demandas, contestaciones, prueba y vista** (`formularios-proceso-civil`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito del demandado que comparece y formula reconvención en juicio verbal» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito del demandado que comparece y formula reconvención en juicio verbal” para mi caso». También puedes invocarla directamente con `/formularios-proceso-civil:escrito-demandado-comparece-formula-reconvencion-civ-0914`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-proceso-civil:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso civil: demandas, contestaciones, prueba y vista) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (5 veces)
- [ ] IMPORTE (5 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] SUPERFICIE (2 veces)
- [ ] LUGAR Y FECHA
- [ ] NOMBRE DE LA FINCA
- [ ] Nº DE DOCUMENTO
- [ ] NÚMERO
- [ ] SEDE

## Normas que cita el formulario

- art. 1502 Código Civil
- art. 250.2 LEC
- art. 394 LEC
- art. 438.3 LEC
- art. 1124 Código Civil
- art. 438.2 LEC
- art. 1101 Código Civil
- art. 7.2 Ley 10/2012

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

- Junto a «…Juicio verbal nº [NÚMERO] A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

Juicio verbal nº [NÚMERO]

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

Don [NOMBRE Y APELLIDOS] Procurador de los Tribunales, en nombre y representación de Don [NOMBRE Y APELLIDOS], según acredito por certificación del registro electrónico de apoderamientos judiciales que acompaño (o mediante designación apud acta ante el Letrado de la Administración de Justicia de [LOCALIDAD] bajo la dirección letrada de D/Dª [NOMBRE Y APELLIDOS], Abogado/a del Iltre. Colegio de [LOCALIDAD], ante el Tribunal comparezco y como mejor en derecho proceda DIGO:

Que habiéndose dado traslado a esta parte de la demanda de juicio verbal formulada por D en reclamación de [IMPORTE] euros en concepto del pago del precio del contrato de compraventa celebrado el día [FECHA], siguiendo instrucciones de mi poderdante por medio del presente escrito y en nombre del mismo formulo en tiempo y forma CONTESTACIÓN A LA DEMANDA, formulando a la vez RECONVENCIÓN contra el demandante D. [NOMBRE Y APELLIDOS], en base a:

I. CONTESTACIÓN A LA DEMANDA

HECHOS

PRIMERO.- Se niegan todos los hechos expuestos en la demanda a excepción de los que se vean aceptados en la presente contestación.

SEGUNDO.- La acción que se ejercita en este proceso es una acción de reclamación de cantidad en virtud del contrato privado de compraventa aportado junto a la demanda, de fecha [FECHA], en el que el actor enajenaba a mi principal la siguiente finca rústica «una parcela de terreno de secano, denominada " [NOMBRE DE LA FINCA] ", sita en la localidad de [LOCALIDAD], de la siguiente extensión: ». Dicha finca figuraba inscrita en el Registro de la Propiedad de [LOCALIDAD], tal como se acredita mediante certificación registral, que acompaño como doc. nº 1 del índice electrónico, de la que se desprende que la finca aparece en el Registro como una única finca.

TERCERO.- Mi mandante satisfizo mediante tres entregas las tres cuartas partes del precio de la venta, fijada en [IMPORTE] euros, es decir, [IMPORTE] euros.

El citado contrato fue elevado a escritura pública ante el Notario de [LOCALIDAD], en fecha [FECHA] la cual acompaño. En ella se mencionaba que el vendedor había efectuado la entrega de la posesión de la finca (acompaño como doc. nº 2 del índice electrónico la citada escritura).

Por tanto, no se ha satisfecho la cantidad de… euros como parte del precio, lo cual tiene su fundamento en que concurre causa de resolución del contrato como se expone a continuación en la acción reconvencional que se ejercita, y en este sentido mi representado hizo uso del derecho que le otorga el art. 1502 del Código Civil.

FUNDAMENTOS DE DERECHO

PRIMERO COMPETENCIA Y PROCEDIMIENTO: Se acepta la tramitación de la causa por los tramites del juicio verbal con fundamento en el art 250.2 LEC y asumiendo las alegaciones en este sentido vertidas en el escrito de demanda, al ser el valor de la finca inferior a 15.000 euros.

SEGUNDO FONDO DE LA RECLAMACIÓN: Se estima improcedente el acce-der a la reclamación por concurrir causa de resolución imputable al actor como se expone a continuación en la demanda reconvencional y estar amparada la conducta de mi representado en el art. 1502 del Código Civil.

TERCERO COSTAS: En materia de costas el art 394 LEC.

En base a lo anterior,

SUPLICO AL TRIBUNAL: que tenga por presentado este escrito con justificante de traslado, teniendo a esta parte por personada en las presentes actuaciones entendiéndose conmigo las siguientes diligencias y por contestada a la demanda interpuesta contra mi principal y tras la pertinente tramitación se sirva dictar sentencia por la que se desestime la demanda presentada contra mi principal con imposición de costas al demandante.

II. RECONVENCIÓN

Por medio del presente escrito se formula reconvención, amparada en lo dispuesto en el art. 438.3 de la LEC, con fundamento en los siguientes.

HECHOS

PRIMERO El pasado [FECHA] mi principal recibió un requerimiento de Don [NOMBRE Y APELLIDOS], que no es parte en este proceso, instándole a que desalojara una porción de la citada finca objeto de la compraventa antes descrita, de una extensión de [SUPERFICIE], aduciendo que esta porción le había sido enajenada por el demandado mediante un contrato privado de compraventa, elevado a escritura pública en fecha [FECHA], el cual me fue entregado por copia (acompaño dicha copia junto al presente escrito, como doc. nº 3 del índice electrónico).

SEGUNDO Resulta claro que mi mandante al consentir sobre el objeto y precio de la compraventa, elementos esenciales de dicho contrato, se refería a la totalidad de la finca de extensión « [SUPERFICIE] », y no a una porción de la misma, sensiblemente inferior, que fue enajenada con mala fe por el propio actor. Por otra parte, mi mandante no puede ejercitar la acción de saneamiento por evicción, puesto que aún no ha sido privado de la posesión de la finca, tal como pone de relieve la STS, de 10 de diciembre de 1996, rec. 379/1993.

TERCERO En consecuencia, procede declarar resuelto el contrato conforme a lo que dispone el art. 1124 del Código Civil y preceptos concordantes, con la obligación del actor de restituir el precio con sus intereses.

FUNDAMENTOS DE DERECHO

PRIMERO REQUISITOS DE LA RECONVENCIÓN La reconvención que se formula reúne los requisitos exigidos en el art. 438.2 LEC; ya que con arreglo al mismo precepto, solo es admisible la reconvención cuando no sea improcedente el juicio verbal y cuando exista conexión entre las pretensiones de la reconvención y las que sean objeto de la demanda principal, requisitos que concurren en este caso, siendo que el valor de la finca enajenada no supera la cantidad de seis mil euros.

SEGUNDO FONDO DE LA RECLAMACIÓN: Es de aplicación lo dispuesto en el art. 1101, 1124 y concordantes del Código Civil en relación con los arts. 1461 y siguientes del citado texto legal.

TERCERO COSTAS: En materia de costas, es de aplicación el art 394 LEC.

En base a lo anterior,

SUPLICO AL TRIBUNAL se tenga por presentado este escrito y documentos, con justificante de traslado, por formulada demanda reconvencional contra el demandante FD, se sirva admitirla y se dicte sentencia por la que se estime la reconvención formulada y, en consecuencia, se declare resuelto el contrato de compraventa cuyo cumplimiento se exige en este proceso y se condene al demandado a abonar a mi mandante la cantidad de [IMPORTE] euros ya satisfecha, más los intereses legales que procedan y que prudencialmente se fijan en [IMPORTE] euros, ofreciéndose mi representado a reintegrar al actor en la posesión de la finca objeto de este proceso, con expresa condena en costas al demandante.

OTROSÍ DIGO I: que esta parte interesa la celebración de vista al existir controversia sobre los hechos y ser necesaria la práctica de prueba para la resolución de este proceso.

En virtud de lo anterior,

SUPLICO AL TRIBUNAL tenga por efectuadas las anteriores manifestaciones y acuerde la celebración de vista.

OTROSÍ II.-Que estando la presente demanda sujeta al abono de la tasa por el ejercicio de la potestad jurisdiccional fijada por la Ley 10/2012, de 20 de noviembre, modificada por Real Decreto Ley 3/2013, de 22 de febrero, y Ley 25/2015, de 28 julio, y por Orden HAP/861/2015, de 7 de mayo, siendo mi representada persona jurídica no exenta, se acompaña a la presente demanda como documento nº [Nº DE DOCUMENTO] la correspondiente autoliquidación con el ejemplar para la Administración de Justicia debidamente validado y en el que consta el pago de la cantidad de 150 euros correspondiente a la cuota fija, sin que se incluya la cuota variable prevista en el artículo 7.2 de la Ley 10/2012 al haber sido declarado inconstitucional y nulo por la STC 140/2016, de 21 de julio.

En virtud de lo anterior

SUPLICO AL TRIBUNAL que tenga por hecha la anterior manifestación a los efectos pertinentes y por acompañado el documento justificativo del abono de la tasa.

En [LUGAR Y FECHA].

========================================================================
