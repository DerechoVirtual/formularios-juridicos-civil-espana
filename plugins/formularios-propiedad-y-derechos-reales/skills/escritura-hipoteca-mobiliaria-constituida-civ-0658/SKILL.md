---
name: escritura-hipoteca-mobiliaria-constituida-civ-0658
description: "Escritura de hipoteca mobiliaria constituida unilateralmente por el propietario. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura de hipoteca mobiliaria constituida unilateralmente por el propietario

> Formulario **CIV-0658** del plugin **Propiedad, posesión, servidumbres e hipotecas** (`formularios-propiedad-y-derechos-reales`) · Civil › Propiedad y derechos reales · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura de hipoteca mobiliaria constituida unilateralmente por el propietario» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura de hipoteca mobiliaria constituida unilateralmente por el propietario” para mi caso». También puedes invocarla directamente con `/formularios-propiedad-y-derechos-reales:escritura-hipoteca-mobiliaria-constituida-civ-0658`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-propiedad-y-derechos-reales:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Propiedad, posesión, servidumbres e hipotecas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (22 veces)
- [ ] LOCALIDAD (9 veces)
- [ ] FECHA (6 veces)
- [ ] DESCRIPCIÓN DEL BIEN (5 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] NOMBRE O DENOMINACIÓN (4 veces)
- [ ] NÚMERO (2 veces)
- [ ] CALLE
- [ ] DENOMINACIÓN SOCIAL
- [ ] DOMICILIO
- [ ] ESTADO CIVIL
- [ ] LUGAR
- [ ] NACIONALIDAD
- [ ] NIF
- [ ] TIPO DE IMPUESTO
- [ ] TOMO
- [ ] TÍTULO
- [ ] ÓRGANO O PERSONA

## Normas que cita el formulario

- No cita artículos concretos; Claude localizará las normas aplicables con Jurisprudenciator si el documento las necesita.

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

En [LUGAR], a [FECHA].

Ante mí, D./Dña. [NOMBRE Y APELLIDOS], perteneciente al colegio notarial de [LOCALIDAD], y con residencia en [LOCALIDAD]

COMPARECE

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, estado civil [ESTADO CIVIL], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], calle [CALLE],en nombre y representación de la sociedad mercantil denominada «[DENOMINACIÓN SOCIAL]», domiciliada en [DOMICILIO], y con NIF número [NIF], constituida, por tiempo indefinido, mediante escritura otorgada ante el notario de [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS], el [FECHA], e inscrita en el Registro Mercantil de [LOCALIDAD], al tomo [TOMO], en su calidad de administrador solidario de la reseñada sociedad, cargo para el que fue nombrado y asegura vigente en escritura otorgada el [FECHA], ante el notario de [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS], con el número [NÚMERO] de su protocolo, e inscrita en el Registro Mercantil de la [LOCALIDAD], en el tomo y hoja arriba indicados, con poderes suficientes para obligarle en este acto, según resulta de la verificación de la representación.

En adelante, EL DEUDOR HIPOTECANTE.

Le identifico por su documento de identidad, anteriormente reseñado y que me ha exhibido.

Le juzgo con capacidad legal suficiente para el otorgamiento de la presente escritura de hipoteca unilateral a favor del estado, y:

EXPONE

I. Que el Deudor hipotecante, es titular de los siguientes bienes:

Título. Le pertenecen por compra en virtud de escritura pública otorgada por el notario de [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS], con fecha [FECHA], con el número [NÚMERO] de su protocolo.

Se hallan libres de cargas y gravámenes, según resulta de las manifestaciones del Deudor hipotecante, y con relación a los bienes inmuebles de la nota simple informativa que me ha sido remitida en el día de hoy por el Registro de la Propiedad de [LOCALIDAD] Advierto al compareciente que sobre la prevalencia de la situación registral existente con anterioridad a la presentación en el Registro de copia autorizada de la presente escritura.

Declara el Deudor hipotecante que los bienes objeto de la presente escritura se encuentran libres de arrendamiento, así como que los bienes inmuebles vendidos no constituyen vivienda habitual de su familia ni de pareja de hecho.

II. Que por resolución de fecha [FECHA], adoptada por [ÓRGANO O PERSONA] y notificada en fecha [FECHA], se ha concedido un aplazamiento de la cantidad de [IMPORTE] euros ( euros), correspondiente al pago del Impuesto [TIPO DE IMPUESTO], fijándose como plazos de vencimiento del pago de la cantidad y de los intereses de demora correspondientes los siguientes:

a) Primer plazo:
b) Segundo plazo:
c) Tercer plazo:

«[NOMBRE O DENOMINACIÓN]».

III. Que el indicado aplazamiento quedaba supeditado a la constitución por parte del Deudor hipotecante de una hipoteca mobiliaria unilateral a favor del Estado.

IV. Que en cumplimiento de la disposición descrita en el expositivo II, y con el objeto de garantizar el cumplimiento del aplazamiento de pago solicitado, el Deudor hipotecante, en la calidad en la que actúa:

