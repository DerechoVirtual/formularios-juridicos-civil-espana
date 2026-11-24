---
name: demanda-juicio-ordinario-nulidad-acta-notarial-civ-0480
description: "Demanda de juicio ordinario de nulidad del acta notarial de notoriedad de declaración de herederos. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio ordinario de nulidad del acta notarial de notoriedad de declaración de herederos

> Formulario **CIV-0480** del plugin **Herencias, testamentos y donaciones** (`formularios-herencias-y-donaciones`) · Civil › Sucesiones y donaciones · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario instando la nulidad del acta de notoriedad de declaración de herederos, otorgada ante Notario.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio ordinario de nulidad del acta notarial de notoriedad de declaración de herederos» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio ordinario de nulidad del acta notarial de notoriedad de declaración de herederos” para mi caso». También puedes invocarla directamente con `/formularios-herencias-y-donaciones:demanda-juicio-ordinario-nulidad-acta-notarial-civ-0480`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-herencias-y-donaciones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Herencias, testamentos y donaciones) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (20 veces)
- [ ] FECHA (9 veces)
- [ ] LOCALIDAD (9 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] SEDE (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] Nº (2 veces)
- [ ] CORREO ELECTRÓNICO
- [ ] DATOS DEL ACTA DE NOTORIEDAD
- [ ] FECHAS
- [ ] LUGAR
- [ ] Nº DE COLEGIADO/A
- [ ] TELÉFONO

## Normas que cita el formulario

- art. 24.1 LEC
- art. 399.1 LEC
- art. 265.2 LEC
- art. 85.1 LOPJ
- art. 52.1.4.º LEC
- art. 6.1.1.º LEC
- art. 7.1 LEC
- art. 10 LEC
- art. 5.2 LEC
- art. 23.1 LEC
- art. 31.1 LEC
- art. 251 LEC
- art. 5 Ley Orgánica 1/2025
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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.R.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…dictada con fecha [FECHA] por el Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

Que mediante el presente escrito vengo a formular DEMANDA DE JUICIO DECLARATIVO ORDINARIO instando la nulidad del acta de notoriedad otorgada ante el Notario de [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS], debiéndose considerar como demandada a D./Dña [NOMBRE Y APELLIDOS], con domicilio, primero en [DOMICILIO]; y segundo, el domicilio laboral en [DOMICILIO]); con email [CORREO ELECTRÓNICO]; y con número de teléfono móvil [TELÉFONO]; todo ello de conformidad con los hechos y fundamentos de derecho que se especificarán.

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa, e, incluso, en una eventual fase de ejecución por medios telemáticos, en términos del art. 399.1 II LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y nº [Nº] de teléfono:

HECHOS

PRIMERO

Mi representada es hija no matrimonial de D./Dña. [NOMBRE Y APELLIDOS], filiación declarada en sentencia firma dictada con fecha [FECHA] por el Tribunal de Instancia de [SEDE], plaza n.º [Nº] [DATOS DEL ACTA DE NOTORIEDAD], cuyo testimonio se acompaña como documento n.º [Nº DE DOCUMENTO]

SEGUNDO

D./Dña. [NOMBRE Y APELLIDOS], falleció intestado el pasado día [FECHA] en la localidad de [LOCALIDAD] Se aporta certificación de la inscripción de defunción del causante, así como la certificación del Registro de Actos de Ultima Voluntad del mismo, en la que consta que no otorgó testamento (documentos números [Nº DE DOCUMENTO]).

TERCERO

Mi mandante es sucesora por ministerio de la ley, junto a la demandada, del finado D./Dña. [NOMBRE Y APELLIDOS].

CUARTO

Esta parte ha tenido conocimiento del acta de notoriedad sobre declaración de herederos otorgada por la demandada ante el Notario de [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS] en fecha [FECHA], excluyendo de tal condición a la actora.

Acompaño como documento n.º [NÚMERO], reproducción de copia del acta notarial, y no teniendo a mi disposición el documento original, de conformidad con el art. 265.2 LEC designo el protocolo general corriente del Notario de [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS]

QUINTO

La parte actora manifiesta que, previo a la presentación de la presente demanda, se han llevado a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad, y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria; incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, con fecha [FECHA] se ha efectuado por la parte actora requerimiento extrajudicial tendente a solicitar de la demandada el otorgamiento de escritura pública notarial complementaria de la otorgada el día [FECHA], en la que se haga constar su condición de heredera universal junto con Doña [NOMBRE Y APELLIDOS] (documento número [Nº DE DOCUMENTO]). Dicho requerimiento no ha sido atendido por la demandada lo que fuerza la interpelación judicial.

A estos hechos le son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

JURÍDICO PROCESALES

I.- COMPETENCIA

Radicando la competencia genérica en el orden civil de la jurisdicción, detenta la competencia objetiva y funcional la Sección Civil del Tribunal de Instancia, por aplicación de lo dispuesto en los arts. 85.1 LOPJ y 45 LEC, y territorialmente es competente el Tribunal a que me dirijo, puesto que está prevenido el fuero territorial preceptivo específico para los juicios sobre cuestiones hereditarias, con arreglo a lo previsto en el art. 52.1.4.º LEC, del lugar del último domicilio del finado, siendo de este partido la población en que se hallaba la residencia donde murió D./Dña. [NOMBRE Y APELLIDOS]

II.- PARTES

CAPACIDAD. Tanto la actora, mi patrocinada, como la demandada son personas físicas mayores de edad, respecto de las que no consta limitación de ejercicio de derechos civiles, por lo que detentan capacidad para ser parte (art. 6.1.1.º LEC), y capacidad procesal, o de obrar en este concreto juicio (art. 7.1 LEC).

