---
name: demanda-alimentos-hijo-contra-padres-civ-0125
description: "Demanda de alimentos de un hijo contra sus padres. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de alimentos de un hijo contra sus padres

> Formulario **CIV-0125** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de alimentos de un hijo contra sus padres» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de alimentos de un hijo contra sus padres” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-alimentos-hijo-contra-padres-civ-0125`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (10 veces)
- [ ] IMPORTE (8 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] Nº (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] SEDE (2 veces)
- [ ] AÑO
- [ ] CALLE
- [ ] DENOMINACIÓN SOCIAL
- [ ] DÍA
- [ ] LUGAR
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] MES
- [ ] Nº DE CURSO
- [ ] PERIODICIDAD

## Normas que cita el formulario

- art. 50.1 LEC
- art. 437 LEC
- art. 250.1.8 LEC
- art. 266.2 LEC
- art. 237 Código Civil
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 394 LEC
- art. 251 LEC

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

### Avisos de actualización (4) — se aplican en el texto, nunca se copian en el documento

- Junto a «…NCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.R.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.
- Junto a «…n [NOMBRE Y APELLIDOS] ante la Sección Civil del Tribunal de Instancia de [SEDE]»: Un solo TI por partido judicial (art. 84.1 LOPJ): sobra «de los de». Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).
- Junto a «…ue por turno de reparto corresponda (o Sección de Familia, Infancia y Capacidad)»: Denominación legal: Sección de Familia, Infancia y Capacidad. Si no existe en el partido, conoce la Sección Civil o la Única (art. 86.3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).

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

Don [NOMBRE Y APELLIDOS] Procurador de los Tribunales, en la representación que ostento de D [NOMBRE Y APELLIDOS], según acredito mediante designación apud-acta otorgada ante el Letrado de la Administración de Justicia [NOMBRE Y APELLIDOS] (o mediante escritura de poderes que acompaño para su unión a los autos por medio de testimonio, previo cotejo y devolución del original), y bajo la dirección Letrada de Don [NOMBRE Y APELLIDOS] ante la Sección Civil del Tribunal de Instancia de [SEDE] que por turno de reparto corresponda (o Sección de Familia, Infancia y Capacidad) comparezco y como mejor proceda en Derecho, DIGO:

Que en la representación que ostento, mediante este escrito y los documentos que lo acompañan, vengo a formular demanda en solicitud de alimentos por parte de mi principal contra sus padres D y Dª, con domicilio en la calle [CALLE], núm. [Nº] de

Baso la demanda en los siguientes

HECHOS

Mi representado es hijo de los demandados D [NOMBRE Y APELLIDOS] y Dª [NOMBRE Y APELLIDOS], siendo en la actualidad mayor de edad (Aporto junto a esta demanda, certificados de nacimiento, matrimonio y copia del libro de familia como documentos número).

Mi representado tiene [Nº] años, vive de forma independiente a sus padres en un piso compartido con otros estudiantes, y está actualmente estudiando [Nº DE CURSO] curso del grado de en la Universidad de [LOCALIDAD], no teniendo ningún tipo de ingresos, por lo que se ven la necesidad de demandar el pago de alimentos a sus padres para continuar con su formación, conforme a lo que disponen los artículos 237-1, 237-4, 237-6 y concordantes del Código Civil de Cataluña.

Tal como se ha indicado, mi representado vive de forma independiente a sus padres, no percibiendo ningún tipo de ingreso, puesto que sus padres, al inicio de este curso dejaron de abonarle cualquier cantidad para su manutención al instalarse en un piso compartido con otros compañeros.

Por tanto, mi representado precisa del abono de alimentos para continuar su formación, puesto que actualmente está cursando los estudios universitarios que corresponden a su edad, habiendo obtenido un rendimiento académico excelente en los cursos anteriores, tal como se acredita por el expediente académico que se acompaña como documento número

Además de las necesidades ordinarias de mi representado de alimento y vestido, debe hacer frente periódicamente a los siguientes gastos (se relacionarían) [PERIODICIDAD]: a) en concepto de matrícula, libros y material la cantidad de [IMPORTE] anuales (se acompañan recibos y justificantes correspondientes al curso anterior); b) en concepto de alquiler, está abonando un importe de [IMPORTE] Euros mensuales (se acompañan recibos de las dos últimas mensualidades como documentos número [Nº DE DOCUMENTO])

Los padres de mi representado tienen una situación económica muy buena, sin otras cargas familiares, puesto que mi representado es hijo único.

Así, y en cuanto al padre, tiene un negocio de por el que tiene unos ingresos mensuales de [IMPORTE] euros.

Por su parte, la madre de mi representada trabaja en la empresa [DENOMINACIÓN SOCIAL] y percibe una remuneración total de [IMPORTE] euros mensuales.

Asimismo, poseen en propiedad la vivienda en que residen y dos inmuebles en las localidades de [LOCALIDAD], los cuales tienen arrendados y perciben unas rentas de [IMPORTE] euros mensuales en total (se acompañan declaraciones de IRPF de los padres de mi representado).

Dadas las necesidades del hijo y las posibilidades de los padres, esta parte entiende que éstos deberían abonar mensualmente a su hijo, en la proporción que se fije por V.I., una cantidad de [IMPORTE] euros, pagaderos los cinco primeros días de cada mes, mediante ingreso en cuenta corriente que a tal efecto se designará por mi principal, cantidad que deberá ser revisada anualmente a fin de ajustarse al índice de precios al consumo, o en virtud de cualquier otro que, en su caso, fije el Instituto Nacional de Estadística u organismo oficial competente que lo sustituya.

Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

FUNDAMENTOS DE DERECHO

Competencia. Es competente el Tribunal de Instancia de esta ciudad, por ser éste el del domicilio del demandado, al amparo del art. 50.1 de la LEC.

Procedimiento. La tramitación del proceso se ajustará a lo establecido en el art. 437 y siguientes de la LEC para el juicio verbal, por aplicación del art. 250.1.8º de la LEC. Al amparo del art. 266.2º de la LEC acompaño a esta demanda los documentos que justifican la pretensión objeto de este proceso.

Legitimación. Mi representado está legitimada activamente para interponer esta demanda al amparo del art. 237-4 del Código Civil de Cataluña y los demandados lo están pasivamente como ascendientes, al amparo del art. 237-2.1 y 237-6 del Código Civil de Cataluña.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

Fundamentos del derecho a alimentos. Son de aplicación el artículo 237-1 (contenido), 237-5 (nacimiento del derecho); 237-7 (pluralidad de obligados); 237-9 (cuantías) y 237-10 (cumplimiento de la obligación), y demás preceptos concordantes.

Costas. Con arreglo a lo establecido en el art. 394 de la LEC procede imponer las costas de este proceso a la parte demandada.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL Que tenga por presentado este escrito con sus copias y documentos acompañados, teniéndome por comparecido y parte en la representación que ostento de D [NOMBRE Y APELLIDOS], tenga por interpuesta demanda en solicitud de alimentos contra D [NOMBRE Y APELLIDOS] y Dª [NOMBRE Y APELLIDOS], y, previos los trámites legales que procedan, dicte en su día sentencia por la que se estime la demanda, se declare el derecho de D [NOMBRE Y APELLIDOS] a percibir alimentos y se condene a los demandados, en la proporción que se determine, al pago de alimentos a su hijo fijando la suma de [IMPORTE] euros mensuales, pagaderos anticipadamente, los cinco primeros días de cada mes, mediante ingreso en la cuenta corriente que a tales efectos se designará, tan pronto esta parte sea requerida para ello, cantidad que se revisará anualmente por el IPC, o por cualquier otro que, a dichos efectos, señale el Instituto Nacional de Estadística u organismo oficial competente que lo sustituya, con expresa imposición de costas a la parte contraria dado que su absoluta desatención ha motivado la interposición de esta demanda.

OTROSÍ PRIMERO DIGO: Que la cuantía de este proceso se fija en [IMPORTE] euros al amparo de la regla 7ª del art. 251 de la LEC.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

firma del Procurador y Abogado

========================================================================
