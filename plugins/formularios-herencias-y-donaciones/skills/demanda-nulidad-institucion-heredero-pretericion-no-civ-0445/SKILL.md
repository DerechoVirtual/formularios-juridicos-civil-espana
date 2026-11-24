---
name: demanda-nulidad-institucion-heredero-pretericion-no-civ-0445
description: "Demanda de nulidad de la institución de heredero por preterición no intencional. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de nulidad de la institución de heredero por preterición no intencional

> Formulario **CIV-0445** del plugin **Herencias, testamentos y donaciones** (`formularios-herencias-y-donaciones`) · Civil › Sucesiones y donaciones · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio declarativo ordinario en ejercicio de acción de nulidad de institución de heredero testamentario por preterición no intencional de uno de los legitimarios solicitando se declare abierta la sucesión ab intestato del causante

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de nulidad de la institución de heredero por preterición no intencional» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de nulidad de la institución de heredero por preterición no intencional” para mi caso». También puedes invocarla directamente con `/formularios-herencias-y-donaciones:demanda-nulidad-institucion-heredero-pretericion-no-civ-0445`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-herencias-y-donaciones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Herencias, testamentos y donaciones) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (23 veces)
- [ ] FECHA (10 veces)
- [ ] Nº DE DOCUMENTO (5 veces)
- [ ] NOMBRE DEL MENOR (4 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] AÑO
- [ ] CORREO ELECTRÓNICO
- [ ] LUGAR
- [ ] Nº
- [ ] Nº DE COLEGIADO/A
- [ ] SEDE
- [ ] TELÉFONO

## Normas que cita el formulario

- art. 24.1 LEC
- art. 399.1 LEC
- art. 85.1 LOPJ
- art. 52.1.4.º LEC
- art. 6.1.1.º LEC
- art. 7.1 LEC
- art. 154 CC
- art. 251 LEC
- art. 253.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 399 LEC
- art. 814 CC
- art. 662 CC
- art. 808 CC
- art. 675 CC
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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: Un solo TI por partido judicial (art. 84.1 LOPJ): sobra «de los de». Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) A la hora de su acreditación, todos los poderes deben estar inscritos en el Registro Electrónico de Apoderamientos Judiciales (REAJ). Se supone que, para su acreditación, basta con la consulta (de dicho Registro) automatizada orientada al dato. Algo que está a disposición de cualquier Letrado de la Administración de Justicia. Sin embargo, dado que el art. 24.2 LEC, configura la certificación de dicha inscripción como vía subsidiaria de acreditación, para el caso de que el sistema no permita aquella consulta automatizada; se señala en el modelo que se acompaña certificación electrónica. El sistema permite emitir dicha certificación para quien inscribe el poder.

(2) La falta de mención en el testamento de todos los herederos forzosos por preterición errónea tiene como efecto la anulación de las disposiciones testamentarias de contenido patrimonial, según dispone el artículo 814, párrafo segundo, número primero CCiv.

(3) El art. 155.3 LEC permite fijar expresar varios domicilios del demandado (el que aparezca en el padrón municipal o conste oficialmente a estos efectos; el que aparezca en Registro oficial o en publicaciones de colegios profesionales, si se trata de empresas o personas colegiadas; donde desarrolle su actividad profesional o laboral no ocasional; si es empresa mercantil, el domicilio de cualquiera de sus administradores, gerentes, o apoderados; o, si es asociación que consta en registro oficial; el domicilio del presidente, miembro o gestor de la Junta correspondiente). Cuando se señalen varios, indicará el orden a seguir para la notificación, con vistas al éxito de la misma.

(4) El art. 155.3 LEC configura una obligación adicional del demandante, consistente en aportar cuantos datos sean de utilidad para localizar al demandado: número de identificación fiscal o de extranjeros, nº [Nº] de teléfono o de fax, dirección de correo electrónico, o similares.

========================================================================

[NOTA DE REVISIÓN: requisito de procedibilidad del art. 5 LO 1/2025 — antes de presentar la demanda hay que intentar un medio adecuado de solución de controversias (MASC) y acreditarlo con la demanda (arts. 264.4.º y 399.3 LEC), salvo las materias excluidas del art. 5.2. Fuente: LO 1/2025, arts. 5 a 7 (BOE-A-2025-76).]


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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.C.

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS] actuando en interés de su hijo menor de edad [NOMBRE DEL MENOR], con domicilio en [LOCALIDAD], representación que acredito mediante escritura de poder otorgada a mi favor (existen tres posibilidades para otorgar el apoderamiento al Procurador de los Tribunales, conforme dispone el art. 24.1 LEC)

