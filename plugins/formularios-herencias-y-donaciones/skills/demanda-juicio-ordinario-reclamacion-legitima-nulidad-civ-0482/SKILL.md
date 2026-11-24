---
name: demanda-juicio-ordinario-reclamacion-legitima-nulidad-civ-0482
description: "Demanda de juicio ordinario de reclamación de legítima por nulidad de la desheredación. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio ordinario de reclamación de legítima por nulidad de la desheredación

> Formulario **CIV-0482** del plugin **Herencias, testamentos y donaciones** (`formularios-herencias-y-donaciones`) · Civil › Sucesiones y donaciones · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario de los hijos desheredados por su padre (por la causa 1.ª del art. 853 CC: negativa injustificada de alimentos) para que se declare la nulidad de la cláusula de desheredación y de la institución de heredero en cuanto perjudique su legítima, y se reconozca su derecho a la legítima en la herencia (arts. 848 a 851 CC).

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio ordinario de reclamación de legítima por nulidad de la desheredación» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio ordinario de reclamación de legítima por nulidad de la desheredación” para mi caso». También puedes invocarla directamente con `/formularios-herencias-y-donaciones:demanda-juicio-ordinario-reclamacion-legitima-nulidad-civ-0482`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-herencias-y-donaciones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Herencias, testamentos y donaciones) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (15 veces)
- [ ] Nº DE DOCUMENTO (14 veces)
- [ ] LOCALIDAD (11 veces)
- [ ] NOMBRE Y APELLIDOS DEL CAUSANTE (9 veces)
- [ ] FECHA (8 veces)
- [ ] DOMICILIO (4 veces)
- [ ] IMPORTE (4 veces)
- [ ] NOMBRE DEL NOTARIO (4 veces)
- [ ] AÑO (3 veces)
- [ ] Nº (3 veces)
- [ ] SEDE (3 veces)
- [ ] CORREO ELECTRÓNICO (2 veces)
- [ ] EL/LA HIJO/A (2 veces)
- [ ] NOMBRE Y APELLIDOS DE LA HEREDERA (2 veces)
- [ ] NOMBRE Y APELLIDOS DE LA PARTE DEMANDADA (2 veces)
- [ ] Nº DE DOCUMENTOS (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] TELÉFONO (2 veces)
- [ ] AGENCIA DE VIAJES
- [ ] CENTRO HOSPITALARIO
- [ ] CLASE DE PENSIÓN
- [ ] COLEGIO
- [ ] DOMICILIO LABORAL
- [ ] DÍA
- [ ] EDAD
- [ ] FECHAS
- [ ] LUGAR DEL FALLECIMIENTO
- [ ] MES
- [ ] NOMBRE Y APELLIDOS DEL LETRADO/A
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº DE COLEGIADO
- [ ] Nº DE PROTOCOLO
- [ ] PROVINCIA

## Normas que cita el formulario

- art. 24.1 LEC
- art. 24.2 LEC
- art. 155.3 LEC
- art. 399.1 LEC
- art. 853 Código Civil
- art. 85.1 LOPJ
- art. 52.1.4.º LEC
- art. 23 LEC
- art. 251 LEC
- art. 253.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 399 LEC
- art. 851 CC
- art. 853.1.ª CC
- art. 849 CC
- art. 853 CC
- art. 850 CC
- art. 848 CC
- art. 142 CC
- art. 148 CC
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

### Avisos de actualización (3) — se aplican en el texto, nunca se copian en el documento

