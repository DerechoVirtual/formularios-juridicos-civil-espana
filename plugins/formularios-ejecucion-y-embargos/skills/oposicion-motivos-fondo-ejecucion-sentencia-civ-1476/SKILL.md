---
name: oposicion-motivos-fondo-ejecucion-sentencia-civ-1476
description: "Oposición por motivos de fondo a la ejecución de sentencia matrimonial por impago de pensiones. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Oposición por motivos de fondo a la ejecución de sentencia matrimonial por impago de pensiones

> Formulario **CIV-1476** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Escrito de oposición a la ejecución de sentencia matrimonial derivada de impago de pensiones, por motivos de fondo, solicitando que se deje sin efecto la ejecución y el alzamiento de los embargos y las medidas de garantía adoptadas

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Oposición por motivos de fondo a la ejecución de sentencia matrimonial por impago de pensiones» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Oposición por motivos de fondo a la ejecución de sentencia matrimonial por impago de pensiones” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:oposicion-motivos-fondo-ejecucion-sentencia-civ-1476`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (6 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] MES (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] IMPORTE (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE DEL HIJO (2 veces)
- [ ] Nº DE CUENTA (IBAN) (2 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] DNI/NIE
- [ ] LUGAR
- [ ] Nº DE DOCUMENTO

## Normas que cita el formulario

- art. 556 LEC
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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Junto a «…ELEGIR: SECCIÓN CIVIL / SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD] DE [LOCALIDAD]»: Denominación legal: Sección de Familia, Infancia y Capacidad. Si no existe en el partido, conoce la Sección Civil o la Única (art. 86.3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).

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

AL TRIBUNAL DE INSTANCIA [ELEGIR: SECCIÓN CIVIL / SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD] DE [LOCALIDAD]

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en nombre y representación de D. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD] y DNI número [DNI/NIE], según tengo acreditado en los autos de Juicio Especial de Divorcio seguidos ante este Tribunal con número de registro [Nº DE PROCEDIMIENTO] y de los que dimana el presente procedimiento de ejecución, comparezco y como mejor proceda en derecho DIGO:

Que en nombre de mi poderdante me persono en los autos de Ejecución de Título Judicial seguidos a instancia de Dña. [NOMBRE Y APELLIDOS] y registrados con el número [NÚMERO], y por medio del presente escrito formulo OPOSICIÓN a la citada ejecución, dentro del plazo concedido al efecto, en virtud de los siguientes:

HECHOS

PRIMERO.- Por auto de fecha [FECHA] se despachó ejecución contra mi cliente en reclamación de cantidad por impago de pensiones atrasadas correspondientes al mes de [MES] que se dicen adeudadas a sus hijos [NOMBRE DEL HIJO] y [NOMBRE DEL HIJO], auto que le fue notificado el pasado día [FECHA], por lo que el presente escrito se ha presentado dentro del término de diez días concedido al efecto para formular oposición.

SEGUNDO.- La sentencia dictada en el procedimiento de divorcio número [Nº DE PROCEDIMIENTO], de la que dimana la presente ejecución, acordó como medidas definitivas sendas pensiones alimenticias a cargo del ejecutado fijadas a favor de los dos hijos habidos en su matrimonio con la ejecutante, a ingresar por meses anticipados, dentro de los cinco primeros días de cada mes en la cuenta bancaria [Nº DE CUENTA (IBAN)], sentencia que mantuvo las mismas medidas adoptadas en la de fecha [FECHA] dictada en el anterior proceso de separación matrimonial número [NÚMERO], y por la que se fijaba como pensión alimenticia la de [IMPORTE] euros mensuales.

TERCERO.- El pasado día [FECHA] se efectuó un ingreso mediante transferencia en el número de cuenta [Nº DE CUENTA (IBAN)] de la que es titular la ejecutante por importe de [IMPORTE] euros, que cubre todas las cantidades reclamadas.

En efecto, no es esa la cuenta de abono designada en la resolución judicial para dar cumplimiento a la obligación alimentaria, pero la actora solicitó a mi representado que desde [FECHA], las cantidades adeudadas se transfirieran a la ejecutante a dicha cuenta de la que es titular, a lo que accedió mi representado, aunque no exista constancia escrita del acuerdo que modificaba la forma en que debían abonarse las pensiones.

De ahí que se transfiriera la cantidad reclamada a la citada cuenta bancaria, de la que es beneficiaria la ejecutante, en concepto de "atrasos pensión alimentos", lo que queda refrendado por el documento bancario que se aporta como documento n.º [NÚMERO], con lo que es claro que la transferencia se realizó para pagar las pensiones alimenticias adeudadas, en absoluta coincidencia con las cantidades que han sido objeto de reclamación.

Pero es que a mayor abundamiento tampoco el ingreso se realiza en una cuenta bancaria distinta de aquélla en la que se han venido abonando desde entonces las cantidades en concepto de "gastos extraordinarios", como se justifica con los resguardos en los que se consignan la recepción de las transferencias correspondientes a los meses de [MES] y [MES], que han sido aceptadas incondicionalmente por la ejecutante (documentos números [Nº DE DOCUMENTO]).

FUNDAMENTOS DE DERECHO

I.- Negamos que sean de aplicación al presente caso los fundamentos de derecho alegados por el ejecutante.

II.- Se alega pago de lo reclamado con base en el art. 556 de la LEC, que dispone que si el título ejecutivo fuera una resolución procesal o arbitral de condena o un acuerdo de mediación, el ejecutado, dentro de los diez días siguientes a la notificación del auto en que se despache ejecución, podrá oponerse a ella por escrito alegando el pago o cumplimiento de lo ordenado en la sentencia, laudo o acuerdo, que habrá de justificar documentalmente.

III.- En materia de costas procesales, a tenor de lo preceptuado en el art. 561.3 LEC, deberán ser impuestas al ejecutante.

En virtud de todo lo expuesto,

SUPLICO AL TRIBUNAL:

que tenga por presentado este escrito con sus copias y me tenga por comparecido y parte en la representación que ostento de D. [NOMBRE Y APELLIDOS]. en el expresado procedimiento de ejecución y mandar que se entiendan conmigo las actuaciones que a partir de este momento se realicen, teniendo por formulada en tiempo y forma oposición a la ejecución despachada, para que, tras la correspondiente tramitación se dicte auto declarando que no procede la ejecución dejando ésta sin efecto y mandando alzar los embargos y las medidas de garantía de la afección que se hubieran adoptado, reintegrándose al ejecutado a la situación anterior al despacho de la ejecución, con imposición de las costas al ejecutante.

Es de Justicia que pido en [LUGAR], a [FECHA].

OTROSÍ DIGO. Que interesa al derecho de esta parte la celebración de vista, por lo que se solicita del Tribunal que se señale un día para su celebración dentro de los diez días siguientes a la conclusión del trámite de impugnación a este escrito de oposición

Es justicia que reitero en lugar y fecha ut supra.

Firma del Abogado/a	Firma del Procurador/a

========================================================================
