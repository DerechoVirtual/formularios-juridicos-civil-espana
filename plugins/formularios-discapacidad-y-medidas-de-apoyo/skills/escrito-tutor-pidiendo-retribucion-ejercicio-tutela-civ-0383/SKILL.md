---
name: escrito-tutor-pidiendo-retribucion-ejercicio-tutela-civ-0383
description: "Escrito del tutor pidiendo retribución por el ejercicio de la tutela. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito del tutor pidiendo retribución por el ejercicio de la tutela

> Formulario **CIV-0383** del plugin **Discapacidad y medidas de apoyo (Ley 8/2021)** (`formularios-discapacidad-y-medidas-de-apoyo`) · Civil › Capacidad y medidas de apoyo · normativa revisada el 24-11-2026.

## Qué es

Órgano jurisdiccional Parte interesada (tutor) Motivación de la complejidad de Gestión de los bienes del tutelado HECHOS FUNDAMENTOS DE DERECHO Suplico Otrosí digo Lugar y fecha Firmas

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito del tutor pidiendo retribución por el ejercicio de la tutela» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito del tutor pidiendo retribución por el ejercicio de la tutela” para mi caso». También puedes invocarla directamente con `/formularios-discapacidad-y-medidas-de-apoyo:escrito-tutor-pidiendo-retribucion-ejercicio-tutela-civ-0383`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-discapacidad-y-medidas-de-apoyo:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Discapacidad y medidas de apoyo (Ley 8/2021)) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] MES (4 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] AÑO (3 veces)
- [ ] DÍA (3 veces)
- [ ] Nº (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] SEDE (2 veces)
- [ ] CALLE
- [ ] IMPORTE
- [ ] LOCALIDAD
- [ ] LUGAR

## Normas que cita el formulario

- art. 274 Código Civil

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

- Junto a «…Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [NÚMERO]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.
- Junto a «…Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [NÚMERO]

Expediente de Jurisdicción Voluntaria: / [Nº DE PROCEDIMIENTO]

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D./D.ª [NOMBRE Y APELLIDOS], mayor de edad, con D.N.I. n.º [NÚMERO], y domicilio en [LOCALIDAD], calle [CALLE], nº [NÚMERO], pta., como tutor de D./Dª [NOMBRE Y APELLIDOS], ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que por medio del presente escrito SOLICITO QUE SE FIJE RETRIBUCIÓN POR EL EJERCICIO DEL CARGO DE TUTOR/CURADOR, conforme a lo dispuesto en el artículo 274 del Código Civil y 48 de la Ley de la Jurisdicción Voluntaria, con base en los siguientes

HECHOS

PRIMERO.- Fui nombrado tutor de D./Dª [NOMBRE Y APELLIDOS], por este Tribunal, en procedimiento de jurisdicción voluntaria [Nº DE PROCEDIMIENTO] /, por resolución de fecha [DÍA] de [MES] de [AÑO] Tras la prestación de fianza a que se refiere el artículo 46 de la Ley de la Jurisdicción Voluntaria y demás trámites legales, acepté el cargo en acta de fecha [DÍA] de [MES] de [AÑO], tras lo cual se me dio posesión del cargo.

SEGUNDO.- En la resolución por la que se efectuó mi nombramiento como tutor no se fijó retribución alguna.

TERCERO.- La complejidad de la administración del patrimonio del tutelado requiere muchas horas de dedicación, que no puedo emplear en realizar otro trabajo remunerado. A continuación se describen las circunstancias de las que deriva la complejidad de la citada administración y la dedicación que la misma requiere

CUARTO.- El patrimonio del tutelado y las rentas que produce son suficientes para que, a su cargo, se proceda a remunerar mi labor como tutor. A continuación se justifica tal alegación

QUINTO.- Con base en las circunstancias antes expuestas considero adecuada una retribución de [IMPORTE] euros anuales (o con periodicidad mensual, trimestral, o semestral, o la que se considere conveniente; o del [Nº] por ciento del rendimiento líquido de los bienes del tutelado). Esta remuneración permitiría cubrir los gastos que me reporta el desempeño de la función de tutor, sin menoscabar la debida atención de los intereses de mi pupilo.

Resultan aplicables a los anteriores hechos, los siguientes

FUNDAMENTOS DE DERECHO

PRIMERO.- El art. 274 del Código civil establece que el tutor tiene derecho a una retribución siempre que el patrimonio del tutelado lo permita. Corresponde al Juez fijar su importe y el modo de percibirlo, para lo cual tendrá en cuenta el trabajo a realizar y el valor y la rentabilidad de los bienes, procurando en lo posible que la cuantía de la retribución no baje del 4 por 100 ni exceda del 20 por 100 del rendimiento líquido de los bienes.

Por su parte, el art. 48 de la Ley de la Jurisdicción Voluntaria dispone: “1. Si se solicitare por el tutor o curador el establecimiento de una retribución y no estuviera fijada en la resolución que hubiera efectuado su nombramiento, el Juez la acordará siempre que el patrimonio del tutelado o asistido lo permita, fijará su importe y el modo de percibirla, atendiendo al trabajo a realizar y al valor y la rentabilidad de los bienes, después de oír al solicitante, al tutelado o asistido si tuviera suficiente madurez y, en todo caso, al menor si fuera mayor de 12 años, al Ministerio Fiscal y a cuantas personas considere oportuno. Tanto el Juez como las partes o el Ministerio Fiscal podrán proponer las diligencias, informes periciales y pruebas que estimen oportunas.

El auto a que se refiere este artículo se ejecutará sin perjuicio del recurso de apelación, que no producirá efectos suspensivos.

2. El mismo procedimiento se seguirá para modificar o extinguir dicha retribución”.

SEGUNDO.- Iura novit curia y los demás que en Derecho procedan.

En su virtud:

SUPLICO AL TRIBUNAL: Que teniendo por presentado este escrito, con los documentos que se acompañan, y copia de todo ello, se sirva admitirlo y, estimando lo que en él se solicita, y previos los trámites legales oportunos, dicte resolución por la que fije a mi favor, en calidad de tutor de D./Dª [NOMBRE Y APELLIDOS] la retribución anual del [Nº] por ciento del rendimiento líquido de los bienes del tutelado (se procurará en lo posible que la cuantía de la retribución no baje del 4 por 100 ni exceda del 20 por 100 del rendimiento líquido de los bienes, por requerirlo así el art. 274 del Código civil), a satisfacer, por años vencidos, en el mes de [MES].

OTROSÍ DIGO: Para acreditar los HECHOS de este escrito, se acompaña los siguientes DOCUMENTOS:

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Fdo.

El tutor

========================================================================
