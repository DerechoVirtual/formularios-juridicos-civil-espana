---
name: demanda-contra-declaracion-desamparo-defectos-formales-civ-0175
description: "Demanda contra la declaración de desamparo por defectos formales. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda contra la declaración de desamparo por defectos formales

> Formulario **CIV-0175** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Al Tribunal Comparecencia, representación y asistencia letrada Interposición de demanda de oposición a la declaración de desamparo HECHOS FUNDAMENTOS DE DERECHO Suplico Otrosí digo primero Otrosí digo segundo Otrosí digo tercero Firmas

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda contra la declaración de desamparo por defectos formales» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda contra la declaración de desamparo por defectos formales” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-contra-declaracion-desamparo-defectos-formales-civ-0175`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (9 veces)
- [ ] AÑO (7 veces)
- [ ] DÍA (7 veces)
- [ ] MES (7 veces)
- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] DENOMINACIÓN DEL DEPARTAMENTO (3 veces)
- [ ] NOMBRE DEL MENOR (3 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] COLEGIO
- [ ] LUGAR
- [ ] OTROS DATOS
- [ ] ÓRGANO ADMINISTRATIVO

## Normas que cita el formulario

- art. 779 LEC
- art. 780.2 LEC
- art. 85.1 LOPJ
- art. 749.2 LEC
- art. 750.1 LEC
- art. 780 LEC
- art. 753 LEC
- art. 3.2 LO 1/2025
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

- Junto a «…CIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA NÚMERO DE [LOCALIDAD]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) En virtud de la Ley Orgánica 7/2015, de 21 de julio, por la que se modifica la Ley Orgánica 6/1985, de 1 de julio, del Poder Judicial (BOE de 22 de julio de 2015) los Letrados/as de la Administración de Justicia pasan a ser "Letrados de la Administración de Justicia" con efectos desde el 1 de octubre de 2015.

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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA NÚMERO DE [LOCALIDAD]

D./Dª [NOMBRE Y APELLIDOS], Procurador de los Tribunales y de D./Dª [NOMBRE Y APELLIDOS] y D./Dª [NOMBRE Y APELLIDOS], como padres de D./Dª [NOMBRE Y APELLIDOS], cuya representación acreditará cuando sea requerido para ello mediante comparecencia apud acta, bajo la dirección técnica de D./Dª [NOMBRE Y APELLIDOS], Letrado del Ilustre Colegio de [COLEGIO], ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que por medio del presente escrito, y dentro del plazo de veinte días concedido mediante diligencia de ordenación de fecha [DÍA] de [MES] de [AÑO], mis representados, con base en lo dispuesto en los arts. 779 y 780 LEC, plantean DEMANDA DE OPOSICIÓN A LA RESOLUCIÓN ADMINISTRATIVA dictada en fecha [DÍA] de [MES] de [AÑO] por la Delegación Territorial de [LOCALIDAD] del Departamento de Acción social [DENOMINACIÓN DEL DEPARTAMENTO] de la Comunidad Autónoma de [LOCALIDAD] por la que se declara en situación de desamparo al/a los menor/es [NOMBRE DEL MENOR], conforme a los siguientes

HECHOS

PRIMERO.- D./Dª [NOMBRE Y APELLIDOS] y D./Dª [NOMBRE Y APELLIDOS] son los padres de [NOMBRE DEL MENOR], nacido en [LOCALIDAD], el día [DÍA] de [MES] de [AÑO] y, por tanto, menor de edad. Se acompaña certificación/es de la inscripción/es de nacimiento del/de los menor/es emitida/as por el encargado del Registro Civil de [LOCALIDAD] como Documento/s nº [Nº DE DOCUMENTO] para acreditar este extremo.

SEGUNDO.- La Delegación Territorial de [LOCALIDAD] del Departamento de Acción Social [DENOMINACIÓN DEL DEPARTAMENTO] de la Comunidad Autónoma de [LOCALIDAD] dictó resolución de fecha [DÍA] de [MES] de [AÑO], por la que declaró la situación legal de desamparo del hijo de mis representados, antes citado, y asumió de modo automático su tutela legal, estableciendo un acogimiento familiar para la guarda del menor. Se acompaña como Documento nº [Nº DE DOCUMENTO] testimonio de la citada resolución.

TERCERO.- En fecha de [DÍA] de [MES] de [AÑO], conforme al art. 780.2 LEC, mis representados presentaron ante este Tribunal un escrito inicial en el que sucintamente expresaban su pretensión de oponerse a la declaración de desamparo de su hijo/s efectuada por la resolución antes citada, así como los demás extremos a los que obliga el precepto.

CUARTA.- Recibido testimonio completo del expediente administrativo, del que se dio traslado a mis representados, el Letrado de la Administración de Justicia les emplazó para que en el plazo de veinte días presentaran la correspondiente demanda, lo que efectúan mediante el presente escrito.

QUINTO.- En el procedimiento que condujo a la declaración de desamparo del/de los menor/es se omitió el preceptivo trámite de audiencia del/de los mismo/s, que cuenta/n ya con doce años de edad [OTROS DATOS]. Así resulta del testimonio completo del expediente administrativo, que se acompaña como Documento nº [Nº DE DOCUMENTO]

Resultan aplicables a los anteriores hechos, los siguientes

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA.- La competencia corresponde a este Tribunal, conforme al art. 779 LEC, en relación con lo dispuesto en el art. 85.1º LOPJ, que la atribuye al Tribunal de Instancia del domicilio de la entidad protectora.

II.- LEGITIMACIÓN.- Ostentan legitimación activa mis representados, como padres del menor/es declarado/s en desamparo y legitimación pasiva, la entidad pública que dictó la resolución en que se contiene dicha declaración, siendo preceptiva la intervención del Ministerio Fiscal, de acuerdo con el art. 749.2 LEC, por estar interesados en el procedimiento uno o varios menores de edad.

III.- REPRESENTACIÓN Y DEFENSA.- Los demandantes se hallan debidamente representados y asistidos por el Procurador y Letrado señalados al inicio, tal y como exige el art. 750.1 LEC.

V.- PROCEDIMIENTO. Dispone el art. 780 LEC: “1. No será necesaria reclamación previa en vía administrativa para formular oposición, ante los Tribunales civiles, a las resoluciones administrativas en materia de protección de menores. La oposición a las mismas podrá formularse en el plazo de dos meses desde su notificación.

Estarán legitimados para formular oposición a las resoluciones administrativas en materia de protección de menores, siempre que tengan interés legítimo y directo en tal resolución, los menores afectados por la resolución, los progenitores, tutores, acogedores, guardadores, el Ministerio Fiscal y aquellas personas que expresamente la ley les reconozca tal legitimación. Aunque no fueran actores podrán personarse en cualquier momento en el procedimiento, sin que se retrotraigan las actuaciones.

Los menores tendrán derecho a ser parte y a ser oídos en el proceso conforme a lo establecido en la Ley Orgánica de Protección Jurídica del Menor. Ejercitarán sus pretensiones en relación a las resoluciones administrativas que les afecten a través de sus representantes legales siempre que no tengan intereses contrapuestos a los suyos, o a través de la persona que se designe como su defensor para que les represente.

2. El proceso de oposición a una resolución administrativa en materia de protección de menores se iniciará mediante la presentación de un escrito inicial en el que el actor sucintamente expresará la pretensión y la resolución a que se opone.

En el escrito consignará expresamente la fecha de notificación de la resolución administrativa y manifestará si existen procedimientos relativos a ese menor.

3. El Letrado de la Administración de Justicia reclamará a la entidad administrativa un testimonio completo del expediente, que deberá ser aportado en el plazo de veinte días.

4. Recibido el testimonio del expediente administrativo, el Letrado de la Administración de Justicia emplazará al actor por veinte días para que presente la demanda, que se tramitará con arreglo a lo previsto en el artículo 753.

5. Si el Ministerio Fiscal, las partes o el Juez competente tuvieren conocimiento de la existencia de más de un procedimiento de oposición a resoluciones administrativas relativas a la protección de un mismo menor, pedirán los primeros y dispondrá el segundo, incluso de oficio, la acumulación ante el Tribunal que estuviera conociendo del procedimiento más antiguo.

Acordada la acumulación, se procederá según dispone el artículo 84, con la especialidad de que no se suspenderá la vista que ya estuviera señalada si fuera posible tramitar el resto de procesos acumulados dentro del plazo determinado por el señalamiento. En caso contrario, el Letrado de la Administración de Justicia acordará la suspensión del que tuviera la vista ya fijada, hasta que los otros se hallen en el mismo estado, procediendo a realizar el nuevo señalamiento para todos con carácter preferente y, en todo caso, dentro de los diez días siguientes.

Contra el auto que deniegue la acumulación podrán interponerse los recursos de reposición y apelación sin efectos suspensivos. Contra el auto que acuerde la acumulación no se dará recurso alguno.”

El art. 753 LEC, por su parte, se remite a los trámites del juicio verbal, con las especialidades que el mismo precepto establece.

De conformidad con lo dispuesto en el art. 779 de la LEC 1/2000, el procedimiento que se insta tendrá carácter preferente.

Conforme a lo dispuesto en el art. 3.2 LO 1/2025, la presente demanda no está sujeta al requisito de MASC, en cuanto se dirige contra una entidad pública como lo es en este caso [ÓRGANO ADMINISTRATIVO].

VI. DERECHO SUSTANTIVO.- La Carta Europea de Derechos del Niño de 8 de julio de 1992 (Resolución del Parlamento Europeo A3-0772/92), art. 8.14, establece el derecho del menor a ser oído, siempre que ello no implique riesgo o perjuicio alguno para el niño, desde el momento en que su madurez y edad lo permitan en todas las decisiones que le afecten, especialmente en todos aquellos procedimientos que impliquen la modificación del ejercicio de la patria potestad, la determinación de la guarda y custodia, la designación de su tutor legal, su entrega en adopción o su eventual colocación en una institución familiar, educativa o con fines de reinserción social.

PPor su parte, la Ley Orgánica 1/1996, en su art. 9 regula el derecho a la audiencia del menor, reiterando lo dispuesto en el art. 12 de la Convención de las Naciones Unidas sobre Derechos del Niño, de 20 de noviembre de 1989, ratificada por España el 30 de noviembre de 1990, garantizando, de este modo, la participación del menor en cualquier proceso que le afecte. El precepto, según redacción por LO 8/2015, de 22 de julio, dispone: “1. El menor tiene derecho a ser oído y escuchado sin discriminación alguna por edad, discapacidad o cualquier otra circunstancia, tanto en el ámbito familiar como en cualquier procedimiento administrativo, judicial o de mediación en que esté afectado y que conduzca a una decisión que incida en su esfera personal, familiar o social, teniéndose debidamente en cuenta sus opiniones, en función de su edad y madurez. Para ello, el menor deberá recibir la información que le permita el ejercicio de este derecho en un lenguaje comprensible, en formatos accesibles y adaptados a sus circunstancias.

En los procedimientos judiciales o administrativos, las comparecencias o audiencias del menor tendrán carácter preferente, y se realizarán de forma adecuada a su situación y desarrollo evolutivo, con la asistencia, si fuera necesario, de profesionales cualificados o expertos, cuidando preservar su intimidad y utilizando un lenguaje que sea comprensible para él, en formatos accesibles y adaptados a sus circunstancias informándole tanto de lo que se le pregunta como de las consecuencias de su opinión, con pleno respeto a todas las garantías del procedimiento.

2. Se garantizará que el menor, cuando tenga suficiente madurez, pueda ejercitar este derecho por sí mismo o a través de la persona que designe para que le represente. La madurez habrá de valorarse por personal especializado, teniendo en cuenta tanto el desarrollo evolutivo del menor como su capacidad para comprender y evaluar el asunto concreto a tratar en cada caso. Se considera, en todo caso, que tiene suficiente madurez cuando tenga doce años cumplidos.

Para garantizar que el menor pueda ejercitar este derecho por sí mismo será asistido, en su caso, por intérpretes. El menor podrá expresar su opinión verbalmente o a través de formas no verbales de comunicación.

No obstante, cuando ello no sea posible o no convenga al interés del menor se podrá conocer la opinión del menor por medio de sus representantes legales, siempre que no tengan intereses contrapuestos a los suyos, o a través de otras personas que, por su profesión o relación de especial confianza con él, puedan transmitirla objetivamente.

3. Siempre que en vía administrativa o judicial se deniegue la comparecencia o audiencia de los menores directamente o por medio de persona que le represente, la resolución será motivada en el interés superior del menor y comunicada al Ministerio Fiscal, al menor y, en su caso, a su representante, indicando explícitamente los recursos existentes contra tal decisión. En las resoluciones sobre el fondo habrá de hacerse constar, en su caso, el resultado de la audiencia al menor, así como su valoración”.

La audiencia del menor, constituye una obligación para la autoridad administrativa que ha de decidir sobre su declaración de desamparo, sin perjuicio de que la opinión de aquél no resulte vinculante.

En el procedimiento que finalizó con la resolución que se impugna se omitió totalmente este fundamental trámite.

VII.- COSTAS.- Procede imponer las costas a la entidad pública demandada, conforme al art. 394 LEC, de cuya aplicación no está exenta.

VIII.- Iura novit curia y los demás que en Derecho procedan.

En su virtud:

SUPLICO AL TRIBUNAL: Que teniendo por presentado este escrito en tiempo y forma con los documentos que se acompañan y sus copias, se sirva admitirlo, tenga por interpuesta DEMANDA DE OPOSICIÓN A LA DECLARACIÓN DE DESAMPARO DEL/DE LOS MENOR/ES [NOMBRE DEL MENOR] efectuada por resolución de fecha [DÍA] de [MES] de [AÑO] de la Delegación Territorial de [LOCALIDAD] del Departamento de Acción Social [DENOMINACIÓN DEL DEPARTAMENTO] de la Comunidad Autónoma de [LOCALIDAD] y, estimando lo que en él se solicita y previos los trámites legales oportunos, declare nula y sin efecto la citada resolución, por incumplimiento del obligado trámite de audiencia del menor y acuerde la entrega inmediata de los menores a sus padres.

OTROSÍ DIGO: Para acreditar los HECHOS de este escrito, se acompaña los siguientes DOCUMENTOS:

OTROSÍ DIGO: La cuantía del procedimiento resulta inestimable, por carecer su objeto de interés económico.

OOTROSÍ DIGO: Intereso que se deje testimonio en autos de la copia de poder de representación para pleitos que acompaño y se me devuelva, por necesitarla para otros usos.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma y número del Letrado	Firma del Procurador
