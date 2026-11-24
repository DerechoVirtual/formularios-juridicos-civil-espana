---
name: demanda-juicio-ordinario-impugna-desheredacion-civ-0476
description: "Demanda de juicio ordinario que impugna la desheredación en el testamento. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio ordinario que impugna la desheredación en el testamento

> Formulario **CIV-0476** del plugin **Herencias, testamentos y donaciones** (`formularios-herencias-y-donaciones`) · Civil › Sucesiones y donaciones · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario en ejercicio de acción de nulidad de institución de heredero testamentario al no existir la causa de desheredación de malos tratos o injurias alegada por el causante.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio ordinario que impugna la desheredación en el testamento» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio ordinario que impugna la desheredación en el testamento” para mi caso». También puedes invocarla directamente con `/formularios-herencias-y-donaciones:demanda-juicio-ordinario-impugna-desheredacion-civ-0476`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-herencias-y-donaciones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Herencias, testamentos y donaciones) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (36 veces)
- [ ] LOCALIDAD (13 veces)
- [ ] FECHA (6 veces)
- [ ] DOMICILIO (4 veces)
- [ ] NÚMERO (4 veces)
- [ ] Nº (3 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] FINCA (2 veces)
- [ ] FOLIO (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] LIBRO (2 veces)
- [ ] SEDE (2 veces)
- [ ] TOMO (2 veces)
- [ ] CALLE
- [ ] CAUSA DE DESHEREDACIÓN
- [ ] CORREO ELECTRÓNICO
- [ ] EJERCICIO
- [ ] FECHA DE LA ESCRITURA
- [ ] FECHAS
- [ ] LUGAR
- [ ] Nº DE COLEGIADO/A
- [ ] Nº DE PROTOCOLO
- [ ] TELÉFONO

## Normas que cita el formulario

- art. 24.1 LEC
- art. 399.1 LEC
- art. 85.1 LOPJ
- art. 52.1 LEC
- art. 12 LEC
- art. 253.1 LEC
- art. 251 LEC
- art. 251.2.ª LEC
- art. 23 LEC
- art. 399 LEC
- art. 5 Ley Orgánica 1/2025
- art. 813 CC
- art. 853 CC
- art. 849 CC
- art. 853 Código Civil
- art. 850 CC
- art. 848 CC
- art. 851 CC
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
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: Un solo TI por partido judicial (art. 84.1 LOPJ): sobra «de los de». Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS] y de D./Dña. [NOMBRE Y APELLIDOS], con domicilios respectivamente en [DOMICILIO] y [DOMICILIO], representación que acredito mediante escritura de poder otorgada a mi favor (existen tres posibilidades para otorgar el apoderamiento al Procurador de los Tribunales, conforme dispone el art. 24.1 LEC)

[OPCIONAL — opción en función de cómo se haya otorgado el poder]

[ELEGIR UNA OPCIÓN: Si el poder se otorga a través de la sede judicial electrónica / Si el poder se otorga mediante comparecencia apud acta / Si el poder se otorga ante Notario]

bajo la dirección letrada de D./Dña [NOMBRE Y APELLIDOS], abogado/a en ejercicio, con despacho profesional abierto en [LOCALIDAD], colegiado nº [Nº DE COLEGIADO/A] del Ilustre Colegio de la Abogacía de [LOCALIDAD], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que mediante el presente escrito vengo a ejercitar ACCIÓN DE NULIDAD DE INSTITUCIÓN DE HEREDERO TESTAMENTARIO, del/la difunto/a D./Dña. [NOMBRE Y APELLIDOS], debiendo ser tenida como parte demandada D./Dña. [NOMBRE Y APELLIDOS], con domicilio, primero en [DOMICILIO]; y segundo, el domicilio laboral en [DOMICILIO]); con email [CORREO ELECTRÓNICO]; y con número de teléfono móvil [TELÉFONO]; todo ello de conformidad con los hechos y fundamentos de derecho que se especificarán.

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa, e, incluso, en una eventual fase de ejecución por medios telemáticos, en términos del art. 399.1 II LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y nº [Nº] de teléfono:

HECHOS

PRIMERO

Mis mandantes, D./Dña. [NOMBRE Y APELLIDOS] Y D./Dña. [NOMBRE Y APELLIDOS] son hijos matrimoniales de D./Dña. [NOMBRE Y APELLIDOS]

También es hija matrimonial, hermana de doble vínculo de los anteriores, D./Dña. [NOMBRE Y APELLIDOS]

Esta circunstancia se colige del testamento de D./Dña. [NOMBRE Y APELLIDOS], otorgado el [FECHA], ante el Notario de [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS], número de protocolo [Nº DE PROTOCOLO] (Documento n.º [Nº] de esta demanda), y si fuera negado de adverso, se hace expresa remisión a los libros del Registro Civil.

