---
name: solicitud-ex-parte-continuar-proceso-sin-demandado-civ-0878
description: "Solicitud ex parte de continuar el proceso sin el demandado (artículo 22.2 Reglamento 2020-1784). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud ex parte de continuar el proceso sin el demandado (artículo 22.2 Reglamento 2020-1784)

> Formulario **CIV-0878** del plugin **Proceso civil: demandas, contestaciones, prueba y vista** (`formularios-proceso-civil`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 24-11-2026.

## Qué es

ESCRITO DE SOLICITUD (EX PARTE) PARA CONTINUAR EL PROCEDIMIENTO JUDICIAL EN AUSENCIA DEL DEMANDADO AL CUMPLIRSE LAS CONDICIONES DEL ARTÍCULO 22.2 REGLAMENTO 2020/1784

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud ex parte de continuar el proceso sin el demandado (artículo 22.2 Reglamento 2020-1784)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud ex parte de continuar el proceso sin el demandado (artículo 22.2 Reglamento 2020-1784)” para mi caso». También puedes invocarla directamente con `/formularios-proceso-civil:solicitud-ex-parte-continuar-proceso-sin-demandado-civ-0878`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-proceso-civil:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso civil: demandas, contestaciones, prueba y vista) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] AÑO
- [ ] COLEGIO
- [ ] DÍA
- [ ] FECHA
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] MES
- [ ] Nº DE COLEGIADO
- [ ] Nº DE COLEGIADO/A
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

- Junto a «…ÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º LA CIUDAD DE [LOCALIDAD]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
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

Tribunal de Instancia n.º [NÚMERO]

Autos de Procedimiento [Nº DE PROCEDIMIENTO] n.º [NÚMERO]

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º LA CIUDAD DE [LOCALIDAD]

Comparece D. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en nombre y representación de D. [NOMBRE Y APELLIDOS], según tengo suficientemente acreditado en los presentes Autos de Juicio n.º [NÚMERO] en virtud de apoderamiento apud acta/escritura de poder notarial, y bajo la Dirección Letrada de D. [NOMBRE Y APELLIDOS], Abogado del Ilustre Colegio de Abogados de [COLEGIO], con número de colegiado [Nº DE COLEGIADO/A]; y como mejor proceda en Derecho,

DIGO

Primero.— Que en fecha [FECHA] se ha notificado el escrito de demanda, en aplicación del Reglamento (UE) 2020/1784 del Parlamento Europeo y del Consejo de 25 de noviembre de 2020 relativo a la notificación y traslado en los Estados miembros de documentos judiciales y extrajudiciales en materia civil o mercantil.

Segundo.— Que, asimismo, ha quedado acreditado que en los presentes Autos se cumplen los demás requisitos previstos en el art. 22.2 Reglamento 2020/1784, puesto que «b) ha transcurrido, desde la fecha de transmisión del documento, un plazo que el órgano jurisdiccional apreciará en cada caso concreto y que será, al menos, de seis meses, y c) no obstante las diligencias oportunas ante las autoridades competentes o entidades del Estado miembro requerido, no se ha podido obtener certificación alguna.».

Tercero.— Que en consecuencia, y a la vista del estado de las presentes actuaciones, interesa se acuerde continuar con el Procedimiento hasta que se dicte la correspondiente sentencia.

Nota: Dependiendo del país donde se realiza la notificación, ésta procede en aplicación del Convenio de La Haya sobre notificación o traslado al extranjero de documentos judiciales y extrajudiciales en materia civil o comercial de 15 de noviembre de 1965 o de Convenios bilaterales firmados por España. En este Convenio también existe un artículo paralelo (artículo 15) al del Reglamento europeo que permite continuar el procedimiento si se dan los requisitos allí previstos (prácticamente los mismos que los que aquí se relacionan).

Por todo lo expuesto y en su virtud,

SUPLICO AL TRIBUNAL: que teniendo por presentado este escrito, se sirva admitirlo a trámite, sea unido a autos, y conforme se interesa, acuerde continuar con el Procedimiento hasta que se dicte la correspondiente sentencia.

Es Justicia que pido en [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma y número del Letrado [Nº DE COLEGIADO]

Firma del Procurador

========================================================================
