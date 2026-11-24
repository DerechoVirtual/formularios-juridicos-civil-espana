---
name: escrito-demandado-denuncia-inexactitud-copia-dictamen-civ-1113
description: "Escrito del demandado que denuncia la inexactitud de la copia del dictamen pericial (art. 280 LEC). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito del demandado que denuncia la inexactitud de la copia del dictamen pericial (art. 280 LEC)

> Formulario **CIV-1113** del plugin **Proceso civil: demandas, contestaciones, prueba y vista** (`formularios-proceso-civil`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 24-11-2026.

## Qué es

Escrito al Tribunal de Instancia por el que el demandado, con arreglo a lo previsto en el art. 280 LEC, denuncia la inexactitud de la copia del dictamen pericial arquitectónico presentado como prueba de la parte actora, como causa de nulidad de lo actuado por haberse producido indefensión.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito del demandado que denuncia la inexactitud de la copia del dictamen pericial (art. 280 LEC)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito del demandado que denuncia la inexactitud de la copia del dictamen pericial (art. 280 LEC)” para mi caso». También puedes invocarla directamente con `/formularios-proceso-civil:escrito-demandado-denuncia-inexactitud-copia-dictamen-civ-1113`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-proceso-civil:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso civil: demandas, contestaciones, prueba y vista) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] AÑO
- [ ] FECHA
- [ ] LUGAR
- [ ] NOMBRE DE LA PARTE
- [ ] NÚMERO
- [ ] SEDE
- [ ] ÓRGANO

## Normas que cita el formulario

- art. 280 LEC
- art. 337.1 LEC
- art. 337.2 LEC
- art. 433 LEC
- art. 338.2 LEC

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

D./Dña. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, que actúa en nombre y representación del demandado D./Dña. [NOMBRE Y APELLIDOS], en los autos de Juicio Ordinario n.º [NÚMERO]/[AÑO], seguidos a instancias de [NOMBRE DE LA PARTE], en los mismos comparezco ante el Tribunal, y como mejor en Derecho proceda, DIGO:

Que por medio del presente escrito, y con arreglo a lo previsto en el art. 280 LEC, se denuncia la inexactitud del dictamen pericial arquitectónico presentado como prueba de la parte actora, como causa de nulidad de lo actuado, con base en las siguientes:

ALEGACIONES

PRIMERA.- La representación de la demandante [ÓRGANO], justificaba en su demanda la urgencia de ejercer su pretensión e imposibilidad de aportar el dictamen pericial del arquitecto superior D./Dña. [NOMBRE Y APELLIDOS], comprometiéndose a acompañarlo cinco días antes de la audiencia previa, al socaire del art. 337.1 LEC, como se aceptó en el auto de admisión.

SEGUNDA.- Paradógicamente, a esta parte demandada sí le fue viable, dentro del plazo de contestación, unir a ésta dictamen pericial de arquitecto superior sobre el objeto de debate, y hubo de esperar precisamente al último día del plazo para conocer el dictamen de adverso, cuya copia se entregó al Procurador suscrito en dicho momento, solicitándose posteriormente en la Audiencia Previa por ambas partes la práctica de la prueba pericial arquitectónica, se solicitó que el perito D./Dña. [NOMBRE Y APELLIDOS], autor del dictamen de la actora, acudiera al acto del juicio para responder a ciertas preguntas o efectuar algunas aclaraciones que explicaran lo que informaba, todo ello en cumplimiento de lo establecido en el art. 337.2 LEC.

TERCERA.- Pues bien, a fin de preparar el acto del juicio del art. 433 LEC, señalado para el día de la fecha, al repasar lo informado por el perito de la mercantil actora, D./Dña. [NOMBRE Y APELLIDOS], enfrentándolo a las aclaraciones derivadas del interés de esta representación, por el discurso incoherente con respecto del otro perito reclutado, D./Dña. [NOMBRE Y APELLIDOS], se ha venido a consultar el dictamen original cosido a los autos, para comprobar que éste contenía extremos ausentes en la copia facilitada al mandatario de esta parte, según se demuestra con la copia sellada con el justificante del traslado a través del servicio de notificaciones del Salón de Procuradores.

Obviamente, al no tener tiempo material para plantear el dictamen pericial contradictoria de los nuevos puntos que se entendían ausente de la prueba contraria, conforme al art. 338.2 LEC, y preparar las aclaraciones adecuadas al dictamen exacto, se causa manifiesta indefensión a nuestro mandante D./Dña. [NOMBRE Y APELLIDOS], al no tener ajustada su proposición de prueba al contenido real de la pericia debatida, y por tanto, procede anular lo actuado desde el acto de la audiencia previa, a fin de determinar el dictamen genuino, y conceder copia completa exacta a esta parte.

Por todo lo anteriormente expuesto,

SUPLICO AL TRIBUNAL

que, por presentado este escrito, junto con el recibo justificativo de haber dado traslado a la representación procesal de la parte, se digne admitirlo, y previa audiencia de la parte actora, declare la nulidad de todo lo actuado a partir de la citación para la audiencia previa, a fin de volver a citar a las partes a dicho acto, a fin de que se proporcione la copia exacta del dictamen pericial aportado, todo sin perjuicio de la responsabilidad en que haya incurrido quien presentó la copia inexacta.

Es justicia debe hacerse en [LUGAR], a [FECHA].

Firma del Abogado	Firma del Procurador/a

========================================================================
