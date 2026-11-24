---
name: demanda-indemnizacion-resolucion-unilateral-civ-0520
description: "Demanda de indemnización por resolución unilateral del arrendamiento de local por el inquilino. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de indemnización por resolución unilateral del arrendamiento de local por el inquilino

> Formulario **CIV-0520** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Modelo de demanda de juicio ordinario sobre reclamación de indemnización de daños y perjuicios por resolución unilateral de contrato de arrendamiento de local por el arrendatario antes del plazo pactado.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de indemnización por resolución unilateral del arrendamiento de local por el inquilino» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de indemnización por resolución unilateral del arrendamiento de local por el inquilino” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:demanda-indemnizacion-resolucion-unilateral-civ-0520`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] Nº DE DOCUMENTO (7 veces)
- [ ] FECHA (6 veces)
- [ ] IMPORTE (6 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] FECHAS (2 veces)
- [ ] CALLE
- [ ] LUGAR
- [ ] SEDE

## Normas que cita el formulario

- art. 21.1 LOPJ
- art. 36.1 LEC
- art. 85.1 LOPJ
- art. 45 LEC
- art. 52.1.7.º LEC
- art. 249.1.6.º LEC
- art. 6.1.1.º LEC
- art. 7 LEC
- art. 10 LEC
- art. 253.1 LEC
- art. 251 LEC
- art. 23 LEC
- art. 399 LEC
- art. 399.3 LEC
- art. 5 Ley Orgánica 1/2025
- art. 1124 CC
- art. 1.256 CC
- art. 1556 CC
- art. 27 LAU
- art. 1106 CC
- art. 1101 CC
- art. 394 LEC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) En los contratos de arrendamiento para uso distinto del de vivienda (en cuya categoría se adscribe el que nos ocupa), al regir en ellos ampliamente lo dispuesto por la voluntad de las partes (art. 4.3 LAU 1994), es perfectamente válido y eficaz que se haya pactado por las partes el desistimiento, con o sin indemnización, rigiéndose en tal caso los requisitos, forma y efectos del desistimiento por lo expresamente convenido.

(2) En el modelo la indemnización se ha calculado sobre la base de las rentas que faltarían por cumplir hasta la finalización del contrato, pero téngase en cuenta que, atendiendo a las circunstancias del cada supuesto concreto, en ocasiones puede resultar desproporcionado exigir al arrendatario el abono de la totalidad de las rentas correspondientes al período incumplido del contrato anticipadamente resuelto, y deberá atemperarse el quantum indemnizatorio, como señala la doctrina jurisprudencial (SSTS de 20 de mayo de 2004, rec. 1968/1998 ó 9 de abril de 2012, rec. 229/2007).

========================================================================


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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a. de los Tribunales en nombre y representación de [LOCALIDAD], con domicilio en [LOCALIDAD], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO]; dirigido por el Abogado D./Dña. [NOMBRE Y APELLIDOS], que redacta y firma el presente escrito, con despacho profesional abierto en esta localidad, calle [CALLE], ante el Tribunal comparezco y como mejor proceda en derecho, DIGO:

Que por medio del presente escrito deduzco DEMANDA DE JUICIO ORDINARIO frente a D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], en reclamación de cantidad por daños y perjuicios derivados de resolución unilateral de contrato de arrendamiento de local, reclamación que se formula por un principal de [IMPORTE] euros, más intereses y costas, en base a los siguientes:

HECHOS

PRIMERO.- Mi mandante es propietario del local comercial sito en la planta baja del edificio número [NÚMERO] de esta localidad.

Se acompaña el título correspondiente como documento n.º [NÚMERO]

SEGUNDO.- Entre el demandado D./Dña. [NOMBRE Y APELLIDOS] y mi representado se convino un contrato de arrendamiento respecto del indicado local en fecha 31 de julio de 2009.

En dicho contrato se estipuló un plazo de duración de tres años, es decir, hasta el [FECHA], a cambio de una renta anual fijada en principio en la suma de [IMPORTE] euros dividida en doce mensualidades de

Se adjunta como documento n.º [NÚMERO] el referido contrato de arrendamiento.

TERCERO.- El pasado mes de enero, sin respetar el plazo de duración del contrato, la arrendataria hoy demandada comunicó a mi patrocinado su decisión de resolver unilateralmente dicho contrato antes de la expiración del periodo contractual, indicando que las llaves quedaban depositadas con efectos de [FECHA]; respondiendo al efecto y de manera inmediata la arrendadora hoy demandante, concretamente en fecha [FECHA] que no aceptaba en forma alguna dicha resolución unilateral y anticipada por no concurrir las causas previstas ni legal ni contractualmente para dicha resolución, y conminándole a cumplir íntegramente la totalidad del plazo convenido.

Se acompañan copias del burofax remitido y recibido como documentos números [Nº DE DOCUMENTO], y del acta notarial por la que puso las llaves del local a disposición de la actora como documento n.º [Nº DE DOCUMENTO]

CUARTO.- La parte actora manifiesta que, previo a la presentación de la presente demanda, se han llevaron a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad, y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria; incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, mi representado envío un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por el demandado por el mismo medio, rechazando el acuerdo/ habiendo sido solo posible un acuerdo parcial, viéndonos en la necesidad de acudir a la presente vía judicial, respecto a los extremos de la controversia en los que se mantiene la discrepancia.

Acompaño como documento nº [Nº DE DOCUMENTO], el requerimiento efectuado y como documento nº [Nº DE DOCUMENTO], la contestación del demandado.

La parte actora manifiesta que, previo a la presentación de la presente demanda, se han llevaron a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad, y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria; incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, mi representado envío un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por el demandado por el mismo medio, rechazando el acuerdo/ habiendo sido solo posible un acuerdo parcial, viéndonos en la necesidad de acudir a la presente vía judicial, respecto a los extremos de la controversia en los que se mantiene la discrepancia.

Acompaño como documento nº [Nº DE DOCUMENTO], el requerimiento efectuado y como documento nº [Nº DE DOCUMENTO], la contestación del demandado.

A los anteriores hechos son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA.

La jurisdicción ordinaria es la única competente para el conocimiento de los juicios que se susciten en territorio español con arreglo a lo establecido en los tratados y convenios internacionales en los que España sea parte, en las normas de la Unión Europea y en las leyes españolas (art. 21.1 LOPJ y art. 36.1 LEC).

La competencia objetiva corresponde a la Sección Civil del Tribunal de Instancia según lo dispuesto en el art. 85.1 LOPJ y art. 45 LEC, así como la territorial con arreglo al art. 52.1.7.º LEC, puesto que el Tribunal competente es el del lugar en que está sita la finca.

II.- PROCEDIMIENTO.

La presente demanda deberá sustanciarse por las normas del juicio ordinario, a tenor de lo prevenido en el art. 249.1.6.º LEC.

III.- CAPACIDAD.

Demandante y demandado, personas físicas, tienen capacidad para ser parte (art. 6.1.1.º LEC), titular de facultades y cargas del proceso, y asimismo plena capacidad procesal, al ser mayores de edad, sin limitación de ejercicio válido de derechos civiles, o para comparecer en juicio, en términos del art. 7 LEC, pretendiendo el actor y siendo pretendido el demandado, en sus respectivos nombres y derechos.

IV.- LEGITIMACIÓN ACTIVA Y PASIVA.

La legitimación activa viene dada a favor del actor por ser el arrendador en el contrato cuya resolución anticipada, unilateral y no justificada determina la obligación de indemnizar a cargo del demandado, al que correlativamente corresponde la legitimación pasiva, en su condición de arrendatario del local arrendado (art. 10 LEC).

V.- CUANTÍA.

Conforme al art. 253.1 LEC cifro la cuantía de la presente demanda en [IMPORTE] euros ( €) que es el importe de la cantidad que se reclama, según resulta de la interpretación combinada de las reglas 1.ª y 9.ª del art. 251 LEC.

VI.- POSTULACIÓN Y DEFENSA.

Conforme a los arts. 23 y 31 LEC se formula esta demanda por medio de Procurador/a. con poder notarial para pleitos, y con dirección y firma de Letrado habilitado. Asimismo se cumplen los requisitos formales del art. 399 LEC.

VII. CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por el art. 264.4º y art. 399.3 de la LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VIII.- FUNDAMENTOS DE DERECHO MATERIALES O SOBRE EL FONDO DEL ASUNTO.

Se ejercita acción personal al amparo de lo dispuesto en los arts. 1124 y 1556 CCiv, a fin de que se declare la resolución unilateral e injustificada del contrato por parte del arrendatario y se le condene a satisfacer al arrendador la correspondiente indemnización derivada de dicha resolución unilateral no permitida.

El contrato no es más que el resultado del concurso o acuerdo de voluntades de los contratantes, por lo que por regla general (como así se colige, entre otros preceptos legales, de lo dispuesto en el art. 1.256 CCiv al concretar que la validez y cumplimiento de los contratos no puede dejarse al arbitrio de uno de los contratantes), para adelantar la pérdida de la eficacia obligatoria que de ello deriva será necesario la misma voluntad conjunta que lo creó (mutuo disenso), salvo que proceda una resolución anticipada por incumplimiento de una de las partes, al amparo de lo dispuesto en el art. 1124 CCiv, o se haya pactado o exista un precepto legal que permita que la voluntad de una de las partes, sin que concurra el consentimiento de la otra, ponga fin a esa vinculación antes de la culminación de la vida contractual (desistimiento unilateral).

En los contratos bilaterales y sinalagmáticos el incumplimiento de uno de los contratantes (tal y como se desprende del precepto legal antes mentado, y para este concreto caso de los arts. 1556 CCiv y arts. 27 y 35 LAU 1994), faculta a la parte que ha cumplido con sus obligaciones o ha estado dispuesta a cumplirlas para optar bien por pedir el cumplimiento o por la resolución del contrato, pudiendo además, en ambos casos, exigir la indemnización de daños y perjuicios, que comprenderá tanto el perjuicio sufrido como el lucro cesante (art. 1106 CCiv).

Es clara la existencia de un incumplimiento contractual por el demandado, cuyo reconocimiento se postula, dado que nada, salvo la voluntad resolutoria de la arrendataria, basada en su propia conveniencia justifica la expiración contractual anterior al plazo pactado.

Conducta incumplidora que ha causado la frustración de la finalidad de obtener ingresos pretendida por la actora, al contratar, frustrando tal incumplimiento la obtención de ganancias, pactadas hasta la fecha 31 de julio del año 2012, con el consiguiente perjuicio derivado de la finalización anticipada del contrato, por voluntad unilateral, del deudor, sin plazo razonable para encontrar otro arrendatario a cambio de la percepción de una renta de mercado.

De ahí que, en la presente demanda, el quantum indemnizatorio derivado de la resolución unilateral no permitida por el contrato se haya calculado sobre la base de las rentas que le hubiese correspondido cobrar el arrendador hasta la extinción del contrato.

De conformidad con todo ello, se reclama la suma de [IMPORTE] euros, fijando el importe de la indemnización en la cuantía correspondiente a los seis meses de renta del periodo contractual que restaría por cumplir, descontado el importe de la fianza de [IMPORTE] euros prestada en su día por el arrendatario.

IX.- INTERESES.

Citamos los arts. 1101 y 1108 CCiv, sobre pago de los intereses moratorios a partir de la interpelación judicial.

IX.- COSTAS.

Conforme al art. 394 LEC las costas del procedimiento habrán de imponerse a la parte demandada.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que, habiendo por presentado este escrito, con sus documentos y copias, se sirva admitirlo, me tenga por parte en la representación que ostento de D./Dña. [NOMBRE Y APELLIDOS] y por interpuesta demanda de juicio ordinario, en el ejercicio de las acciones antedichas, frente a D./Dña. [NOMBRE Y APELLIDOS], emplazarle para que comparezca y conteste, seguir el procedimiento por sus trámites y, en su momento, dictar sentencia por la que, estimando íntegramente la demanda, declare la resolución del contrato de arrendamiento que vinculaba a las partes, por incumplimiento contractual del demandado D./Dña. [NOMBRE Y APELLIDOS], y condene a éste a indemnizar a mi patrocinado en la cantidad de [IMPORTE] euros, más los intereses legales desde la fecha de presentación de la demanda, como consecuencia de la resolución anticipada del mismo antes de plazo, con expresa imposición de las costas del procedimiento.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a./a
