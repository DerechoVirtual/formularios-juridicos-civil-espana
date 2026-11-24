---
name: demanda-contenciosa-revision-medidas-judiciales-apoyo-civ-0398
description: "Demanda contenciosa de revisión de las medidas judiciales de apoyo a persona con discapacidad. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda contenciosa de revisión de las medidas judiciales de apoyo a persona con discapacidad

> Formulario **CIV-0398** del plugin **Discapacidad y medidas de apoyo (Ley 8/2021)** (`formularios-discapacidad-y-medidas-de-apoyo`) · Civil › Capacidad y medidas de apoyo · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio declarativo especial sobre reintegración de capacidad o modificación de la limitación judicial de la misma exclusivamente en cuanto a la administración de sus bienes, conforme a lo previsto en el art. 761 LEC.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda contenciosa de revisión de las medidas judiciales de apoyo a persona con discapacidad» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda contenciosa de revisión de las medidas judiciales de apoyo a persona con discapacidad” para mi caso». También puedes invocarla directamente con `/formularios-discapacidad-y-medidas-de-apoyo:demanda-contenciosa-revision-medidas-judiciales-apoyo-civ-0398`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-discapacidad-y-medidas-de-apoyo:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Discapacidad y medidas de apoyo (Ley 8/2021)) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (11 veces)
- [ ] FECHA (5 veces)
- [ ] Nº DE DOCUMENTO (4 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] CALLE
- [ ] COLEGIO
- [ ] LUGAR
- [ ] Nº DE COLEGIADO/A
- [ ] Nº DE EXPEDIENTE
- [ ] SEDE

## Normas que cita el formulario

- art. 761 LEC
- art. 756.2 LEC
- art. 753 LEC
- art. 6.1.1 LEC
- art. 7.2 LEC
- art. 23 LEC
- art. 757.1 LEC
- art. 268 CC
- art. 291 CC
- art. 759 LEC

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
- Junto a «…rador/a ========================================================================»: requisito de procedibilidad del art. 5 LO 1/2025 — antes de presentar la demanda hay que intentar un medio adecuado de solución de controversias (MASC) y acreditarlo con la demanda (arts. 264.4.º y 399.3 LEC), salvo las materias excluidas del art. 5.2. Fuente: LO 1/2025, arts. 5 a 7 (BOE-A-2025-76).

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

D./Dña. [NOMBRE Y APELLIDOS], Procurador de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS], que es el representante legal como tutor de su hermano D./Dña. [NOMBRE Y APELLIDOS], a virtud de poder para pleitos cuya copia acompaño para su unión a los autos mediante testimonio bastante, con ruego de devolución de la copia autorizada por necesitarla a otros usos, bajo dirección del Letrado D./Dña. [NOMBRE Y APELLIDOS], colegiado nº [Nº DE COLEGIADO/A] del Iltre. Colegio de Abogados de [COLEGIO], con despacho abierto en [LOCALIDAD], calle [CALLE], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que por medio del presente escrito, en la representación que ostento, vengo a formular demanda de juicio declarativo especial sobre REVISIÓN DE CAPACIDAD de D./Dña. [NOMBRE Y APELLIDOS], frente al MINISTERIO FISCAL, con base a los siguientes datos de hecho y argumentos jurídicos:

HECHOS

PRIMERO.- En virtud de sentencia firme de fecha [FECHA], dictada en autos nº [Nº DE PROCEDIMIENTO] / seguidos por ese Tribunal de Instancia, se nombró curador de su hermano D./Dña. [NOMBRE Y APELLIDOS] a mi representado, quien asumía facultades plenas de representación de la persona con discapacidad para todos los actos de gestión, administración y disposición de su patrimonio.

En el citado auto se fijaba un plazo de tres años para la revisión de las medidas, a cuya acreditación acompaño como documento nº [Nº DE DOCUMENTO] testimonio del mismo con expresión de su firmeza.

SEGUNDO.- El discapacitado padece una esquizofrenia de tipo residual (295.6 x), según criterios diagnósticos de la DSM -III-R, de carácter permanente, que disminuye moderadamente sus facultades intelectivas y volitivas por ser trastorno de inicio temprano y de curso muy prolongado, pero que se encuentra en franca fase de remisión terapeútica.

En su día, cuando se produjo el proceso primitivo de adopción judicial de medidas de apoyo, la disminución cognitiva se acrecentaba por un trastorno de la esfera afectiva (pérdida de interés por lo ambiental) que le convertiría en víctima fácil de sugestiones expoliadoras.

Se adjunta el dictamen médico forense emitido en los precitados autos como documento nº [Nº DE DOCUMENTO].