- Junto a «…N CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] QUE POR TURNO DE REPARTO CORRESPONDA»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…de nulidad de la disposición testamentaria que desheredó a mis dos patrocinados.»: comprobar la redacción vigente de los arts. 848 a 857 CC tras la Ley 8/2021 antes de citar literalmente las causas de desheredación.
- Junto a «…OCALIDAD], a [DÍA] de [MES] de [AÑO]. Firma del Abogado/a Firma del Procurador/a»: requisito de procedibilidad (art. 5 LO 1/2025): antes de demandar hay que intentar un medio adecuado de solución de controversias y acreditarlo con la demanda, salvo las materias excluidas del art. 5.2.

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] QUE POR TURNO DE REPARTO CORRESPONDA

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [DOMICILIO], y D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [DOMICILIO], representación que acredito mediante:

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]
— poder otorgado a mi favor a través de la sede judicial electrónica (inscrito en el Registro Electrónico de Apoderamientos Judiciales), cuya certificación acompaño como documento n.º [Nº DE DOCUMENTO];
— poder otorgado mediante comparecencia apud acta ante el Letrado de la Administración de Justicia, inscrito en el Registro Electrónico de Apoderamientos Judiciales, cuya certificación acompaño como documento n.º [Nº DE DOCUMENTO];
— escritura de poder otorgada a mi favor ante el Notario D./Dña. [NOMBRE DEL NOTARIO], con n.º de protocolo [Nº DE PROTOCOLO], inscrita en el Registro Electrónico de Apoderamientos Judiciales, cuya certificación acompaño como documento n.º [Nº DE DOCUMENTO];

(Existen tres posibilidades para otorgar el apoderamiento al Procurador de los Tribunales, conforme dispone el art. 24.1 LEC. Todos los poderes deben estar inscritos en el Registro Electrónico de Apoderamientos Judiciales para su acreditación; basta, en principio, la consulta automatizada del Registro por el Letrado de la Administración de Justicia, y la certificación de la inscripción es la vía subsidiaria del art. 24.2 LEC, por lo que el modelo acompaña la certificación electrónica.)

bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS DEL LETRADO/A], abogado/a en ejercicio, con despacho profesional abierto en [LOCALIDAD], colegiado/a n.º [Nº DE COLEGIADO] del Ilustre Colegio de la Abogacía de [COLEGIO], ante el Tribunal comparezco y, como mejor en Derecho proceda, DIGO:

Que mediante el presente escrito vengo a formular DEMANDA DE JUICIO DECLARATIVO ORDINARIO contra D./Dña. [NOMBRE Y APELLIDOS DE LA PARTE DEMANDADA], con domicilio en [DOMICILIO] (primero) y [DOMICILIO LABORAL] (segundo, domicilio laboral), con correo electrónico [CORREO ELECTRÓNICO] y número de teléfono móvil [TELÉFONO], en ejercicio de la acción que se concretará en el cuerpo del escrito y en el suplico, y todo ello de conformidad con los hechos y fundamentos de Derecho que se desarrollarán a continuación.

(El art. 155.3 LEC permite expresar varios domicilios del demandado: el que figure en el padrón municipal o conste oficialmente a estos efectos; el que aparezca en registro oficial o en publicaciones de colegios profesionales, si se trata de empresas o personas colegiadas; aquel donde desarrolle su actividad profesional o laboral no ocasional; si es empresa mercantil, el de cualquiera de sus administradores, gerentes o apoderados; o, si es asociación inscrita en registro oficial, el del presidente, miembro o gestor de la junta correspondiente. Cuando se señalen varios, se indicará el orden a seguir para la notificación. El mismo precepto obliga al demandante a aportar cuantos datos sean de utilidad para localizar al demandado: NIF o NIE, teléfono, correo electrónico o similares.)

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa e, incluso, en una eventual fase de ejecución por medios telemáticos, en términos del art. 399.1, párrafo segundo, LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y número de teléfono: [CORREO ELECTRÓNICO] / [TELÉFONO].

HECHOS

PRIMERO.–

Mis representados son hijos de D./Dña. [NOMBRE Y APELLIDOS DEL CAUSANTE], habidos del matrimonio de éste con su madre D./Dña. [NOMBRE Y APELLIDOS], siendo que aquel primero falleció en [LUGAR DEL FALLECIMIENTO], el [FECHA].

Se acompañan certificados de defunción, matrimonio y nacimiento como documentos n.º [Nº DE DOCUMENTO] a [Nº DE DOCUMENTO].

SEGUNDO.–

