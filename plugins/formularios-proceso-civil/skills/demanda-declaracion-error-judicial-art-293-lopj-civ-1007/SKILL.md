---
name: demanda-declaracion-error-judicial-art-293-lopj-civ-1007
description: "Demanda de declaración de error judicial (art. 293 LOPJ). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de declaración de error judicial (art. 293 LOPJ)

> Formulario **CIV-1007** del plugin **Proceso civil: demandas, contestaciones, prueba y vista** (`formularios-proceso-civil`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 24-11-2026.

## Qué es

Modelo de demanda de error judicial, de conformidad con lo dispuesto en el artículo 293 de la Ley Orgánica del Poder Judicial.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de declaración de error judicial (art. 293 LOPJ)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de declaración de error judicial (art. 293 LOPJ)” para mi caso». También puedes invocarla directamente con `/formularios-proceso-civil:demanda-declaracion-error-judicial-art-293-lopj-civ-1007`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-proceso-civil:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso civil: demandas, contestaciones, prueba y vista) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] DESCRIBIR
- [ ] IMPORTE
- [ ] LUGAR
- [ ] NOMBRE DE LAS PARTES
- [ ] NOMBRE DEL SOLICITANTE
- [ ] Nº DE DOCUMENTO
- [ ] Nº DE HECHO
- [ ] PARTE DEMANDADA
- [ ] RESOLUCIÓN O ACTUACIÓN ERRÓNEA
- [ ] TIPO DE RECURSO
- [ ] TIPO Y Nº DE PROCEDIMIENTO
- [ ] ÓRGANO JUDICIAL
- [ ] ÓRGANO O PERSONA

## Normas que cita el formulario

- art. 293.1 b) LOPJ
- art. 293.1 c) LOPJ
- art. 514 Ley 1/2000
- art. 3.2 LO 1/2025
- art. 292 LOPJ
- art. 293.1 LOPJ
- art. 295 LOPJ
- art. 292.2 LOPJ
- art. 293.1 f) LOPJ
- art. 61 LOPJ
- art. 293.1 a) LOPJ

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

A LA SALA PRIMERA DEL TRIBUNAL SUPREMO

D./Doña [NOMBRE Y APELLIDOS], Procurador de los Tribunales en representación de D./Doña [NOMBRE Y APELLIDOS], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], ante esa Sala comparezco, bajo la dirección letrada de D./Doña [NOMBRE Y APELLIDOS], colegiado n.º [NÚMERO] del Ilustre Colegio de Abogados de Madrid, y como mejor proceda en Derecho, DIGO:

Que en la representación que ostento deduzco demanda de ERROR JUDICIAL, de conformidad con lo dispuesto en el artículo 293 de la Ley Orgánica del Poder Judicial, contra la sentencia dictada con fecha [FECHA] por [ÓRGANO JUDICIAL] en los Autos de Juicio [Nº DE PROCEDIMIENTO] n.º [NÚMERO], sobre [DESCRIBIR], seguidos a instancia de [NOMBRE DEL SOLICITANTE] contra [PARTE DEMANDADA], con fundamento en los siguientes

HECHOS

PRIMERO

A los anteriores hechos son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA

Según lo dispuesto en el art. 293.1 b) LOPJ, la demanda solicitando la declaración del error judicial se deducirá ante la Sala del Tribunal Supremo correspondiente al mismo orden jurisdiccional a quien se imputa el error.

II.- PROCEDIMIENTO

De conformidad con lo dispuesto en el art. 293.1 c) LOPJ, el procedimiento para sustanciar la pretensión será el del recurso de revisión en materia civil, es decir, por el procedimiento establecido en el art. 514 de la Ley 1/2000, de 7 de enero, de Enjuiciamiento Civil.

III.- LEGITIMACIÓN

La legitimación activa la ostenta mi representado por ser el perjudicado por la actuación jurisdiccional que ha sido causante del error, y respecto a la pasiva han de intervenir como partes, además de quienes lo fueron en el proceso precedente, el Ministerio Fiscal y la Administración del Estado, que será parte demandada de conformidad con lo dispuesto en el art. 293.1 c) LOPJ.

IV.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

Conforme a lo dispuesto en el art. 3.2 LO 1/2025, la presente demanda no está sujeta al previo intento de resolución de controversias en vía no jurisdiccional, en cuanto se excluye la obligatoriedad de los MASC en asuntos donde una de las partes sea una entidad del sector público. Dado que el error judicial es el paso previo para una reclamación de responsabilidad patrimonial contra el Estado, entra en esta exclusión, no existiendo, por otro lado, un "conflicto transfronterizo", "civil" o "mercantil" ordinario entre particulares que sea susceptible de mediación o conciliación ante el Tribunal Supremo.

V.- FUNDAMENTOS DE DERECHO MATERIAL DE LA PRETENSIÓN DEDUCIDA

En cumplimiento del mandato recogido en el art. 121 CE se regula en los arts. 292 a 296 LOPJ la responsabilidad objetiva del Estado por los daños y perjuicios sufridos por los justiciables por razón del funcionamiento de la Administración de Justicia; actuando la declaración judicial de reconocimiento de la existencia del error judicial como requisito habilitante del nacimiento de la acción indemnizatoria a reclamar en vía admistrativa, primero, y después en vía contencioso-administrativa en su caso (art. 293.1 y 2 LOPJ).

