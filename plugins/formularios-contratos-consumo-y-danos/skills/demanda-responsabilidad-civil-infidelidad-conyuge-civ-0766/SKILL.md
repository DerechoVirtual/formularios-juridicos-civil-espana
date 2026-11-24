---
name: demanda-responsabilidad-civil-infidelidad-conyuge-civ-0766
description: "Demanda de responsabilidad civil por la infidelidad de un cónyuge. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de responsabilidad civil por la infidelidad de un cónyuge

> Formulario **CIV-0766** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario por la que un cónyuge reclama a su excónyuge una indemnización de daños morales y patrimoniales (arts. 1902 CC o, subsidiariamente, 1101 CC) por haber incumplido el deber de fidelidad con ocultación de que los hijos que creía suyos eran de un tercero, habiendo prosperado la impugnación de paternidad.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de responsabilidad civil por la infidelidad de un cónyuge» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de responsabilidad civil por la infidelidad de un cónyuge” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-responsabilidad-civil-infidelidad-conyuge-civ-0766`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] AÑO (15 veces)
- [ ] DÍA (15 veces)
- [ ] MES (15 veces)
- [ ] Nº (12 veces)
- [ ] IMPORTE (11 veces)
- [ ] NOMBRE Y APELLIDOS DE LA DEMANDADA (5 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] IMPORTE TOTAL (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] NOMBRE DEL MENOR (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL DEMANDANTE (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL FACULTATIVO (2 veces)
- [ ] SEDE (2 veces)
- [ ] COLEGIO DE ABOGADOS
- [ ] DOCUMENTO QUE ACREDITA EL INTENTO DE SOLUCIÓN EXTRAJUDICIAL
- [ ] INDICAR EL MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] NOMBRE Y APELLIDOS DEL CÓNYUGE
- [ ] NOMBRE Y APELLIDOS DEL LETRADO
- [ ] NOMBRE Y APELLIDOS DEL PADRE BIOLÓGICO
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] NOMBRE/S DE LOS HIJOS
- [ ] Nº DE DOCUMENTO
- [ ] Nº DE HIJOS
- [ ] PROFESIÓN

## Normas que cita el formulario

- art. 1964 CC
- art. 1969 CC
- art. 1968.2.º Código Civil
- art. 5 Ley Orgánica 1/2025
- art. 67 Código Civil
- art. 152.4.º CC
- art. 855.1.º CC
- art. 1343 CC
- art. 1101 CC
- art. 1902 CC
- art. 1902 Código Civil

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

- Junto a «…os arts. 1969 y 1101 CC.] A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…n relación con lo dispuesto en el art. 85 de la Ley Orgánica del Poder Judicial.»: el original citaba el art. 22.3.º y el art. 85.1.º LOPJ, anteriores a la LO 1/2025; comprobar los apartados vigentes tras la creación de los Tribunales de Instancia.
- Junto a «…eredación (art. 855.1.º CC); o causa de revocación de donaciones (art. 1343 CC).»: comprobar la redacción vigente de los arts. 152, 855 y 1343 CC tras las reformas posteriores (en particular, Ley 8/2021), por si ha variado la numeración o el contenido de los apartados citados.

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

[NOTA PARA EL PROFESIONAL, A SUPRIMIR ANTES DE PRESENTAR: téngase en cuenta en el Fundamento de Derecho sobre el plazo que, si el demandante decide basar su demanda en la responsabilidad contractual del cónyuge infiel, el plazo de referencia será el general de cinco años del art. 1964 CC, en relación con los arts. 1969 y 1101 CC.]

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dª [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, en nombre y representación de D./Dª [NOMBRE Y APELLIDOS DEL DEMANDANTE], mayor de edad, de profesión [PROFESIÓN], con domicilio en [DOMICILIO], cuya representación acreditaré mediante comparecencia apud acta cuando sea requerido para ello [ELEGIR: (sin más) / "representación que acredito mediante copia de poder que ruego me sea devuelta una vez testimoniada"], comparezco en este Tribunal con la asistencia del Letrado D./Dª [NOMBRE Y APELLIDOS DEL LETRADO], del Ilustre Colegio de Abogados de [COLEGIO DE ABOGADOS], y DIGO:

Que por medio del presente escrito y en la representación que ostento, interpongo demanda de JUICIO ORDINARIO contra D./Dª [NOMBRE Y APELLIDOS DE LA DEMANDADA], mayor de edad, con domicilio en [DOMICILIO], en reclamación de cantidad por responsabilidad civil.

La presente demanda se basa en los siguientes

HECHOS

PRIMERO.- Mi representado/a contrajo matrimonio [ELEGIR: civil / canónico] con D./Dª [NOMBRE Y APELLIDOS DEL CÓNYUGE], en [LOCALIDAD], el día [DÍA] de [MES] de [AÑO]. Se acompaña como Documento nº [Nº] certificación de matrimonio expedida por el Registro Civil de [LOCALIDAD], para acreditar este hecho.

SEGUNDO.- Durante el matrimonio nacieron [Nº DE HIJOS] hijo/s, llamado/s [NOMBRE/S DE LOS HIJOS]; el primero, el día [DÍA] de [MES] de [AÑO], y el segundo, el día [DÍA] de [MES] de [AÑO]. Se acompañan como Documentos nº [Nº] y nº [Nº] certificación de la inscripción de nacimiento de uno y otro, expedida por el Registro Civil de [LOCALIDAD].

TERCERO.- El día [DÍA] de [MES] de [AÑO], los cónyuges suscribieron un convenio regulador, protocolizado notarialmente, procediendo así a una separación de cuerpos y bienes, quedando los hijos bajo la guarda y custodia de [ELEGIR: la madre / el padre], con las obligaciones del otro progenitor respecto a las cargas matrimoniales, que incluían el pago de una pensión de alimentos de [IMPORTE] euros ([IMPORTE] €) mensuales por cada uno de los hijos menores de edad, en total [IMPORTE TOTAL] euros ([IMPORTE TOTAL] €) mensuales.

CUARTO.- En fecha [DÍA] de [MES] de [AÑO], D./Dª [NOMBRE Y APELLIDOS DE LA DEMANDADA] presentó demanda contra mi representado/a, impugnando su paternidad respecto a los hijos mencionados, procedimiento en el que recayó sentencia de fecha [DÍA] de [MES] de [AÑO], en la que se declaró que el verdadero padre de los citados hijos no era mi representado/a, sino D./Dª [NOMBRE Y APELLIDOS DEL PADRE BIOLÓGICO], con los derechos y obligaciones inherentes a dicha relación paterno-filial, debiendo hacerse en el Registro Civil correspondiente las oportunas rectificaciones e inscripciones. Se acompaña, como Documento nº [Nº], testimonio de la referida sentencia.

QUINTO.- En fecha [DÍA] de [MES] de [AÑO], se instó por D./Dª [NOMBRE Y APELLIDOS DE LA DEMANDADA], cónyuge de mi representado/a, demanda de divorcio contra éste/a, recayendo sentencia el día [DÍA] de [MES] de [AÑO], que quedó firme. Se acompaña, como Documento nº [Nº], testimonio de la sentencia de divorcio.

SEXTO.- La infidelidad del cónyuge de mi representado/a ha tenido como grave resultado el nacimiento de [Nº] hijo/s que, durante los años transcurridos hasta el descubrimiento de la realidad por mi representado/a, trató y quiso éste/a como propios, convencido/a de que lo eran, efectuando los gastos dirigidos a su manutención, en el más amplio sentido.

Para combatir el trauma ocasionado por la sensación de pérdida de los que consideraba como hijos y el dolor ocasionado por el comportamiento de su cónyuge, mi representado/a ha necesitado tratamiento psiquiátrico. Se acompaña como Documento nº [Nº] informe emitido por el Dr./Dra. [NOMBRE Y APELLIDOS DEL FACULTATIVO], que lo ha tratado.

Se han derivado, pues, de los referidos hechos daños patrimoniales y económicos causados por la conducta de la demandada, a quien fue su cónyuge y creyó ser el padre/madre de sus hijos. Conducta grave, que debe ser calificada de dolosa, pues la demandada ocultó conscientemente los citados hechos a mi representado/a, provocando el error del que se derivarían los daños referidos.

Aunque el daño moral sufrido no puede tener exacta traducción pecuniaria, merece una compensación económica, en cuyo concepto se solicita la cantidad de [IMPORTE] euros, que deberá satisfacerle la demandada.

En relación con el daño patrimonial sufrido, comprende las siguientes cantidades en concepto de gastos invertidos en dar cumplimiento a la obligación de alimentos de los supuestos hijos, obligación que resulta ser inexistente por carecer en realidad los alimentistas de la condición de hijos de mi representado/a y no estar éste/a obligado/a a alimentarlos:

1. [IMPORTE] euros mensuales satisfechos en concepto de alimentos a favor del menor [NOMBRE DEL MENOR], tras la separación de los cónyuges, desde el día [DÍA] de [MES] de [AÑO] hasta el día [DÍA] de [MES] de [AÑO]. Suman un total de [IMPORTE TOTAL] euros. (Se repite por cada uno de los menores.) Se acompaña como Documento nº [Nº] justificante bancario del ingreso de tales cantidades en la cuenta de la que es titular D./Dª [NOMBRE Y APELLIDOS DE LA DEMANDADA], en la que se han venido abonando las mismas.

2. [IMPORTE] euros en que se estiman los gastos invertidos en la manutención del menor [NOMBRE DEL MENOR] antes de la separación de los cónyuges, desde el día [DÍA] de [MES] de [AÑO], en que aquél nació, hasta el día [DÍA] de [MES] de [AÑO]. Se ha calculado la suma multiplicando por el número de meses transcurridos la cantidad de [IMPORTE] euros, coincidente con la cuantía mensual de la pensión de alimentos que se ha venido satisfaciendo tras la separación. (Se repite por cada uno de los menores.)

A las anteriores debe sumarse la cantidad de [IMPORTE] euros satisfecha en concepto de gastos médicos por el tratamiento psiquiátrico que, como consecuencia de los hechos descritos, ha requerido mi representado/a. Se acompañan como Documentos nº [Nº] a [Nº] facturas emitidas por el Dr./Dra. [NOMBRE Y APELLIDOS DEL FACULTATIVO], que lo ha tratado.

También se reclama, en concepto de lucro cesante, la cantidad de [IMPORTE] euros, para compensar la disminución de ingresos de mi representado/a como consecuencia de la incapacidad para su trabajo habitual que sufrió, como consecuencia del trauma psicológico derivado de los hechos descritos, durante los meses transcurridos desde el día [DÍA] de [MES] de [AÑO] hasta el día [DÍA] de [MES] de [AÑO]. Se acompañan los Documentos nº [Nº] y nº [Nº] como justificativos de la baja laboral y las razones de la misma, así como de la disminución de los ingresos de mi representado/a.

Por último, se estima como compensación justa por los daños morales asociados al sufrimiento de mi representado/a por la pérdida de quienes consideraba sus hijos, la de [IMPORTE] euros.

SÉPTIMO.- Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial. En este sentido, se acudió a [INDICAR EL MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO] [DOCUMENTO QUE ACREDITA EL INTENTO DE SOLUCIÓN EXTRAJUDICIAL].

Resultan aplicables a los citados hechos los siguientes

FUNDAMENTOS DE DERECHO

JURISDICCIÓN.- Es competente la jurisdicción civil, de acuerdo con lo establecido en el art. 22 de la Ley Orgánica del Poder Judicial.

COMPETENCIA.- Son competentes los Tribunales de [SEDE], lugar en que tiene su domicilio la demandada, de acuerdo con el artículo 50.1 de la Ley de Enjuiciamiento Civil, en relación con lo dispuesto en el art. 85 de la Ley Orgánica del Poder Judicial.

PROCEDIMIENTO.- La presente demanda debe sustanciarse por los trámites del juicio ordinario, en virtud de lo dispuesto en el artículo 249.2 de la Ley de Enjuiciamiento Civil, por exceder la cuantía reclamada de quince mil euros.

CAPACIDAD.- Ambas partes tienen capacidad para ser parte, conforme a lo dispuesto en los artículos 6 y siguientes de la Ley de Enjuiciamiento Civil.

LEGITIMACIÓN.- Están legitimados activa y pasivamente el/la demandante y el/la demandada. El primero/a, como perjudicado/a por el comportamiento doloso de la demandada al incumplir el deber de fidelidad conyugal y ocultar a su cónyuge que los hijos que éste/a creía suyos eran producto de aquella infidelidad, del que se han derivado daños para aquél/aquélla; y la segunda, como causante de tales daños.

REPRESENTACIÓN Y DEFENSA.- El/La demandante comparece representado/a y defendido/a, respectivamente, por el Procurador y el Letrado que constan en el encabezamiento de este escrito, de acuerdo con lo dispuesto en los artículos 23.1 y 31.1 de la Ley de Enjuiciamiento Civil.

PLAZO DE EJERCICIO.- Esta acción de responsabilidad civil derivada de daños se ejercita dentro del plazo de un año que establece el artículo 1968.2.º del Código Civil, en relación con los artículos 1969 y 1902 del mismo Código.

CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.- La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4.º y 399.3 de la Ley de Enjuiciamiento Civil, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

DERECHO SUSTANTIVO.- Los artículos 67 y 68 del Código Civil imponen a los cónyuges, como concreción del debido respeto entre los mismos, el deber de guardarse fidelidad, que los consortes asumen, autolimitando su esfera de libertad personal, al contraer matrimonio.

El incumplimiento de esta obligación lesiona la dignidad del cónyuge (art. 10 de la Constitución) y constituye infracción de un deber jurídico.

La marcada impronta ética que caracteriza al deber de fidelidad no obsta a su carácter jurídico. Así resulta, entre otras consideraciones, del reconocimiento por la ley de determinados efectos civiles derivados de su quiebra: cese de la obligación legal de alimentos (art. 152.4.º CC); causa de desheredación (art. 855.1.º CC); o causa de revocación de donaciones (art. 1343 CC).

Además, la quiebra del deber de fidelidad, cuando genera daños personales y/o patrimoniales, hace surgir la obligación de indemnizar los mismos. Dicha obligación puede basarse en el incumplimiento contractual (arts. 1101 y concordantes CC), si se considera que la fidelidad conyugal es una obligación contractual que tiene su origen en el contrato de matrimonio; o, de no admitirse esto, en el instituto de la responsabilidad extracontractual (arts. 1902 y concordantes CC).

Las circunstancias y los daños se agravan cuando, como resultado de las relaciones extramatrimoniales del cónyuge, nacieron hijos que el otro consideró como suyos, amó y cuidó como tales, hasta que descubrió que no era él/ella, sino el amante de su cónyuge, el padre/madre de los mismos, circunstancias que concurren en el caso de mi representado/a. Por otra parte, la demandada ha actuado con dolo, ocultando esta realidad a su cónyuge.

Así pues, al incumplimiento del deber de fidelidad en sentido estricto, que, por otra parte, puede calificarse de grave y reiterado o continuado en el tiempo, se suma la procreación de un hijo (o varios) extramatrimonial con ocultación al cónyuge y el pago de alimentos por éste.

Las Audiencias Provinciales han condenado en diversas ocasiones al resarcimiento de este tipo de daños en casos equivalentes al de mi representado/a. En este sentido, puede citarse la sentencia de la Audiencia Provincial de Valencia de 2 de noviembre de 2004. En ella se consideró que, si el adulterio va acompañado de una intención cualificada de causar daño, como en el supuesto del engaño al marido en relación con su no paternidad, ha lugar al resarcimiento del daño causado por la vía del art. 1902 CC. En el mismo sentido se pronuncian las siguientes sentencias: Audiencia Provincial de Valencia de 5 de septiembre de 2007, rec. 467/2007; Audiencia Provincial de Barcelona de 16 de enero de 2007; Audiencia Provincial de Cádiz de 3 de abril de 2008, rec. 83/2007; Audiencia Provincial de Barcelona de 31 de octubre de 2008, rec. 131/2008, y de 23 de julio de 2009, rec. 792/2008; Audiencia Provincial de Murcia de 18 de noviembre de 2009.

IURA NOVIT CURIA y los demás que en derecho procedan.

COSTAS.- Procede imponer al/a la demandado/a el pago de las costas, en virtud de lo dispuesto en el art. 394 de la Ley de Enjuiciamiento Civil.

Por lo expuesto,

SUPLICO AL TRIBUNAL: Que, tras admitir este escrito con los documentos que lo acompañan y sus copias, tenga por interpuesta demanda, que habrá de sustanciarse por los trámites del juicio ordinario, en nombre de D./Dª [NOMBRE Y APELLIDOS DEL DEMANDANTE], en ejercicio de la acción de reclamación de daños y perjuicios por responsabilidad civil extracontractual, basada en el art. 1902 del Código Civil, o, subsidiariamente, de responsabilidad civil contractual con base en el art. 1101 del mismo Código, contra D./Dª [NOMBRE Y APELLIDOS DE LA DEMANDADA]; y, previos los trámites legales que procedan, dicte sentencia en la que, estimando íntegramente la demanda, condene a la demandada a satisfacer a mi representado/a la cantidad de [IMPORTE] euros en concepto de indemnización de daños morales y patrimoniales, que resulta de sumar las partidas detalladas en el Hecho SEXTO de la presente, salvo fijación de otra por el juzgador. Y se condene al/a la demandado/a al pago de las costas del presente procedimiento.

OTROSÍ DIGO.- En cumplimiento de lo dispuesto en el art. 253 de la Ley de Enjuiciamiento Civil, esta parte fija la cuantía del procedimiento, calculada de acuerdo con lo dispuesto en el art. 251 de la misma Ley, en la cantidad de [IMPORTE] euros.

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma y número de colegiado del Letrado Firma del Procurador
