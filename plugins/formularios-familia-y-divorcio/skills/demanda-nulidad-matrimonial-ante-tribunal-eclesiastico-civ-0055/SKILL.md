---
name: demanda-nulidad-matrimonial-ante-tribunal-eclesiastico-civ-0055
description: "Demanda de nulidad matrimonial ante el Tribunal Eclesiástico. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de nulidad matrimonial ante el Tribunal Eclesiástico

> Formulario **CIV-0055** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de nulidad matrimonial ante el Tribunal Eclesiástico» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de nulidad matrimonial ante el Tribunal Eclesiástico” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-nulidad-matrimonial-ante-tribunal-eclesiastico-civ-0055`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] DÍA (7 veces)
- [ ] MES (7 veces)
- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] AÑO (6 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] NÚMERO (4 veces)
- [ ] CALLE (2 veces)
- [ ] CAUSA
- [ ] COLEGIO
- [ ] DESCRIPCIÓN DEL DOCUMENTO
- [ ] EDAD
- [ ] LUGAR
- [ ] Nº

## Normas que cita el formulario

- No cita artículos concretos; Claude localizará las normas aplicables con Jurisprudenciator si el documento las necesita.

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

AL RVDO. TRIBUNAL ECLESIÁSTICO DEL ARZOBISPADO DE [LOCALIDAD]

D./Dª [NOMBRE Y APELLIDOS], Procurador de los Tribunales, según acredito mediante copia de [DESCRIPCIÓN DEL DOCUMENTO] que acompaño, cuya devolución intereso una vez testimoniada, y de D./Dª [NOMBRE Y APELLIDOS], mayor de edad, católico, vecino de [LOCALIDAD], calle [CALLE], nº [NÚMERO], pta., según resulta del poder de representación procesal que se acompaña, y asistido/a del Letrado D./Dª [NOMBRE Y APELLIDOS], col. nº [NÚMERO] del Ilustre Colegio de Abogados de [COLEGIO], ante el Tribunal comparezco y DIGO:

Que en la representación que ostento y siguiendo instrucciones de mi mandante, interpongo DEMANDA DE NULIDAD matrimonial contra D./Dª [NOMBRE Y APELLIDOS], mayor de edad, bautizada en la Iglesia Católica, con domicilio en [LOCALIDAD], calle [CALLE], nº [NÚMERO], pta., la que se basa y fundamenta en los siguientes:

HECHOS

D./Dª [NOMBRE Y APELLIDOS] y D./Dª [NOMBRE Y APELLIDOS], contando con [EDAD] y [Nº] años de edad respectivamente, contrajeron formalmente matrimonio canónico el día [DÍA] de [MES] de [AÑO], en la Iglesia Parroquial de [LOCALIDAD] de

Se adjunta a la presente demanda Partida de matrimonio con números UNO de documentos.

De su unión matrimonial han nacido tres hijos, el [DÍA] de [MES] de [AÑO], el [DÍA] de [MES] de [AÑO] y [NOMBRE Y APELLIDOS], el [DÍA] de [MES] de

Se acompañan Partidas de Bautismo con números DOS, TRES y CUATRO de documentos.

Los esposos cesaron la convivencia marital a finales de [AÑO], iniciando inmediatamente los trámites legales en solicitud del pronunciamiento judicial de Separación. La sentencia declarando dicha Separación fue dictada por el Tribunal de Instancia (Sección Civil, plaza n.º [NÚMERO]) -Familia- de [LOCALIDAD], en fecha [DÍA] de [MES] de [AÑO] Posteriormente, los cónyuges tramitaron, por la vía del mutuo acuerdo y ante la misma jurisdicción civil, el procedimiento judicial de su Divorcio, recayendo Sentencia el [DÍA] de [MES] de

Adjuntamos bajo número CINCO y SEIS de documentos copia de las referidas Sentencias junto a los Convenios Reguladores suscritos por los cónyuges y aprobados judicialmente.

Considerando en conciencia que su matrimonio fue nulo y sin que le mueva ningún otro interés que no sea el de clarificar esta cuestión sometiéndola al discernimiento y criterio de la Iglesia, es por lo que Javier inicia este proceso.

FUNDAMENTOS DE DERECHO

El canon 1.673 del Corpus Iuris Canonici, en relación con el artículo 10 de la Instrucción Pontificia Dignitas Connubii y disposiciones concordantes, según el cual es competente el Tribunal al que se dirige la demanda para poder entender de la presente causa por mantener el/la esposo/a demandado/a su domicilio en el territorio de esta diócesis.

El canon 1.674-1 del CIC, en relación con el artículo 92.1 de la Instrucción Pontificia Dignitas Connubii, que establece la legitimación de cualquiera de los cónyuges para acusar de nulidad su matrimonio.

Deberá tramitarse la presente causa conforme a cuanto ha sido establecido para el Juicio contencioso ordinario, al amparo de lo previsto en los cánones 1.501, siguientes y concordantes, del Corpus Iuris Canonici.

El canon 1.483 del CIC, en relación con los artículos 101 al 113 de la Instrucción Pontificia Dignitas Connubii, en lo que se refiere a los requisitos de abogados y procuradores.

En su virtud,

SUPLICO AL TRIBUNAL, que habiendo por presentada esta demanda, la admita, teniéndome por comparecido en la representación que ostento, se sirva dar traslado de la misma al/a la esposo/a demandado/a y al Defensor del Vínculo; y en su día, tras recibimiento a prueba en fase de instrucción de la causa y demás trámites legales, dicte sentencia por la que declare la nulidad del matrimonio contraído por el/la actor/a con el/la demandada por los capítulos de [CAUSA], concurrentes en uno o ambos esposos.

PRIMER OTROSÍ DIGO: Que reuniendo quienes suscriben los requisitos necesarios para defender y representar al/a la actor/a, interesa del Tribunal confiera a su favor la oportuna comisión canónica a tal efecto, SUPLICO DEL TRIBUNAL, así se acuerde.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Fdo.: Abogado y Procurador

========================================================================
