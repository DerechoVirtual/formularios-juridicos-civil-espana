---
name: oposicion-conyuge-no-ejecutado-embargo-gananciales-civ-1684
description: "Oposición del cónyuge no ejecutado al embargo de gananciales por existir bienes privativos. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Oposición del cónyuge no ejecutado al embargo de gananciales por existir bienes privativos

> Formulario **CIV-1684** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Escrito del cónyuge no ejecutado oponiéndose al embargo de bienes gananciales por deuda que no es de su responsabilidad al existir bienes privativos del ejecutado y solicitando se resuelva alzar el embargo de su bien ganancial.

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Oposición del cónyuge no ejecutado al embargo de gananciales por existir bienes privativos» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Oposición del cónyuge no ejecutado al embargo de gananciales por existir bienes privativos” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:oposicion-conyuge-no-ejecutado-embargo-gananciales-civ-1684`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] NÚMERO (4 veces)
- [ ] FECHA (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] AÑO
- [ ] DENOMINACIÓN SOCIAL
- [ ] LUGAR
- [ ] NOMBRE DE LA EMBARCACIÓN
- [ ] SEDE

## Normas que cita el formulario

- art. 562.1.3.º LEC
- art. 1.373 CC
- art. 541 LEC
- art. 538.3 LEC
- art. 541.4 LEC

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

- Junto a «…MILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS] Procurador de los Tribunales, que actúa en nombre y representación de Doña [NOMBRE Y APELLIDOS], según tengo acreditado en los presentes autos de Ejecución de Título Judicial seguidos bajo número [NÚMERO]/[AÑO], ante el Tribunal y como mejor proceda en derecho DIGO:

Que por medio del presente escrito, y dentro del plazo de quince días concedido en auto de fecha [FECHA], al amparo del art. 562.1.3.º LEC vengo a OPONERME al embargo de bienes gananciales en la ejecución contra Don [NOMBRE Y APELLIDOS], con base en las siguientes

ALEGACIONES

PRIMERA.- Se han embargado sueldos de mi mandante como bienes gananciales para responder subsidiaria o indirectamente de la deuda ejecutiva de su esposo Don [NOMBRE Y APELLIDOS], de carácter privativo, contraída con la compañía de seguros ejecutante CLÍNICA [DENOMINACIÓN SOCIAL], S.L.

SEGUNDA.- Se ha notificado el embargo para que se ejercite la opción por mi mandante de pedir la disolución de la sociedad de gananciales, y sustituir el embargo trabado por el de la parte del ejecutado en aquélla, pero la sustitución sólo procede ante la falta o insuficiencia de bienes privativos del cónyuge deudor, como establece el art. 1.373 CCiv, siendo que Don [NOMBRE Y APELLIDOS] es titular de una embarcación de recreo, de nombre [NOMBRE DE LA EMBARCACIÓN], con matrícula n.º [NÚMERO], inscrita en la Sección de Buques del Registro Bienes Muebles de [LOCALIDAD], y que se halla atracado en el puerto de [LOCALIDAD], la cual tiene precio estimado suficiente para satisfacer las cantidades por las que se despachó ejecución, y podría ser embargada.

Se acompaña nota del Registro de Bienes Muebles como documento n.º [NÚMERO], junto con valoración emitida por perito tasador de compañía de seguros D./Dña. [NOMBRE Y APELLIDOS], como documento n.º [NÚMERO].

TERCERA.- Aunque el art. 541 LEC no contempla específicamente una fórmula de oposición al embargo de bienes gananciales por deudas privativas fuera de la disolución de la sociedad de gananciales, el embargo de bienes de un patrimonio comunitario separado especial, como la comunidad de gananciales, es un supuesto de extensión objetiva de la ejecución a terceros no legitimados pasivamente en el título ejecutivo del art. 538.3 LEC, por lo que el cónyuge no deudor tienen los mismos medios de defensa que la parte ejecutada, como remarca el art. 541.4 LEC, y por lo tanto, los medios de impugnación de actos ejecutivos, y entre tales el escrito para remediar la infracción cometida del art. 562.1.3.º LEC.

SUPLICO AL TRIBUNAL

que, por presentado el presente escrito, con los documentos que se acompañan, junto con el recibo justificativo de haber trasladado copia de todo ello a la representación procesal del ejecutante, se sirva admitirlo, y en mérito a lo manifestado, se resuelva alzar el embargo del bien ganancial de mi mandante Doña [NOMBRE Y APELLIDOS], y concediendo contradicción a las partes personadas, se sustituya por el del bien privativo del ejecutado Don [NOMBRE Y APELLIDOS],

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a

========================================================================
