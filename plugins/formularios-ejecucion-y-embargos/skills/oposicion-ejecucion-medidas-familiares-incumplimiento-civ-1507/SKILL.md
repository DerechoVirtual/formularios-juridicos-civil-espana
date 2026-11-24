---
name: oposicion-ejecucion-medidas-familiares-incumplimiento-civ-1507
description: "Oposición a la ejecución de medidas familiares por incumplimiento del régimen de visitas. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Oposición a la ejecución de medidas familiares por incumplimiento del régimen de visitas

> Formulario **CIV-1507** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Oposición a la ejecución de medidas familiares por incumplimiento del régimen de visitas» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Oposición a la ejecución de medidas familiares por incumplimiento del régimen de visitas” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:oposicion-ejecucion-medidas-familiares-incumplimiento-civ-1507`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (3 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] FECHAS
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] MES
- [ ] NOMBRE DE LA PARTE
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº
- [ ] Nº DE DOCUMENTO
- [ ] NÚMERO
- [ ] SEDE
- [ ] ÓRGANO
- [ ] ÓRGANO JUDICIAL

## Normas que cita el formulario

- art. 556 LEC

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

- Junto a «…Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Denominación legal: Sección de Familia, Infancia y Capacidad. Si no existe en el partido, conoce la Sección Civil o la Única (art. 86.3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «….3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

PROCEDIMIENTO DE DIVORCIO Nº [Nº DE PROCEDIMIENTO]

TRIBUNAL [ÓRGANO JUDICIAL]

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D. [NOMBRE Y APELLIDOS] Procurador de los Tribunales, en nombre y representación de [NOMBRE DEL REPRESENTADO/A], parte ejecutada en el procedimiento de ejecución arriba referenciado, según tengo acreditado en autos, ante el Tribunal comparezco y como mejor proceda en Derecho DIGO:

Que dentro del plazo concedido paso a formular OPOSICIÓN A LA EJECUCIÓN instada de contrario alegando que mi representado está cumpliendo puntualmente lo ordenado en la sentencia, ello en base a los siguientes:

HECHOS

Se acepta que mi mandante, progenitor no custodio, tiene reconocido en la sentencia el derecho a visitar a su hijo menor los fines de semana alternos y la mitad de las vacaciones, pero es totalmente falso que haya incumplido de manera reiterada las obligaciones derivadas del régimen de visitas, puesto que los únicos supuestos en que se ha producido el incumplimiento lo ha sido por la conducta obstativa de la madre, que ha puesto todo tipo de obstáculos para el normal desarrollo de la relación paterno filial.

Concretamente, el padre no ha podido comunicar con su hijo en los siguientes fines de semana en virtud de las siguientes circunstancias:

1) el día [FECHA] el padre compareció a recoger a su hijo en el domicilio materno, no contestando nadie, e intentando contactar telefónicamente con la madre en su móvil número [NÚMERO] sin obtener respuesta por cuanto que se encontraba apagado. Tampoco obtuvo explicación alguna por parte de la madre en los días posteriores. Como consecuencia de estos hechos, el padre formuló denuncia que se acompaña como documento número

2) el siguiente fin de semana del día [FECHA] se produjeron los mismos hechos, ante lo cual mi representado requirió la presencia del Notario D, el cual levantó acta que se acompaña como documento número [Nº DE DOCUMENTO], formulando seguidamente denuncia ante la Policía de [LOCALIDAD] que se acompaña como documento número

3) tras dos fines de semana cumpliendo normalmente el régimen de visitas, el fin de semana de los días [FECHAS] y [FECHA] la madre alegó que el hijo estaba enfermo y que no podía ir con su padre, impidiéndole el acceso al domicilio. En este caso, mi representado iba acompañado por dos amigos D. [NOMBRE Y APELLIDOS] y Dª., los cuales presenciaron estos hechos, tal como se acreditará mediante la proposición de la testifical oportuna.

Por tanto, mi mandante ha cumplido puntualmente sus obligaciones y sólo ha sido la madre quien ha impedido la relación, por lo que la ejecución que ahora se insta sólo pone de manifiesto la mala fe con que está actuando la demandante, reservándose esta parte el ejercicio de las acciones que le corresponden para depurar las responsabilidades derivadas de dicha conducta.

A los anteriores hechos le son aplicables los siguientes

FUNDAMENTOS DE DERECHO

Procedimiento

Artículo 776 LECiv, en relación con los artículos 556 y 560 de la LEC.

Legitimación

Artículo 556.1 LECiv, al ser parte ejecutada en el presente proceso de ejecución [Nº DE PROCEDIMIENTO].

Oposición a la ejecución

Por motivos de fondo, al amparo del art. 556 de la LEC, al haber cumplido mi representado lo dispuesto en la sentencia.

Costas

Han de imponerse al ejecutante de conformidad con los artículos 539.2 y 559.2.2 LECiv.

En su virtud,

SUPLICO AL TRIBUNAL: Tenga por presentado este escrito, documentos y copias, se sirva admitirlos y unirlos a autos, teniendo por formalizada, en tiempo y forma, oposición a la demanda ejecutiva instada por [NOMBRE DE LA PARTE] contra mi mandante, y previa sustanciación, estime la oposición deducida y proceda a dictar auto dejando sin efecto la ejecución despachada, condenando en costas a la ejecutante [ÓRGANO].

OTROSÍ DIGO que tratándose de una controversia fáctica respecto de la cual es necesaria la práctica de prueba, además de la documental aportada, se interesa que por el tribunal se acuerde la celebración de vista para sustanciar la oposición.

Por lo que SUPLICO AL TRIBUNAL que acuerde la celebración de vista.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma Abogado y Procurador

========================================================================