SEGUNDO

D./Dña. [NOMBRE Y APELLIDOS] otorgó testamento el [FECHA], al que se ha hecho referencia, y se acompaña como documento n.º [NÚMERO], mediante copia simple, remitiéndonos al protocolo del nominado fedatario público donde obra su original.

TERCERO

El testamento de referencia es el que rigió la sucesión de D./Dña. [NOMBRE Y APELLIDOS], conforme se acredita por el certificado expedido por el Registro de Actos de Última Voluntad, en la Dirección General de los Registros y del Notariado. Acompaño como Documento n.º dicha certificación.

D./Dña. [NOMBRE Y APELLIDOS], fue designada en dicho testamento heredera universal única de D./Dña. [NOMBRE Y APELLIDOS], que otorgó acta de aceptación y manifestación de herencia de fecha [FECHA], ante el Notario de [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS], con n.º [NÚMERO] de su protocolo, y que ha sido inscrita en el Registro de la Propiedad de [LOCALIDAD], a la finca [FINCA], folio [FOLIO], tomo [TOMO], libro [LIBRO] de [LOCALIDAD], inscripción

Se acompaña como Documento n.º [Nº], nota simple del asiento registral, en que aparece la referida acta notarial, señalando los libros y el protocolo del Notario para su adveración, de resultar precisa.

CUARTO

D./Dña. [NOMBRE Y APELLIDOS] falleció el día [FECHA] en [LOCALIDAD].

Acompaño como Documento n.º certificación literal de la defunción.

QUINTO

En el testamento de mérito, otorgado por D./Dña. [NOMBRE Y APELLIDOS] (cláusula segunda del Documento n.º [NÚMERO]) se indica genéricamente que ‘deshereda de su herencia a sus hijos D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS] por malos tratos o injurias [CAUSA DE DESHEREDACIÓN] ‘ sin hacer alguna mención más ni alegar las circunstancias que puedan evidenciarlas.

SEXTO

No existe causa legal de desheredación que recaiga sobre D./Dña. [NOMBRE Y APELLIDOS] y D./Dña.. [NOMBRE Y APELLIDOS]

SÉPTIMO

La parte actora manifiesta que, previo a la presentación de la presente demanda, se han llevado a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad, y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria; incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, mi representado envió un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por el demandado por el mismo medio, rechazando el acuerdo/ habiendo sido solo posible un acuerdo parcial, viéndonos en la necesidad de acudir a la presente vía judicial, respecto a los extremos de la controversia en los que se mantiene la discrepancia.

Acompaño como documento nº [Nº DE DOCUMENTO], el requerimiento efectuado y como documento nº [Nº DE DOCUMENTO], la contestación del demandado.

A estos hechos le son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA

Radicando la competencia genérica en el orden civil de la jurisdicción, detenta la competencia objetiva y funcional la Sección Civil del Tribunal de Instancia, por aplicación de lo dispuesto en los arts. 85.1 LOPJ y 45 LEC.

Conforme a lo dispuesto en el ordinal 4.º del art. 52.1 LEC es territorialmente competente el Tribunal de Instancia de [SEDE] por ser el del lugar donde la finada D./Dña. [NOMBRE Y APELLIDOS], tuvo su último domicilio.

II.- CAPACIDAD Y LEGITIMACIÓN

Tanto mis mandantes D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS], como la demandada D./Dña. [NOMBRE Y APELLIDOS], son personas físicas, mayores de edad, en pleno ejercicio de sus derechos civiles, por lo que tienen capacidad para ser parte y capacidad procesal ex arts. 6.1.1.º y 7.1 LEC.

Están legitimados activamente mis mandantes, en cuanto que hijos de la testadora y desheredados por ella, siendo pues titulares del derecho subjetivo hereditario legítimo, que ejercen en términos del art. 12 LEC, y como lo que se pretende es la anulación de la institución de heredera de la demandada, como única y universal, deberá ser tenida como parte legítima pasiva.

III.- PROCEDIMIENTO

La presente demanda deberá sustanciarse por las normas del juicio ordinario, a tenor de lo prevenido en los arts. 248 y 249.2 LEC, toda vez que el criterio de atribución preferente de la materia objeto del proceso resulta inaplicable, al carecer de especialidad típica la de éste, y cumplir entonces el criterio de cuantía, que rebasa con creces los quince mil euros.

IV.- CUANTÍA

