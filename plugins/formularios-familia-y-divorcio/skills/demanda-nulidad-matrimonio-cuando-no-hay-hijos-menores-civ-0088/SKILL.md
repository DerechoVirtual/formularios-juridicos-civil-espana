---
name: demanda-nulidad-matrimonio-cuando-no-hay-hijos-menores-civ-0088
description: "Demanda de nulidad del matrimonio cuando no hay hijos menores. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de nulidad del matrimonio cuando no hay hijos menores

> Formulario **CIV-0088** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de nulidad del matrimonio cuando no hay hijos menores» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de nulidad del matrimonio cuando no hay hijos menores” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-nulidad-matrimonio-cuando-no-hay-hijos-menores-civ-0088`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (12 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] Nº (3 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] AÑO
- [ ] DESCRIBIR
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] DÍA
- [ ] FECHA
- [ ] LUGAR
- [ ] MES
- [ ] Nº DE ARTÍCULO
- [ ] SEDE
- [ ] TIPO DE MATRIMONIO (CIVIL / CANÓNICO)

## Normas que cita el formulario

- art. 770 LEC
- art. 46.2 CC

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
- Junto a «…m. [Nº] ========================================================================»: requisito de procedibilidad del art. 5 LO 1/2025 — antes de presentar la demanda hay que intentar un medio adecuado de solución de controversias (MASC) y acreditarlo con la demanda (arts. 264.4.º y 399.3 LEC), salvo las materias excluidas del art. 5.2. Fuente: LO 1/2025, arts. 5 a 7 (BOE-A-2025-76).

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

Don/Doña [NOMBRE Y APELLIDOS] Procurador de los Tribunales en representación de Don/Doña [NOMBRE Y APELLIDOS], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], como mejor proceda en derecho ante el Tribunal comparezco y DIGO:

Que en la representación que ostento deduzco DEMANDA DE NULIDAD MATRIMONIAL, contra Don/Doña [NOMBRE Y APELLIDOS], por la causa tipificada en el artículo [Nº DE ARTÍCULO] del Código Civil, en base a los siguientes

HECHOS

PRIMERO Don [NOMBRE Y APELLIDOS] y doña [NOMBRE Y APELLIDOS] contrajeron matrimonio [TIPO DE MATRIMONIO (CIVIL / CANÓNICO)] en [LOCALIDAD] con fecha de [FECHA], inscrito en el Registro Civil de [LOCALIDAD] según acredito mediante documento núm. [Nº DE DOCUMENTO]

SEGUNDO Del citado matrimonio no han nacido hijos.

TERCERO Don [NOMBRE Y APELLIDOS] y doña [NOMBRE Y APELLIDOS] en [LOCALIDAD] entablaron relaciones de noviazgo que a los escasos meses concluyeron en el matrimonio que se celebró en

Al año escaso de convivencia, mi mandante tuvo conocimiento a través de don [NOMBRE Y APELLIDOS] que su esposo había contraído nupcias en [LOCALIDAD] con doña [NOMBRE Y APELLIDOS] lo cual resultó cierto según las gestiones practicadas por mi principal, obteniendo documento acreditativo de su matrimonio según se justifica con el núm. [Nº] que se adjunta.

CUARTO Dicho hecho al principio fue negado por el demandado si bien frente a la evidencia

documental afirmó que era sólo un matrimonio de conveniencia y que inició los trámites de nulidad ante los Tribunales de [LOCALIDAD]. En consecuencia, mi mandante ha contraído matrimonio con persona que ya se hallaba casada, por lo cual procede decretar la ineficacia absoluta del segundo matrimonio, ignorando mi representada la existencia del anterior que lo fue con doña [NOMBRE Y APELLIDOS].

QUINTO En orden a los efectos o medidas consecuencia de orden personal y patrimonial derivados de la nulidad, ha de reseñarse que el sistema económico matrimonial era el de la sociedad de gananciales; el demandado posee un saneado patrimonio consistente en [DESCRIBIR]. Durante este año se han adquirido los siguientes bienes [DESCRIPCIÓN DEL BIEN] según se justifica mediante documentos números [Nº DE DOCUMENTO]. A los anteriores hechos le son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

Artículo 769 LECiv, sobre la competencia, correspondiendo el conocimiento de la demanda a la Sección Civil del Tribunal de Instancia del domicilio conyugal sito en

Artículos 770 LECiv, y 437 y siguientes de la LECiv en cuanto al procedimiento a seguir, por los trámites establecidos para el Juicio Verbal con las salvedades previstas en el artículo 770 LECiv.

Artículo 74 del Código Civil, que faculta a los cónyuges y demás personas con interés legítimo y directo, requisito que concurre en mi mandante por ser cónyuge.

Fundamentos de derecho material de la acción deducida. Artículo 72.2 en relación con el artículo 46.2, ambos del CC.

« La unidad del vínculo matrimonial es uno de los principios de orden público de nuestro ordenamiento jurídico en cuya virtud está establecido en la regulación del matrimonio el impedimento de ligamen como uno de los llamados impedimentos dirimentes, cuando existe un matrimonio anterior no disuelto, siendo la nulidad la consecuencia prevista para el matrimonio contraído con este impedimento.»

Artículo 394 LECiv, sobre las costas procesales.

Por todo lo cual,

SUPLICO AL TRIBUNAL: Que teniendo por presentada la presente demanda con los documentos que se adjuntan y copias de todo ello, se sirva admitirlo, tenga al procurador que suscribe por personado y parte en la representación que ostenta de doña [NOMBRE Y APELLIDOS], y previo recibimiento del pleito a prueba que desde este momento se deja interesado, tras los trámites oportunos, se dicte sentencia, por la que se declare, la NULIDAD MATRIMONIAL DE LOS CÓNYUGES, extendiéndose a todos los actos y derechos que el demandado don [NOMBRE Y APELLIDOS] disfruta, consecuencia del fraudulento matrimonio.

Es Justicia que pido en [LUGAR], a [DÍA] de [MES] de [AÑO].

Fdo. Letrado

Coleg. núm. [Nº]

Fdo. Procurador

Coleg. núm. [Nº]

========================================================================
