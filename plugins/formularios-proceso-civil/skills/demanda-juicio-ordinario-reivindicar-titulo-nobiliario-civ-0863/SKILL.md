---
name: demanda-juicio-ordinario-reivindicar-titulo-nobiliario-civ-0863
description: "Demanda de juicio ordinario para reivindicar un título nobiliario. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio ordinario para reivindicar un título nobiliario

> Formulario **CIV-0863** del plugin **Proceso civil: demandas, contestaciones, prueba y vista** (`formularios-proceso-civil`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 24-11-2026.

## Qué es

Demanda sobre materia de derechos honoríficos consistente en que se declare el mejor derecho genealógico del actor para llevar, usar, y poseer con todos los honores, prerrogativas y preeminencias el título de Vizconde, condenando a las codemandadas (Vizcondesa e hija) a estar y pasar por ello y a respetar la declaración de ineficacia proclamada.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio ordinario para reivindicar un título nobiliario» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio ordinario para reivindicar un título nobiliario” para mi caso». También puedes invocarla directamente con `/formularios-proceso-civil:demanda-juicio-ordinario-reivindicar-titulo-nobiliario-civ-0863`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-proceso-civil:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso civil: demandas, contestaciones, prueba y vista) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (29 veces)
- [ ] LOCALIDAD (10 veces)
- [ ] FECHA (7 veces)
- [ ] Nº DE DOCUMENTO (6 veces)
- [ ] NOMBRE DEL TÍTULO NOBILIARIO (5 veces)
- [ ] AÑO (3 veces)
- [ ] Nº (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] FECHAS (2 veces)
- [ ] CORREO ELECTRÓNICO
- [ ] DÍA
- [ ] LUGAR
- [ ] MES Y AÑO
- [ ] Nº DE COLEGIADO/A
- [ ] SEDE
- [ ] TELÉFONO

## Normas que cita el formulario

- art. 24.1 LEC
- art. 399.1 LEC
- art. 265.2 LEC
- art. 9.2 LOPJ
- art. 36 LEC
- art. 44 LEC
- art. 85.1 LOPJ
- art. 50.1 LEC
- art. 249.1 LEC
- art. 10 LEC
- art. 23 LEC
- art. 5 Ley Orgánica 1/2025
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
(1) A la hora de su acreditación, todos los poderes deben estar inscritos en el Registro Electrónico de Apoderamientos Judiciales (REAJ). Se supone que, para su acreditación, basta con la consulta (de dicho Registro) automatizada orientada al dato. Algo que está a disposición de cualquier Letrado de la Administración de Justicia. Sin embargo, dado que el art. 24.2 LEC, configura la certificación de dicha inscripción como vía subsidiaria de acreditación, para el caso de que el sistema no permita aquella consulta automatizada; se señala en el modelo que se acompaña certificación electrónica. El sistema permite emitir dicha certificación para quien inscribe el poder.

(2) El art. 155.3 LEC permite fijar expresar varios domicilios del demandado (el que aparezca en el padrón municipal o conste oficialmente a estos efectos; el que aparezca en Registro oficial o en publicaciones de colegios profesionales, si se trata de empresas o personas colegiadas; donde desarrolle su actividad profesional o laboral no ocasional; si es empresa mercantil, el domicilio de cualquiera de sus administradores, gerentes, o apoderados; o, si es asociación que consta en registro oficial; el domicilio del presidente, miembro o gestor de la Junta correspondiente). Cuando se señalen varios, indicará el orden a seguir para la notificación, con vistas al éxito de la misma.

(3) El art. 155.3 LEC configura una obligación adicional del demandante, consistente en aportar cuantos datos sean de utilidad para localizar al demandado: número de identificación fiscal o de extranjeros, nº [Nº] de teléfono o de fax, dirección de correo electrónico, o similares.


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

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], representación que acredito mediante escritura de poder otorgada a mi favor (existen tres posibilidades para otorgar el apoderamiento al Procurador de los Tribunales, conforme dispone el art. 24.1 LEC)

[OPCIONAL — opción en función de cómo se haya otorgado el poder]

[ELEGIR UNA OPCIÓN: Si el poder se otorga a través de la sede judicial electrónica / Si el poder se otorga mediante comparecencia apud acta / Si el poder se otorga ante Notario]

bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS], abogado/a en ejercicio, con despacho profesional abierto en [LOCALIDAD], colegiado nº [Nº DE COLEGIADO/A] del Ilustre Colegio de la Abogacía de [LOCALIDAD], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que mediante el presente escrito vengo a formular DEMANDA DE JUICIO DECLARATIVO ORDINARIO SOBRE MATERIA DE DERECHOS HONORÍFICOS, contra D./Dña. [NOMBRE Y APELLIDOS], con domicilio, primero en [DOMICILIO]; y segundo, el domicilio laboral en [DOMICILIO]); con email [CORREO ELECTRÓNICO]; y con número de teléfono móvil [TELÉFONO].

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa, e, incluso, en una eventual fase de ejecución por medios telemáticos, en términos del art. 399.1 II LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y nº [Nº] de teléfono:

Fundamento mi pretensión en los siguientes:

HECHOS

PRIMERO.- La Reina Isabel II otorgó la merced del Vizcondado de [NOMBRE DEL TÍTULO NOBILIARIO] mediante Real Carta de 6 de marzo de 1855 a favor de D./Dña. [NOMBRE Y APELLIDOS], así como para sus herederos y sucesores.

Se aporta como documento n.º [Nº DE DOCUMENTO] la carta concesional.

SEGUNDO.- D./Dña. [NOMBRE Y APELLIDOS] falleció en [LOCALIDAD], sin descendencia, quedando vacante el título por un largo periodo de tiempo, hasta que la descendiente D./Dña. [NOMBRE Y APELLIDOS], nacida en [LOCALIDAD], el [FECHA], lo rehabilitó en fecha 21 de julio de [AÑO] (Carta de Sucesión otorgada el 5 de enero de [AÑO]).

Se aporta como documento n.º [Nº DE DOCUMENTO] el certificado literal de nacimiento de D./Dña. [NOMBRE Y APELLIDOS], y como documento n.º [Nº], la mentada carta, resolución de la Dirección General de lo Contencioso del Ministerio de Justicia de 11 de enero de [AÑO].

TERCERO.- Desde esta última poseedora acreditada (Segunda Vizcondesa), una vez que falleció sin herederos, pasó el título nobiliario en conflicto a la demandada, D./Dña. [NOMBRE Y APELLIDOS] —sobrino/a de aquélla— que obtuvo Carta de Sucesión el 22 de diciembre de 1986, la que previamente había obtenido la cesión de su madre codemandada, del mismo nombre, otorgada en escritura de 24 de enero de 1986.

Acompañamos como documento n.º [Nº DE DOCUMENTO] la mentada carta, resolución de la Dirección General de lo Contencioso del Ministerio de Justicia de 14 de julio de 1986, y como documento n.º [Nº], reproducción de copia de la escritura notarial de cesión por [NOMBRE Y APELLIDOS], y no teniendo a mi disposición el documento original, de conformidad con el art. 265.2 LEC designo el protocolo general corriente del Notario de [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS]

CUARTO.- Mi principal es el hijo primogénito de D. [NOMBRE Y APELLIDOS], que falleció en [LOCALIDAD] el [DÍA] de [MES Y AÑO], y era hijo del hermano mayor de D.ª [NOMBRE Y APELLIDOS], y por consiguiente primo y sobrino de las codemandadas.

Se adjuntan como documentos nos certificaciones literales de nacimiento y defunción de D. Fernando [NOMBRE Y APELLIDOS], de su hijo demandante y de nacimiento del demandante.

QUINTO.- El indicado hermano mayor de D.ª [NOMBRE Y APELLIDOS], abuelo paterno de mi poderdante, D./Dña. [NOMBRE Y APELLIDOS], nació en [LOCALIDAD] el [FECHA] y murió en [LOCALIDAD] el [FECHA].

Se adjuntan como documentos nos.y certificaciones literales de nacimiento y defunción de D./Dña. [NOMBRE Y APELLIDOS]

Sobre estos hechos se vierten los siguientes razonamientos o valoraciones:

1.- Mi principal es colateral, en la misma línea y grado de la finada D.ª [NOMBRE Y APELLIDOS] (), por lo que por relación a la última poseedora del Título gozaba del mejor derecho nobiliario por ser varón.
2.- Mi principal, de otra parte, suprimida la varonía y el sexo, detenta su mejor derecho basado en que al tiempo de la rehabilitación del Título por D.ª [NOMBRE Y APELLIDOS] (nacida el [FECHA]), que lo ostentó creando una nueva cabeza de línea en la sucesión de la merced, vivía su abuelo paterno, D. [NOMBRE Y APELLIDOS], padre de D. [NOMBRE Y APELLIDOS] y hermano de la primera, estando ambos en igualdad de línea y grado con relación al primer Vizconde, pero el abuelo del actor era, no sólo varón sino el de mayor edad, y aunque hubiera podido rehabilitar el Título con mejor derecho o impugnar la concesión, no lo efectuó, por razón de su ideología republicana, y al contrario, respetó la decisión de su hermana pequeña, y mantuvo su postura hasta su fallecimiento en [LOCALIDAD].

Por lo tanto, se apoya también la reivindicación en la representación que se ejercita del mejor derecho que podía asistirle a su antecesor D. [NOMBRE Y APELLIDOS]

QUINTO.- Previamente a la presentación de la presente demanda, se llevaron a cabo diversos esfuerzos de negociación con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad, y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria.

Entre las acciones realizadas, se incluyen el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución; así como la participación en reuniones llevadas a cabo los días [FECHAS], cuyos objetivos fueron buscar una conciliación respecto de las diferencias planteadas.

Se adjuntan como prueba copias de las comunicaciones enviadas y recibidas durante el proceso de negociación, incluidas cartas, correos electrónicos y/o actas de reuniones como documentos números [Nº DE DOCUMENTO].

Finalmente, mi representado envió un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por el demandado por el mismo medio, rechazando el acuerdo, viéndonos en la necesidad de acudir a la presente vía judicial.

Acompaño como documento nº [Nº DE DOCUMENTO], el requerimiento efectuado y como documento nº [Nº DE DOCUMENTO], la contestación del demandado.

A los anteriores hechos, son aplicables los siguientes:

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA

A) JURISDICCIÓN

POTESTAD JURISDICCIONAL.- La potestad jurisdiccional se ejerce por los Tribunales determinados por las leyes, según las normas de competencia y procedimiento que las mismas establezcan (art. 117.3 CE)

JURISDICCIÓN CIVIL.- Los Tribunales del orden civil conocerán, además de las materias que les son propias, de todas aquellas que no estén atribuidas a otro orden jurisdiccional (art. 9.2 LOPJ).

ÁMBITO DE LA JURISDICCIÓN.- La extensión y límites de la jurisdicción de los Tribunales civiles españoles se determinará por lo dispuesto en la Ley Orgánica del Poder Judicial y en los tratados y convenios internacionales en los que España sea parte (art. 36 LEC), no existiendo en el presente asunto elemento ninguno de extranjería.

B) COMPETENCIA

PREDETERMINACIÓN LEGAL DE LA COMPETENCIA.- Para que los Tribunales civiles tengan competencia en cada caso se requiere que el conocimiento del pleito les esté atribuido por normas con rango de ley y anteriores a la incoación de las actuaciones de que se trate (art. 44 LEC).

COMPETENCIA OBJETIVA.- Corresponde a los Tribunales de Instancia, puesto que no viene atribuída por Ley esta causa civil a otros Tribunales (art. 85.1º LOPJ y 45 LEC).

COMPETENCIA TERRITORIAL.- No siendo aplicable en este caso ninguna regla imperativa de atribución de la competencia territorial, y tampoco mediando pacto de sumisión expresa por escrito, se está al fuero legal subsidiario de las personas físicas (art. 50.1 LEC), por lo que se presenta la demanda ante los Tribunales del partido donde tiene el domicilio la demandada.

II.- PROCEDIMIENTO.

Conforme al número 1.º del art. 249.1 LEC el procedimiento ajustado a derecho será el del juicio declarativo ordinario regulado en los arts. 399 a 436 de la misma Ley.

III.- CAPACIDAD Y REPRESENTACIÓN.

Mi mandante es mayor de edad, en pleno disfrute de sus derechos civiles, por lo que detenta capacidad para ser parte por sí, y capacidad procesal, o para comparecer en juicio, siendo también mayores de edad las codemandas, respecto de las que se ignora exista limitación alguna de capacidad (arts. 6.1.1º y 7.1 LEC).

IV.- LEGITIMACIÓN.

