---
name: solicitud-revision-jurisdiccion-voluntaria-medidas-civ-0400
description: "Solicitud de revisión en jurisdicción voluntaria de las medidas de apoyo a persona con discapacidad. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de revisión en jurisdicción voluntaria de las medidas de apoyo a persona con discapacidad

> Formulario **CIV-0400** del plugin **Discapacidad y medidas de apoyo (Ley 8/2021)** (`formularios-discapacidad-y-medidas-de-apoyo`) · Civil › Capacidad y medidas de apoyo · normativa revisada el 24-11-2026.

## Qué es

Solicitud de revisión de resolución de medidas judiciales de apoyo a persona con discapacidad, solicitando que quede sujeto a la curatela del actual curador, con límite para la capacidad de obrar exclusivamente en cuanto a la administración de sus bienes.

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de revisión en jurisdicción voluntaria de las medidas de apoyo a persona con discapacidad» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de revisión en jurisdicción voluntaria de las medidas de apoyo a persona con discapacidad” para mi caso». También puedes invocarla directamente con `/formularios-discapacidad-y-medidas-de-apoyo:solicitud-revision-jurisdiccion-voluntaria-medidas-civ-0400`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-discapacidad-y-medidas-de-apoyo:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Discapacidad y medidas de apoyo (Ley 8/2021)) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] CALLE (2 veces)
- [ ] FECHA (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] SEDE (2 veces)
- [ ] COLEGIO
- [ ] LUGAR
- [ ] Nº
- [ ] Nº DE COLEGIADO/A
- [ ] NÚMERO
- [ ] TIPO Y Nº DE PROCEDIMIENTO

## Normas que cita el formulario

- art. 42 bis.c LJV
- art. 268.I CC
- art. 42 bis c) LJV
- art. 268 CC
- art. 3 LJV
- art. 4 LJV

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

- Junto a «…MILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.
- Junto a «…guidos ante la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], con domicilio en esta ciudad, c/ [CALLE], nº [NÚMERO], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño a este escrito, bajo dirección de la Letrado/a D./Dña. [NOMBRE Y APELLIDOS], colegiada nº [Nº DE COLEGIADO/A] del Iltre. Colegio de Abogados de [COLEGIO], cuyo despacho se abre en [LOCALIDAD], calle [CALLE], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que en la representación acreditada, promuevo EXPEDIENTE DE JURISDICCIÓN VOLUNTARIA para la REVISIÓN DE MEDIDAS JUDICIALES DE APOYO de D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con residencia en el mismo domicilio, sometido a curatela de mi mandante, todo ello al amparo de lo dispuesto en el art. 42 bis.c) LJV y en base a los siguientes:

Hechos y consideraciones jurídicas:

1º) En virtud de auto firme de fecha [FECHA] dictado en los autos [TIPO Y Nº DE PROCEDIMIENTO] seguidos ante la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº] se declaró que D./Dña. [NOMBRE Y APELLIDOS], padecía una esquizofrenia de tipo residual (295.6 x), según criterios diagnósticos de la DSM -III-R, de carácter permanente, que disminuye moderadamente sus facultades intelectivas y volitivas por ser trastorno de inicio temprano y de curso muy prolongado, pero que se encuentra en franca fase de remisión terapeútica.

En el citado auto se fijaba un plazo de tres años para la revisión de las medidas. Acompaño como documento nº testimonio del auto con expresión de su firmeza.

En su día, cuando se produjo el proceso primitivo de adopción de medidas judiciales de apoyo, la disminución cognitiva se acrecentaba por un trastorno de la esfera afectiva (pérdida de interés por lo ambiental) que le convertiría en víctima fácil de sugestiones expoliadoras.

Se adjunta el dictamen médico forense emitido en los precitados autos como documento nº [Nº DE DOCUMENTO].

2º) En el informe médico del psiquiatra del centro de salud de [LOCALIDAD], que ha venido atendiendo al discapacitado estos últimos tres años (DOCUMENTO Nº [Nº DE DOCUMENTO] de los unidos a esta demanda), se coincide en el diagnóstico de esquizofrenia residual, pero se deja constancia de que las descompensaciones reactivas a situaciones desfavorables del entorno familiar han desaparecido absolutamente, siendo tales las que motivaron las catorce hospitalizaciones que ha sufrido el discapacitado a lo largo de quince años previos a la adopción de las medidas judiciales de apoyo en el Hospital psiquiátrico de [LOCALIDAD], fruto de un ambiente sociofamiliar que ya no le afecta.

