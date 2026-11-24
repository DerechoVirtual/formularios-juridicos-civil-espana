---
name: escrito-pidiendo-acumular-ejecuciones-titulos-civ-1680
description: "Escrito pidiendo acumular ejecuciones de títulos extrajudiciales entre las mismas partes. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito pidiendo acumular ejecuciones de títulos extrajudiciales entre las mismas partes

> Formulario **CIV-1680** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Escrito solicitando la acumulación de los procesos de ejecución pendientes entre el mismo acreedor ejecutante y el mismo deudor ejecutado que se siguen en diferentes Tribunales.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito pidiendo acumular ejecuciones de títulos extrajudiciales entre las mismas partes» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito pidiendo acumular ejecuciones de títulos extrajudiciales entre las mismas partes” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:escrito-pidiendo-acumular-ejecuciones-titulos-civ-1680`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NÚMERO (6 veces)
- [ ] DENOMINACIÓN SOCIAL (5 veces)
- [ ] FECHA (4 veces)
- [ ] AÑO (3 veces)
- [ ] IMPORTE (3 veces)
- [ ] IMPORTE EN CIFRA (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] NOMBRE DE LA URBANIZACIÓN
- [ ] Nº
- [ ] Nº DE DOCUMENTO
- [ ] SEDE

## Normas que cita el formulario

- art. 3 Ley 57/1968
- art. 555.1 LEC
- art. 86 LEC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…ue despacha ejecución el [FECHA]. SEGUNDO.- Conforme al art. 3 de la Ley 57/1968»: La Ley 57/1968 quedó derogada el 1-1-2016 (Ley 20/2015, disposición final 3.ª); su régimen está hoy en la disposición adicional 1.ª de la Ley 38/1999, de Ordenación de la Edificación. La Ley 57/1968 sigue aplicándose a las garantías constituidas antes de esa fecha. Fuente: BOE-A-1999-21567, DA 1.ª.

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

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, que actúa en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], como tengo debidamente acreditado en autos de Ejecución de Título no judicial n.º [Nº]/[AÑO], que se sigue contra SEGUROS MUTUOS [DENOMINACIÓN SOCIAL] S.A., en los mismos comparezco y como mejor en Derecho proceda, DIGO:

PRIMERO.- El presente procedimiento se refiere a la ejecución contra SEGUROS MUTUOS [DENOMINACIÓN SOCIAL] S.A. por el importe de las cantidades entregada a PROMOCIONES [DENOMINACIÓN SOCIAL] S.A. para la compra de la vivienda endosada elemento n.º [NÚMERO] de la urbanización [NOMBRE DE LA URBANIZACIÓN] de [LOCALIDAD], con el interés legal devengado hasta su devolución, y que se garantizó por seguro de caución por la dicha aseguradora, habiéndose dictado, previo requerimiento infructuoso, auto que despacha ejecución el [FECHA].

SEGUNDO.- Conforme al art. 3 de la Ley 57/1968 , se aportó con la demanda ejecutiva el contrato de seguro unido al requerimiento notarial y acta de presencia, en que se acredita la no iniciación de la entrega de la vivienda el [FECHA], lo cual es título ejecutivo para exigir al asegurador la entrega de las cantidades a que se tiene derecho por la resolución del contrato de compraventa.

TERCERO.- Mi mandante también contrató la compra de la vivienda que hace elemento n.º [NÚMERO] de la misma urbanización, de la segunda fase edificatoria, e igualmente se le proporcionó contrato de seguro de caución de la compañía SEGUROS MUTUOS [DENOMINACIÓN SOCIAL] S.A., y como quiera que tampoco se ha entregado el inmueble en el plazo contractual previsto, que finaba el [FECHA], acompañando la póliza de los mismos documentos fehacientes acreditativos, se presentó nueva demanda ejecutiva, que se repartió AL TRIBUNAL DE INSTANCIA N.º [NÚMERO], que ha dado lugar a Ejecución de Título No Judicial n.º [NÚMERO]/[AÑO], habiéndose despachado por principal de [IMPORTE] euros.

Se acompañan copias testimoniadas de la demanda ejecutiva, contrato de seguro, requerimiento notarial y acta de presencia, y auto que despacha la ejecución, como documentos nos. a [Nº DE DOCUMENTO].

CUARTO.- El art. 555.1 LEC, autoriza a instancias de cualquiera de las partes, acordar la acumulación de los procesos de ejecución pendientes entre el mismo acreedor ejecutante y el mismo deudor ejecutado, lo que se sustanciará, en este caso, conforme a los arts. 86 a 97 LEC.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que, por presentado este escrito con los documentos anejos y copias de todo ello, se sirva admitirlo, tenga por solicitada la acumulación de ejecuciones, se comunique por el medio más rápido AL TRIBUNAL DE INSTANCIA N.º [NÚMERO], y seguido que sea el oportuno procedimiento, acuerde la acumulación que se solicita de la Ejecución de Título No Judicial n.º [NÚMERO]/[AÑO] de que conoce aquél a la Ejecución de estos autos, formulando requerimiento de acumulación, y aceptado éste, se siga un solo proceso ejecutivo para la satisfacción a mi mandante por SEGUROS MUTUOS [DENOMINACIÓN SOCIAL] S.A. de la suma acumulada de ambos procedimientos, es decir [IMPORTE] euros ([IMPORTE EN CIFRA] €) de principal, más [IMPORTE] euros ([IMPORTE EN CIFRA] €) que se presupuestan para intereses y costas.

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a

ATENCIÓN

La Ley 57/1968, de 27 de julio, sobre percibo de cantidades anticipadas en la construcción y venta de viviendas fue derogada a partir del 1 de enero de 2016 por la disposición derogatoria tercera de la Ley 38/1999, de Ordenación de la Edificación, introducida por Ley 20/2015, de 14 de julio, de ordenación, supervisión y solvencia de las entidades aseguradoras y reaseguradoras, que no establece ya el carácter ejecutivo del aval o de la póliza de seguro de caución en la compra de viviendas, que determinaba anteriormente el art. 3 de la Ley 57/1968, por lo que el formulario seguirá siendo válido solo para las cantidades entregadas con anterioridad al 1 de enero de 2016.

========================================================================
