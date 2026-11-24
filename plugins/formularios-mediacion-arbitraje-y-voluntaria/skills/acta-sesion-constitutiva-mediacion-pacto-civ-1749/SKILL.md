---
name: acta-sesion-constitutiva-mediacion-pacto-civ-1749
description: "Acta de la sesión constitutiva de mediación con pacto de confidencialidad. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Acta de la sesión constitutiva de mediación con pacto de confidencialidad

> Formulario **CIV-1749** del plugin **Mediación, MASC, arbitraje y jurisdicción voluntaria** (`formularios-mediacion-arbitraje-y-voluntaria`) · Civil › Jurisdicción voluntaria, MASC, mediación y arbitraje · normativa revisada el 24-11-2026.

## Qué es

Acta de sesión constitutiva de mediación, que contiene los extremos que debe contener el acta, según el art. 19 de la Ley 5/2012; y pacto de confidencialidad, también ajustado a las prevenciones de la Ley en su art. 9.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Acta de la sesión constitutiva de mediación con pacto de confidencialidad» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Acta de la sesión constitutiva de mediación con pacto de confidencialidad” para mi caso». También puedes invocarla directamente con `/formularios-mediacion-arbitraje-y-voluntaria:acta-sesion-constitutiva-mediacion-pacto-civ-1749`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-mediacion-arbitraje-y-voluntaria:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Mediación, MASC, arbitraje y jurisdicción voluntaria) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] Nº (2 veces)
- [ ] AÑO
- [ ] FECHA
- [ ] Nº DE PROCEDIMIENTO
- [ ] OTROS DATOS
- [ ] SEDE

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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Junto a «…e la sección de lo mercantil del Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) En el escrito se menciona que los que van a ser mediados son partes de un procedimiento mercantil; pero también cabe la opción de que las partes acudan a la mediación voluntariamente, y no derivados por el Tribunal.

========================================================================


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

En Madrid, siendo las [Nº] horas del día [FECHA], se encuentran reunidos en la sede del Servicio de Mediación de la Cámara de Comercio de Madrid

— D./DÑA. [NOMBRE Y APELLIDOS]
— D./DÑA. [NOMBRE Y APELLIDOS]

Constituyen, como demandante y demandado, respectivamente, las partes del procedimiento ordinario n.º [Nº DE PROCEDIMIENTO]/[AÑO], que se tramita ante la sección de lo mercantil del Tribunal de Instancia de [SEDE], plaza n.º [Nº] [OTROS DATOS], en cuyo marco han sido invitados a acudir a la presente sesión constitutiva, con objeto de poner fin al conflicto que mantienen en relación a la acción declarativa de competencia desleal y la acción indemnizatoria, contenidas en la demanda que dio origen al proceso.

Declaran que han sido informados del programa de actuaciones adecuado al asunto, que será dirigido por el mediador, D./DÑA. [NOMBRE Y APELLIDOS], se celebrará en la sede de la Cámara de Comercio, utilizando el idioma castellano, durante un máximo de cinco sesiones de hora media, a razón de una por semana; sin perjuicio de que el acuerdo pueda alcanzarse sin necesidad de celebrar todas ellas, o pueda ser prorrogado a petición de ambas partes. Tienen conocimiento, asimismo, de que el coste de cada sesión es de [IMPORTE] euros, de los cuales [IMPORTE] euros corresponden a los honorarios del citado mediador, y [IMPORTE] euros consisten en los gastos generales relativos a la utilización de las instalaciones de la Cámara de Comercio

Manifiestan su aceptación voluntaria de la mediación proyectada y la asunción de las obligaciones legales, derivadas de ello, conforme a lo previsto en la Ley 5/2012 de 6 de julio, de mediación en asuntos civiles y mercantiles. En este sentido, conocen, principalmente, la obligación de cumplir con lo acordado y la posibilidad de ejecutar forzosamente el eventual acuerdo de mediación que se alcance. Y, asimismo, aceptan el siguiente:

Pacto de confidencialidad

1.- El procedimiento de mediación, y la documentación utilizada en la misma, es privado y confidencial, por lo que cualquier acuerdo entre las partes mediante el cual se dé por resuelta la desavenencia será confidencial, salvo que ambas partes autoricen de forma expresa y por escrito su divulgación, o se solicite mediante resolución judicial motivada por cualquier tribunal del orden jurisdiccional penal.

2.- En caso de no concurrir alguna de dichas excepciones, ninguna de las partes podrá presentar como elemento de prueba en un proceso judicial, arbitral o cualquier otro proceso similar:

a) cualquier documento, declaración o comunicación presentada por otra parte o por el Mediador en el procedimiento de Mediación, salvo que dicho documento, declaración o comunicación pueda obtenerse de forma independiente por la parte que esté interesada en presentarla en un proceso judicial, arbitral o cualquier otro proceso similar;
b) cualquier opinión o sugerencia expresada por cualquiera de las partes durante el procedimiento de Mediación relativa a una posible resolución de la desavenencia;
c) cualquier reconocimiento realizado durante el procedimiento de Mediación;
d) cualquier opinión expresada o propuesta hecha por el Mediador; o
e) el hecho de que una de las partes haya manifestado durante el procedimiento de Mediación, su disposición de aceptar una propuesta de transacción.

3.- Salvo acuerdo escrito en contrario de todas las partes, el Mediador no podrá actuar, en calidad de juez/a, árbitro/a, experto/a, representante o consejero/a de una de las partes en un proceso judicial, arbitral o similar, en relación con la misma desavenencia objeto del procedimiento de Mediación.

4.- El Mediador no podrá declarar en ningún otro proceso judicial, arbitral o similar en relación con cualquier aspecto del procedimiento de Mediación, salvo acuerdo escrito en contrario de todas las partes o que sea exigido por un órgano jurisdiccional penal.

Lo que firman el lugar y fecha indicados.

Firma	Firma
