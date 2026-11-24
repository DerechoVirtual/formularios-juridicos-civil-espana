---
name: oposicion-demandante-declinatoria-arbitraje-alegando-civ-1772
description: "Oposición del demandante a la declinatoria por arbitraje alegando nulidad del convenio arbitral. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Oposición del demandante a la declinatoria por arbitraje alegando nulidad del convenio arbitral

> Formulario **CIV-1772** del plugin **Mediación, MASC, arbitraje y jurisdicción voluntaria** (`formularios-mediacion-arbitraje-y-voluntaria`) · Civil › Jurisdicción voluntaria, MASC, mediación y arbitraje · normativa revisada el 24-11-2026.

## Qué es

Escrito de la parte demandante por el que se opone a la declinatoria de jurisdicción propuesta por la demandada con base en un convenio arbitral, alegando la nulidad de la cláusula de sumisión a arbitraje incluida en un contrato de adhesión con un consumidor (en el ejemplo, un contrato de préstamo con una entidad de crédito). Se presenta en el plazo de cinco días desde el traslado de la declinatoria (art. 65 LEC).

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Oposición del demandante a la declinatoria por arbitraje alegando nulidad del convenio arbitral» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Oposición del demandante a la declinatoria por arbitraje alegando nulidad del convenio arbitral” para mi caso». También puedes invocarla directamente con `/formularios-mediacion-arbitraje-y-voluntaria:oposicion-demandante-declinatoria-arbitraje-alegando-civ-1772`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-mediacion-arbitraje-y-voluntaria:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Mediación, MASC, arbitraje y jurisdicción voluntaria) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] LOCALIDAD
- [ ] LOCALIDAD DE DOMICILIO
- [ ] LOCALIDAD DEL ARBITRAJE
- [ ] MES
- [ ] NOMBRE Y APELLIDOS DEL ABOGADO/A, Nº DE COLEGIADO
- [ ] NOMBRE Y APELLIDOS DEL DEMANDANTE
- [ ] Nº
- [ ] Nº DE CLÁUSULA
- [ ] Nº DE HECHO
- [ ] Nº DE PROCEDIMIENTO
- [ ] SEDE

## Normas que cita el formulario

- art. 63.2 LEC
- art. 65.1 LEC
- art. 65 LEC

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

- Junto a «…E PROCEDIMIENTO] A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA N.º [Nº] DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…upuesto específico», supuesto no recogido en la cláusula del contrato litigioso.»: el original citaba el art. 90.1 TRLGDCU, el art. 83.1 y el art. 57.4; comprobar su numeración y redacción vigentes en el RDLeg 1/2007 tras las reformas posteriores.

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

Juicio n.º [Nº DE PROCEDIMIENTO]

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA N.º [Nº] DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, actuando en representación de [NOMBRE Y APELLIDOS DEL DEMANDANTE], parte actora en este proceso según tengo acreditado en autos, ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que habiendo recibido traslado del escrito de declinatoria de jurisdicción por sumisión a arbitraje presentado por la parte demandada, por medio de este escrito y dentro del plazo de cinco días establecido legalmente, vengo a OPONERME A LA DECLINATORIA deducida de contrario en base a los siguientes

HECHOS

ÚNICO.– En la declinatoria presentada se indica que la cláusula [Nº DE CLÁUSULA] del contrato de préstamo cuya nulidad se pretende establece la sumisión de la controversia a arbitraje.

Negamos rotundamente la alegación fáctica realizada de contrario en el sentido de que mi representado no es consumidor, lo cual pretende concluir el demandado con la sola referencia a su condición de empresario que figura en sus datos personales, cuando en ningún momento se trata de un contrato referido a su actividad económica o profesional, sino de un crédito concertado para hacer frente a gastos familiares, según consta expresamente en el contrato, por lo que actuó como consumidor de un producto financiero en la contratación con la entidad demandada, domiciliándose los pagos en una libreta expresamente denominada de «consumidor».

Como ya indicábamos en el hecho [Nº DE HECHO] de la demanda, el contrato en cuestión es un contrato de adhesión elaborado unilateralmente por la entidad bancaria demandada, el cual está sujeto a las prescripciones de la Ley 7/1998, sobre condiciones generales de la contratación, puesto que está todo él prerredactado por la entidad de crédito aquí demandada, incluso el denominado «convenio arbitral», sin que contenga el mismo inciso alguno específico del caso, concertándose con una persona que tiene la condición de consumidor, como es mi mandante, por lo que la cláusula es nula según dispone el artículo 9.2 de la Ley de Arbitraje, que se remite a las normas reguladoras de este tipo de contratos, en este caso, la normativa de consumidores y usuarios (texto refundido de la Ley General para la Defensa de los Consumidores y Usuarios, RDLeg 1/2007) y la Ley de Condiciones Generales de la Contratación, de cuya regulación se deduce indiscutiblemente la nulidad de la cláusula en cuestión, como exponemos ampliamente en los fundamentos de derecho cuarto y quinto, y de ello la jurisdicción del órgano al que nos dirigimos.

