---
name: apelacion-contra-auto-deniega-ejecutar-laudo-arbitral-civ-1504
description: "Apelación contra el auto que deniega ejecutar un laudo arbitral en materia de arrendamientos. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Apelación contra el auto que deniega ejecutar un laudo arbitral en materia de arrendamientos

> Formulario **CIV-1504** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Escrito de interposición de recurso de apelación por la parte ejecutante contra el auto que deniega el despacho de ejecución de un laudo arbitral (en el ejemplo, resolución de un arrendamiento de vivienda por impago de renta), sosteniendo que la materia es arbitrable. Se interpone ante el tribunal que dictó el auto, para conocimiento de la Audiencia Provincial (arts. 458 y 552.2 LEC).

Es un modelo de tipo **recursos**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Apelación contra el auto que deniega ejecutar un laudo arbitral en materia de arrendamientos» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Apelación contra el auto que deniega ejecutar un laudo arbitral en materia de arrendamientos” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:apelacion-contra-auto-deniega-ejecutar-laudo-arbitral-civ-1504`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA DEL AUTO (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A (2 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] AÑO
- [ ] DOMICILIO DEL INMUEBLE
- [ ] DÍA
- [ ] FECHA
- [ ] FECHA DEL LAUDO
- [ ] IMPORTE
- [ ] IMPORTE DEL DEPÓSITO
- [ ] LOCALIDAD
- [ ] MES
- [ ] NOMBRE Y APELLIDOS DEL ABOGADO/A, Nº DE COLEGIADO
- [ ] NOMBRE Y APELLIDOS DEL EJECUTANTE
- [ ] Nº
- [ ] PROVINCIA
- [ ] SEDE

## Normas que cita el formulario

- art. 517.2.º LEC
- art. 39.5 LAU
- art. 2 Ley 60/2003

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

- Junto a «…DIMIENTO] A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…exigido para interponer el recurso, por importe de [IMPORTE DEL DEPÓSITO] euros.»: el original fijaba el depósito en 50 euros; comprobar la cuantía vigente del depósito para recurrir en la disposición adicional decimoquinta LOPJ.

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

Proceso de ejecución número [Nº DE PROCEDIMIENTO]

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS DEL EJECUTANTE], parte demandante en este proceso seguido con el número [Nº DE PROCEDIMIENTO], según tengo acreditado en autos, ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que en fecha [FECHA] se me ha notificado el auto de fecha [FECHA DEL AUTO] denegando el despacho de ejecución y, no encontrándolo ajustado a Derecho, dicho sea con los debidos respetos y en términos de defensa, por medio del presente escrito, y de conformidad con lo dispuesto en los arts. 458 y 552.2 de la LEC, interpongo contra el mismo RECURSO DE APELACIÓN para ante la Audiencia Provincial de [PROVINCIA], impugnando el pronunciamiento denegatorio del despacho de ejecución, alegando los siguientes

MOTIVOS

PRIMERO.– Infracción del artículo 2 de la Ley de Arbitraje, en relación con los artículos 517.2.º y 549 de la LEC, al tratarse de una materia que puede ser objeto de arbitraje.

La demanda ejecutiva pretendía la ejecución del laudo de fecha [FECHA DEL LAUDO] que declaraba resuelto el contrato de arrendamiento de vivienda sita en [DOMICILIO DEL INMUEBLE] por falta de pago de la renta, condenando al demandado al desalojo del inmueble así como al pago de [IMPORTE] euros por razón de las rentas impagadas, siendo denegado el despacho de ejecución en el auto objeto de apelación razonando en que la regulación arrendaticia urbana, y la procesal correlativa, es de carácter imperativo, considerándose normas de orden público por razón del derecho de enervación de la acción, o por aplicación del fuero de competencia territorial inderogable, considerando que tales controversias en ningún caso pueden someterse a un arbitraje.

Esta interpretación es contraria a la sostenida de forma uniforme por las Audiencias Provinciales, que vienen declarando que la materia de arrendamientos urbanos no está excluida del arbitraje, que la regulación del contrato de arrendamiento mediante norma imperativa no significa la existencia de un derecho indisponible que impida el arbitraje, y que las normas de competencia territorial dictadas para el proceso no son aplicables a los arbitrajes que, por definición, excluyen la actividad procesal.

En relación con la posibilidad de someter a arbitraje los conflictos de arrendamientos urbanos, el AAP Madrid de 25 de noviembre de 2009, rec. 550/2009, entre otros muchos, expresa que la exposición de motivos de la LAU de 1994 prevé el arbitraje como método de solución de conflictos y que, en sintonía con esa posibilidad, el art. 39.5 de la LAU de 1994 permitía la solución de conflictos arrendaticios por tribunales arbitrales, sin que la derogación de tal precepto por la LEC de 2000 signifique la imposibilidad de someter la cuestión al arbitraje, puesto que la finalidad de la disposición derogatoria única de la LEC era eliminar los procesos especiales diseminados por todo el ordenamiento jurídico, pero no suprimir la posibilidad del arbitraje arrendaticio convirtiendo en indisponible una materia que no lo es esencialmente. En el mismo sentido, el artículo 2 de la Ley de Arbitraje de 2003 engloba la materia arrendaticia, puesto que, desde la naturaleza del contrato, no hay mayores obstáculos dispositivos, en tanto que se trata de la transferencia temporalmente limitada de la posesión inmediata de un bien inmueble, y de todas las condiciones de uso del mismo, a cambio de un precio cierto, y desde la naturaleza del proceso de desahucio, tampoco hay problemas dispositivos por cuanto que la función del proceso es regular el cumplimiento del contrato de arrendamiento, equilibrando el disfrute continuo y permanente de la posesión de cosa ajena con la contraprestación económica correspondiente a la renta y demás cantidades asumidas por el arrendatario, acordando su resolución ante la mora comprobada del inquilino.

Por otra parte, la existencia de normas imperativas en el arrendamiento no significa que no existan derechos disponibles en materia arrendaticia, puesto que no debe confundirse el carácter de las normas jurídicas con el ejercicio de los derechos privados de los que se puede disponer, incluso en el máximo grado de disposición que implica la renuncia, según ya expresara la STS de 21 de marzo de 1985, que añadía que el carácter imperativo de las normas no convierte a las controversias surgidas en torno a un derecho en no susceptibles de arbitraje y, en consecuencia, el límite de lo que puede ser objeto de arbitraje debe situarse en aquellas materias que contraríen el orden público, que no es el caso del laudo dictado en materia arrendaticia.

El artículo 2.1 de la Ley de Arbitraje establece que «son susceptibles de arbitraje las controversias sobre materias de libre disposición conforme a derecho», por lo que, atendiendo al carácter patrimonial de las normas arrendaticias concernidas por el arbitraje, la LAU no hace indisponible la materia que regula, tanto más cuando se trata de determinar el cumplimiento contractual y, muy significadamente, el de la principal obligación del arrendatario.

Así lo entiende de forma uniforme la interpretación de las Audiencias, pudiendo citarse el AAP Barcelona de 16 de marzo de 2005, rec. 693/2004; la SAP Vizcaya de 17 de mayo de 2005, rec. 616/2004, y la SAP Madrid de 3 de febrero de 2009, entre otras muchas, de las que se infiere que la cuestión arrendaticia se encuentra entre las contempladas en el artículo 2 de la Ley 60/2003, de 23 de diciembre (Ley de Arbitraje), el cual establece que son susceptibles de arbitraje las controversias sobre materias de libre disposición conforme a derecho, ámbito en el que se incardinan los arrendamientos y, entre ellos, los de fincas urbanas, según igualmente admitió la Ley de Arrendamientos Urbanos 29/1994, y tienen declarado numerosas Audiencias Provinciales, lo cual comporta la exclusión de las normas procesales (salvo las que afectan al orden público del procedimiento) contenidas en la Ley de Enjuiciamiento Civil, que son sustituidas por las que libremente convengan las partes (artículo 25 de la Ley de Arbitraje), entre las que se encuentra la de fijar el lugar del arbitraje (artículo 26), tal como indica el AAP Madrid, Sección 10.ª, de 15 de diciembre de 2010, rec. 751/2010.

Tal como se acreditó en nuestra demanda ejecutiva, la pretensión de ejecución del laudo lo es en virtud de una cláusula arbitral suscrita e incorporada a un contrato de arrendamiento celebrado entre dos particulares, por lo que no es de aplicación la normativa de defensa de los consumidores.

En consecuencia, dándose los requisitos establecidos en los artículos 517.2 y 549.1, párrafo 2.º, el título aportado, laudo arbitral, lleva aparejada ejecución, conforme exige el artículo 517.2, y se aportan los documentos acreditativos de la notificación del laudo a las partes, conforme exige el artículo 550, por lo que sí concurren los requisitos establecidos en dichos preceptos para despachar la ejecución interesada. Partiendo de lo anterior, es procedente el despacho de ejecución por cumplirse los requisitos legalmente establecidos, por lo que se solicita de la Sala que revoque la resolución recurrida y que acuerde el despacho de ejecución en los términos solicitados en nuestra demanda ejecutiva.

En base a lo anterior,

SUPLICO AL TRIBUNAL que tenga por presentado este escrito, teniendo por interpuesto el recurso de apelación frente al auto dictado en las presentes actuaciones de fecha [FECHA DEL AUTO] y, tras la pertinente tramitación, se dicte por éste auto en el que, declarando haber lugar al recurso de apelación, se acuerde el despacho de ejecución en los términos solicitados en nuestra demanda ejecutiva.

OTROSÍ DIGO, que de conformidad con lo dispuesto en los apartados 3 y 6 de la disposición adicional decimoquinta de la LOPJ acompaño a este escrito resguardo de consignación en la cuenta de Depósitos y Consignaciones abierta a nombre del Tribunal del depósito exigido para interponer el recurso, por importe de [IMPORTE DEL DEPÓSITO] euros.

Por lo que,

SUPLICO AL TRIBUNAL que tenga por constituido el depósito, dejando interesada desde este momento su devolución para el caso de estimación total o parcial del recurso.

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma Procurador: [NOMBRE Y APELLIDOS DEL PROCURADOR/A]

Firma Abogado: [NOMBRE Y APELLIDOS DEL ABOGADO/A, Nº DE COLEGIADO]
