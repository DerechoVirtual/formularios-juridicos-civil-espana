---
name: escrito-contestacion-demanda-reclamacion-impugnacion-civ-0266
description: "Escrito de contestación a la demanda de reclamación o impugnación de paternidad. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito de contestación a la demanda de reclamación o impugnación de paternidad

> Formulario **CIV-0266** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito de contestación a la demanda de reclamación o impugnación de paternidad» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito de contestación a la demanda de reclamación o impugnación de paternidad” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:escrito-contestacion-demanda-reclamacion-impugnacion-civ-0266`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] FECHA (3 veces)
- [ ] SEDE (3 veces)
- [ ] AÑO
- [ ] DENOMINACIÓN SOCIAL
- [ ] LOCALIDAD
- [ ] LUGAR Y FECHA
- [ ] MES
- [ ] NOMBRE DEL HOSPITAL
- [ ] Nº DE DOCUMENTO

## Normas que cita el formulario

- art. 73.4 LEC
- art. 377.1 LEC
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

### Avisos de actualización (4) — se aplican en el texto, nunca se copian en el documento

- Junto a «…AD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º LOS DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).
- Junto a «…2666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.
- Junto a «…n [NOMBRE Y APELLIDOS] ante la Sección Civil del Tribunal de Instancia de [SEDE]»: Un solo TI por partido judicial (art. 84.1 LOPJ): sobra «de los de». Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º LOS DE [SEDE]

Don [NOMBRE Y APELLIDOS], Procurador de los Tribunales, actuando en nombre y representación de Doña [NOMBRE Y APELLIDOS], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], y bajo la dirección letrada de Don [NOMBRE Y APELLIDOS] ante la Sección Civil del Tribunal de Instancia de [SEDE] que por turno de reparto corresponda [NOMBRE Y APELLIDOS] comparezco y, como mejor proceda en Derecho, DIGO:

Que por medio del presente escrito paso a evacuar en tiempo y forma el trámite conferido en virtud de providencia dictada con fecha [FECHA], notificada el siguiente día [FECHA], CONTESTANDO LA DEMANDA DE RECLAMACIÓN O IMPUGNACIÓN DE PATERNIDAD interpuesta por Don [NOMBRE Y APELLIDOS]; oponiéndome a la misma en base a los siguientes

HECHOS

PRIMERO.- Niego lo hechos expuestos por la parte demandante, salvo aquello expresamente aceptado, dado que no hacen honor a la verdad, igual que ocurre con las deducciones que de ellos se pretenden utilizar.

SEGUNDO.- Que al margen de que el fracaso de la pretensión impide en todo caso examinar una nueva determinación de la filiación, con respecto a los hechos relacionados con las acciones pretendidas, debe comenzarse diciendo que el domicilio indicado como común no lo era en realidad, dado que en todo caso funcionaba como despacho a efectos mercantiles, en tanto los litigantes eran socios de una misma empresa, como prueban los recibos aportados por la adversa, donde figura como pagador la empresa [DENOMINACIÓN SOCIAL], siendo provechoso el empadronamiento en esa misma localidad por motivos rigurosamente empresariales. Acompaño en prueba de lo manifestado Documentos núm. uno a cuatro, en prueba de lo manifestado.

En cuanto a la aseveración de la posesión de estado de esta parte con el demandante, señalar que la investigación privada llevada a cabo por mi representado ofrece conclusiones que en todo caso hacen rechazar un hecho de ese tipo. Antes bien, el menor ha sido desprotegido en otras ocasiones, sin que sea posible afirmar que ha recibido trato de hijo, no ya del demandado, sino de cualquiera.

TERCERO.- En cuanto al rechazo de la prueba biológica propuesta por el demandante, debe manifestarse que este extremo se justificará en los fundamentos jurídicos que a continuación se exponen.

Por otra parte, y a raíz de un reciente análisis de sangre, se dispone de una serie de datos que podrían compararse a los del demandante, si el mismo tiene a bien realizar un examen del ADN, lo que sacaría de dudas al juzgador. Pero si por aquello de las casualidades apareciera coincidencia de esos datos, existe un hecho fundamental que desvirtuaría por completo las pretensiones de la actora, pues esta parte era incapaz para la fecundación en el momento de la concepción del demandante, como constatan los análisis realizados en el Hospital [NOMBRE DEL HOSPITAL], el día [FECHA], del mes [MES], del año [AÑO], prueba menos lesiva para la integridad física de mi representado. Acompaño en prueba de lo manifestado documentos núms. cinco a seis.

A los anteriores Hechos le son de aplicación los siguientes

FUNDAMENTOS JURÍDICOS

I. Competencia. Esta parte no discute las normas procesales indicadas por el demandante en cuanto a la competencia objetiva y territorial del órgano judicial y el procedimiento que debe llevarse a cabo.

En el caso de que se discuta la acumulación de acciones, como cuestión jurídica al margen de la discusión de fondo, se añadiría lo siguiente: Al amparo del artículo 402 de la Ley de Enjuiciamiento Civil, esta parte se opone a la acumulación pretendida, porque entiende que no se cumplen las exigencias procesales de la misma, establecidas en los artículos 71, 72 y 73.1 de la LEC. En consecuencia, deberá resolverse sobre esta materia en la audiencia previa al juicio. En aplicación del artículo 73.4 de la LEC, cuando no quepa la acumulación entre las acciones que se pretendieran mantener por el actor, se concluirá en el archivo de la demanda, sin más trámites. Cuando un precedente rechazo de la acumulación no lo impida, se incorporaría el acuerdo sobre la legitimación activa y pasiva indicada por la actora, si se considera correcto.

II. El principio de prueba que se exige para la admisión de la demanda sólo actúa de control a fin y efecto de impedir demandas caprichosas o claramente infundadas; aunque ésta sea, dicho con el debido respeto y en términos de defensa, la calificación que merecen las peticiones de la actora. En todo caso indicar que el principio de prueba nunca podrá confundirse con la prueba de los hechos que constituyan la pretensión, y que tendrán lugar en el juicio oral.

Por consiguiente, no es posible atribuir ese tipo de eficacia procesal al acta de manifestaciones aportada con el escrito de demanda. Su formación unilateral esquiva la garantía de la contradicción, impidiendo que alcance la categoría de prueba preconstituida. Igualmente se indica la parcialidad de casi todos los testimonios propuestos por el demandante, y de ese modo la necesidad de tachar a la mayoría de los testigos aportados de contrario, en atención al artículo 377.1 de la LEC, en concreto: Don [NOMBRE Y APELLIDOS], Doña [NOMBRE Y APELLIDOS] y Don [NOMBRE Y APELLIDOS]

III. De la prueba propuesta por esta parte se desvirtuarán por completo las pretensiones del demandante.

La negativa de mi representado a la práctica de la prueba biológica solicitada por el actor, tiene su fundamento legal en el artículo 15 de nuestra Carta Magna, en tanto las consecuencias de someterse a una prueba biológica, a la que en ningún caso se siente obligada esta parte porque jamás existieron relaciones sexuales con la madre del demandante en las fechas indicadas, podría causar un daño irreparable en su entorno social y su convivencia patrimonial, sin contar con el perjuicio económico que acarrearía trasladarse al Instituto de Toxicología de [LOCALIDAD]. En cualquier caso, no cabe dar valor ni eficacia a la negativa de someterse a la práctica de la prueba biológica si se declara probada la inexistencia de relaciones sexuales o cohabitación.

IV. Costas. En cuanto a las costas es de aplicación artículo 394 de la LEC.

V. Demás normas concordantes y de aplicación: Iura novit Curia.

Por lo expuesto,

SOLICITO AL TRIBUNAL: Que tras la preceptiva audiencia previa al juicio se rechace por indebida la acumulación de acciones efectuada por el demandante y se archiven las actuaciones. Si ello no ocurre, se solicita que se dicte sentencia de conformidad con este escrito de contestación, rechazando todas las pretensiones de la parte actora, a quien deben imponerse las costas generadas en el presente pleito.

Es Justicia que insto en [LUGAR Y FECHA].

Firmas de Letrado y Procurador.

========================================================================