Cumpliendo lo prevenido en el art. 253.1 LEC, hacemos constar que la cuantía de esta demanda es sólo relativamente determinable en [IMPORTE] euros, con arreglo a la regla 12.ª, en relación con la regla 3.ª.4.º del art. 251 LEC, puesto se trata de pleito relativo a una herencia siendo que, en definitiva, se pretende por el derecho a adquirir ‘ope legis’ una cuota de una masa de bienes y derechos, de entre los que se identifica como prácticamente el que absorbe todo el valor de la herencia, la vivienda sita en [LOCALIDAD], calle [CALLE], n.º [NÚMERO], que es finca [FINCA], al folio [FOLIO], tomo [TOMO], libro [LIBRO] de [LOCALIDAD], inscrita en el Registro de la Propiedad de [LOCALIDAD], y su valor catastral -utilizando el criterio subsidiario del art. 251.2.ª LEC- asciende a [IMPORTE] euros.

Se aportan nota simple de la inscripción registral, en que aparece la titularidad, que es el Documento n.º 3 de la demanda, y copia del recibo del Impuesto sobre Bienes Inmuebles del ejercicio [EJERCICIO], como Documento n.º [Nº DE DOCUMENTO].

V.- POSTULACIÓN Y DEFENSA

Conforme a los arts. 23 y 31 LEC se formula esta demanda por medio de Procurador/a de los Tribunales con poder para este pleito, que se conferirá ante el Letrado de la Administración de Justicia, y con dirección y firma de Letrado habilitado ante el Tribunal.

Asimismo se cumplen los requisitos formales del art. 399 LEC.

VI.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VII.- FONDO DE LA CUESTIÓN CONTROVERTIDA

El art. 813 CCiv prevé que "el testador no podrá privar a los herederos de su legítima sino en los casos expresamente determinados por la Ley" e, igualmente, el artículo 848 señala que "la desheredación sólo podrá tener lugar por alguna de las causas que expresamente señala la Ley", siendo para los descendientes las contempladas en el art. 853 CCiv, que se refiere a la negación de alimentos al padre o ascendiente que deshereda, y el maltrato de obra o la injuria grave de palabra al mismo, además de las causas de indignidad contempladas en los números 2.º, 3.º, 5.º y 6.º del artículo 756 del referido Código. Pero, además, la Jurisprudencia ha mantenido el carácter absolutamente restrictivo con que deben aplicarse las causas de desheredación que contempla la ley [STS de 14 de marzo de 1.994 ], no admitiéndose la analogía, ni la interpretación extensiva, ni siquiera la argumentación de "minoris ad maiorem" [STS de 28 de junio de 1.993 ], exigiéndose, para que tenga efecto tal desheredación, conforme a los artículos 849 y 850 CCiv, que se exprese en el testamento la causa legal en la que se funde, que dicha causa sea una de las que contempla la ley, y que los herederos del testador prueben la certeza de la causa de la desheredación si los desheredados la negaren.

Aunque la ley no impone al testador describir los hechos que constituyen la causa de desheredación, lo que sí le impone es que exprese una de las causas previstas en la ley. El Tribunal Supremo, ya desde la antigua sentencia de fecha cuatro de noviembre de mil novecientos cuatro, y con referencia a la causa de desheredación contenida en el apartado segundo del art. 853 del Código Civil establece que no es preciso que el testador determine el hecho concreto constitutivo de la desheredación aunque sí la causa; por cuanto su certeza puede ser contradicha, y debe en este caso probarse en juicio para que la desheredación sea válida y eficaz en perjuicio del desheredado.

La cuestión radica entonces en determinar si concurre o no la causa de desheredación invocada y a quién corresponde la prueba de la misma. A juicio de esta representación, la cuestión resulta clara:

"La prueba de ser cierta la causa de la desheredación corresponderá a los herederos del testador si el desheredado la negare" (art. 850 CCiv)

El tenor literal de la norma es claro y el mismo ha sido confirmado por una abundante jurisprudencia del Tribunal Supremo [SSTS de 15 de junio de 1990 y 10 de junio de 1988 ]. Por lo demás, es conforme con las reglas que rigen la carga de la prueba; la prueba de la desheredación recaerá sobre los herederos y legatarios eventuales demandados, entre otras razones, porque hacerla recaer sobre los hijos demandantes supondría forzarles a probar un hecho negativo: la no concurrencia de los hechos constitutivos de la causa de desheredación.

