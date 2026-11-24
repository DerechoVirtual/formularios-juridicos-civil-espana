---
name: impugnacion-oposicion-ejecucion-forzosa-laudo-arbitral-civ-1500
description: "Impugnación de la oposición a la ejecución forzosa de un laudo arbitral. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Impugnación de la oposición a la ejecución forzosa de un laudo arbitral

> Formulario **CIV-1500** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Impugnación de la oposición a la ejecución forzosa de un laudo arbitral» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Impugnación de la oposición a la ejecución forzosa de un laudo arbitral” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:impugnacion-oposicion-ejecucion-forzosa-laudo-arbitral-civ-1500`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] AÑO
- [ ] DÍA
- [ ] EXPONER EL MOTIVO
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] MES
- [ ] NOMBRE DE LA CORTE ARBITRAL
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] NOMBRE Y APELLIDOS
- [ ] NOMBRE Y APELLIDOS DEL ABOGADO
- [ ] Nº DE PROCEDIMIENTO

## Normas que cita el formulario

- art. 559.2 LEC

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

Sección Civil del Tribunal de Instancia núm de [LOCALIDAD]

Proceso de ejecución

AL TRIBUNAL

D. [NOMBRE Y APELLIDOS] Procurador de los Tribunales y de [NOMBRE DEL REPRESENTADO/A], según tengo acreditado en los autos arriba expresados [Nº DE PROCEDIMIENTO], ante el Tribunal comparezco y DIGO:

Que, evacuando el traslado conferido, y de conformidad a lo dispuesto en el art. 559.2 de la LEC, IMPUGNO la oposición a la ejecución deducida de contrario, ello en base a los siguientes

HECHOS

PRIMERO.- Se niegan los hechos relatados en el escrito de oposición.

El laudo arbitral no adolece de nulidad radical en tanto que se trata de una materia que es susceptible de arbitraje conforme al artículo 2 de la Ley de Arbitraje, puesto que se refiere a una controversia de libre disposición de las partes.

El convenio arbitral tenía como objeto el ejercicio de los derechos y obligaciones surgidos de un contrato de arrendamiento, que puede ser actuado en la vía del arbitraje y ello en tanto que debemos tener en cuenta que en el artículo 2.1 de la Ley de Arbitraje se expone que: "Son susceptibles de arbitraje las controversias sobre materias de libre disposición conforme a derecho", y como declaró la STS de 21 de marzo de 1985, el carácter imperativo de las normas, como es el caso de los arrendamientos urbanos, no convierte a las controversias surgidas en torno a un derecho en no susceptibles de arbitraje y, en consecuencia, el límite de lo que puede ser objeto de arbitraje debe situarse en aquellas materias que contraríen el orden público, pudiendo citarse en tal sentido el Auto de la Audiencia Provincial de Barcelona 72/2005, de 16 de marzo, y la Sentencia de la Audiencia Provincial de Vizcaya 373/2005, de 17 de mayo.

En relación al arbitraje en materia de arrendamientos urbanos, es doctrina consolidada de las Audiencias (v. gr.SAP Madrid, Secc. 14.ª, 114/2009 de 3 de febrero, rec. 4/2008 y SAP Madrid, Sec. 11.ª, 255/2009 de 22 de junio, rec. 7/2007), que la Ley de Arrendamientos Urbanos no hace indisponible la materia que regula, tanto más cuando se trata de determinar el cumplimiento contractual y, muy significadamente, el de la principal obligación del arrendatario, sin que en la suscripción del convenio arbitral se advierta ninguna situación de privilegio o abuso para el propietario que sólo persigue la obtención de la contraprestación pactada por la cesión del uso y disfrute de la vivienda de la que es titular.

En base a lo anteriormente expuesto, se interesa que se desestime el motivo de oposición alegado de contrario, habiendo sometido las partes libremente la posible controversia derivada del incumplimiento del contrato suscrito por esta a un arbitraje conforme la ley 60/2003, y a la Corte [NOMBRE DE LA CORTE ARBITRAL] como organismo arbitral, aceptado expresamente el convenio arbitral, que dictó en legal forma el laudo que se ejecuta.

SEGUNDO.- [EXPONER EL MOTIVO]
A los anteriores hechos le son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

Procedimiento

Artículo 559 LECiv

Impugnación de la oposición

Artículo 559.2 LEC, que establece que el ejecutante podrá impugnar la oposición fundada en la inexistencia de defectos procesales, como es el caso.

Costas

Artículos 559.2 LEC, imponiéndose al ejecutado debido a su mala fe y temeridad.

Por lo expuesto,

SUPLICO AL TRIBUNAL: Tenga por presentado este escrito, con justificante de traslado a la parte contraria, se sirva admitirlo, teniendo por formulada, en tiempo y forma, impugnación a la oposición formulada de contrario, acordando desestimarla y mandar seguir la ejecución adelante, con imposición de costas al ejecutado.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma Abogado [NOMBRE Y APELLIDOS DEL ABOGADO] Firma Procurador

========================================================================
