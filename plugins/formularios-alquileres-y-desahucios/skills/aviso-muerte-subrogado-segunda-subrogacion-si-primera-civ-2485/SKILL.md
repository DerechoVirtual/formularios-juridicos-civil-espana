---
name: aviso-muerte-subrogado-segunda-subrogacion-si-primera-civ-2485
description: "Aviso de muerte del subrogado y segunda subrogación si la primera fue desde el 1 de enero de 1995. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Aviso de muerte del subrogado y segunda subrogación si la primera fue desde el 1 de enero de 1995

> Formulario **CIV-2485** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 25-11-2026.

## Qué es

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Aviso de muerte del subrogado y segunda subrogación si la primera fue desde el 1 de enero de 1995» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Aviso de muerte del subrogado y segunda subrogación si la primera fue desde el 1 de enero de 1995” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:aviso-muerte-subrogado-segunda-subrogacion-si-primera-civ-2485`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] COMPLETAR (5 veces)
- [ ] FECHA (2 veces)
- [ ] CALLE
- [ ] FINCA
- [ ] NÚMERO

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

Notas al pie del formulario original:
(1) La Disp. Trans. Segunda de la L. 29/1994, 24 nov., modifica sustancialmente el régimen de subrogaciones mortis causa en los contratos de arrendamientos de vivienda celebrados con anterioridad al 9 de mayo de 1985, y cuya disciplina se contenía en los arts. 58 y 59 del TRLAU 1964.

El art. 58 mencionado disponía:

«1. Al fallecimiento del inquilino titular del contrato de arrendamiento, SU CÓNYUGE, DESCENDIENTES, con preferencia los hijos varones menores de edad, las hijas solteras y los mayores impedidos físicamente, hijos adoptivos que hubieran sido adoptados antes de cumplir los 18 años, ASCENDIENTES y HERMANOS, con preferencia las hermanas solteras, tanto en el parentesco legítimo como en el natural, que con aquél hubiesen convivido habitualmente en la vivienda con dos años de antelación a la fecha del fallecimiento podrán subrogarse en los derechos y obligaciones del arrendamiento. No será necesaria la convivencia de los que estuviesen sometidos a la patria potestad del fallecido y, respecto al cónyuge, bastará la mera convivencia, sin exigencia en el plazo de antelación.

2. Cuando fueren varios los beneficiarios del derecho a que se refiere el número anterior, sólo uno de ellos podrá utilizarlo. A falta de acuerdo entre los mismos, se observará el orden de prelación establecido en el número anterior, con preferencia, dentro de cada grupo, de la proximidad de grado, de la legitimidad y, en su caso, del doble vínculo de la consanguinidad, resolviéndose los casos de igualdad a favor del que tuviere mayor número de cargas familiares, con prioridad del sexo femenino. Los padres septuagenarios serán preferibles a los descendientes.

3. En el caso de arrendamiento de local destinado por el arrendatario al ejercicio de su profesión facultativa y colegiada, al fallecimiento del titular del contrato podrán subrogarse en los derechos y obligaciones del arrendamiento, en primer lugar, su cónyuge, y en su defecto o renuncia, sus hijos, siempre que aquél o éstos ejerzan la misma profesión que el arrendatario fallecido y en el propio local.

4. La subrogación deberá notificarse fehacientemente al arrendador dentro de los noventa días siguientes a la fecha del fallecimiento del inquilino.

Si el arrendador no recibiese en tiempo tal notificación podrá requerir a los ocupantes de la vivienda para que se le comunique la subrogación del beneficiario, con advertencia de que, transcurridos treinta días sin recibir esta última notificación, tendrá lugar la resolución del contrato de arrendamiento, lo que así efectivamente sucederá si no se notificare la subrogación en este último plazo.»

A partir de la entrada en vigor de la L. 29/1994, 24 nov. de Arrendamientos Urbanos, la subrogación a que se alude en el art. 58 transcrito sólo puede tener lugar en favor del CÓNYUGE del arrendatario, no separado legalmente o de hecho, o, en su defecto, DE LOS HIJOS DEL ARRENDATARIO que conviviesen con él durante los dos años anteriores al fallecimiento y, en defecto de los anteriores, se podrán subrogar LOS ASCENDIENTES DEL ARRENDATARIO QUE ESTUVIESEN A SU CARGO y conviviesen con él con una antelación mínima de tres años a la fecha de su fallecimiento.

El contrato se extinguirá al fallecimiento del subrogado, salvo que lo sea un hijo del arrendatario no afectado por una discapacidad igual o superior al 65%, en cuyo caso se extinguirá a los dos años o en la fecha en que el subrogado cumpla veinticinco años, si ésta fuese posterior. Si el subrogado fuese el cónyuge y al tiempo del fallecimiento hubiesen hijos del arrendatario que conviviesen con aquél, podrá tener lugar una última subrogación, quedando extinguido el contrato a los dos años o cuando el hijo alcance la edad de 25 años si esta fecha es posterior, o por su fallecimiento si está afectado por la discapacidad antes mencionada.

La convivencia, que deberá ser habitual y darse necesariamente en la vivienda arrendada, es una circunstancia que, en cada caso, habrá de ser acreditada por quien pretende la subrogación.

En cuanto a procedimiento y orden de prelación regirá lo dispuesto en el art. 16 de la L. 29/1994, 24 nov.

Conviene decir que, incomprensiblemente, en la redacción del Proyecto de Ley de Arrendamientos Urbanos que fue publicado en el Boletín Oficial del Congreso de los Diputados de 21 de febrero de 1994 se había soslayado la doctrina emanada del Tribunal Constitucional que tiene su génesis en la S.T.C. 222/1992, 11 dic. Se declaró por el Alto Tribunal que el art. 58.1 del TRLAU 1964 era inconstitucional, por discriminatorio, en la medida en que excluía del beneficio de la subrogación mortis causa a quien hubiere convivido de modo marital (more uxorio) y estable con el arrendatario fallecido. En el fallo de la Sentencia calendada se declaró la inconstitucionalidad sobrevenida de tal exclusión pero no la nulidad de la regla legal que concedía al «cónyuge» el beneficio de la subrogación.

Atendiendo acaso a dicha doctrina y, cómo no, a la realidad social vigente, la Disp. Trans. Segunda que comentamos atribuye los mismos derechos que al cónyuge del arrendatario a la persona que hubiera venido conviviendo con el arrendatario de forma permanente en análoga relación de afectividad a la de cónyuge, con independencia de su orientación sexual durante al menos los dos años anteriores al tiempo del fallecimiento, salvo que hubiera descendencia en común, en cuyo caso bastará la mera convivencia.

Durante los 10 años siguientes a la entrada en vigor de la L. 29/1994, 24 nov., si la subrogación prevista en el apartado 4 de la Disp. Trans. Segunda ha tenido lugar en favor de hijos mayores de 65 años o que fueren perceptores de prestaciones públicas por jubilación o invalidez permanente en grado de incapacidad permanente absoluta o gran invalidez, el contrato se extingue al fallecimiento del hijo subrogado (Disp. Trans. Segunda, ap. 8 L. 29/1994, 24 nov.).

(2) Si la primera subrogación, realizada a partir de la entrada en vigor de la L. 29/1994, se produce a favor del cónyuge, establece el último párrafo del apartado 4 de la Disp. Trans. Segunda de la LAU 1994 que, si al tiempo de su fallecimiento hubiese hijos del arrendatario que conviviesen con aquél, podrá haber una ulterior subrogación. En tal caso, el contrato quedará extinguido a los dos años o cuando el hijo alcance la edad de veinticinco años si esta fecha es posterior, o por su fallecimiento si está afectado por una discapacidad igual o superior al 65 por 100. Si el que pretende la subrogación se halla afecto a tal tipo de discapacidad, deberá acompañar también el documento que lo acredite. A tales efectos, téngase en cuenta que la Disp. Adic. Novena de la LAU 1994 dispone que: «A los efectos prevenidos en esta Ley, la situación de minusvalía y su grado deberán ser declarados, de acuerdo con la normativa vigente, por los centros y servicios de las Administraciones Públicas competentes».


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