D./Dña. [NOMBRE Y APELLIDOS DEL CAUSANTE] otorgó último testamento abierto, ante el Notario de [LOCALIDAD], D./Dña. [NOMBRE DEL NOTARIO], en el que expresamente deshereda a mis representados, atribuyéndoles haber incurrido en la causa primera del art. 853 del Código Civil, e instituye heredera universal a su esposa D./Dña. [NOMBRE Y APELLIDOS DE LA HEREDERA].

Se acompaña copia del citado testamento como documento n.º [Nº DE DOCUMENTO].

TERCERO.–

D./Dña. [NOMBRE Y APELLIDOS DEL CAUSANTE] se separó de hecho de su primera esposa, D./Dña. [NOMBRE Y APELLIDOS], en el año [AÑO], al trasladarse la madre a vivir, junto con los hijos, a la ciudad de [LOCALIDAD], separándose legalmente los cónyuges por sentencia del Tribunal de Instancia n.º [Nº] de [SEDE], de [FECHA] (se aporta como documento n.º [Nº DE DOCUMENTO]), en la que se establece una pensión de alimentos de [EL/LA HIJO/A], que queda bajo la guarda de la madre, a cargo del padre, de [IMPORTE] euros mensuales, y cuya sentencia fue confirmada, salvo en lo relativo a la cuantía de la pensión establecida a favor de la esposa, que se reduce a la suma de [IMPORTE] euros mensuales, por la dictada en grado de apelación con fecha [FECHA] por la Sección [Nº] de la Audiencia Provincial de [PROVINCIA] (documento n.º [Nº DE DOCUMENTO] de esta demanda), y finalmente el divorcio de los cónyuges se produjo por sentencia de fecha [FECHA] del Tribunal de Instancia n.º [Nº] de [SEDE], en la que se vienen a ratificar las medidas acordadas en anterior sentencia de separación, la cual se acompaña como documento n.º [Nº DE DOCUMENTO].

CUARTO.–

El testador D./Dña. [NOMBRE Y APELLIDOS DEL CAUSANTE] contrajo matrimonio con la demandada D./Dña. [NOMBRE Y APELLIDOS], el [FECHA], si bien la convivencia con la misma se remonta a, por lo menos, [NÚMERO] años antes.

Se aporta certificado de matrimonio como documento n.º [Nº DE DOCUMENTO].

QUINTO.–

[HECHOS SOBRE LA SITUACIÓN DE SALUD Y AUTONOMÍA DEL TESTADOR QUE DESVIRTÚAN EL ESTADO DE NECESIDAD. En el modelo original: el testador había sufrido en el año [AÑO] una hemorragia cerebral, practicándosele una craniectomía para extraer un coágulo, tras lo que recuperó el habla y la vista, quedando inicialmente paralizado del lado derecho si bien posteriormente, tras realizar rehabilitación, fue recuperando movilidad hasta llegar a valerse por sí mismo, llegando incluso a conducir un vehículo adaptado y realizar viajes y excursiones organizadas para la tercera edad, en las que no le acompañaba su esposa.]

Acompañamos copia de documentación clínica como documentos n.º [Nº DE DOCUMENTOS] y certificación de [AGENCIA DE VIAJES] como documento n.º [Nº DE DOCUMENTO].

SEXTO.–

D./Dña. [NOMBRE Y APELLIDOS DEL CAUSANTE] venía percibiendo una pensión de [CLASE DE PENSIÓN] con una cuantía de [IMPORTE] euros, habiendo adquirido años antes un vehículo adaptado a su situación y una vivienda con garaje y bodega, en la que habitaba junto con su esposa, sita en [LOCALIDAD], calle [DOMICILIO], n.º [NÚMERO].

Se acompaña certificación del Instituto Nacional de la Seguridad Social como documento n.º [Nº DE DOCUMENTO] y certificado del Registro de la Propiedad de [LOCALIDAD] como documento n.º [Nº DE DOCUMENTO].

SÉPTIMO.–