Según lo dispuesto en los arts. 292 y ss. LOPJ y doctrina jurisprudencial que los interpreta, los requisitos para que pueda estimarse la acción declarando un error judicial son:

a) Comisión del error en una actuación judicial encuadrable dentro de las funciones propiamente jurisdiccionales, como sucede en el caso de autos, que se consumó en un procedimiento [Nº DE PROCEDIMIENTO].
b) Acción u omisión del Juez que no constituya delito ni pudiera calificarse de ignorancia inexcusable, y que provenga de la valoración de hechos o de la aplicación del derecho, quedando excluido el producido por conducta culposa o dolosa del perjudicado (art. 295 LOPJ).

Al respecto, es reiterada la jurisprudencia que ha declarado:

el error judicial se configura como aquella actuación en que se incluyen equivocaciones manifiestas y palmarias en la fijación de los hechos o en la interpretación o aplicación de la Ley, pero como quiera que este proceso especial no puede confundirse con una tercera instancia, sólo cabe su apreciación cuando el Tribunal haya actuado abiertamente fuera de los cauces legales partiendo de hechos distintos de aquellos que hubieran sido objeto de debate, sin que pueda traerse a colación el ataque a conclusiones que no resulten ilógicas dentro del esquema traído al proceso, pero sí que es debido a una equivocada información sobre los hechos enjuiciados por contradecir lo que es evidente o a una aplicación del derecho que se basa en normas inexistentes o entendidas de modo palmario fuera de su sentido y alcance ‘ [SSTS de 4 de febrero, 13 de abril y 16 de junio de 1988 (; 21 de abril, 19 de mayo y 5 de diciembre de 1989; 18 de abril de 1992; 3 de marzo, rec. 2893/1990; 15 de octubre de 1993y 16 de octubre de 1993, rec. 1668/1986; 7 de febrero de 1994, rec. 1744/1991].

La sentencia impugnada incide en el error que se denuncia que, según abundante y uniforme doctrina jurisprudencial ha de ser patente, grave y palmario (STS de 1 de marzo de 1996, rec. 6891/1992).

Y en el presente caso queda constancia del error en la actividad jurisdiccional al margen de los cauces legales, en la [RESOLUCIÓN O ACTUACIÓN ERRÓNEA].

c) Justificación de un daño efectivo, evaluable económicamente e individualizado con relación a una persona (art. 292.2 LOPJ) y que se concreta, en el supuesto de autos, en la cuantía de [IMPORTE].
d) Agotamiento de los recursos legales dentro del proceso, en tanto la resolución que ha originado el error ha adquirido firmeza y se han utilizado todos los recursos ordinarios posibles (art. 293.1 f) LOPJ), puesto que interpuesto recurso [TIPO DE RECURSO], éste ha sido desestimado.

Se hace constar que el recurso de amparo no es uno de los comprendidos en el art. 293.1 f) LOPJ, ya que no se trata de recurso propiamente jurisdiccional y por ello no actúa dicho recurso como previo al procedimiento de error judicial (SSTS -I- de 22 de abril de 1996, rec. 2637/1994; 4 de diciembre de 1996, rec. 1867/1992), criterio mayoritario mantenido por esa Sala y que cuenta además con el apoyo del Auto de 22 de mayo de 1997 de la Sala Especial del art. 61 LOPJ, en el sentido de que el plazo de tres meses debe contarse desde la resolución judicial no susceptible de recurso, sin comprender en éste el de amparo constitucional (STS 15 de febrero de 2001, rec. 99/1999).

e) Ejercicio de la acción dentro del plazo de tres meses desde el día en que pudo ejercitarse (art. 293.1 a) LOPJ), cumplido en autos según se ha razonado en el hecho [Nº DE HECHO] de este escrito.

VI.- COSTAS

En materias de costas resulta de aplicación el artículo 394 de la Ley de Enjuiciamiento Civil.

Por lo expuesto,

SUPLICO A LA SALA

Que teniendo por presentado este escrito, documentos acompañados y copias de todo ello los admita, me tenga por comparecido y parte en la representación que ostento, entendiéndose conmigo las sucesivas actuaciones, y por promovida DEMANDA DE ERROR JUDICIAL contra la resolución firme de [FECHA], dictada por [ÓRGANO O PERSONA] en los autos [TIPO Y Nº DE PROCEDIMIENTO], reclamándose los autos originales de ese juicio para su incorporación a las presentes actuaciones, ordenándose emplazar a [NOMBRE DE LAS PARTES] para que comparezcan a usar de sus derechos, librándose al efecto los oportunos despachos; y tras la sustanciación del procedimiento, seguido por el trámite previsto en el artículo 514 de la Ley de Enjuiciamiento Civil, con la audiencia del Ministerio Fiscal y de la Administración del Estado, representada por el Letrado del Estado, se dicte sentencia declarando el error judicial del reseñado órgano judicial, y todo ello con expresa condena en costas del presente procedimiento a quien se opusiere.

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a

========================================================================
