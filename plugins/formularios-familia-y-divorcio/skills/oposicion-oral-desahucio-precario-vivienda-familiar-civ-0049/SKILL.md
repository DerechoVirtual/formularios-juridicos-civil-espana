---
name: oposicion-oral-desahucio-precario-vivienda-familiar-civ-0049
description: "Oposición oral al desahucio por precario de la vivienda familiar alegando fraude de ley. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Oposición oral al desahucio por precario de la vivienda familiar alegando fraude de ley

> Formulario **CIV-0049** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Contestación oral del demandado en la vista de un juicio verbal de desahucio por precario, cuando el demandante es un tercero que adquirió la vivienda familiar por una partición hereditaria hecha en fraude de ley (art. 6.4 CC) para privar de su uso al cónyuge a quien se atribuyó en sentencia de separación o divorcio; se apoya en la doctrina de la STS de 18 de marzo de 2008, rec. 5847/2000.

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Oposición oral al desahucio por precario de la vivienda familiar alegando fraude de ley» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Oposición oral al desahucio por precario de la vivienda familiar alegando fraude de ley” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:oposicion-oral-desahucio-precario-vivienda-familiar-civ-0049`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] LOS PADRES / EL PADRE / LA MADRE
- [ ] MES
- [ ] Nº DE DOCUMENTO
- [ ] Nº DE PLAZA
- [ ] Nº DE PROCEDIMIENTO
- [ ] SEDE

## Normas que cita el formulario

- art. 6.4 Código Civil
- art. 1058 Código Civil
- art. 1261 Código Civil
- art. 1058 CC

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

- Junto a «…AD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº DE PLAZA]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.

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

Juicio de desahucio por precario nº [Nº DE PROCEDIMIENTO]

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº DE PLAZA]

Con la venia, manifestamos nuestra disconformidad con las pretensiones de la parte actora y nos oponemos a la demanda interpuesta, interesando su íntegra desestimación con imposición de las costas al/a la demandante, conforme a los siguientes argumentos:

EN RELACIÓN CON LOS HECHOS ADUCIDOS EN LA DEMANDA:

En desacuerdo con la titularidad de la parte demandante sobre la vivienda litigiosa, por derivar de una partición de herencia otorgada en fraude de ley, como luego se razona. Dicha herencia es la del [PARENTESCO, p. ej. padre] del cónyuge de la/del demandada/o. Este último, siendo propietario de la vivienda litigiosa, cedió su uso gratuitamente a su hijo/a, D./Dña. [NOMBRE Y APELLIDOS], y al cónyuge de éste, demandado/a en este procedimiento, para que establecieran allí su domicilio familiar. Tras el fallecimiento del propietario, la vivienda se adjudicó, en escritura denominada de partición parcial de la herencia (que se ha acompañado a la demanda), a los actores, [PARENTESCO CON EL CÓNYUGE DEL DEMANDADO, p. ej. hermanos] del cónyuge de la/del demandada/o. Ahora bien, dicha adjudicación se ha realizado, insisto, en fraude de ley, por lo que no es susceptible de sustentar la legitimación de la parte actora en la acción de desahucio por precario interpuesta. Así se induce, entre otras circunstancias, del hecho de no constar en la citada escritura de partición otros bienes con los que pudiera satisfacerse los derechos hereditarios del cónyuge de mi mandante.

De acuerdo con la existencia y fecha del matrimonio y con la cesión de la vivienda a título gratuito, en su día, por [LOS PADRES / EL PADRE / LA MADRE] del esposo/a de la/del demandada/o para que fuera utilizada por el matrimonio y el hijo común de ambos.

De acuerdo con la existencia de divorcio y la atribución del uso de la vivienda familiar en la correspondiente sentencia a la/al demandada/o, bajo cuya guarda y custodia quedaba el hijo común de la pareja.

De acuerdo con la existencia de requerimientos extrajudiciales de la parte actora a la/al demandada/o para que desalojase la vivienda. Sin embargo, la parte demandada respondió a dichos requerimientos negándose a dejar libre la vivienda por haberle sido atribuido su uso por sentencia judicial y carecer la actora de título legítimo que ampare su propiedad y, en consecuencia, la acción de desahucio por precario, como a continuación se razona. Se presenta, como prueba documental nº [Nº DE DOCUMENTO], burofax de fecha [DÍA] de [MES] de [AÑO], en que consta la citada respuesta.

EN RELACIÓN CON LOS FUNDAMENTOS DE DERECHO PROCESALES ADUCIDOS EN LA DEMANDA:

De acuerdo con los relativos a jurisdicción, competencia, procedimiento, representación, defensa y capacidad.

En desacuerdo con los relativos a legitimación de las partes, por entender que la partición de herencia de la que deriva la titularidad actual de la parte demandante sobre la vivienda litigiosa se efectuó en fraude de ley, precisamente para dar pie al presente procedimiento de desahucio en precario y privar a la/al demandante del uso de la vivienda. Este extremo guarda relación con los fundamentos de Derecho sustantivo, a los que nos referimos a continuación.

EN RELACIÓN CON LOS FUNDAMENTOS DE DERECHO SUSTANTIVOS:

Hay que decir que, tras el fallecimiento de D. [NOMBRE] y Dña. [NOMBRE], [PARENTESCO, p. ej. suegros] de mi representado/a y propietarios de la vivienda litigiosa, el pleno dominio de ésta fue adjudicado en partición de herencia a D./Dña. [NOMBRE Y APELLIDOS], hijo/a de los finados y hermano/a del ex esposo/a de mi representada/o, que es quien ha interpuesto la demanda de desahucio que ha dado lugar al presente procedimiento.

Es cierto que el Tribunal Supremo, ante la situación de precario que se crea en virtud de la cesión gratuita de los padres a los hijos por razón de su matrimonio, tiene declarado que la atribución de uso a uno de los cónyuges que se produce por virtud del proceso de crisis matrimonial no supone la creación de un derecho real específico ni puede interferir en los derechos de terceros ajenos al proceso de separación o divorcio. Sin embargo, el mismo Tribunal, en su sentencia de 18 de marzo de 2008, rec. 5847/2000, ha entendido que, si la partición de herencia de la que deriva la titularidad del actor sobre la vivienda cuyo desalojo se solicita ha sido realizada en fraude de ley y con la finalidad, precisamente, de crear un título para la reivindicación, por aplicación de lo dispuesto en el artículo 6.4 del Código Civil, tal fraude no puede alterar la situación de hecho existente en orden a la ocupación de la vivienda por los demandados, ex esposa e hijos a los que se atribuyó el uso de la vivienda en sentencia de separación matrimonial.

La citada sentencia señala: «Como ya se ha dicho, la sentencia recurrida basa la desestimación de la demanda en que la actuación del demandante se ha producido en fraude de ley, lo que determina su ineficacia frente a la parte demandada y el mantenimiento a favor de la misma del derecho de uso que le venía conferido sobre la vivienda familiar a raíz del proceso matrimonial. La sentencia de esta Sala de 9 de marzo de 2006, con cita de la de 28 de enero de 2005, viene a recoger la doctrina jurisprudencial sobre la interpretación del artículo 6.4 del Código Civil en los siguientes términos: "el fraude de ley requiere como elemento esencial un acto o serie de actos que, pese a su apariencia de legalidad, violan el contenido ético de los preceptos en que se amparan, ya se tenga o no conciencia de burlar la Ley (sentencias, entre otras, de 17 de abril de 1997, 3 de febrero de 1998, 21 de diciembre de 2000). Se caracteriza (sentencias, entre otras, de 4 de noviembre de 1994, 23 de enero de 1999, 27 de mayo de 2001, 13 de junio de 2003) por la presencia de dos normas: la conocida, denominada «de cobertura», que es a la que se acoge quien intenta el fraude, y la que a través de ésta se pretende eludir, que es la norma denominada «eludible o soslayable», amén que ha de perseguir un resultado contrario a lo ordenado o prohibido imperativamente (sentencia de 27 de marzo de 2001 y 30 de septiembre de 2002). Es claro que no se requiere la intención, o conciencia, o idea dirigida a burlar la ley (sentencias de 17 de abril de 1997, 3 de febrero de 1998 y otras), pero es preciso que la Ley en que se ampara el acto presuntamente fraudulento no le proteja suficientemente (sentencia de 23 de febrero de 1993) y que la actuación se encamine a la producción de un resultado contrario o prohibido por una norma tenida como fundamental en la materia, y tal resultado se manifieste de forma notoria e inequívoca (sentencias de 4 de noviembre de 1982 y 30 de junio de 1993)".

En el caso presente resulta indiscutible que se ha constituido una titularidad del demandante (…) sobre la vivienda en cuestión que, en principio, le habilita para dar fin a la situación de precario de la que se beneficia la demandada. Pero existen hechos, que son los que ha tenido presentes la Audiencia, que demuestran el "iter" fraudulento y preconcebido en la sucesión del bien para crear una legitimación "ad hoc" que permita ejercer al actor los derechos dominicales de que se pretende valer, a los que se anuda una dejación de derechos por parte del esposo de la demandada en cuanto a los que pudieran corresponderle sobre la vivienda de que se trata.

No puede desconocerse que el artículo 1058 del Código Civil atribuye a los herederos mayores de edad que gocen, además, de la libre disposición de sus bienes, la facultad de distribuir la herencia de la manera que tengan por conveniente. Dicha facultad, en palabras de la sentencia de 19 de junio de 1997, es tan amplia que permite a los coherederos realizar actos particionales más allá de los propios divisorios y de lo dispuesto por el causante, con lo que se trata más bien de actos de disposición que de partición. La naturaleza de este hecho (dar ejecución a la distribución del caudal hereditario) es de relación contractual, al surgir del acuerdo unánime de las voluntades de los interesados, que se perfecciona con la concurrencia de los requisitos del artículo 1261 del Código Civil, al acomodarse a sus intereses (SS. 3 de enero de 1962, 25 de febrero de 1966, 21 de mayo de 1966, 18 de febrero de 1967, 8 de febrero de 1996 y 12 de noviembre de 1996), sin que sea necesario que afecte a todos los bienes, pues puede proyectarse sobre parte de los mismos, subsistiendo una comunidad hereditaria sobre los restantes o llevarse a cabo la definitiva en su momento, que tendrá en cuenta la parcial precedente, y ésta tiene acceso al Registro de la Propiedad, conforme a los artículos 14 de la Ley Hipotecaria y 80 de su Reglamento. Pero no es tal la situación generada en el caso pues, siendo herederos tanto el actor (…) como su tío, esposo de la demandada, en lugar de efectuar una verdadera partición, total o parcial, realizan algo distinto buscando un resultado antijurídico al amparo de dicha norma, como es atribuir pro indiviso a los primeros (que tienen conjuntamente un derecho a la mitad del caudal hereditario) la propiedad íntegra de la vivienda, excluyendo de todo derecho sobre ella al esposo de la demandada (titular de un derecho a la herencia que representa la mitad restante de la misma) sin siquiera señalar si existen o no otros bienes hereditarios al faltar un inventario de los mismos. Resulta así que, al amparo de una norma de cobertura (artículo 1058 CC), se actúa en perjuicio de quien tiene un derecho sobre un bien (en este caso, la vivienda) que resultaría inatacable si tal bien se hubiera atribuido en la partición a quien lógicamente habría de corresponder, no sólo por ser el mayor partícipe en la herencia sino también por habérsele concedido inicialmente su posesión sin haber sido revocada tal concesión en momento alguno.»

En consecuencia, el Tribunal Supremo rechaza la acción de desahucio por precario.

El caso de la citada sentencia guarda identidad de razón con el actual. En efecto, al otorgar la denominada «escritura de partición parcial de herencia», los comparecientes en dicha escritura realizaron algo distinto, buscando un resultado antijurídico al amparo del art. 1058 CC, como es atribuir al actor (coheredero por iguales partes junto con el excónyuge de mi mandante) la propiedad íntegra de la vivienda, excluyendo de todo derecho sobre ella al esposo/a de mi representada/o (titular de un derecho a la herencia que representa la mitad de la misma) sin siquiera señalar si existen o no otros bienes hereditarios al faltar un inventario de los mismos. Resulta así, al igual que en el caso de la citada sentencia, «que al amparo de una norma de cobertura (artículo 1058 CC) se actúa en perjuicio de quien tiene un derecho sobre un bien (en este caso, la vivienda) que resultaría inatacable si tal bien se hubiera atribuido en la partición a quien lógicamente habría de corresponder (…) por habérsele concedido inicialmente su posesión sin haber sido revocada tal concesión en momento alguno».

Por todo ello, debe llegarse a igual solución que en el caso de la STS de 18 de marzo de 2008, rec. 5847/2000, desestimando la acción de desahucio, con expresa imposición de costas, lo cual interesamos, a la vez que solicitamos el recibimiento del pleito a prueba.