La parte actora manifiesta que, previamente a la presentación de la presente demanda, se han llevado a cabo negociaciones con la parte demandada con el objetivo de cumplir el requisito de procedibilidad y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria, incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, mediante requerimiento notarial de fecha [FECHA], mis representados exigieron a la demandada que no ejecutara el testamento sino que, como hijos de su finado esposo, les reconociera sus derechos de legítima, prescindiendo de una desheredación cuya causa no desconocía inexistente.

No ha mediado respuesta alguna, por lo que no ha quedado más recurso que acudir a los tribunales, aportando el acta del Notario de [LOCALIDAD], D./Dña. [NOMBRE DEL NOTARIO], como documento n.º [Nº DE DOCUMENTO].

A los anteriores hechos son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

I.– PRESUPUESTOS SUBJETIVOS

I.1. JURISDICCIÓN Y COMPETENCIA

Radicando la competencia genérica en el orden civil de la jurisdicción, detenta la competencia objetiva y funcional la Sección Civil del Tribunal de Instancia, por aplicación de lo dispuesto en los arts. 85.1 LOPJ y 45 LEC, y territorialmente es competente el Tribunal a que me dirijo, puesto que está prevenido el fuero territorial preceptivo específico para los juicios sobre cuestiones hereditarias, con arreglo a lo previsto en el art. 52.1.4.º LEC, del lugar del último domicilio del finado, siendo de este partido la población en que se hallaba la residencia donde murió D./Dña. [NOMBRE Y APELLIDOS DEL CAUSANTE].

I.2. CAPACIDAD Y LEGITIMACIÓN

Mis mandantes son personas físicas, mayores de edad, en pleno ejercicio de sus derechos civiles, así como lo es el/la demandado/a, D./Dña. [NOMBRE Y APELLIDOS], por lo que todos tienen capacidad para ser parte y capacidad procesal ex arts. 6.1.1.º y 7.1 LEC.

Corresponde la legitimación activa directa a mis mandantes, ya que son herederos forzosos legitimarios, como hijos del causante, y está legitimada pasivamente de forma directa la demandada, en su condición de heredera testamentaria.

I.3. POSTULACIÓN Y DEFENSA

Conforme a los arts. 23 y 31 LEC se formula esta demanda por medio de representación de Procurador/a de los Tribunales con poder para pleitos, y bajo dirección y firma de Letrado habilitado ante el Tribunal.

II.– PRESUPUESTOS OBJETIVOS

II.1. PROCEDIMIENTO

La presente demanda deberá sustanciarse por las normas del juicio ordinario, a tenor de lo prevenido en los arts. 248, 249.2 y 253.3 LEC, toda vez que ningún criterio de atribución preferente de la materia objeto del proceso resulta aplicable, puesto que la regla 12.ª del art. 251 LEC, referida a pleitos relativos a una herencia, se corresponde con condenas afectantes a los bienes o masas patrimoniales, y no a las meras declaraciones de nulidad parcial de testamento y de la condición de heredero forzoso con derecho a la legítima que constriñe los derechos hereditarios de la demandada.

II.2. CUANTÍA

Cumpliendo lo prevenido en el art. 253.1 y 3 LEC, hacemos constar que la cuantía de esta demanda es indeterminada.

II.3. CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4.º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

II.4. REQUISITOS FORMALES

No aparecen, aparte de los requisitos genéricos de la demanda en juicio ordinario del art. 399 LEC, otros de carácter formal cuya falta, por el tipo de acción, invalidarían el proceso para pronunciarse sobre el fondo del asunto.

III.– FONDO DEL ASUNTO

Los actores, mis patrocinados, ejercitan la acción de impugnación del testamento otorgado por su finado padre, con fundamento en el art. 851 CCiv, porque adolece de nulidad el testamento otorgado por éste, D./Dña. [NOMBRE Y APELLIDOS DEL CAUSANTE], con fecha [FECHA], en cuanto que contiene una cláusula de desheredación de dichos actores, sus hijos D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS], en la medida en que, basada tal desheredación en haber negado los descendientes alimentos al progenitor, nunca ha existido una reclamación expresa de alimentos por parte del testador a los actores, correspondiendo dicha prueba a quien aprovecha el testamento, la viuda, instituida heredera universal única, y por ende en ningún momento se ha podido negar por parte de los hijos alimentos a su padre que, además, no consta los necesitase.

