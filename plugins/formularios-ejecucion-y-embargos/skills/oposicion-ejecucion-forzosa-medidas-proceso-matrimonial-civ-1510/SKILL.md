---
name: oposicion-ejecucion-forzosa-medidas-proceso-matrimonial-civ-1510
description: "Oposición a la ejecución forzosa de medidas de un proceso matrimonial. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Oposición a la ejecución forzosa de medidas de un proceso matrimonial

> Formulario **CIV-1510** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Oposición a la ejecución forzosa de medidas de un proceso matrimonial» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Oposición a la ejecución forzosa de medidas de un proceso matrimonial” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:oposicion-ejecucion-forzosa-medidas-proceso-matrimonial-civ-1510`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] AÑO (2 veces)
- [ ] FECHA (2 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] DÍA
- [ ] IMPORTE
- [ ] LUGAR
- [ ] MES
- [ ] NOMBRE DE LA PARTE
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] NOMBRE Y APELLIDOS
- [ ] Nº
- [ ] SEDE
- [ ] ÓRGANO JUDICIAL

## Normas que cita el formulario

- art. 559.1.3 LEC
- art. 776.4 LEC
- art. 556 LEC
- art. 776 LEC

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

- Junto a «…Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Denominación legal: Sección de Familia, Infancia y Capacidad. Si no existe en el partido, conoce la Sección Civil o la Única (art. 86.3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «….3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

PROCEDIMIENTO DE DIVORCIO Nº [Nº DE PROCEDIMIENTO]

TRIBUNAL [ÓRGANO JUDICIAL]

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D. [NOMBRE Y APELLIDOS] Procurador de los Tribunales, en nombre y representación de [NOMBRE DEL REPRESENTADO/A], parte ejecutada en el procedimiento de ejecución arriba referenciado, según tengo acreditado en autos, ante el Tribunal comparezco y como mejor proceda en Derecho DIGO:

Que dentro del plazo concedido paso a formular OPOSICIÓN A LA EJECUCIÓN instada basada en defectos procesales, al amparo del art. 559.1.3º de la LEC por nulidad radical del despacho de ejecución (en su caso, se alegarían otros motivos conforme a los artículos 556 y 559.1 ), ello en base a los siguientes:

HECHOS

La pretensión formulada por la parte ejecutante de que mi representado abone como gastos extraordinarios los correspondientes a clases extraescolares de inglés, de baloncesto, piano y mecanografía, así como los correspondientes a campamentos de verano, cuotas mensuales de colegio en el que viene escolarizada la menor, intercambios de verano de el año [AÑO] y gastos farmacéuticos, dio lugar al auto despachando ejecución al que ahora nos oponemos por infringir lo dispuesto en el art. 776.4ª de la LEC, en tanto que no se ha sustanciado el trámite previo para declarar la procedencia de los gastos extraordinarios y determinar su cuantía.

En efecto, ninguno de los gastos reclamados pueden ejecutarse con amparo en el pronunciamiento de la sentencia firme de divorcio en concepto de gastos extraordinarios, los cuales se caracterizan por carecer de una periodicidad prefijada, en cuanto dimanantes de sucesos de imprevisible o difícil previsión apriorística, de tal modo que pueden surgir o no, debiendo además vincularse a necesidades que han de cubrirse de modo ineludible, en orden al cuidado, desarrollo y formación en todos los órdenes del menor. A mayor abundamiento, ninguno de los desembolsos ahora reclamados constituyen gastos extraordinarios, pues ni son imprevisibles, ni han sido realizados con la anuencia de mi representado.

En este caso, según se desprende del convenio regulador de fecha [FECHA], aprobado por sentencia firme de fecha [FECHA], los gastos ahora reclamados estaban contemplados en la cantidad a tanto alzado establecida como pensión alimenticia por importe de [IMPORTE] euros, y ello en tanto que eran gastos y actividades extraescolares ya desarrolladas por el menor con anterioridad a que los cónyuges suscribieran dicho convenio, de manera que no pueden ampararse en la presente ejecución cantidades ya incluidas en la pensión alimenticia y por educación, por ausencia del presupuesto básico de la ejecución, no otro que contener pronunciamiento de condena al pago de determinada obligación.

Asimismo, el auto infringe lo dispuesto en el art. 776.4 de la LEC en cuanto a que establece un cauce específico para la integración y liquidación de conceptos no expresamente contemplados en el marco de la sentencia que constituye el título de ejecución, de tal manera que si los conceptos por los que se reclama no vienen expresamente contemplados en el título, como ocurre en este caso, no se produce incumplimiento de las obligaciones impuestas en el mismo, y por tanto en este marco de un juicio de ejecución no se amparan las pretensiones de ejecución aquí sostenidas, de conformidad con lo dispuesto en el artículo 559.1.3º de la L.E.Civil.

A los anteriores hechos le son aplicables los siguientes

FUNDAMENTOS DE DERECHO

Procedimiento

Artículo 776 de la LECiv, en relación con los artículos 556 y 559 de la LEC.

Legitimación

Artículo 556.1 LECiv, al ser parte ejecutada en el presente proceso de ejecución [Nº DE PROCEDIMIENTO].

Oposición a la ejecución

Por defectos procesales fundada en el artículo 776 de la LECiv en relación con los artículos 559.1.3º y 776.4º de la LECiv respecto a la nulidad del despacho de ejecución por no cumplir el documento presentado los requisitos legales exigidos.

Costas

Han de imponerse al ejecutante de conformidad con los artículos 539.2 y 559.2.2 LECiv.

En su virtud,

SUPLICO AL TRIBUNAL: Tenga por presentado este escrito, documentos y copias, se sirva admitirlos y unirlos a autos, teniendo por formalizada, en tiempo y forma, oposición a la demanda ejecutiva instada por [NOMBRE DE LA PARTE] contra mi mandante, y previa sustanciación, con suspensión de la ejecución, estime la oposición deducida y proceda a dictar auto dejando sin efecto la ejecución despachada, condenando en costas al ejecutante.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

========================================================================