3º) Si se repasa el proceso de adopción de medidas judiciales de apoyo, la conclusión de inhabilidad para regir sobre su persona y bienes, más que médico-legal, fue suma del examen de los parientes próximos, calificadamente su hermana, de que se precisara una medicación constante, muy peligrosa si se tomara con descontrol, y del examen judicial, por las mismas manifestaciones del sujeto a curatela, que asumió su discapacidad, de modo que toda su fijación se centraba, de una lado en el estado del caserío donde vivía, y de otra en los ingresos hospitalarios que le han sido desdichadamente tan frecuentes.

4º) Esta parte está en condiciones de demostrar que, actualmente, lo que ya se documenta médicamente como una situación de regresión estable de la enfermedad mental, desde el punto de vista de la socialización y de recuperación de autoestima y facultades de gobierno personales autorizarán, al examen judicial, una decisión de deseable limitación de la privación que pesa sobre D./Dña. [NOMBRE Y APELLIDOS] en el entero de su capacidad de obrar; de manera que aun no habiendo transcurrido el plazo de revisión de las medidas de apoyo, se está en el caso de solicitar su revisión conforme a lo establecido en el art. 268.III CCiv y en el art. 42 bis c).1 LJV.

5º) El art. 42 bis c).2 LJV establece que el Tribunal que dictó las medidas será también competente para conocer de la citada revisión, siempre que la persona con discapacidad permanezca residiendo en la misma circunscripción. En caso contrario, el Tribunal de la nueva residencia habrá de pedir un testimonio completo del expediente al Tribunal que anteriormente conoció del mismo, que lo remitirá en los diez días siguientes a la solicitud.

6º) El procedimiento a seguir en el presente supuesto es el de jurisdicción voluntaria, regulado en el art. 42 bis c) LJV, debiendo darse traslado a quien ejerza las funciones de apoyo, al Ministerio Fiscal y a los interesados personados en el expediente previo.

7º) Está legitimado activamente el promotor del expediente conforme a lo establecido en el art. 42 bis c).1 LJV, cuando dispone: “cualquiera de las personas mencionadas en el apartado 3 del artículo 42 bis a), así como quien ejerza el apoyo, podrá solicitar la revisión de las medidas antes de que transcurra el plazo previsto en el auto”. Por su parte, el art. 42 bis a).3 LJV:" Podrá promover este expediente el Ministerio Fiscal, la propia persona con discapacidad, su cónyuge no separado de hecho o legalmente o quien se encuentre en una situación de hecho asimilable y sus descendientes, ascendientes o hermanos”.

8º) El art. 268 CCiv establece que las medidas tomadas por la autoridad judicial en el procedimiento de provisión de apoyos serán proporcionadas a las necesidades de la persona que las precise, respetarán siempre la máxima autonomía de esta en el ejercicio de su capacidad jurídica y atenderán en todo caso a su voluntad, deseos y preferencias y que se revisarán, en todo caso, ante cualquier cambio en la situación de la persona que pueda requerir una modificación de dichas medidas.

9º) Que conforme a lo dispuesto en el art. 3 LJV la solicitud está firmada por abogado y procurador, pese a que su intervención no es preceptiva en el caso de autos.

10º) Que conforme a los art. 4 LJV la tramitación del expediente se practicará con intervención del Ministerio Fiscal.

11º)

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito, con sus documentos y copias, lo admita a trámite, teniéndome por comparecido y parte en la representación que ostento, se sirva iniciar expediente de JURISDICCIÓN VOLUNTARIA DE REVISIÓN DE MEDIDAS JUDICIALES DE APOYO de D./Dña. [NOMBRE Y APELLIDOS], y seguido que sea el oportuno procedimiento, tras los trámites legales una vez recabados los informes que V.I. estime oportunos, se dicte auto, por el que se se declare modificado el alcance de actos sujetos a asistencia del curador de D./Dña. [NOMBRE Y APELLIDOS], determinándose que quede sujeto a la curatela del actual tutor D./Dña. [NOMBRE Y APELLIDOS], con límite para la capacidad de obrar exclusivamente en cuanto a la administración de sus bienes, y salvo en cuanto a pequeño peculio de dinero efectivo, pero sin límite en el autogobierno personal.

Y para aseguramiento y constancia se mande inscribir la parte dispositiva de la sentencia estimatoria en el Registro Civil.

Es justicia que pido en [LUGAR], a [FECHA].

OTROSÍ DIGO: que se acompaña en anexo relación de documentos e informes presentados, debidamente foliados y con índice electrónico, para su debida localización y consulta.

Por lo que,

SUPLICO AL TRIBUNAL tenga hecha esta manifestación a los efectos oportunos y por aportados los documentos e informe pericial relacionados en el anexo.

Reitero Justicia en lugar y fecha ‘ut supra’.

Firma del Abogado/a	Firma del Procurador/a

========================================================================