La cláusula de desheredación expresada en el acto de última voluntad es la señalada en el art. 853.1.ª CCiv, que consiste en «haber negado, sin motivo legítimo, los alimentos al padre o ascendiente que le deshereda», y se niega en absoluto la verdad de la imputación, solicitando la declaración de nulidad de la disposición testamentaria que desheredó a mis dos patrocinados.

Como dijo la STS de 15 de junio de 1990, ha de tenerse en cuenta que la disposición desheredatoria impugnada es una declaración de voluntad testamentaria, solemne (art. 849 CCiv), en virtud de la cual quien goza de la facultad de testar priva a sus herederos forzosos del derecho a legítima cuando en ellos concurre cualquiera de las causas legales (art. 853 CCiv) de la que sean responsables. Su carácter solemne requiere que se manifieste en testamento, que exista alguna de las causas tasadas y que se indique por el testador la aplicada, puesto que la certeza puede ser contradicha por el desheredado y, en tal caso, ha de demostrarse en juicio la existencia de la misma (art. 850 CCiv), señalando, por su parte, la STS de 28 de junio de 1993 la interpretación restrictiva de la institución que se impone, proclamada en el art. 848 CCiv y sostenida por jurisprudencia inconcusa, orientada en la defensa de la sucesión legitimaria, sin admitirse nunca la analogía, ni la interpretación extensiva, ni siquiera la argumentación «de minoris ad maiorem». La interpretación «ad restringenda» en la aplicación de las causas de desheredación, por su carácter claramente sancionador, se remarca en la STS de 4 de noviembre de 1997, rec. 3056/1993.

La causa 1.ª del art. 853 CCiv consiste en la negativa injusta de los alimentos al progenitor causante, y ha de concretarse en una específica obligación de alimentos, con prueba de las circunstancias que eventualmente darían lugar a ello. No puede interpretarse la obligación de alimentos en forma extensiva incluyendo toda clase de cuidados y atenciones, incluso las de naturaleza afectiva, sino las específicas del art. 142 CCiv, comprensivo de «lo indispensable para el sustento, habitación, vestido y asistencia médica». Se requiere, pues: a) un estado de necesidad; b) un requerimiento o petición a los eventuales y futuros herederos legitimarios, como alimentantes; y c) una negativa injustificada de los desheredados a prestarlos.

Pues bien, de ninguna de las maneras pueden tenerse por probados actos que puedan entenderse comprendidos en la citada causa 1.ª del art. 853 CCiv.

En efecto, no consta la negativa de los hijos a prestar alimentos a su padre, puesto que, para que hubiera podido darse tal negativa, aunque fuera tácita, sería preciso que hubiera mediado una previa solicitud de alimentos por parte del causante, y ello no ha ocurrido nunca. Tampoco ha existido realmente la necesidad para subsistir de la persona que tendría derecho a ello, D./Dña. [NOMBRE Y APELLIDOS DEL CAUSANTE] (art. 148 CCiv), y así queda acreditado que el testador disponía de una capacidad económica importante, como lo prueba que era beneficiario de una pensión de unos [IMPORTE] euros mensuales, que no le hacía merecedor de recibir alimentos, puesto que incluso le permitió la adquisición de un vehículo adaptado y una vivienda y, en cuanto a la asistencia médica, la tenía cubierta por la Seguridad Social, y así consta haber sido atendido en dos ocasiones en el [CENTRO HOSPITALARIO] (nos remitimos a los documentos números [Nº DE DOCUMENTOS]).

