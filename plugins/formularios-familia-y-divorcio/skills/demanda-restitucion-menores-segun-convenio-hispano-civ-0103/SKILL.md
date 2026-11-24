---
name: demanda-restitucion-menores-segun-convenio-hispano-civ-0103
description: "Demanda de restitución de menores según el Convenio hispano-marroquí de 1997. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de restitución de menores según el Convenio hispano-marroquí de 1997

> Formulario **CIV-0103** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de restitución de menores según el Convenio hispano-marroquí de 1997» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de restitución de menores según el Convenio hispano-marroquí de 1997” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-restitucion-menores-segun-convenio-hispano-civ-0103`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] FECHA (2 veces)
- [ ] NOMBRE DEL MENOR (2 veces)
- [ ] Nº (2 veces)
- [ ] Nº DE COLEGIADO (2 veces)
- [ ] AÑO
- [ ] CALLE
- [ ] COLEGIO
- [ ] DÍA
- [ ] LUGAR
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] MES
- [ ] Nº DE COLEGIADO/A
- [ ] Nº DE DOCUMENTO
- [ ] PAÍS
- [ ] SEDE
- [ ] ÓRGANO JUDICIAL

## Normas que cita el formulario

- art. 778 LEC
- art. 85.1 LOPJ
- art. 5 Ley Orgánica 1/2025
- art. 778 bis LEC

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

- Junto a «…MILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, con número de colegiado/a [Nº DE COLEGIADO/A] y de D/Dña. [NOMBRE Y APELLIDOS] con pasaporte de [PAÍS] núm. [Nº], mayor de edad, con domicilio en [LOCALIDAD], según acredito mediante copia electrónica de poder notarial de representación, con la dirección Letrada del Abogado/a D./Dña. [NOMBRE Y APELLIDOS], colegiado/a núm. [Nº DE COLEGIADO] del Ilustre Colegio de Abogados de [COLEGIO], ante el Tribunal comparezco y, como mejor proceda en derecho, DIGO:

Que, al amparo de lo dispuesto en los arts. 778 quáter y siguientes de la LECiv, formulo DEMANDA en solicitud de LA RESTITUCIÓN A MI REPRESENTADA DEL MENOR, sustraído ilícitamente por su padre Don [NOMBRE Y APELLIDOS], residente en esta ciudad, calle [CALLE], fundamentándolo en los siguientes:

HECHOS

PRIMERO. - El menor [NOMBRE DEL MENOR] cuya guarda y custodia había sido atribuida a la madre en virtud de sentencia judicial dictada por el Tribunal [ÓRGANO JUDICIAL] de Marruecos en fecha [FECHA] estaba disfrutando en [LOCALIDAD] España de las visitas otorgadas en dicha sentencia a su padre don [NOMBRE Y APELLIDOS] con residencia habitual en España, que finalizaban en fecha [FECHA] momento en el cual el padre debía desplazarse a [LOCALIDAD] Marruecos y entregar al menor a su madre.

Acompañamos en prueba de ello la citada sentencia como Documento núm. 1.

SEGUNDO. - Al llegar la fecha indicada el padre no ha devuelto el menor a su madre negándose a entregárselo.

Acompañamos en prueba de ello denuncia formulada ante la Policía como Documento núm. 2.

TERCERO. - Ante esta situación y en virtud de lo dispuesto en los convenios de Luxemburgo, de La Haya de 1980, y sobre asistencia judicial, reconocimiento y ejecución de resoluciones judiciales en materia de custodia, derecho de visita y devolución de menores entre el Reino de España y el Reino de Marruecos, procederá a la devolución inmediata del menor a la compañía del progenitor que tenía antes de la sustracción la guarda y custodia del menor.

CUARTO.- Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

A los anteriores hechos son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

PRIMERO.- NORMATIVA APLICABLE:

Son aplicables los convenios de Luxemburgo, de La Haya de 1980, y sobre asistencia judicial, reconocimiento y ejecución de resoluciones judiciales en materia de custodia, derecho de visita y devolución de menores entre España y Marruecos, al cumplirse los ámbitos de aplicación, temporal, material y espacial de los citados Convenios, que tienen entre otros, el objetivo de garantizar la devolución de los menores desplazados o retenidos ilegalmente en uno de los dos Estados contratantes; en el presente supuesto se ha producido la retención ilícita de un menor.

SEGUNDO.- COMPETENCIA: Es competente el Tribunal de Instancia al que tengo el honor de dirigirme, por ser el que ostenta competencias en materia de familia en la capital de provincia de la circunscripción donde se halla el menor, conforme a lo dispuesto en el art. 778 quáter 2 LEC, en relación con lo dispuesto en el art. 85.1º LOPJ.

TERCERO.- PROCEDIMIENTO: Debe seguirse el procedimiento del art. 778 quáter y siguientes de la LECiv, el cual tiene carácter urgente y preferente según dispone el apartado 5 del art. 778 quáter.

CUARTO.- LEGITIMACIÓN: El apartado 3 del art. 778 quáter establece que podrán promover el procedimiento la persona, institución u organismo que tenga atribuida la guarda y custodia o un régimen de estancia o visitas, relación o comunicación del menor, la Autoridad Central española encargada del cumplimiento de las obligaciones impuestas por el correspondiente convenio, en su caso, y, en representación de ésta, la persona que designe dicha autoridad, debiendo intervenir el Ministerio Fiscal.

QUINTO.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD: La presente demanda cumple con los requisitos de procedibilidad exigidos por el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

SEXTO.- El menor tenía su residencia habitual en Marruecos y se le retuvo indebidamente en España vulnerando -cuando finalizaron las visitas a las que tenía derecho el padre- la guarda y custodia que tenía atribuida legalmente la madre no devolviéndolo al lugar de su residencia habitual (Marruecos), por lo que se ha dirigido una comunicación a la Autoridad Central marroquí para que se comunique con la española en los términos del art. 4 del Convenio el Reino de España y el Reino de Marruecos. La solicitud incluye información relativa a la identidad del demandante, del menor; los motivos en los que se basa el demandante para reclamar la restitución; toda la información disponible relativa a la localización del menor y la identidad de la persona con la que se supone que está el menor.

SÉPTIMO.- Es de aplicación el art. 8 del Convenio entre el Reino de España y el Reino de Marruecos sobre asistencia judicial, reconocimiento y ejecución de resoluciones judiciales en materia de derecho de custodia y derecho de visita y devolución de menores que establece: «1.Cuando la solicitud de devolución, una vez ocurrido el desplazamiento ilegal del menor, sea presentada ante las Autoridades centrales de uno de los Estados contratantes, antes de haber transcurrido un plazo de seis meses, la Autoridad judicial competente deberá ordenar su devolución inmediata ».

En el presente caso la solicitud de restitución se ha presentado transcurridos [Nº] meses de la sustracción pero la restitución debe ser acordada al cumplirse el tenor del art. 9 del Convenio: «Cuando se presente la solicitud de devolución después de transcurrido un plazo de seis meses, la Autoridad judicial ordenará la devolución del menor, en las mismas condiciones, a menos que quede demostrado que el menor se ha integrado en su nuevo entorno o que su devolución le puede exponer a algún peligro físico o psíquico o a una situación intolerable».

El menor no se ha integrado en su nuevo medio y la restitución no será perjudicial para él.

OCTAVO.- No concurre ninguna de las causas de denegación de la restitución del menor relacionadas en los convenios de Luxemburgo, de La Haya de 1980, p entre el Reino de España y el Reino de Marruecos sobre asistencia judicial, reconocimiento y ejecución de resoluciones judiciales en materia de derecho de custodia y derecho de visita y devolución de menores.

Podrán estar legitimados también cualquier otra persona, institución u organismo que tenga atribuido el derecho de custodia del menor, así como la autoridad central española -Secretaría General Técnica del Ministerio de Justicia-, encargada del cumplimiento del presente Convenio y, en representación de ésta la persona, que designe dicha autoridad

Debido a la diferencia entre el derecho marroquí y el español es preciso tener muy en cuenta la mención del art. 9 in fine del Convenio entre el Reino de España y el Reino de Marruecos, que establece: «Al considerar las circunstancias, las Autoridades judiciales tendrán en cuenta: Únicamente el interés del menor, sin ninguna otra restricción derivada de su derecho interno».

No obstante, la Autoridad judicial no estará obligada a ordenar la devolución del menor cuando: a) el menor sea nacional, exclusivamente, del Estado requerido y, según la ley interna de este Estado, el padre con el que se encuentra el menor sea el único titular de pleno derecho de la patria potestad. b) Se alegue una resolución ejecutiva relativa a la custodia en el territorio del Estado requerido.

NOVENO.- COSTAS:

En virtud del mandato del art. 778 quinquies, apartado 10, procede la imposición de costas al demandado.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL: Que teniendo por presentado este escrito de demanda, con los documentos y copias que se acompañan, se sirva admitirlo, me tenga por comparecido en la representación que ostento y, con audiencia del Ministerio Fiscal, se

DICTE AUTO POR EL QUE SE CONCEDA LA RESTITUCIÓN DEL MENOR [NOMBRE DEL MENOR] A SU PAÍS DE ORIGEN.

OTROSÍ DIGO, Que siendo urgente la situación más arriba descrita según lo establecido en el artículo 778 bis, apartado 8, de la LECiv.

SUPLICO AL TRIBUNAL, que se ponga al menor, inmediatamente, bajo la custodia de mi mandante, a la que legalmente corresponde la custodia.

Es Justicia que pido en [LUGAR], a [DÍA] de [MES] de [AÑO].

Fdo.:

Colegiado/a núm. [Nº DE COLEGIADO]

========================================================================
