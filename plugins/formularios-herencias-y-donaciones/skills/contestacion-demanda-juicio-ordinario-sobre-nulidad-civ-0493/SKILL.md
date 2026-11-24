---
name: contestacion-demanda-juicio-ordinario-sobre-nulidad-civ-0493
description: "Contestación a la demanda de juicio ordinario sobre nulidad de testamento. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contestación a la demanda de juicio ordinario sobre nulidad de testamento

> Formulario **CIV-0493** del plugin **Herencias, testamentos y donaciones** (`formularios-herencias-y-donaciones`) · Civil › Sucesiones y donaciones · normativa revisada el 24-11-2026.

## Qué es

Contestación a la demanda de juicio ordinario sobre nulidad de testamento alegando el demandado la excepción procesal de falta de capacidad de la actora; la excepción procesal por defecto de la representación por ilegalidad del poder del Procurador/a de la parte actora y la habilidad del testador

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contestación a la demanda de juicio ordinario sobre nulidad de testamento» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contestación a la demanda de juicio ordinario sobre nulidad de testamento” para mi caso». También puedes invocarla directamente con `/formularios-herencias-y-donaciones:contestacion-demanda-juicio-ordinario-sobre-nulidad-civ-0493`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-herencias-y-donaciones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Herencias, testamentos y donaciones) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (38 veces)
- [ ] LOCALIDAD (9 veces)
- [ ] Nº DE DOCUMENTO (9 veces)
- [ ] FECHA (4 veces)
- [ ] AÑO (3 veces)
- [ ] NÚMERO (2 veces)
- [ ] CALLE
- [ ] COLEGIO
- [ ] DENOMINACIÓN SOCIAL
- [ ] IMPORTE
- [ ] LUGAR
- [ ] Nº DE PROCEDIMIENTO
- [ ] SEDE

## Normas que cita el formulario

- art. 418.2 LEC
- art. 1.217 CC
- art. 23.1 LEC
- art. 418.1 LEC
- art. 217.1 LEC
- art. 217.2 LEC
- art. 199 CC
- art. 394 LEC
- art. 338.2 LEC

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, que actúa en representación de D./Dña. [NOMBRE Y APELLIDOS], en razón de poder para pleitos que, por copia fehaciente acompaño, con ruego de su devolución por necesitarla a otros usos, previo testimonio bastante en autos, dirigida por el Letrado en ejercicio del Iltre. Colegio de Abogados de [COLEGIO], D./Dña. [NOMBRE Y APELLIDOS], con despacho abierto en [LOCALIDAD], calle [CALLE], en el Juicio Ordinario nº [Nº DE PROCEDIMIENTO]/[AÑO] comparezco, y como mejor proceda en Derecho DIGO:

Que en representación de mi poderdante me persono y muestro parte en el juicio indicado, y paso a contestar la demanda y solicitar una Sentencia conforme al "Suplico" de este escrito, en base de las siguientes consideraciones fácticas y jurídicas.

HECHOS

PRIMERO

Niego y desconozco todos los alegados en la demanda que no se ajusten totalmente a los que paso a expresar, y afirmo, además, que D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS] eran amigos de mucha antigüedad y no como se pretende por la parte contraria, de suyo tiempo antes del matrimonio con la actora, tratando el segundo al primero como a un hijo.

La actora fue el ama de llaves del Sr./a. D./Dña. [NOMBRE Y APELLIDOS] desde la juventud, y sólo ya jubilada, y cuando éste padeció su primer infarto cerebral el [FECHA], contrajeron ambos matrimonio.

Fue en dicha coyuntura, con el ingreso hospitalario de D./Dña. [NOMBRE Y APELLIDOS] que le conoció D./Dña. [NOMBRE Y APELLIDOS]

SEGUNDO

