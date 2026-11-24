---
name: oposicion-extraordinaria-ejecucion-hipotecaria-civ-1423
description: "Oposición extraordinaria a la ejecución hipotecaria por abusividad de la cláusula que la fundamenta. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Oposición extraordinaria a la ejecución hipotecaria por abusividad de la cláusula que la fundamenta

> Formulario **CIV-1423** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Escrito formulando incidente extraordinario de oposición a la ejecución hipotecaria fundada en el carácter abusivo de la cláusula contractual en la que se fundamenta la ejecución, al amparo de lo establecido en la Disposición Transitoria Cuarta de la Ley 1/2013, de 14 de mayo, de medidas para reforzar la protección a los deudores hipotecarios, reestructuración de deuda y alquiler social.

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Oposición extraordinaria a la ejecución hipotecaria por abusividad de la cláusula que la fundamenta» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Oposición extraordinaria a la ejecución hipotecaria por abusividad de la cláusula que la fundamenta” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:oposicion-extraordinaria-ejecucion-hipotecaria-civ-1423`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (5 veces)
- [ ] IMPORTE (3 veces)
- [ ] AÑO (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] DÍA
- [ ] LUGAR
- [ ] MES
- [ ] MES Y AÑO
- [ ] Nº
- [ ] Nº DE CLÁUSULA
- [ ] Nº DE DOCUMENTO
- [ ] SEDE

## Normas que cita el formulario

- art. 556.1 LEC
- art. 556 LEC
- art. 695.1.4 LEC
- art. 1.1 Ley 7/1998
- art. 3 Real Decreto Legislativo 1/2007
- art. 693.1 LEC
- art. 695.3 LEC

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

Notas al pie del formulario original:
(1) De conformidad con lo establecido en la Disposición Transitoria 4ª de la Ley 1/2013, de 14 de mayo, de medidas para reforzar la protección a los deudores hipotecarios, reestructuración de deuda y alquiler social, el presente modelo no tendría actualmente utilidad posible.

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D./Dña. [NOMBRE Y APELLIDOS] Procurador de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS], según tengo acreditado en el procedimiento de ejecución hipotecaria que se sigue en ese Tribunal con el número [NÚMERO], como mejor proceda en derecho DIGO:

Que por medio del presente escrito, y al amparo de lo establecido en la Disposición Transitoria Cuarta de la Ley 1/2013, de 14 de mayo, de medidas para reforzar la protección a los deudores hipotecarios, reestructuración de deuda y alquiler social, formulo incidente extraordinario de OPOSICIÓN A LA EJECUCIÓN HIPOTECARIA acordada por este Tribunal por auto de fecha [FECHA] Oposición que baso en los siguientes:

HECHOS

PRIMERO.- Por auto de fecha [FECHA] se despachó ejecución hipotecaria contra mi cliente en reclamación de la cantidad de [IMPORTE] euros, desglosada en [IMPORTE] euros en concepto de principal, y [IMPORTE] euros en concepto de intereses devengados hasta la fecha de la certificación, más los intereses de demora que, en su caso, puedan devengarse durante la ejecución y las costas de ésta. El citado auto le fue notificado el pasado día [FECHA], habiendo transcurrido el periodo de oposición de diez días previsto en el art. 556.1 LEC.

SEGUNDO.- La demanda de ejecución hipotecaria iniciadora del procedimiento, se fundamenta en el impago de una única cuota, que se hizo inevitable a raíz de la finalización de la prestación de desempleo a la que tenía derecho mi cliente, y que fue efectiva el [DÍA] de [MES Y AÑO]. Se acompaña copia de la certificación del INEM, como documento nº 1.

Y así, se dejó de abonar, en concreto, la cuota relativa al pasado mes de [MES] de [AÑO], habiéndose aperturado la presente ejecución en función de la facultad prevista expresamente en la cláusula [Nº DE CLÁUSULA] del contrato de préstamo hipotecario, elevado a escritura pública en fecha [FECHA] de [AÑO], y obrante en autos al aportarse con la demanda; mediante la cual el acreedor hipotecario podía instar el vencimiento anticipado, y por ende, la presente ejecución por el impago de cualquiera de las cuotas. En concreto, la referida cláusula tiene el siguiente tenor: "No obstante el plazo pactado, el BANCO podrá exigir de manera anticipada, total o parcialmente, la devolución del capital con los intereses y gastos hasta el día de la completa solvencia, entre otros, cuando se deje de abonar una parte cualquiera del capital del préstamo o de sus intereses."

El contrato en cuestión, tiene una duración de 30 años, con un total de 360 cuotas previstas, habiendo satisfecho mi mandante, hasta el momento del impago, las 36 cuotas iniciales, durante los tres primeros años del contrato. Se adjunta extracto bancario en el que se refleja el pago indicado, como documento nº [Nº DE DOCUMENTO].

FUNDAMENTOS DE DERECHO

PRIMERO.- La Disposición Transitoria Cuarta de la Ley 1/2013, de 14 de mayo, de medidas para reforzar la protección a los deudores hipotecarios, reestructuración de deuda y alquiler social, prevé que en los procedimientos ejecutivos en curso a la entrada en vigor de dicha Ley en los que hubiera transcurrido el plazo de oposición de diez días del art. 556 LEC, las partes ejecutadas dispondrán de un plazo preclusivo de un mes para formular un incidente extraordinario de oposición basado en la existencia de cláusulas abusivas, computando dicho plazo desde el día siguiente a la entrada en vigor de la ley (15 de mayo de 2013), quedando mientras tanto en suspenso el proceso de ejecución.

SEGUNDO.- El art. 695.1.4ª LEC, reformado por la citada Ley 1/2013, establece como causa de oposición del ejecutado en los procedimientos de ejecución de bienes hipotecados, entre otras, el carácter abusivo de una cláusula contractual que constituya el fundamento de la ejecución o que hubiese determinado la cantidad exigible.

En el presente caso, la ejecución frente a la que se alza mi mandante tiene como fundamento la cláusula nº [NÚMERO] del contrato que sirve de título para la ejecución, y que prevé que el impago parcial o total de cualquiera de las 360 cuotas, tanto por el principal o por los intereses, previstas en el contrato puede fundamentar la ejecución, con la trascendencia que la misma supone para el deudor hipotecario, el cual ve como se vence anticipadamente el contrato, se generan una serie de intereses de demora de entidad, y se ve abocado, con escasas posibilidades de evitación, a la pérdida del inmueble adquirido en calidad de vivienda, y en el que ha tenido durante los últimos tres años su residencia habitual.

TERCERO.- En consecuencia, la cláusula fundamento de la ejecución frente a la que se alza la presente oposición, revista el carácter de abusiva, al tratarse de una condición general de contratación, impuesta a mi cliente, y que genera un desequilibrio contractual en contra de las exigencias de la buena fe, en perjuicio del consumidor. Extremos todos ellos recogidos en la sentencia del pleno del Tribunal Supremo de fecha 9 de mayo de 2.013, Rec. 485/2012, al resumir la legislación vigente sobre la materia, y que, a continuación se relaciona.

Así y en primer lugar, la misma se encuadra en el art. 1.1 de la Ley 7/1998, de 13 de abril sobre Condiciones Generales de la Contratación, al tratarse de una cláusula predispuesta (redactada unilateralmente por la entidad bancaria con carácter previo a iniciar, siquiera, negociaciones con mi mandante), impuesta (el cliente debe firmar en bloque el contrato, sin posibilidad de negociación alguna de cualquiera de sus cláusulas, más allá de negociar el interés variable finalmente asignado al préstamo), y aplicada con generalidad a todos los préstamos que concede la aquí ejecutante a la pluralidad de personas con las que contrata.

En segundo lugar, es de aplicación, el art. 3 del Real Decreto Legislativo 1/2007, de 16 de noviembre, por el que se aprueba el texto refundido de la Ley General para la Defensa de los Consumidores y Usuarios y otras leyes complementarias, al tratarse mi mandante de una persona física que acude a la entidad financiera para poder adquirir una vivienda, que se dedica al ámbito sanitario como visitador médico, y que, desde luego, actúa con un propósito ajeno a su actividad comercial, empresarial, oficio o profesión. De esta forma, entra en juego la normativa de protección a los consumidores, sobre la base del sistema de protección que establece la Directiva 93/13, bajo el prisma de que el consumidor se halla en situación de inferioridad respecto al profesional, en lo referido tanto a la capacidad de negociación como al nivel de información, situación que le lleva a adherirse a las condiciones redactadas de antemano por el profesional sin poder influir en el contenido de éstas (en este sentido, la sentencia del Tribunal de Justicia de la Unión Europea de fecha 27 de junio de 2.000).

Y así para evitar abusos en este tipo de relación contractual entre un pequeño consumidor y una entidad bancaria del calibre de la ejecutante, el art. 82.1 del citado texto legal dispone que son cláusulas abusivas "todas aquellas estipulaciones no negociadas individualmente y todas aquellas prácticas no consentidas expresamente que, en contra de las exigencias de la buena fe causen, en perjuicio del consumidor y usuario, un desequilibrio importante de los derechos y obligaciones de las partes que se deriven del contrato. El carácter abusivo de una cláusula se apreciará teniendo en cuenta la naturaleza de los bienes o servicios objeto del contrato y considerando todas las circunstancias concurrentes en el momento de su celebración, así como todas las demás cláusulas del contrato o de otro del que éste dependa"; y el art. 8.2 LCGC "serán nulas las Condiciones Generales que sean abusivas, cuando el contrato se haya celebrado con un consumidor, aquellas que no cumplan los requisitos que relaciona el art. 10 LGDCU 1984 (concreción, claridad, sencillez, buena fe y justo equilibrio entre los derechos y obligaciones de las partes etc.), y, en todo caso las definidas en el artículo 10 bis) y Disposición Adicional primera LGDCU". Remisión esta última, que debe entenderse referida, al texto de noviembre de 2.007, que deroga la misma.

Notas que concurren en la cláusula antes referida, si atendemos a la naturaleza de las prestaciones objeto del contrato, con arreglo al art. 82.3 del citado texto legal, interpretado por la citada sentencia del Tribunal Supremo, Sala Primera, de lo Civil, Sección Pleno, 241/2013 de 9 May. 2013, Rec. 485/2012, la cual indica que el desequilibrio puede manifestarse en la propia oferta desequilibrada, en la fase genética o en la ejecución del contrato, o en ambos momentos, con cita de la Sentencia del Tribunal Supremo, Sala Primera, de lo Civil, 663/2010, de 4 Nov. 2010, Rec. 982/2007 o Sentencia Tribunal Supremo, Sala Primera, de lo Civil, 861/2010 de 29 Dic. 2010, Rec. 1074/2007, que mantuvieron la posibilidad de cláusulas abusivas precisamente en contratos de préstamo. Y así, en el presente caso, cualquier impago, por mínimo que sea, en el marco de una relación obligacional de 30 años, pueda da lugar (como efectivamente ha sido) al vencimiento anticipado del contrato, tras tres años consecutivos con íntegro abono de todo lo adeudado; sin que mi cliente dispusiera de ninguna suerte de prórroga, negociación previa, o ayuda para poder abonar íntegramente una cuota, que le fue imposible a consecuencia de la grave situación económica sufrida. Lo que, con casi total seguridad, abocará a la pérdida del inmueble que sirve de vivienda.

Y este desequilibrio cuantitativo entre el montante total del capital a devolver, y la ínfima parte impagada, debe calificarse como contrario a la buena fe, en la perspectiva ofrecida por la mencionada doctrina jurisprudencial del Tribunal Supremo, que atiende a la finalidad de las condiciones generales —su incorporación a pluralidad contratos con consumidores— y de su control abstracto, no es posible limitarla a la esfera subjetiva. Es decir, mi cliente se vio obligado a aceptar dicho desequilibrio, sin posibilidad alguna de evitarla, como le hubiera ocurrido a cualquier consumidor medio. Máxime, como indica el Tribunal Supremo, tratándose de préstamos hipotecarios en los que es notorio que el consumidor confía en la apariencia de neutralidad de las concretas personas de las que se vale el empresario (personal de la sucursal) para ofertar el producto. En esta misma línea, la sentencia del Tribunal de Justicia Europeo de 14 de marzo de 2013, C-415/2011, señala que "el juez nacional debe comprobar a tal efecto si el profesional podía estimar razonablemente que, tratando de manera leal y equitativa con el consumidor, éste aceptaría una cláusula de ese tipo en el marco de una negociación individual".

Por último, la Ley 1/2013 de medidas para reforzar la protección a los deudores hipotecarios, reestructuración de deuda y alquiler social, ha modificado el art. 693.1 LEC, en el sentido de precisarse el impago de tres cuotas (o cantidad equivalente a la misma) para poder acceder a la ejecución hipotecaria. De esta forma, aunque el precepto no se encontraba en vigor en el momento en que se despacha ejecución, la propia norma marca un mínimo, tres meses, que ahondan en el desequilibrio del vencimiento que nos ocupa en función del impago de una única cuota.

Por todo ello, puede concluirse que nos encontramos ante una condición general de contratación, pacto accesorio del contrato, con carácter de cláusula abusiva, que en virtud de la redacción actual del art. 695.1.4ª LEC, y al tratarse del fundamento de la ejecución, constituye una causa de oposición a la misma.

CUARTO.- Por lo tanto, conforme a la oposición formulada procede, en primer término, suspender la ejecución y, tras los pertinentes trámites, dictar resolución acordando su sobreseimiento, de conformidad con el art. 695.3 párrafo 2º LEC, mediante auto apelable.

QUINTO.- Las costas deberán ser impuestas al ejecutante, conforme a lo dispuesto en los arts. 539.2 y 561.2 LEC, al verse sobreseída la ejecución hipotecaria interesada.

En virtud de todo lo expuesto SE INTERESA que se tenga por presentado este escrito y por formulado incidente extraordinario de oposición a la ejecución hipotecaria promovida de contrario, se proceda por el Letrado de la Administración de Justicia a la suspensión de la misma hasta la resolución del incidente, debiéndose convocar a las partes a una comparecencia donde serán oídas y podrán aportar los documentos oportunos, dictándose finalmente auto apelable, mediante el cual, estimándose la OPOSICIÓN a la ejecución, se proceda a su sobreseimiento, con imposición de las costas generadas a la parte ejecutante.

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a
