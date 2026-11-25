---
name: aviso-arrendador-fin-contrato-vencer-plazo-pactado-lau-civ-2495
description: "Aviso del arrendador de fin del contrato al vencer el plazo pactado, LAU 1994. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Aviso del arrendador de fin del contrato al vencer el plazo pactado, LAU 1994

> Formulario **CIV-2495** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 25-11-2026.

## Qué es

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Aviso del arrendador de fin del contrato al vencer el plazo pactado, LAU 1994» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Aviso del arrendador de fin del contrato al vencer el plazo pactado, LAU 1994” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:aviso-arrendador-fin-contrato-vencer-plazo-pactado-lau-civ-2495`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (3 veces)
- [ ] CALLE (2 veces)
- [ ] COMPLETAR (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] Nº DE CLÁUSULA (2 veces)
- [ ] PISO (2 veces)
- [ ] FINCA
- [ ] LUGAR
- [ ] Nº
- [ ] NÚMERO

## Normas que cita el formulario

- art. 9 LAU

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

- Al principio del formulario: Rehecho: el preaviso del arrendador es de cuatro meses (art. 10.1 LAU, no treinta días), solo tras la duración mínima de cinco/siete años; se añade la prórroga extraordinaria (art. 10.2 y 10.3 LAU) y se actualiza la transcripción del art. 202 del Reglamento Notarial a su redacción vigente.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) La actual legislación locaticia prevé, como sabemos, un plazo mínimo de duración del arrendamiento de vivienda de cinco años (siete años si el arrendador fuese persona jurídica), ora porque se convenga ya inicialmente tal plazo, ora por el juego de la prórroga obligatoria hasta alcanzar tal duración (art. 9.1 LAU), durante el cual el arrendador no puede oponerse a la prórroga salvo en el caso de necesidad de la vivienda del art. 9.3 LAU. Y, a continuación, regula la prórroga tácita por plazos anuales hasta un máximo de tres años más, salvo que el arrendatario manifieste al arrendador con un mes de antelación a la fecha de terminación de cualquiera de las anualidades, su voluntad de no renovar el contrato (art. 10.1 LAU).

Este formulario se circunscribe a la notificación que habrá de dirigir el propietario al inquilino, con la antelación establecida legalmente -cuatro meses, como mínimo, a la fecha de vencimiento del contrato o de cualquiera de sus prórrogas, una vez transcurridos como mínimo cinco años de duración, o siete si el arrendador es persona jurídica (art. 10.1 LAU)- a fin de que no opere la prórroga del contrato. Los contratos celebrados antes del 6 de marzo de 2019 se rigen por el régimen jurídico que les era de aplicación (disposición transitoria primera del Real Decreto-ley 7/2019).

Aun notificada en plazo la voluntad de no renovar, el arrendatario de vivienda habitual puede solicitar una prórroga extraordinaria: de hasta un año, si acredita una situación de vulnerabilidad social y económica mediante informe o certificado de los servicios sociales, que el arrendador debe aceptar obligatoriamente cuando sea gran tenedor (art. 10.2 LAU); o por plazos anuales hasta un máximo de tres años, si la vivienda se ubica en una zona de mercado residencial tensionado declarada, salvo las excepciones previstas en el art. 10.3 LAU.

Repárese en la dicción del art. 7 del R.D. 297/1996, 23 feb., en la hipótesis de que hubiera procedido a inscribirse el contrato de arrendamiento en el Registro de la Propiedad. En tal caso, será bastante para cancelar la inscripción la copia del acta notarial por la que el arrendador notifique al arrendatario su voluntad de no renovar el contrato, siempre que la notificación se haya hecho en tiempo oportuno y personalmente por el Notario en la forma prevenida por el art. 202 del Reglamento Notarial (art. 7.4 del R.D. 297/1996). Este precepto, en su redacción vigente desde el 30 de enero de 2007, regula el objeto y forma de las actas de notificación y requerimiento, rezando del siguiente tenor:

«Art. 202. Las actas de notificación tienen por objeto transmitir a una persona una información o una decisión del que solicita la intervención notarial, y las de requerimiento, además, intimar al requerido para que adopte una determinada conducta.

El notario, discrecionalmente, y siempre que de una norma legal no resulte lo contrario, podrá efectuar las notificaciones y los requerimientos enviando al destinatario la cédula, copia o carta por correo certificado con aviso de recibo.

Siempre que no se utilice el procedimiento a que hace referencia el párrafo anterior, el notario se personará en el domicilio o lugar en que la notificación o el requerimiento deban practicarse, según la designación efectuada por el requirente, dando a conocer su condición de notario y el objeto de su presencia. De no hallarse presente el requerido, podrá hacerse cargo de la cédula cualquier persona que se encuentre en el lugar designado y haga constar su identidad. Si nadie se hiciere cargo de la notificación, se hará constar esta circunstancia. Cuando el edificio tenga portero podrá entenderse la diligencia con el mismo.

La diligencia se cumplimentará mediante entrega de cédula que, suscrita por el notario con media firma al menos, contendrá el texto literal de la notificación o el requerimiento y expresará el derecho de contestación del destinatario y su plazo, conforme al artículo 204. Si la diligencia se entendiera con persona distinta de éste, la cédula deberá entregarse en sobre cerrado en el que se hará constar la identidad del notario y el domicilio de la Notaría. El notario advertirá, en todo caso, al receptor de la obligación de hacer llegar a poder del destinatario el documento que le entrega, consignando en la diligencia este hecho, la advertencia y la respuesta que recibiere.

La cédula podrá ir extendida en papel común y no será necesario dejar en la matriz nota de su expedición; bastará indicar el carácter con que se expide y la fecha de su entrega.

El notario siempre que no pueda hacer entrega de la cédula deberá enviar la misma por correo certificado con acuse de recibo, tal y como establece el Real Decreto 1829/1999, de 3 de diciembre, o por cualquier otro procedimiento que permita dejar constancia fehaciente de la entrega.

La diligencia podrá practicarse en cualquier lugar distinto del designado, siempre que el destinatario se preste a ello y sea identificado por el notario.

Si se hubiere conseguido cumplimentar el acta, se hará constar así, la manera en que se haya producido la notificación y la identidad de la persona con la que se haya entendido la diligencia; si ésta se negare a manifestar su identidad o su relación con el destinatario o a hacerse cargo de la cédula, se hará igualmente constar. Si se hubiere utilizado el correo, o cualquier otro medio de envío de los previstos en este artículo, se consignarán sucesivamente las diligencias correspondientes.

La notificación o el requerimiento quedarán igualmente cumplimentados y se tendrán por hechos en cualquiera de las formas expresadas en este artículo».

Téngase en cuenta, también, lo dispuesto en el art. 82 de la Ley Hipotecaria.


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