LEGITIMACIÓN. Le corresponde la legitimación activa ordinaria directa (art. 10 LEC) a mi representada por su condición de heredera forzosa omitida en la declaración de herederos de D./Dña. [NOMBRE Y APELLIDOS], y ostenta la demandada la legitimación pasiva correlativa, por ser la única designada en la citada declaración que se viene a impugnar, a quien afecta la pretensión de declaración que se formula (art. 5.2 LEC).

POSTULACIÓN. Esta parte, como será debido para la personación que convenga a la contraria, comparece por medio de Procurador/a de los Tribunales habilitado ante el tribunal (art. 23.1 LEC), y bajo la dirección del Letrado en ejercicio (art. 31.1 LEC).

III.- PROCEDIMIENTO

La presente demanda deberá sustanciarse por las normas del juicio ordinario, a tenor de lo prevenido en los arts. 248, 249.2 y 253.3 LEC, toda vez que ningún criterio de atribución preferente de la materia objeto del proceso resulta aplicable, puesto que la regla 12.ª del art. 251 LEC, referida a pleitos relativos a una herencia, se corresponde con condenas afectantes a los bienes o masas patrimoniales, y no a la mera declaración de nulidad del acta de notoriedad notarial, y de la condición de heredera abintestato de la actora que constriñe los derechos hereditarios de la demandada.

IV.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

JURÍDICO SUSTANTIVOS

Se ejercita en la presente demanda acción personal declarativa de nulidad del acta de notoriedad sobre declaración de herederos abintestato otorgada por la demandada ante el Notario de [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS] en fecha [FECHA], y ello como consecuencia de que en la misma se declara como única heredera del fallecido a la demandada cuando, en realidad, también la actora tiene esa misma condición de heredera como hija suya siendo omitida en esa declaración.

Por tanto, resultando determinada la filiación no matrimonial de la actora en virtud de sentencia firme dictada con fecha [FECHA] por el Tribunal de Instancia de [SEDE], plaza n.º [NÚMERO] (cfr.: art. 113CCiv), su condición de heredera abintestato de su padre fallecido, junto con el resto de los hijos de éste, le proviene de las disposiciones del Código Civil al respecto (arts. 930 y ss.), y el acta de notoriedad en la que se considera acreditada la condición de heredero abintestato en la herencia de su padre sólo para la demandada pero omitiendo como heredera a la actora, hija no matrimonial del Sr./a. es nula por ser contraria a derecho.

Por otro lado, es doctrina jurisprudencial reiterada que la declaración de herederos no solo puede hacerse por auto dictado en expediente de jurisdicción voluntaria (que no produce efecto de cosa juzgada) o acta de notoriedad notarial (cfr.: art. 209 bis RN), sino también en juicio declarativo ordinario. Esta posibilidad se ha contemplado en la jurisprudencia (así, por ejemplo, en la STS de 9 de diciembre de 1992, rec. 1/1990, que se remonta a otra del mismo Tribunal de 30 de octubre de 1917), cuando la declaración sea necesario para resolver las cuestiones planteadas en el pleito, pero igualmente debe reconocerse cuando existe un interés legitimador del actor en el mismo sentido, como ocurre en este caso, pues se omitió a la actora de su condición de heredera en el acta de notoriedad a la que ya se ha hecho referencia.

De modo que es también de aplicación pertinente la jurisprudencia permisiva de que la declaración de herederos abintestato se obtenga a través de un juicio declarativo ordinario, siempre que los extremos sobre los que recae tal declaración tengan en él la correspondiente justificación, sin que la nulidad del acta que deriva de la omisión de la actora como heredera del fallecido, subsanable con la declaración que se solicita en la presente demanda, en el sentido que la demandante como hija del fallecido Sr./a. [NOMBRE Y APELLIDOS], es heredera abintestato del mismo y con los derechos que le corresponden en esa condición de acuerdo con las disposiciones del Código Civil al efecto, en concurrencia con los demás herederos, afecte a la condición de herederos del resto de las personas que allí se declaran como tales.

COSTAS

Serán de cuenta del demandado por lo dispuesto en el art. 394.1 LEC, respecto del principio de vencimiento cuasiobjetivo para declarativos en primera instancia.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que teniendo por presentado este escrito, con los documentos y las copias que se acompañan, se sirva admitirlo, tener por comparecido y parte al Procurador/a de los Tribunales D./Dña. [NOMBRE Y APELLIDOS] en la representación que ostento, entendiéndose conmigo las sucesivas diligencias, y por interpuesta demanda de juicio ordinario frente a Don/Doña [NOMBRE Y APELLIDOS], y seguido que sea el procedimiento por sus trámites, se venga a dictar sentencia por la que declare:

1) Que la actora en tanto que hija del difunto D./Dña. [NOMBRE Y APELLIDOS], tiene derecho a sucederle como heredera forzosa del mismo.
2) Que la demandada ha otorgado acta de notoriedad de herederos abintestato excluyendo de tal condición a la actora.
3) Que como consecuencia de las anteriores declaraciones el acta de notoriedad de herederos abintestato otorgada por Don/Doña [NOMBRE Y APELLIDOS], por ante el Notario de [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS], el día [FECHA] al número [NÚMERO] de protocolo es nula de pleno derecho por ser contraria a derecho.
4) La imposición de las costas del juicio a la parte demandada.

Es justicia de hacerse en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a