TERCERO.- En el informe médico del psiquiatra del centro de salud de [LOCALIDAD], que ha venido atendiendo al discapacitado estos últimos tres años (documento nº [Nº DE DOCUMENTO] de los unidos a esta demanda), se coincide en el diagnóstico de esquizofrenia residual, pero se deja constancia de que las descompensaciones reactivas a situaciones desfavorables del entorno familiar han desaparecido absolutamente, siendo tales las que motivaron las catorce hospitalizaciones que ha sufrido el tutelado a los largo de quince años previos a ser incapacitado en el Hospital psiquiátrico de [LOCALIDAD], fruto de un ambiente sociofamiliar que ya no le afecta.

CUARTO.- Si se repasa el proceso de de adopción de medidas judiciales de apoyo, la conclusión de inhabilidad para regir sobre su persona y bienes, más que médico-legal, fue suma del examen de los parientes próximos, calificadamente su hermana, de que se precisara una medicación constante, muy peligrosa si se tomara con descontrol, y del examen judicial, por las mismas manifestaciones del tutelado, que asumió su discapacidad, de modo que toda su fijación se centraba, de un lado en el estado del caserío donde vivía, y de otra en los ingresos hospitalarios que le han sido desdichadamente tan frecuentes.

QUINTO.- Con fecha [FECHA] fue promovido expediente de jurisdicción voluntaria para la revisión de medidas judiciales de apoyo de D./Dña [NOMBRE Y APELLIDOS] contra el que se formuló oposición por parte de [NOMBRE Y APELLIDOS] en fecha [FECHA], dando por finalizado el expediente.

Se aporta como documento nº [Nº DE DOCUMENTO] resolución recaída en el citado expediente de jurisdicción voluntaria nº [Nº DE EXPEDIENTE] seguido ante el Tribunal al que me dirijo, cuya incorporación a estos autos se solicitará por medio de otrosí, donde obra asimismo la oposición formulada.

SEXTO.- Esta parte está en condiciones de demostrar que, actualmente, lo que ya se documenta médicamente como una situación de regresión estable de la enfermedad mental, desde el punto de vista de la socialización y de recuperación de autoestima y facultades de gobierno personales autorizarán, al examen judicial, una decisión de reintegración, o cuanto menos una deseable limitación de la privación que pesa sobre D./Dña. [NOMBRE Y APELLIDOS] en el entero de su capacidad de obrar.

En el caso, habiéndose producido oposición en el expediente de jurisdicción voluntaria de revisión, se pondrá fin al expediente mediante auto y se podrá instar la revisión de las medidas conforme a lo previsto en el art. 761 LEC, lo que se hace a medio de la presente demanda.

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA.

Es competente el Tribunal al que me dirijo, de acuerdo con lo establecido en el art. 756.2 LEC, por ser el que conoció del previo expediente de jurisdicción voluntaria.

II.- PROCEDIMIENTO.

La demanda se sustanciará por los trámites del juicio verbal con contestación escrita, que es el declarativo especial en materias de estado civil del Capítulo II del Título I del Libro IV LEC, de conformidad con art. 753 LEC, dada la remisión del art. 761 II LEC.

III.- CAPACIDAD.

Gozando de capacidad para ser parte las personas físicas y el Fiscal (art. 6.1.1º y 6º LEC), declarada la discapacidad plena del pupilo del actor, carece ahora de capacidad procesal o para comparecer en juicio, sino a través de su curador y representante legal (art. 7.2 LEC), tal y como ocurre en este supuesto.

En cualquier caso se requiere la capacidad de postulación, mediante la representación técnica de procurador de los tribunales y la dirección de abogado en ejercicio (arts. 23, 31 y 750 LEC).

IV.- LEGITIMACIÓN.

En virtud del art. 761 II LEC están legitimados para promover el proceso contencioso de revisión las personas mencionadas en el art. 757.1 LEC (la persona interesada, su cónyuge no separado de hecho o legalmente o quien se encuentre en una situación de hecho asimilable, su descendiente, ascendiente o hermano), así como quien ejerza el apoyo de la persona con discapacidad, de modo que mi mandante se encuentra activamente legitimado para el ejercicio de la acción, puesto que es el curador de su hermano.

Tiene legitimación pasiva, extraordinaria por interés público, y en defensa de los intereses del discapacitado y la seguridad jurídica, el Ministerio Fiscal (arts. 749.1 y 758.2 LEC).

V.- FONDO DEL ASUNTO. Pretensión principal y subsidiaria.

