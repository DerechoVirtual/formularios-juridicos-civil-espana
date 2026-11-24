---
name: demanda-juicio-ordinario-extinguir-adopcion-civ-0361
description: "Demanda de juicio ordinario para extinguir una adopción. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio ordinario para extinguir una adopción

> Formulario **CIV-0361** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario por la que el progenitor biológico que, sin culpa suya, no intervino ni prestó su asentimiento en el expediente de adopción de su hijo menor por un tercero (pareja de la madre) solicita la extinción de la adopción (art. 180.2 del Código Civil), con restitución de los apellidos.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio ordinario para extinguir una adopción» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio ordinario para extinguir una adopción” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-juicio-ordinario-extinguir-adopcion-civ-0361`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (7 veces)
- [ ] NOMBRE Y APELLIDOS DE LA MADRE (7 veces)
- [ ] FECHA (6 veces)
- [ ] CALLE, NÚMERO, LOCALIDAD (4 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] NOMBRE Y APELLIDOS DEL ACTOR (4 veces)
- [ ] NOMBRE Y APELLIDOS DEL ADOPTANTE (4 veces)
- [ ] AÑO (3 veces)
- [ ] DÍA (3 veces)
- [ ] MES (3 veces)
- [ ] Nº (3 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] CALLE (2 veces)
- [ ] CORREO ELECTRÓNICO (2 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] NOMBRE DEL MENOR (2 veces)
- [ ] Nº DE TELÉFONO (2 veces)
- [ ] PAÍS (2 veces)
- [ ] SEDE (2 veces)
- [ ] APELLIDOS
- [ ] DENOMINACIÓN DEL GRUPO
- [ ] DOMICILIO
- [ ] DOMICILIO EN EL EXTRANJERO
- [ ] NOMBRE DEL NOTARIO
- [ ] Nº DE COLEGIADO
- [ ] Nº DE EXPEDIENTE
- [ ] PUESTO

## Normas que cita el formulario

- art. 24.1 LEC
- art. 399.1 LEC
- art. 779 LEC
- art. 50 LEC
- art. 180.2 CC
- art. 177 CC
- art. 6.1.6.º LEC
- art. 541 LOPJ
- art. 40.1 LJV
- art. 180 CC
- art. 249.2 LEC
- art. 23 LEC
- art. 399 LEC
- art. 394 LEC
- art. 24.2 LEC
- art. 155.3 LEC

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

- Al principio del formulario: formulario adaptado a la reforma procesal de la LO 1/2025. Comprobar la redacción vigente de los arts. 177 y 180 del Código Civil tras la Ley 26/2015 (asentimiento de los progenitores, legitimación y plazo de caducidad para pedir la extinción) y el precepto exacto del art. 5.2 de la LO 1/2025 que excluye esta materia del requisito de procedibilidad, pues el original citaba el art. 4.1 II.
- Junto a «…MILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.

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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]

Q.P.T.C.

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS DEL ACTOR], con domicilio en [CALLE, NÚMERO, LOCALIDAD], representación que acredito mediante poder otorgado a mi favor (existen tres posibilidades para otorgar el apoderamiento al Procurador de los Tribunales, conforme dispone el art. 24.1 LEC) (1):

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— (Si el poder se otorga a través de la sede judicial electrónica) mediante comparecencia electrónica, a través de la sede judicial electrónica e inscrito en el Registro Electrónico de Apoderamientos Judiciales; y a cuya justificación acompaño certificación de dicho Registro aportada como documento n.º [Nº DE DOCUMENTO], y que se puede acreditar mediante consulta automatizada orientada al dato, por parte del órgano judicial al cual tengo el honor de dirigirme.

— (Si el poder se otorga mediante comparecencia apud acta) mediante comparecencia personal apud acta ante el Tribunal Decano de [LOCALIDAD], posteriormente inscrito en el Registro Electrónico de Apoderamientos Judiciales; y a cuya justificación acompaño certificación de dicho Registro aportada como documento n.º [Nº DE DOCUMENTO], y que se puede acreditar mediante consulta automatizada orientada al dato, por parte del órgano judicial al cual tengo el honor de dirigirme.

— (Si el poder se otorga ante Notario) mediante escritura de poder otorgada a mi favor, ante el Notario/Notaria [NOMBRE DEL NOTARIO], con Notaría sita en [LOCALIDAD]. El poder se inscribió en el Registro Electrónico de Apoderamientos Judiciales; lo cual justifico mediante certificación de dicho Registro aportada como documento n.º [Nº DE DOCUMENTO], y que se puede acreditar mediante consulta automatizada orientada al dato, por parte del órgano judicial al cual tengo el honor de dirigirme.

bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS], abogado/a en ejercicio, con despacho profesional abierto en [CALLE, NÚMERO, LOCALIDAD], colegiado n.º [Nº DE COLEGIADO] del Ilustre Colegio de la Abogacía de [LOCALIDAD], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que mediante el presente escrito vengo a formular demanda de juicio ordinario para la extinción de la adopción del hijo de mi mandante llevada a efecto por D./Dña. [NOMBRE Y APELLIDOS DEL ADOPTANTE], con domicilio (2), primero en [CALLE, NÚMERO, LOCALIDAD]

[OPCIONAL — incluir si procede]

y segundo, el domicilio laboral en [CALLE, NÚMERO, LOCALIDAD];

con (3) email [CORREO ELECTRÓNICO] y con número de teléfono móvil [Nº DE TELÉFONO]; y por D./Dña. [NOMBRE Y APELLIDOS DE LA MADRE] con el mismo domicilio; todo ello de conformidad con los hechos y fundamentos de derecho que se especificarán.

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa, e, incluso, en una eventual fase de ejecución, por medios telemáticos, en términos del art. 399.1 II LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y n.º de teléfono: [CORREO ELECTRÓNICO] / [Nº DE TELÉFONO].

HECHOS

PRIMERO.- Mi patrocinado y D./Dña. [NOMBRE Y APELLIDOS DE LA MADRE] se conocieron en [LOCALIDAD], entablándose entre ellos una relación sentimental semejante a la de los casados, que arrancó desde [FECHA] hasta [FECHA], cuando, por divergencias surgidas entre ambos, se puso fin a la misma, habiendo convivido en relación afectiva semejante a la de las parejas casadas en la vivienda sita en calle [CALLE] n.º [Nº] de [LOCALIDAD].

SEGUNDO.- De dicha unión sentimental nació con fecha [DÍA] de [MES] de [AÑO] un hijo extramatrimonial de nombre [NOMBRE DEL MENOR], que fue inscrito en el Registro Civil de [LOCALIDAD], reconocido por el padre dentro del plazo de práctica de la inscripción, habiendo quedado por tanto perfectamente determinada la filiación paterna y materna, según se demuestra con la certificación que se acompaña como documento número 1.

TERCERO.- La separación de la unión de hecho referida se produjo de manera civilizada, y D./Dña. [NOMBRE Y APELLIDOS DE LA MADRE] pasó a residir con su hijo menor en el domicilio de los padres de ésta sito en [DOMICILIO], donde también residen los padres de mi representado, pactándose que quedara la madre con la guarda y custodia, dadas las exigencias de trabajo de mi mandante, que hubo de trasladarse a [PAÍS] para ocuparse de la dirección administrativa y contable de las empresas del Grupo [DENOMINACIÓN DEL GRUPO] en dicho país, del cual forma parte [DENOMINACIÓN SOCIAL], compañía para la cual presta sus servicios desde [FECHA].

D./Dña. [NOMBRE Y APELLIDOS DEL ACTOR] ha desempeñado dicha función desde [FECHA] a [FECHA], fijando su residencia en la vivienda sita en [DOMICILIO EN EL EXTRANJERO], donde ha residido hasta la actualidad, habiéndose cumplido sin problemas un régimen de prestación de alimentos a cargo del progenitor no custodio.

La comunicación de padre con el hijo ha sido constante en lo que permite la crianza del menor y el trabajo de D./Dña. [NOMBRE Y APELLIDOS DEL ACTOR], regresando éste todos los veranos al domicilio de sus padres, y aprovechando los períodos vacacionales para relacionarse con su hijo.

CUARTO.- Sin embargo, desde [FECHA] la madre estableció una relación con otro hombre, y tanto aquélla como su familia fueron paulatinamente poniendo trabas a las visitas de mi poderdante, alegando actividades extraescolares que menguaban el tiempo libre del menor, y negando la posibilidad de pernocta del menor con el padre, aduciendo pretextadas razones de salud, pese a todo lo cual la comunicación con el menor no se ha interrumpido en ningún momento.

QUINTO.- El pasado día [DÍA] de [MES] de [AÑO], se comunicó a mi representado que se presentara en España, y se le notificó la decisión de reincorporarle al nuevo centro de la empresa [DENOMINACIÓN SOCIAL] ubicado en la calle [CALLE] de esta localidad, concretamente en el puesto de trabajo de nueva creación de [PUESTO], encontrándose entonces con el desolador panorama de que, durante su ausencia, D./Dña. [NOMBRE Y APELLIDOS DEL ADOPTANTE] —que había contraído matrimonio con D./Dña. [NOMBRE Y APELLIDOS DE LA MADRE]— tras instar un expediente para adoptar al hijo de mi representado, había obtenido el auto constitutivo de la adopción, encontrándose inscrito el adoptado con los apellidos [APELLIDOS]. Se aporta como documento número dos certificación registral donde consta la inscripción marginal de la adopción, dejando designados a efectos probatorios los archivos del Tribunal de Instancia n.º [Nº] de [SEDE], donde se tramitó el expediente de adopción n.º [Nº DE EXPEDIENTE].

SEXTO.- Que a pesar de ser perfectamente conocido por D./Dña. [NOMBRE Y APELLIDOS DE LA MADRE] el domicilio en [PAÍS] de mi representado, como lo demuestran las cartas remitidas a D./Dña. [NOMBRE Y APELLIDOS DEL ACTOR] recientemente (documentos [Nº]), e incluso el domicilio de los padres de mi representado en la misma población donde reside, se ocultaron al Tribunal estos datos para conseguir que, a través de la citación edictal en el Boletín Oficial de la provincia, se constituyese la adopción del hijo de mi representado, sin que pudiese intervenir en el expediente, tal y como es preceptivo, lo que motiva la impugnación de la adopción.

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA.

Radicando la competencia genérica en el orden civil de la jurisdicción, detenta la competencia objetiva y funcional la Sección Civil del Tribunal de Instancia, por aplicación de lo dispuesto en la Disposición adicional 2.ª de la Ley 21/1987, de 11 de noviembre. Resulta territorialmente competente el Tribunal al que me dirijo, conforme al art. 779 LEC, puesto que es el del partido del lugar donde tiene su domicilio el adoptante, es decir, el demandado —coincidiendo con el fuero general establecido en el art. 50 LEC—.

II.- LEGITIMACIÓN.

Conforme a lo dispuesto en el art. 180.2 CC, está legitimado activamente cualquiera de los progenitores que, sin culpa suya, no hubiese intervenido en el expediente de adopción en los términos expresados en el art. 177 CC. Pasivamente, lo está D./Dña. [NOMBRE Y APELLIDOS DEL ADOPTANTE], al ser el adoptante del hijo de mi representado.

Al haber intervenido en el proceso de constitución de la adopción el otro progenitor, D./Dña. [NOMBRE Y APELLIDOS DE LA MADRE], ésta deberá intervenir en el proceso como demandada, por haber participado en el acto que se impugna.

Tiene legitimación pasiva, extraordinaria por interés público, el Ministerio Fiscal, puesto que se postula llevar a cabo una rectificación del Registro Civil, y así, la demanda debe dirigirse necesariamente contra el Ministerio Fiscal, actuando en defensa de la legalidad.

III.- CAPACIDAD Y REPRESENTACIÓN.

Tanto mi mandante como los demandados son personas físicas en pleno ejercicio de sus derechos civiles, como lo son los mayores de edad sin medidas de apoyo judiciales que afecten a su capacidad, por lo que tienen capacidad para ser parte y capacidad procesal ex arts. 6.1.1.º y 7.1 LEC.

El Ministerio Fiscal tiene capacidad para ser parte en los procesos civiles en armonía con el art. 6.1.6.º LEC, de modo que ostenta capacidad procesal, sin tener que intermediarse sus individuos con otros profesionales del Derecho, cuando está prevista su intervención legalmente, en defensa de la legalidad y del interés público tutelado por la Ley, por tratarse de materia propia del estado civil (art. 124 CE, art. 541 LOPJ y art. 3.6 EOMF).

IV.- PROCEDIMIENTO.

El art. 40.1 LJV se remite al juicio declarativo que corresponda, para las actuaciones judiciales de extinción de la adopción por la impugnación de los padres naturales recogida en el art. 180 CC, por lo que, no existiendo disposición expresa en contrario, y debido a la imposibilidad de fijar una cuantía, conforme a la regla del artículo 249.2 LEC, el proceso deberá seguirse por los trámites del juicio declarativo ordinario.

V.- POSTULACIÓN.

Conforme a los arts. 23 y 31 LEC se formula esta demanda por medio de Procurador/a de los Tribunales con poder para pleitos, y con dirección y firma de Letrado ejerciente habilitado ante el Tribunal, cumpliéndose los requisitos formales del art. 399 LEC.

VI.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda no está sujeta al previo intento de resolución de controversias en vía no jurisdiccional por tratarse de materias excluidas del requisito de procedibilidad de acuerdo con la LO 1/2025 (art. 4.1 II según el original; comprobar el art. 5.2), atendiendo a la materia de orden público de las cuestiones relativas a los menores de edad.

VII.- FONDO DE LA CUESTIÓN CONTROVERTIDA.

Se solicita la extinción de la adopción por resolución judicial, mediante el ejercicio de la acción de impugnación que se concreta en el art. 180.2 CC, conforme al cual «el Juez acordará la extinción de la adopción a petición de cualquiera de los progenitores que, sin culpa suya, no hubieren intervenido en el expediente en los términos expresados en el artículo 177», que dispone que deberán asentir a la adopción los progenitores del adoptando que no se hallare emancipado, a menos que estuvieran privados de la patria potestad por sentencia firme o incursos en causa legal para tal privación, siendo que el padre impugnante no intervino ni prestó el asentimiento para la adopción, por causa no imputable a él, pues tanto la madre biológica como el adoptante conocían su paradero.

No hay perjuicio grave para el menor teniendo en cuenta el poco tiempo que lleva el adoptado viviendo con la familia adoptiva y el escaso o nulo grado de integración que puede haber alcanzado con su padre adoptivo. No existe razón para alterar el régimen filial del menor, constituyendo una nueva relación familiar que extingue los vínculos con la familia anterior, y es la extinción de la adopción la solución más estable y justa para el menor, cuyos intereses deben primar frente a los otros que puedan estar en juego.

La demanda se interpone dentro del plazo de caducidad que prevé el art. 180.2 CC, siendo el dies «a quo» de dicho plazo aquel en que quedó constituida la adopción.

VIII.- COSTAS.

Conforme al artículo 394 LEC las costas han de imponerse a los demandados, si se oponen y resultan vencidos.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que, habiendo por presentado este escrito de demanda con los documentos que lo acompañan y copias de uno y otros, se digne admitirlos y tenga por comparecido y parte a mi representado, y por promovido juicio ordinario frente a D./Dña. [NOMBRE Y APELLIDOS DEL ADOPTANTE] y D./Dña. [NOMBRE Y APELLIDOS DE LA MADRE], y disponga darles traslado para que, siendo de su interés, comparezcan y la contesten, y seguido que sea todo el pertinente procedimiento, con citación del Ministerio Fiscal, se dicte en su día sentencia por la que estimando la demanda, se declare la extinción de la adopción del menor [NOMBRE DEL MENOR], y como consecuencia de ello, la restitución de los apellidos que ostentaba su hijo conforme a su filiación biológica, y todo ello con expresa imposición de costas a los demandados.

Es justicia de hacerse en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a: [NOMBRE Y APELLIDOS] | Firma del Procurador/a: [NOMBRE Y APELLIDOS]

NOTA (1): A la hora de su acreditación, todos los poderes deben estar inscritos en el Registro Electrónico de Apoderamientos Judiciales (REAJ). Se supone que, para su acreditación, basta con la consulta automatizada orientada al dato de dicho Registro, algo que está a disposición de cualquier Letrado de la Administración de Justicia. Sin embargo, dado que el art. 24.2 LEC configura la certificación de dicha inscripción como vía subsidiaria de acreditación, para el caso de que el sistema no permita aquella consulta automatizada, se señala en el modelo que se acompaña certificación electrónica. El sistema permite emitir dicha certificación para quien inscribe el poder.

NOTA (2): El art. 155.3 LEC permite expresar varios domicilios del demandado (el que aparezca en el padrón municipal o conste oficialmente a estos efectos; el que aparezca en registro oficial o en publicaciones de colegios profesionales, si se trata de empresas o personas colegiadas; donde desarrolle su actividad profesional o laboral no ocasional; si es empresa mercantil, el domicilio de cualquiera de sus administradores, gerentes o apoderados; o, si es asociación que consta en registro oficial, el domicilio del presidente, miembro o gestor de la Junta correspondiente). Cuando se señalen varios, indicará el orden a seguir para la notificación, con vistas al éxito de la misma.

NOTA (3): El art. 155.3 LEC configura una obligación adicional del demandante, consistente en aportar cuantos datos sean de utilidad para localizar al demandado: número de identificación fiscal o de extranjeros, n.º de teléfono o de fax, dirección de correo electrónico, o similares.
