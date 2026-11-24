---
name: escrito-conyuge-no-ejecutado-oponiendose-embargo-civ-1677
description: "Escrito del cónyuge no ejecutado oponiéndose al embargo de ganancial por ser privativa la deuda. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito del cónyuge no ejecutado oponiéndose al embargo de ganancial por ser privativa la deuda

> Formulario **CIV-1677** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Escrito de oposición especial del cónyuge no ejecutado ante el embargo de bien ganancial solicitando se declare, a los solos efectos incidentales, que la deuda por la que se procede es privativa y de la exclusiva responsabilidad del ejecutado.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito del cónyuge no ejecutado oponiéndose al embargo de ganancial por ser privativa la deuda» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito del cónyuge no ejecutado oponiéndose al embargo de ganancial por ser privativa la deuda” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:escrito-conyuge-no-ejecutado-oponiendose-embargo-civ-1677`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] FECHA (2 veces)
- [ ] Nº (2 veces)
- [ ] AÑO
- [ ] DENOMINACIÓN SOCIAL
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] NOMBRE DE LA PARTE
- [ ] Nº DE DOCUMENTO
- [ ] SEDE

## Normas que cita el formulario

- art. 541.2 LEC
- art. 539.1 LEC
- art. 1.373 CC
- art. 217.5 LEC
- art. 1.366 CC
- art. 561.3 LEC

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

### Avisos de actualización (3) — se aplican en el texto, nunca se copian en el documento

- Junto a «…Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).
- Junto a «…2666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.

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

D./Dña. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, que actúa en nombre y representación de Doña [NOMBRE Y APELLIDOS], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], en los autos de Ejecución de Título Judicial nº [Nº]/[AÑO], ante el Tribunal comparezco, y como mejor en Derecho proceda, DIGO:

Que con fecha [FECHA] ha sido notificado a mi mandante el embargo de bienes gananciales en el procedimiento de referencia, seguido contra Don [NOMBRE Y APELLIDOS] acordado mediante decreto, junto con la demanda ejecutiva de [NOMBRE DE LA PARTE], y el auto que despacha la ejecución, y dentro de plazo, vengo a oponerme a la ejecución concretada en los bienes comunes.

La presente oposición se basa en los siguientes:

HECHOS

PRIMERO.- Respecto a los aspectos formales y de contenido de la demanda ejecutiva, nada se tiene que oponer.

SEGUNDO.- Igualmente se admite como cierto el matrimonio de mi mandante con el ejecutado, y la vigencia del régimen de bienes legal supletorio de gananciales en el momento de contraer la deuda.

TERCERO.- El sueldo de mi mandante como funcionaria de la Diputación Provincial de [LOCALIDAD], es bien ganancial, y se manifiesta que los bienes gananciales no responden de la deuda por la que se sigue la ejecución.

A los anteriores hechos son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

I. PRESUPUESTO SUBJETIVOS.

Mi mandante es persona física en pleno ejercicio de sus derechos civiles, por lo que tiene capacidad ‘sub specie partium’ y capacidad procesal (arts. 6.1.1º y 7.1 LEC).

Está legitimada activamente para esta oposición especial, que es una pretensión incidental, como tercero interviniente litisconsorcial en el proceso de ejecución enderezada frente al cónyuge Don [NOMBRE Y APELLIDOS] por la llamada judicial derivada del embargo de bienes gananciales conforme art. 541.2 LEC.

Con arreglo al art. 539.1 LEC, es menester la representación por Procurador de los Tribunales y la dirección letrada.

II. IRRESPONSABILIDAD DE LA COMUNIDAD DE GANANCIALES.

En armonía con lo dispuesto en los arts. 1.373 CCiv y art. 541.2 LEC, y con que en el Derecho material la privatividad de una deuda contraída por persona casada en régimen de bienes comunitario opera como concepto por exclusión (es decir, que el débito no encaja en los supuestos de consorcialidad de arts. 1.365, 1.368, etc), cuando una deuda se ha contraído solo por uno de los casados en régimen legal de gananciales, el principio es que no responden los bienes gananciales de la misma (idéntica regla en los regímenes forales comunitarios: arts. 220 CDFA, 138 LDCPV, o ley 85 Fuero Nuevo de Navarra).

Como se admite el embargo indiscriminado de bienes gananciales para hacer frente a tales deudas individuales, que la sociedad de gananciales, siquiera externa o provisionalmente, quede vinculada para el pago de la deuda ejecutiva, por haberse adquirido en el marco de gestión individual legalizada del marido deudor Don [NOMBRE Y APELLIDOS], se configura por una suerte de presunción legal -arts. 217.5 y 385 LEC- en carga de probar por el ejecutante el hecho del que se desprende tal vinculación. Véanse las SSAP Madrid -Sección 13ª- de 13 de abril de 1998, rec. 999/1996, y -Sección 10ª- de 17 de febrero de 2000.

Si bien el art. 1.366 CCiv considera de responsabilidad y cargo de la sociedad de gananciales las obligaciones extracontractuales, no así las contraídas sin beneficio de la sociedad conyugal, y con culpa grave del cónyuge deudor, debiendo probar el ejecutante que la solidarización de deudas de la sociedad mercantil COMERCIAL [DENOMINACIÓN SOCIAL] S.L. con el ejecutado Don [NOMBRE Y APELLIDOS] procede de actuación con tal beneficio o sin culpa.

De los documentos aportados aparece claramente que ni uno ni otro supuesto, que permite fundar la responsabilidad de los bienes comunes, concurren en este caso.

Por ello, procede alzar el embargo trabado sobre bienes gananciales y dar a mi mandante la oportunidad de ejercitar la opción que le reconoce el artículo 1.373 CCiv, en relación con el 541 LEC.

III. COSTAS.

Las costas procesales de este incidente específico por irresponsabilización de bienes gananciales deben ser impuestas al ejecutante promotor de la llamada a juicio de mi poderdante, con arreglo al art. 561.3 LEC, y en todo caso, por la regla de art. 539.2.pfo.1º en relación con 394.1 LEC.

En virtud de lo expuesto

SUPLICO AL TRIBUNAL

que, por presentado este escrito, junto con el justificante de haber entregado copia de este escrito a los Procuradores de ejecutante y ejecutado, se sirva admitirlo, se me tenga por personado, entendiéndose conmigo las ulteriores sucesivas diligencias, y seguido que sea el trámite pertinente, se declare, a los solos efectos incidentales, que la deuda por la que se procede es privativa y de la exclusiva responsabilidad del ejecutado, con lo demás que sea procedente en Derecho, imponiendo las costas de esta oposición a la parte ejecutante.

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a

========================================================================
