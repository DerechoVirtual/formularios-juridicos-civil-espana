---
name: demanda-ejecucion-provisional-indicacion-bienes-sobre-civ-1625
description: "Demanda de ejecución provisional con indicación de los bienes sobre los que trabar embargo. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de ejecución provisional con indicación de los bienes sobre los que trabar embargo

> Formulario **CIV-1625** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Demanda dirigida al Tribunal de Instancia, solicitando la ejecución provisional de una sentencia de condena dictada en primera instancia apelada, indicando el demandante bienes sobre los que practicar la traba y solicitando medidas de localización e investigación por no ser suficientes los bienes señalados.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de ejecución provisional con indicación de los bienes sobre los que trabar embargo» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de ejecución provisional con indicación de los bienes sobre los que trabar embargo” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:demanda-ejecucion-provisional-indicacion-bienes-sobre-civ-1625`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (4 veces)
- [ ] IMPORTE (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] NOMBRE DE LA ENTIDAD (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] LUGAR
- [ ] MARCA/MODELO
- [ ] MATRÍCULA
- [ ] Nº
- [ ] OTROS DATOS
- [ ] PARTE DEMANDADA
- [ ] PROFESIÓN
- [ ] SEDE
- [ ] TIPO Y Nº DE PROCEDIMIENTO

## Normas que cita el formulario

- art. 526 LEC
- art. 538 LEC
- art. 539 LEC

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

D./Dña. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de profesión [PROFESIÓN], con domicilio en [LOCALIDAD], según tengo acreditado en autos [TIPO Y Nº DE PROCEDIMIENTO], comparezco ante el Tribunal y como mejor proceda en Derecho DIGO:

Que por medio del presente escrito se formula demanda instando la ejecución provisional de la sentencia de fecha [FECHA], dictada en los autos anteriormente reseñados.

HECHOS

PRIMERO.- El pasado día [FECHA] por el tribunal al que me dirijo se dictó sentencia por la que se condenaba al demandado al abono de la cantidad de [IMPORTE] euros, intereses legales y costas causadas.

SEGUNDO.- La sentencia antes mencionada fue apelada por la parte condenada al pago por considerarla lesiva a sus intereses.

TERCERO.- Con fecha [FECHA] se ha notificado a esta parte diligencia de ordenación teniendo por interpuesto recurso de apelación contra la sentencia dictada en estos autos. Por lo tanto, con el fin de que no se irroguen nuevos perjuicios a mi patrocinado a causa de la lógica dilación que lleva consigo la tramitación de la apelación, es por lo que se solicita la ejecución provisional de la sentencia.

CUARTO.- Esta parte conoce que el condenado-apelante es propietario de una vivienda sita en [LOCALIDAD] e inscrita en el Registro de la Propiedad de [LOCALIDAD], así como de un vehículo marca [MARCA/MODELO] y matrícula [MATRÍCULA] No obstante, al no ser los bienes detallados suficientes para hacer frente a las responsabilidades reclamadas, es procedente oficiar a [NOMBRE DE LA ENTIDAD], para que informen a este Tribunal de la posible existencia de otros bienes o derechos del ejecutado de los que tengan constancia, ya que a esta parte le consta que el demandado es titular de [Nº] y siempre que mi patrocinado se ha dirigido a [NOMBRE DE LA ENTIDAD], sólo ha obtenido respuestas negativas y poco colaboradoras.

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA.-

Según el art. 526 de la LEC, quien haya obtenido un pronunciamiento a su favor en sentencia de condena dictada en primera instancia podrá, sin simultánea prestación de caución, pedir y obtener la ejecución provisional, conforme a lo previsto en los artículos siguientes, ante el Tribunal competente para la primera instancia (art. 524.2).

II.- LEGITIMACIÓN.-

El art. 526 legitima para solicitar la ejecución provisional a "quien haya obtenido un pronunciamiento a su favor en sentencia de condena dictada en primera instancia".

Por otro lado, el art. 538 de la LEC regula quienes son partes y sujetos de la ejecución forzosa, estando en el presente supuesto legitimado activamente mi poderdante por ser el acreedor de las cantidades reclamadas y haber obtenido a su favor sentencia de condena frente al deudor condenado, quien por esta causa ostenta la legitimación pasiva.

III.- POSTULACIÓN.-

Al tratarse de la ejecución provisional de una sentencia dictada en un proceso en el que es preceptiva la intervención de abogado y Procurador/a., la presente demanda viene firmada por dichos profesionales, de conformidad con lo dispuesto en el artículo 539 de la LEC.

IV.- Al ser la sentencia de condena y no estando incluida en los supuestos enumerados en el artículo 525 de la Ley Procesal Civil, procede que se despache la ejecución provisional, ya que la solicitud se ha formulado con posterioridad a la notificación de la resolución de tener por interpuesto el recurso de apelación y antes de que se haya resuelto dicho recurso.

V.- Dado que esta parte conoce bienes del demandado sobre los que practicar la traba, se designan los mismos de acuerdo con el artículo 549-1,3º, interesándose a su vez que se oficie a los organismos y entidades expresados para que informen lo pertinente sobre otros bienes del deudor conforme al ordinal 4º del precepto citado, habiéndose expresado sucintamente en el hecho cuarto de esta demanda las razones por las que se estima que los organismos a oficiar disponen de información sobre el patrimonio del ejecutado.

En virtud de todo lo anterior,

SUPLICO AL TRIBUNAL:

que se tenga por presentada esta demanda, y, previa la apertura de la correspondiente pieza separada, se despache ejecución provisional de la sentencia contra [PARTE DEMANDADA] condenando a pagar al ejecutado la cantidad de [IMPORTE] euros de principal, intereses legales y costas causadas que se presupuestan en [IMPORTE] euros, procediéndose al embargo de los bienes del ejecutado designados y a oficiar a las entidades y organismos enumerados a fin de que informen de otros posibles bienes del deudor, ya que los reseñados se consideran insuficientes para cubrir las responsabilidades reclamadas.

OTROSI DIGO.-

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

Que habiéndose remitido ya los autos al tribunal competente para resolver la apelación, acompaño testimonio de particulares con todo lo necesario para la ejecución.

(O bien: [OTROS DATOS])

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a

========================================================================
