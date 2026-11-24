---
name: recurso-apelacion-contra-auto-inadmite-peticion-civ-1148
description: "Recurso de apelación contra el auto que inadmite la petición inicial de proceso monitorio. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Recurso de apelación contra el auto que inadmite la petición inicial de proceso monitorio

> Formulario **CIV-1148** del plugin **Cobrar deudas: monitorio y cambiario** (`formularios-reclamar-deudas-monitorio`) · Civil › Monitorio y cambiario · normativa revisada el 24-11-2026.

## Qué es

Escrito interponiendo recurso de apelación contra auto de inadmisión a trámite de petición inicial de procedimiento monitorio.

Es un modelo de tipo **recursos**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Recurso de apelación contra el auto que inadmite la petición inicial de proceso monitorio» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Recurso de apelación contra el auto que inadmite la petición inicial de proceso monitorio” para mi caso». También puedes invocarla directamente con `/formularios-reclamar-deudas-monitorio:recurso-apelacion-contra-auto-inadmite-peticion-civ-1148`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-reclamar-deudas-monitorio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Cobrar deudas: monitorio y cambiario) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (5 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] LUGAR (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] Nº
- [ ] Nº DE DOCUMENTO
- [ ] NÚMERO
- [ ] ÓRGANO O PERSONA

## Normas que cita el formulario

- art. 458.1 LEC
- art. 459 LEC
- art. 812.1.2.ª LEC
- art. 812.1 LEC

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

- Junto a «…A LA SECCION CIVIL DE LA AUDIENCIA PROVINCIAL DE»: La AP no tiene «Sección Civil» como denominación legal: se cita la Sección por su número. Fuente: LOPJ arts. 80 y 82 (Audiencia Provincial, sin cambio de denominación).

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

A LA SECCION CIVIL DE LA AUDIENCIA PROVINCIAL DE

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, actuando en nombre de [NOMBRE DEL REPRESENTADO/A] S.L., cuya representación tengo acreditada en los Autos de Proceso Monitorio n.º [NÚMERO], ante la Sala comparezco y como mejor proceda en derecho DIGO:

Que en fecha [FECHA] se dictó Auto en este proceso cuya parte dispositiva es del tenor literal siguiente:

"QUE DEBO ACORDAR LA INADMISIÓN DEL PROCESO MONITORIO formulado por el Procurador/a D./Dña. [NOMBRE Y APELLIDOS], en representación de [NOMBRE DEL REPRESENTADO/A] S.L. contra D./Dña. [NOMBRE Y APELLIDOS] "

Que entendiendo que dicha resolución no es ajustada a derecho, dicho sea con los debidos respetos y en términos de defensa, dentro del plazo de veinte días legalmente establecido en el art. 458.1 LEC, por medio del presente escrito interpongo contra la misma RECURSO DE APELACIÓN, en el que expongo las siguientes:

ALEGACIONES

De conformidad a lo dispuesto en el art. 459 LEC, por infracción de lo dispuesto en el art. 812.1.2.ª LEC.

Dicho precepto dice que podrá acudir al proceso monitorio quien pretenda de otro el pago de deuda dineraria de cualquier importe, líquida, determinada, vencida y exigible, cuando la deuda se acredite de alguna de las formas siguientes: 2.ª Mediante facturas, albaranes de entrega, certificaciones, telegramas, telefax o cualesquiera otros documentos que, aun unilateralmente creados por el acreedor, sean de los que habitualmente documentan los créditos y deudas en relaciones de la clase que aparezca existente entre acreedor y deudor.

La resolución de fecha [FECHA] acuerda la inadmisión del proceso monitorio porque, como explicita en el fundamento jurídico [Nº] de dicha resolución, mi mandante presenta dos facturas, no firmadas por el deudor, y las considera insuficientes porque debió de haber aportado el acreedor, además de esos documentos unilaterales, cualquier otro que pudiera acreditar la relación comercial existente entre las partes.

Pues bien, a juicio de esta parte, a los efectos de admisión a trámite del procedimiento monitorio, el Juez únicamente ha de comprobar si con la petición monitoria se han presentado documentos que, integrados con las alegaciones del acreedor sobre el origen y cuantía de la deuda, constituyen un principio de prueba acreditativa de la existencia de la deuda que se reclama, sin que, en modo alguno, pueda reclamarse en este momento procesal una justificación plena de la existencia o certeza del crédito.

Basta con atender a la relación de documentos que se detalla en el apartado 2.º del art. 812.1 LEC, para ver que la presentación de dos facturas, que pueden ser definidas como una cuenta detallada con descripción e indicación de la naturaleza, medida, número y precio de los distintos objetos dados en venta, es más que suficiente para crear una buena apariencia jurídica de la deuda que se reclama, que es lo único que en este momento procesal se precisa para la admisión del monitorio, no la justificación plena de la existencia o certeza del crédito.

Por lo expuesto,

SUPLICO A LA AUDIENCIA PROVINCIAL:

Que habiendo por presentado este escrito se sirva tener por interpuesto RECURSO DE APELACIÓN frente a la resolución dictada en las presentes actuaciones de fecha [FECHA] y tras la pertinente tramitación, se dicte por ésta Auto en el que, estimando el recurso de apelación interpuesto por [ÓRGANO O PERSONA] S.L., se revoque la citada resolución y en su lugar ordene la admisión a trámite de la solicitud de procedimiento monitorio instada por la apelante contra D./Dña. [NOMBRE Y APELLIDOS] y que por el Tribunal de instancia se acuerde expedir requerimiento de pago, conforme a lo interesado.

Es justicia que pido en [LUGAR], a [FECHA].

OTROSÍ DIGO que, de conformidad con lo dispuesto en los apartados 3.b) y 6 de la disposición adicional decimoquinta de la LOPJ acompaño a este escrito como documento número [Nº DE DOCUMENTO] resguardo de consignación en la cuenta de Depósitos y Consignaciones abierta a nombre del Tribunal del depósito exigido para interponer el recurso por importe de 50 euros, por lo que,

SUPLICO AL TRIBUNAL que tenga por causada la manifestación anterior a los efectos oportunos.

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a
