---
name: demanda-modificacion-convenio-regulador-pedida-ambos-civ-0349
description: "Demanda de modificación del convenio regulador pedida por ambos cónyuges o uno con el otro. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de modificación del convenio regulador pedida por ambos cónyuges o uno con el otro

> Formulario **CIV-0349** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda de modificación del convenio regulador aprobado en una sentencia de separación o divorcio, formulada por ambos cónyuges de común acuerdo o por uno con el consentimiento del otro, con propuesta de nuevo convenio (art. 777 LEC). El modelo plantea el cambio de la guarda y custodia de un hijo menor por alteración sustancial de las circunstancias (art. 90 CC).

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de modificación del convenio regulador pedida por ambos cónyuges o uno con el otro» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de modificación del convenio regulador pedida por ambos cónyuges o uno con el otro” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-modificacion-convenio-regulador-pedida-ambos-civ-0349`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (12 veces)
- [ ] LOCALIDAD (8 veces)
- [ ] NOMBRE (7 veces)
- [ ] FECHA (6 veces)
- [ ] Nº DE DOCUMENTO (5 veces)
- [ ] EDAD (3 veces)
- [ ] PÁGINA (3 veces)
- [ ] TOMO (3 veces)
- [ ] AÑO (2 veces)
- [ ] DÍA (2 veces)
- [ ] MES (2 veces)
- [ ] NOMBRE DEL HIJO/A (2 veces)
- [ ] Nº DE DOCUMENTOS (2 veces)
- [ ] SEDE (2 veces)
- [ ] SEPARACIÓN/DIVORCIO (2 veces)
- [ ] AJUSTAR A LO PACTADO EN EL CONVENIO ORIGINAL.
- [ ] CLASE DE PROCEDIMIENTO
- [ ] COLEGIO
- [ ] CORREO ELECTRÓNICO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DOMICILIO
- [ ] NOMBRE DEL NOTARIO
- [ ] NOMBRE Y APELLIDOS DEL LETRADO/A
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº
- [ ] Nº DE COLEGIADO
- [ ] Nº DE PROCEDIMIENTO
- [ ] Nº DE PROTOCOLO
- [ ] PROFESIÓN Y CONDICIONES DE TRABAJO
- [ ] TELÉFONO
- [ ] TIEMPO

## Normas que cita el formulario

- art. 24.1 LEC
- art. 24.2 LEC
- art. 777 LEC
- art. 399.1 LEC
- art. 769 LEC
- art. 775.1 LEC
- art. 777.5 LEC
- art. 777.9 LEC
- art. 90 CC
- art. 92.2 CC
- art. 94 CC

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

AL TRIBUNAL DE INSTANCIA DE [SEDE]
SECCIÓN CIVIL
SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [DOMICILIO], representación que acredito mediante:

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]
— poder otorgado a mi favor a través de la sede judicial electrónica (inscrito en el Registro Electrónico de Apoderamientos Judiciales), cuya certificación acompaño como documento n.º [Nº DE DOCUMENTO];
— poder otorgado mediante comparecencia apud acta ante el Letrado de la Administración de Justicia, inscrito en el Registro Electrónico de Apoderamientos Judiciales, cuya certificación acompaño como documento n.º [Nº DE DOCUMENTO];
— escritura de poder otorgada a mi favor ante el Notario D./Dña. [NOMBRE DEL NOTARIO], con n.º de protocolo [Nº DE PROTOCOLO], inscrita en el Registro Electrónico de Apoderamientos Judiciales, cuya certificación acompaño como documento n.º [Nº DE DOCUMENTO];

(Existen tres posibilidades para otorgar el apoderamiento al Procurador de los Tribunales, conforme dispone el art. 24.1 LEC. Todos los poderes deben estar inscritos en el Registro Electrónico de Apoderamientos Judiciales para su acreditación; basta, en principio, la consulta automatizada del Registro por el Letrado de la Administración de Justicia, y la certificación de la inscripción es la vía subsidiaria del art. 24.2 LEC, por lo que el modelo acompaña la certificación electrónica.)

bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS DEL LETRADO/A], abogado/a en ejercicio, con despacho profesional abierto en [LOCALIDAD], colegiado/a n.º [Nº DE COLEGIADO] del Ilustre Colegio de la Abogacía de [COLEGIO], ante el Tribunal comparezco y, como mejor en Derecho proceda, DIGO:

Que mediante el presente escrito vengo a formular demanda de MODIFICACIÓN DE CONVENIO REGULADOR por el procedimiento establecido en el art. 777 LEC, a la que se acompaña PROPUESTA DE NUEVO CONVENIO, todo ello de conformidad con los hechos y fundamentos de Derecho que se especificarán.

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa e, incluso, en una eventual fase de ejecución por medios telemáticos, en términos del art. 399.1, párrafo segundo, LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y número de teléfono: [CORREO ELECTRÓNICO] / [TELÉFONO].

HECHOS

PRIMERO.– Dña. [NOMBRE Y APELLIDOS] y D. [NOMBRE Y APELLIDOS] contrajeron matrimonio en [LOCALIDAD], el día [DÍA] de [MES] de [AÑO], inscrito en el Registro Civil de dicha localidad, tomo [TOMO], página [PÁGINA].

SEGUNDO.– Del referido matrimonio nacieron y viven dos hijos llamados:

[NOMBRE DEL HIJO/A], nacido/a en [LOCALIDAD] el día [FECHA], constando inscrito su nacimiento en el Registro Civil de [LOCALIDAD], tomo [TOMO], página [PÁGINA], y

[NOMBRE DEL HIJO/A], nacido/a en [LOCALIDAD] el día [FECHA], constando inscrito su nacimiento en el Registro Civil de [LOCALIDAD], tomo [TOMO], página [PÁGINA].

TERCERO.– Dña. [NOMBRE Y APELLIDOS] y D. [NOMBRE Y APELLIDOS] se hallan [ELEGIR: separados / divorciados] en virtud de sentencia firme de fecha [FECHA], dictada por [ÓRGANO JUDICIAL: Sección de Familia, Infancia y Capacidad del Tribunal de Instancia n.º [Nº] de [SEDE]], en los autos de [CLASE DE PROCEDIMIENTO] n.º [Nº DE PROCEDIMIENTO].

En dicha sentencia, que es firme, se aprobaba en su integridad el convenio suscrito por ambas partes con fecha [FECHA].

El contenido del convenio no ha sido modificado por ninguna otra resolución.

En el citado convenio, teniendo en cuenta las circunstancias concurrentes, se establecía en la cláusula primera:

I.– Guarda y custodia de los hijos: los hijos quedan bajo la guarda y custodia de la madre, con la que convivirán. La patria potestad sobre los hijos será compartida por ambos progenitores. [AJUSTAR A LO PACTADO EN EL CONVENIO ORIGINAL.]

CUARTO.– En el momento de aprobarse dicho convenio las circunstancias eran que D./Dña. [NOMBRE Y APELLIDOS] estaba empleado/a como [PROFESIÓN Y CONDICIONES DE TRABAJO], lo que exigía su ausencia del domicilio durante prolongadas temporadas.

En la actualidad, la situación es la siguiente: a) D./Dña. [NOMBRE Y APELLIDOS] trabaja desde [FECHA] con contrato laboral indefinido en la empresa [DENOMINACIÓN SOCIAL] y tiene residencia fija en [LOCALIDAD]; b) el hijo común llamado [NOMBRE] ha manifestado la voluntad de vivir con su padre, sin que la madre se oponga a su decisión; c) la madre, Dña. [NOMBRE Y APELLIDOS], padece un delicado estado de salud que le imposibilita atender adecuadamente al cuidado de los dos hijos.

QUINTO.– Que es voluntad de ambos progenitores solicitar judicialmente dicha modificación, por lo que se plantea la presente demanda de modificación de convenio, y únicamente respecto de la atribución de la guarda y custodia del hijo menor llamado [NOMBRE] al padre, D./Dña. [NOMBRE Y APELLIDOS], en el domicilio de éste, estableciéndose para la madre, Dña. [NOMBRE Y APELLIDOS], un régimen de visitas en los términos que resultan del convenio regulador propuesto.

A tal fin, Dña. [NOMBRE Y APELLIDOS] y D. [NOMBRE Y APELLIDOS] han procedido de mutuo acuerdo a elaborar una nueva propuesta de convenio regulador para que regule sus relaciones futuras y sustituya al aportado con la demanda de [FECHA].

Como fundamento de los anteriores hechos adjuntan a la presente demanda los siguientes documentos:

1. En relación con el hecho PRIMERO, para acreditar la existencia del matrimonio, la oportuna certificación de la inscripción de matrimonio del Registro Civil, que se acompaña como documento n.º [Nº DE DOCUMENTO].

2. Respecto al hecho SEGUNDO, para acreditar la existencia de los hijos habidos en común, se adjunta certificación de inscripción de nacimiento, que se acompaña como documentos n.º [Nº DE DOCUMENTOS].

3. En prueba del hecho TERCERO se acompaña testimonio de la resolución judicial y el convenio regulador como documentos n.º [Nº DE DOCUMENTOS].

4. Finalmente se adjunta propuesta de nuevo convenio regulador, firmada por ambos cónyuges, que en prueba de su conformidad el hijo también firma, como documento n.º [Nº DE DOCUMENTO].

FUNDAMENTOS DE DERECHO

I.– COMPETENCIA.

Es competente el Tribunal al que nos dirigimos de conformidad con lo dispuesto en el art. 769 LEC, al corresponder al lugar del último domicilio conyugal.

II.– LEGITIMACIÓN.

La legitimación activa corresponde a ambos cónyuges conforme a lo dispuesto en el art. 775.1 LEC. Con arreglo al art. 777.5 LEC, deberá oírse al Ministerio Fiscal y al hijo común llamado [NOMBRE] en el caso de que el Tribunal lo considere necesario o así lo solicite el Ministerio Fiscal.

III.– PROCEDIMIENTO.

La modificación del convenio regulador tiene asignado el trámite señalado en el art. 777 LEC, dado que la petición se hace por uno de los cónyuges con el consentimiento del otro (art. 777.9 LEC).

IV.– CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda no está sujeta al previo intento de resolución de controversias en vía no jurisdiccional de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia, por tratarse en sí de un acuerdo consensual y voluntario entre las partes, necesitando únicamente la homologación del mismo por parte del Tribunal.

V.– FUNDAMENTOS DE DERECHO MATERIALES O SOBRE EL FONDO DEL ASUNTO.

El art. 90 CCiv señala que las medidas que el Juez acuerde en defecto de acuerdo o las convenidas por los cónyuges podrán ser modificadas judicialmente o por nuevo convenio cuando se alteren sustancialmente las circunstancias.

Las medidas relativas al cuidado de los hijos comunes menores de edad deben ser adoptadas siempre en su beneficio, como ha manifestado reiteradamente la jurisprudencia, debiendo prevalecer siempre el bienestar de los mismos.

En el caso presente, resulta claro que se han alterado las circunstancias que en su día fueron tenidas en cuenta para confiar la custodia y compañía de los dos hijos menores a la madre como consecuencia del proceso de [SEPARACIÓN/DIVORCIO] seguido, pues resulta patente tanto la indisposición física de la madre para ocuparse de ambos como la voluntad del menor [NOMBRE], que ya tiene [EDAD] años, de querer vivir con su padre, con el que de hecho, y pese a lo acordado en la sentencia de [SEPARACIÓN/DIVORCIO] al principio citada, viene conviviendo desde hace [TIEMPO], por lo que es conveniente legalizar esa situación de hecho confiando la custodia y compañía del hijo menor [NOMBRE] al padre, que es quien realmente lo tiene, estimándose esta medida como la beneficiosa para el hijo, conforme a la prescripción contenida en el art. 92.2 CCiv, que ordena al Juez velar por el cumplimiento de su derecho a ser oído cuando deba adoptar cualquier medida sobre la custodia, el cuidado y la educación de los hijos menores. Y, si bien es cierto que la jurisprudencia viene entendiendo que, en aplicación del art. 92 del citado Código, habrá de procurarse no separar a los hermanos, en este caso concreto concurren muy especiales circunstancias que imponen dar prioridad al supremo interés del menor, conforme enseña la Convención sobre los Derechos del Niño (1989), que expresa que «el interés del menor debe constituir la principal preocupación de los implicados en el proceso, por encima incluso del interés del padre, de la madre y de los hermanos», sobre todo teniendo en cuenta que los dos hijos menores tienen actualmente [EDAD] y [EDAD] años, respectivamente, es decir, que poseen capacidad de discernimiento suficiente para decidir con cuál de los progenitores desean seguir conviviendo. Todo ello, claro está, sin perjuicio de que la patria potestad se ejerza por ambos progenitores, que deberán velar por una mayor comunicación entre los hermanos fomentando el afecto y cariño entre ellos, cosa que siempre han hecho, y para cuyo fin se ha de mantener el mismo derecho de visitas para la madre, respecto de su hijo [NOMBRE], que anteriormente se estableció en favor del padre, quien a su vez deberá avivar sus relaciones con el otro hijo cuya custodia y compañía se encomienda a la madre, dado que la convivencia de los hijos con los padres y los hermanos solo ventajas puede reportarles, conforme a lo dispuesto en el art. 94 CCiv.

En su virtud,

SUPLICO AL TRIBUNAL

que, habiendo por presentado este escrito junto con los documentos y copias que se acompañan, se sirva admitirlo, y por formulada demanda de modificación de convenio regulador, de mutuo acuerdo, entendiéndose conmigo las sucesivas diligencias, y previos los pertinentes trámites, los cónyuges sean requeridos para que comparezcan y se ratifiquen por separado, con intervención del Ministerio Fiscal y oyéndose al hijo menor [NOMBRE] en el caso de que el Tribunal lo estimare necesario, dictándose en su día sentencia aprobando la modificación de convenio regulador otorgada por ambos cónyuges.

Es justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a Firma del Procurador/a
