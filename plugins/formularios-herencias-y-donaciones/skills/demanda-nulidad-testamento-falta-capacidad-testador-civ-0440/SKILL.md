---
name: demanda-nulidad-testamento-falta-capacidad-testador-civ-0440
description: "Demanda de nulidad de testamento por falta de capacidad del testador (Derecho civil catalán). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de nulidad de testamento por falta de capacidad del testador (Derecho civil catalán)

> Formulario **CIV-0440** del plugin **Herencias, testamentos y donaciones** (`formularios-herencias-y-donaciones`) · Civil › Sucesiones y donaciones · normativa revisada el 24-11-2026.

## Qué es

Parte HECHOS Situación de incapacidad Prueba de la situación de falta de capacidad natural Elementos que corroboran la falta de capacidad Proceso de negociación previo y medios de solución de controversias de manera amistosa y extrajudicial FUNDAMENTOS DE DERECHO Suplico Otrosí de cuantía Firmas

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de nulidad de testamento por falta de capacidad del testador (Derecho civil catalán)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de nulidad de testamento por falta de capacidad del testador (Derecho civil catalán)” para mi caso». También puedes invocarla directamente con `/formularios-herencias-y-donaciones:demanda-nulidad-testamento-falta-capacidad-testador-civ-0440`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-herencias-y-donaciones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Herencias, testamentos y donaciones) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] FECHA (7 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] Nº DE DOCUMENTO (4 veces)
- [ ] AÑO
- [ ] DIAGNÓSTICO
- [ ] DÍA
- [ ] IMPORTE
- [ ] LUGAR
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] MES
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº
- [ ] OTROS DATOS
- [ ] SEDE

## Normas que cita el formulario

- art. 52.1.4.º LEC
- art. 251 LEC
- art. 422 CC
- art. 5 Ley Orgánica 1/2025
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

D [NOMBRE Y APELLIDOS] Procurador de los Tribunales, actuando en representación de [NOMBRE DEL REPRESENTADO/A] según se acredita por certificación del registro electrónico de apoderamientos judiciales que acompaño o mediante apoderamiento apud-acta otorgado ante el Letrado de la Administración de Justicia de [LOCALIDAD] por medio de la presente formulo demanda de juicio ordinario en ejercicio de impugnación del testamento otorgado por el causante D [NOMBRE Y APELLIDOS], la cual dirijo contra los herederos D [NOMBRE Y APELLIDOS] y D [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD] en base a los siguientes

HECHOS

Que mi mandante es hijo del causante D fallecido el día [FECHA] según resulta de las certificaciones de nacimiento, matrimonio y defunción que se adjuntan como documentos número

El causante D [NOMBRE Y APELLIDOS] otorgó testamento en fecha [FECHA] ante el Notario de [LOCALIDAD] D [NOMBRE Y APELLIDOS] copia que acompaño a la presente como documento nº [Nº DE DOCUMENTO], en el cual, entre otras disposiciones, instituía como herederos universales a los demandados, sin hacer mención alguna de mi representado.

Dicho testamento revocaba el otorgado en fecha [FECHA], en el cual se instituía como herederos universales, por partes iguales, a mi representado y a sus hermanos, ahora demandados (acompaño como documentos [Nº DE DOCUMENTO] testamento de fecha [FECHA] y certificado del Registro de Actos de Última Voluntad).

Que el causante, a la fecha de otorgar testamento, sufría una enfermedad mental severa que afectaba completamente a su entendimiento, encontrándose en una fase avanzada de demencia senil, no hallándose en plena capacidad y lucidez para comprender dicho acto.

El hecho de otorgar el testamento ahora impugnado, revocando el anterior, otorgado en fechas inmediatamente anteriores, sólo puede explicarse por la intervención de los herederos demandados, puesto que el estado de salud del causante le impedía el otorgamiento del testamento, tal como se expondrá a continuación.

El causante, de [Nº] años de edad al momento de otorgar el testamento, sufría una enfermedad mental degenerativa, estando sometido a tratamiento médico, tal y como se desprende del informe realizado por el Dr.que acompaño como documento nº [Nº DE DOCUMENTO], en el cual se incluye el diagnóstico de [DIAGNÓSTICO], lo cual lógicamente impedía que el causante pudiera otorgar testamento al carecer de la capacidad natural para hacerlo.

