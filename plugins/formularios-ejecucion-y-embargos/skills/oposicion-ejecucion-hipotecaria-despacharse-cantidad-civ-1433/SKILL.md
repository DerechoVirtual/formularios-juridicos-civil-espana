---
name: oposicion-ejecucion-hipotecaria-despacharse-cantidad-civ-1433
description: "Oposición a la ejecución hipotecaria por despacharse por una cantidad derivada de cláusula abusiva. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Oposición a la ejecución hipotecaria por despacharse por una cantidad derivada de cláusula abusiva

> Formulario **CIV-1433** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Escrito de oposición del ejecutado (persona física consumidora) a una ejecución hipotecaria ya despachada, dentro del plazo de diez días, por ser abusiva la cláusula (en el modelo, la de intereses de demora) que determina la cantidad exigible, conforme al art. 695.1.4.ª LEC; solicita la suspensión de la ejecución y su continuación solo por el principal.

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Oposición a la ejecución hipotecaria por despacharse por una cantidad derivada de cláusula abusiva» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Oposición a la ejecución hipotecaria por despacharse por una cantidad derivada de cláusula abusiva” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:oposicion-ejecucion-hipotecaria-despacharse-cantidad-civ-1433`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (6 veces)
- [ ] PORCENTAJE (6 veces)
- [ ] Nº DE CLÁUSULA (3 veces)
- [ ] FECHA (2 veces)
- [ ] FIRMA (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL EJECUTADO (2 veces)
- [ ] APARTADO
- [ ] AÑO
- [ ] DENOMINACIÓN SOCIAL DEL EJECUTANTE
- [ ] DNI/NIE
- [ ] DOMICILIO
- [ ] DÍA
- [ ] LOCALIDAD
- [ ] MES
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº DE DOCUMENTO
- [ ] Nº DE PLAZA
- [ ] Nº DE PROCEDIMIENTO
- [ ] NÚMERO
- [ ] PROFESIÓN O ACTIVIDAD
- [ ] SEDE

## Normas que cita el formulario

- art. 695.1.4.ª LEC
- art. 1.1 Ley 7/1998
- art. 394.1 LEC
- art. 1108 CC
- art. 114 LH

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

### Avisos de actualización (3) — se aplican en el texto, nunca se copian en el documento

- Al principio del formulario: el modelo se redactó con la regulación posterior a la Ley 1/2013 (art. 114 LH y su Disposición Transitoria 2.ª). Debe contrastarse con la redacción del art. 114 LH dada por la Ley 5/2019, de 15 de marzo, reguladora de los contratos de crédito inmobiliario, y con la jurisprudencia posterior del TJUE y del Tribunal Supremo sobre intereses de demora y efectos de la nulidad.
- Junto a «… A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº DE PLAZA]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…xto refundido de la Ley General para la Defensa de los Consumidores y Usuarios».»: el original reproducía el art. 8.2 LCGC en su redacción antigua, con remisión al art. 10 bis y a la disposición adicional primera de la Ley 26/1984, derogada por el TRLGDCU; comprobar la redacción vigente del art. 8.2 LCGC antes de entrecomillarlo.

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº DE PLAZA]

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS DEL EJECUTADO], con domicilio en [DOMICILIO] y DNI número [DNI/NIE], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], ante el Tribunal comparezco y como mejor proceda en derecho DIGO:

Que en nombre de mi poderdante me persono en los autos de ejecución hipotecaria seguidos a instancia de la entidad [DENOMINACIÓN SOCIAL DEL EJECUTANTE] y registrados con el número [Nº DE PROCEDIMIENTO], y por medio del presente escrito formulo oposición a la citada ejecución, dentro del plazo concedido al efecto, en virtud de los siguientes

HECHOS

PRIMERO.- Por auto de fecha [FECHA] se despachó ejecución hipotecaria contra mi cliente en reclamación de la cantidad de [IMPORTE] euros, desglosada en [IMPORTE] euros en concepto de principal y [IMPORTE] euros en concepto de intereses devengados hasta la fecha de la certificación, más los intereses de demora que, en su caso, puedan devengarse durante la ejecución y las costas de ésta. El citado auto le fue notificado el pasado día [FECHA], por lo que el presente escrito se ha presentado dentro del término de diez días concedido al efecto para formular oposición.

SEGUNDO.- La cantidad indicada correspondiente a los intereses calculados y, en su caso, por calcular se fundamenta en la cláusula nº [Nº DE CLÁUSULA] del contrato de préstamo que obra en autos. En concreto, se señala que «Las obligaciones dinerarias de la parte prestataria, dimanantes de este contrato, vencidas y no satisfechas, devengarán desde el día siguiente al de su vencimiento, sin necesidad de requerimiento alguno y sin perjuicio de la facultad de vencimiento anticipado atribuida al Banco en la Cláusula [Nº DE CLÁUSULA], un interés de demora del [PORCENTAJE] % NOMINAL ANUAL, calculado y liquidable por meses naturales o fracción en su caso y siempre por periodos vencidos. Los intereses vencidos y no satisfechos devengarán y se liquidarán en igual forma nuevos intereses al tipo de interés moratorio aquí establecido. Las cantidades resultantes como intereses de demora se considerarán firmes en el momento en que se perciban, sin perjuicio del derecho del Banco a exigir los intereses moratorios devengados hasta cada momento, y quedarán garantizadas exclusivamente con cargo a la cantidad máxima consignada en el apartado [APARTADO] de la cláusula [Nº DE CLÁUSULA]».

FUNDAMENTOS DE DERECHO

PRIMERO.- El art. 695.1.4.ª LEC, reformado por la Ley 1/2013, de 14 de mayo, de medidas para reforzar la protección a los deudores hipotecarios, reestructuración de deuda y alquiler social, establece como causa de oposición del ejecutado en los procedimientos de ejecución de bienes hipotecados, entre otras, el carácter abusivo de una cláusula contractual que constituya el fundamento de la ejecución o que hubiese determinado la cantidad exigible.

En el presente caso, la ejecución frente a la que se alza mi mandante se inicia por una cantidad concreta que se corresponde al principal impagado en cantidad de [IMPORTE] euros, así como los intereses moratorios previstos en el préstamo en su día concertado, del [PORCENTAJE] %, para un total de [IMPORTE] euros por los generados hasta el momento de la certificación, más los que se generen con posterioridad.

SEGUNDO.- En consecuencia, la cláusula que determina la cantidad exigible de la ejecución frente a la que se alza la presente oposición reviste el carácter de abusiva, al tratarse de una condición general de la contratación, impuesta a mi cliente, y que genera un desequilibrio contractual en contra de las exigencias de la buena fe, en perjuicio del consumidor. Extremos todos ellos recogidos en la sentencia del Tribunal Supremo, Sala Primera, Pleno, 241/2013, de 9 de mayo de 2013, rec. 485/2012, al resumir la legislación vigente sobre la materia, y que a continuación se relaciona.

Así, y en primer lugar, la misma se encuadra en el art. 1.1 de la Ley 7/1998, de 13 de abril, sobre Condiciones Generales de la Contratación, al tratarse de una cláusula predispuesta (redactada unilateralmente por la entidad bancaria con carácter previo a iniciar, siquiera, negociaciones con mi mandante), impuesta (el cliente debe firmar en bloque el contrato, sin posibilidad de negociación alguna de sus cláusulas) y aplicada con generalidad a todos los préstamos que concede la aquí ejecutante a la pluralidad de personas con las que contrata.

En segundo lugar, es de aplicación el art. 3 del texto refundido de la Ley General para la Defensa de los Consumidores y Usuarios y otras leyes complementarias, aprobado por Real Decreto Legislativo 1/2007, de 16 de noviembre, al tratarse mi mandante de una persona física que acude a la entidad financiera para poder adquirir una vivienda, que se dedica a [PROFESIÓN O ACTIVIDAD] y que, desde luego, actúa con un propósito ajeno a su actividad comercial, empresarial, oficio o profesión. De esta forma, entra en juego la normativa de protección a los consumidores, sobre la base del sistema de protección que establece la Directiva 93/13/CEE, bajo el prisma de que el consumidor se halla en situación de inferioridad respecto al profesional, en lo referido tanto a la capacidad de negociación como al nivel de información, situación que le lleva a adherirse a las condiciones redactadas de antemano por el profesional sin poder influir en el contenido de éstas (en este sentido, la sentencia del Tribunal de Justicia de la Unión Europea de fecha 27 de junio de 2000).

Y así, para evitar abusos en este tipo de relación contractual entre un pequeño consumidor y una entidad bancaria del calibre de la ejecutante, el art. 82.1 del citado texto legal dispone que son cláusulas abusivas «todas aquellas estipulaciones no negociadas individualmente y todas aquellas prácticas no consentidas expresamente que, en contra de las exigencias de la buena fe causen, en perjuicio del consumidor y usuario, un desequilibrio importante de los derechos y obligaciones de las partes que se deriven del contrato. El carácter abusivo de una cláusula se apreciará teniendo en cuenta la naturaleza de los bienes o servicios objeto del contrato y considerando todas las circunstancias concurrentes en el momento de su celebración, así como todas las demás cláusulas del contrato o de otro del que éste dependa»; y el art. 8.2 de la Ley sobre Condiciones Generales de la Contratación: «serán nulas las condiciones generales que sean abusivas, cuando el contrato se haya celebrado con un consumidor, entendiendo por tales en todo caso las definidas en el artículo 82 y siguientes del texto refundido de la Ley General para la Defensa de los Consumidores y Usuarios».

Notas que concurren en la cláusula antes referida, si atendemos a la naturaleza de las prestaciones objeto del contrato, con arreglo al art. 82.3 del citado texto legal, interpretado por la citada sentencia del Tribunal Supremo, Sala Primera, Pleno, 241/2013, de 9 de mayo de 2013, rec. 485/2012, la cual indica que el desequilibrio puede manifestarse en la propia oferta desequilibrada, en la fase genética o en la ejecución del contrato, o en ambos momentos, con cita de las sentencias del Tribunal Supremo, Sala Primera, 663/2010, de 4 de noviembre de 2010, rec. 982/2007, y 861/2010, de 29 de diciembre de 2010, rec. 1074/2007, que mantuvieron la posibilidad de cláusulas abusivas precisamente en contratos de préstamo. Y así, en el presente caso, se apertura la ejecución por una cantidad realmente impagada, el principal, y por unos intereses claramente abusivos, que conforman una cantidad muy superior a la realmente debida y que supone un importe más de [NÚMERO] veces el interés legal del dinero vigente en el momento de la firma del contrato ([PORCENTAJE] %). Todo ello hace imposible que mi cliente pueda hacer frente al montante total reclamado y le aboca, indefectiblemente, a perder la vivienda. En la sentencia de la Audiencia Provincial de Córdoba, Sección 3.ª, 22/2007, de 5 de febrero de 2007, rec. 18/2007, se sostiene que no debe olvidarse que el interés de demora tiene, ciertamente, una finalidad sancionadora por no adecuarse la conducta del deudor al régimen jurídico pactado por las partes y, sobre todo, que el interés de demora tiene no sólo como objetivo sancionar o castigar al deudor que no cumple, sino, como plásticamente dice determinada doctrina, «disuadir a potenciales incumplidores de hacerlo». Precisamente por razón de dicha naturaleza indemnizatoria y disuasoria, el interés de demora es notablemente más elevado que el remuneratorio, pero esto no implica una autorización en blanco para el acreedor, de forma que pueda establecer sin ningún techo la sanción que desee, sino que ha de ser una sanción equilibrada, una sanción que no conlleve un interés desproporcionado que genere un desequilibrio en las prestaciones de las partes. En esta misma línea, la sentencia de la Audiencia Provincial de Valencia, Sección 7.ª, 404/2012, de 13 de julio de 2012, rec. 152/2012, aprecia tal carácter en unos intereses de demora que superan en cinco veces el citado interés legal [ADAPTAR AL CASO: proporción real entre el interés pactado y el interés legal].

Y este desequilibrio cuantitativo entre lo realmente impagado y la cantidad a devolver, y entre el interés normal del dinero y el moratorio fijado en el contrato, debe calificarse como contrario a la buena fe, en la perspectiva ofrecida por la mencionada doctrina jurisprudencial del Tribunal Supremo, que atiende a la finalidad de las condiciones generales (su incorporación a pluralidad de contratos con consumidores) y de su control abstracto, que no es posible limitarla a la esfera subjetiva. Es decir, mi cliente se vio obligado a aceptar dicho desequilibrio, sin posibilidad alguna de evitarlo, como le hubiera ocurrido a cualquier consumidor medio. Máxime, como indica el Tribunal Supremo, tratándose de préstamos hipotecarios en los que es notorio que el consumidor confía en la apariencia de neutralidad de las concretas personas de las que se vale el empresario (personal de la sucursal) para ofertar el producto. En esta misma línea, la sentencia del Tribunal de Justicia de la Unión Europea de 14 de marzo de 2013, C-415/11, señala que «el juez nacional debe comprobar a tal efecto si el profesional podía estimar razonablemente que, tratando de manera leal y equitativa con el consumidor, éste aceptaría una cláusula de ese tipo en el marco de una negociación individual».

Por último, la Ley 1/2013 modificó el art. 114 de la Ley Hipotecaria en el sentido de imponer un límite máximo para los intereses de demora de tres veces el interés legal del dinero. De esta forma, aunque el precepto no sea de aplicación a la presente ejecución [ADAPTAR AL CASO: la Disposición Transitoria 2.ª de la citada ley dispone su aplicación respecto a aquellas hipotecas constituidas tras el 15 de mayo de 2013 o, en el caso de las hipotecas anteriores, respecto a las cantidades devengadas con posterioridad], la propia norma fija el máximo, que se situaría en el [PORCENTAJE] % (siendo el interés legal del dinero el [PORCENTAJE] %). Lo que ahonda en el desequilibrio y carácter abusivo del porcentaje del [PORCENTAJE] % aquí impugnado, que supera dicho límite [ADAPTAR AL CASO: en más del doble / en la medida que corresponda].

De esta forma, puede concluirse que nos encontramos ante una condición general de la contratación, pacto accesorio del contrato, con carácter de cláusula abusiva, que, en virtud de la redacción del art. 695.1.4.ª LEC y al tratarse de la regla que determina la mayor parte de la cantidad exigible, constituye una causa de oposición a la misma.

TERCERO.- Por lo tanto, conforme a la oposición formulada procede, en primer término, suspender la ejecución y, tras los pertinentes trámites, dictar resolución acordando la continuación del procedimiento, de conformidad con el art. 695.3, párrafo 2.º, LEC, mediante auto apelable. Si bien, la cantidad por la que se prosiga la ejecución deberá reducirse exclusivamente a la cantidad correspondiente al principal, excluyendo cualquier cantidad en concepto de intereses derivado de la cláusula abusiva. De esta forma, el nuevo mandato legislativo viene a positivizar la jurisprudencia emanada del Tribunal de Justicia de la Unión Europea, de la cual es ejemplo la sentencia de fecha 14 de junio de 2012, C-618/10, la cual, tras declarar una cláusula abusiva, manifiesta que no puede modificar ni integrar el contenido del contrato tras declararla nula por abusiva. Considera que, si el juez nacional tuviera la facultad de modificar el contenido de las cláusulas abusivas que figuran en tales contratos, dicha facultad podría poner en peligro la consecución del objetivo a largo plazo previsto en el art. 7 de la Directiva 93/13/CEE; pues contribuiría a eliminar el efecto disuasorio que ejerce sobre los profesionales el hecho de que, pura y simplemente, tales cláusulas abusivas no se apliquen frente a los consumidores. Esto es, si el contrato se corrige, los profesionales podrían verse tentados a utilizar cláusulas abusivas al saber que, aun cuando llegara a declararse la nulidad de las mismas, el contrato podría ser integrado por el juez nacional en lo que fuera necesario, garantizando de este modo el interés de dichos profesionales (véase la nota explicativa al final).

CUARTO.- Las costas de esta oposición deberán ser impuestas al ejecutante, conforme al art. 394.1 LEC.

En virtud de todo lo expuesto SE INTERESA que se tenga por presentado este escrito y por personado y parte al procurador que suscribe en nombre y representación de [NOMBRE Y APELLIDOS DEL EJECUTADO], con quien se entenderán las sucesivas diligencias, teniendo por formulada oposición a la ejecución hipotecaria promovida de contrario, por lo que se procederá por el Letrado de la Administración de Justicia a la suspensión de la misma, debiéndose convocar a las partes a una comparecencia donde serán oídas y podrán aportar los documentos oportunos, dictándose finalmente auto apelable, mediante el cual, estimándose la oposición a la ejecución, se continúe la misma exclusivamente por la cantidad de [IMPORTE] euros, con imposición de las costas generadas a la parte ejecutante.

Es de Justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a: [FIRMA] Firma del Procurador/a: [FIRMA]

NOTA EXPLICATIVA

En cuanto a los efectos de la nulidad de la cláusula de intereses, se propone la solicitud de exclusión de los mismos, en virtud de la jurisprudencia del Tribunal de Justicia de la Unión Europea indicada, sin perjuicio de reseñar que existe otra posibilidad. Así, en las «Conclusiones de la Jornada sobre las repercusiones de la doctrina del TJUE en materia de cláusulas abusivas en ejecuciones hipotecarias», que tuvo lugar el 8 de mayo de 2013, en un curso organizado por el Servicio de Formación Continua del Consejo General del Poder Judicial, se concluyó que, en el caso de las cláusulas de intereses de demora, la nulidad comportará la expulsión de la cláusula y se considera que el principal devengará los intereses legalmente previstos, existiendo a estos efectos dos posiciones mayoritarias: la que defiende la aplicación del Código Civil (intereses del art. 1108 CC) o la que sostiene la aplicación de la Ley Hipotecaria (interés del art. 114 LH).

Más recientemente, respondiendo a cuestión prejudicial, la STJUE de 21 de enero de 2015, C-482/13, declaró que la legislación española en materia de ejecución hipotecaria (arts. 552.1, 561.1.3.ª y 695.1.4.ª LEC; 114 LH y DT 2.ª Ley 1/2013), que establece que el juez nacional está obligado a hacer que se recalculen los intereses de demora resultantes de la aplicación de un tipo superior a tres veces el interés legal del dinero, es compatible con el Derecho de la Unión.

No obstante, el juez español debe tener la posibilidad de considerar abusiva la cláusula que imponga tales intereses y, en consecuencia, de dejarla sin aplicación (véase en este sentido el auto del Tribunal de Instancia (Sección Civil) de Cáceres de 23 de enero de 2015, proc. 136/2014).
