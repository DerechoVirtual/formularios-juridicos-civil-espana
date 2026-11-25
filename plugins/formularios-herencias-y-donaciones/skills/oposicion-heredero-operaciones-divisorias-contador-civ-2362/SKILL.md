---
name: oposicion-heredero-operaciones-divisorias-contador-civ-2362
description: "Oposición del heredero a las operaciones divisorias del contador por error de cálculo. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Oposición del heredero a las operaciones divisorias del contador por error de cálculo

> Formulario **CIV-2362** del plugin **Herencias, testamentos y donaciones** (`formularios-herencias-y-donaciones`) · Civil › Sucesiones y donaciones · normativa revisada el 25-11-2026.

## Qué es

Escrito presentado por heredero parte en un proceso de división judicial de herencia, en el que se opone a las operaciones divisorias realizadas por el Contador-partidor.

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Oposición del heredero a las operaciones divisorias del contador por error de cálculo» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Oposición del heredero a las operaciones divisorias del contador por error de cálculo” para mi caso». También puedes invocarla directamente con `/formularios-herencias-y-donaciones:oposicion-heredero-operaciones-divisorias-contador-civ-2362`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-herencias-y-donaciones:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Herencias, testamentos y donaciones) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] COMPLETAR (7 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] FECHA (2 veces)
- [ ] Nº (2 veces)
- [ ] AÑO
- [ ] DESCRIBIR
- [ ] LUGAR
- [ ] Nº DE PROCEDIMIENTO
- [ ] SEDE

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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) Frente a la regulación de la LEC 1881, el artículo 787 de la LEC 1/2000 reduce a uno solo los dos trámites sucesivos para examen y oposición, fijando en diez días el plazo durante el cual pueden los interesados examinar las operaciones divisorias, al tiempo que les confiere explícitamente la posibilidad de obtener copias a su costa —vid. Disp. Adic. Cuarta LEC 1/2000—. Dentro de este mismo plazo, las partes pueden desplegar alguno de los siguientes comportamientos:

a) Aceptarlas tácitamente, dejando transcurrir el plazo sin evacuar alegación alguna;
b) Aceptarlas expresamente, manifestándolo así ante el órgano jurisdiccional, y aunque la norma no sea tan explícita como lo fuera el art. 1080 C.C., ha de entenderse que se mantiene la misma posibilidad de prestar este asentimiento por escrito o por comparecencia.

En estos dos casos, el Letrado de la Administración de Justicia aprobará por Decreto las operaciones realizadas ordenando su protocolización (art. 787.2). La ausencia de impugnación no impedirá, en su caso, que se pueda formular las acciones de rescisión por lesión o de nulidad de los arts. 1076 y 1079 C.C. —SS.T.S., 3 de diciembre de 1928, 7 de febrero de 1969, 3 de febrero de 1982 —.

c) Formalizar oposición, oportuna y formalmente —sólo por escrito, con firma de Abogado y Procurador—, expresando los particulares a que se contrae la disconformidad y el fundamento de la desavenencia. En este caso se citará a las partes y al contador a una comparecencia dentro de los diez días siguientes. Si en el curso de la misma se alcanzara algún acuerdo, luego de efectuadas, en su caso, las correcciones oportunas se aprobarán la operaciones divisorias por el Letrado de la Administración de Justicia mediante Decreto, acordando su protocolización.

Si se mantuvieren las desavenencias, luego de propuesta la prueba de que los interesados intenten valerse, continuará sustanciándose la oposición por los trámites del juicio verbal.

Acerca de las causas en que puede fundarse la oposición admite la doctrina —MANRESA; DE LA PLAZA; DE CASTRO GARCÍA— y la jurisprudencia —A.T.S. de 7 de julio de 1945, SS.T.S. de 30 de enero de 1951, 16 de noviembre de 1955— tanto las de índole adjetiva, relativas a la inobservancia de las normas de procedimiento establecidas en la Ley, cuanto las de carácter sustantivo, que puedan dar lugar a la nulidad o la rescisión.