FUNDAMENTOS DE DERECHO

Competencia

Para resolver la presente declinatoria corresponde al Tribunal que conoce del asunto ante el que sigue la tramitación de la causa (art. 63.2 LEC).

Legitimación

Le corresponde a esta parte ante su condición de demandante en las presentes actuaciones (art. 65.1 LEC).

Procedimiento

Es el previsto en el artículo 65 de la LEC.

Fondo de la declinatoria

Nulidad de pleno derecho del convenio arbitral. El convenio arbitral litigioso está incorporado a un contrato de adhesión que contraviene la normativa reguladora de los derechos de los consumidores y usuarios, concretamente el artículo 90.1 del texto refundido de la LGDCU aprobado por Real Decreto Legislativo 1/2007, dado que mi mandante intervino en su condición de consumidor y la cláusula de sumisión a arbitraje es nula por abusiva de conformidad con lo dispuesto en dicho precepto, a cuyo tenor son nulas por abusivas las cláusulas que establezcan «la sumisión a arbitrajes distintos del arbitraje de consumo, salvo que se trate de órganos de arbitraje institucionales creados por normas legales para un sector o un supuesto específico», supuesto no recogido en la cláusula del contrato litigioso.

En efecto, la cláusula de arbitraje enjuiciada entraña sin duda una restricción de las facultades procesales de mi representado, principalmente porque le priva del acceso a la tutela de los órganos jurisdiccionales estatales y subsidiariamente porque el arbitraje debería desarrollarse en [LOCALIDAD DEL ARBITRAJE], estando él domiciliado en [LOCALIDAD DE DOMICILIO], distante centenares de kilómetros de dicha ciudad, como es notorio, siendo que la entidad demandada, con sucursales en todo el territorio nacional, tiene el centro de negocios en dicha localidad.

El propio Tribunal de Justicia de la Unión Europea ha reafirmado en su sentencia de 4 de junio de 2009, C-243/08 (que analiza la validez de un pacto de sumisión al fuero del domicilio del profesional en un contrato de servicios de telefonía entre una empresa húngara y una abonada, y cita otros precedentes como las sentencias de 27 de junio de 2000, C-240/98, caso Océano Grupo Editorial y Salvat Editores, y de 26 de octubre de 2006, C-168/05, caso Mostaza Claro) las facultades de los jueces nacionales para examinar de oficio, particularmente en el marco del examen de la admisibilidad de la demanda, la abusividad de las cláusulas contenidas en contratos con los consumidores en cuanto dispongan de «los elementos de hecho y de derecho» necesarios para ello, con la única salvedad de que el consumidor, debidamente informado por el juez, renuncie a invocar esa abusividad. Entiende el TJUE que esa conclusión se corresponde con una de las premisas de la Directiva 93/13/CEE (inferioridad del consumidor frente al profesional tanto en orden a la capacidad de negociación como en lo relativo al nivel de información), y se justifica ya que el designio del legislador comunitario por que la protección dispensada en esa directiva al consumidor tenga un efecto verdaderamente útil exige la atribución al juez de potestades que propicien la transformación del «equilibrio formal» de las partes en el contrato en «equilibrio real». En el caso del arbitraje, es evidente la voluntad de la ley de prohibir los convenios arbitrales distintos del sistema arbitral de consumo insertos a modo de condición general en contratos con consumidores, limitando únicamente su validez si se adoptan cuando el consumidor está en condiciones de evaluar correctamente el alcance de la decisión, esto es, «una vez surgido el conflicto material o controversia entre las partes del contrato», no antes (artículo 57.4 de la LGDCU).

Fondo de la reclamación

La nulidad de la cláusula de sumisión a arbitraje determina la jurisdicción de los tribunales ordinarios. De acuerdo con lo expuesto, el artículo 9.2 de la Ley de Arbitraje prescribe la invalidez de las cláusulas contenidas en un contrato de adhesión que infrinjan las normas aplicables a este tipo de contratos, siendo indudable que la cláusula de arbitraje alegada por la demandada, en la medida en que redunda en una obstaculización de los derechos procesales del consumidor, es nula y ha de tenerse por no puesta, de conformidad con el artículo 83.1 de la LGDCU de 2007, lo que determina necesariamente la desestimación de la declinatoria de jurisdicción.

En base a lo anterior,

SUPLICO AL TRIBUNAL que me tenga por opuesto a la declinatoria formulada de contrario, dictando auto por el que se desestime la misma y se mantenga la competencia de este Tribunal, alzando la suspensión de la tramitación que en su día se decretó. Todo ello con expresa imposición de las costas derivadas de esta declinatoria a la parte proponente.

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma Abogado: [NOMBRE Y APELLIDOS DEL ABOGADO/A, Nº DE COLEGIADO]

Firma Procurador: [NOMBRE Y APELLIDOS DEL PROCURADOR/A]