En consecuencia, efectivamente había una situación de distanciamiento mutuo entre el testador y sus hijos, iniciándose la situación de desafecto desde la separación del testador con la primera esposa y madre de mis mandantes, y que, por lo que hace a [EL/LA HIJO/A], D./Dña. [NOMBRE Y APELLIDOS], se mantiene desde que éste/a tenía [EDAD] años de edad, y que halló ocasión, según su propia manifestación, en la negativa del padre a facilitarle la llave de la que había sido casa familiar, ya que aquel por entonces ya convivía con la demandada D./Dña. [NOMBRE Y APELLIDOS], para que pudiera pasar sus vacaciones en [LOCALIDAD], adonde se había trasladado desde su residencia en [LOCALIDAD], teniendo que irse a casa de una amistad; y asimismo, con razón en que D./Dña. [NOMBRE Y APELLIDOS] le insistía para que renunciara a la pensión de alimentos que le había sido fijada en la sentencia de separación y para cuyo pago hubo de acordarse judicialmente la retención ante la falta de cumplimiento voluntario por parte del padre.

En definitiva, aunque los demandantes se hallaban alejados, física y moralmente, de su padre, hasta el punto de no mantener contacto alguno con el mismo, aunque si no lo visitaron durante su última enfermedad ni asistieron a su sepelio fue por no haber sido avisados de la enfermedad y muerte por sus familiares en [LOCALIDAD], no se convierte ello en causa de desheredación. En este sentido, la precitada STS de 28 de junio de 1993 reconoce que la falta de relación afectiva y comunicación entre los hijos y el padre, e incluso el abandono sentimental sufrido por éste, o la ausencia de interés del hijo por los problemas del padre o su última enfermedad, son circunstancias que corresponden al campo de la moral y «escapan a la apreciación y a la valoración jurídica, y que en definitiva solo están sometidas al tribunal por la conciencia». Esto al margen de que en el caso presente tampoco podrá demostrarse un abandono moral.

En cualquier caso, si los desheredados, mis patrocinados, no negaron alimentos al padre, no se demuestra la causa de la desheredación (art. 850 CCiv) por la parte a quien le incumbe, la cláusula testamentaria conteniendo la desheredación es ineficaz, debiéndose estar a lo dispuesto en el art. 851 CCiv, esto es, a la declaración de la nulidad de la institución de heredero en cuanto perjudique al desheredado, si bien salvando las disposiciones testamentarias en lo que no perjudiquen a la legítima.

IV.– COSTAS

Conforme al principio del vencimiento objetivo del art. 394.1 LEC, las costas irrogadas a esta parte en el juicio declarativo en la primera instancia se han de pronunciar a cargo de la demandada.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito, con sus copias y documentos que se acompañan, se sirva admitir uno y otros; en su virtud, tener por interpuesta, en la representación que ostento, la presente demanda de juicio declarativo ordinario contra D./Dña. [NOMBRE Y APELLIDOS DE LA PARTE DEMANDADA], quien deberá ser emplazada a fin de que pueda contestar, si a su derecho le conviene, y previos los oportunos trámites legales, en su día dicte sentencia por la que se declare:

1.– La nulidad de la cláusula del testamento otorgado por D./Dña. [NOMBRE Y APELLIDOS DEL CAUSANTE] ante el Notario de [LOCALIDAD], D./Dña. [NOMBRE DEL NOTARIO], el día [FECHA], que deshereda a los actores, D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS].

2.– La nulidad de la institución de heredera única y universal de D./Dña. [NOMBRE Y APELLIDOS DE LA HEREDERA], en todo aquello que afecte al derecho de legítima de los hijos.

3.– El derecho de D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS], como herederos forzosos, a la legítima de dos tercios en la herencia de su padre.

Todo ello con expresa imposición de las costas procesales a la parte demandada que se oponga.

OTROSÍ DIGO: que, siendo general para pleitos el poder que presenta el/la Procurador/a que suscribe, y precisándolo para otros usos,

SUPLICO AL TRIBUNAL

que, teniendo por hecha la manifestación anterior, se acuerde el desglose de la copia auténtica del poder para pleitos y su devolución a esta parte.

Es justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a Firma del Procurador/a
