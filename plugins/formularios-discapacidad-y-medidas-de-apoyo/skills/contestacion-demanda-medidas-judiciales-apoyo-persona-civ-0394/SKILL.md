---
name: contestacion-demanda-medidas-judiciales-apoyo-persona-civ-0394
description: "Contestación a la demanda de medidas judiciales de apoyo a persona con discapacidad. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contestación a la demanda de medidas judiciales de apoyo a persona con discapacidad

> Formulario **CIV-0394** del plugin **Discapacidad y medidas de apoyo (Ley 8/2021)** (`formularios-discapacidad-y-medidas-de-apoyo`) · Civil › Capacidad y medidas de apoyo · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contestación a la demanda de medidas judiciales de apoyo a persona con discapacidad» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contestación a la demanda de medidas judiciales de apoyo a persona con discapacidad” para mi caso». También puedes invocarla directamente con `/formularios-discapacidad-y-medidas-de-apoyo:contestacion-demanda-medidas-judiciales-apoyo-persona-civ-0394`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-discapacidad-y-medidas-de-apoyo:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Discapacidad y medidas de apoyo (Ley 8/2021)) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] FECHA (2 veces)
- [ ] AÑO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DÍA
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] MES
- [ ] NOMBRE DEL HOSPITAL
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº
- [ ] NÚMERO
- [ ] PROFESIÓN
- [ ] SEDE

## Normas que cita el formulario

- art. 756 LEC
- art. 753 LEC
- art. 249 CC
- art. 268 CC
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

### Avisos de actualización (3) — se aplican en el texto, nunca se copian en el documento

- Junto a «…Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).
- Junto a «…2666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.

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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D/Dª [NOMBRE Y APELLIDOS] Procurador de los Tribunales actuando en nombre y representación de D/Dª [NOMBRE Y APELLIDOS], mayor de edad, casado, de profesión [PROFESIÓN], vecino de esta ciudad C/, tal y como consta en la copia electrónica del poder notarial de representación informática (o digitalizada) que se adjunta, actuando bajo la dirección Letrada de D/Dª [NOMBRE Y APELLIDOS], Colegiado/a núm. con domicilio profesional en [LOCALIDAD], ante el Tribunal comparezco y como mejor proceda en Derecho DIGO:

Que en virtud del presente escrito en tiempo y forma paso a contestar y a oponerme a la demanda de adopción de medidas judiciales de apoyo seguido ante ese Tribunal con el número [NÚMERO], interpuesta por la representación procesal de D/Dª [NOMBRE Y APELLIDOS], en base a los siguientes

HECHOS

PRIMERO.- El demandante que solicita la adopción de medidas judiciales de apoyo y nombramiento de curador de mi representado lo hace en base al supuesto estado mental que determina «una situación que le impide el gobierno de su persona», aportándose un informe médico expedido por el departamento de salud mental del hospital [NOMBRE DEL HOSPITAL] en el que se le diagnostica un «trastorno ciclotímico».

SEGUNDO.- No obstante, tal y como se expone en el informe médico psiquiátrico elaborado por el Doctor en psiquiatría D. [NOMBRE Y APELLIDOS] que se aporta como DOCUMENTO NÚM. 1, «la ciclotimia es una patología maniaco-depresiva pero de menor entidad, sin síntomas alucinatorios o delirantes y con menor repercusión en la actividad social y familiar del sujeto», por lo cual dicha patología en modo alguno afecta a la capacidad jurídica de mi representado, tal como ya se alegó en el escrito de oposición presentado en el expediente de jurisdicción voluntaria seguido previamente.

TERCERO.- Además, si bien es cierto que mi representado estuvo recibiendo tratamiento psiquiátrico continuado durante las fechas que se refieren de contrario, hay que señalar que en la actualidad se encuentra dado de alta desde fecha [FECHA], tal y como se señala en el informe de alta expedido por el Psiquiatra Dr. D. [NOMBRE Y APELLIDOS], sin mayores secuelas que el encontrarse sometido a tratamiento farmacológico y seguimientos periódicos, tal y como consta en el DOCUMENTO NÚM. 1 aportado.

CUARTO.- En ningún caso son ciertas las afirmaciones vertidas de contrario en el expositivo tercero de la demanda formulada de contrario atribuyendo a mi representado «actividades desordenadas, vida caótica, consumo de alcohol y falta de capacidad para la dirección de los negocios de antigua titularidad paterna que han hecho que los mismos se encuentren en una situación próxima a la defenestración».

QUINTO.- Desde que en fecha [FECHA] mi representado recibió por fallecimiento de su padre D. la titularidad de las siguientes mercantiles [DENOMINACIÓN SOCIAL] la gestión de las mismas ha sido impecable aumentándose el volumen de negocio en un %, tal y como consta en el informe expedido por el Auditor de cuentas Colegiado núm. D. Que se aporta como DOCUMENTO NÚM. 2.

A los anteriores hechos le son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

I. COMPETENCIA.

De acuerdo con lo establecido en el artículo 756 LEC corresponderá la competencia al Tribunal de Instancia al que me dirijo, por resultar que el demandado tiene su domicilio en la misma.

II. PROCEDIMIENTO.

De acuerdo con lo establecido en el artículo 753 LEC, el presente procedimiento se sustanciará por los trámites del Juicio verbal, con las especialidades establecidas en los artículos 748 y ss. LEC y respecto al proceso de adopción de las medidas judiciales de apoyo de los artículos 756 y ss. LEC.

III. ADOPCIÓN DE MEDIDAS JUDICIALES DE APOYO: IMPROCEDENCIA

El art. 249 del CC establece que las medidas de apoyo a las personas mayores de edad o menores emancipadas que las precisen para el adecuado ejercicio de su capacidad jurídica tendrán por finalidad permitir el desarrollo pleno de su personalidad y su desenvolvimiento jurídico en condiciones de igualdad. Estas medidas de apoyo deberán estar inspiradas en el respeto a la dignidad de la persona y en la tutela de sus derechos fundamentales. Las de origen legal o judicial solo procederán en defecto o insuficiencia de la voluntad de la persona de que se trate. Todas ellas deberán ajustarse a los principios de necesidad y proporcionalidad, no cumpliéndose los requisitos para su adopción.

Tampoco se cumplen los requisitos de los arts. 268 y siguientes del CC para la constitución de la curatela, al tener mi representado suficiente capacidad jurídica para gobernarse por sí mismo.

IV. COSTAS.

El artículo 394 LEC.

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL: Tenga por presentado este escrito con los documentos anexos, justificante de traslado de copias, teniendo por comparecido al Procurador de los Tribunales D. [NOMBRE Y APELLIDOS], en representación de [NOMBRE DEL REPRESENTADO/A], entendiéndose conmigo las sucesivas diligencias, teniendo por contestada la demanda de adopción de medidas judiciales de apoyo formulada por la representación procesal de D. [NOMBRE Y APELLIDOS] y seguido el juicio por todos sus trámites se dicte sentencia en virtud de la cual se absuelva libremente a mi representado de la totalidad de pedimentos formulados de contrario, con imposición de costas a la demandante.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma Abogado y Procurador

========================================================================