Entiende esta parte que la actora, D./Dña. [NOMBRE Y APELLIDOS] es persona incapaz de gobernar su persona y administrar sus bienes, según se desprende del Informe Médico Neurológico que acompañamos, puesto que, amén de su avanzada edad, padece afasia completa y sufrió el año [AÑO] una hemiplejia izquierda (documento nº [Nº DE DOCUMENTO]).

De los mismos términos del testamento impugnado se colige, ya que se designa a dicha señora, viuda del causante, usufructuaria universal vitalicia, gravando la nuda propiedad del heredero único, mi mandante, y se contienen previsiones para el caso de incapacitación, incluido el nombramiento de tutor a mi representado.

Se solicitará la correspondiente pericia médica a fin de demostrar el aserto.

TERCERO

La actora, que realmente no es capaz de hacerse entender, ni comprende la plena transcendencia de los actos de la personalidad, ha sido ‘captada’ por un tal D./Dña. [NOMBRE Y APELLIDOS], administrativo de la denominada ‘Gestoría [DENOMINACIÓN SOCIAL] ‘, entidad a través de la cual el finado D./Dña. [NOMBRE Y APELLIDOS] realizó la adquisición de valores mobiliarios en varias ocasiones en los últimos tiempos, y a la que se encomendó para asesoramiento fiscal y administración de las rentas de los locales comerciales propiedad de D./Dña. [NOMBRE Y APELLIDOS]

Se acompañan como documentos nos. a [Nº DE DOCUMENTO], demostración de estas relaciones, y de la intervención del dicho D./Dña. [NOMBRE Y APELLIDOS]

A raíz de que mi poderdante pretendió la regularización registral de la titularidad de los inmuebles propiedad de D./Dña. [NOMBRE Y APELLIDOS], después de su llorada pérdida, y la averiguación de las acciones, participaciones, fondos, y depósitos bancarios de la herencia, D./Dña. [NOMBRE Y APELLIDOS] vedó a mi patrocinado el acceso al domicilio de D./Dña. [NOMBRE Y APELLIDOS] y procedió a reclutar al abogado director de la demanda, la cual se ha presentado después de una impresentable propuesta de reparto del patrimonio hereditario, y de que esta parte dedujera solicitud de procedimiento de división de herencia de arts. 782 y ss. LEC.

Se acompañan la copia de fax recibido por el letrado suscrito y que enviara el de contrario (documento nº [Nº DE DOCUMENTO]), y testimonio de demanda y decreto/auto de admisión del juicio divisorio nº [NÚMERO]/[AÑO] por el Tribunal de Instancia nº [NÚMERO] (documento nº [Nº DE DOCUMENTO]).

CUARTO

El poder que esgrime la Procurador/a D./Dña. [NOMBRE Y APELLIDOS], en pretendida representación de D./Dña. [NOMBRE Y APELLIDOS], expresa otorgamiento precisamente por D./Dña. [NOMBRE Y APELLIDOS] como apoderado de aquélla, pero no se inserta el poder del sustituyente, original ni por copia adverada, por lo que resulta ilegal y no puede producir efecto alguno.

Duda esta parte de la validez y condiciones para conferir poderes por D./Dña. [NOMBRE Y APELLIDOS] y de la amplitud de las facultades contenidas.

QUINTO

Cronológicamente, el testamento que impugna la demanda se otorga el día [FECHA] en el intermedio entre dos ingresos en el Servicio de Urgencias del Hospital de [LOCALIDAD], consecuencia de infartos cerebrales, el segundo al de tres días del otorgamiento, e inmediatamente antes de su ingreso en el Servicio de Urgencias del Hospital de [LOCALIDAD] que acabará con la defunción del Sr./a D./Dña. [NOMBRE Y APELLIDOS], producido al de cinco días.

Lo anterior resulta de la prueba documental recabada por el Servicio de Salud de [LOCALIDAD]

El informe del segundo ingreso en el Hospital de [LOCALIDAD], hace constar expresamente que el paciente acude consciente (documento nº [Nº DE DOCUMENTO]), por lo que nada indica que no lo estuviera tres días antes, cuando no había sufrido otro episodio de su dolencia.

