---
name: demanda-juicio-ordinario-acumula-reclamacion-cantidad-civ-1021
description: "Demanda de juicio ordinario que acumula reclamación de cantidad y de daños y perjuicios. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio ordinario que acumula reclamación de cantidad y de daños y perjuicios

> Formulario **CIV-1021** del plugin **Proceso civil: demandas, contestaciones, prueba y vista** (`formularios-proceso-civil`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio declarativo ordinario ejercitando las acciones acumuladas de reclamación de cantidad y de daños y perjuicios.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio ordinario que acumula reclamación de cantidad y de daños y perjuicios» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio ordinario que acumula reclamación de cantidad y de daños y perjuicios” para mi caso». También puedes invocarla directamente con `/formularios-proceso-civil:demanda-juicio-ordinario-acumula-reclamacion-cantidad-civ-1021`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-proceso-civil:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso civil: demandas, contestaciones, prueba y vista) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (4 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] FECHA (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] TIPO DE ACCIÓN (2 veces)
- [ ] CORREO ELECTRÓNICO
- [ ] DENOMINACIÓN SOCIAL
- [ ] FECHAS
- [ ] FUNDAMENTOS
- [ ] IMPORTE
- [ ] LUGAR
- [ ] NATURALEZA DE LAS PARTES
- [ ] NOMBRE DE LA PARTE
- [ ] Nº
- [ ] Nº DE APARTADO
- [ ] Nº DE COLEGIADO/A
- [ ] Nº DE PROCEDIMIENTO
- [ ] Nº DE REGLA
- [ ] TELÉFONO

## Normas que cita el formulario

- art. 24.1 LEC
- art. 399.1 LEC
- art. 9.2 LOPJ
- art. 85.1 LOPJ
- art. 36 LEC
- art. 44 LEC
- art. 45 LEC
- art. 52 LEC
- art. 249 LEC
- art. 6 LEC
- art. 10 LEC
- art. 253 LEC
- art. 251 LEC
- art. 23 LEC
- art. 399 LEC
- art. 5 Ley Orgánica 1/2025
- art. 394 LEC
- art. 71.2 LEC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE Q.P.T.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE Q.P.T.C.

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales y de la entidad mercantil [DENOMINACIÓN SOCIAL], con domicilio social en [LOCALIDAD], representación que acredito mediante escritura de poder otorgada a mi favor (existen tres posibilidades para otorgar el apoderamiento al Procurador de los Tribunales, conforme dispone el art. 24.1 LEC)

[OPCIONAL — opción en función de cómo se haya otorgado el poder]

[ELEGIR UNA OPCIÓN: Si el poder se otorga a través de la sede judicial electrónica / Si el poder se otorga mediante comparecencia apud acta / Si el poder se otorga ante Notario]

bajo la dirección letrada de D./Dña [NOMBRE Y APELLIDOS], abogado/a en ejercicio, con despacho profesional abierto en [LOCALIDAD], colegiado nº [Nº DE COLEGIADO/A] del Ilustre Colegio de la Abogacía de [LOCALIDAD], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que, siguiendo instrucciones de mi mandante, vengo a interponer demanda DE JUICIO [Nº DE PROCEDIMIENTO], en ejercicio de la acción [TIPO DE ACCIÓN], contra D./Dña [NOMBRE Y APELLIDOS], con domicilio, primero en [DOMICILIO]; y segundo, el domicilio laboral en [DOMICILIO]); con email [CORREO ELECTRÓNICO]; y con número de teléfono móvil [TELÉFONO]; en ejercicio de la acción de [TIPO DE ACCIÓN], según se especificará en el cuerpo del escrito y en el suplico, y todo ello de conformidad con los siguientes hechos y fundamentos de derecho.

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa, e, incluso, en una eventual fase de ejecución por medios telemáticos, en términos del art. 399.1 II LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y nº [Nº] de teléfono: ……

Se ejercitan en la presente demanda las acciones acumuladas de reclamación de cantidad y de daños y perjuicios.

Fundamento la misma en los siguientes hechos y consideraciones jurídicas:

HECHOS

PRIMERO

SEGUNDO.-

TERCERO.-

CUARTO.- Sobre el proceso de negociación previo y medios de solución de controversias de manera amistosa y extrajudicial.

La parte actora manifiesta que, previo a la presentación de la presente demanda, se han llevado a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad, y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria; incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, mi representado envió un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por el demandado por el mismo medio, rechazando el acuerdo/ habiendo sido solo posible un acuerdo parcial, viéndonos en la necesidad de acudir a la presente vía judicial, respecto a los extremos de la controversia en los que se mantiene la discrepancia.

Acompaño como documento nº [Nº DE DOCUMENTO], el requerimiento efectuado y como documento nº [Nº DE DOCUMENTO], la contestación del demandado.

VALORACIÓN FÁCTICA

APORTACIÓN DE PRUEBA

A los efectos de acreditar el fundamento de las pretensiones que se deducen, acompaño:

DOCUMENTO N.º [NÚMERO]

DOCUMENTO N.º [NÚMERO]

DOCUMENTO N.º [NÚMERO]

A los anteriores hechos, son aplicables los siguientes

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA

A) JURISDICCIÓN

POTESTAD JURISDICCIONAL.- La potestad jurisdiccional se ejerce por los Tribunales determinados por las leyes, según las normas de competencia y procedimiento que las mismas establezcan (art. 117.3 CE).

JURISDICCIÓN CIVIL.- Los Tribunales del orden civil conocerán, además de las materias que les son propias, de todas aquellas que no estén atribuidas a otro orden jurisdiccional (art. 9.2 LOPJ).