Corresponde al demandante la legitimación activa, según el art. 10 LEC, por afirmarse titular del derecho sobre el objeto litigioso y de la acción que tiene para reclamar la tutela judicial, la legitimación pasiva a las codemandadas porque se afirma que son las dos partes en el negocio transmisivo del objeto litigioso y detentadora unas de ellas de éste, que es la merced del Vizcondado, y en definitiva se pide pronunciamiento que les atañe e interesa.

El Ministerio Fiscal, conforme a la Circular 1/2001, de 5 de abril, sobre la incidencia de la nueva Ley de Enjuiciamiento Civil en la intervención del Fiscal en los procesos civiles, no está legitimado para intervenir en los procedimientos que se susciten en relación con los títulos nobiliarios.

V.- POSTULACIÓN Y DEFENSA.

Conforme a lo previsto en los arts. 23 y 31 LEC, se presenta la demanda por medio de Procurador de los Tribunales con poder general para pleitos, legalmente habilitado ante el Tribunal, y bajo dirección de Letrado en ejercicio colegiado, cuyo nombre y apellido se consignan y que firma la misma.

VI.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VII.- FONDO DE LA CUESTIÓN CONTROVERTIDA

A) PRETENSIONES

1.º) En primer lugar, se solicita se deje sin efecto el negocio jurídico distributivo en virtud del cual D.ª [NOMBRE Y APELLIDOS] adjudicó el título de [NOMBRE DEL TÍTULO NOBILIARIO] a favor de su hija, del mismo nombre D.ª [NOMBRE Y APELLIDOS], por cesión de los derechos derivados de su hermana, nulidad que se insta con carácter previo, por ostentar el demandante mejor derecho a dicho título que el que ostentaba el distribuyente; nulidad que afectará a todos los favorecidos por dicha distribución y que aquí se demandan.

2º) La segunda acción que se ejercita es la declarativa del mejor derecho genealógico para usar, disfrutar y poseer con todos los honores, prerrogativas y preeminencias el título de [NOMBRE DEL TÍTULO NOBILIARIO], y en su caso, la acción de nulidad o ineficacia jurídica de los actos realizados por los demandados o sus causantes en perjuicio del derecho de mi poderdante.

B) PRESCRIPCIÓN

No es de aplicación la única prescripción admitida en Derecho nobiliario, la adquisitiva, mediante la cual, la línea o rama que durante cuarenta o más años la detenta y ostenta de forma pública, pacífica e ininterrumpida será mantenida frente a todos, inclusive con mejor derecho. Al no haber transcurrido el citado plazo de cuarenta años, por interrupción civil en virtud de la demanda interpuesta por el actor, no procede el instituto de la prescripción nobiliaria al supuesto que nos ocupa.

La prescripción adquisitiva admitida en Derecho nobiliario, tiene su origen en las Leyes de Toro de las que precisamente dimanan los preceptos de inscripción recogidos en el CCiv, arts. 1.930 y ss., y se fundamenta en una presunción de abandono por parte del que ostentaría un mejor derecho, unida a la seguridad del derecho.

La prescripción adquisitiva requiere, según el art. 1.941, una posesión en concepto de dueño y de forma pública, pacífica y no interrumpida. El concepto de dueño se sustituye por el de titular de la dignidad, puesto que salvo el primer concesionario los demás son meros tenedores.

No ha transcurrido el plazo de usucapión, ya que D.ª [NOMBRE Y APELLIDOS] obtuvo la rehabilitación del título litigioso en fecha de [FECHA] tal que aún no han transcurrido cuarenta años.

C) PREEMINENCIA NOBILIARIA DE LA MASCULINIDAD.

La legislación vigente sobre títulos nobiliarios fue restablecida por Ley de 4 de mayo de 1.948, de concesión y rehabilitación de Títulos Nobiliarios (artículo uno), en relación al Decreto de 4 de junio de 1.948, concesión y rehabilitación de títulos y grandezas, cuyo artículo 5.º proclama que el orden a suceder en todas las dignidades nobiliarias se acomodará estrictamente a lo dispuesto en el título y sólo en el caso de no previsión se mantendrá el que tradicionalmente se ha seguido en esta materia, es decir, con arreglo a los tres factores que condicionan el mejor derecho, primogenitura, masculinidad y representación.