Pero es que los informes del Hospital de [LOCALIDAD] nos sirven para representarnos cuál era la situación del Sr./a D./Dña. [NOMBRE Y APELLIDOS] en la fecha en que otorgó el testamento, nueve días antes, que lógicamente no podía ser peor, sino mejor.

En la primera hoja del informe extendido por el Hospital de [LOCALIDAD], y firmada por la Doctor/a [NOMBRE Y APELLIDOS], se hace constar, a la hora de describir su estado desde el día de su ingreso precedente, es decir, tres días después de otorgar el testamento, una situación física del Sr./a. D./Dña. [NOMBRE Y APELLIDOS], en que se dice (documento nº [Nº DE DOCUMENTO]):

‘se le encuentran hematomas en piernas y cara, según refiere por haberse caído en la calle. Tampoco ha comido y ha bebido poco‘

Lógicamente, si se cayó en la calle, es que no estaba encamado, y si refirió el episodio es que se comunicaba cabalmente con la doctora, por lo que ‘a fortiori’, tres días antes de sufrir un último infarto cerebral, pudo acudir a la notaría y otorgar su voluntad en testamento.

Pero consta también un informe de Psiquiatría realizado por el Doctor/a [NOMBRE Y APELLIDOS] que dice textualmente (documento nº [Nº DE DOCUMENTO]):

‘Psiquiatría (20:30 horas): Cierto enlentecimiento del pensamiento y reiteración en el lenguaje. Defensas obsesivas (minuciosidad) ante la conciencia de estar perdiendo la capacidad superior, que no corresponde bien a clínica demenciativa instaurada‘

D./Dña. [NOMBRE Y APELLIDOS] había ya padecido un infarto cerebral antes de otorgar testamento, pero si, después de padecer otro y antes de que en el Hospital de [LOCALIDAD] evolucionara hacia isquemia aguda, y multitinfartos cerebrales, diagnóstico previo al coma y muerte, se produce una situación de conciencia de la pérdida de capacidad superior, se concluye que ésta se tenía antes.

Se sabe que D./Dña. [NOMBRE Y APELLIDOS] padecía de un Mucocele en seno frontal derecho, lesiones isquémicas en sustancia blanca y núcleos de la base, y ello residuaba una artorfia cerebral y cerebelosa desde hacía ya cuatro años, tiempo en el que otorgó el testamento que designaba única sucesora a su viuda, sin que parezca a quien demanda que en esta decisión hubiera insanidad del disponente, y sí por el contrario en la adoptada previamente a empeorar definitivamente.

SEXTO

Capaz o no la demandante, lo cierto es que ella con sus ‘asesores forzosos’, han realizado actos que acreditan haber tenido y tener por buenas las disposiciones del testamento, según se induce, por ejemplo de dos circunstancias:

Las remesas, de [IMPORTE] euros mensuales, y que acreditan los documentos que acompañamos con nos. a [Nº DE DOCUMENTO], las cuales libra mi poderdante a la usufructuaria de los fondos bancarios de la herencia de D./Dña. [NOMBRE Y APELLIDOS] (en los que aquél posee firma autorizada).

La proposición de acuerdo extrajudicial del precitado documento nº [Nº DE DOCUMENTO], inviable de resultar que el testamento fuera absolutamente nulo y que supondría una transacción, equivalente al reconocimiento de recíproca contraprestación de esta parte, en contradicción absurda con la postura que mantienen.

FUNDAMENTOS DE DERECHO

I.- Excepción procesal por falta de capacidad procesal de la actora, ya que su incapacidad para regir su persona no le permite comparecer en juicio, al haber perdido naturalmente el pleno ejercicio de derechos civiles, estando legitimado el Ministerio Fiscal para que se decrete en declarativo contradictorio, lo cual resulta posible dentro de este procedimiento (STS de 30 de enero de 1995 (rec. 3110/1991)), y es denuncia de presupuesto procesal que no concurre para conocer de la pretensión en cuanto al fondo, y sin perjuicio de la adopción de medidas cautelares, y de que se nombre defensor judicial mientras se sustancia la incapacitación.