Las secciones civiles de los Tribunales de Instancia conocerán en el orden civil, en primera instancia, de los juicios que no vengan atribuidos por esta ley a otros Tribunales (art. 85.1º LOPJ).

LÍMITES DE LA JURISDICCIÓN.- La extensión y límites de la jurisdicción de los Tribunales civiles españoles se determinará por lo dispuesto en la LOPJ y en los tratados y convenios internacionales en los que España sea parte (art. 36 LEC).

B) COMPETENCIA

PREDETERMINACIÓN LEGAL DE LA COMPETENCIA.- Para que los Tribunales civiles tengan competencia en cada caso se requiere que el conocimiento del pleito les esté atribuido por normas con rango de ley y anteriores a la incoación de las actuaciones de que se trate (art. 44 LEC).

COMPETENCIA OBJETIVA. TRIBUNALES DE INSTANCIA.- Corresponde a dichos órganos jurisdiccionales, el conocimiento en primera instancia, de todos los asuntos civiles que por disposición legal expresa no se hallen atribuidos a otros Tribunales. Conocerán, asimismo, dichos Tribunales de los asuntos, actos, cuestiones y recursos que les atribuye la LOPJ (art. 45 LEC).

COMPETENCIA TERRITORIAL.-

SI EXISTE REGLA IMPERATIVA DE ATRIBUCIÓN DE COMPETENCIA.- En el supuesto concreto es aplicable la regla [Nº DE REGLA] del art. 52 LEC, que establece normas imperativas de competencia territorial.

SI NO ES DE APLICACIÓN NINGUNA REGLA IMPERATIVA DE ATRIBUCIÓN DE COMPETENCIA Y EXISTE PACTO DE SUMISIÓN.- No siendo aplicable en este caso ninguna regla imperativa de atribución de la competencia territorial, y existiendo pacto de sumisión expresa por escrito, designando los Tribunales de [LOCALIDAD], es por lo que corresponde la competencia territorial a los Tribunales de Instancia de

SI NO EXISTE REGLA IMPERATIVA DE ATRIBUCIÓN DE COMPETENCIA NI PACTO DE SUMISIÓN.- En defecto de reglas imperativas de atribución, o de sumisión tácita o expresa, se estará a los fueros legales subsidiarios, por el siguiente orden:

1.º) Fueros especiales no imperativos de los números 2.º y 3.º del apartado 1 del art. 52 LEC.
2.º) En su defecto, el fuero general de las personas físicas (art. 50).
3.º) Por último, el fuero general de las personas jurídicas y de los entes sin personalidad (art. 51).

II.- PROCEDIMIENTO

Conforme al apartado [Nº DE APARTADO] del art. 249 LEC el procedimiento ajustado a derecho será el del juicio declarativo ordinario regulado en los arts. 399 a 436 de la misma Ley.

III.- CAPACIDAD Y REPRESENTACIÓN

La tienen demandante y demandada por [NATURALEZA DE LAS PARTES] a tenor de lo dispuesto en los arts. 6 y 7 LEC.

IV.- LEGITIMACIÓN

Corresponde al demandante y demandado citados, según el art. 10 LEC, el primero por el derecho y acción que tiene para reclamar, y el segundo como obligado por su intervención en el negocio del que se trae causa y porque el pronunciamiento que en definitiva se pretende le atañe e interesa.

V.- CUANTÍA

Conforme al art. 253 LEC cifro la cuantía de la presente demanda en [IMPORTE], fijación que amparo en el siguiente fundamento (Se expresará justificadamente la cuantía de la demanda, calculada conforme a las reglas legales de los arts. 251 y 252 LEC. Deberán presentarse los documentos o dictámenes que acrediten el valor de la cosa litigiosa. Si no es posible la determinación, aun en forma relativa, la demanda se considerará de cuantía indeterminada) [FUNDAMENTOS]), calculada con arreglo a las reglas número/s del/de los artículo/s 251/y 252 de dicha Ley.

VI.- POSTULACIÓN Y DEFENSA

Conforme a lo previsto en los arts. 23 y 31 LEC, se presenta la demanda por medio de Procurador/a legalmente habilitado y bajo dirección de Letrado firmante de la misma.

VII.- REQUISITOS FORMALES

Se inicia el presente procedimiento por medio de demanda que reúne todos los requisitos exigidos en el art. 399 LEC.

VIII.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

IX.- FONDO DE LA CUESTIÓN CONTROVERTIDA

X.- COSTAS

Conforme al art. 394 LEC, las costas han de imponerse a la demandada.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que habiendo por presentado este escrito de demanda con los documentos que lo acompañan y copias de uno y otros, los admita y me tenga por comparecido en parte en la representación que ostento y que acreditada dejo; y por promovido juicio declarativo ordinario frente [NOMBRE DE LA PARTE], dé al mismo el curso señalado en la ley y, en su día, dicte sentencia en la que, estimando íntegramente la demanda

Todo ello con imposición de las costas del juicio a la parte demandada.

OTROSÍ DIGO que habiendo ejercitado la acción de reclamación de cantidad y la de daños y perjuicios solicito se las tenga por acumuladas en este proceso, por ser compatibles entre sí aunque provienen de distintos títulos, y estar dirigidas contra un mismo deudor y demandado, conforme permite el art. 71.2 LEC.

SUPLICO AL TRIBUNAL que teniendo por realizadas las manifestaciones que anteceden se digne acordar conforme a lo interesado en el cuerpo de las mismas.

Es justicia de hacerse en [LUGAR], a [FECHA].

Firma del Abogado	Firma del Procurador/a