[OPCIONAL — opción en función de cómo se haya otorgado el poder]

[ELEGIR UNA OPCIÓN: Si el poder se otorga a través de la sede judicial electrónica / Si el poder se otorga mediante comparecencia apud acta / Si el poder se otorga ante Notario]

bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS], abogado/a en ejercicio, con despacho profesional abierto en [LOCALIDAD], colegiado nº [Nº DE COLEGIADO/A] del Ilustre Colegio de la Abogacía de [LOCALIDAD], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que mediante el presente escrito vengo a formular a DEMANDA de JUICIO DECLARATIVO ORDINARIO ejercitando ACCIÓN DE NULIDAD DE INSTITUCIÓN DE HEREDERO respecto al patrimonio hereditario del difunto D./Dña. [NOMBRE Y APELLIDOS], contra D./Dña [NOMBRE Y APELLIDOS], con domicilio, primero en [DOMICILIO]; y segundo, el domicilio laboral en [DOMICILIO]); con email [CORREO ELECTRÓNICO]; y con número de teléfono móvil [TELÉFONO] y D./Dña. [NOMBRE Y APELLIDOS]; todo ello de conformidad con los hechos y fundamentos de derecho que se especificarán.

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa, e, incluso, en una eventual fase de ejecución por medios telemáticos, en términos del art. 399.1 II LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y nº [Nº] de teléfono:

HECHOS

PRIMERO

D./Dña. [NOMBRE Y APELLIDOS] otorgó testamento notarial el [FECHA], instituyendo herederos universales de todos sus bienes, por partes iguales, a las dos hijos habidos de su matrimonio con Don/Doña [NOMBRE Y APELLIDOS], los hoy demandados D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS]

Acompañamos copia simple, haciendo documento n.º [NÚMERO], por no disponer del original testamento de D./Dña. [NOMBRE Y APELLIDOS]

SEGUNDO

Dicho testador, desde antes, convivía con mi patrocinada, Don/Doña [NOMBRE Y APELLIDOS], con la que posteriormente, el [FECHA], tuvo un hijo, en cuya representación legal, como menor de edad, actúa aquélla, que fue reconocido como hijo extramatrimonial por ambos progenitores con el nombre de [NOMBRE DEL MENOR], como se acredita mediante la oportuna certificación, que se acompaña como documento n.º [Nº DE DOCUMENTO]

TERCERO

Con fecha [FECHA] D./Dña. [NOMBRE Y APELLIDOS] y Don/Doña [NOMBRE Y APELLIDOS] suscribieron un convenio para proceder a la regulación de la guardia y custodia, régimen de visitas, alimentos y contribución a los gastos médicos, del hijo común, protocolizándolo notarialmente, y que se justifica en el documento n.º [Nº DE DOCUMENTO]

CUARTO

El pasado día [FECHA] falleció D./Dña. [NOMBRE Y APELLIDOS] sin haber llegado a otorgar testamento posterior al de [FECHA], antes mencionado. En el testamento no se menciona al hijo extramatrimonial del causante, que fue concebido y nació después de otorgado éste, ni nada ha recibido imputable a la legítima.

Se acompaña el certificado de defunción y del Registro General de Actos de última voluntad, como documentos nos [Nº DE DOCUMENTO]

QUINTO

Mediante burofax de fecha [FECHA] mi representada exigió a los demandados que se pusieran en contacto con el despacho de abogados que redactó la carta, a fin de debatir el pago de los derechos como hijo del finado D./Dña. [NOMBRE Y APELLIDOS], en la herencia del progenitor común, recibiendo contestación por la que se negaba el hecho de la filiación.

Se aporta la carta de reclamación, con su acuse de recibo, como documento n.º [NÚMERO], y la contestación como n.º [NÚMERO]

Finalmente, mi representado envió un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por el demandado por el mismo medio, rechazando el acuerdo, viéndonos en la necesidad de acudir a la presente vía judicial.

Acompaño como documento nº [Nº DE DOCUMENTO], el requerimiento efectuado y como documento nº [Nº DE DOCUMENTO], la contestación del demandado.

A los anteriores hechos son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA

Radicando la competencia genérica en el orden civil de la jurisdicción, detenta la competencia objetiva y funcional la Sección Civil del Tribunal de Instancia, por aplicación de lo dispuesto en los arts. 85.1 LOPJ y 45 LEC, y territorialmente es competente el Tribunal a que me dirijo, puesto que está prevenido el fuero territorial preceptivo específico para los juicios sobre cuestiones hereditarias, con arreglo a lo previsto en el art. 52.1.4.º LEC, del lugar del último domicilio del finado, siendo de este partido la población en que se hallaba la residencia donde murió D./Dña. [NOMBRE Y APELLIDOS]