Es principio fundamental de nuestro Derecho nobiliario, según tiene reconocido el TS en reiterada jurisprudencia, que deberá cumplirse estrictamente la voluntad del fundador, y en su defecto, como es caso, cuando se hayan señalado especialidades en la Carta Concesional, el orden sucesorio se discernirá por el tradicional en la materia.

El orden tradicional para suceder de las dignidades nobiliarias, hasta fecha reciente, no era otro que el establecido para la sucesión a la Corona del Reino de España, hoy en día regulado por el art. 57 de la Constitución Española de 1978.

Resolviendo cuestión de constitucionalidad, la STCo 126/1997, de 3 de julio, declaró que "admitida la constitucionalidad de los títulos nobiliarios por su naturaleza meramente honorífica y la finalidad de mantener vivo el recuerdo histórico al que se debe su otorgamiento, no cabe entender que un determinado elemento de dicha institución —el régimen de su transmisión ‘mortis causa’— haya de apartarse de las determinaciones establecidas en la Real carta de concesión. La voluntad regia que ésta expresa no puede alterarse sin desvirtuar el origen y la naturaleza histórica de la institución pues como ya dijimos en la mencionada STCo 27/1982, resultaría la insalvable contradicción de ser la nobleza causa discriminatoria y por ende inconstitucional a la hora de valorar la condición para adquirir el título, pero no a la hora de valorar la existencia misma y la constitucionalidad del título en cuestión", y añade que "la legislación histórica aplicable a la sucesión regular en los títulos nobiliarios y, en particular, la Partida Segunda, Ley II del Título XV, de la que deriva la regla o criterio de la preferencia del varón sobre la mujer en igualdad de línea y grado, aplicable en virtud de lo dispuesto en los artículos 13 de la Ley de 11 de octubre de 1820, de desvinculación de Títulos y Grandezas y 1 de la Ley de 4 de mayo de 1948, de concesión y rehabilitación de Títulos Nobiliarios, no es contraria al artículo 14 de la Constitución Española".

Esta doctrina del Tribunal Constitucional obligó a la jurisprudencia de la Sala Primera a variar su más moderna línea, anterior a la citada sentencia de 1997 y acoger meramente el principio de la preferencia nobiliaria del varón frente a la mujer —SSTS de fecha 11, 12 y 13 de diciembre de 1997, recs. 4036/1992, 1041/1993 y 2538/1996—.

Posteriormente, el principio de derecho histórico y tradicional de preferencia nobiliaria del varón frente a la mujer desaparece con la Ley 33/2006, de 30 de octubre, que consagra plenamente la igualdad del hombre y la mujer en el orden de sucesión de los títulos nobiliarios, ponderando la STS de 3 de abril de 2008, Rec. 4913/2000, los grados de retroactividad relativa que son admisibles como modulación al principio general de irretroactividad de las normas, compatibilizando tal principio con el reconocimiento de ciertos efectos que la Ley nueva puede desplegar en torno a situaciones jurídicas creadas en el pasado.

D) REPRESENTACIÓN EN EL ORDEN SUCESORIO DE COLATERALES.

Con independencia de lo anterior, y aunque aún antes de la promulgación de la citada norma pudiera mantenerse la abrogación por anticonstitucionalidad sobrevenida, hay que aducir que ello no operaba con retroactividad de grado máximo para alterar, a la luz de normas entonces vigentes, problemas sucesorios acaecidos y agotados en el tiempo pasado [SSTS de 22 de marzo de 1991, 24 de enero de 1995, Rec. 3130/1991 y 18 de abril de 1995, Rec. 53/1992); y después de suprimida por voluntad del legislador la regla de masculinidad, aunque se asuma que se trata de una retroactividad media relativa a hechos anteriores con efectos aún no consumados ni producidos, pues la rehabilitación del título lo es "sin perjuicio de tercero" (SAP Barcelona de 8 de mayo de 2007, Rec. 917/2006), no debe en todo caso confundirse masculinidad con primogenitura.

Debe destacarse que, de conformidad con lo esclarecido por la reiterada jurisprudencia del Tribunal Supremo, en los títulos nobiliarios se sucede con arreglo a los tradicionales principios de primogenitura y representación, conjugados con las siguientes normas preferenciales:

