---
name: contestacion-demanda-extincion-pareja-hecho-sin-hijos-civ-0231
description: "Contestación a la demanda de extinción de pareja de hecho sin hijos comunes en Cataluña. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contestación a la demanda de extinción de pareja de hecho sin hijos comunes en Cataluña

> Formulario **CIV-0231** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contestación a la demanda de extinción de pareja de hecho sin hijos comunes en Cataluña» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contestación a la demanda de extinción de pareja de hecho sin hijos comunes en Cataluña” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:contestacion-demanda-extincion-pareja-hecho-sin-hijos-civ-0231`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] FECHA (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] SEDE (2 veces)
- [ ] AÑO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DÍA
- [ ] LUGAR
- [ ] MES
- [ ] Nº
- [ ] Nº DE HECHO
- [ ] PUESTO DE TRABAJO

## Normas que cita el formulario

- art. 234.1 Código Civil
- art. 234 Código Civil
- art. 234.13 Código Civil
- art. 234.9 Código Civil
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

### Avisos de actualización (3) — se aplican en el texto, nunca se copian en el documento

- Junto a «…PACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [NÚMERO]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.
- Junto a «…LIDOS] ante la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. «De los de» es residuo de los varios juzgados de una plaza. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

Proceso declarativo número [NÚMERO]

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [NÚMERO]

Don/Dª [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en la representación que ostento de D. [NOMBRE Y APELLIDOS], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], y bajo la dirección Letrada de Don [NOMBRE Y APELLIDOS] ante la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº] en el proceso declarativo arriba expresado comparezco y, como mejor proceda en Derecho, DIGO:

Que habiéndose dado traslado a esta parte de la demanda formulada por D. [NOMBRE Y APELLIDOS] en reclamación de efectos económicos derivados de la extinción de la relación estable de pareja de hecho, siguiendo instrucciones de mi poderdante por medio del presente escrito y en nombre del mismo formulo en tiempo y forma CONTESTACIÓN A LA DEMANDA, la cual baso en los siguientes

HECHOS

En total disconformidad con el correlativo en cuanto a la constitución de la pareja de hecho entre el demandante y el demandado.

Me opongo al correlativo por cuanto en ningún momento ha existido una relación estable de pareja de hecho entre los litigantes por los siguientes motivos:

No existe relación de pareja de hecho por no cumplirse el requisito de convivencia marital del artículo 234.1 del Código Civil de Cataluña, puesto que si bien el demandante y demandado, si bien convivían en el mismo domicilio por razones esencialmente económicas al compartir gastos de arriendo y de mantenimiento, en ningún momento han tenido una relación afectiva análoga a la conyugal, de tal manera que negamos rotundamente que esta relación pueda ser conceptuada como de pareja de hecho.

Aun aceptando la existencia de una relación afectiva entre los litigantes, no existe relación de pareja de hecho puesto que el artículo 234.1 del Código Civil de Cataluña exige una convivencia marital de un periodo ininterrumpido mínimo de dos años, siendo que del propio contenido de la demanda se desprende que no se ha cumplido este requisito temporal no existiendo descendencia común entre los convivientes ni habiéndose formalizado escritura pública.

Nos oponemos a la existencia de una relación de pareja de hecho por cuanto que no puede constituirse pareja estable al tratarse de una de las personas indicadas en el artículo 234-2 del Código Civil de Cataluña, puesto que mi representado es menor de edad no emancipado (o está ligado por vínculo matrimonial con otra persona, según se acredita por certificación del Registro Civil de [LOCALIDAD]) (o está registrado como pareja de hecho de otra persona según se acredita por certificación del Registro de Parejas de Hecho de [LOCALIDAD]) ( o es pariente en línea recta por consanguinidad o adopción o colateral dentro del segundo grado prohibido por la legislación vigente, según se acredita por las certificaciones del Registro Civil que se acompañan como documentos [Nº DE DOCUMENTO]), por lo que no se cumplen los requisitos del citado artículo 234.2 para la existencia de pareja estable.

En disconformidad con el hecho [Nº DE HECHO] de la demanda en los términos expuestos de contrario.

La reclamación es improcedente, según resulta de los hechos de la demanda, puesto que se ha excedido el plazo de prescripción establecido en el artículo 234.13 del Código Civil de Cataluña, precepto que dispone que la reclamación de los derechos debe formularse en el plazo de un año a contar desde la extinción de la pareja estable, siendo que la extinción se produjo el día [FECHA], y la demanda se interpone en fecha [FECHA] una vez transcurrido en exceso el plazo de un año establecido en el precepto.

Subsidiariamente, y para el improbable caso en que se estimara que la relación de mi mandante con el actor constituye una unión estable de hecho y que no se ha producido la prescripción, debemos manifestar que en absoluto se ha producido la situación de hecho que determina la aplicación del derecho a la prestación alimentaria del artículo 234-10 del Código Civil de Cataluña por cuanto la convivencia en modo alguno redujo la capacidad del demandante para la obtención de ingresos, puesto que el demandante durante todo este tiempo ha estado desempeñando la actividad laboral por cuenta ajena de [PUESTO DE TRABAJO] en la empresa [DENOMINACIÓN SOCIAL], a la cual se dedicaba antes de convivir con mi representado, percibiendo idénticas retribuciones.

Tampoco se dan los requisitos para fijar la compensación a que se refiere el artículo 234.9 del Código Civil de Cataluña, puesto que en modo alguno el demandante ha trabajado para la casa sustancialmente más que mi representado, ni existe dedicación para mi representado, puesto que todas las tareas del hogar han sido compartidas, dedicándose cada conviviente a sus ocupaciones laborales y distribuyéndose el resto de tareas, como se acreditará oportunamente en la fase probatoria de este proceso, de lo que resulta la improcedencia de la reclamación formulada de contrario.

FUNDAMENTOS DE DERECHO

Conformes con la competencia objetiva y territorial del Tribunal, la legitimación "ad procesum", y el procedimiento adecuado escogido, compareciendo esta parte con la debida representación técnica y asistencia letrada.

En cuanto al fondo de la pretensión, nos oponemos por falta de legitimación "ad causam" al no existir pareja de hecho entre los litigantes, según resulta de la regulación del artículo 234.1 del Código Civil de Cataluña que dispone "Dos personas que conviven en una comunidad de vida análoga a la matrimonial se consideran pareja estable en cualquiera de los siguientes casos: a) Si la convivencia dura más de dos años ininterrumpidos; b) Si durante la convivencia, tienen un hijo común; c) Si formalizan la relación en escritura pública", en tanto que el artículo 234.2 prohíbe formar pareja estable a las siguientes personas: "a) Los menores de edad no emancipadas. b) Las personas relacionadas por parentesco en línea recta, o colateral dentro del segundo grado. c) las personas casadas y no separadas de hecho. d) Las personas que convivan en pareja con una tercera persona".

Oponemos asimismo prescripción, tal como establece el artículo 234.13, que dispone que "los derechos a la compensación económica por razón de trabajo y a la prestación alimentaria prescriben en el plazo de un año a contar de la extinción de la pareja estable y deben reclamarse, si procede, en el mismo procedimiento en que se determinan los demás efectos de la extinción de la pareja estable".

Asimismo, y en cuanto al fondo, nos oponemos a la pretensión indemnizatoria por falta de fundamento, al no darse los requisitos establecidos legalmente para que se fije una pensión periódica y/o compensación económica recogidos en los artículos 234.9 y 234.10 del Código Civil de Cataluña. En cuanto a los requisitos para el establecimiento de la compensación económica por razón de trabajo y de la prestación alimentaria citamos las SSTSJ Cataluña 4 de octubre de 2004, rec. 26/2004; 9 de mayo de 2005, rec. 122/2004 y 4 de julio de 2006, rec. 105/2005, entre otras.

Las costas deben imponerse a la actora, de conformidad con lo dispuesto en el artículo 394 LEC.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL que teniendo por presentado este escrito, con sus documentos, y copias de todo ello, se sirva admitirlo, y tenga por formulada CONTESTACIÓN A LA DEMANDA y, tras los trámites legales, dicte Sentencia desestimatoria de la pretensión formulada de contrario, todo ello con expresa imposición de costas a la parte actora.

Es justicia que pido en [LUGAR], a [DÍA] de [MES] de [AÑO].

========================================================================
