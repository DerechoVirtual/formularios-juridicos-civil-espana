---
name: auto-declara-personalisimo-hacer-sigue-ejecucion-civ-1969
description: "Auto que declara personalísimo el hacer y sigue la ejecución por su equivalente con multa única. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Auto que declara personalísimo el hacer y sigue la ejecución por su equivalente con multa única

> Formulario **CIV-1969** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

Auto declarando personalísimo el hacer contenido en la sentencia cuya ejecución se despachó y acordando seguir adelante con la ejecución, de conformidad con lo solicitado por el ejecutante, para obtener el equivalente pecuniario de la prestación debida, imponiéndose al ejecutado una multa única.

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Auto que declara personalísimo el hacer y sigue la ejecución por su equivalente con multa única» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Auto que declara personalísimo el hacer y sigue la ejecución por su equivalente con multa única” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:auto-declara-personalisimo-hacer-sigue-ejecucion-civ-1969`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (3 veces)
- [ ] IMPORTE (3 veces)
- [ ] IMPORTE EN CIFRA (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] DESCRIBIR (2 veces)
- [ ] LUGAR
- [ ] Nº
- [ ] NÚMERO

## Normas que cita el formulario

- art. 709 LEC
- art. 709.2 LEC
- art. 451 LEC

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

- Ninguna.

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

AUTO

En [LUGAR], a [FECHA].

Juez/a Sr./a.

ANTECEDENTES DE HECHO

PRIMERO.- El pasado día [FECHA] se dictó auto despachando ejecución contra D./Dña. [NOMBRE Y APELLIDOS], que fue requerido para que, en el plazo de [Nº] días, realizara el hacer consistente en [DESCRIBIR], de acuerdo con lo ordenado en la sentencia firme dictada por este Tribunal en fecha [FECHA].

SEGUNDO.- Por el ejecutado se presentó un escrito, dentro del plazo estipulado en el auto despachando ejecución, en el que manifestó los motivos por los que se negaba a hacer lo que el título disponía, entendiendo que la obligación no era personalísima.

TERCERO.- Transcurrido el plazo de ejecución concedido a D./Dña. [NOMBRE Y APELLIDOS], y teniendo conocimiento de las alegaciones formuladas por el mismo, el ejecutante solicitó que se declarara que la obligación era de hacer personalísimo, y se aceptara su opción de que se le entregara un equivalente pecuniario de aquél.

FUNDAMENTOS DE DERECHO

PRIMERO.- En la ejecución de un título cuyo objeto sea una obligación de hacer lo primero que debe resolver el órgano judicial, de conformidad con lo dispuesto en el art. 709 LEC, es cuál sea la naturaleza de aquélla, es decir, si es o no de naturaleza personalísima, ya que de ello dependerá, exista o no negativa a cumplir por parte del ejecutado, que pueda optar en los términos establecidos por el artículo anterior el ejecutante.

SEGUNDO.- El ejecutado, D./Dña. [NOMBRE Y APELLIDOS], una vez que fue requerido se opuso al requerimiento ordenado por entender que la obligación impuesta en la sentencia no era de hacer personalísimo, alegación que fue rechazada por la parte contraria, quien al no cumplir aquél solicitó que, partiendo de ser "personalísima" la obligación, se accediera a su petición, en virtud de la cual optó por el equivalente pecuniario de la prestación objeto del título, y a cargo del ejecutado antes referido.

TERCERO.- La obligación impuesta al ejecutado es de naturaleza personalísima, porque tal naturaleza tienen las obligaciones consistentes en [DESCRIBIR], porque la misma no puede ser realizada por ningún tercero ajeno al mismo, al ser esenciales las cualidades personales que ostenta el ejecutado, todo ello según se desprende de las alegaciones, documentos y del propio título base de la ejecución, es decir, de la sentencia. Por tanto, debe accederse a la petición formulada por el ejecutante.

CUARTO.- Al haber optado el ejecutante por el equivalente, procede por lo ya expuesto, al tener el mismo la facultad legal de elegir, resolver en el sentido pedido, imponiéndole a su vez al ejecutado una multa única que ascenderá al cincuenta por ciento del precio o valor del hacer personalísimo de conformidad con lo dispuesto en los arts. 709.2 y 711 LEC.

En este caso, al constar que el precio o contraprestación del hacer personalísimo asciende a la cantidad de [IMPORTE] euros ([IMPORTE EN CIFRA] €), tal y como se recoge en el título ejecutivo, por lo que la multa a imponer será la de [IMPORTE] euros ([IMPORTE EN CIFRA] €).

PARTE DISPOSITIVA

En atención a todo lo anterior SE DECLARA el hacer contenido en la sentencia cuya ejecución se despachó PERSONALÍSIMO, y ha lugar a ACORDAR seguir adelante con la ejecución, de conformidad con lo solicitado por el ejecutante, para obtener el equivalente pecuniario de la prestación debida, imponiéndose al ejecutado una multa única de [IMPORTE] euros ([IMPORTE EN CIFRA] €).

Contra esta resolución cabe recurso de reposición en el plazo de CINCO DÍAS contados desde la notificación de esta resolución, conforme a los arts. 451 y 452 LEC.

Para interponer el recurso será necesario la constitución de un depósito de 25 euros, sin cuyo requisito no será admitido a trámite. El depósito se constituirá consignando dicho importe en la Cuenta de Depósitos y Consignaciones que este Tribunal tiene abierta en el grupo Banesto (Banco Español de Crédito) con el número [NÚMERO], indicando en el campo concepto del resguardo de ingreso que se trata de un "Recurso" código 00-Reposición. La consignación deberá ser acreditada al interponer el recurso (disp. adic. 15.ª de la LOPJ).

Están exentos de constituir el depósito para recurrir los incluidos en el apartado 5 de la disposición citada y quienes tengan reconocido el derecho a la asistencia jurídica gratuita.

Así lo acuerdo, mando y firmo:

Firma del Juez/a

========================================================================
