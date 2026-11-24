---
name: contrato-promesa-compraventa-inmueble-clausula-penal-civ-0837
description: "Contrato de promesa de compraventa de inmueble con cláusula penal y pago aplazado. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de promesa de compraventa de inmueble con cláusula penal y pago aplazado

> Formulario **CIV-0837** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Contrato de promesa de compraventa de bien inmueble con cláusula penal y pago aplazado con obligación del promitente comprador de subrogarse o liquidar la hipoteca concertada por el vendedor, siendo el promitente vendedor una sociedad inmobiliaria. Destacar que el mismo se encuentra sujeto a condición suspensiva y resolutoria.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de promesa de compraventa de inmueble con cláusula penal y pago aplazado» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de promesa de compraventa de inmueble con cláusula penal y pago aplazado” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:contrato-promesa-compraventa-inmueble-clausula-penal-civ-0837`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- `formulario.md`: el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `marco.md`: la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (10 veces)
- [ ] LOCALIDAD (7 veces)
- [ ] IMPORTE (5 veces)
- [ ] NÚMERO (5 veces)
- [ ] FECHA (4 veces)
- [ ] DENOMINACIÓN SOCIAL (3 veces)
- [ ] ENTIDAD BANCARIA (2 veces)
- [ ] SUCURSAL (2 veces)
- [ ] AÑO
- [ ] CALLE
- [ ] CARGO
- [ ] CÓDIGO DE CUENTA DE COTIZACIÓN
- [ ] DATOS REGISTRALES
- [ ] DOMICILIO
- [ ] IDENTIFICACIÓN DE LA VIVIENDA
- [ ] INSTITUCIÓN ARBITRAL
- [ ] LUGAR
- [ ] MUNICIPIO
- [ ] NOMBRE DE LA CALLE
- [ ] NOMBRE DE LA PROMOCIÓN
- [ ] Nº
- [ ] Nº DE COLEGIADO/A
- [ ] Nº DE CUENTA (IBAN)
- [ ] Nº DE PARCELAS
- [ ] Nº DE TRIMESTRE
- [ ] OTROS DATOS
- [ ] PLAZO

## Normas que cita el formulario

- art. 1.504 Código Civil
- art. 5 Real Decreto 515/1989
- art. 1.522 Código Civil
- art. 106 Real Decreto Legislativo 2/2004

---

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

Notas al pie del formulario original:
(1) Jurisprudencia de interés.- En el ámbito de la diferenciación entre los supuestos de auténticos contratos de compraventa y contratos de promesa de compra.

— Audiencia Provincial de Alicante, Sección 9ª, Sentencia 328/2011 de 14 Jul. 2011, rec. 39/2011.

«(...) En relación con el concepto de la promesa de comprar y vender la STS de 24 de octubre de 2008, Rec. 2454/2002, nos dice que" La Sentencia de 5 de octubre de 2005, Rec. 563/1999, en línea con la doctrina consolidada de esta Sala, diferencia el precontrato de compraventa del definitivo, constituyendo el precontrato "una primera fase del iter contractus: la relación jurídica obligacional nace en aquél y posteriormente, de común acuerdo o por exigencia de una de las partes, se pone en vigor el contrato que había sido preparado. Así, se distinguen dos fases: la primera, el precontrato que es distinto del contrato y no produce los efectos de éste, como pudiera ser la transmisión de la propiedad, sino sólo el que las partes pueden exigirse el paso a la fase segunda, que es la celebración del contrato preparado y es éste el que producirá los efectos que le son propios. Distinción entre el precontrato consistente en la promesa de venta y el contrato de compraventa que han seguido con clara precisión las Sentencias de 11 de octubre de 2000, rec. 2750/1995, 20 de abril de 2001, rec. 968/1996 y 31 de diciembre de 2001, rec. 2652/1996.»

— Audiencia Provincial de Granada, Sección 3ª, Sentencia 213/2010 de 28 May. 2010, rec. 190/2010.

« (...) La jurisprudencia siempre ha distinguido entre la promesa bilateral de vender y comprar y el contrato de compraventa" (STS de 23 de marzo de 1995, rec. 632/1992); y que "es incuestionable que no siempre se presenta de la misma forma y manera el contrato de promesa de venta, pues unas veces las propias partes contratantes han dejado para el futuro la propia obligación de celebrar el contrato definitivo, sino también la total y completa determinación de los elementos y circunstancias del referido contrato; en otros supuestos, las mismas partes, demuestran su decidida voluntad —en todos los pormenores y detalles— de celebrar un auténtico contrato de compraventa, que de momento no pueden actuar por impedirlo la concurrencia de determinados obstáculos como falta de autorizaciones o liberación de gravámenes, o simplemente porque en dicho instante no les conviene la celebración en firme y desean esperar cierto plazo, poniendo de manifiesto su voluntad de presente, sino exacta y total para cuando cesen aquellos obstáculos o venza el término establecido, momento a partir del cual es incuestionable que si uno incumple lo prometido el otro estará facultado a exigir el cumplimiento no de la promesa en sí, sino también del contrato definitivo al que aquella voluntad se determinó y para cuya realidad actual no existe ya obstáculo.»

— Otras sentencias de interés. Audiencia Provincial de Barcelona, Sección 14ª, Sentencia 274/2014 de 17 Jul. 2014, Rec. 21/2013.

========================================================================


### Flujo

1. **Paso 0**: comprueba Jurisprudenciator (arriba).
2. Lee `formulario.md` entero y la parte de `marco.md` que afecte al caso. Limítate a la materia de este formulario: no añadas contenido ajeno a él.
3. Pide los datos de la lista en una sola tanda. Si un dato aparece varias veces, aclara a qué persona o acto corresponde cada vez. Lo que el usuario no sepa se queda como hueco visible con su etiqueta (p. ej. [FECHA]).
4. Resuelve cada [ELEGIR …] y cada [OPCIONAL …] según los hechos, y sustituye cualquier indicación entre paréntesis del formulario («(se describirá…)», «(indicar…)») por el contenido que corresponda. Redacta las partes que dependen del caso (hechos, motivos, descripción de bienes).
5. Aplica los avisos de actualización en el lugar que indican. Comprueba con `buscar_articulo` cada norma citada; si alguna ha cambiado, usa la redacción vigente. Si citas jurisprudencia, localízala con `buscar_sentencias` o `buscar_por_cita` y léela con `leer_sentencias`.
6. Antes de entregarlo, pasa `verificar_escrito` con las frases que citan normas o sentencias y corrige lo que señale.
7. **Documento final = el formulario tal cual, rellenado y limpio.**
   - Empieza exactamente por la primera línea de `formulario.md` y sigue su estructura y su orden hasta la firma.
   - No pongas en el documento título, nombre del formulario o de la skill, código, encabezados, «Para qué sirve», leyendas, avisos, notas de uso, comentarios ni explicaciones. Tampoco marcas [ELEGIR…] u [OPCIONAL…]: ya están resueltas.
   - Formato Word (.docx, con la skill de Word disponible): **Times New Roman 12 pt** en todo el documento, **interlineado 1,15**, **texto justificado**, márgenes de 2,5 cm. Los rótulos del formulario (REUNIDOS, CLÁUSULAS, HECHOS, SUPLICO…) en su propia línea y en negrita, sin cambiar su texto.
8. En el chat (nunca dentro del documento): datos pendientes, partes redactadas por ti, normas y sentencias comprobadas con Jurisprudenciator (y, si algún dato sale de internet, cuál y su enlace) y, si es un escrito judicial o administrativo, el plazo y el órgano ante el que se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.