A su vez, los interesados pueden fundar la oposición en la existencia de actuaciones presuntamente constitutivas de cohecho, de maquinaciones fraudulentas en los avalúos, o de falsedad documental. En tal caso, o si alguno de aquellos promoviese juicio penal en averiguación del ilícito punible se procederá en la forma ordenada en el art. 40 LEC 1/2000, suspendiéndose entre tanto el curso de los autos civiles, a menos que aquéllos renuncien al avalúo impugnado y presenten otro sobre el que recaiga absoluta conformidad..

(2) El Parlamento de Cataluña ha aprobado la Ley del Libro Cuarto del Código Civil de Cataluña. Las modificaciones se concentran, especialmente, en materia de formas testamentarias, pactos sucesorios, sucesión intestada, derechos del cónyuge viudo o conviviente, legítima y supresión de la reserva.

Amplía las causas de indignidad sucesoria a los delitos de violencia familiar y de género que establece, entre otros aspectos, que los condenados por violencia de género no tendrán derecho a la sucesión de su pareja.

En caso de muerte sin testamento, se reconocen los mismos derechos a todos los tipos de pareja, es decir, a los matrimonios y las uniones estables de pareja, heterosexuales u homosexuales. Concreta que lo relevante es la "existencia de una comunidad de vida estable y los lazos de afecto entre los que conviven como pareja, y no el carácter institucional del vínculo que los une".


### Flujo

1. **Paso 0**: comprueba Jurisprudenciator (arriba).
2. Lee entero `assets/formulario.md` (el formulario que vas a rellenar, en la carpeta de esta skill) y la parte de `../indice/marco.md` que afecte al caso. Limítate a la materia de este formulario: no añadas contenido ajeno a él.
3. Pide los datos de la lista en una sola tanda. Si un dato aparece varias veces, aclara a qué persona o acto corresponde cada vez. Lo que el usuario no sepa se queda como hueco visible con su etiqueta (p. ej. [FECHA]).
4. Resuelve cada [ELEGIR …] y cada [OPCIONAL …] según los hechos, y sustituye cualquier indicación entre paréntesis del formulario («(se describirá…)», «(indicar…)») por el contenido que corresponda. Redacta las partes que dependen del caso (hechos, motivos, descripción de bienes).
5. Aplica los avisos de actualización en el lugar que indican. Comprueba con `buscar_articulo` cada norma citada; si alguna ha cambiado, usa la redacción vigente. Si citas jurisprudencia, localízala con `buscar_sentencias` o `buscar_por_cita` y léela con `leer_sentencias`.
6. Antes de entregarlo, pasa `verificar_escrito` con las frases que citan normas o sentencias y corrige lo que señale.
7. **Documento final = el formulario tal cual, rellenado y limpio.**
   - Empieza exactamente por la primera línea de `assets/formulario.md` y sigue su estructura y su orden hasta la firma.
   - No pongas en el documento título, nombre del formulario o de la skill, código, encabezados, «Para qué sirve», leyendas, avisos, notas de uso, comentarios ni explicaciones. Tampoco marcas [ELEGIR…] u [OPCIONAL…]: ya están resueltas.
   - Formato Word (.docx, con la skill de Word disponible): **Times New Roman 11 pt** en todo el documento, **interlineado 1,15**, **texto justificado**, márgenes de 2,5 cm. Los rótulos del formulario (REUNIDOS, CLÁUSULAS, HECHOS, SUPLICO…) en su propia línea y en negrita, sin cambiar su texto.
8. En el chat (nunca dentro del documento): datos pendientes, partes redactadas por ti, normas y sentencias comprobadas con Jurisprudenciator (y, si algún dato sale de internet, cuál y su enlace) y, si es un escrito judicial o administrativo, el plazo y el órgano ante el que se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.
