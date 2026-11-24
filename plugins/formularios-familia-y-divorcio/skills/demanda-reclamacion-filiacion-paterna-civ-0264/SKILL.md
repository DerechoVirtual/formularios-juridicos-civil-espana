---
name: demanda-reclamacion-filiacion-paterna-civ-0264
description: "Demanda de reclamación de filiación paterna. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de reclamación de filiación paterna

> Formulario **CIV-0264** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de reclamación de filiación paterna» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de reclamación de filiación paterna” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-reclamacion-filiacion-paterna-civ-0264`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (15 veces)
- [ ] FECHA (7 veces)
- [ ] LOCALIDAD (7 veces)
- [ ] AÑO (4 veces)
- [ ] MES (4 veces)
- [ ] CALLE (2 veces)
- [ ] ENTIDAD BANCARIA (2 veces)
- [ ] Nº (2 veces)
- [ ] PISO (2 veces)
- [ ] PUERTA (2 veces)
- [ ] LUGAR Y FECHA
- [ ] Nº DE DOCUMENTO
- [ ] SEDE

## Normas que cita el formulario

- art. 133.1 Código Civil
- art. 764.1 LEC
- art. 765 LEC
- art. 766 LEC
- art. 749.1 LEC
- art. 50 LEC
- art. 753 LEC
- art. 405 LEC
- art. 752.1 LEC
- art. 767.1 LEC
- art. 5.2 Ley Orgánica 1/2025
- art. 120.4 Código Civil
- art. 767 LEC
- art. 767.4 LEC
- art. 767.3 LEC
- art. 111.2 Código Civil
- art. 113 Código Civil
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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…NCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.R.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.R.C.

Don [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en nombre y representación que ostento de Doña [NOMBRE Y APELLIDOS], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], y bajo la dirección Letrada de Don [NOMBRE Y APELLIDOS], ante el Tribunal de Instancia que por turno de reparto corresponda comparezco y, como mejor proceda en Derecho, DIGO:

Que a través del presente escrito, y en virtud de la representación conferida, interpongo demanda en juicio declarativo especial por la que ejercito acción de RECLAMACIÓN DE FILIACIÓN PATERNA EXTRAMATRIMONIAL, sin existencia de posesión de estado, en contra de Don [NOMBRE Y APELLIDOS], vecino de la localidad de [LOCALIDAD], con domicilio en calle [CALLE], núm. [Nº], piso [PISO], puerta [PUERTA], la cual baso en los siguientes

HECHOS

PRIMERO.- Sobre la convivencia de la madre de mi representado con el demandado, Don [NOMBRE Y APELLIDOS], goza de abundante prueba, que una vez practicada en el acto de la vista oral demostrará que desde [FECHA] ambos litigantes decidieron formar una vida en común en el domicilio sito en la calle [CALLE], núm. [Nº], piso [PISO], puerta [PUERTA], de la localidad de [LOCALIDAD]. Esta vivienda fue arrendada a la pareja, que firmaron un contrato documentado en la Cámara de la Propiedad urbana de [LOCALIDAD], que acompaño como documento núm. uno. Para abonar las facturas corrientes y el mismo arriendo, se utilizó una cuenta abierta en la entidad financiera [ENTIDAD BANCARIA], donde figuraron durante cinco años los nombres del demandante y la demandada, que acompaño como documento núm. dos. Asimismo, en fecha [FECHA], ambos se inscribieron en el correspondiente padrón municipal, que acompaño como documento núm. tres.

. Mi representada, Doña [NOMBRE Y APELLIDOS], madre de Don [NOMBRE Y APELLIDOS] según consta en el Registro Civil de [LOCALIDAD] y acredito mediante certificado literal del citado Registro que acompaño como documento núm. uno, mantuvo relaciones maritales con el demandado desde varios años antes del nacimiento del citado niño, que tuvo lugar el día [FECHA], del mes [MES], del año [AÑO]. De esto es prueba el domicilio en común en el que vivían demandante y demandado en esas fechas, vendido recientemente, por medio de escritura pública que se aporta a los autos como documento núm. dos, y el empadronamiento en una misma dirección durante todo ese tiempo, aportando en prueba de lo manifestado certificado de empadronamiento del Ayuntamiento como documento núm. tres. Por diferencias entre las partes se produjo una ruptura de la relación sentimental que motivó el cambio de la vivienda.

SEGUNDO.- Que el día [FECHA], del mes [MES], del año [AÑO], tuvo lugar el nacimiento de mi mandante, siendo inscrito en el Registro Civil de [LOCALIDAD], según es de ver la certificación literal de mencionado Registro que acompaño como documento núm. cuatro. Un mes después su madre decidió abandonar el domicilio común, en concreto el día [FECHA], del mes [MES], del año [AÑO], puesto que la vida en pareja no funcionaba en absoluto. El desempleo de ambos progenitores había obligado a pedir ayuda a los abuelos maternos del demandante, como en su momento podrán testificar. Pero además indicar que el demandado afirmó desde el embarazo que el bebé no era suyo, motivo que impidió la inscripción paterna en el Registro Civil, siendo continuos los ataques de celos que provocaban discusiones interminables en el domicilio, y que pueden atestiguar numerosos vecinos.

Una vez el hijo de mi representada cumplió la edad de dos años, fue abierta a su nombre una cuenta de ahorro en la entidad financiera [ENTIDAD BANCARIA], tal como acredito con documento núm. cuatro que acompaño, en la que también figuró como titular el hoy demandado Don [NOMBRE Y APELLIDOS], quien ha realizado ingresos periódicos en dicha cuenta, aunque de pequeñas cantidades, hasta el día [FECHA], del mes [MES], del año [AÑO]. A su vez, los gastos escolares han sido pagados por mitad por el demandado, que también ha venido abonando un pago mensual para contribuir a la manutención del menor, desde que se separó de la madre de éste y hasta fechas recientes. Además, el tratamiento dispensado se equipara al de un hijo, como pueden atestiguar tanto los abuelos maternos como los padres del demandado, y también vecinos del actual domicilio en el que vive el menor con su madre. Se aporta con la demanda un acta notarial de manifestaciones a instancia de la actora, donde los testigos Don [NOMBRE Y APELLIDOS], Doña [NOMBRE Y APELLIDOS] declaran que a todos les consta que, en fecha [FECHA], el demandado mantenía relaciones de pareja, de un modo exclusivo, con la actora en esta causa. Asimismo, testigos sin sospecha de parcialidad, podrán asegurar que el demandado visitaba diariamente al hijo, estando presente el día de su bautizo y el de su comunión. Como es de ver, la posesión de estado es perfectamente compatible con el período de embarazo de mi representada.

TERCERO.- Que a los efectos de audiencia, se relacionan a continuación las personas aludidas y sus domicilios: Don [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], Doña [NOMBRE Y APELLIDOS] con domicilio en [LOCALIDAD]. A su vez, considera esta parte que la práctica de la prueba biológica permitiría determinar sin género de dudas la paternidad del demandado con respecto al demandante.

FUNDAMENTOS JURÍDICOS

I.- Legitimación. De conformidad con el artículo 133.1 del Código Civil en la nueva redacción dada por la Ley 8/2021, de 2 de junio, al amparo del artículo 764.1 de la LEC, la legitimación activa sólo pertenece al hijo en los casos de filiación extramatrimonial donde no exista posesión de estado, y se trata de una acción de reclamación ejercitable durante toda la vida:

1. La acción de reclamación de filiación no matrimonial, cuando falte la respectiva posesión de estado, corresponderá al hijo durante toda su vida.

Si el hijo falleciere antes de transcurrir cuatro años desde que alcanzare la mayoría de edad o desde que se eliminaren las medidas de apoyo que tuviera previstas a tales efectos, o durante el año siguiente al descubrimiento de las pruebas en que se funde la demanda, su acción corresponderá a sus herederos por el tiempo que faltare para completar dichos plazos.

Por su parte, el artículo 765 de la LEC en la nueva redacción dada por la Ley 8/2021, de 2 de junio dispone:

“Las acciones de determinación o de impugnación de la filiación que, conforme a lo dispuesto en la legislación civil, correspondan al hijo menor de edad, podrán ser ejercitadas por su representante legal o por el Ministerio Fiscal, indistintamente”.

De conformidad con el artículo 766 de la LEC, se atribuye la legitimación pasiva a quienes ostenten la condición de progenitores. En este caso debe considerarse legitimado pasivo a Don [NOMBRE Y APELLIDOS], puesto que la demanda le atribuye la paternidad de nuestro representado, paternidad que no reconoce.

Asimismo, es preceptiva la intervención del Ministerio Fiscal, en virtud de los artículos 749.1 de la LEC y 3.6 de su Estatuto orgánico.

II. Competencia. Las acciones ejercidas sobre filiación hacen competente objetivo al tribunal de instancia, según el artículo 85.1º de la Ley Orgánica del Poder Judicial y el artículo 45 de la Ley de Enjuiciamiento Civil.

La competencia territorial, por su parte, se atribuye aplicando el fuero general de las personas físicas, señalado en los apartados primero y segundo del artículo 50 de la LEC, que como regla general establece el domicilio del demandado.

III. Procedimiento. En lo que hace referencia al procedimiento es de aplicación el artículo 753 de la LEC, que establece el cauce procesal del juicio verbal, si bien bajo la exigencia de una contestación a la demanda regulada en el artículo 405 de la LEC, y permitiendo que los hechos que llevarán a la decisión judicial sean introducidos en el proceso en cualquier momento y de manera distinta a la habitual, según el artículo 752.1 de la LEC, siempre que se lleguen a debatir en contradicción.

Y ello con las especialidades del artículo 767.1 LEC que se analizarán más adelante.

IV. Cumplimiento de los requisitos de procedibilidad. La presente demanda no está sujeta al previo intento de resolución de controversias en vía no jurisdiccional por tratarse de materias excluidas del requisito de procedibilidad de acuerdo con el art. 5.2 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

V.Filiación no matrimonial. La filiación no matrimonial quedará determinada legalmente por sentencia firme, tal como indica el artículo 120.4 del Código Civil.

VI. Especialidades en materia de procedimiento y prueba.

Dispone el artículo 767 LEC:

1. En ningún caso se admitirá la demanda sobre determinación o impugnación de la filiación si con ella no se presenta un principio de prueba de los hechos en que se funde.

2. En los juicios sobre filiación será admisible la investigación de la paternidad y de la maternidad mediante toda clase de pruebas, incluidas las biológicas.

3. Aunque no haya prueba directa, podrá declararse la filiación que resulte del reconocimiento expreso o tácito, de la posesión de estado, de la convivencia con la madre en la época de la concepción, o de otros hechos de los que se infiera la filiación, de modo análogo. 4. La negativa injustificada a someterse a la prueba biológica de paternidad o maternidad permitirá al tribunal declarar la filiación reclamada, siempre que existan otros indicios de la paternidad o maternidad y la prueba de ésta no se haya obtenido por otros medios.

En virtud del apartado segundo del artículo 767 de la LEC, en los juicios sobre filiación será admisible la investigación de la paternidad mediante toda clase de pruebas, incluidas las biológicas, tal como ya señala el artículo 39.2 de la Constitución. Junto al resto de prueba presentada, la negativa injustificada del demandado a someterse al examen médico biológico podría considerarse una presunción a favor de las pretensiones de la actora, por virtud del artículo 767.4 de la LEC, puesto que el resto de datos ofrecidos conformarían indicios suficientes para apoyar un resultado probatorio.

Por su parte, el artículo 767.3 de la LEC indica que, incluso sin una prueba directa podrá declararse la filiación que resulte del reconocimiento tácito, la convivencia con la madre en la época de la concepción, o de otros hechos de los que se infiera filiación, de modo análogo. En definitiva, se trata de determinar judicialmente que el demandado es el padre biológico de mi representado, generándose entre ambos un vínculo jurídico recíproco, a la postre paterno filial, acorde con el lazo de sangre o natural ya existente. Ello no obstante, establece el artículo 111.2ºdel Código Civil que el demandado deberá ser excluido de la patria potestad y demás funciones tuitivas, y no ostentará derechos por ministerio de la Ley respecto del hijo o sus descendientes, o en sus herencias, cuando la filiación haya sido judicialmente determinada contra su oposición, quedando a salvo las obligaciones del progenitor en cuanto a velar por los hijos y prestarles alimentos.

Por su parte, el artículo 113 del Código Civil indica que, a falta de otros medios de prueba, la filiación puede acreditarse por la posesión de estado. Es decir, la apariencia fáctica y social del estado de filiación pretendido, que se plasma con una ininterrumpida, continua y pública relación de nomen, tractatus y fama.

VII. Costas. En cuanto a las costas es de aplicación artículo 394 de la LEC.

VIII. Demás normas concordantes y de aplicación: Iura novit Curia.

Por lo expuesto,

SOLICITO AL TRIBUNAL: Que tenga por presentado este escrito con los documentos acompañados y sus copias; admita todo ello; y por promovido por el Procurador que suscribe, con quien se entiendan las sucesivas diligencias, en nombre y representación de Don [NOMBRE Y APELLIDOS], con devolución de la escritura de poderes una vez quede testimonio en autos, JUICIO ESPECIAL DE DETERMINACIÓN DE FILIACIÓN PATERNA contra Don [NOMBRE Y APELLIDOS]; y que previa práctica de la prueba presentada, se dicte sentencia que declare la filiación pretendida, comunicando la resolución judicial firme al Registro Civil y otros Registros públicos que correspondan, a fin de ordenar que tras el nombre de mi representado figure el primer apellido del demandado, realizando cualquier otra rectificación que sea necesaria en el acta de nacimiento; y que al mismo tiempo, que se excluya de la patria potestad, demás funciones tuitivas y derechos relacionados con el menor o sus descendientes, o sobre sus herencias, si la determinación de la filiación se verificase contra la oposición del demandado, imponiendo las costas procesales a este último, con expresa declaración de temeridad y mala fe.

Es Justicia que insto en [LUGAR Y FECHA]

Firmas de Letrado y Procurador.

========================================================================