En primer lugar, tendrá preferencia el grupo parental formado por los descendientes del primer titular de la dignidad, este grupo prefiere y excluye al de los ascendientes y éste a su vez, al de los colaterales; en segundo lugar, la línea anterior prefiere y excluye a las posteriores; en tercer lugar, el más próximo en grado prefiere y excluye al más remoto; en cuarto lugar, en igualdad de línea y grado, el de más edad, prefiere y excluye al menor.

De conformidad con la Ley 40 de Toro ni la proximidad de grado ni la mayor edad, con relación al primer titular de la dignidad, operan más que cuando se trata de parientes consanguíneos de una misma línea, ya que, si pertenecían a líneas distintas, la anterior prefiere y excluye a cada una de las posteriores

La polémica sobre el mejor derecho a una dignidad nobiliaria, en los últimos tiempos, se viene debatiendo en torno a si debe determinar la preferencia con relación al último poseedor de la dignidad, D.ª [NOMBRE Y APELLIDOS], o por el contrario la preferencia debe determinarse en relación con el primer [NOMBRE DEL TÍTULO NOBILIARIO], D.

Pues bien, como señala el Dictamen del Consejo de Estado n.º 43.358, de 30 de Julio de 1981, las leyes y los principios a tener en cuenta en la materia son y deben ser siempre los mismos, en vía administrativa o en vía judicial. El principio de posesión civilísima en Derecho nobiliario, y los rectos principios que regulan esta materia tienen su base en que la concesión inicial es guía y norte para resolver los casos de sucesión, por lo que toda sucesión honorífica se acompaña la cláusula de sin perjuicio de tercero de mejor derecho, y en definitiva, en defecto de normas específicas de sucesión en la Carta Concesional se aplica el orden tradicionalmente seguido en la materia, que en el caso presente atañería al principio de propincuidad, en cuanto se refiere al más próximo pariente en razón a la proximidad de grado y recogido en las Partidas (Segunda, Ley II del Título XV precitada), pues se dice: "Pero si todos falleciesen debe heredar el Reino el más propincuo pariente que oviesse".

Este orden implica indubitadamente que la sucesión se refiere al primer concesionario, a la cabeza de la estirpe, a los efectos de la sucesión y que el grado debe respetarse, dentro siempre de esa línea como elemento determinante.

Si se parte del cómputo con respecto al [NOMBRE Y APELLIDOS], como primer poseedor legal, y a efectos de la relación parental y preferencia genealógica, ha de tenerse inevitablemente en cuenta que, aunque el título se refiere a sucesores y herederos, y no exclusivamente a los hijos varones, en modo alguno excluyó la primogenitura de D. [NOMBRE Y APELLIDOS], abuelo paterno de mi mandante, en cuanto le otorga preferencia (STS de 13 de febrero de 1996, Rec. 1763/1992), conformando cabeza de línea en la que se integra éste, respecto a D.ª [NOMBRE Y APELLIDOS], como cabeza de línea de las codemandada

De esta manera la rehabilitante, prescidiendo de su sexo, no resultó más propincua que el cabeza de la línea del actor, y lo mismo las demandadas, madre e hija, por razón de la proximidad de parentesco de la cabeza de línea de primogenitura en la que ha de reputarse estuvo la merced, pues la de la demandada corresponde a la segunda genitura, conforme al árbol genealógico aportado al expediente de rehabilitación en fecha

VIII.- COSTAS.

Conforme al artículo 394 LEC las costas han de imponerse a las demandadas, por principio de vencimiento.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que, habiendo por presentado este escrito de demanda con los documentos que lo acompañan y copias de uno y otros, los admita y me tenga por comparecido en parte en la representación que ostento, y por promovido juicio declarativo ordinario, se sirva darle el curso señalado en la ley y, en su día, venga a dictar sentencia en la que, estimando íntegramente la demanda, previa declaración de nulidad del negocio jurídico distributivo en virtud del cual D.ªadjudicó el título dea favor de su hija D.ª, y de todos los actos realizados por ésta o su causante en perjuicio del derecho del demandante D., se declare el mejor derecho genealógico de éste para llevar, usar, y poseer con todos los honores, prerrogativas y preeminencias el título de [NOMBRE DEL TÍTULO NOBILIARIO], condenando a las codemandadas a estar y pasar por ello y a respetar la declaración de ineficacia proclamada, todo ello con imposición de las costas del juicio a la parte demandada, si se opusiera a la demanda.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a