Procede poner fin al proceso, previo dictamen pericial, y en todo caso, corresponderá tratamiento conforme al art. 418.2 LEC en la audiencia previa.

II.- Excepción procesal por defecto de la representación por ilegalidad del poder del Procurador/a de la parte actora, al incumplir el mandato del art. 1.217 CCiv, en relación con el art. 166 del Reglamento Notarial y doctrina jurisprudencial [STS de 30 de diciembre de 1991 y las que cita], por relación con art. 23.1 LEC, que deberá depurarse con arreglo al art. 418.1 LEC.

III.- Fondo del asunto. La incapacidad testamentifactora ha de existir en el momento de otorgar el testamento y tal capacidad se presume, y es precisa una prueba concreta, inequívoca y convincente en evidencia para declarar la incapacidad (STS de 26 de abril de 1995 (rec. 1748/1992) y las numerosas que cita).

La regla de juicio al servicio del Juez acuciado a resolver (arts. 217.1 LEC y 11.3 LOPJ), cuando un hecho no se pruebe existente o inexistente en el proceso, es la del perjuicio de la posición de quien lleva legalmente el ‘onus probandi’, que en principio pesa al actor respecto de los hechos de ordinario constitutivos del derecho deducido, que integran el presupuesto de la norma cuya aplicación quiere la pretensión, gravando al demandado la de los hechos especiales, impeditivos, extintivos o excluyentes (así arts. 217.2 y 3 LEC).

Esta parte se limita a negar el hecho constitutivo de la inhabilidad de D./Dña. [NOMBRE Y APELLIDOS] al momento de otorgar testamento, y nada tiene que probar, puesto que aquélla se presume en los mayores de edad no incapacitados (arts. 199 y 200 CCiv). Pero es que, de la documentación de la sanidad pública con que se cuenta, y de los testimonios que se recabaran de los especialistas que trataron a D./Dña. [NOMBRE Y APELLIDOS] en días inmediatos al acto de última voluntad, habrá de probarse la presencia de capacidad volitiva y cognoscitiva que presentaba el Sr./a D./Dña. [NOMBRE Y APELLIDOS] en el preciso momento de su ingreso hospitalario, tres días después de acudir a la notaría, y sufrido un nuevo infarto cerebral.

El Sr./a D./Dña. [NOMBRE Y APELLIDOS] era una persona que comprendía lo que se le decía al ingresar en urgencias, tenía conciencia de la realidad, hasta tal punto de que tenía cabal conocimiento de que había nombrado un heredero pocos días antes, puesto que comentó con el psiquiatra Doctor/a [NOMBRE Y APELLIDOS] que no tenía descendencia ni parientes cercanos, y que su preocupación por perder capacidad le había llevado a testar en su amigo y cuidador de toda confianza, consciente de la incapacidad de su esposa (ello en ese episodio de reiteraciones machaconas por conciencia de la pérdida de capacidad superior que se describe).

Los interesados dictámenes periciales de contrario son juicios de valor sobre los mismos certificados médicos que ha leído esta parte y puede leer el Tribunal, y resultan inanes ante su tenor.

D./Dña. [NOMBRE Y APELLIDOS] presentaba un cuadro clínico de lesiones por infartos cerebrales múltiples que se remontaban a tiempo atrás, anterior al testamento en que nombra universal única heredera a su esposa D./Dña. [NOMBRE Y APELLIDOS]