Si bien es cierto que el notario autorizante D [NOMBRE Y APELLIDOS] afirma apreciar la capacidad natural del otorgante, lo cierto es que existen elementos que desvirtúan tal apreciación como se deriva claramente del hecho de que el mismo día [FECHA] en que se otorgó el testamento, el causante tuvo que ser atendido en el servicio de urgencias del Hospital de [LOCALIDAD] al presentar un cuadro de desorientación psíquica y sensorial, tal como se acredita por los informes que se acompañan como documentos número

A raíz de esta patología, el causante D [NOMBRE Y APELLIDOS] fue ingresado en el Hospital psiquiátrico de [LOCALIDAD], siendo visitado ese mismo día por su hermana Dª [NOMBRE Y APELLIDOS], a quien ni tan siquiera reconoció tal como se acreditará oportunamente, falleciendo una semana después.

De todo ello se deduce claramente que la apreciación del notario autorizante sobre la capacidad del causante se basó en un juicio erróneo, puesto que el mismo carecía de mínimas facultades para otorgar testamento, desvirtuándose de este modo la presunción de capacidad del testador, tal como se probará en el curso de este proceso.

Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

FUNDAMENTOS DE DERECHO

Competencia

Corresponde a los Tribunales de [LOCALIDAD] al ser el lugar en el que el finado tuvo su último domicilio con fundamento en el artículo 52.1.4.º LEC.

Legitimación

Le corresponde a esta parte la legitimación activa ante su condición de hijo del causante y heredero forzoso, pudiendo ser beneficiado por la declaración de nulidad, correspondiendo la legitimación pasiva a los herederos demandados.

Procedimiento

Versando la presente demanda sobre sucesión testamentaria, y no teniendo la misma regulada ninguna tramitación especial, debe decidirse la misma por los trámites del juicio ordinario, conforme establece el artículo 249, apartado 2, de la Ley de Enjuiciamiento Civil [OTROS DATOS], al exceder su cuantía de la cantidad de 15.000 euros, calculada conforme al artículo 251, regla 12ª, de la LEC.

Plazo de ejercicio de la acción de nulidad

Se ejercita la presente acción de nulidad antes de que trascurran cuatro años desde que el demandante conoció o pudo conocer razonablemente la causa de nulidad, de conformidad a lo que dispone el artículo 422-3 del CC de Cataluña.

Cumplimiento de los requisitos de procedibilidad.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

Nulidad del testamento

Se ejercita la acción de nulidad del testamento citado en base a la incapacidad de testar del causante tomando como fundamento los artículos 421-3, 421-4, 422-1.1, del Código Civil de Cataluña, disponiendo este último precepto que es nulo el testamento otorgado sin cumplir los requisitos legales de capacidad. La falta de capacidad natural no resulta desvirtuada por la intervención de notario, puesto que la apreciación de capacidad de éste puede ser objeto de prueba en contrario, tal como se deriva de los documentos acompañados con esta demanda y se acreditará en el curso de este proceso a través de la prueba que pretende ejercitar esta parte.

Efectos de la nulidad

Es de aplicación el artículo 422-4 cuando establece que la nulidad del testamento determina que la sucesión se rija por el testamento anterior válido, debiendo estarse al otorgado en fecha

En materia de costas el artículo 394 LEC señala que las de primera instancia se imponen a la parte que vea en primera instancia rechazadas sus pretensiones.

En base a lo anterior,

SUPLICO AL TRIBUNAL que tenga por presentada la presente demanda con los documentos a ella adjuntos y sus copias, y tras la pertinente tramitación, se dicte por ese Tribunal sentencia en que se declare nulo el testamento objeto de la presente demanda otorgado por el causante en fecha [FECHA], declarando la validez del testamento anterior otorgado en fecha [FECHA], condenando a los demandados a estar y pasar por dicha declaración, con imposición de costas si se opusieran a la demanda.

OTROSÍ PRIMERO DIGO.- Se fija la cuantía de este procedimiento en [IMPORTE] euros, de conformidad a lo que dispone el artículo 251, regla 12ª, de la LEC.

SUPLICO AL TRIBUNAL se tenga por efectuada la anterior manifestación a los efectos pertinentes.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma Abogado Firma procurador

========================================================================
