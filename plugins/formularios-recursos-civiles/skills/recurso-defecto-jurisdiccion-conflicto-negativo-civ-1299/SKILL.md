---
name: recurso-defecto-jurisdiccion-conflicto-negativo-civ-1299
description: "Recurso por defecto de jurisdicción en conflicto negativo de competencia. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Recurso por defecto de jurisdicción en conflicto negativo de competencia

> Formulario **CIV-1299** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 24-11-2026.

## Qué es

Recurso por defecto de jurisdicción, conflicto negativo de competencia que surge cuando en primer lugar, determinado órgano jurisdiccional aprecia su falta de jurisdicción, indicando en su decisión el orden jurisdiccional que estima competente y, posteriormente, los órganos de este segundo orden jurisdiccional declaran también su falta de jurisdicción en un proceso cuyos sujetos y pretensiones fueren los mismos

Es un modelo de tipo **recursos**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Recurso por defecto de jurisdicción en conflicto negativo de competencia» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Recurso por defecto de jurisdicción en conflicto negativo de competencia” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:recurso-defecto-jurisdiccion-conflicto-negativo-civ-1299`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (5 veces)
- [ ] Nº DE DOCUMENTO (4 veces)
- [ ] SEDE (4 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] ACTO O RESOLUCIÓN
- [ ] LUGAR
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] ÓRGANO JUDICIAL

## Normas que cita el formulario

- art. 50 LOPJ
- art. 42 LOPJ
- art. 43 LCS
- art. 1902 CC
- art. 9 LOPJ
- art. 50.3 LOPJ
- art. 50.1 LOPJ
- art. 9.4 LOPJ
- art. 2 LPAC
- art. 9.2 LOPJ

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

### Avisos de actualización (0) — se aplican en el texto, nunca se copian en el documento

- Ninguno.

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

AL TRIBUNAL [ÓRGANO JUDICIAL]

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales y de [NOMBRE DEL REPRESENTADO/A], según tengo ya acreditado en los presentes autos registrados como [Nº DE PROCEDIMIENTO], asistido por el/la Letrado/a [NOMBRE Y APELLIDOS], ante el Tribunal comparezco y, como mejor proceda en Derecho, DIGO:

Que mediante el presente escrito, y al amparo de lo dispuesto en el art. 50 LOPJ, interpongo RECURSO POR DEFECTO DE JURISDICCIÓN ante este Tribunal y para la SALA DE CONFLICTOS DE COMPETENCIA regulada en el art. 42 LOPJ, conforme a los siguientes:

HECHOS

PRIMERO

En fecha [FECHA], mi mandante interpuso demanda de juicio ordinario (cuya copia se acompaña como documento [Nº DE DOCUMENTO]) ante la Sección Civil del Tribunal de Instancia de [SEDE], contra [ACTO O RESOLUCIÓN] UTE, concesionaria de aguas del Ayuntamiento de [LOCALIDAD], en la que se reclamaba el pago de una cantidad en ejercicio de la acción de subrogación o reembolso ex art. 43 LCS, enmarcada en el ámbito de exigencia de responsabilidad civil extracontractual de los arts. 1902 y 1903 CCiv, por los daños ocasionados en el local de su asegurada, [DENOMINACIÓN SOCIAL] S.L., como consecuencia de una inundación producida el día [FECHA] por una subida de presión en las conducciones de agua por unas obras de reparación de la red subterránea de distribución del agua potable, ejecutadas por la demandada.

Por la Sección Civil del Tribunal de Instancia [SEDE], se dictó Auto de fecha [FECHA] en el que se acordó la falta de jurisdicción de dicho Tribunal para conocer el procedimiento por corresponder el asunto al orden jurisdiccional contencioso-administrativo (Documento [Nº DE DOCUMENTO]).

SEGUNDO

A la vista de la anterior resolución esta parte interpuso recurso contencioso-administrativo (cuya copia se acompaña como documento [Nº DE DOCUMENTO]) frente a la desestimación presunta de su reclamación patrimonial dirigida contra el mismo demandado, [DENOMINACIÓN SOCIAL] UTE, ante la Sección de lo Contencioso-Administrativo [LOCALIDAD], siendo repartido al Tribunal al que me dirijo, que lo registró como procedimiento abreviado [Nº DE PROCEDIMIENTO], en el que de nuevo reclamaba el pago de la indemnización que había satisfecho a su asegurada, en ejercicio de acción de repetición por daños derivados de culpa por responsabilidad extracontractual de una entidad que, en régimen de concesión administrativa, explota la gestión del servicio municipal de aguas, actuando como un supuesto de los contenidos en los arts. 1902 y 1903 CCiv, al tratarse de los daños producidos por una inundación debida a un incremento de la presión en las conducciones de agua.

Dicho Tribunal al que había correspondido el conocimiento del recurso ha efectuado declaración de incompetencia de jurisdicción por medio de auto, de fecha [FECHA] (cuya copia igualmente se acompaña como documento [Nº DE DOCUMENTO]), con la siguiente parte dispositiva: "Se declara la falta de jurisdicción en el presente recurso contencioso administrativo por considerar corresponde al orden jurisdiccional civil. Contra esta resolución cabe en el plazo de diez días recurso por defecto de jurisdicción conforme al art. 50 LOPJ. El recurso se interpondrá ante este Tribunal, quien, tras oír a las partes personadas remitirá las actuaciones a la Sala de Conflictos".

A los anteriores hechos les son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

I

El remedio previsto en el art. 50 LOPJ, llamado "recurso por defecto de jurisdicción" requiere como presupuestos indispensables para su interposición dos requisitos, que se cumplen en este caso.

El primero consiste en que el órgano del orden jurisdiccional indicado en la resolución a la que se refiere el apartado 6 del art. 9 LOPJ declare su falta de jurisdicción. El iter procedimental que se infiere de tal previsión legal es el que sigue: a) En primer lugar debe producirse una declaración de incompetencia por parte de un órgano judicial que indique en su resolución cual es el orden jurisdiccional competente; b) Una vez producida tal declaración, y no antes, el demandante debe acudir al orden al que es remitido; la razón estriba en que solo puede existir conflicto o enfrentamiento de criterios judiciales cuando la resolución del segundo orden se dicta respondiendo a la previa declaración de incompetencia del primero, y conociendo sus argumentos; de ahí que el art. 50.3 LOPJ se refiera al órgano que declaró "en primer lugar" su falta de jurisdicción. Dicho en otros términos, el litigante no puede crear artificialmente el conflicto planteando simultáneamente la misma pretensión ante órganos de dos órdenes jurisdiccionales distintos; para acudir al segundo, debe necesariamente esperar la resolución del primero; c) Finalmente es necesario que el órgano del orden Jurisdiccional al que remitió el que entendió primero, dicte una resolución firme declarando su falta de jurisdicción, que integra el conflicto negativo de competencia.

El segundo requisito que exige el art. 50.1 LOPJ es que la resolución firme que dicte el órgano que entendió en segundo lugar se produzca en un proceso cuyos sujetos y pretensiones fuesen los mismos que los del proceso suscitado ante el orden Jurisdiccional que primero declinó conocer del asunto.

II

El recurso se interpondrá ante el órgano que dictó la última resolución, declinando su jurisdicción, el cual, tras oír a las partes personadas, si las hubiere, remitirá las actuaciones a la Sala de Conflictos prevista en el art. 42 LOPJ.

La Sala reclamará del Tribunal que declaró en primer lugar su falta de jurisdicción que le remita las actuaciones y, oído el Ministerio Fiscal por plazo no superior a diez días, dictará auto dentro de los diez siguientes por medio del cual se encauzará definitivamente la concreta pretensión de la recurrente en el orden jurisdiccional al que corresponda resolverla.

III

Mi mandante sostiene que la competencia corresponde en este caso a la jurisdicción civil y, en particular, al Tribunal de Instancia [SEDE]

En efecto, la vis atractiva del orden contencioso-administrativo para conocer de las reclamaciones que, por responsabilidad patrimonial, se dirijan contra las Administraciones Públicas opera si aquella responsabilidad se atribuye a personas jurídico-públicas, aun cuando cuenten con un seguro de responsabilidad o en la producción del daño hayan concurrido particulares (arts. 9.4 LOPJ y 2.e) LJCA). Sin embargo, cuando la acción se plantea exclusivamente frente a sociedades mercantiles que, pese a gestionar un servicio municipal y estar participadas por capital público, se rigen por el derecho privado y no ejercen potestades públicas, sin que les convenga la calificación de Administraciones Públicas a la luz de lo dispuesto en los arts. 2 LPACAP, y 1.2 LJCA, la competencia corresponde a los tribunales del orden civil que, con arreglo al art. 9.2 LOPJ, conocen, además de las materias que les son propias, todas aquellas que no estén atribuidas a otro orden jurisdiccional.

En definitiva, en la decisión de conflictos similares ha puesto de manifiesto esa Sala —entre otros, en el Auto del Tribunal Supremo, 19 de noviembre de 2.007, rec. 17/2007; el Auto del Tribunal Supremo, 18 de diciembre de 2.009, rec. 5/2009 y el Auto del Tribunal Supremo, 18 de diciembre de 2.009, rec. 14/2009— que la mera condición de concesionaria de un servicio público, en este caso municipal, no atribuye a quien lo sea la condición de administración pública ni la de ejerciente de potestades administrativas.

De ahí que, como en la demanda no se imputa daño alguno a un ente que sea merecedor de aquella calificación, el conocimiento de la pretensión deducida por mi mandante —una aseguradora que, pagada la indemnización a su asegurada, ejercita contra quien señala como causante del daño a la concesionaria demandada— corresponde a los órganos judiciales del orden civil.

En virtud de lo expuesto,

SOLICITO AL TRIBUNAL

que teniendo por presentado este escrito en tiempo y forma, junto con los documentos que al mismo acompañan, se sirva admitirlo, dé traslado a la contraparte y, acuerde tener por interpuesto recurso por defecto de jurisdicción, así como elevar las actuaciones a la Sala Especial de Conflictos de Competencia del Tribunal Supremo, para que reclame las actuaciones AL TRIBUNAL DE INSTANCIA DE [SEDE] y cumplidos los demás trámites legalmente establecidos resuelva cuál de los órganos jurisdiccionales en conflicto es competente, determinando a qué órgano corresponde el conocimiento del asunto.

Es justicia de hacerse en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
