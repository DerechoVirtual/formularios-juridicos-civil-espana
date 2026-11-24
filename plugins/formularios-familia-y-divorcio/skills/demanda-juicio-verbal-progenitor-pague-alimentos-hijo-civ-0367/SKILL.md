---
name: demanda-juicio-verbal-progenitor-pague-alimentos-hijo-civ-0367
description: "Demanda de juicio verbal para que el progenitor pague alimentos al hijo. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio verbal para que el progenitor pague alimentos al hijo

> Formulario **CIV-0367** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Escrito de demanda al Tribunal de Instancia de juicio verbal de alimentos. Los alimentos se reclaman por una hija extramatrimonial frente al padre que ha dejado de satisfacerlos tras la muerte de la madre. Aunque la cuestión es discutida por la doctrina, el modelo contempla la NO sujeción al previo intento de resolución de controversias en vía no jurisdiccional por tratarse de materias excluidas del requisito de procedibilidad de acuerdo con el art. 4.1 II LO 1/2025, entre las cuales se encuentran los conflictos que afecten a derechos y obligaciones que no estén a disposición de las partes.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio verbal para que el progenitor pague alimentos al hijo» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio verbal para que el progenitor pague alimentos al hijo” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-juicio-verbal-progenitor-pague-alimentos-hijo-civ-0367`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (11 veces)
- [ ] IMPORTE (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] DOMICILIO (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] CALLE
- [ ] CORREO ELECTRÓNICO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DÍA
- [ ] FECHA
- [ ] IMPORTE EN CIFRA
- [ ] LUGAR
- [ ] NOMBRE DE LA ENTIDAD
- [ ] Nº
- [ ] Nº DE COLEGIADO/A
- [ ] SEDE
- [ ] TELÉFONO
- [ ] ÓRGANO

## Normas que cita el formulario

- art. 24.1 LEC
- art. 437.1 LEC
- art. 50.1 LEC
- art. 250.1.8.º LEC
- art. 266.1.º LEC
- art. 4.1 LO 1/2025
- art. 253.1 LEC
- art. 251 LEC
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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…MILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) A la hora de su acreditación, todos los poderes deben estar inscritos en el Registro Electrónico de Apoderamientos Judiciales (REAJ). Se supone que, para su acreditación, basta con la consulta (de dicho Registro) automatizada orientada al dato. Algo que está a disposición de cualquier Letrado de la Administración de Justicia. Sin embargo, dado que el art. 24.2 LEC, configura la certificación de dicha inscripción como vía subsidiaria de acreditación, para el caso de que el sistema no permita aquella consulta automatizada; se señala en el modelo que se acompaña certificación electrónica. El sistema permite emitir dicha certificación para quien inscribe el poder.

(2) El art. 155.3 LEC permite fijar expresar varios domicilios del demandado (el que aparezca en el padrón municipal o conste oficialmente a estos efectos; el que aparezca en Registro oficial o en publicaciones de colegios profesionales, si se trata de empresas o personas colegiadas; donde desarrolle su actividad profesional o laboral no ocasional; si es empresa mercantil, el domicilio de cualquiera de sus administradores, gerentes, o apoderados; o, si es asociación que consta en registro oficial; el domicilio del presidente, miembro o gestor de la Junta correspondiente). Cuando se señalen varios, indicará el orden a seguir para la notificación, con vistas al éxito de la misma.

(3) El art. 155.3 LEC configura una obligación adicional del demandante, consistente en aportar cuantos datos sean de utilidad para localizar al demandado: número de identificación fiscal o de extranjeros, nº [Nº] de teléfono o de fax, dirección de correo electrónico, o similares.

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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], representación que acredito mediante escritura de poder otorgada a mi favor (existen tres posibilidades para otorgar el apoderamiento al Procurador de los Tribunales, conforme dispone el art. 24.1 LEC)

[OPCIONAL — opción en función de cómo se haya otorgado el poder]

[ELEGIR UNA OPCIÓN: Si el poder se otorga a través de la sede judicial electrónica / Si el poder se otorga mediante comparecencia apud acta / Si el poder se otorga ante Notario]

bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS], abogado/a en ejercicio, con despacho profesional abierto en [LOCALIDAD], colegiado nº [Nº DE COLEGIADO/A] del Ilustre Colegio de la Abogacía de [LOCALIDAD], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que mediante el presente escrito vengo a formular DEMANDA DE JUICIO VERBAL DE ALIMENTOS, contra D./Dña. [NOMBRE Y APELLIDOS], con domicilio, primero en [DOMICILIO]; y segundo, el domicilio laboral en [DOMICILIO]); con email [CORREO ELECTRÓNICO]; y con número de teléfono móvil [TELÉFONO].

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa, e, incluso, en una eventual fase de ejecución por medios telemáticos, en términos del art. 399.1 II con relación al art. 437.1, ambos LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y nº [Nº] de teléfono:

Todo ello de conformidad con los siguientes hechos y fundamentos de derecho:

HECHOS

PRIMERO.- D./Dña. [NOMBRE Y APELLIDOS], mantuvo una relación semejante a la de los casados con el hoy demandado D./Dña. [NOMBRE Y APELLIDOS], de la que nació mi mandante el [ÓRGANO], que fue inscrita en el Registro Civil con mención de ambos progenitores. Se acompaña la correspondiente certificación literal de nacimiento expedida en el Registro Civil de [LOCALIDAD] (DOCUMENTO N.º [NÚMERO]).

SEGUNDO.- Durante un largo período de años no ha hubo mayores problemas de convivencia entre la madre de mi patrocinada y el hoy demandado, que compartían vivienda con el padre de aquélla, D./Dña. [NOMBRE Y APELLIDOS], hasta que a raíz de la repentina muerte de D./Dña. [NOMBRE Y APELLIDOS], en la primavera del presente año, y con la excusa de que no se había cumplido con la expectativa de que la vivienda se escriturara por D./Dña. [NOMBRE Y APELLIDOS] a favor de la difunta en proindiviso con el demandado, abandonó éste el domicilio común, trasladándose a vivir a casa de una hermana, sita en esta ciudad, calle [CALLE], sin que desde entonces y hasta el momento actual haya recibido su hija cantidad alguna para atender al sustento propio.

TERCERO.- Mi representada carece de recursos patrimoniales, y no percibe ningún ingreso, ya que se ha dedicado hasta el momento al estudio, cursando la carrera de geografía, y depende en este momento totalmente de las ayudas de su abuelo, que percibe una pensión de Seguridad Social que asciende a [IMPORTE] euros mensuales. Se aporta certificación del INSS (DOCUMENTO N.º [NÚMERO]).

El demandado tiene un trabajo fijo en la empresa [DENOMINACIÓN SOCIAL] por el que percibe unos ingresos mensuales de [IMPORTE] euros, como se acreditará.

))

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA.

Es competente el Tribunal al que me dirijo, por aplicación del art. 50.1 LEC, dado que pertenece a su circunscripción el lugar de domicilio del demandado.

II.- PROCEDIMIENTO.

Es procedente el trámite del juicio verbal por razón de la materia, en razón del art. 250.1.8.º LEC.

III.- PARTES.

De conformidad con el art. 266.1.º LEC, la legitimación ordinaria, en nombre propio, debe acreditarse preliminarmente de manera documental, lo que se cumple con la certificación registral que establece la filiación.

Tratándose de un juicio verbal por razón de la materia y no por razón de la cuantía, conforme a los arts. 23.1 y 31.1 LEC, es preceptiva la intervención de procurador de los tribunales y de abogado en ejercicio, ambos habilitados ante el Tribunal, estando identificados representante y director letrado en el encabezamiento de la demanda.

IV.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

Esta parte humildemente entiende que la presente demanda no está sujeta al previo intento de resolución de controversias en vía no jurisdiccional por tratarse de materias excluidas del requisito de procedibilidad de acuerdo con el art. 4.1 II LO 1/2025, entre las cuales se encuentran los conflictos que afecten a derechos y obligaciones que no estén a disposición de las partes.

V.- FUNDAMENTOS DE DERECHO MATERIALES O SOBRE EL FONDO DEL ASUNTO

Art. 143.2.º CCiv, que establece, con arraigo constitucional en el deber de asistencia en todos los órdenes que deben los padres a los hijos (art. 39.3 CE), la obligación de ascendientes y descendientes de darse recíprocamente alimentos.

Art. 142 CCiv, sobre el contenido y extensión de los mismos, dado que la actora no ha terminado su formación, sin que le sea imputable, puesto que le quedan dos cursos de su carrera universitaria, y además de sustento, habitación y vestido, la educación es deber de alimentos amplios del padre respecto de la hija, aun siendo ésta mayor de edad.

Art. 146 CCiv, que dispone que la cuantía de los alimentos será proporcionada al caudal o medios de quien los da y a las necesidades de quien los recibe, a cuyo objeto de evaluación se propone la nula fuente de ingresos de la hija, la aportación de vivienda y alimentación en sentido riguroso por el abuelo —ascendiente co-obligado—, y se fija la contribución para todo el resto de lo indispensable en las condiciones socioeconómicas habituales y el coste de los estudios, por relación a las rentas del demandado.

Art. 148 CCiv, que dice que se abonarán desde la fecha en que se interponga la demanda.

VI.- CUANTÍA DE LA DEMANDA.

La cuantía de la demanda, se justifica a los efectos del art. 253.1 LEC, en la cantidad de [IMPORTE], conforme a la regla 7.ª del art. 251 LEC.

VII.- COSTAS.

Las costas procesales se han de imponer al demandado por principio del vencimiento del art. 394 LEC.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito con los documentos que lo acompañan y sus copias, tenga por interpuesta demanda de juicio verbal de alimentos y, admitiéndola, acuerde dar traslado al demandado para que comparezca y la conteste, y seguido el juicio por sus trámites, dicte sentencia por la que, estimando la demanda, se condene al demandado D./Dña. [NOMBRE Y APELLIDOS] a que abone a mi representada, desde la fecha de la interposición de la demanda, la cantidad mensual de [IMPORTE] euros ([IMPORTE EN CIFRA] €), pagaderas por meses anticipados dentro de los [DÍA] primeros días de cada mes, que se actualizará anualmente de acuerdo con el índice oficial del coste de la vida fijado por el Instituto Nacional de Estadística u organismo que lo sustituya, con expresa imposición de las costas del juicio al demandado.

OTROSÍ DIGO: Que interesa al derecho de esta parte valerse del medio de prueba documental consistente en que se libre oficio a [NOMBRE DE LA ENTIDAD] a fin de que por su representante legal se certifique el importe de los ingresos íntegros y líquidos percibidos por [NOMBRE Y APELLIDOS] durante el año

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a