Sus limitaciones no le hicieron vacilar ante una decisión repleta de razón, ya que si había conseguido un amigo y guarda, mi mandante, y su consorte sufría una afasia completa con hemiplejía izquierda, además de ser muy anciana, puesto que la herencia en definitiva no tenía descendientes o parientes a quien dejarse, y fallecido los cónyuges se deferiría al Estado, parecía más prudente, y ello después de un infarto cerebral del que se repuso en el día [FECHA], tras ingreso en Urgencias del Hospital de [LOCALIDAD], lo que anunciaba un empeoramiento, confiar en la persona que realmente podía hacerse cargo, designándola heredero universal, pero nudo propietario, ya que todo el usufructo vitalicio se reservaba a la cónyuge supérstite, e incluso se encomendaba a mi representado para tutor de D./Dña. [NOMBRE Y APELLIDOS]

No hay nada de cierto en que la demandante haya quedado excluida de la herencia, sino que sencillamente lo que reste de la misma al fallecimiento de aquélla no carecerá de sucesor.

Ha habido interesados en que esto no se cumpla, una vez que se empezó a ejecutar, librándose una renta a la viuda y precaviéndose el inventario judicial en procedimiento divisorio.

Y no puede ejercitar acción de nulidad del testamento quien expresa o tácitamente haya reconocido su validez, por fuerza del principio vinculante de los actos propios (STS de 31 de enero de 1995 ó 30 de septiembre de 1996).

IV.- Por lo relativo a costas procesales, es de empleo el art. 394 LEC que se menciona de adverso, pero con el efecto de condena a la actora, que será vencida por la resistencia de esta parte.

En su virtud,

SUPLICO AL TRIBUNAL

que habiendo por presentado este escrito con el poder, documentos y copias que se acompañan, se sirva tenerme por comparecida y parte en nombre de quien represento; por contestada la demanda en tiempo y forma y, seguido el juicio por sus regulares trámites, dicte Sentencia por la que se desestime íntegramente la demanda:

Absolviendo en la instancia, sin entrar a conocer del fondo y por las razones adjetivas señaladas, que son presupuestos procesales que no se llenan y resulten insubsanables o subsidiariamente,

Absolviendo libremente por las resistencias de fondo, y en cualquier caso,

Con imposición de costas a la parte actora.

OTROSI DIGO: La incapacidad de la actora D./Dña. [NOMBRE Y APELLIDOS] es presupuesto del proceso que debe ser depurado de oficio inmediatamente, o en su caso, dará lugar al sobreseimiento en la audiencia previa, pero tanto si para ello se precisa un contradictorio incidental previo con prueba, como para la prueba misma del proceso principal, es interés de esta parte proponer prueba pericial de un MÉDICO-PSIQUIATRA que, previo estudio de los antecedentes que obran en autos y examen de la demandante, emita dictamen acerca de si D./Dña. [NOMBRE Y APELLIDOS] padece alguna enfermedad psíquica o psíquico-somática, que la impida gobernar su persona y administrar su bienes, y en caso positivo, se pronuncie sobre su entidad o alcance discapacitante, su irreversibilidad, la constancia o carácter episódico, y data aproximada de cuando se instauró la enfermedad incapacitante.

Aunque se sostenga que la designación judicial de perito, que resulta pertinente y útil, del art. 338.2 LEC, resulta defectiva de la aportación de dictamen por escrito por la parte, es evidente que en el supuesto actual esta parte demandada no puede obtener un dictamen por su cuenta, ya que ni siquiera tiene posibilidad de acercarse a la actora, y mucho menos de contratar un psiquiatra que sea recibido.

En su virtud,

SUPLICO AL TRIBUNAL

que de lo dicho haga el mérito oportuno, y tenga por causada petición de designación judicial de perito médico especialista en psiquiatría con el objeto indicado, a expensas de lo que resuelva para la audiencia previa, y los términos que, en su caso, haya de proponerse prueba.

Todo es de hacerse en Justicia, que reitero en lugar y fecha que constan.

Por ser de Justicia que pido en [LUGAR], a [FECHA].

SING:

Firma de Abogado/a	Firma de Procurador/a

========================================================================
