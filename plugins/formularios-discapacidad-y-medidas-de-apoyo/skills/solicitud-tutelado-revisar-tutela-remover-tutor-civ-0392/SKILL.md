---
name: solicitud-tutelado-revisar-tutela-remover-tutor-civ-0392
description: "Solicitud del tutelado de revisar la tutela y remover al tutor. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud del tutelado de revisar la tutela y remover al tutor

> Formulario **CIV-0392** del plugin **Discapacidad y medidas de apoyo (Ley 8/2021)** (`formularios-discapacidad-y-medidas-de-apoyo`) · Civil › Capacidad y medidas de apoyo · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud del tutelado de revisar la tutela y remover al tutor» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud del tutelado de revisar la tutela y remover al tutor” para mi caso». También puedes invocarla directamente con `/formularios-discapacidad-y-medidas-de-apoyo:solicitud-tutelado-revisar-tutela-remover-tutor-civ-0392`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-discapacidad-y-medidas-de-apoyo:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Discapacidad y medidas de apoyo (Ley 8/2021)) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (7 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] SEDE (3 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] LUGAR (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] MES
- [ ] NOMBRE DEL CENTRO
- [ ] Nº
- [ ] Nº DE DOCUMENTO
- [ ] NÚMERO
- [ ] PROFESIÓN
- [ ] TIPO Y Nº DE PROCEDIMIENTO

## Normas que cita el formulario

- art. 761 LEC
- art. 291 Código Civil

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

- Junto a «…Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).
- Junto a «…2666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.

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

Procedimiento

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D/Dª [NOMBRE Y APELLIDOS] Procurador de los Tribunales actuando en nombre y representación de D/Dª [NOMBRE Y APELLIDOS], mayor de edad, casado, de profesión [PROFESIÓN], vecino de esta ciudad C/, según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], actuando bajo la dirección Letrada de D/Dª [NOMBRE Y APELLIDOS], Colegiado/a núm. con domicilio profesional en [LOCALIDAD], ante el Tribunal comparezco y como mejor proceda en Derecho DIGO:

Que en la representación que ostento EXPEDIENTE DE JURISDICCIÓN VOLUNTARIA DE REVISIÓN DE LA MEDIDA DE TUTELA de D. [NOMBRE Y APELLIDOS], acordada en la Sentencia dictada por este Tribunal el [FECHA], todo ello en base a los siguientes

HECHOS

PRIMERO.- En virtud de sentencia firme de fecha [FECHA] dictada en los autos [TIPO Y Nº DE PROCEDIMIENTO] seguidos ante la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [NÚMERO] se declaró que D. padecía un enolismo de larga evolución, señalándose que la dependencia alcohólica había derivado en una psicosis paranoide toxicofílica declarándose la incapacidad parcial del mismo. En dicha Sentencia se nombraba tutor a

Dicha sentencia fue objeto de recurso de apelación por la representación procesal de D. ante la Audiencia Provincial de [LOCALIDAD], sentencia que fue confirmada por dicho órgano jurisdiccional en virtud de sentencia de fecha [FECHA] Se aportan sendas copias testimoniadas de ambas resoluciones judiciales como DOCUMENTOS Núms. 1 y 2 respectivamente.

SEGUNDO.- Desde la constitución del órgano tutelar hasta la fecha de interposición de la presente solicitud, las circunstancias concurrentes han variado ostensiblemente. En fecha [FECHA] mi representado ingresó en el centro de desintoxicación homologado [NOMBRE DEL CENTRO] dependiente del Ministerio de Sanidad al objeto de iniciar el correspondiente tratamiento de desintoxicación. Dicho tratamiento que se ha prolongado durante año y medio ha sido en régimen cerrado con supervisión médica y psiquiátrica.

Mi representado ha seguido la totalidad del tratamiento con gran éxito encontrándose a fecha de la interposición de la presente solicitud totalmente desintoxicado. Se aporta como DOCUMENTO NÚM. 3 informe expedido por la dirección facultativa de dicho centro en que se certifica dicha afirmación.

TERCERO.- Por otro lado, teniendo en cuenta que la dependencia alcohólica había generado una psicosis paranoide toxicofílica mi representado ha recabado informe del psiquiatra adscrito al centro de desintoxicación al efecto de que determine cuál es el estado de dicha afección al momento presente. Se emite informe, que se aporta como DOCUMENTO NÚM. 4, en virtud del cual se pone de manifiesto que «si bien el consumo de alcohol prolongado produce desarrollo de trastornos de tipo paranoide, fundamentalmente de tipo celotípicos que afectan muy gravemente a las facultades volitivas e intelectivas de quien las sufre, en el caso presente D. habiendo superado con notable éxito y tratamiento intensivo su adicción al alcohol no puede decirse que en la actualidad sufra trastorno paranoide de ninguna índole, siendo su diagnóstico psiquiátrico de absoluta normalidad».

FUNDAMENTOS DE DERECHO

