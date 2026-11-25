---
name: propuesta-medidas-separacion-divorcio-contencioso-civ-0080
description: "Propuesta de medidas por separación o divorcio contencioso (Derecho catalán). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Propuesta de medidas por separación o divorcio contencioso (Derecho catalán)

> Formulario **CIV-0080** del plugin **Familia: separación, divorcio y medidas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 25-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Propuesta de medidas por separación o divorcio contencioso (Derecho catalán)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Propuesta de medidas por separación o divorcio contencioso (Derecho catalán)” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:propuesta-medidas-separacion-divorcio-contencioso-civ-0080`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: separación, divorcio y medidas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (5 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] AÑO
- [ ] GRUPO PROFESIONAL
- [ ] PETICIÓN

## Normas que cita el formulario

- art. 232 CC

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
(1) El art. 233-14 CCC establece que el cónyuge cuya situación económica, como consecuencia de la ruptura de la convivencia, resulte más perjudicada tiene derecho a solicitar en el primer proceso matrimonial una prestación compensatoria que no exceda del nivel de vida de que gozaba durante el matrimonio ni del que pueda mantener el cónyuge obligado al pago, teniendo en cuenta el derecho de alimentos de los hijos, que es prioritario.

Para la determinación de la prestación, el art 233-15 establece que la autoridad judicial, para fijar la cuantía y duración de la prestación compensatoria, debe valorar especialmente:

a) La posición económica de los cónyuges, teniendo en cuenta, si procede, la compensación económica por razón del trabajo o las previsibles atribuciones derivadas de la liquidación del régimen económico matrimonial.

b) La realización de tareas u otras decisiones tomadas en interés de la familia durante la convivencia, si eso ha reducido la capacidad de uno de los cónyuges para obtener ingresos.

c) Las perspectivas económicas previsibles de los cónyuges, teniendo en cuenta su edad y estado de salud y la forma en que se atribuye la guarda de los hijos comunes.

d) La duración de la convivencia.

e) Los nuevos gastos familiares del deudor, si procede.

Señala la doctrina las escasas variaciones que las nuevas disposiciones introducen respecto de la anterior regulación en el Código de Familia, por lo que resulta vigente la mayoría de la doctrina fijada por el TSJC en sus resoluciones respecto de la institución.

Así cabe mantener, como señaló el STSJ en diversas resoluciones, que la pensión compensatoria tiene su fundamento en la debilitación económica que puede sufrir uno de los cónyuges a consecuencia de la disolución matrimonial respecto a la situación o estatus que mantenía constante el vínculo. Así se deduce en forma meridiana de la propia dicción legal en la medida en que concede la pensión al cónyuge que "vegi més perjudicada la seva situació econòmica" y en la medida en que no puede exceder del "nivell de vida de que gaudia durant el matrimoni".

Se configura, pues, como una compensación del perjuicio que origina la separación o el divorcio en uno de los cónyuges, por lo que el presupuesto necesario para su nacimiento es la acreditación de ese perjuicio, para lo que se ha de atender al patrimonio e ingresos del demandante de la prestación y al nivel de vida que disfrutó la familia durante el matrimonio, por lo que el propósito de la prestación es reequilibradora.

La STSJC 19/2010 de 27 de mayo, Rec. 176/2009, refiere la doctrina por él establecida en reiteradas resoluciones en los siguientes términos:

" [NOMBRE DE LA PARTE] hemos llegado a calificarla, siguiendo a la mejor doctrina, como una institución que prolonga la solidaridad matrimonial después de la ruptura de la convivencia, a fin de equilibrar en la forma más equitativa posible la situación económica en que queda el cónyuge más perjudicado económicamente por la nulidad, separación o divorcio, en relación con la que mantenía constante la relación matrimonial (STSJC 8/2006 de 27 feb., Rec. 134/2005), si bien con una vocación inequívoca de caducidad, en la medida en que así lo indica la fijación legal de una serie de causas que pueden producir su extinción, bien por motivos contemplados al tiempo de su constitución -fijación de un plazo- o bien por causas sobrevenidas relacionadas con su naturaleza y función reequilibradora (STSJC 47/2003 de 11 dic., Rec. 88/2003)".

Debe tenerse en consideración que la repercusión económica de la ruptura en el acreedor de la prestación ha de producirse en el momento de la finalización de la convivencia y atendiendo a su situación económica anterior a la misma, no debiendo exceder la prestación del nivel de vida que tuvo durante el matrimonio ni del que pueda corresponder al obligado a raíz de la ruptura, atendidas las obligaciones alimenticias que éste pudiera tener para con los hijos, a las que se atribuyen expresamente carácter preferente. Así pues la comparación a efectuar ha de ser entre el nivel de vida que tuvo el presunto acreedor de la prestación y el que pasó a tener a raíz de la cesación de la convivencia, desnivel que tratará de cubrir la prestación, si bien ello ha de efectuarse en consideración a los limites referidos de las obligaciones económicas y nivel de vida correspondiente a raíz de la ruptura al deudor de la prestación.

(2) El art. 232.5 CCC regula también la que denomina compensación económica por razón de trabajo, que nace para equilibrar en lo posible las desigualdades que se puedan generar durante una convivencia estable cuando uno de los convivientes se dedica al cuidado del hogar y de los hijos o ayuda en el negocio percibiendo en tal caso una remuneración insuficiente, mientras que el otro se dedica al trabajo externo. Se trata de conseguir un equilibrio patrimonial justo y mesurado a la hora de la crisis de convivencia pero con la vista puesta en la necesidad de retribuir un trabajo y un esfuerzo colateral pero convergente no remunerado o remunerado hasta entonces insuficientemente.

========================================================================


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
