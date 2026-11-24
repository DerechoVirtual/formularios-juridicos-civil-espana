---
name: escrito-perito-designado-rechaza-cargo-causa-civ-0857
description: "Escrito del perito designado que rechaza el cargo por causa justificada. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito del perito designado que rechaza el cargo por causa justificada

> Formulario **CIV-0857** del plugin **Proceso civil: demandas, contestaciones, prueba y vista** (`formularios-proceso-civil`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 24-11-2026.

## Qué es

Escrito del perito designado declinando su nombramiento por coincidir con la realización de pruebas médicas

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito del perito designado que rechaza el cargo por causa justificada» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito del perito designado que rechaza el cargo por causa justificada” para mi caso». También puedes invocarla directamente con `/formularios-proceso-civil:escrito-perito-designado-rechaza-cargo-causa-civ-0857`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-proceso-civil:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso civil: demandas, contestaciones, prueba y vista) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] NÚMERO (2 veces)
- [ ] AÑO
- [ ] CALLE
- [ ] DNI/NIE
- [ ] ENFERMEDAD
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] NOMBRE DEL HOSPITAL
- [ ] PROFESIÓN
- [ ] SEDE
- [ ] TIPO DE INTERVENCIÓN

## Normas que cita el formulario

- art. 138.3 Ley 15/2015
- art. 38 Ley 50/1980
- art. 138.3 LJV
- art. 138 LJV

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

A LA SECCIÓN DE LO MERCANTIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS], con DNI [DNI/NIE], de profesión [PROFESIÓN], y domicilio profesional en [LOCALIDAD], calle [CALLE], nº [NÚMERO], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que por medio del presente escrito, y de conformidad con el art. 138.3 de la Ley 15/2015, de 2 de julio, de la Jurisdicción Voluntaria (en lo sucesivo, LJV), comparezco para alegar justa causa y no aceptar el nombramiento como perito. Todo ello, en base a los siguientes

Hechos y consideraciones jurídicas:

1.ª) El pasado [FECHA] se me notificó decreto del Letrado de la Administración de Justicia del órgano al cual tengo el honor de dirigirme, en el que se comunicaba mi nombramiento como tercer perito conforme a lo dispuesto en el art. 38 de la Ley 50/1980, de 8 de octubre, de Contrato de Seguro (en lo sucesivo, LCS), en el marco del expediente de jurisdicción voluntaria tramitado con nº [NÚMERO]/[AÑO].

2.ª) Que en la referida comunicación se me requería para que en el plazo legal de dos días previsto en el art. 342.1 de la Ley de Enjuiciamiento Civil, compareciera en el Tribunal, y manifestara si acepto el cargo.

3.ª) Que por medio del presente escrito, y dentro del plazo indicado, comparezco y manifiesto mi voluntad de no aceptar el cargo, alegando justa causa, tal y como dispone el art. 138.3 LJV. En este sentido, el próximo [FECHA] tengo cita en el Hospital de [NOMBRE DEL HOSPITAL], para someterme a una operación de [TIPO DE INTERVENCIÓN], prescrita médicamente para recuperarme de la enfermedad crónica de [ENFERMEDAD] que padezco desde hace tres años. El cirujano que realizará la operación,
Dr. D. [NOMBRE Y APELLIDOS]
Dra. Dña.
[NOMBRE Y APELLIDOS], ha indicado un periodo mínimo de recuperación de cinco semanas, incompatible con el plazo de 30 días previsto en el apartado cuarto del citado precepto legal. Acompaño a este escrito certificado médico expedido por el mencionado facultativo, en el cual se recogen todos los extremos expuestos.

4.ª) En consecuencia, y en virtud de dicha justa causa, manifiesto mi voluntad de no aceptar el cargo, solicitando que, conforme al art. 342.2 de la Ley de Enjuiciamiento Civil, el Letrado de la Administración de Justicia considere aquella suficiente, sustituyéndome por el perito siguiente en la lista correspondiente.

Por todo lo expuesto, al amparo del art. 138 LJV,

SUPLICO AL TRIBUNAL

Que teniendo por presentado este escrito se me tenga por no aceptado en el nombramiento de tercer perito, y se considere suficiente la justa causa alegada para ello, sustituyéndome por el siguiente perito tasador de seguros de la lista correspondiente.

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma del perito
