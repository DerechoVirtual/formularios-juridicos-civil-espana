---
name: recurso-apelacion-valoracion-negativa-prueba-biologica-civ-2240
description: "Recurso de apelación por la valoración de la negativa a la prueba biológica de paternidad. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Recurso de apelación por la valoración de la negativa a la prueba biológica de paternidad

> Formulario **CIV-2240** del plugin **Hijos: custodia, visitas, alimentos, filiación y adopción** (`formularios-hijos-custodia-y-alimentos`) · Civil › Familia · normativa revisada el 25-11-2026.

## Qué es

Escrito de interposición de recurso de apelación contra sentencia dictada en proceso sobre impugnación de filiación paterna, al considerar el recurrente que la sentencia impugnada realiza una interpretación errónea de la doctrina del Tribunal Supremo sobre la negativa al sometimiento a la práctica de la prueba biológica.

Es un modelo de tipo **recursos**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Recurso de apelación por la valoración de la negativa a la prueba biológica de paternidad» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Recurso de apelación por la valoración de la negativa a la prueba biológica de paternidad” para mi caso». También puedes invocarla directamente con `/formularios-hijos-custodia-y-alimentos:recurso-apelacion-valoracion-negativa-prueba-biologica-civ-2240`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-hijos-custodia-y-alimentos:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Hijos: custodia, visitas, alimentos, filiación y adopción) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] COMPLETAR (8 veces)
- [ ] FECHA (3 veces)
- [ ] IMPORTE
- [ ] LUGAR
- [ ] Nº DE COLEGIADO/A

## Normas que cita el formulario

- art. 767.1 LEC
- art. 398 LEC

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

- Junto a «…A LA SECCION CIVIL DE LA AUDIENCIA PROVINCIAL DE [COMPLETAR]»: La AP no tiene «Sección Civil» como denominación legal: se cita la Sección por su número. Fuente: LOPJ arts. 80 y 82 (Audiencia Provincial, sin cambio de denominación).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) Ofreciendo una especial relevancia como indicio la negativa a la práctica de la prueba biológica, al menos cuando, esta negativa no ha sido acompañada de ninguna razón que la justifique, los demás indicios concurrentes no es exigible que generen una virtualidad probatoria plena por sí mismos, ni siquiera que sean aptos para jugar un papel preponderante en la construcción de la presunción, sino que basta que tengan una eficacia coadyuvante en términos de normalidad o razonabilidad desde el punto de vista del orden acostumbrado de las cosas, acreditado por la experiencia, para corroborar el indicio especialmente significado derivado de la negativa a la práctica de la prueba pericial biológica.

Así en el Fundamento Segundo de la Sentencia de la Audiencia Provincial de Castellón Sección 1.ª, de 20 Jun. 2008, rec. 247/2007, se señala:

«(...) De este modo, la vinculación del afectado a la práctica de la prueba biológica no constituye propiamente un deber, sino, como varias veces ha dicho la jurisprudencia del Tribunal Supremo (entre las más recientes, SSTS de 7 de diciembre de 2005, rec. 506/1997 y 2 de febrero de 2006, Rec. 1094/2001), una carga procesal, puesto que su incumplimiento no puede dar lugar a imponer su realización mediante medios coactivos, sino que únicamente determina que, en caso de ser injustificada la negativa, recaigan sobre la persona renuente las consecuencias de la falta de prueba, siempre que concurran los requisitos determinados por la doctrina constitucional y la jurisprudencia civil (la existencia de indicios suficientes para [COMPLETAR], conjuntamente con la consideración de dicha negativa como indicio muy cualificado, considerar determinada presuntivamente la paternidad reclamada)

En segundo lugar nos referiremos al valor de los indicios coadyuvantes.

Como dice la STS 27 de febrero de 2007, rec 2965/1996, la virtualidad que debe otorgarse a los indicios que puedan confluir con la negativa a la práctica de la prueba biológica, depende del grado de relevancia indiciaria que deba atribuirse a ésta.

En la doctrina del Tribunal Constitucional se registran diversas apelaciones a la jurisprudencia más moderna y ya reiterada de esta Sala en relación con los requisitos para la valoración de la negativa, las cuales demuestran que nuestra línea jurisprudencial ocupa un espacio situado dentro de los límites que conforman el marco constitucional cuando declara que la negativa a la prueba biológica no constituye un elemento probatorio equiparable a los demás en cuanto a su grado de eficacia presuntiva, sino que desempeña un papel especialmente relevante, como se deduce de la afirmación reiterada en nuestras sentencias, especialmente en las más recientes, en el sentido de que dicha negativa constituye un indicio "valioso" o "muy cualificado", sintagma este último que se invoca y reproduce literalmente en algunas de las sentencias del Tribunal Constitucional que se refieren a esta materia, perfilando así el marco constitucional dentro de cuyos límites ha de manifestarse con sentido propio nuestro poder de juzgar y nuestra función de fijar la orientación jurisprudencial que debe presidir la aplicación de la Ley por los Tribunales civiles.

Nuestra construcción jurisprudencial se funda en un conjunto de valoraciones formadas a lo largo de un proceso de consolidación, relacionadas con la ponderación de la finalidad de la norma y de los intereses que integran la realidad social -que la Ley nos ordena atender cuando nos apodera para fijar su interpretación- y centradas, primordialmente, en el punto de vista de la protección que para el menor supone la seguridad jurídica y objetiva en la determinación de la paternidad, en estrecha correspondencia con la naturaleza de la prueba biológica, la facilidad para su realización, su acreditada solvencia científica y su eficacia instrumental, y en armonía con la relevancia constitucional de los principios de protección integral de los hijos y de seguridad jurídica aplicada al estado civil de las personas.»


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