I. COMPETENCIA.

La competencia objetiva corresponde al Tribunal de Instancia de [SEDE], por ser quien declaró incapaz a mi representado, en virtud de lo dispuesto en el artículo 43.2 de la Ley de la Jurisdicción Voluntaria en la nueva redacción dada por la Ley 8/2021 de 2 de junio, a cuyo tenor:

2. El órgano judicial que haya conocido de un expediente sobre tutela, curatela o guarda de hecho, será competente para conocer de todas las incidencias, trámites y adopción de medidas o revisiones posteriores, siempre que el menor o persona con discapacidad resida en la misma circunscripción. En caso contrario, para conocer de alguna de esas incidencias, será preciso que se pida testimonio completo del expediente al Tribunal que anteriormente conoció del mismo, el cual lo remitirá en los diez días siguientes a la solicitud

II. PROCEDIMIENTO.

La sustanciación del presente procedimiento se llevará a cabo por los trámites del artículo 42 bis c) 3 de la Ley de la Jurisdicción Voluntaria en la nueva redacción dada por la Ley 8/2021 de 2 de junio.

La Disposición transitoria quinta de la Ley 8/2021 de 2 de junio “Revisión de las medidas ya acordadas” dispone:

Las personas con capacidad modificada judicialmente, los declarados pródigos, los progenitores que ostenten la patria potestad prorrogada o rehabilitada, los tutores, los curadores, los defensores judiciales y los apoderados preventivos podrán solicitar en cualquier momento de la autoridad judicial la revisión de las medidas que se hubiesen establecido con anterioridad a la entrada en vigor de la presente Ley, para adaptarlas a esta. La revisión de las medidas deberá producirse en el plazo máximo de un año desde dicha solicitud.

Para aquellos casos donde no haya existido la solicitud mencionada en el párrafo anterior, la revisión se realizará por parte de la autoridad judicial de oficio o a instancia del Ministerio Fiscal en un plazo máximo de seis años.

Para la tramitación de estos procedimientos de revisión los órganos judiciales se podrán auxiliar de herramientas tecnológicas que permitan obtener de manera automatizada la información sobre el fallecimiento de la persona interesada, en su caso.

Por su parte, el artículo 761 de la LEC, en la nueva redacción dada por la Ley 8/2021 de 2 de junio dispone con respecto a la revisión de las medidas de apoyo judicialmente adoptadas:

Las medidas contenidas en la sentencia dictada serán revisadas de conformidad con lo previsto en la legislación civil, debiendo seguirse los trámites previstos a tal efecto en la Ley de Jurisdicción Voluntaria.

En caso de que se produjera oposición en el expediente de jurisdicción voluntaria de revisión a que se refiere el párrafo anterior, o si dicho expediente no hubiera podido resolverse, se deberá instar el correspondiente proceso contencioso conforme a lo previsto en el presente Capítulo, pudiendo promoverlo cualquiera de las personas mencionadas en el apartado 1 del artículo 757, así como quien ejerza el apoyo de la persona con discapacidad.

III. LEGITIMACIÓN.

De acuerdo con el artículo 42. Bis c) 1, párrafo 2º de la Ley de la Jurisdicción Voluntaria la legitimación activa corresponde a mi mandante por haber resultado incapacitado en virtud de sentencia firme de fecha [FECHA].

“Cualquiera de las personas mencionadas en el apartado 3 del artículo 42 bis a), así como quien ejerza el apoyo, podrá solicitar la revisión de las medidas antes de que transcurra el plazo previsto en el auto”.

IV. FUNDAMENTACIÓN JURÍDICA DE LA ACCIÓN DEDUCIDA.

Dispone el artículo 291 del Código Civil en la nueva redacción dada por la Ley 8/2021 de 2 de junio:

La curatela se extingue de pleno derecho por la muerte o declaración de fallecimiento de la persona con medidas de apoyo.

Asimismo, la curatela se extingue por resolución judicial cuando ya no sea precisa esta medida de apoyo o cuando se adopte una forma de apoyo más adecuada para la persona sometida a curatela.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL: Tenga por presentado el presente escrito junto con el poder anexo, documentos y copias. Se admita todo ello y dé trámite legal. Tenga por presentado EXPEDIENTE DE JURISDICCIÓN VOLUNTARIA DE REVISIÓN DE LA MEDIDA DE TUTELA de D. [NOMBRE Y APELLIDOS] y en su virtud, tenga a bien declarar la extinción de la medida de la tutela acordada en la Sentencia de [FECHA] y en consecuencia, recovar el nombramiento del tutor D. nombrado a tal efecto, exigiendo a éste la rendición legal de cuentas. Y en caso de oposición, se declare contencioso el expediente, remitiendo a las partes al procedimiento de la Ley de Enjuiciamiento Civil. Es así de Justicia que pido en [LUGAR], a [FECHA].

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma Abogado y Procurador

========================================================================
