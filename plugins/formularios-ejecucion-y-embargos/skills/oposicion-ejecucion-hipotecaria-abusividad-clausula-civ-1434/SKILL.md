---
name: oposicion-ejecucion-hipotecaria-abusividad-clausula-civ-1434
description: "Oposición a la ejecución hipotecaria por abusividad de la cláusula que fundamenta el despacho. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Oposición a la ejecución hipotecaria por abusividad de la cláusula que fundamenta el despacho

> Formulario **CIV-1434** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Escrito de oposición a la ejecución hipotecaria fundada en el carácter abusivo de la cláusula contractual en la que se fundamenta la ejecución, por haberse despachado ejecución tras impago de una de las cuotas.

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Oposición a la ejecución hipotecaria por abusividad de la cláusula que fundamenta el despacho» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Oposición a la ejecución hipotecaria por abusividad de la cláusula que fundamenta el despacho” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:oposicion-ejecucion-hipotecaria-abusividad-clausula-civ-1434`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (4 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] AÑO (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] DENOMINACIÓN SOCIAL
- [ ] DÍA
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] MES
- [ ] MES Y AÑO
- [ ] Nº
- [ ] Nº DE CLÁUSULA
- [ ] SEDE

## Normas que cita el formulario

- art. 695.1.4 LEC
- art. 1.1 Ley 7/1998
- art. 3 Real Decreto Legislativo 1/2007
- art. 693.1 LEC
- art. 695.3 LEC
- art. 231 LEC

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
(1) Normativa aplicable:

— Código Civil: Artículos 1255,1258.

— Ley 1/2000 de 7 de enero de Enjuiciamiento Civil: Artículos 539.2, 552, 557.1.7ª, 561.2, 693.1, 695.1.4ª, 695.3.

— Real Decreto Legislativo 1/2007, de 16 de noviembre, por el que se aprueba el texto refundido de la Ley General para la Defensa de los Consumidores y Usuarios y otras leyes complementarias: Artículos 3, 4, 59, 80, 82, 83.

— Ley 7/1998, de 13 de abril, sobre Condiciones Generales de la Contratación: Artículos 1.1, 10

— Directiva 93/13/CEE, de 5 de abril, sobre cláusulas abusivas en los contratos celebrados con consumidores: Artículos 3 y 4.

(2) Jurisprudencia de interés:

— Tribunal Supremo, Sala Primera, de lo Civil, Sentencia 241/2013 de 9 May. 2013, Rec. 485/2012 (

«(...) 114. En definitiva, como ha reiterado el TJUE "el juez nacional debe apreciar de oficio el carácter abusivo de una cláusula contractual" (SSTJUE de 6 de octubre de 2009, Asturcom Telecomunicaciones, C40/08, apartado 32, 14 junio 2012, C-618/10, Banco Español de Crédito, apartado 42+43 y 21 febrero 2013, C-472/2011, Caso Banif Plus Bank Zrt 23).

115. A esta obligación no es ajeno este Tribunal, ya que la efectividad de la Directiva y la tutela de los intereses de los consumidores frente a las cláusulas abusivas resulta imperativa para la totalidad de los tribunales de la Unión.

1.4. La prueba de oficio de la abusividad.

116. Este deber no solo comprende el de apreciar la abusividad cuando esta aparezca demostrada de forma clara y contundente. Cuando existan motivos razonables para entender que una cláusula es abusiva, si es preciso, se debe acordar la práctica de prueba. En este sentido, con referencia a un supuesto de atribución de competencia jurisdiccional territorial exclusiva en un contrato celebrado entre un profesional y un consumidor, el Tribunal de Justicia declaró que "el juez nacional debe acordar de oficio diligencias de prueba para determinar si una cláusula está comprendida en el ámbito de aplicación de la Directiva"»

— Audiencia Provincial de Zamora, Sentencia 96/2014 de 4 Jun. 2014, Rec. 95/2014

«(...) Por otro lado, respecto a este tipo de cláusulas el art. 693.1 LEC, en su nueva redacción dada por la Ley 1/2013, de 14 de mayo —aunque no sea aplicable a la póliza del presente proceso pero si puede servir como criterio interpretativo— condiciona la facultad de instar la ejecución del préstamo hipotecario al impago de al menos tres plazos mensuales, limitándose lógicamente la ejecución a las cantidades adeudadas; y el art. 693.2 admite la facultad de declarar el vencimiento anticipado de la totalidad de una deuda a plazos ante el impago de al menos tres plazos mensuales, si así se hubiera pactado expresamente. Esto debe ponerse en relación con la doctrina jurisprudencial aplicable al caso, y así la STS 16-12-09, rec. 2114/2005, proclama como doctrina jurisprudencial más reciente la validez de estas cláusulas de vencimiento anticipado, con base en el principio de libertad de pactos del art. 1255 CC, si bien precisando que solo serán de aplicación cuando concurra justa causa, entendiendo por tal la objetivamente manifiesta y verdadera dejación de las obligaciones de carácter esencial, es decir la insolvencia sobrevenida del deudor o claro peligro de que no pueda atender la prestación principal, como sucede cuando el número de cuotas impagadas es tan elevado y reiterado en el tiempo que cabe deducir que el deudor no va a pagar ninguna cuota más, es decir, que nunca va a devolver el préstamo.

Así, en el caso de autos, debemos partir de los siguientes datos deducidos de la prueba practicada:1) Cuando los prestarios dejan de pagar la primera cuota del préstamo ya había venido pagando las cuotas mensuales de los cinco años anteriores; 2) El cierre de la cuenta para proceder a la reclamación se realizó cuando había impagado 8 mensualidades; 3) Cuando se presenta la demanda ya había dejado de pagar el importe de diez mensualidades.

Por tanto, debemos considerar como nula por abusiva la cláusula 6 bis del apartado a), pues el establecer como causa de vencimiento anticipado el impago de una sola cuota del préstamo, cuando en el momento de la firma del contrato no se había revelado una situación de insolvencia o claro peligro de no hacer frente al pago de la deuda, como ha quedado de manifiesto por el hecho de que los prestatarios pagaron las cuotas de cinco años, es claramente abusivo por desproporcionado, como viene a corroborar la Ley 1/2013, de 14 de mayo, que establece como posible causa de vencimiento anticipado a fijar en los contratos el impago de tres plazos mensuales. Ahora bien, no queremos terminar la resolución de este primer motivo, sin referirnos a que la declaración de nulidad de dicha cláusula, no conlleva, lógicamente, que no se pueda interesar el vencimiento anticipado del contrato hasta el momento de su terminación, sino que cabe perfectamente aplicar la doctrina general de los contratos, pues lo único que se dice con la declaración de nulidad de dicha cláusula es que la entidad bancaria no podrá interesar el vencimiento anticipado del contrato por el impago de un plazo.»

— Otras Sentencias de interés.- Tribunal de Justicia de la Unión Europea, Sala Primera, Sentencia de 14 Mar. 2013, C-415/2011; Audiencia Provincial de Lleida, Sección 2ª, Sentencia 188/2015 de 27 Abr. 2015, Rec. 510/2014

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

D./Dña. [NOMBRE Y APELLIDOS] Procurador/a de los Tribunales, en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD] y D.N.I. número [NÚMERO], conforme acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], ante el Tribunal comparezco y como mejor proceda en derecho DIGO:

Que en nombre de mi poderdante me persono en los autos de ejecución hipotecaria seguidos a instancia de la entidad [DENOMINACIÓN SOCIAL] y registrados con el número [NÚMERO], y por medio del presente escrito formulo oposición a la citada ejecución, dentro del plazo concedido al efecto, en virtud de los siguientes

HECHOS

PRIMERO.- Por auto de fecha [FECHA] se despachó ejecución hipotecaria contra mi cliente en reclamación de la cantidad de [IMPORTE] euros ( [IMPORTE] €) en concepto de principal e intereses devengados hasta la fecha de la certificación, más los intereses de demora que, en su caso, puedan devengarse durante la ejecución y las costas de ésta, auto que le fue notificado el pasado día [FECHA], por lo que el presente escrito se ha presentado dentro del término de diez días concedido al efecto para formular oposición.

SEGUNDO.- La demanda de ejecución hipotecaria iniciadora del procedimiento, se fundamenta en el impago de una única cuota, que se hizo inevitable a raíz de la finalización de la prestación de desempleo a la que tenía derecho mi cliente, y que fue efectiva el [DÍA] de [MES Y AÑO] Se acompaña copia de la certificación del INEM, como documento n.º [Nº DE DOCUMENTO].

Y así, se dejó de abonar, en concreto, la cuota relativa al pasado mes de [MES] de [AÑO], habiéndose aperturado la presente ejecución en función de la facultad prevista expresamente en la cláusula [Nº DE CLÁUSULA] del contrato de préstamo hipotecario, elevado a escritura pública en fecha [FECHA] de [AÑO], y obrante en autos al aportarse con la demanda; mediante la cual el acreedor hipotecario podía instar el vencimiento anticipado, y por ende, la presente ejecución por el impago de cualquiera de las cuotas. En concreto, la referida cláusula tiene el siguiente tenor: "No obstante el plazo pactado, el BANCO podrá exigir de manera anticipada, total o parcialmente, la devolución del capital con los intereses y gastos hasta el día de la completa solvencia, entre otros, cuando se deje de abonar una parte cualquiera del capital del préstamo o de sus intereses."

El contrato en cuestión, tiene una duración de 30 años, con un total de 360 cuotas previstas, habiendo satisfecho mi mandante, hasta el momento del impago, las 36 cuotas iniciales, durante los tres primeros años del contrato. Se adjunta extracto bancario en el que se refleja el pago indicado, como documento n.º 2.

FUNDAMENTOS DE DERECHO

PRIMERO.- El art. 695.1.4ª LEC, reformado por Ley 1/2013, de 14 de mayo, de medidas para reforzar la protección a los deudores hipotecarios, reestructuración de la deuda y alquiler social, establece como causa de oposición del ejecutado en los procedimientos de ejecución de bienes hipotecados, entre otras, el carácter abusivo de una cláusula contractual que constituya el fundamento de la ejecución o que hubiese determinado la cantidad exigible.

En el presente caso, la ejecución frente a la que se alza mi mandante tiene como fundamento la cláusula n.º [NÚMERO] del contrato que sirve de título para la ejecución, y que prevé que el impago parcial o total de cualquiera de las 360 cuotas, tanto por el principal o por los intereses, previstas en el contrato puede fundamentar la ejecución, con la trascendencia que la misma supone para el deudor hipotecario, el cual ve como se vence anticipadamente el contrato, se generan una serie de intereses de demora de entidad, y se ve abocado, con escasas posibilidades de evitación, a la pérdida del inmueble adquirido en calidad de vivienda, y en el que ha tenido durante los últimos tres años su residencia habitual.

SEGUNDO.- En consecuencia, la cláusula fundamento de la ejecución frente a la que se alza la presente oposición, revista el carácter de abusiva, al tratarse de una condición general de contratación, impuesta a mi cliente, y que genera un desequilibrio contractual en contra de las exigencias de la buena fe, en perjuicio del consumidor. Extremos todos ellos recogidos en la sentencia del pleno del Tribunal Supremo de fecha 9 de mayo de 2013, rec. 485/2012, al resumir la legislación vigente sobre la materia, y que, a continuación se relaciona.

Así y en primer lugar, la misma se encuadra en el art. 1.1 de la Ley 7/1998, de 13 de abril, sobre Condiciones Generales de la Contratación, al tratarse de una cláusula predispuesta (redactada unilateralmente por la entidad bancaria con carácter previo a iniciar, siquiera, negociaciones con mi mandante), impuesta (el cliente debe firmar en bloque el contrato, sin posibilidad de negociación alguna de cualquiera de sus cláusulas, más allá de negociar el interés variable finalmente asignado al préstamo), y aplicada con generalidad a todos los préstamos que concede la aquí ejecutante a la pluralidad de personas con las que contrata.

En segundo lugar, es de aplicación, el art. 3 del Real Decreto Legislativo 1/2007, de 16 de noviembre, por el que se aprueba el texto refundido de la Ley General para la Defensa de los Consumidores y Usuarios y otras leyes complementarias, al tratarse mi mandante de una persona física que acude a la entidad financiera para poder adquirir una vivienda, que se dedica al ámbito sanitario como visitador médico, y que, desde luego, actúa con un propósito ajeno a su actividad comercial, empresarial, oficio o profesión. De esta forma, entra en juego la normativa de protección a los consumidores, sobre la base del sistema de protección que establece la Directiva 93/13/CEE, bajo el prisma de que el consumidor se halla en situación de inferioridad respecto al profesional, en lo referido tanto a la capacidad de negociación como al nivel de información, situación que le lleva a adherirse a las condiciones redactadas de antemano por el profesional sin poder influir en el contenido de éstas (en este sentido, la sentencia del Tribunal de Justicia de la Unión Europea de fecha 27 de junio de 2.000, C-240/1998).

Y así para evitar abusos en este tipo de relación contractual entre un pequeño consumidor y una entidad bancaria del calibre de la ejecutante, el art. 82.1 del citado texto legal dispone que son cláusulas abusivas "todas aquellas estipulaciones no negociadas individualmente y todas aquellas prácticas no consentidas expresamente que, en contra de las exigencias de la buena fe causen, en perjuicio del consumidor y usuario, un desequilibrio importante de los derechos y obligaciones de las partes que se deriven del contrato. El carácter abusivo de una cláusula se apreciará teniendo en cuenta la naturaleza de los bienes o servicios objeto del contrato y considerando todas las circunstancias concurrentes en el momento de su celebración, así como todas las demás cláusulas del contrato o de otro del que éste dependa"; y el art. 8.2 LCGC "serán nulas las condiciones generales que sean abusivas, cuando el contrato se haya celebrado con un consumidor, aquellas que no cumplan los requisitos que relaciona el art. 10 LGDCU 1984 (concreción, claridad, sencillez, buena fe y justo equilibrio entre los derechos y obligaciones de las partes etc.), y, en todo caso las definidas en el artículo 10 bis) y Disposición Adicional primera LGDCU". Remisión esta última, que debe entenderse referida, al texto de noviembre de 2.007, que deroga la misma.

Notas que concurren en la cláusula antes referida, si atendemos a la naturaleza de las prestaciones objeto del contrato, con arreglo al art. 82.3 del citado texto legal, interpretado por la citada sentencia del Tribunal Supremo, Sala Primera, de lo Civil, Sección Pleno, 241/2013 de 9 May. 2013, Rec. 485/2012, la cual indica que el desequilibrio puede manifestarse en la propia oferta desequilibrada, en la fase genética o en la ejecución del contrato, o en ambos momentos, con cita de la sentencia del Tribunal Supremo, Sala Primera, de lo Civil, 663/2010 de 4 Nov. 2010, Rec. 982/2007 ó Sentencia del Tribunal Supremo, Sala Primera, de lo Civil, 861/2010 de 29 Dic. 2010, Rec. 1074/2007, que mantuvieron la posibilidad de cláusulas abusivas precisamente en contratos de préstamo. Y así, en el presente caso, cualquier impago, por mínimo que sea, en el marco de una relación obligacional de 30 años, pueda dar lugar (como efectivamente ha sido) al vencimiento anticipado del contrato, tras tres años consecutivos con íntegro abono de todo lo adeudado; sin que mi cliente dispusiera de ninguna suerte de prórroga, negociación previa, o ayuda para poder abonar íntegramente una cuota, que le fue imposible a consecuencia de la grave situación económica sufrida. Lo que, con casi total seguridad, abocará a la pérdida del inmueble que sirve de vivienda.

Y este desequilibrio cuantitativo entre el montante total del capital a devolver, y la ínfima parte impagada, debe calificarse como contrario a la buena fe, en la perspectiva ofrecida por la mencionada doctrina jurisprudencial del Tribunal Supremo, que atiende a la finalidad de las condiciones generales —su incorporación a pluralidad contratos con consumidores— y de su control abstracto, no es posible limitarla a la esfera subjetiva. Es decir, mi cliente se vio obligado a aceptar dicho desequilibrio, sin posibilidad alguna de evitarla, como le hubiera ocurrido a cualquier consumidor medio. Máxime, como indica el Tribunal Supremo, tratándose de préstamos hipotecarios en los que es notorio que el consumidor confía en la apariencia de neutralidad de las concretas personas de las que se vale el empresario (personal de la sucursal) para ofertar el producto. En esta misma línea, la sentencia del Tribunal de Justicia Europeo de 14 de marzo de 2013, C-415/2011, señala que "el juez nacional debe comprobar a tal efecto si el profesional podía estimar razonablemente que, tratando de manera leal y equitativa con el consumidor, éste aceptaría una cláusula de ese tipo en el marco de una negociación individual".

Por último, la Ley 1/2013 de medidas para reforzar la protección a los deudores hipotecarios, reestructuración de deuda y alquiler social, ha modificado el art. 693.1 LEC, en el sentido de precisarse el impago de tres cuotas (o cantidad equivalente a la misma) para poder acceder a la ejecución hipotecaria. De esta forma, aunque el precepto no se encontraba en vigor en el momento en que se despacha ejecución (la Disposición Transitoria 4ª de la citada ley dispone su aplicación respecto a aquellas actuaciones ejecutivas pendientes de realizar, en los procesos en tramitación a fecha 15 de mayo de 2.013), la propia norma marca un mínimo, tres meses, que ahondan en el desequilibrio del vencimiento que nos ocupa en función del impago de una única cuota.

De esta forma, puede concluirse que nos encontramos ante una condición general de contratación, pacto accesorio del contrato, con carácter de cláusula abusiva, que en virtud de la redacción actual del art. 695.1.4ª LEC, y al tratarse del fundamento de la ejecución, constituye una causa de oposición a la misma.

TERCERO.- Por lo tanto, conforme a la oposición formulada procede, en primer término, suspender la ejecución y, tras los pertinentes trámites, dictar resolución acordando su sobreseimiento, de conformidad con el art. 695.3 párrafo 2º LEC, mediante auto apelable.

CUARTO.- Las costas de esta oposición deberán ser impuestas al ejecutante, conforme a lo dispuesto en los arts. 539.2 y 561.2 LEC, al verse sobreseída la ejecución hipotecaria interesada.

En virtud de todo lo expuesto,

SUPLICO AL TRIBUNAL:

Que se tenga por presentado este escrito y por personado y parte al procurador que suscribe en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], con quien se entenderán las sucesivas diligencias,; se sirva admitirlo junto con los documentos que lo acompañan y, en virtud de lo expuesto en el mismo, tenga por formulada oposición a la ejecución hipotecaria promovida de contrario, procediéndose por el Letrado de la Administración de Justicia a la suspensión de la misma, debiéndose convocar a las partes a una comparecencia donde serán oídas y podrán aportar los documentos oportunos, dictándose finalmente auto apelable, mediante el cual, estimándose la OPOSICIÓN a la ejecución, se proceda a su sobreseimiento, con imposición de las costas generadas a la parte ejecutante.

Es de Justicia que pido en [LUGAR], a [FECHA].

PRIMER OTROSÍ DIGO.- Que esta parte manifiesta la expresa voluntad de cumplir con los requisitos exigidos por la Ley, interesando que de incurrir en algún defecto procesal se cuide de que pueda ser subsanado, a tenor de lo dispuesto en el art. 231 de la LEC.

DE NUEVO SUPLICO AL TRIBUNAL: Que se sirva tener por hecha la precedente manifestación de intenciones.

En igual lugar y fecha

Firma del Abogado/a	Firma del Procurador/a