El art. 268 CCiv establece que las medidas tomadas por la autoridad judicial en el procedimiento de provisión de apoyos serán proporcionadas a las necesidades de la persona que las precise, respetarán siempre la máxima autonomía de esta en el ejercicio de su capacidad jurídica y atenderán en todo caso a su voluntad, deseos y preferencias y que se revisarán, en todo caso, ante cualquier cambio en la situación de la persona que pueda requerir una modificación de dichas medidas. Por su parte, el art. 291 CCiv establece que la curatela se extingue por resolución judicial cuando ya no sea precisa esta medida de apoyo o cuando se adopte una forma de apoyo más adecuada para la persona sometida a curatela.

Expresamente viene determinada en el art. 761 I LEC la posibilidad de revisión las medidas de apoyo judicialmente adoptadas por sentencia y la modificación de su alcance, de conformidad con lo previsto en la legislación civil, mediante la plena pérdida de efectos o mediante la rectificación de los límites de la capacidad, lo que se acostumbra describir como eficacia limitada temporalmente de la cosa juzgada en este género de procesos, aunque más bien se trata de que la pretensión de adopción de medidas de apoyo es una, y la de recuperación, o la de modificación de los límites de la discapacidad otra distinta, fundada en hechos relevantes posteriores, por lo que no existe genuina identidad objetiva.

Nos remitimos al contenido de los informes médicos aportados y a lo que en período probatorio quedare fijado, a través del empleo de la prueba preceptiva que ordena el art. 759 LEC, de examen judicial de la persona afectada, audiencia de parientes próximos, y dictamen facultativo, a fin de constatar la positiva evolución experimentada por [NOMBRE Y APELLIDOS], que le permite actualmente cuidar y controlar su persona.

Siempre ha de tenerse presente que el proceso sobre provisión de medidas judiciales de apoyo a personas con discapacidad presenta unos caracteres especiales que lo distancian notablemente de los demás procesos civiles, pues aparte de repudiar en gran medida el principio dispositivo, rehúye la verdad formal para desplazarse a la persecución de la verdad material, con la obligada adscripción al principio de libertad en materia de pruebas, y elusión de formalismos enervantes.

Conforme a lo previsto en el art. 761 LEC, se postula en primer lugar, la reintegración de la plena capacidad de D./Dña. [NOMBRE Y APELLIDOS], que supone la extinción de la tutela conforme al citado art. 291 CCiv, y subsidiariamente, la modificación de la declaración de discapacidad, estableciendo un régimen de curatela referido exclusivamente a la administración de los bienes, con arreglo a los arts. 268 y ss. CCiv.

VI.- PUBLICIDAD. Pretensión accesoria.

Conforme al art. 4.11º LRC 20/2011, la resoluciones judiciales dictadas en procedimientos de provisión de medidas judiciales de apoyo a personas con discapacidad son inscribibles en el Registro Civil por cuanto se refieren a la identidad, estado civil y demás circunstancias de la persona.

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentada esta demanda, con sus documentos y copias, la admita a trámite, teniéndome por comparecido y parte en la representación que ostento, se sirva tener por interpuesta demanda de reintegración de la capacidad, o modificación de la limitación judicial de la misma, seguido que sea el oportuno procedimiento, se dicte sentencia, por la que se acuerde la revisión de las medidas decretadas en sentencia de fecha [FECHA], disponiendo la extinción de la curatela o, subsidiariamente, la limitación de los actos sujetos a asistencia del curador, con límite para la capacidad de obrar exclusivamente en cuanto a la administración de sus bienes, y salvo en cuanto a pequeño peculio de dinero efectivo, pero sin límite en el autogobierno personal, junto a lo demás que en Derecho proceda.

Y para aseguramiento y constancia se mande inscribir la parte dispositiva de la sentencia estimatoria en el Registro Civil del nacimiento.

Es justicia que pido en [LUGAR], a [FECHA].

OTROSÍ PRIMERO DIGO: que se acompaña en anexo relación de documentos e informes presentados, debidamente foliados y con índice electrónico, para su debida localización y consulta, por lo que

SUPLICO AL TRIBUNAL tenga hecha esta manifestación a los efectos oportunos y por aportados los documentos e informe pericial relacionados en el anexo.

OTROSÍ SEGUNDO DIGO

que solicito que se incorporen íntegramente a este proceso las actuaciones seguidas en el procedimiento de jurisdicción voluntaria nº [Nº DE PROCEDIMIENTO], en expediente de revisión de medidas judiciales de apoyo respecto a la misma persona con discapacidad y que finalizó por oposición de tercero interesado.

Por lo que, nuevamente

SUPLICO AL TRIBUNAL que acuerde de conformidad.

Reitero Justicia en lugar y fecha ‘ut supra’.

Firma del Abogado/a	Firma del Procurador/a

========================================================================
