---
name: oposicion-acumulacion-procesos-ante-mismo-tribunal-civ-0904
description: "Oposición a la acumulación de procesos ante el mismo tribunal. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Oposición a la acumulación de procesos ante el mismo tribunal

> Formulario **CIV-0904** del plugin **Proceso civil: demandas, contestaciones, prueba y vista** (`formularios-proceso-civil`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 24-11-2026.

## Qué es

Escrito por el que una parte se opone a la acumulación de otro proceso ya pendiente ante el mismo tribunal, alegando que no son procesos acumulables por seguir trámites distintos (artículo 77 de la Ley de Enjuiciamiento Civil) y que la cuestión pudo ventilarse en el mismo proceso (artículo 78.2).

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Oposición a la acumulación de procesos ante el mismo tribunal» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Oposición a la acumulación de procesos ante el mismo tribunal” para mi caso». También puedes invocarla directamente con `/formularios-proceso-civil:oposicion-acumulacion-procesos-ante-mismo-tribunal-civ-0904`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-proceso-civil:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso civil: demandas, contestaciones, prueba y vista) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº DE PROCEDIMIENTO (4 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] FECHA
- [ ] LOCALIDAD
- [ ] MES
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR
- [ ] NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL DEL REPRESENTADO
- [ ] Nº
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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Junto a «…DIMIENTO] A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

Proceso número [Nº DE PROCEDIMIENTO]

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

Don/Doña [NOMBRE Y APELLIDOS DEL PROCURADOR], Procurador/a de los Tribunales y de [NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL DEL REPRESENTADO], según tengo acreditado en los autos de proceso civil [Nº DE PROCEDIMIENTO] arriba referenciados, ante el Tribunal comparezco y, como mejor proceda en Derecho, DIGO:

Que, evacuando el traslado conferido por [ELEGIR: diligencia de ordenación / providencia] de fecha [FECHA], mediante el presente escrito vengo a oponerme a la acumulación de procesos, en base a las siguientes

ALEGACIONES

PRIMERA.– Motivo de oposición referido a no ser procesos acumulables.

Nos oponemos a la acumulación de procesos por cuanto no se dan los requisitos establecidos en el artículo 77 de la Ley de Enjuiciamiento Civil.

El citado precepto establece que solo procederá la acumulación de procesos declarativos que deban sustanciarse por los mismos trámites, siendo que este proceso, [NATURALEZA DEL PROCESO EN CURSO: por ejemplo, de tutela de derechos fundamentales], sigue los trámites del [CAUCE: por ejemplo, proceso ordinario, de tramitación preferente y con intervención del Ministerio Fiscal, conforme al artículo 249.1.2.º de la Ley de Enjuiciamiento Civil]. Por su parte, el proceso que se pretende acumular, [NATURALEZA DEL PROCESO QUE SE PRETENDE ACUMULAR: por ejemplo, de reclamación de la paternidad], se tramita por la vía del [CAUCE: por ejemplo, artículo 753 de la Ley de Enjuiciamiento Civil], además de que carece de dicho carácter preferente, siguiendo sus reglas específicas en cuanto a legitimación, procedimiento y prueba, recogidas en [PRECEPTOS: por ejemplo, los artículos 764 a 768 de la Ley de Enjuiciamiento Civil].

En consecuencia, siendo procesos declarativos de distinta tramitación y existiendo trámites claramente incompatibles entre ambos procesos, interesamos que se deniegue la acumulación.

SEGUNDA.– Motivo de oposición referido a la posibilidad de haberse ventilado la cuestión en el mismo proceso.

Nos oponemos asimismo por cuanto se incumple lo dispuesto en el apartado 2 del artículo 78 de la Ley de Enjuiciamiento Civil, puesto que no se justifica que no pudiera promoverse el proceso que ahora se pretende acumular con la primera demanda, con su ampliación o con la reconvención.

En este sentido, el proceso que se pretende acumular se inició por demanda donde se recogían pretensiones y cuestiones que debieron y pudieron haberse introducido por [ELEGIR: la parte actora en su escrito de demanda o, en su caso, en un eventual escrito de ampliación / la parte demandada deduciendo la correspondiente pretensión reconvencional].

Por tanto, no justificándose ninguna causa impeditiva del ejercicio de la acción en el momento procesal oportuno, por aplicación del artículo 78.2 de la Ley de Enjuiciamiento Civil deberá denegarse la acumulación del proceso número [Nº DE PROCEDIMIENTO] al presente proceso.

Por lo expuesto,

SUPLICO AL TRIBUNAL: que tenga por presentado este escrito, al que acompaño justificante de traslado previo, y, en su virtud, se nos tenga por opuestos a la acumulación al presente proceso del proceso número [Nº DE PROCEDIMIENTO] seguido ante este Tribunal, acordando dictar auto denegando la acumulación de procesos.

Es justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firmas del Abogado y del Procurador