II.- CAPACIDAD Y LEGITIMACIÓN

Todos los intervinientes detentan capacidad para ser parte ex art. 6.1.1.º LEC, en cuanto que son personas físicas, y la falta de capacidad de obrar y procesal del menor [NOMBRE DEL MENOR], se suple con la representación de su madre, titular de la patria potestad (art. 7.1 y 2 LEC en relación con art. 154 CCiv).

Corresponde la legitimación activa directa a mi mandante, actuando en interés de su hijo menor de edad como legal representante, ya que es heredero forzoso legitimario, como hijo del causante, y están legitimados pasivamente de forma directa los codemandados, en su condición de herederos testamentarios.

La viuda del causante carece de legitimación pasiva, puesto que en modo alguno puede resultar afectada por la sentencia que se dicte, ya que tiene derecho al usufructo del tercio destinado a mejora, en todo caso, es decir, tanto si se anula como si no se anula la institución de herederos, y cualquiera que sea el número de éstos.

III.- PROCEDIMIENTO

La presente demanda deberá sustanciarse por las normas del juicio ordinario, a tenor de lo prevenido en los arts. 248, 249.2 y 253.3 LEC, toda vez que ningún criterio de atribución preferente de la materia objeto del proceso resulta aplicable, puesto que la regla 12.ª del art. 251 LEC, referida a pleitos relativos a una herencia, se corresponde con condenas afectantes a los bienes o masas patrimoniales, y no a la mera declaración de nulidad de la institución hereditaria y apertura de la sucesión ab intestato del causante.

IV.- CUANTÍA

Cumpliendo lo prevenido en el art. 253.1 y 3 LEC, hacemos constar que la cuantía de esta demanda es indeterminada.

V.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VI.- REQUISITOS FORMALES

No aparecen, aparte de los requisitos genéricos de la demanda en juicio ordinario del art. 399 LEC, otros de carácter formal cuya falta, por el tipo de acción, invalidarían el proceso para pronunciarse sobre el fondo del asunto.

VII.- FONDO DEL ASUNTO

La preterición es la omisión del legitimario en el testamento, sin que éste haya recibido atribución alguna en concepto de legítima; en el presente caso, efectivamente, al hijo extramatrimonial del causante no se le menciona en el testamento (fue concebido y nació después de otorgado éste) ni nada recibió imputable a la legítima. La declaración de principio del art. 814 CCiv es clara: la preterición de un heredero forzoso (quiere decir legitimario) no perjudica la legítima, tras cuyo principio declara los efectos distinguiendo si la preterición es intencional o errónea (no intencional, la llama). La primera se produce cuando el testador no ha mencionado ni hecho atribución alguna al legitimario, sabiendo (intencionadamente) que éste existe; la segunda, cuando el testador omitió la mención del legitimario hijo o descendiente (no otro) porque ignoraba (erróneamente) su existencia.

Estos conceptos vienen referidos al testamento, no a la muerte. Es decir, que la preterición se produce si en el testamento se omite al legitimario, sin importar que en la apertura de la sucesión, producida por la muerte del causante, éste haya sabido o no de la existencia de aquél. No se tiene en cuenta la preterición al tiempo de la muerte, según conozca o no de la existencia del legitimario, sino al tiempo del testamento.

Por otro lado, desde la promulgación de la Constitución en 1978, todos los hijos ostentan los mismos derechos, sin posible discriminación en atención a que tengan o no la condición de matrimoniales, según se desprende de lo prevenido en los arts. 14 y 39 de dicha norma.

En consecuencia y de acuerdo con la normativa vigente, si cualquier progenitor omite hacer uso de la facultad que le concede el art. 662 CCiv respecto a la regulación del curso y destino de sus bienes, después de su fallecimiento, una vez acaecido éste, la herencia se repartirá a partes iguales entre sus hijos, ya sean matrimoniales, extramatrimoniales o adoptivos.

Por ello, quien realmente desee establecer alguna diferencia, debe otorgar testamento haciendo uso, en él, de las facultades de disposición que respecto a dos de los tercios de su haber hereditario le atribuyen los párrafos segundo y tercero del art. 808 CCiv.

Desde otro punto de vista, ha de afirmarse que resulta difícil interpretar un testamento teniendo en cuenta hechos que ocurren o actitudes que se adoptan o se omiten varios años después de su otorgamiento. Así, se presenta como inadmisible valorar la inactividad testamentaria de D./Dña. [NOMBRE Y APELLIDOS] entre el [FECHA] y el [FECHA] como producto de su deliberada voluntad de reducir a su hijo extramatrimonial a la legítima estricta que pudiera corresponderle, lo que convertiría en intencional su pretensión.

