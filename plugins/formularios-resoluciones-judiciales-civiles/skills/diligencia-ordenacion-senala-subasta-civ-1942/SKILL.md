---
name: diligencia-ordenacion-senala-subasta-civ-1942
description: "Diligencia de ordenación que señala la subasta. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Diligencia de ordenación que señala la subasta

> Formulario **CIV-1942** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

DILIGENCIA DE ORDENACIÓN LETRADO DE LA ADMINISTRACIÓN DE JUSTICIA SR./A. Firmas Diligencia de ordenación sacando a subasta por el precio de su valoración pericial los bienes muebles embargados al ejecutado, señalando la fecha de la celebración y publicándolo por edictos.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Diligencia de ordenación que señala la subasta» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Diligencia de ordenación que señala la subasta” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:diligencia-ordenacion-senala-subasta-civ-1942`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (4 veces)
- [ ] LUGAR (2 veces)
- [ ] IMPORTE
- [ ] LOCALIDAD
- [ ] NOMBRE Y APELLIDOS
- [ ] NÚMERO

## Normas que cita el formulario

- art. 643 LEC
- art. 652 LEC
- art. 646.1 LEC
- art. 645.1 LEC
- art. 646 LEC
- art. 650.5 LEC

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

DILIGENCIA DE ORDENACIÓN LETRADO DE LA ADMINISTRACIÓN DE JUSTICIA SR./A.

En [LUGAR], a [FECHA].

Por presentado el anterior escrito por el Procurador Sr./a [NOMBRE Y APELLIDOS], únase a los autos de su razón.

Conforme se interesa en dicho escrito y disponen los arts. 643 y 644 LEC, en atención a la valoración definitiva del bien embargado a los efectos de la ejecución, siendo previsible que con su realización se obtenga una cantidad de dinero que cubra, cuanto menos, los gastos originados para la subasta, se acuerda la celebración de la misma para la realización del bien mueble embargado consistente en (breve descripción del bien embargado o de los lotes en que se integran los mismos) sirviendo de tipo a efectos de subasta y en ausencia de precio pactado entre las partes, el fijado en resolución de fecha [FECHA] consistente en [IMPORTE] euros (o detalle del valor de ejecución de cada lote).

La subasta tendrá lugar en el Portal dependiente de la Agencia Estatal Boletín Oficial del Estado para la celebración electrónica de subastas a cuyo sistema de gestión tendrán acceso todas las Oficinas judiciales. Todos los intercambios de información que deban realizarse entre las Oficinas judiciales y el Portal de Subastas se realizarán de manera telemática. Cada subasta estará dotada con un número de identificación único.

La subasta se abrirá transcurridas, al menos, veinticuatro horas desde la publicación del anuncio en el "Boletín Oficial del Estado", cuando haya sido remitida al Portal de Subastas la información necesaria para el comienzo de la misma.

Una vez abierta la subasta solamente se podrán realizar pujas electrónicas con sujeción a las normas de esta Ley en cuanto a tipos de subasta, consignaciones y demás reglas que le fueren aplicables. En todo caso el Portal de Subastas informará durante su celebración de la existencia y cuantía de las pujas.

Para poder participar en la subasta electrónica, los interesados deberán estar dados de alta como usuarios del sistema, accediendo al mismo mediante mecanismos seguros de identificación y firma electrónicos de acuerdo con lo previsto en la Ley 59/2003, de 19 de diciembre, de firma electrónica, de forma que en todo caso exista una plena identificación de los licitadores. El alta se realizará a través del Portal de Subastas mediante mecanismos seguros de identificación y firma electrónicos e incluirá necesariamente todos los datos identificativos del interesado. A los ejecutantes se les identificará de forma que les permita comparecer como postores en las subastas dimanantes del procedimiento de ejecución por ellos iniciado sin necesidad de realizar consignación.

El ejecutante, el ejecutado o el tercer poseedor, si lo hubiere, podrán, bajo su responsabilidad y, en todo caso, a través de la oficina judicial ante la que se siga el procedimiento, enviar al Portal de Subastas toda la información de la que dispongan sobre el bien objeto de licitación, procedente de informes de tasación u otra documentación oficial, obtenida directamente por los órganos judiciales o mediante Notario y que a juicio de aquéllos pueda considerarse de interés para los posibles licitadores. También podrá hacerlo el LAJ por su propia iniciativa, si lo considera conveniente.

Las pujas se enviarán telemáticamente a través de sistemas seguros de comunicaciones al Portal de Subastas, que devolverá un acuse técnico, con inclusión de un sello de tiempo, del momento exacto de la recepción de la postura y de su cuantía. El postor deberá también indicar si consiente o no la reserva a que se refiere el párrafo segundo del apartado 1 del art. 652 LEC y si puja en nombre propio o en nombre de un tercero. Serán admisibles posturas por importe superior, igual o inferior a la más alta ya realizada, entendiéndose en los dos últimos supuestos que consienten desde ese momento la reserva de consignación y serán tenidas en cuenta para el supuesto de que el licitador que haya realizado la puja igual o más alta no consigne finalmente el resto del precio de adquisición. En el caso de que existan posturas por el mismo importe, se preferirá la anterior en el tiempo. El portal de subastas sólo publicará la puja más alta entre las realizadas hasta ese momento.

Anúnciese la subasta por medio de edicto, con los requisitos establecidos en el art. 646.1 LEC.

Al otrosí primero, habida cuenta la importancia de los bienes que se sacan a subasta, conforme se interesa por la parte ejecutante en su escrito de fecha [FECHA] y dispone el art. 645.1 y 2 LEC se acuerda la publicación de los edictos señalando la subasta, con el contenido que indica el art. 646 LEC en los siguientes medios de difusión social (relación de periódicos públicos o privados en los que se insertarán los edictos) quedando obligado al pago cada parte, de los gastos derivados de las medidas que, para la publicidad de la subasta, hubieran solicitado, sin perjuicio de incluir en la liquidación de costas los gastos que, por este concepto, soporte el ejecutante.

Notifíquese la presente resolución al ejecutado, haciéndole saber que, según lo dispuesto en el art. 650.5 LEC, en cualquier momento anterior a la aprobación del remate o de la adjudicación al ejecutante podrá el ejecutado liberar sus bienes pagando íntegramente lo que se deba al ejecutante por principal, intereses y costas. En este supuesto, el LAJ acordará mediante decreto la suspensión de la subasta o dejar sin efecto la misma, y lo comunicará inmediatamente en ambos casos al Portal de Subastas.

Contra esta resolución cabe interponer recurso de reposición, mediante escrito ante el LAJ que se presenta dentro de los cinco días hábiles siguientes al de notificación, y en el que deberá indicarse la infracción cometida a juicio del recurrente, y sin perjuicio del cual se llevará a efecto lo acordado.

Para interponer el recurso será necesario la constitución de un depósito de 25 euros, sin cuyo requisito no será admitido a trámite. El depósito se constituirá consignando dicho importe en la Cuenta de Depósitos y Consignaciones que este Tribunal tiene abierta en [LOCALIDAD] con el número [NÚMERO], indicando en el campo concepto del resguardo de ingreso que se trata de un "Recurso" código 00-Reposición. La consignación deberá ser acreditada al interponer el recurso (disp. adic. 15.ª de la LOPJ).

Están exentos de constituir el depósito para recurrir los incluidos en el apartado 5 de la disposición citada y quienes tengan reconocido el derecho a la asistencia jurídica gratuita.

Así lo acuerdo y firmo,

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma del Letrado/a de la Administración de Justicia

========================================================================
