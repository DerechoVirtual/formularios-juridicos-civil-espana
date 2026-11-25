---
name: comunicacion-inquilino-necesita-obras-no-estructurales-civ-2511
description: "Comunicación del inquilino de que necesita obras no estructurales en la finca por discapacidad. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Comunicación del inquilino de que necesita obras no estructurales en la finca por discapacidad

> Formulario **CIV-2511** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 25-11-2026.

## Qué es

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Comunicación del inquilino de que necesita obras no estructurales en la finca por discapacidad» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Comunicación del inquilino de que necesita obras no estructurales en la finca por discapacidad” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:comunicacion-inquilino-necesita-obras-no-estructurales-civ-2511`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] CALLE (2 veces)
- [ ] COMPLETAR (2 veces)
- [ ] FECHA (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] PISO (2 veces)
- [ ] LUGAR

## Normas que cita el formulario

- art. 3 Ley 15/1995
- art. 7 Ley 15/1995

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
(1) La L. 15/1995, 30 may., sobre límites del dominio sobre inmuebles para eliminar barreras arquitectónicas a las personas con discapacidad, posibilita, como expresa su art. 1, apartado 2, «Las obras de adecuación de fincas urbanas ocupadas por personas minusválidas que impliquen reformas en su interior, si están destinadas a usos distintos del de vivienda, o modificación de elementos comunes del edificio que sirvan de paso necesario entre la finca urbana y la vía pública, tales como escaleras, ascensores, pasillos, portales o cualquier elemento arquitectónico, o las necesarias para la instalación de dispositivos electrónicos que favorezcan su comunicación con el exterior».

Se excepciona del ámbito de aplicación de la Ley «... las obras de adecuación del interior de las viviendas instadas por los arrendatarios de las mismas que tengan la condición de minusválidos o que convivan con personas que ostenten dicha condición en los términos del art. 24 de la Ley 29/1994, de 24 de noviembre, de Arrendamientos Urbanos, que se regirán por ésta» (art. 2.3 Ley 15/1995, de 30 de mayo).

Son requisitos esenciales para que nazca tal derecho:

1.º Que no se trate de obras a realizar en el interior de la vivienda arrendada, ya que éstas tienen su cauce específico en el art. 24 de la L. 29/1994, 24 nov., precepto que es asimismo aplicable a contratos de arrendamientos de vivienda que se encontraran vigentes el día 1 de enero de 1995, ya hubieren sido concertados antes del 9 de mayo de 1985 (Disp. Trans. Segunda.2 L. 29/1994, 24 nov.) ya con posterioridad a dicha fecha (Disp. Trans. Primera.1 L. 29/1994, 24 nov.).
2.º Ostentar la condición de beneficiario, siéndolo quienes padeciendo una disminución permanente para andar, subir escaleras o salvar barreras arquitectónicas, con independencia de que se precise o no el uso de prótesis o de sillas de ruedas, sean titulares de fincas urbanas en calidad de propietarios, arrendatarios, subarrendatarios o usufructuarios, o sean usuarios de las mismas.

Se considera usuario al cónyuge, a la persona que conviva con el titular de forma permanente en análoga relación de afectividad con independencia de su orientación sexual, y a los familiares que con él convivan. También se consideran usuarios a los trabajadores personas con discapacidad vinculados por una relación laboral con el titular.

También se consideran beneficiarios a las personas mayores de setenta años, sin necesidad de que acrediten su discapacidad.

3.º Que sean necesarias obras de reforma en el interior de la finca o en los pasos de comunicación con la vía pública para salvar las barreras arquitectónicas, de modo que se permita su adecuado y fácil uso por personas con discapacidad. Ahora bien, las obras a realizar no pueden afectar a la estructura o fábrica del edificio ni menoscabar la resistencia de los materiales empleados en la construcción, y al tiempo, deben ser compatibles con las características arquitectónicas e históricas del edificio.

Para ejercitar tal derecho, el titular o usuario debe notificar por escrito al propietario, a la comunidad o a la mancomunidad de propietarios, la necesidad de realizar las obras acompañando los siguientes documentos:

a) Certificación del Registro Civil o de la autoridad administrativa competente relativa a los requisitos arriba enunciados.
b) Certificación de la condición de persona con discapacidad expedida por la Administración competente. Es de señalar que ya la Disp. Adic. Novena de la Ley 29/1994, 24 nov., establecía que «A los efectos prevenidos en esta ley, la situación de minusvalía y su grado deberán ser declarados, de acuerdo con la normativa vigente, por los centros y servicios de las Administraciones Públicas competentes».

Se exime de la necesidad del certificado de discapacidad a las personas mayores de setenta años.

c) Proyecto técnico detallado de las obras a realizar.

En el plazo máximo de sesenta días deberá comunicarse por escrito al solicitante la conformidad u oposición razonada a la ejecución de las obras, pudiendo proponerse las soluciones alternativas que se estimen pertinentes. El transcurso del plazo máximo sin comunicación expresa equivale a una aceptación tácita y podrán iniciarse las obras. La oposición realizada fuera de plazo carece de cualquier tipo de eficacia.

De existir discrepancia entre las partes, bien porque temporáneamente haya habido oposición a las obras, bien porque propuestas soluciones alternativas no hubieran sido aceptadas por el titular o usuario, éste podrá solicitar el amparo judicial por los trámites del juicio verbal (art. 6 Ley 15/1995), previo intento de un medio adecuado de solución de controversias, requisito de procedibilidad del art. 5 de la Ley Orgánica 1/2025.

Los gastos que originen las obras de adecuación, que quedarán en beneficio de la propiedad, correrán a cargo del solicitante sin perjuicio de las ayudas, exenciones o subvenciones que pudiera obtener.

La mencionada Ley 15/1995, 30 may., es de aplicación, en defecto de las normas dictadas por las Comunidades Autónomas en ejercicio de sus competencias, en materia de Derecho civil, foral o especial, de conformidad con lo establecido en los Estatutos de Autonomía.


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
