---
name: demanda-ordinaria-desahucio-tramitada-cauce-juicio-civ-2432
description: "Demanda ordinaria de desahucio tramitada por el cauce del juicio de retracto. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda ordinaria de desahucio tramitada por el cauce del juicio de retracto

> Formulario **CIV-2432** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 25-11-2026.

## Qué es

Demanda de juicio declarativo ordinario con la que el antiguo arrendatario de un local de negocio cuyo contrato (anterior al 9 de mayo de 1985) se extinguió conforme a la Disposición Transitoria Tercera de la LAU de 1994 ejercita su derecho preferente a continuar en el local cuando el arrendador, dentro del año siguiente a la extinción y sin notificárselo, lo ha arrendado a otra persona: pide subrogarse en el nuevo contrato y el desahucio del nuevo arrendatario por los trámites del retracto (apartado 11 de dicha disposición).

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda ordinaria de desahucio tramitada por el cauce del juicio de retracto» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda ordinaria de desahucio tramitada por el cauce del juicio de retracto” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:demanda-ordinaria-desahucio-tramitada-cauce-juicio-civ-2432`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (9 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] CALLE (4 veces)
- [ ] FECHA (4 veces)
- [ ] NOMBRE Y APELLIDOS / DENOMINACIÓN SOCIAL DEL NUEVO ARRENDATARIO (4 veces)
- [ ] NOMBRE Y APELLIDOS DEL ARRENDADOR/A (3 veces)
- [ ] IDENTIFICACIÓN DEL LOCAL (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] NOMBRE Y APELLIDOS / DENOMINACIÓN SOCIAL DEL DEMANDADO/A (2 veces)
- [ ] NOMBRE Y APELLIDOS / DENOMINACIÓN SOCIAL DEL DEMANDANTE (2 veces)
- [ ] Nº DE FAX (2 veces)
- [ ] TELÉFONO (2 veces)
- [ ] AÑO
- [ ] COLEGIO
- [ ] DURACIÓN
- [ ] DÍA
- [ ] FECHAS
- [ ] IMPORTE EN LETRA
- [ ] MES
- [ ] NOMBRE DEL ABOGADO/A
- [ ] NOMBRE DEL PROCURADOR/A
- [ ] NOMBRE Y APELLIDOS DEL ABOGADO/A
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL DEL DEMANDADO/A
- [ ] NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL DEL DEMANDANTE
- [ ] Nº DE COLEGIADO
- [ ] SEDE

## Normas que cita el formulario

- art. 36 LEC
- art. 45 LEC
- art. 52.1.7.º LEC
- art. 23 LEC
- art. 249.1.7.º LEC
- art. 253 LEC
- art. 251 LEC
- art. 5 Ley Orgánica 1/2025
- art. 394 LEC

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

- Junto a «…acredita con el DOC. [Nº] que se acompaña, mi poderdante procedió a abandonarlo.»: los plazos de extinción del apartado 4 de la DT 3.ª LAU (arrendatario persona jurídica), incluidos los incrementos previstos en ese apartado y en el apartado 7, se cuentan desde la entrada en vigor de la Ley el 1 de enero de 1995; comprobar la fecha efectiva de extinción del contrato y que no ha transcurrido el año al que se refiere el apartado 11. Con todos los incrementos (veinte años más cinco por traspaso y cinco por revisión de renta), los arrendamientos de persona jurídica se extinguieron, como máximo, el 1 de enero de 2025; en los de persona física (apartado 3), la extinción se produce por la jubilación o el fallecimiento del arrendatario o del cónyuge subrogado.
- Junto a «…querimiento efectuado y como documento n.º [Nº] la contestación del demandado/a.»: la acción está sujeta a un plazo de caducidad de sesenta días naturales (apartado 11 de la DT 3.ª LAU). La solicitud de negociación suspende la caducidad en los términos del art. 7 de la Ley Orgánica 1/2025; controlar el cómputo antes de presentar la demanda.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

- Ninguna.

### Flujo

1. **Paso 0**: comprueba Jurisprudenciator (arriba).
2. Lee entero `assets/formulario.md` (el formulario que vas a rellenar, en la carpeta de esta skill) y la parte de `../indice/marco.md` que afecte al caso. Limítate a la materia de este formulario: no añadas contenido ajeno a él.
3. Pide los datos de la lista en una sola tanda. Si un dato aparece varias veces, aclara a qué persona o acto corresponde cada vez. Lo que el usuario no sepa se queda como hueco visible con su etiqueta (p. ej. [FECHA]).
4. Resuelve cada [ELEGIR …] y cada [OPCIONAL …] según los hechos, y sustituye cualquier indicación entre paréntesis del formulario («(se describirá…)», «(indicar…)») por el contenido que corresponda. Redacta las partes que dependen del caso (hechos, motivos, descripción de bienes).
5. Aplica los avisos de actualización en el lugar que indican. Comprueba con `buscar_articulo` cada norma citada; si alguna ha cambiado, usa la redacción vigente. Si citas jurisprudencia, localízala con `buscar_sentencias` o `buscar_por_cita` y léela con `leer_sentencias`.
6. Antes de entregarlo, pasa `verificar_escrito` con las frases que citan normas o sentencias y corrige lo que señale.
7. **Documento final = el formulario tal cual, rellenado y limpio.**
   - Empieza exactamente por la primera línea de `assets/formulario.md` y sigue su estructura y su orden hasta la firma.
   - No pongas en el documento título, nombre del formulario o de la skill, código, encabezados, «Para qué sirve», leyendas, avisos, notas de uso, comentarios ni explicaciones. Tampoco marcas [ELEGIR…] u [OPCIONAL…]: ya están resueltas.
   - Formato Word (.docx, con la skill de Word disponible): **Times New Roman 11 pt** en todo el documento, **interlineado 1,15**, **texto justificado**, márgenes de 2,5 cm. Los rótulos del formulario (REUNIDOS, CLÁUSULAS, HECHOS, SUPLICO…) en su propia línea y en negrita, sin cambiar su texto.
8. En el chat (nunca dentro del documento): datos pendientes, partes redactadas por ti, normas y sentencias comprobadas con Jurisprudenciator (y, si algún dato sale de internet, cuál y su enlace) y, si es un escrito judicial o administrativo, el plazo y el órgano ante el que se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.
