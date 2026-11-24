---
name: demanda-modificacion-medidas-incumplimiento-reiterado-civ-0290
description: "Demanda de modificación de medidas por incumplimiento reiterado de visitas por el custodio. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de modificación de medidas por incumplimiento reiterado de visitas por el custodio

> Formulario **CIV-0290** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda de modificación de medidas definitivas (arts. 775 y 776 LEC) para pedir el cambio de la guarda y custodia cuando el progenitor custodio incumple de forma reiterada el régimen de visitas, comunicación y estancia fijado en la sentencia a favor del otro progenitor.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de modificación de medidas por incumplimiento reiterado de visitas por el custodio» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de modificación de medidas por incumplimiento reiterado de visitas por el custodio” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-modificacion-medidas-incumplimiento-reiterado-civ-0290`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (3 veces)
- [ ] AÑO (2 veces)
- [ ] CLASE DE PROCEDIMIENTO (2 veces)
- [ ] DÍA (2 veces)
- [ ] FIRMA (2 veces)
- [ ] MES (2 veces)
- [ ] NOMBRE DEL MENOR (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL PROGENITOR CUSTODIO (2 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] SEDE (2 veces)
- [ ] FECHA
- [ ] LOCALIDAD
- [ ] NOMBRE Y APELLIDOS DEL DEMANDADO
- [ ] NOMBRE Y APELLIDOS DEL DEMANDANTE
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº DE DOCUMENTO
- [ ] NÚMERO
- [ ] RESOLUCIÓN EN LA QUE SE ACORDARON

## Normas que cita el formulario

- art. 776.3.ª LEC

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

- Junto a «…Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.

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

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales y de [NOMBRE Y APELLIDOS DEL DEMANDANTE], cuya representación tengo acreditada en los autos [CLASE DE PROCEDIMIENTO], registrados con el número [Nº DE PROCEDIMIENTO], seguidos frente a [NOMBRE Y APELLIDOS DEL DEMANDADO], cuyos datos personales obran en las actuaciones, siguiendo instrucciones de mi mandante y como mejor proceda en derecho, DIGO:

Que mediante el presente escrito formulo DEMANDA DE MODIFICACIÓN DE MEDIDAS acordadas en [RESOLUCIÓN EN LA QUE SE ACORDARON], contra D./Dña. [NOMBRE Y APELLIDOS DEL PROGENITOR CUSTODIO], por incumplimiento del régimen de visitas, en base a lo siguiente:

PRIMERO.– D./Dña. [NOMBRE Y APELLIDOS DEL PROGENITOR CUSTODIO] y mi representado/a se hallan [ELEGIR: separados / divorciados] en virtud de sentencia firme de fecha [DÍA] de [MES] de [AÑO], dictada en los autos de [CLASE DE PROCEDIMIENTO] n.º [Nº DE PROCEDIMIENTO].

SEGUNDO.– En el fallo de la citada sentencia se adoptaron como medidas definitivas, entre otras, la atribución de la guarda y custodia al/a la progenitor/a demandado/a del hijo común menor de edad [NOMBRE DEL MENOR], y un régimen de visitas, comunicación y estancia para el otro progenitor, que retiene la cotitularidad de la patria potestad, en beneficio del menor.

TERCERO.– El/La demandado/a jamás ha consentido que el actor ejercite el derecho de visitas que se le reconoció en la sentencia de mérito. Son [NÚMERO] los requerimientos judiciales que se le han dirigido, e incluso tiene abiertas diligencias previas en la Sección de Instrucción del Tribunal de Instancia de [SEDE], por delito de desobediencia grave a la autoridad (DOCUMENTOS NÚMEROS [Nº] a [Nº]).

CUARTO.– La ejecución incumplida con reiteración debe recibir la sanción del art. 776.3.ª LEC, es decir, la modificación del régimen de guarda y custodia.

QUINTO.– Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [INDICAR EL MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS AL QUE LAS PARTES SE HAN SOMETIDO EN CUMPLIMIENTO DEL REQUISITO DE PROCEDIBILIDAD QUE EXIGE LA LO 1/2025], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento n.º [Nº DE DOCUMENTO] [ESPECIFICAR EL DOCUMENTO QUE ACREDITA QUE SE HA ACUDIDO A UN MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS].

En su virtud,

SUPLICO AL TRIBUNAL

que, habiendo por presentado este escrito junto con los documentos y copias que se acompañan, se sirva admitirlo y por formulada solicitud de modificación de medidas definitivas acordadas en la sentencia de [FECHA], y previos los trámites legales, se acuerde la modificación de las medidas que se establecieron en la sentencia de [ELEGIR: separación / divorcio], sustituyéndolas por la atribución de la guarda y custodia del hijo menor [NOMBRE DEL MENOR] al actor, reconociéndose para el/la progenitor/a hasta ahora custodio/a un régimen de visitas como el de la sentencia para el progenitor no custodio, con expresa condena en costas a la parte demandada.

Es justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a: [FIRMA] Firma del Procurador/a: [FIRMA]
