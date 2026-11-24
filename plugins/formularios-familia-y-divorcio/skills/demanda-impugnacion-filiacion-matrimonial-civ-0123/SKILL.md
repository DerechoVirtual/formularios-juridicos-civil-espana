---
name: demanda-impugnacion-filiacion-matrimonial-civ-0123
description: "Demanda de impugnación de filiación matrimonial. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de impugnación de filiación matrimonial

> Formulario **CIV-0123** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de impugnación de filiación matrimonial» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de impugnación de filiación matrimonial” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-impugnacion-filiacion-matrimonial-civ-0123`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] NOMBRE DEL MENOR (3 veces)
- [ ] DNI/NIE (2 veces)
- [ ] FECHA (2 veces)
- [ ] PÁGINA (2 veces)
- [ ] TOMO (2 veces)
- [ ] AÑO
- [ ] CALLE
- [ ] COLEGIO
- [ ] DÍA
- [ ] MES
- [ ] NOMBRE DE LA CLÍNICA
- [ ] Nº

## Normas que cita el formulario

- art. 85.1 LOPJ
- art. 5.2 Ley Orgánica 1/2025
- art. 136 Código Civil
- art. 753 Ley 1/2000

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

- Junto a «…A, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE Q.P.T.R.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE Q.P.T.R.C.

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales en nombre y representación de D. [NOMBRE Y APELLIDOS], mayor de edad, casado, con DNI [DNI/NIE] y [DNI/NIE], respectivamente, y domicilio a efectos de notificaciones en la calle [CALLE], sita en [LOCALIDAD], cuya representación procesal acreditaré el día que se determine mediante comparecencia apud acta ante el LAJ del Tribunal competente para conocer de este proceso, bajo la dirección técnica de D./Dña. [NOMBRE Y APELLIDOS], Abogado/a del Ilustre Colegio de Abogados de [COLEGIO], Colegiado núm. [Nº], ante este Tribunal comparezco y, como mejor proceda en Derecho y

DIGO

Que mediante el presente escrito y siguiendo instrucciones de mi mandante formulo demanda de impugnación legal de filiación matrimonial de [NOMBRE DEL MENOR], contra la demandada Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], que baso en los siguientes

HECHOS

Que el día [FECHA] D. y Dña. contrajeron matrimonio civil en Valencia, que quedó inscrito en el Registro Civil de dicha localidad, en el Tomo [TOMO] y Página [PÁGINA], cuya certificación literal de matrimonio se aporta como DOCUMENTO núm. 1.

Que fruto de dicho matrimonio ha nacido y vive una hija llamada [NOMBRE DEL MENOR], nacida el día [FECHA], constando inscrito su nacimiento en el Registro Civil de [LOCALIDAD], al Tomo [TOMO], Página [PÁGINA], cuya certificación literal de nacimiento como hijo matrimonial de ambos se aporta en prueba como DOCUMENTO núm. 2.

Que después del nacimiento de la hija, mi representado D. tuvo conocimiento de que meses antes de comunicarle la noticia del embarazo, su mujer Dña. fue inseminada sin conocimiento ni consentimiento del marido. Con la finalidad de salir de la duda sobre si la menor era hija suya o no, practicó a la menor las correspondientes pruebas biológicas para la determinación de su paternidad, que resultaron negativas. En prueba se presenta el informe médico emitido por la Clínica [NOMBRE DE LA CLÍNICA], que se aporta como DOCUMENTO número 3.

A estos hechos, son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

COMPETENCIA JURISDICCIONAL: La competencia objetiva: Es de aplicación el párrafo 3º del artículo 117 de la Constitución española, que asigna exclusivamente a los Juzgados y Tribunales determinados por las Leyes, el ejercicio de la potestad jurisdiccional en todo tipo de procesos, juzgando y haciendo ejecutar lo juzgado. La competencia territorial: Hay que atenerse a lo dispuesto en el artículo 769 de la Ley de Enjuiciamiento Civil, en relación con lo dispuesto en el art. 85.1º LOPJ, que hace referencia al Tribunal de Instancia del lugar del último domicilio común de los progenitores. Por consiguiente, al estar fijado su último domicilio en [LOCALIDAD], que es donde reside además la demandada en la actualidad, resulta competente el Tribunal de Instancia de dicha provincia ciudad.

LEGITIMACIÓN DE LAS PARTES: Mi representado se encuentra en pleno ejercicio de sus derechos civiles y no está incurso en causa de incapacitación alguna, por lo que tienen la capacidad procesal establecida en los arts. 6.1 y 7.1 de la Ley de Enjuiciamiento Civil. Además mi mandante se encuentra legitimado activamente y el contrario pasivamente, pues según el artículo 766 de la Ley de Enjuiciamiento Civil, serán parte demandada en estos procesos, si no hubieran interpuesto ellos la demanda, las personas a las que en ésta se atribuya la condición de progenitores y de hijo, cuando se pida la determinación de la filiación.

CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD: La presente demanda no está sujeta al previo intento de resolución de controversias en vía no jurisdiccional por tratarse de materias excluidas del requisito de procedibilidad de acuerdo con el art. 5.2 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

DERECHO SUSTANTIVO: De acuerdo con lo establecido en el segundo apartado del art. 136 del Código Civil, que le permite al padre impugnar la paternidad de la filiación inscrita como suya en el Registro Civil.

PROCEDIMIENTO: El procedimiento por el que se sustanciarán los procesos de impugnación de filiación legalmente determinada es el verbal de conformidad con el artículo 753 de la Ley 1/2000, de 7 de enero, de Enjuiciamiento Civil. Es posible imputar las costas derivadas del mismo de acuerdo con lo previsto en el artículo 394 de la citada Ley.

Por todo lo cual,

SUPLICO AL TRIBUNAL: Que tenga por presentado este escrito de demanda así como los documentos que lo acompañan y copias de todo ello y se sirva admitirlo, teniéndome por parte en la representación acreditada, y por formulada DEMANDA de impugnación de filiación matrimonial de [NOMBRE Y APELLIDOS], contra Dª. y en tal sentido dicte, en su día, previo los trámites legales oportunos y la práctica de pruebas que considere pertinentes, sentencia por la que se acuerde declarar que no siendo D. [NOMBRE Y APELLIDOS], progenitor de [NOMBRE DEL MENOR], no se deriva obligación legal alguna como progenitor, y mande en su día que quede sea inscrita la misma en el asiento correspondiente en el Registro Civil; e imponga las costas que del procedimiento se deriven.

Es justicia que pido en la Ciudad de [LOCALIDAD], a [DÍA] de [MES] de [AÑO]

Fdo. Procurador/a

D./Dña. [NOMBRE Y APELLIDOS]

Fdo. Letrado/a

D./Dña. [NOMBRE Y APELLIDOS]

========================================================================
