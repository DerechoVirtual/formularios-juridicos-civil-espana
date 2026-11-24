---
name: demanda-desahucio-arrendamiento-rustico-anterior-2004-civ-0601
description: "Demanda de desahucio de arrendamiento rústico anterior a 2004 por fin del plazo y prórrogas legales. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de desahucio de arrendamiento rústico anterior a 2004 por fin del plazo y prórrogas legales

> Formulario **CIV-0601** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio verbal de desahucio sobre declaración de extinción de contrato de arrendamiento de finca rústica por expiración del plazo del arrendamiento junto a sus prórrogas legales. Arrendamiento sujeto a la LAR 83/1980.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de desahucio de arrendamiento rústico anterior a 2004 por fin del plazo y prórrogas legales» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de desahucio de arrendamiento rústico anterior a 2004 por fin del plazo y prórrogas legales” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:demanda-desahucio-arrendamiento-rustico-anterior-2004-civ-0601`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] LOCALIDAD (7 veces)
- [ ] FECHA (6 veces)
- [ ] Nº DE DOCUMENTO (4 veces)
- [ ] Nº DE PARCELA (4 veces)
- [ ] NÚMERO (4 veces)
- [ ] IMPORTE (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] ACCIÓN EJERCITADA
- [ ] CORREO ELECTRÓNICO
- [ ] FECHAS
- [ ] FOLIO
- [ ] IMPORTE EN CIFRA
- [ ] LIBRO
- [ ] LUGAR
- [ ] NOMBRE O DENOMINACIÓN
- [ ] Nº
- [ ] Nº DE COLEGIADO/A
- [ ] Nº DE POLÍGONO
- [ ] SEDE
- [ ] SUPERFICIE
- [ ] TELÉFONO
- [ ] TOMO

## Normas que cita el formulario

- art. 24.1 LEC
- art. 437.1 LEC
- art. 85 LOPJ
- art. 45 LEC
- art. 52.1.7.º LEC
- art. 248.3 LEC
- art. 250.1.1.º LEC
- art. 6.1.1.º LEC
- art. 7.1 LEC
- art. 10 LEC
- art. 251 LEC
- art. 23.1 LEC
- art. 31.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 1577 CC
- art. 1.566 CC
- art. 394.1 LEC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.R.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.R.C.

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], representación que acredito mediante escritura de poder otorgada a mi favor (existen tres posibilidades para otorgar el apoderamiento al Procurador de los Tribunales, conforme dispone el art. 24.1 LEC)

[OPCIONAL — opción en función de cómo se haya otorgado el poder]

[ELEGIR UNA OPCIÓN: Si el poder se otorga a través de la sede judicial electrónica / Si el poder se otorga mediante comparecencia apud acta / Si el poder se otorga ante Notario]

bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS], abogado/a en ejercicio, con despacho profesional abierto en [LOCALIDAD], colegiado nº [Nº DE COLEGIADO/A] del Ilustre Colegio de la Abogacía de [LOCALIDAD], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que mediante el presente escrito vengo a formular DEMANDA DE JUICIO VERBAL, contra D./Dña. [NOMBRE Y APELLIDOS], con domicilio, primero en [DOMICILIO]; y segundo, el domicilio laboral en [DOMICILIO]); con email [CORREO ELECTRÓNICO]; y con número de teléfono móvil [TELÉFONO]; en ejercicio de la acción de [ACCIÓN EJERCITADA], según se especificará en el cuerpo del escrito y en el suplico.

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa, e, incluso, en una eventual fase de ejecución por medios telemáticos, en términos del art. 399.1 II con relación al art. 437.1, ambos LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y nº [Nº] de teléfono:

Todo ello de conformidad con los siguientes hechos y fundamentos de derecho:

HECHOS

PRIMERO.- D./Dña. [NOMBRE Y APELLIDOS] es propietario de la finca inscrita al folio [FOLIO], tomo [TOMO], del libro [LIBRO] del Registro de la Propiedad de [LOCALIDAD], que se corresponde con las parcelas [Nº DE PARCELA], [Nº DE PARCELA] y [Nº DE PARCELA], y [Nº DE PARCELA] del Polígono [Nº DE POLÍGONO] del Catastro de rústica del Ayuntamiento de

Se acompañan para la identidad de la casa y predios, certificados del Registro de la Propiedad, y de la Oficina Catastral de [LOCALIDAD], como documentos números [Nº DE DOCUMENTO] y [Nº DE DOCUMENTO].

SEGUNDO.- Entre el demandante D./Dña. [NOMBRE Y APELLIDOS] y el demandado, el primero en concepto de arrendador y el segundo en concepto de arrendatario, se concertó con fecha [FECHA] un contrato de arrendamiento en virtud del cual el demandante cedía al demandado la posesión útil de la finca descrita, sita en este término municipal y conocida como ‘[NOMBRE O DENOMINACIÓN]’, de una extensión aproximada de [SUPERFICIE] Hectáreas, por un plazo de duración de seis años y por una renta anual de [IMPORTE], la cual se fue revalorizando posteriormente hasta la suma de [IMPORTE] anuales que es la última satisfecha por el arrendatario.

Se acompaña como documento n.º [NÚMERO], original del contrato de arrendamiento.

TERCERO.- No obstante haberse pactado la duración del contrato durante seis años, debido al juego de las prórrogas de la legislación arrendaticia, así como al tácito acuerdo de los litigantes, el citado contrato ha venido prorrogándose tácitamente hasta la actualidad.

CUARTO.- Con fecha [FECHA], al cumplirse los veintiún años de duración del contrato, se notificó fehacientemente al arrendatario la voluntad del arrendador de darlo por finalizado (documento n.º [NÚMERO]).

QUINTO.- Pese a haber transcurrido los plazos, convencional y de prórroga, de la vigencia de la relación contractual, y no obstante los continuos esfuerzos desplegados extrajudicialmente por el compareciente para resolver el problema planteado por el incumplimiento del arrendatario de su obligación de dejar a disposición del actor la finca que a éste pertenece, y que se han llevado a cabo mediante múltiples comunicaciones verbales, ello no ha sido posible, por lo que el demandado D./Dña. [NOMBRE Y APELLIDOS] fue requerido notarialmente para que dando por extinguido el contrato restituyera la posesión de la finca a la finalización del año agrícola en curso.

Se adjunta la copia auténtica del acta de requerimiento notarial practicado a D./Dña. [NOMBRE Y APELLIDOS], el día [FECHA], por el Notario de [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS], con nº [NÚMERO] de su protocolo general corriente (documento n.º [NÚMERO])

El dicho requerimiento notarial no ha sido contestado por el demandado, no dejando más alternativa a esta parte que la vía judicial.

SEXTO.- La parte actora manifiesta que, previo a la presentación de la presente demanda, se han llevado a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad, y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria; incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, mi representado envío un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por el demandado por el mismo medio, rechazando el acuerdo/ habiendo sido solo posible un acuerdo parcial, viéndonos en la necesidad de acudir a la presente vía judicial, respecto a los extremos de la controversia en los que se mantiene la discrepancia.

Acompaño como documento nº [Nº DE DOCUMENTO], el requerimiento efectuado y como documento nº [Nº DE DOCUMENTO], la contestación del demandado.

A los anteriores hechos son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA.

Sin duda de la competencia genérica del orden civil de la jurisdicción, la competencia específica atribuye el conocimiento de este asunto al Tribunal a quien tengo el honor de dirigirme por ser el de Instancia (art. 85 LOPJ y art. 45 LEC), que detenta competencia objetiva, y la funcional de la instancia, y que ostenta competencia territorial, por cuanto en los juicios sobre arrendamiento de inmuebles es competente el tribunal del lugar en que esté sita la finca, según el art. 52.1.7.º LEC.

II.- PROCEDIMIENTO.

El procedimiento a través del cual se ha de sustanciar la pretensión es el correspondiente al JUICIO VERBAL, conforme al art. 248.3 LEC, que indica aplicable el criterio prioritario de la materia, estando la pretensión recuperatoria de la posesión de la finca por resolución debida al advenimiento del término con relación a un contrato de arrendamiento inmobiliario rústico, entre las listadas en el art. 250.1.1.º LEC, por lo que se seguirán los trámites de los arts. 437 y ss. LEC.

III.- CAPACIDAD.

Demandante y demandado, personas físicas, tienen capacidad para ser parte (art. 6.1.1.º LEC), titular de facultades y cargas del proceso, y asimismo plena capacidad procesal, al ser mayores de edad, sin limitación de ejercicio válido de derechos civiles, o para comparecer en juicio, en términos del art. 7.1 LEC, pretendiendo el actor y siendo pretendido el demandado, en sus respectivos nombres y derechos.

IV.- LEGITIMACIÓN.

Está legitimado el actor para promover este juicio, por estar directa y activamente interesado en la pretensión jurídica deducida, como titular del derecho a dar por extinguido el contrato obteniendo la recuperación de la posesión inmediata, y haber en su día concertado y convenido como arrendador con el demandado el contrato pactado, así como por ser titular del bien cuyo recuperación se interesa y de acuerdo con lo establecido en los arts. 83.1.b) LAR 83/1980; arts. 1.546 y 1.569 CCiv.; y art. 10 LEC.

Y está legitimada la parte demandada, como arrendatario poseedor, por dirigirse contra ella el presente proceso y estar directa y pasivamente interesada en la resolución que se dicte en esta litis, al haber firmado, como arrendatario, el contrato cuya declaración de extinción se pretende en este juicio, así como por hallarse en la situación a que se refieren los arts. 83.1.b) LAR 83/1980 y art. 10 LEC.

V.- CUANTÍA.

Se hace constar que la cuantía de la demanda es de [IMPORTE] euros ([IMPORTE EN CIFRA] €), que se corresponde con la anualidad de renta pactada en el contrato, conforme a la regla 9.ª del art. 251 LEC.

VI.- POSTULACIÓN Y DEFENSA.

Esta parte, como será debido para la personación que convenga a la contraria, comparece por medio de Procurador de los Tribunales habilitado ante el tribunal (art. 23.1 LEC), y bajo la dirección del Letrado en ejercicio (art. 31.1 LEC).

VII.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VIII.- JURÍDICO-SUSTANTIVOS.

Se promueve acción de resolución de contrato de arrendamiento rústico sujeto a la Ley 83/1980 de 31 de diciembre, derogada por la vigente Ley 49/2003, pero que resulta aplicable al contrato vigente, puesto que era la del momento de su celebración (DT 1.ª LAR 49/2003), con base en la expiración del periodo de duración y sus prórrogas, según el art. 83.1.b) en relación con el art. 25 LAR 83/1980.

Establece el art. 25.3 LAR 83/1980 que, en todo caso, el tiempo total de prórrogas legales no excederá de quince años, transcurridos los cuales se extinguirá el contrato y el arrendador podrá arrendar nuevamente la finca a quien tuviera por conveniente en los términos señalados en el art. 14 LAR 83/1980.

Ello, con independencia de que, si al terminar el contrato, permanece el arrendatario disfrutando durante quince días de la cosa arrendada con aquiescencia del arrendador, existe tácita reconducción por el tiempo establecido en el art. 1577 CCiv por tratarse de un predio rústico (art. 1.566 CCiv).

La doctrina jurisprudencial de la Sala I TS ha negado la tácita reconducción, precisamente cuando ha existido requerimiento —sentencias de 2 de marzo de 1.993, rec. 2415/1990 y 22 de noviembre de 1.994—, por lo que es evidente que iniciada la relación arrendaticia en fecha [FECHA] ha expirado el plazo máximo de duración señalado en el art. 25 LAR 83/1980, que se fija en veintiún años.

IX.- COSTAS.

Serán de cuenta del demandado, como previene el art. 394.1 LEC, consagrando el principio de vencimiento cuasiobjetivo para declarativos en primera instancia.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que teniendo por presentado este escrito de demanda junto con los documentos que se acompañan y copias simples de todo ello, se sirva admitirlo a trámite, me tenga por comparecido y parte demandante en la representación que acredito, y por formulada demanda de desahucio por expiración del término del contrato de arrendamiento, acuerde dar traslado al demandado para que comparezca y la conteste, y seguido el juicio por sus trámites, se dicte sentencia por la que estimando íntegramente la demanda, se declare extinguido el contrato de arrendamiento de la finca descrita, condenando al demandado a estar y pasar por dicha resolución, y a que desaloje, deje libre y a disposición de la actora la finca denominada, en el término municipal de [LOCALIDAD], bajo apercibimiento de lanzamiento si no lo verifica en el plazo legal, condenando asimismo a la demandada al pago de las costas procesales causadas.

OTROSÍ DIGO que por necesitar para otros usos la copia de escritura de poder acreditativa de la representación del suscrito Procurador, intereso y

SUPLICO AL TRIBUNAL se sirva acordar su desglose y devolución a esta parte, dejando en autos testimonio de la misma.

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a
