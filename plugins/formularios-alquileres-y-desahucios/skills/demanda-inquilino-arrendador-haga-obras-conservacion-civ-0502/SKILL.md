---
name: demanda-inquilino-arrendador-haga-obras-conservacion-civ-0502
description: "Demanda del inquilino para que el arrendador haga las obras de conservación de la vivienda (LAU 94). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda del inquilino para que el arrendador haga las obras de conservación de la vivienda (LAU 94)

> Formulario **CIV-0502** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Modelo de demanda de juicio declarativo ordinario exigiendo al arrendador la realización de reparaciones necesarias en la vivienda arrendada, puesto que este está obligado a realizar, sin derecho a elevar por ello la renta, todas las reparaciones que fuesen necesarias para conservar la vivienda en las condiciones de habitabilidad para servir al uso convenido.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda del inquilino para que el arrendador haga las obras de conservación de la vivienda (LAU 94)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda del inquilino para que el arrendador haga las obras de conservación de la vivienda (LAU 94)” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:demanda-inquilino-arrendador-haga-obras-conservacion-civ-0502`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NÚMERO (5 veces)
- [ ] Nº DE DOCUMENTO (4 veces)
- [ ] FECHA (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] CALLE (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] FECHAS
- [ ] IMPORTE
- [ ] LUGAR
- [ ] PARTE DEMANDADA
- [ ] PUERTA
- [ ] SEDE

## Normas que cita el formulario

- art. 21.1 LOPJ
- art. 36.1 LEC
- art. 85.1 LOPJ
- art. 45 LEC
- art. 52.1.7.º LEC
- art. 249.1.6.º LEC
- art. 6.1.1.º LEC
- art. 7 LEC
- art. 253.1 LEC
- art. 251 LEC
- art. 23 LEC
- art. 5 Ley Orgánica 1/2025
- art. 21.1 LAU
- art. 1.554.2.º CC
- art. 27.1 LAU
- art. 21.3 LAU
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

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a. de los Tribunales, en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], con asistencia del Letrado suscrito D/Dña. [NOMBRE Y APELLIDOS], que tiene abierto despacho en [LOCALIDAD],calle [CALLE], ante el Tribunal comparezco y como mejor proceda en derecho, DIGO:

Que mediante el presente escrito y en nombre de mi mandante formulo demanda de juicio declarativo ordinario contra [PARTE DEMANDADA], a fin de que, previos los trámites correspondientes, se dicte sentencia estimatoria de los pedimentos del suplico, en base a los siguientes:

HECHOS

PRIMERO.- Por demandante y demandado se suscribió el contrato de arrendamiento sobre la vivienda sita en esta ciudad, calle [CALLE], número [NÚMERO], puerta [PUERTA], a la que se refiere la presente demanda, y que el demandante ocupa desde entonces en concepto de inquilino.

Se acompaña dicho contrato como documento n.º [NÚMERO], y como documento n.º [NÚMERO] justificante del importe actualizado de la renta.

SEGUNDO.- Después de numerosos intentos de solución extrajudicial, mi mandante requirió al propietario y arrendador de dicha vivienda en fecha [FECHA] a fin de que procediera a la reparación de los elementos fundamentales de dicha vivienda que se relacionan:

Nos remitimos al contenido del requerimiento notarial que acompañamos como documento n.º [NÚMERO], y como documentos n.º [NÚMERO] a [Nº DE DOCUMENTO], las fotografías acreditativas del estado en que se encuentra la vivienda.

TERCERO.- Al día de la fecha el arrendador no ha efectuado las reparaciones necesarias para conservar la vivienda en las condiciones de habitabilidad para el uso convenido, no ha enviado técnicos que comprobaran las necesidades de reparación, ni ha posibilitado solución alguna, por lo que se ha forzado a acudir a los tribunales.

A los anteriores hechos son de aplicación los siguientes:

CUARTO.- La parte actora manifiesta que, previo a la presentación de la presente demanda, se han llevaron a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad, y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria; incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, mi representado envío un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por el demandado por el mismo medio, rechazando el acuerdo/ habiendo sido solo posible un acuerdo parcial, viéndonos en la necesidad de acudir a la presente vía judicial, respecto a los extremos de la controversia en los que se mantiene la discrepancia.

Acompaño como documento nº [Nº DE DOCUMENTO], el requerimiento efectuado y como documento nº [Nº DE DOCUMENTO], la contestación del demandado.

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA.

La Jurisdicción ordinaria es la única competente para el conocimiento de los juicios que se susciten en territorio español con arreglo a lo establecido en los tratados y convenios internacionales en los que España sea parte, en las normas de la Unión Europea y en las leyes españolas (art. 21.1 LOPJ y art. 36.1 LEC).

La competencia objetiva corresponde a la Sección Civil del Tribunal de Instancia según lo dispuesto en el art. 85.1 LOPJ y art. 45 LEC.

La competencia territorial asimismo corresponde, conforme al art. 52.1.7.º LEC, por cuanto el Tribunal es el del partido del lugar en que está sita la finca.

II.- PROCEDIMIENTO.

El art. 249.1.6.º LEC dice que se decidirá en juicio ordinario las demandas que versen sobre cualesquiera asuntos relativos a arrendamientos urbanos, salvo excepciones que no comprenden el presente supuesto.

III.- CAPACIDAD.

Demandante y demandado, personas físicas, tienen capacidad para ser parte (art. 6.1.1.º LEC), titular de facultades y cargas del proceso, y asimismo plena capacidad procesal, al ser mayores de edad, sin limitación de ejercicio válido de derechos civiles, o para comparecer en juicio, en términos del art. 7 LEC, pretendiendo el actor y siendo pretendido el demandado, en sus respectivos nombres y derechos.

IV.- LEGITIMACIÓN.

La legitimación corresponde a mi poderdante activamente como arrendatario de la vivienda, y el demandado está legitimado pasivamente como propietario y arrendador de la misma.

V.- CUANTÍA.

Conforme al art. 253.1 LEC cifro la cuantía de la presente demanda en [IMPORTE] euros (€), importe de una anualidad de renta, según resulta de la regla 9.ª del art. 251 LEC.

VI.- POSTULACIÓN Y DEFENSA.

Conforme a los arts. 23 y 31 LEC, se formula esta demanda por medio de Procurador/a. de los Tribunales con poder general para pleitos y especial para percibir cantidades, con la dirección y firma de Letrado ejerciente colegiado.

VII. CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 de la LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VIII.- ASUNTO DE FONDO.

El arrendador está obligado a realizar sin derecho a elevar por ello la renta todas las reparaciones que fuesen necesarias para conservar la vivienda en las condiciones de habitabilidad para servir al uso convenido (art. 21.1 LAU 1994). Ello es paragonable al mandato del art. 1.554.2.º CCiv, consagrando la consecuencia del principio fundamental de conservar la cosa arrendada en estado de servir al uso a que ha sido destinada, y por tanto, a realizar en ella, mientras subsista el contrato, todas las reparaciones necesarias.

Las reparaciones son aquellas que hacen referencia tanto a las obras u operaciones encaminadas a la restauración de los deterioros o menoscabos sufridos en la vivienda arrendada, cuanto a la conservación de la misma, es decir, aquellas que deben realizarse ineludiblemente y no aumentan el valor ni la productividad de la cosa arrendada. El concepto es del gasto u obra sin la cual quedaría la cosa arrendada inservible para su uso, e incluso llegaría a destruirse.

La obligación de reparar no es personalísima, por lo que es exigible al arrendador y, en su caso, a sus herederos. Y, por lo mismo, están facultados para exigir su cumplimiento el arrendatario y las personas que tengan derecho a subrogarse y habiten con aquél en la vivienda arrendada.

Por su parte, el art. 27.1 LAU 1994 dispone que el incumplimiento por cualquiera de las partes de las obligaciones resultantes del contrato dará derecho a la parte que hubiera cumplido las suyas a exigir el cumplimiento o a promover la resolución del contrato.

En este sentido, se ha cumplido por mi mandante lo establecido en el art. 21.3 LAU 1994 ya que se ha puesto en conocimiento fehaciente del arrendador y en el plazo mas breve posible la necesidad de dichas reparaciones, facilitando al arrendador la verificación directa, por si mismo o por los técnicos que designara, del estado de la vivienda.

IX.- COSTAS.

Conforme al art. 394 LEC, las costas del procedimiento habrán de imponerse al demandado, si fuere vencido, y aunque se allanare, por su evidente mala fe, al haber forzado el proceso

Por lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentada esta demanda con sus documentos y copias la admita a trámite teniéndome por comparecido y parte en la representación que ostento, acordando dar traslado al demandado para que comparezca y la conteste, y seguido que sea todo el procedimiento, se dicte en su día sentencia por la que estimando la demanda se condene al arrendador demandado a realizar las reparaciones mencionada en el Hecho segundo de esta demanda, con imposición de todas las costas causadas.

Es justicia que pido en [LUGAR], a [FECHA].

Firma el Abogado/a	Firma el Procurador/a

========================================================================
