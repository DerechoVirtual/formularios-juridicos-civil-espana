---
name: demanda-reduccion-exoneracion-renta-finca-rustica-civ-0602
description: "Demanda de reducción o exoneración de renta de finca rústica (arrendamiento sujeto a la LAR 1980). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de reducción o exoneración de renta de finca rústica (arrendamiento sujeto a la LAR 1980)

> Formulario **CIV-0602** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Modelo de demanda de juicio ordinario, sobre exoneración o reducción de renta de finca rústica conforme al artículo 44 LAR de la Ley 83/1980, de 31 de diciembre, de Arrendamientos Rústicos, derogada por la vigente Ley 49/2003, pero que resulta aplicable al contrato vigente.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de reducción o exoneración de renta de finca rústica (arrendamiento sujeto a la LAR 1980)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de reducción o exoneración de renta de finca rústica (arrendamiento sujeto a la LAR 1980)” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:demanda-reduccion-exoneracion-renta-finca-rustica-civ-0602`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] FECHA (5 veces)
- [ ] NÚMERO (5 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] CALLE (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] COLEGIO
- [ ] FECHAS
- [ ] IMPORTE EN CIFRA
- [ ] LITROS POR METRO CUADRADO
- [ ] LUGAR
- [ ] MES
- [ ] NOMBRE DE LA FINCA
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº
- [ ] PLAZO
- [ ] TIPO DE CULTIVO

## Normas que cita el formulario

- art. 85 LOPJ
- art. 45 LEC
- art. 52.1.7 LEC
- art. 249.1.6 LEC
- art. 6.1.1 LEC
- art. 7.1 LEC
- art. 10 LEC
- art. 253.1 LEC
- art. 251 LEC
- art. 23 LEC
- art. 399 LEC
- art. 399.3 LEC
- art. 5 Ley Orgánica 1/2025
- art. 44 Ley 83/1980
- art. 1575 CC
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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE Q.P.T.R.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE Q.P.T.R.C.

D./Dña. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en nombre y representación de [NOMBRE DEL REPRESENTADO/A], con domicilio en [LOCALIDAD], según acredito con la copia de escritura de poder que he aceptado y acompaño, con ruego de que se devuelva previo testimonio en autos, con asistencia del Letrado suscrito D./Dña. [NOMBRE Y APELLIDOS], abogado ejerciente n.º [NÚMERO] del Iltre. Colegio de Abogados de [COLEGIO], que tiene abierto despacho en [LOCALIDAD], calle [CALLE], ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que por medio del presente escrito deduzco demanda de juicio ordinario, sobre exoneración (o reducción) de renta de finca rústica, contra D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con D.N.I. n.º [NÚMERO], y con domicilio en [LOCALIDAD], calle [CALLE], basándola en los siguientes hechos y fundamentos de derecho:

HECHOS

PRIMERO.- Mi mandante es arrendatario de la finca rústica sita en el término municipal de [LOCALIDAD], y conocida como ‘ [NOMBRE DE LA FINCA] ‘, con una extensión superficial de [Nº] hectáreas, propiedad del demandado D./Dña. [NOMBRE Y APELLIDOS], como consta en el contrato de arrendamiento celebrado con fecha [FECHA], por un plazo de duración de [PLAZO] y por una renta de [IMPORTE].

Se acompaña dicho contrato como documento n.º [NÚMERO].

SEGUNDO.- Con motivo de un fuerte temporal ocurrido el día [FECHA] de [MES] de este año, se produjeron inundaciones en la finca, calculándose por los expertos en una cantidad aproximada a los [LITROS POR METRO CUADRADO] litros por metro cuadrado, dando lugar a que se perdieran totalmente todas las cosechas de ese año agrícola, lo que hace imposible que mi representado pueda satisfacer la renta pactada, no obstante lo cual el arrendador, hoy demandado, insiste en que se le haga efectiva la misma.

Se acompaña certificación acreditativa de este extremo como documento n.º [NÚMERO].

TERCERO.- Con fecha [FECHA], dentro del plazo de treinta días que establece por la Ley, se notificó notarialmente a D./Dña. [NOMBRE Y APELLIDOS] la pérdida total de las cosechas por las causas señaladas en el ordinal segundo de los Hechos de esta demanda.

Para acreditarlo acompaño como documento n.º [NÚMERO], copia de la notificación fehaciente efectuada por el Notario de esta localidad D./Dña. [NOMBRE Y APELLIDOS].

CUARTO.- La parte actora manifiesta que, previo a la presentación de la presente demanda, se han llevaron a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad, y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria; incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, mi representado envío un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por el demandado por el mismo medio, rechazando el acuerdo/ habiendo sido solo posible un acuerdo parcial, viéndonos en la necesidad de acudir a la presente vía judicial, respecto a los extremos de la controversia en los que se mantiene la discrepancia.

Acompaño como documento nº [Nº DE DOCUMENTO], el requerimiento efectuado y como documento nº [Nº DE DOCUMENTO], la contestación del demandado.

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA.

Sin duda de la competencia genérica del orden civil de la jurisdicción, la competencia específica atribuye el conocimiento de este asunto al Tribunal a quien tengo el honor de dirigirme por ser la Sección Civil del Tribunal de Instancia (art. 85 LOPJ y art. 45 LEC), la que detenta competencia objetiva, y la funcional de la instancia, y que ostenta competencia territorial, por cuanto en los juicios sobre arrendamiento de inmuebles es competente el tribunal del lugar en que esté sita la finca, según el art. 52.1.7º LEC.

II.- PROCEDIMIENTO.

La demanda deberá sustanciarse por las normas del juicio ordinario del Título II del Libro II LEC, a tenor de lo expresamente prevenido en el art. 249.1.6º LEC, al tener por objeto pretensiones relativas a contrato de arrendamiento de finca rústica, sin que opere la exclusión material de la acción de desahucio o de mera reclamación de cantidad.

III.- CAPACIDAD.

Demandante y demandado, personas físicas, tienen capacidad para ser parte (art. 6.1.1º LEC), titular de facultades y cargas del proceso, y asimismo plena capacidad procesal, al ser mayores de edad, sin limitación de ejercicio válido de derechos civiles, o para comparecer en juicio, en términos del art. 7.1 LEC, pretendiendo el actor y siendo pretendido el demandado, en sus respectivos nombres y derechos.

IV.- LEGITIMACIÓN.

La legitimación activa corresponde al demandante por ser el arrendatario de la finca, y la pasiva la tiene el demandado en cuanto obligado a lo que se pide como arrendador de la finca, por haber concertado el contrato. (arts. 10 LEC).

V.- CUANTÍA.

Conforme al art. 253.1 LEC cifro la cuantía de la presente demanda en [IMPORTE] euros ([IMPORTE EN CIFRA] €), importe de una anualidad de renta, según resulta de la regla 9ª del art. 251 LEC.

VI.- POSTULACIÓN Y DEFENSA.

Conforme a los arts. 23 y 31 LEC se formula esta demanda por medio de Procurador con poder notarial para pleitos, y con dirección y firma de Letrado habilitado. Asimismo se cumplen los requisitos formales del art. 399 LEC.

VII. CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por el art. 264.4º y art. 399.3 de la LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VIII.- FONDO DEL ASUNTO.

VIII.1.- Es de aplicación el artículo 44 de la Ley 83/1980, de 31 de diciembre, de Arrendamientos Rústicos, derogada por la vigente Ley 49/2003, pero que resulta aplicable al contrato vigente, puesto que era la del momento de su celebración (Disposición transitoria 1ª LAR 49/2003, de 26 de noviembre) a cuyo tenor ‘procederá la reducción e incluso la exoneración de la renta cuando, por caso fortuito o fuerza mayor y tratándose de riesgos ordinariamente no asegurables, se perdiere antes de terminar todas las operaciones de recolección más de la mitad de los productos que ordinariamente produzca la finca. La renta se reducirá en igual porcentaje en que hayan quedado reducidos los productos de la finca’.

VIII.2.- El artículo 1575 CCiv. establece que el arrendatario tendrá derecho a la rebaja de la renta en caso de pérdida de más de la mitad de frutos por casos fortuitos extraordinarios e imprevistos, entendiéndose por caso fortuito extraordinario, entre otros supuestos, la inundación insólita.

VIII.3.- Se ha cumplido también el requisito que exige el artículo 45 LAR 1980: ‘Para que el arrendatario pueda ejercitar el derecho de reducción o exoneración es necesario que notifique fehacientemente el siniestro al arrendador en el plazo de treinta días desde que se produzca, y que actúe con diligencia a fin de conseguir, en su caso, la efectividad de cualquier indemnización a que pudiera haber derecho’.

IX.- COSTAS.

Conforme al art. 394 LEC, las costas procesales han de imponerse a la parte demandada, con la estimación de la demanda.

En virtud de lo anteriormente expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito con sus copias, se digne admitir uno y otras, formar juicio ordinario especial arrendaticio, en el que se tenga a quien comparece a través de mandatario procesal como parte legítima, entendiéndose con el dicho mandatario todas las actuaciones, y en mérito a lo alegado, seguido que sea todo el pertinente procedimiento, se venga a dictar en su día definitiva Sentencia por la que se exonere al arrendatario de la obligación de satisfacer la renta correspondiente a la cosecha de este año de [TIPO DE CULTIVO], condenando al demandado a pasar por esta declaración, con imposición de las costas.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
