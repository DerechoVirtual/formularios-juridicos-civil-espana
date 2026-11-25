---
name: aviso-arrendador-muerte-inquilino-local-subrogacion-civ-2480
description: "Aviso al arrendador de la muerte del inquilino del local y de la subrogación del cónyuge o familiar. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Aviso al arrendador de la muerte del inquilino del local y de la subrogación del cónyuge o familiar

> Formulario **CIV-2480** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 25-11-2026.

## Qué es

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Aviso al arrendador de la muerte del inquilino del local y de la subrogación del cónyuge o familiar» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Aviso al arrendador de la muerte del inquilino del local y de la subrogación del cónyuge o familiar” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:aviso-arrendador-muerte-inquilino-local-subrogacion-civ-2480`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] COMPLETAR (2 veces)
- [ ] FECHA (2 veces)
- [ ] CALLE
- [ ] FINCA
- [ ] LOCALIDAD
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
(1) El art. 60 del TRLAU 1964, regula la subrogación mortis causa en los arrendamientos de locales de negocio. Es así que, fallecido el arrendatario del local, el heredero le sustituirá en todos sus derechos y obligaciones y, a falta de tal o de su deseo de sustituir al arrendatario fallecido, el socio del finado podrá continuar el arrendamiento aun en el supuesto de una sociedad civil. Tal subrogación sólo es aplicable a dos subrogaciones, de manera que, fallecido el primer sustituto del arrendatario, sólo podrá tener lugar otra subrogación más.

Cada subrogación que se efectúe de conformidad con el art. mencionado, da derecho al arrendador a aumentar la renta en los términos expresados en el art. 42 del TRLAU 1964; esto es, en la cuantía que se convenga con el subrogado y, a falta de acuerdo, en un 15% de la renta que se satisfaga.

Empero, la Disp. Trans. Tercera de la L. 29/1994, 24 nov., de Arrendamientos Urbanos, ha venido a modificar sustancialmente tal régimen para aquellos contratos de arrendamiento de local de negocio en favor de persona física que a la fecha de entrada en vigor de la L.A.U. se encontraran en situación de prórroga legal siempre que se hubieran celebrado antes del 9 de mayo de 1985. En tales casos, el arrendamiento se extinguirá por la jubilación o fallecimiento del arrendatario, salvo que se subrogue su cónyuge y continúe la misma actividad desarrollada en el local. En defecto de cónyuge supérstite que continúe la actividad, o en caso de haberse subrogado éste, a su jubilación o fallecimiento, si en ese momento no hubieran transcurrido veinte años a contar desde la aprobación de la Ley, podrá subrogarse en el contrato un descendiente del arrendatario que continúe la actividad desarrollada en el local. En este caso, el contrato durará por el número de años suficientes hasta completar veinte años a contar desde la entrada en vigor de la Ley.

Se excluye expresamente la primera subrogación cuando precedentemente, y de acuerdo con lo dispuesto en el art. 60 del TRLAU 1964 ya se hubieran producido dos transmisiones. Y se proscribe la segunda subrogación cuando ya se hubiera producido en el arrendamiento una transmisión, de acuerdo con lo previsto en el mencionado art. 60.

En cuanto a las situaciones de jubilación del arrendatario ya existentes a 1 de enero de 1995, fecha de entrada en vigor de la L.A.U., entendemos que las previsiones de la Disp. Trans. Tercera no les afectan, al carecer de efecto retroactivo. En el apartado de «Novedades Jurisprudenciales más destacadas» se insertan sentencias de diversas Audiencias Provinciales que han mantenido dicha interpretación, o la inversa, al entender que sí debe operar la retroactividad.

En interpretación del art. 60 del TRLAU 1964, se había dicho que el mero hecho de la condición de heredero no transmite, mortis causa, y sin más, el derecho arrendaticio si éste no va unido a la continuación del negocio (STS, Sala Primera, de lo Civil, de 26 Junio 1993 ). La ratio legis del precepto consiste en que la prerrogativa que se concede al heredero o al socio, en su caso, redunde en defensa y reconocimiento del patrimonio comercial (SS.T.S. 30 jun. 1958, 29 jun. 1962 y 6 mar. 1963). En el mismo sentido, STS, Sala Primera, de lo Civil, de 22 Junio 1992 .

Referente al plazo para notificar la subrogación, véase la STS, Sala Primera, de lo Civil, 26/2009, de 29 Enero 2009, rec. 4132/2001


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
