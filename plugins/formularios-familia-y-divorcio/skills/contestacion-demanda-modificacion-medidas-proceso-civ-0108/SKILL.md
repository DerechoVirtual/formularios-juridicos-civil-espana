---
name: contestacion-demanda-modificacion-medidas-proceso-civ-0108
description: "Contestación a la demanda de modificación de medidas de un proceso matrimonial (Derecho catalán). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contestación a la demanda de modificación de medidas de un proceso matrimonial (Derecho catalán)

> Formulario **CIV-0108** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Escrito de oposición a la solicitud de modificación de medidas definitivas (en este modelo, la reducción de la pensión de alimentos de los hijos por el nacimiento de nuevos hijos del obligado al pago) adoptadas en un proceso matrimonial sujeto al Derecho civil de Cataluña. Lo presenta el progenitor demandado en el incidente, una vez emplazado para contestar (art. 775 LEC y art. 233-7 del Código Civil de Cataluña).

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contestación a la demanda de modificación de medidas de un proceso matrimonial (Derecho catalán)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contestación a la demanda de modificación de medidas de un proceso matrimonial (Derecho catalán)” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:contestacion-demanda-modificacion-medidas-proceso-civ-0108`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS DEL SOLICITANTE (2 veces)
- [ ] Nº (2 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] SEDE (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] EDAD
- [ ] FECHA
- [ ] IMPORTE
- [ ] LOCALIDAD
- [ ] MES
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] NOMBRE Y APELLIDOS DEL REPRESENTADO/A
- [ ] NÚMERO

## Normas que cita el formulario

- art. 233 Código Civil
- art. 769 LEC
- art. 775 LEC
- art. 749.2 LEC

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

A LA SECCIÓN [ELEGIR: DE FAMILIA, INFANCIA Y CAPACIDAD / CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, en la representación que ostento de D./Dña. [NOMBRE Y APELLIDOS DEL REPRESENTADO/A], según tengo acreditado en autos ante la Sección [ELEGIR: Civil / de Familia, Infancia y Capacidad] del Tribunal de Instancia, comparezco y, como mejor proceda en Derecho, DIGO:

Que, habiendo sido emplazado/a para contestar a la solicitud deducida por la representación de D./Dña. [NOMBRE Y APELLIDOS DEL SOLICITANTE], de modificación de medidas definitivas adoptadas en la sentencia de fecha [FECHA], dictada en el proceso matrimonial número [Nº DE PROCEDIMIENTO], por medio del presente escrito me opongo a dicha solicitud, contestación que baso en los siguientes

HECHOS

Se acepta el correlativo, habiéndose decretado en virtud de sentencia firme de divorcio dictada en estos autos por la Sección [ELEGIR: Civil / de Familia, Infancia y Capacidad] del Tribunal de Instancia de [SEDE], plaza n.º [Nº], en autos [Nº DE PROCEDIMIENTO], la disolución por divorcio del matrimonio de mis representados, fijando, entre otras medidas definitivas y por lo que ahora interesa, una pensión alimenticia a favor de los hijos comunes, a satisfacer por el solicitante por importe de [IMPORTE] euros mensuales, actualizables conforme al índice del IPC.

No se acepta el correlativo, puesto que no ha existido ninguna alteración sustancial de las circunstancias que se tuvieron en cuenta para adoptar la medida.

El/La demandante pretende que se minore la pensión alimenticia para los hijos comunes por cuanto ha formado una nueva familia y ha tenido [NÚMERO] hijo/s de [EDAD], por lo cual manifiesta que se han modificado las circunstancias tenidas en cuenta a la hora de adoptar la sentencia.

En primer lugar, debe subrayarse que no es de aplicación el art. 233-18 del Código Civil de Cataluña para el caso de pensión alimenticia de los hijos, puesto que se refiere a la incidencia de los nuevos gastos familiares en la prestación compensatoria a favor del otro cónyuge, y en este caso no se fijó dicha prestación compensatoria. Dicha previsión está pensada para priorizar el derecho de alimentos de los hijos sobre otras pensiones, pero no es el caso ahora contemplado, donde se está pretendiendo la reducción de la pensión a favor de los hijos.

Por tanto, es de aplicación el criterio reiterado expresado, entre otras muchas, en la SAP Barcelona de 19 de marzo de 2004, en el sentido de que la constitución de una nueva familia no es bastante para minorar la cuantía de los alimentos relativa a descendientes fruto de otra relación convivencial, pues la asunción voluntaria de nuevas obligaciones nunca ha de servir para exonerar al obligado de cumplir con las anteriormente asumidas, ni pueden, obviamente, perjudicar los derechos alimenticios de cualquiera de sus descendientes. Por otra parte, los ingresos del/de la demandante son más que suficientes para atender a las necesidades de sus hijos anteriores y a los de su nueva familia, dignos de toda protección, por lo que la circunstancia de tener nueva descendencia no puede ser entendida como sustancial para modificar la prestación alimenticia de los hijos del anterior matrimonio. En este sentido, la jurisprudencia viene interpretando que, para la modificación de una medida definitiva, es necesario que la modificación se funde en alteraciones verdaderamente trascendentes, fundamentales y no de escasa o de relativa importancia, que sean permanentes o duraderas y no coyunturales o transitorias, que no sean imputables a la voluntad de quien insta la modificación y que no hubieran sido previstas por los cónyuges o el juzgador en el momento en que fueron establecidas; en este caso, no existen circunstancias sobrevenidas, verdaderamente trascendentes, fundamentales y permanentes que impidan al/a la demandante hacer frente a la pensión fijada en la sentencia, por lo que nos oponemos a la pretensión deducida de contrario, debiendo desestimarse la solicitud.

A los anteriores hechos les son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

Competencia y procedimiento. Se acepta la competencia del Tribunal de conformidad con lo dispuesto en el art. 769 LEC, debiendo tramitarse por el procedimiento establecido en el art. 775 LEC.

Legitimación e intervención del Ministerio Fiscal. Se acepta, por cuanto la ostentan ambas partes por su condición de cónyuges del matrimonio. Procede la intervención del Ministerio Fiscal, por existir [ELEGIR: un hijo menor / hijos menores] de edad, conforme a lo previsto en el art. 749.2 LEC.

Improcedencia de la modificación de medidas. El art. 233-7 del Código Civil de Cataluña establece como requisito preceptivo para la modificación de medidas definitivas que se produzca una variación sustancial de las circunstancias que se tuvieron en cuenta al momento de dictarlas, no dándose los citados requisitos en el presente supuesto. No es de aplicación el art. 233-18 para la pensión alimenticia de los hijos.

Costas. Art. 394 LEC, debiendo imponerse las costas a la parte demandante incidental.

En su virtud,

SUPLICO AL TRIBUNAL: Que tenga por presentado este escrito con los documentos acompañados y sus copias; lo admita y tenga por contestada la solicitud de modificación de medidas definitivas deducida por la representación de D./Dña. [NOMBRE Y APELLIDOS DEL SOLICITANTE] y, tras los trámites legales, desestime la pretensión deducida de contrario, con imposición de costas a la parte demandante.

Es justicia que insto en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a y del Procurador/a
