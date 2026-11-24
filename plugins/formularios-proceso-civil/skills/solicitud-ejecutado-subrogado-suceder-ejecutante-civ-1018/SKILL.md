---
name: solicitud-ejecutado-subrogado-suceder-ejecutante-civ-1018
description: "Solicitud del ejecutado subrogado de suceder al ejecutante en el proceso contra el codeudor. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud del ejecutado subrogado de suceder al ejecutante en el proceso contra el codeudor

> Formulario **CIV-1018** del plugin **Proceso civil: demandas, contestaciones, prueba y vista** (`formularios-proceso-civil`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 24-11-2026.

## Qué es

Escrito de la parte ejecutada, subrogada por pago o cesión, solicitando la sucesión procesal del ejecutante en el proceso contra el codeudor por transmisión del objeto litigioso (cambio de parte endógeno).

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud del ejecutado subrogado de suceder al ejecutante en el proceso contra el codeudor» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud del ejecutado subrogado de suceder al ejecutante en el proceso contra el codeudor” para mi caso». También puedes invocarla directamente con `/formularios-proceso-civil:solicitud-ejecutado-subrogado-suceder-ejecutante-civ-1018`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-proceso-civil:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso civil: demandas, contestaciones, prueba y vista) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] ENTIDAD BANCARIA (5 veces)
- [ ] FECHA (4 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] LUGAR (2 veces)
- [ ] ACTO O RESOLUCIÓN
- [ ] AÑO
- [ ] LOCALIDAD
- [ ] NOMBRE DE LA PARTE
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº
- [ ] Nº DE COLEGIADO/A
- [ ] SEDE

## Normas que cita el formulario

- art. 540.1 LEC
- art. 17.1 LEC
- art. 1.209 CC
- art. 149 LH

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, actuando en nombre y representación procesal de [NOMBRE DE LA PARTE], cuyas circunstancias ya constan, en virtud del poder ‘apud acta’ que se ha otorgado ante la Letrado de la Administración de Justicia, asistido del Letrado ejerciente D./Dña. [NOMBRE Y APELLIDOS], con despacho abierto en [LOCALIDAD], colegiado nº [Nº DE COLEGIADO/A] en el Colegio de esta provincial, en el Proceso de Ejecución de Título Extrajudicial n.º [Nº]/[AÑO], que sigue el Tribunal a instancias del [ENTIDAD BANCARIA], en los mismos comparezco y como mejor proceda en Derecho, DIGO:

Que por el presente escrito, vengo a solicitar la sucesión procesal por transmisión del objeto litigioso, con base en las siguientes:

ALEGACIONES

PRIMERA

Se sigue en el Tribunal a que me honro en dirigirme proceso de ejecución de título extrajudicial (póliza de préstamo) a instancias del [ENTIDAD BANCARIA], en el que por Auto de fecha [FECHA] se despachó ejecución contra [ACTO O RESOLUCIÓN], deudora principal por débito de treinta y seis mil euros y otros diez mil ochocientos que se calcularon para intereses de mora procesal y costas del proceso ejecutivo, y contra los avalistas solidarios, y

SEGUNDA

Mi mandante [NOMBRE DEL REPRESENTADO/A] ha pagado al [ENTIDAD BANCARIA]. cuarenta y seis mil ochocientos euros, en concepto de principal, intereses y gastos de ejecución correspondiente al préstamo cuyo documento sirve de título ejecutivo en este proceso, y la entidad prestamista ha aceptado expresamente la subrogación en la condición que ostenta el [ENTIDAD BANCARIA]. tanto en el crédito, como a los efectos del presente proceso ejecutivo.

A su demostración, se acompaña documento de carta de pago de fecha [FECHA]

TERCERA

El art. 540.1 LEC prevé el supuesto de pretensión de despacho de ejecución a favor de quien acredite ser sucesor de quien figura como ejecutante en el título ejecutivo, estableciendo un trámite de adveración documental de la sucesión, por lo que para el supuesto, como el presente, de sucesión que acaece después del despacho, debe recurrirse a la prevención general de sucesión procesal del art. 17.1 LEC, y solicitarse que se tenga a mi representado en la posición que ocupaba el [ENTIDAD BANCARIA]. ejecutante, por adquisición del crédito.

CUARTA

La línea de separación conceptual entre la cesión de contrato, que carece de regulación expresa en el CCiv, y la subrogación, que se regula como una forma de pago y tiene su régimen en sede de novación (lo mismo la cesión con consentimiento del cedido y la subrogación convencional del art. 1.209 CCiv -con la que aquí no contamos- que la cesión sin consentimiento por disposición legal -ejemplos antedichos- y la subrogación legal, que nos ocupa, de los arts. 1.158 y 1.210 CCiv) pertenece a la mística de los civilistas, siendo la línea de la jurisprudencia lógicamente favorable a la identidad de tratamiento y efectos (SSTS de 11 de enero de 1.983 y 29 de mayo de 1.984),y también la línea del legislador (vid. art. 149 LH respecto a la cesión del crédito hipotecario).

Acreditada esta adquisición del crédito ejecutivo, tiene que asumirse que quien era co-ejecutado gana la posición de ejecutante frente a la mercantil deudora principal, y los avalistas solidarios, Y [NOMBRE Y APELLIDOS] y Z [NOMBRE Y APELLIDOS], respecto de estos últimos que debe reducirse la reclamación en cuotaparte de mi patrocinado, es decir, en una tercera parte.

Por todo lo expuesto,

AL TRIBUNAL SUPLICO

que, teniendo por presentado este escrito, con su documento anexo, y copias de todo ello, se sirva admitir uno y otras, y previa audiencia de las partes ejecutadas, con suspensión del proceso, por plazo de diez días, conforme a lo manifestado en el cuerpo de este escrito, se declare la sucesión de mi representadoen la posición de parte ejecutante, por haberle transmitido el. el crédito ejecutivo, y se me tenga por personado en dicha calidad, entendiéndose conmigo todas las sucesivas actuaciones, siguiendo la ejecución y los embargos trabados frente a los coejecutados, con reducción de la responsabilidad frente a los avalistas solidariosy, a la cantidad de veinticuatro mil euros, como principal, con la correlativa proporcional reducción de la presupuestada para intereses y costas, y lo demás que procede en Justicia de hacerse en [LUGAR], a [FECHA].

En [LUGAR], a [FECHA].

Firma del Abogado	Firma del Procurador/a

========================================================================
