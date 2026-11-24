---
name: demanda-juicio-verbal-sobre-comunicacion-visitas-civ-0359
description: "Demanda de juicio verbal sobre comunicación y visitas de los abuelos con su nieto menor. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio verbal sobre comunicación y visitas de los abuelos con su nieto menor

> Formulario **CIV-0359** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio verbal sobre derecho de comunicación y visita de los abuelos respecto de su nieto menor.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio verbal sobre comunicación y visitas de los abuelos con su nieto menor» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio verbal sobre comunicación y visitas de los abuelos con su nieto menor” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-juicio-verbal-sobre-comunicacion-visitas-civ-0359`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (16 veces)
- [ ] LOCALIDAD (8 veces)
- [ ] NÚMERO (5 veces)
- [ ] NOMBRE DEL MENOR (4 veces)
- [ ] AÑO (3 veces)
- [ ] FECHA (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] Nº (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] SEDE (2 veces)
- [ ] CALLE
- [ ] CORREO ELECTRÓNICO
- [ ] LUGAR
- [ ] MES
- [ ] Nº DE COLEGIADO/A
- [ ] PROVINCIA
- [ ] TELÉFONO
- [ ] TIPO DE ACCIÓN
- [ ] TIPO Y Nº DE PROCEDIMIENTO

## Normas que cita el formulario

- art. 24.1 LEC
- art. 437.1 LEC
- art. 85.1 LOPJ
- art. 45 LEC
- art. 50.1 LEC
- art. 749.2 LEC
- art. 250.1.13.º LEC
- art. 2.º Ley 42/2003
- art. 23 LEC
- art. 5 Ley Orgánica 1/2025
- art. 160 CC
- art. 160.2 CC
- art. 94 CC
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

### Avisos de actualización (3) — se aplican en el texto, nunca se copian en el documento

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: Un solo TI por partido judicial (art. 84.1 LOPJ): sobra «de los de». Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).
- Junto a «…que conoció la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.C.

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], representación que acredito mediante escritura de poder otorgada a mi favor (existen tres posibilidades para otorgar el apoderamiento al Procurador de los Tribunales, conforme dispone el art. 24.1 LEC)

[OPCIONAL — opción en función de cómo se haya otorgado el poder]

[ELEGIR UNA OPCIÓN: Si el poder se otorga a través de la sede judicial electrónica / Si el poder se otorga mediante comparecencia apud acta / Si el poder se otorga ante Notario]

bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS], abogado/a en ejercicio, con despacho profesional abierto en [LOCALIDAD], colegiado nº [Nº DE COLEGIADO/A] del Ilustre Colegio de la Abogacía de [LOCALIDAD], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que mediante el presente escrito vengo a formular DEMANDA DE JUICIO VERBAL SOBRE DERECHO DE COMUNICACIÓN Y VISITA DE LOS ABUELOS RESPECTO DE SU NIETO MENOR, contra D./Dña. [NOMBRE Y APELLIDOS], con domicilio, primero en [DOMICILIO]; y segundo, el domicilio laboral en [DOMICILIO]); con email [CORREO ELECTRÓNICO]; y con número de teléfono móvil [TELÉFONO]; debiéndose cursar traslado al Ministerio Fiscal, al venir interesado un menor; en ejercicio de la acción de [TIPO DE ACCIÓN].

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa, e, incluso, en una eventual fase de ejecución por medios telemáticos, en términos del art. 399.1 II con relación al art. 437.1, ambos LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y nº [Nº] de teléfono:

Sirvan a la presente demanda los siguientes:

HECHOS

PRIMERO.- Mis patrocinados son padres comunes matrimoniales de D./Dña. [NOMBRE Y APELLIDOS], según acreditan mediante certificaciones en extracto de matrimonio, y de nacimiento de dicho hijo, que se aportan como documentos números [Nº DE DOCUMENTO] y [Nº DE DOCUMENTO].

SEGUNDO.- D./Dña. [NOMBRE Y APELLIDOS], y la hoy demandada D./Dña. [NOMBRE Y APELLIDOS], se conocieron en [LOCALIDAD], aproximadamente en el otoño del año [AÑO], entablándose entre ellos una relación sentimental que desembocó en una situación de convivencia que se prolongó hasta el mes de [MES] de [AÑO], cuando, por divergencias surgidas entre ambos, se puso fin a la misma.

Se aporta certificación censal del Ayuntamiento de [LOCALIDAD], acerca de los dos convivientes en la vivienda sita en calle [CALLE], como documento n.º [NÚMERO].

TERCERO.- De la relación entre D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS] nació un hijo, de nombre [NOMBRE DEL MENOR], el cual fue inscrito en el Registro Civil de [LOCALIDAD], reconocido por el padre dentro del plazo de práctica de la inscripción, conforme se demuestra con la certificación literal de nacimiento que se acompaña como documento n.º [NÚMERO].

CUARTO.- La separación de la unión de hecho referida dio lugar a que la hoy demandada pasara a residir con su hijo menor [NOMBRE DEL MENOR] en [LOCALIDAD], donde se dirige la presente, y formulara pretensión la madre de retener la guarda y custodia del hijo común, así como solicitud de alimentos a cargo del padre, que dio lugar a juicio verbal n.º [NÚMERO]/[AÑO], de que conoció la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº] [TIPO Y Nº DE PROCEDIMIENTO], en que recayó sentencia de fecha [FECHA], cuya copia se adjunta haciendo documento n.º [NÚMERO].

Dicha sentencia se halla en fase de ejecución forzosa.

QUINTO.- La comunicación de padre con el hijo habido con la demandada no ha podido ser constante, en un principio por la ruptura a tierna edad del menor, luego por los avatares del conflicto sobre prestaciones alimenticias, y al final, por motivos del trabajo del padre D./Dña. [NOMBRE Y APELLIDOS], que presta servicios en una empresa de montajes metálicos, y fue trasladado a la provincia de [PROVINCIA].

Con independencia de ello, la madre ha restringido al máximo las visitas a su nieto de mis mandantes, que residen en esta misma población, primero alegando problemas de salud del menor, y una vez ingresado en una guardería, diversas actividades que reducían el tiempo libre fuera del horario de ésta, y negando en todo momento la posibilidad de llevarse el niño a casa de los abuelos.

Desde que la demandada ha pasado a convivir con otro varón, ha prohibido todo acercamiento a su nieto por los demandantes.

SEXTO.- No han tenido fruto ninguno de los intentos pacíficos de conseguir un acuerdo por mis poderdantes sobre régimen de las visitas a su nieto [NOMBRE DEL MENOR], alegándose el incumplimiento de las aportaciones alimenticias, que no son obligación de mis mandantes, y a pesar de que éstos tienen comprometido un esfuerzo económico, dentro de sus escasos posibles, para el sostenimiento y educación del menor.

Para demostrarlo, se acompaña testimonio del acto de conciliación sin avenencia, que se celebró en fecha [FECHA], ante el Juez de Paz de [LOCALIDAD], a los efectos de cumplir el requisito de procedibilidad para la iniciación de la vía jurisdiccional, que es documento n.º [NÚMERO].

A los anteriores hechos, son aplicables los siguientes

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA.

Correspondiendo la competencia genérica sobre cuestiones de estado al orden civil de la jurisdicción, detenta la competencia objetiva y funcional la Sección Civil del Tribunal de Instancia que por reparto corresponda, por aplicación de lo dispuesto en el art. 85.1 LOPJ y art. 45 LEC, y puesto que no está prevenido un fuero preceptivo específico, resulta territorialmente competente el Tribunal a que me dirijo, puesto que es el del partido del lugar donde tiene su domicilio la demandada, que es el fuero general de las personas físicas ex art. 50.1 LEC.

II.- CAPACIDAD Y LEGITIMACIÓN.

Tanto mis mandantes como la demandada son personas físicas en pleno ejercicio de sus derechos civiles, mayores de edad que no están incapacitados, por lo que tienen capacidad para ser parte y capacidad procesal ex arts. 6.1.1.º y 7.1 LEC.

Corresponde la legitimación activa a mis mandantes por encontrarse en la determinada situación jurídica de parentesco con [NOMBRE DEL MENOR], como sus abuelos, y la legitimación pasiva corresponde a la demandada D./Dña. [NOMBRE Y APELLIDOS], puesto que es quien ostenta la guarda de su hijo en potestad, quien es el nieto, la cual no puede impedir el ejercicio del derecho de relación, mediante comunicación y visitas, como viene haciendo, y justifica impetrar tutela judicial.

Tiene intervención adhesiva de carácter preceptivo el Ministerio Fiscal de conformidad con art. 749.2 LEC, a quien se deberá conceder traslado como impera el art. 753.

III.- PROCEDIMIENTO.

La presente demanda deberá sustanciarse por las normas del juicio verbal con cauce especial del capítulo I del Título I del Libro IV LEC, de conformidad con el art. 250.1.13.º LEC, que introdujo —con la referencia al ordinal 12.º— el art. 2.º de la Ley 42/2003, de 21 de noviembre, de modificación del Código Civil y de la Ley de Enjuiciamiento Civil en materia de relaciones familiares de los nietos con los abuelos, siendo finalmente retocado con la reforma de la Ley 13/2009 de 3 de noviembre.

IV.- POSTULACIÓN.

Conforme a los arts. 23 y 31 LEC se formula esta demanda por medio de Procurador de los Tribunales con poder notarial para pleitos, y con dirección y firma de Letrado ejerciente habilitado ante el tribunal.

V.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VI.- FONDO DE LA CUESTIÓN CONTROVERTIDA.

Después de que el art. 160 CCiv, en su versión desde la Ley 21/1987 de 11 de noviembre, estipulara el derecho de padre y la madre, aunque no ejerzan la patria potestad, a relacionarse con sus hijos menores, de manera negativa se estipulaba con generalidad que no pudieran impedirse tampoco sin justa causa las relaciones personales entre el hijo, y otros parientes y allegados.

El art. 1.º.5 de la citada Ley 42/2003, concediendo nueva redacción al art. 160 CCiv, especificó que las relaciones personales de los menores no cabe sean vedadas con sus abuelos, en la línea de reconocer la necesidad de un tratamiento explícito y reforzado a la contribución al desarrollo personal de aquéllos de esas relaciones no circunscritas a lo paternofilial que son las de abuelos y nietos.

Como razonaba la Exposición de Motivos, los abuelos gozan respecto de los nietos de una autoridad moral y de una distancia de los problemas de la ruptura de la pareja de progenitores, que ayuda a instaurar una relación familiar estable y con viabilidad de desarrollo, contrarrestando los efectos negativos de la hostilidad o enfrentamiento entre los padres, derivados de la crisis de su unión, lo cual neutraliza el trauma de la separación y lleva el privilegio de la proximidad de parentesco y de su experiencia vital.

Así, conforme al art. 39 CE está consagrada en nuestro ordenamiento la igualdad de los hijos ante la ley con independencia de su filiación, y el deber de los padres de prestar asistencia de toda clase a los hijos habidos dentro o fuera del matrimonio, en el marco del fomento de la protección integral del menor y de la familia, la cual obviamente no es sólo la matrimonial. Y en la cohesión y transmisión de los valores de la familia, desempeñan un papel fundamental los abuelos, debiendo los poderes públicos favorecer, ante la crisis de las relaciones familiares de los progenitores, el mantenimiento del espacio de socialización, en interés de los menores, que representa la comunicación con los abuelos.

Precisamente, el art. 160.2 CCiv, en la redacción dada por la Ley 26/2015, de 28 de julio, de modificación del sistema de protección a la infancia y a la adolescencia, vuelve a ampliar el derecho del menor a relacionarse con sus parientes incluyendo expresamente a los hermanos.

Pues bien, cuando los padres viven separados, la patria potestad se ejerce por aquel con quien el hijo conviva (art. 156, párrafo 5.º CCiv), pero con independencia de que el hijo de los demandantes D./Dña. [NOMBRE Y APELLIDOS] no reclame tal ejercicio o la distribución de funciones con la madre del menor, no dejan de detentar los abuelos de éste una prerrogativa legal como derecho de su nieto de contar con el contacto físico y anímico de estos abuelos paternos en orden al desarrollo de su personalidad, del todo semejante al derecho de comunicación y visita al hijo matrimonial referido por el art. 94 CCiv en supuesto de nulidad, separación, y divorcio.

Precisamente, el ejercicio del derecho del nieto se precave para casos como el presente, de ausencia del padre o de desinterés por relacionarse con el hijo, por obstáculos de hecho, cual el alejamiento por necesidad laboral.

En caso de oposición a que se desenvuelva este derecho, el Juez, a petición de los abuelos, resolverá atendidas las circunstancias, precaviendo el párrafo segundo del art. 160.2 CCiv, que ello no suponga medida potestativa de la infracción de resolución judicial que suspenda o restrinja las relaciones de los menores con alguno de sus progenitores, sin que la sentencia a propósito de este asunto suponga ninguna suspensión ni restricción de tal tipo.

No habiendo sido posible el acuerdo de establecer un régimen de visitas de los abuelos de manera extrajudicial, se propone una tradicional atribución del tiempo libre extraescolar, como sigue:

Los abuelos D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS] podrán tener consigo a su nieto, recogiéndole de la salida de la guardería y devolviéndole en el domicilio de la madre antes de las 22 horas, una tarde de cada día entre semana, a su elección, de lunes a viernes, y le podrán tener en su compañía cada fin de semana alterno, del sábado a las 10 horas hasta el domingo a las 20.30 horas.

Asimismo, en vacaciones de Navidad, el hijo pasará una mitad de sus vacaciones escolares con los predichos abuelos y la otra mitad con la madre, aquéllos la primera mitad los años pares, y dicha primera mitad la madre los años impares; en las de Semana Santa, el hijo pasará los años pares con la madre y los impares con los abuelos; y durante el período de vacaciones de verano escolares, pasará el hijo el mes de julio con la madre los años pares, y el mes de agosto con los abuelos, de modo que los años impares pase el hijo julio con los abuelos y agosto con la madre.

Las visitas de semana se suspenderán en los periodos vacacionales, y las comunicaciones con los abuelos se compatibilizarán con las que en un futuro puedan regularse con el progenitor del nieto Don [NOMBRE Y APELLIDOS]

VII.- COSTAS.

Conforme al artículo 394 LEC las costas han de imponerse a la demandada, si se opone y resulta vencida.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que, habiendo por presentado este escrito de demanda con los documentos que lo acompañan y sus copias, se digne admitir uno y otros, y teniéndome por comparecido y parte en la representación que ostento, y por promovido juicio verbal frente a D./Dña. [NOMBRE Y APELLIDOS], acuerde emplazarla, así como al Ministerio Fiscal, para que, en su caso, comparezca y conteste, y seguido que sea todo el pertinente procedimiento, se dicte en su día sentencia por la que estimando la demanda, se decrete un régimen de comunicación y visitas de los demandantes con su nieto menor de edad, en las condiciones reseñadas en el fundamento de derecho quinto del cuerpo de la demanda, o las que se determinen más adecuadas al interés del menor por S.Sª. Ilma., con condena a la demandada a estar y pasar por la antedicha declaración a todo efecto, así como al pago de las costas del juicio a la parte demandada.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a
