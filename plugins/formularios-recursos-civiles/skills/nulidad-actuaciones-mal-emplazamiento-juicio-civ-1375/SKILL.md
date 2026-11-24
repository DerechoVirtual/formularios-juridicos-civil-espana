---
name: nulidad-actuaciones-mal-emplazamiento-juicio-civ-1375
description: "Nulidad de actuaciones por mal emplazamiento en juicio de impugnación de acuerdos de comunidad. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Nulidad de actuaciones por mal emplazamiento en juicio de impugnación de acuerdos de comunidad

> Formulario **CIV-1375** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 24-11-2026.

## Qué es

Escrito solicitando la nulidad de actuaciones por defecto de emplazamiento en juicio ordinario de impugnación de acuerdo de Comunidad de propietarios.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Nulidad de actuaciones por mal emplazamiento en juicio de impugnación de acuerdos de comunidad» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Nulidad de actuaciones por mal emplazamiento en juicio de impugnación de acuerdos de comunidad” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:nulidad-actuaciones-mal-emplazamiento-juicio-civ-1375`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (14 veces)
- [ ] FECHA (7 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] AÑO
- [ ] LUGAR
- [ ] NOMBRE DE LA PARTE
- [ ] Nº DE PROCEDIMIENTO
- [ ] SEDE

## Normas que cita el formulario

- art. 497.1 LEC
- art. 238.3.º LOPJ
- art. 225.3.º LEC
- art. 231 LEC
- art. 240.1 LOPJ
- art. 227.1 LEC
- art. 243 LOPJ
- art. 230 LEC

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

D./Dña. [NOMBRE Y APELLIDOS], Procuradora de los Tribunales, y de la COMUNIDAD DE PROPIETARIOS DE LA CASA N.ºDE LA CALLEDE, como tengo acreditado en autos mediante el poder ‘apud acta’ otorgado por la Sr./a Presidente/a, D./Dña. [NOMBRE Y APELLIDOS], ayer día [FECHA], y cuyas circunstancias constan, en los autos de juicio ordinario n.º [Nº DE PROCEDIMIENTO]/[AÑO], a instancias de D./Dña. [NOMBRE Y APELLIDOS], comparezco y como mejor en Derecho proceda, DIGO:

Que mediante el presente escrito vengo a deducir petición de nulidad de actuaciones desde el momento inmediato a la diligencia de emplazamiento de esta parte en el presente juicio, de impugnación de acuerdo comunitario por el copropietario D./Dña. [NOMBRE Y APELLIDOS], con base en las siguientes:

ALEGACIONES

PRIMERA

Presentada y admitida a trámite el [FECHA] demanda del Procurador/a Sr./a [NOMBRE Y APELLIDOS], en representación de D./Dña. [NOMBRE Y APELLIDOS], recayó diligencia de ordenación de [FECHA] en que se declaró la rebeldía de mi principal por no haber comparecido a contestar, a raíz de expirar el plazo de veinte días desde la notificación y emplazamiento practicado el anterior día [FECHA], y notificada por correo dicha resolución, conforme al art. 497.1 LEC, que se entregó a la Presidente de la Comunidad D./Dña. [NOMBRE Y APELLIDOS], por primera vez tuvo conocimiento mi representada de la existencia de este juicio ordinario.

SEGUNDA

La Sr./a Presidente/a de la Comunidad demandada compareció en el Tribunal al día siguiente a ser enterada, y otorgó poder ante la Secretaría a favor de la Procuradora Sr./a [NOMBRE Y APELLIDOS], produciéndose al inmediato siguiente a esta petición de nulidad de lo actuado.

TERCERA

La nulidad radical de los actos judiciales hasta sentencia definitiva puede decretarse de oficio en el caso de que se haya prescindido de las formas esenciales del procedimiento con indefensión efectiva de alguna de las partes, de tal modo que la firmeza o cosa juzgada formal de resoluciones interlocutorias, si bien la nulidad tenga que hacerse valer por las partes a través de los recursos que legalmente les cumplen de ordinario, no es nunca valladar insalvable para que se decrete la invalidez de lo que no vale en el orden público procesal, sujetando el principio de legalidad al de sanación de actos procesales bajo criterio superior de la tutela judicial efectiva, incluso si la nulidad se "sugiere" por la parte afectada, como es el caso (cfr.: arts. 238.3.º, 240 LOPJ —arts. 225.3.º, 227 LEC— y art. 231 LEC). El único requisito para la utilización de los poderes de oficio en este campo es la bilateralidad de audiencia.

CUARTA

El vicio de nulidad absoluta en el caso surge de la conjunción de tres circunstancias:

a) que se prescinda de las formas del procedimiento;
b) que la elusión formal procure efectiva indefensión, y
c) que la indefensión no haya sido querida o asumida por el interesado (cfr.: art. 238.3.º LOPJ —art. 225.3.º LEC—).

Conforme a constante y reiterada doctrina constitucional (por todas, STC 251/88 de 20 de diciembre), se ha establecido que del mandato contenido en el art. 24.1 CE se deriva que la indefensión debe ser entendiendo aquélla que produce un efectivo y real menoscabo del derecho de defensa, es decir, no se trata de una abstracción, de manera que una determinada irregularidad que atañe a las posibilidades de conducta procesal de parte sea originadora de indefensión, y otra nunca lo sea, sino que debe examinarse la circunstancia por comprobar si el demérito de defensa es un pretexto o algo verídico.

Por otro lado la indefensión relevante no es situación objetiva de falta de defensa sino subjetiva, en el sentido de que haya tenido que imponerse contra la voluntad del justiciable, que acredite su voluntad expresa o tácita contraria, sin que se amparen intencionadas ausencias de ‘voz’ procesal o simplemente la negligencia en el levantamiento de las cargas legales para ser oído.

QUINTA

Pues bien, el emplazamiento de [NOMBRE DE LA PARTE] en una persona de la que se llamaba D./Dña. [NOMBRE Y APELLIDOS], y que no firma, sin que se hagan constar las razones, externamente es lícito y eficaz, y sin embargo, son nulos los actos judiciales cuyo defecto formal implica la ausencia de requisitos indispensables para alcanzar su fin (art. 240.1 LOPJ —art. 227.1 LEC—), y aunque la citación de un vecino copropietario entera válidamente a la Comunidad de propietarios, que no tiene personalidad jurídica, y no es exigible la citación a su órgano de representación, si se demuestra que el fin garantizado de enteramiento no se verifica, cumple anular.

Y quien fue enterado, realmente es vecino del inmueble, padre de una copropietaria, pero está aquejado de incapacidad natural, por demencia senil que es evidente para cualquiera que entra en contacto con dicha persona, pero que simplemente el dato de su avanzadísima edad —nacido en 1908—, debiera bastar para comprender que no entendió lo que se le comunicaba, o no lo recordaría, o no lo transmitiría cabalmente a los responsables de la Comunidad.

Se acompañan certificación de nacimiento de D./Dña. [NOMBRE Y APELLIDOS], e informe médico en que se hace constar la enfermedad psíquica del mismo, como documentos números [Nº DE DOCUMENTO] y [Nº DE DOCUMENTO].

SEXTA

El caso es que la Comunidad no ha tenido conocimiento de dicha notificación y emplazamiento, y una vez conocidos los hechos, y averiguado dónde paró el agente notificador, tampoco se ha encontrado la copia de la resolución, demanda y documentos, que no se sabe dónde los guardara o tirara D./Dña. [NOMBRE Y APELLIDOS]

Cuando consta que el/la Presidente/a de la Comunidad demandada recibió noticia cabal desde el Tribunal de este proceso, al notificársele la rebeldía, se sigue al postrer día el otorgamiento de poder ‘apud acta’ a Procurador de los Tribunales, y hoy, escrito con firma de Letrado en solicitud de nulidad de actuaciones, sin que se alegue por nadie que hubiera un enteramiento anterior, ni medien indicios de tal cosa.

SÉPTIMA

Objetivamente, el no poder contestar la demanda supone la inviabilidad de plantear la resistencia a la pretensión actora, quedando las posibilidades defensivas de esta parte, por razón de la tesis de la ‘ficta contestatio’ de nuestro sistema procesal en juicios declarativos, reducida a confiar en que la parte actora no logre probar los hechos constitutivos de su pretensión, y a plantear en la audiencia previa meras contrapruebas que impidan, extingan o excluyan la existencia de tales hechos, lo que supone mengua capital de defensa.

OCTAVA

El Tribunal no pudo tener constancia de la condición del sujeto emplazado, pero cuando la tiene, ha de vedar que se tenga por eficaz un acto que se prueba no alcanzó su fin, ni era viable que lo alcanzara, determinando una carencia de garantías evidente. Si a pesar de cumplirse con su fin, el acto de comunicación debe sujetarse a las formas legales, porque se sujete a éstas aparentemente, si se justifica que no cumplió su fin, no es válido.

Y como hay explícita voluntad de resistencia, y no se ha hecho dejación del derecho propio, es decir, resulta efectiva la indefensión dimanante de un vicio formal, que no ha sido asumida por el que la invoca, la conclusión es que ha existido un quebrantamiento sustancial del acto de comunicación que interpela para contestar a la demanda, y no ha conseguido acreditar el fin previsto del enteramiento cabal y completo a la demandada, mientras que ha provocado indefensión no pretextativa (arts. 238.3.º y 240.1 y 2 LOPJ —arts. 225.3.º y 227.1 y 2 LEC—)

NOVENA

La sanción ante ello es la declaración de nulidad con expulsión del mundo jurídico de los actos procesales posteriores al momento inmediatamente anterior a la providencia de [FECHA] excepto de los que, independientes, hubiesen permanecido invariables aún sin haberse cometido la infracción de nulidad (art. 243 LOPJ —art. 230 LEC—), que son la consideración de personada y parte de la demandada con su representación procesal del proveído del día de ayer de

Por principio de subsanación (art. 231 LEC), y dado que la Comunidad demandada está personada y ha obtenido copia de la demanda y sus documentos, sencillamente corresponder concederle plazo de veinte días para contestar.

En su virtud,

AL TRIBUNAL SUPLICO

que, teniendo por presentado este escrito con sus documentos adjuntos, y copia de uno y otros, se digne admitirlo, y previa audiencia de la contraparte, en mérito a lo manifestado, decrete la nulidad de todas las actuaciones en el presente juicio promovido por el Procurador de los Tribunales D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], hasta el momento inmediatamente anterior al dictado de la providencia de [FECHA], a excepción de la resolución que tiene por personada y parte a la demandada, COMUNIDAD DE PROPIETARIOS DEL NºDE LA CALLEDE, representada por la Procuradora de los Tribunales D./Dña. [NOMBRE Y APELLIDOS], concediéndoseme plazo de veinte días a fin de contestar a la demanda

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a

========================================================================