Muy al contrario, según pacífica doctrina, en el caso de que los hijos hayan nacido después de otorgado el testamento la no intencionalidad de su preterición en el mismo queda demostrada ex re ipsa. Conclusión que todavía se impone con mayor fuerza cuando, como aquí sucede, el momento de la concepción del hijo preterido es asimismo posterior a aquel otorgamiento.

En definitiva, ha de entenderse, siguiendo la doctrina jurisprudencial que plasma la STS de 23 de enero de 2001, Rec. 3506/1995, recaída en supuesto idéntico:

a) Que el causante no se hallaba animado de especiales intenciones en cuanto a su hijo extramatrimonial, en el momento de expresar su última voluntad ante el Notario autorizante de su único testamento. Simplemente, no podía presumir que llegase a producirse su nacimiento, por lo que la no referencia al mismo es lógica y su preterición debe ser calificada de no intencional.
b) Que la inactividad del causante respecto a llevar a cabo un nuevo otorgamiento tras el nacimiento y reconocimiento de su tercer hijo en el año [AÑO] no puede servir de elemento interpretativo respecto al contenido de la voluntad testamentaria expresada el

Por lo tanto, únicamente puede afirmarse que D./Dña. [NOMBRE Y APELLIDOS] -fuera o no conocedor de las consecuencias jurídicas de su conducta- se limitó a dejar las cosas como estaban y, pudiendo hacerlo, no volvió a testar al objeto de establecer diferencias en cuanto a las porciones hereditarias correspondientes a uno y otros hijos. Este silencio ha de interpretarse como conformidad de que se produjera el efecto que las leyes establecen para tales casos, que no es otro que el prevenido en el segundo párrafo, supuesto segundo del art. 814 CCiv.

Por otro lado, si bien es cierto que la voluntad del testador ha de considerarse como realmente relevante —así lo dispone el art. 675 CCiv— no lo es menos precisamente la concreta voluntad que el testador ha formado en atención a la realidad o a la situación que puede contemplar y valorar en el momento en que lleva a cabo el otorgamiento.

Si esa realidad se altera después de forma significativa y el testador omite otorgar nuevo testamento, revocando, modificando o adicionando el anterior, su voluntad y su intención dejan de ser relevantes por haber sido debidamente expresadas, y el intérprete ha de limitarse a la constatación del hecho omisivo o negativo y a la necesaria aplicación de los preceptos establecidos para dar solución a la inactividad del causante.

Desde jurisprudencia anciana se ha entendido que la preterición ha de resultar exclusivamente del testamento, por ser éste la expresión más solemne de quien dispone de sus bienes para después de su muerte evitando formular hipótesis sobre la posible causa de la omisión del heredero, ya que la presunta voluntad del causante carece de toda eficacia si no aparece del propio testamento.

Por consiguiente, ha de estarse al hecho de la omisión del hijo extramatrimonial, en el testamento del causante, cuyo otorgamiento anterior incluso a la concepción de [NOMBRE DEL MENOR], convierte a su preterición en no intencional, con la consecuencia práctica de que todos los hijos de D./Dña. [NOMBRE Y APELLIDOS] van a obtener la igualdad de trato que la Constitución propugna.

VIII.- COSTAS

Conforme al principio del art. 394.1 LEC, del vencimiento objetivo, las costas irrogadas a esta parte en el juicio declarativo en la primera instancia se han de pronunciar a cargo del demandado.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL

que teniendo por presentado este escrito, con sus copias y documentos que se acompañan, se sirva admitir uno y otros; en su virtud tener por interpuesta en la representación que ostento, la presente demanda de Juicio declarativo Ordinario contra D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS], quienes deberán ser emplazados a fin de que puedan contestar, si a su derecho les conviene, y previos los oportunos trámites legales, en su día dicte sentencia por la que se declare la nulidad de la institución hereditaria en el testamento de D./Dña. [NOMBRE Y APELLIDOS], declarándose abierta la sucesión ab intestato del causante, notificándose esta resolución al Registro General de Actos de Ultima Voluntad, con expresa imposición de las costas procesales al demandado que se oponga.

OTROSÍ DIGO: Que siendo general para pleitos el poder que presenta la Procurador/a suscrita, y precisándolo para otros usos.

Por lo expuesto,

AL TRIBUNAL SUPLICO

que, teniendo por hecha la afirmación anterior, se acuerde el desglose de la copia auténtica del poder para pleitos y la devolución a esta parte.

Es justicia de hacerse en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a
