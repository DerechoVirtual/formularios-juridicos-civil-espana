---
name: demanda-desahucio-precario-contra-conviviente-ocupa-civ-2234
description: "Demanda de desahucio por precario contra el conviviente que ocupa la vivienda tras morir su pareja. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de desahucio por precario contra el conviviente que ocupa la vivienda tras morir su pareja

> Formulario **CIV-2234** del plugin **Familia: separación, divorcio y medidas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 25-11-2026.

## Qué es

Demanda de juicio verbal de desahucio en precario, en la que se reivindica el inmueble con fundamento en la extinción de una pareja de hecho por fallecimiento de uno de los convivientes, que no da lugar a título alguno de posesión del superviviente ocupante.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de desahucio por precario contra el conviviente que ocupa la vivienda tras morir su pareja» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de desahucio por precario contra el conviviente que ocupa la vivienda tras morir su pareja” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-desahucio-precario-contra-conviviente-ocupa-civ-2234`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: separación, divorcio y medidas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] CALLE (2 veces)
- [ ] FECHA (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] COMPLETAR
- [ ] LUGAR
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] Nº DE COLEGIADO/A
- [ ] PROFESIÓN
- [ ] SEDE

## Normas que cita el formulario

- art. 36 Ley 1/2000
- art. 68 Ley 1/2000
- art. 52.1.7 Ley 1/2000
- art. 6 Ley 1/2000
- art. 10 Ley 1/2000
- art. 250.2 Ley 1/2000
- art. 253 Ley 1/2000
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 1750 Código Civil
- art. 1740 Código Civil
- art. 1543 Código Civil
- art. 394 Ley 1/2000

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

- Junto a «… CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE] QUE POR TURNO DE REPARTO CORRESPONDA»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) La regulación específica de las parejas no casadas es hoy una realidad en algunas Comunidades Autónomas:

Andalucía: Ley 5/2002, de 16 de diciembre, de Parejas de Hecho, Decreto 35/2005, de 15 de febrero, por el que se constituye y regula el Registro de Parejas de Hecho

Aragón: Título VI del Libro II del Código del Derecho Foral de Aragón

Asturias: Ley 4/2002, de 23 de mayo, de parejas estables

Cantabria: Ley 1/2005, de 16 de mayo, de Parejas de Hecho de la Comunidad Autónoma de Cantabria

Castilla-La Mancha: Decreto 124/2000, de 11 de julio, registro de parejas de hecho

Castilla y León: Decreto 117/2002, de 24 de octubre, registro de uniones de hecho

Cataluña: Capítulo IV del título III del libro segundo del Código Civil de Cataluña

Extremadura: Ley 5/2003, de 20 de marzo, de parejas de hecho

Galicia: Disp. Adic. 3.ª Ley 2/2006, de 14 de junio, de Derecho Civil de Galicia

Islas Baleares: Ley 18/2001, de 19 de diciembre, de parejas estables

Islas Canarias: Ley 5/2003, de 6 de marzo, de parejas de hecho

Madrid: Ley 11/2001, de 19 de diciembre, de uniones de hecho

Navarra: Ley Foral 6/2000, de 3 de julio, igualdad jurídica de las parejas estables

País Vasco: Ley 2/2003, de 7 de mayo, de parejas de hecho

Valencia: Ley 5/2012, de 15 de octubre, de la Generalitat, de Uniones de Hecho Formalizadas de la Comunitat Valenciana, Decreto 34/2022 de 1 de abril, del Consell, por el que se regulan la organización y el funcionamiento del Registro de Uniones de Hecho Formalizadas, así como los procedimientos de inscripción, modificación y cancelación de uniones en el mismo.

(2) La sentencia del Tribunal Supremo, Sala Primera, de lo Civil, de 27 de marzo de 2008, rec. 190/2001, argumenta para desestimar el recurso interpuesto por el conviviente supérstite en demanda de desahucio por precario interpuesta por los herederos de la dueña de la vivienda, que no se puede aplicar en el caso del derecho de uso de la vivienda familiar, la misma doctrina cuando se trata de la ruptura de la convivencia entre convivientes que cuando fallece uno de ellos.

«TERCERO. En el segundo motivo se denuncia la infracción de la jurisprudencia sobre unión de hecho y más concretamente, las sentencias de 10 marzo 1998 y 16 diciembre 1996 . Dice el recurrente que "la jurisprudencia viene admitiendo frente a la idea de que las parejas de hecho no les son aplicables las normas reguladoras del matrimonio ni de los regímenes económico matrimoniales, y por razón de analogía, y basándose en la necesidad de protección al conviviente perjudicado, que las normas sobre uso de la vivienda familiar, deben proyectarse más allá de su estricto ámbito a situaciones como la convivencia prolongada de un hombre y una mujer como pareja, en este caso, al fallecer la pareja" del recurrente. Este tiene un título posesorio que no se basa en la mera tolerancia y tiene fundamento propio.

Este motivo se desestima.

Las sentencias que se citan como infringidas se refieren todas ellas al supuesto de la ruptura de las relaciones de convivencia de hecho y a los efectos que va a producir entre los convivientes; en estas situaciones, la jurisprudencia de esta Sala ha venido sosteniendo, (por todas, la sentencia de 12 septiembre 2005, rec. 980/2002), que se trata de una situación no regulada, pero no prohibida, en la que en defecto de pacto entre los convivientes, deben aplicarse los principios generales del derecho. En el presente litigio no se produce ninguna de las condiciones que permiten la aplicación de la doctrina que se cita como infringida, porque el problema no se plantea entre los convivientes, sino entre el conviviente supérstite y los herederos de la conviviente premuerta, que falleció sin haber otorgado testamento ni favorecer de ningún modo al superviviente. Por ello no puede considerarse que el recurrente ostente ningún título que le permita mantener la posesión de la vivienda propiedad de la premuerta. No alega ningún título que justifique su posesión y le permita oponerla frente a la acción de desahucio por precario interpuesta por los titulares de la vivienda. Esta falta es determinante para el éxito de la acción ejercitada por los herederos.

Además, si bien es cierto que la Constitución, en su Art. 47 protege el derecho a la vivienda y que este es uno de los argumentos utilizados en la STC 222/1992 para declarar inconstitucional la anterior legislación sobre arrendamientos urbanos que no preveía la subrogación del conviviente supérstite en el título de arrendatario, la situación del recurrente tampoco puede equipararse, porque simplemente carece de título y se encontraba en la vivienda como precarista, por lo que, fallecida la propietaria, no tiene ninguna legitimación para oponerse a la demanda interpuesta por los herederos nuevos propietarios. Asimismo, la jurisprudencia que el propio recurrente cita como infringida impide la aplicación por analogía de las reglas del régimen económico matrimonial de los gananciales, puesto que ambas sentencias declaran que "[...] debe rechazarse la aplicación analógica de los regímenes económico matrimoniales, puesto que la libertad que se autoconceden los convivientes al margen de las formalidades matrimoniales, no puede paradójica y contradictoriamente tener parigual con vinculaciones societarias de carácter económico [...]".»


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