Sobre esta cuestión, parece sumamente interesante traer a colación la precitada STS de 28 de junio de 1993, en la que se declaró que las alusiones genéricas referidas a injurias o insultos no pueden tenerse en cuenta a los fines de su encaje en el art. 853.2.ª dada su falta de justificación suficiente, y mucho más cuando ha de imponerse una interpretación restrictiva de la institución de la desheredación que no sólo proclama el art. 848 CCiv sino también la abundante jurisprudencia orientada en defensa de la sucesión legitimaria, y continúa afirmando dicha resolución que la falta de relación afectiva y comunicación entre la hija y el padre, el abandono sentimental sufrido por éste durante la última enfermedad, la ausencia de interés de la hija en relación con los problemas del padre, etc. son circunstancias que, de ser ciertas, corresponden al campo de la moral escapan a la valoración jurídica y en definitiva sólo están sometidas al Tribunal de la conciencia.

La Jurisprudencia tiene declarado que solo las condenas dictadas por órgano Jurisdiccional penal hacen prueba de la causa de desheredación, debiendo constar la misma en forma concreta y específica, según determinaba la STS de 15 de junio de 1.990, no admitiéndose la simple referencia genérica a maltrato de obra o a la existencia de injuria grave, de tal forma que las palabras ofensivas o irrespetuosas no son suficientes si no quedan especificadas o relacionadas para poder apreciar la necesaria existencia de los malos tratos de obra o de injurias graves, sino también la gravedad de estas últimas.

Los desheredados ni maltrataron de obra ni injuriaron de palabra a la madre, y no demostrada la causa de la desheredación (art. 850 CCiv) por la parte a quien le incumbe, la consecuencia aparece claramente establecida en la ley:

"La desheredación hecha sin expresión de causa, o por causa cuya certeza, si fuere contradicha, no se probare, o que no sea una de las señaladas en los cuatro siguientes artículos, anulará la institución de heredero en cuanto perjudique al desheredado; pero valdrán los legados, mejoras y demás disposiciones testamentarias en lo que no perjudiquen a dicha legítima" (art. 851 CCiv)

La anulación de institución de heredero se limita ‘en cuanto perjudique al desheredado’, valiendo las disposiciones testamentarias en lo que no perjudiquen dicha legítima; significará que al hijo heredero forzoso se le debe restituir su legítima estricta, y no la mejora, en cuanto que de ésta puede disponer el testador entre cualesquiera de los restantes descendientes (art. 808, párrafo 2.º, en relación con 823 CCiv).

VIII.- COSTAS

Se deben imponer a la parte demandada, por el criterio del vencimiento que establece para los declarativos en la instancia el art. 394.1 LEC.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito, se digne admitirlo, junto con sus documentos, y por comparecido a quien postula en la representación procesal que se le confiere haber por deducida, en calidad de parte actora, se entiendan conmigo todas las diligencias a partir de este momento, y se incoe JUICIO ORDINARIO por DEMANDA DE NULIDAD DE INSTITUCIÓN DE HEREDERO TESTAMENTARIO, dé traslado de la demanda a D./Dña. [NOMBRE Y APELLIDOS] para que la conteste, si a su derecho le conviene, reciba el pleito a prueba, y dicte en su día Sentencia por la que:

1.- Declare inexistente la causa de desheredación prevista en la Cláusula Segunda del testamento otorgado por D./Dña. [NOMBRE Y APELLIDOS] ante el Notario de [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS], y que causó el númerode su protocolo y, en consecuencia, se declare que D./DÑA. [NOMBRE Y APELLIDOS] y D./DÑAhan sido injustamente desheredados por la testadora
2.- Declare la nulidad de la institución de heredera contenida en dicho testamento a favor de D./Dña. [NOMBRE Y APELLIDOS] en lo que perjudique la legítima de D./DÑA. [NOMBRE Y APELLIDOS] y D./DÑA, que los mismos tienen derecho a percibir.
3.- Reduzca la institución de heredero del testamento de D./Dña. [NOMBRE Y APELLIDOS] el, ante el Notario de [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS], y que causó el númerode su protocolo, en lo que represente el valor de una novena parte del haber hereditario que corresponde como legítima estricta a D./DÑA, y de otra novena parte que corresponde por el mismo título a D./DÑA..
4.- Declare la nulidad de la escritura pública de fecha [FECHA DE LA ESCRITURA], autorizada por el Notario de [LOCALIDAD]

D./Dña.(n.ºde su protocolo), por la que, con base en el testamento, aceptó la herencia D./Dña. [NOMBRE Y APELLIDOS] y se adjudicó todos los bienes, derechos y acciones integrantes de dicha herencia, debiendo cancelarse, asimismo, la inscripción que dicha adjudicación causó en el Registro de la Propiedad de
5.- Condene a la demandada a estar y pasar por las anteriores declaraciones que correspondan, a todos sus pertinentes efectos, y
6.- Condene a la demandada al reintegro de las costas procesales causadas a la parte actora por la demandada.

Es justicia de hacerse en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a