OTORGA

Primero

A favor del Estado, hipoteca mobiliaria unilateral sobre los bienes descritos en el expositivo I de la presente escritura.

Segundo

La presente hipoteca se constituye a favor del Estado, con el objeto de garantizar el pago del principal aplazado igual a [IMPORTE] euros ( euros), así como la cantidad correspondiente a la liquidación de los intereses de demora, que asciende a [IMPORTE] euros ( euros), y al 25 por 100 de la suma de ambos conceptos, equivalente a [IMPORTE] euros ( euros), conforme a lo previsto en el Real Decreto 939/2005, de 29 de julio, por el que se aprueba el Reglamento General de Recaudación.

El Deudor hipotecante hace distribución de la responsabilidad hipotecante entre los bienes hipotecados de la siguiente forma:

1. El [DESCRIPCIÓN DEL BIEN], responderá de [IMPORTE] euros ( euros), respecto del principal, de [IMPORTE] euros ( euros), respecto de los intereses de demora, y de [IMPORTE] euros ( euros), respecto de la cantidad complementaria.
2. El [DESCRIPCIÓN DEL BIEN], responderá de [IMPORTE], euros ( euros), respecto del principal, de [IMPORTE] euros ( euros), respecto de los intereses de demora, y de [IMPORTE] euros ( euros), respecto de la cantidad complementaria.
3. El [DESCRIPCIÓN DEL BIEN], responderá de [IMPORTE] euros ( euros), respecto del principal, de [IMPORTE] euros ( euros), respecto de los intereses de demora, y de [IMPORTE] euros ( euros), respecto de la cantidad complementaria.
4. El [DESCRIPCIÓN DEL BIEN], responderá de [IMPORTE] euros ( euros), respecto del principal, de [IMPORTE] euros ( euros), respecto de los intereses de demora, y de [IMPORTE] euros ( euros), respecto de la cantidad complementaria.
5. El [DESCRIPCIÓN DEL BIEN], responderá de [IMPORTE] euros ( euros), respecto del principal, de [IMPORTE] euros ( euros), respecto de los intereses de demora, y de [IMPORTE] euros ( euros), respecto de la cantidad complementaria.

Tercero

La hipoteca constituida se extenderá a toda clase de indemnizaciones que correspondan al deudor hipotecante, concedidas o debidas por razón de los bienes hipotecados, si el siniestro o hecho que los motiva acaeciera con posterioridad a la fecha de la presente escritura.

Cuarto

En caso de incumplimiento total o parcial de cualquiera de los plazos establecidos, acreditado mediante la correspondiente certificación al descubierto del débito cuyo ingreso se haya omitido, podrá procederse a la ejecución de la hipoteca.

La ejecución de la hipoteca se llevará a cabo por los órganos de Recaudación y por el Procedimiento de apremio. A tales efectos se fija como valor de tasación de cada uno de los bienes hipotecados el siguiente:

1 [IMPORTE]
2 [IMPORTE]
3 [IMPORTE]
4. «[NOMBRE O DENOMINACIÓN]».

Quinto

El Deudor hipotecante señala como domicilio para la práctica de las notificaciones necesarias para la ejecución de la presente Hipoteca el siguiente «especificar domicilio».

Sexto

La aceptación por parte del Estado de la hipoteca constituida será hará constar en el Registro mediante nota marginal que se practicará en virtud de oficio de «[NOMBRE O DENOMINACIÓN]», retrotrayéndose los efectos a la fecha de la presente escritura. Si dicha aceptación no consta en el plazo de dos meses a contar desde el requerimiento que al efecto se obliga a realizar el Deudor hipotecante, podrá cancelarse unilateralmente por el mismo la presente hipoteca.

OTORGAMIENTO Y AUTORIZACIÓN

Hago las reservas y advertencias legales y fiscales que incumben a las partes en su aspecto material, formal y sancionador, y especialmente advierto del plazo de treinta días hábiles siguientes a la firma de esta escritura para presentar a liquidar el impuesto correspondiente, de la afección de los bienes al pago del mismo y responsabilidades, en su caso, derivadas del incumplimiento.

Asimismo advierto de las consecuencias de una posible inexactitud de sus declaraciones o de falsedades en el documento y del tratamiento fiscal que se derivarían de las diferencias de valor resultantes de una comprobación administrativa.

Leo esta escritura a los comparecientes, previa advertencia y renuncia a su derecho de hacerlo por sí mismos y enterados de su contenido, prestan su consentimiento y la firman.

Y yo, el Notario, DOY FE de que mi actuación ha sido pactada de común acuerdo por las partes adquirente y transmitente, y en cuanto fuera procedente, de todo lo demás contenido en este instrumento público, extendido en «número» folios de papel de uso exclusivo para documentos notariales, de la serie «[TÍTULO]», números «[NOMBRE O DENOMINACIÓN]».

========================================================================
