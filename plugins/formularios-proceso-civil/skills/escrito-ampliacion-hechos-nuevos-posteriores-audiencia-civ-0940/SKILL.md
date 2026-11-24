---
name: escrito-ampliacion-hechos-nuevos-posteriores-audiencia-civ-0940
description: "Escrito de ampliación de hechos nuevos posteriores a la audiencia previa. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito de ampliación de hechos nuevos posteriores a la audiencia previa

> Formulario **CIV-0940** del plugin **Proceso civil: demandas, contestaciones, prueba y vista** (`formularios-proceso-civil`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito de ampliación de hechos nuevos posteriores a la audiencia previa» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito de ampliación de hechos nuevos posteriores a la audiencia previa” para mi caso». También puedes invocarla directamente con `/formularios-proceso-civil:escrito-ampliacion-hechos-nuevos-posteriores-audiencia-civ-0940`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-proceso-civil:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso civil: demandas, contestaciones, prueba y vista) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] IMPORTE (4 veces)
- [ ] FECHA (3 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE DEL HOSPITAL (2 veces)
- [ ] DESCRIPCIÓN DE LA INTERVENCIÓN
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº
- [ ] NÚMERO

## Normas que cita el formulario

- art. 286 LEC

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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA

D. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, actuando en representación de [NOMBRE DEL REPRESENTADO/A], según consta acreditado en el proceso ordinario número [NÚMERO] que se sigue ante ese Tribunal, comparezco y como proceda en Derecho DIGO:

-Que al amparo de lo dispuesto en el art. 286 de la LEC, y habiendo ocurrido en el día de ayer un hecho de relevancia para la decisión de este pleito, como es la operación quirúrgica de mi representado como consecuencia de las secuelas sufridas por el accidente y descritas en el hecho cuarto de nuestra demanda, formulo el presente ESCRITO DE AMPLIACIÓN DE HECHOS, alegando los siguientes:

PRIMERO.- Como consecuencia del atropello sufrido el día [FECHA], el demandante D. sufrió las lesiones y secuelas relatadas en el hecho cuarto de nuestro escrito de demanda, entre ellas la de

Como consecuencia del proceso degenerativo propio de la secuela descrita, el demandante acudió el pasado día [FECHA] a la consulta del doctor [NOMBRE Y APELLIDOS], quien le diagnóstico un agravamiento de la lesión, que requería de inmediata intervención quirúrgica, prescribiendo su ingreso en el mismo día en el Hospital [NOMBRE DEL HOSPITAL], lo cual se produjo a las [Nº] horas (acompañamos como documentos números [Nº DE DOCUMENTO] certificado librado por el Doctor [NOMBRE Y APELLIDOS] ordenando el ingreso hospitalario y parte de ingreso hospitalario expedido por el Hospital [NOMBRE DEL HOSPITAL]).

SEGUNDO.- Tras realizar las pertinentes pruebas, en el día de ayer [FECHA] fue intervenido quirúrgicamente mi representado por el equipo de cirugía del citado Hospital, con anestesia general, consistiendo la operación en [DESCRIPCIÓN DE LA INTERVENCIÓN], estando ingresado en planta, siendo de prever que la hospitalización se prolongue durante quince días (acompañamos como documento número [Nº DE DOCUMENTO], informe médico del cirujano Doctor [NOMBRE Y APELLIDOS]).

TERCERO.- Como consecuencia de esta agravación en las lesiones, determinadas por el propio proceso degenerativo de las mismas, mi representado tiene previsto estar setenta días de baja laboral, y sufrir una hospitalización de quince días, siendo de prever que la secuela resulte agravada (acompañamos como documento número [Nº DE DOCUMENTO], informe médico del Doctor [NOMBRE Y APELLIDOS] sobre el pronóstico de la intervención y consecuencias de la misma).

Por lo expuesto, AL TRIBUNAL SUPLICO que, con admisión de este escrito de ampliación de hechos y documentos acompañados con justificante de traslado, tenga por ampliados los hechos y, en su virtud, se tenga por concretada la indemnización solicitada en la cantidad de [IMPORTE] euros pretendida en la demanda, con más la que resulte de las lesiones a razón de [IMPORTE] euros por día de hospitalización, de [IMPORTE] euros por día de baja con impedimento, y de [IMPORTE] euros por las secuelas.

OTROSÍ DIGO que, para el caso que los hechos resulten controvertidos, propongo la práctica de los siguientes medios de prueba:

1. Documental, dando por reproducidos los documentos acompañados en este escrito.

2. Testifical, a fin de ser interrogados los siguientes testigos:

a) D. [NOMBRE Y APELLIDOS], de profesión médico, con domicilio en [LOCALIDAD]

b) D. [NOMBRE Y APELLIDOS], de profesión médico-cirujano, con domicilio en [LOCALIDAD]

Ambos testigos han atendido a mi representado en relación a estos hechos y por ello ostentan la condición de testigo-peritos.

Por lo que AL TRIBUNAL SUPLICO que, en su caso, admita la prueba propuesta por esta parte en relación a los hechos ampliados, acordando lo procedente para su práctica, solicitando que sean citados por el Tribunal los testigos propuestos, para ser interrogados en el acto del juicio ya señalado.

En L. y F.

(Firma Procurador y Abogado)

========================================================================
