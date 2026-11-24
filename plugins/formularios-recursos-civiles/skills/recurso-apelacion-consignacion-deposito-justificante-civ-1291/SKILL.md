---
name: recurso-apelacion-consignacion-deposito-justificante-civ-1291
description: "Recurso de apelación con consignación, depósito y justificante de la tasa judicial. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Recurso de apelación con consignación, depósito y justificante de la tasa judicial

> Formulario **CIV-1291** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **recursos**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Recurso de apelación con consignación, depósito y justificante de la tasa judicial» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Recurso de apelación con consignación, depósito y justificante de la tasa judicial” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:recurso-apelacion-consignacion-deposito-justificante-civ-1291`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (5 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] IMPORTE
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] MES
- [ ] MOTIVO
- [ ] Nº
- [ ] PRONUNCIAMIENTOS IMPUGNADOS

## Normas que cita el formulario

- art. 458 LEC
- art. 459 LEC
- art. 394 LEC
- art. 449.1 LEC

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

Proceso número [NÚMERO]

A LA AUDIENCIA PROVINCIAL DE [LOCALIDAD]

D. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en nombre y representación de D. [NOMBRE Y APELLIDOS], parte demandada en este proceso seguido con el número [NÚMERO], según tengo acreditado en autos, ante el Tribunal comparezco y como mejor proceda en derecho DIGO:

1) Que en fecha [FECHA] se dictó sentencia en este proceso, la cual fue notificada a esta parte en fecha [FECHA]

2) Que entendiendo que dicha sentencia no es ajustada a derecho, dicho sea con los debidos respetos y en términos de defensa, por medio del presente escrito interpongo contra la misma RECURSO DE APELACIÓN, (se harían constar los pronunciamientos que se impugnan [PRONUNCIAMIENTOS IMPUGNADOS]) impugnando todos sus pronunciamientos, tanto el condenatorio de mi representado al pago de la indemnización, como los relativos a intereses y costas.

3) Que, de conformidad a lo dispuesto en el art. 458 de la LEC, fundo el recurso de apelación en las siguientes

ALEGACIONES

Al amparo del art. 459 de la LEC, por infracción de lo dispuesto en el art.

Por infracción del artículo 394 de la LEC en relación al extremo relativo a la imposición de costas a esta parte.

De forma subsidiaria, y para el caso que no se estimaran los motivos anteriores, se alega la infracción del artículo 394 de la LEC, puesto que en la sentencia recurrida, pese a indicar que es estima la demanda, lo cierto es que solamente la estima en parte ya que de los pedimentos a), b) y c) que en la misma se contenían solamente se han visto estimados los dos primeros, no así el tercero, entendiendo que esta decisión desestimatoria del pedimento c) así como aquella en la que se establece que cada parte abone las costas generadas a su instancia y las comunes por mitad.

En cuanto al pedimento c) la sentencia lo desestima implícitamente en el fundamento [Nº] por [MOTIVO], si bien no lleva al fallo dicha desestimación.

Por tanto, y respecto de las costas, ante la estimación parcial de las pretensiones de la demanda, no pueden imponerse a mi representado ex art. 394 LEC, por lo que debe revocarse el pronunciamiento en este apartado.

En base a lo anterior,

SUPLICO A LA SALA: Que tenga por presentado este escrito con la certificación del traslado previo a las demás partes teniendo por interpuesto recurso de apelación frente a la sentencia dictada el pasado día [FECHA] en las presentes actuaciones de fecha [FECHA] y tras la pertinente tramitación y remisión de las actuaciones a la Ilma. Audiencia Provincial, se dicte por esta sentencia en la que, declarando haber lugar al recurso de apelación presentado, se revoque la citada sentencia y acordando

OTROSÍ PRIMERO DIGO que en cumplimiento de lo dispuesto en el art. 449.1 y 2 de la LEC esta parte ha consignado las cantidades correspondientes a las rentas vencidas correspondientes al periodo reclamado y a la tramitación del proceso, según al contrato de arrendamiento suscrito en fecha [FECHA], que hasta este momento ascienden a [IMPORTE] euros, manifestando su voluntad de abonar las que venzan sucesivamente durante la sustanciación del recurso.

Acompaño como documento número [Nº DE DOCUMENTO] resguardo acreditativo de la consignación en la cuenta de depósitos y consignaciones del Tribunal al que me dirijo.

Para el caso que el Tribunal no considerara suficiente el cumplimiento de los requisitos, esta parte manifiesta expresamente su voluntad de cumplir los requisitos legales, depositando las cantidades correspondientes con arreglo a derecho.

OTROSÍ SEGUNDO DIGO que, de conformidad con lo dispuesto en los apartados 3.b) y 6 de la disposición adicional decimoquinta de la LOPJ acompaño a este escrito como documento número [Nº DE DOCUMENTO] resguardo de consignación en la cuenta de Depósitos y Consignaciones abierta a nombre del Tribunal del depósito exigido para interponer el recurso por importe de 50 euros.

Por todo lo que, SUPLICO AL TRIBUNAL que tenga por hecha la anterior manifestación a los efectos pertinentes y por acompañado el documento justificativo del abono de la tasa.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma Abogado Firma Procurador

========================================================================
