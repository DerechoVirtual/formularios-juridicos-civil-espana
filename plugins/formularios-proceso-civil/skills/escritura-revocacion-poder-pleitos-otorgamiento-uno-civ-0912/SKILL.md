---
name: escritura-revocacion-poder-pleitos-otorgamiento-uno-civ-0912
description: "Escritura de revocación de poder para pleitos y otorgamiento de uno nuevo. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura de revocación de poder para pleitos y otorgamiento de uno nuevo

> Formulario **CIV-0912** del plugin **Proceso civil: demandas, contestaciones, prueba y vista** (`formularios-proceso-civil`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 24-11-2026.

## Qué es

Escritura notarial por la que el poderdante revoca un poder anterior, con requerimiento notarial al antiguo apoderado para que se dé por notificado y devuelva las copias, y otorga en el mismo acto un nuevo poder de representación procesal a favor de procuradores y letrados.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura de revocación de poder para pleitos y otorgamiento de uno nuevo» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura de revocación de poder para pleitos y otorgamiento de uno nuevo” para mi caso». También puedes invocarla directamente con `/formularios-proceso-civil:escritura-revocacion-poder-pleitos-otorgamiento-uno-civ-0912`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-proceso-civil:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso civil: demandas, contestaciones, prueba y vista) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (8 veces)
- [ ] AÑO (4 veces)
- [ ] DÍA (4 veces)
- [ ] MES (4 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] CALLE (2 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] DNI/NIE (2 veces)
- [ ] LETRA (2 veces)
- [ ] NOMBRE DEL NOTARIO (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL LETRADO (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR (2 veces)
- [ ] Nº (2 veces)
- [ ] PISO (2 veces)
- [ ] CARGO
- [ ] COLEGIO NOTARIAL
- [ ] DESCRIPCIÓN DEL PODER
- [ ] DOMICILIO
- [ ] ESTADO CIVIL
- [ ] FECHA
- [ ] NOMBRE Y APELLIDOS DEL APODERADO
- [ ] NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL DEL PODERDANTE
- [ ] Nº DE FOLIOS
- [ ] Nº DE PROTOCOLO
- [ ] NÚMEROS
- [ ] PROFESIÓN
- [ ] SERIE

## Normas que cita el formulario

- No cita artículos concretos; Claude localizará las normas aplicables con Jurisprudenciator si el documento las necesita.

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

En [LOCALIDAD], mi residencia, a [DÍA] de [MES] de [AÑO].

Ante mí, [NOMBRE DEL NOTARIO], Notario del Ilustre Colegio Notarial de [COLEGIO NOTARIAL], y al efecto de otorgar escritura de poder.

COMPARECE/N:

Don/Doña [NOMBRE Y APELLIDOS], mayor de edad, [ELEGIR: casado/a / soltero/a], vecino/a de [LOCALIDAD], con domicilio en [LOCALIDAD], en la calle [CALLE], número [Nº], piso [PISO], letra [LETRA], con DNI/NIE número [DNI/NIE].

[OPCIONAL — incluir si hay más de un compareciente]
Don/Doña [NOMBRE Y APELLIDOS], mayor de edad, [ELEGIR: casado/a / soltero/a], vecino/a de [LOCALIDAD], con domicilio en [LOCALIDAD], en la calle [CALLE], número [Nº], piso [PISO], letra [LETRA], con DNI/NIE número [DNI/NIE].

INTERVIENE/N

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— En nombre propio: [ELEGIR: Interviene en su propio nombre y derecho. / Intervienen ambos en su propio nombre y derecho.]

— En representación: Don/Doña [NOMBRE Y APELLIDOS], en nombre y representación de [DENOMINACIÓN SOCIAL], constituida el [DÍA] de [MES] de [AÑO], ejerce esta representación como [CARGO], estando facultado/a para este otorgamiento por acuerdo de fecha [DÍA] de [MES] de [AÑO], según resulta de la certificación o escritura de poder que se incorpora a esta matriz. Me asegura el/la compareciente la vigencia de esta representación.

TIENE/N, a mi juicio, la capacidad legal necesaria para formalizar esta escritura de REVOCACIÓN DE PODER ANTERIOR Y OTORGAMIENTO DE NUEVO PODER, y a tal efecto,

EXPONEN

ANTECEDENTES

En fecha [DÍA] de [MES] de [AÑO] los comparecientes otorgaron la escritura de poder que a continuación se indica y a favor del apoderado/a que también se menciona:

— Escritura de fecha [FECHA], autorizada por el Notario de [LOCALIDAD], Don/Doña [NOMBRE DEL NOTARIO], con el número [Nº DE PROTOCOLO] de su protocolo, de poder de [DESCRIPCIÓN DEL PODER].

— Apoderado/a: Don/Doña [NOMBRE Y APELLIDOS DEL APODERADO], mayor de edad, de estado civil [ESTADO CIVIL], de profesión [PROFESIÓN], vecino/a de [LOCALIDAD], domiciliado/a en [DOMICILIO].

REVOCACIÓN DEL PODER ANTERIOR

En este acto el/la compareciente REVOCA íntegramente la escritura de poder citada, requiriéndome a mí, el Notario, para que notifique al apoderado la revocación a todos los efectos legales, en el domicilio del mismo antes mencionado, y le requiera a su vez para que me entregue la copia o copias que de dicha escritura de poder disponga el apoderado.

OTORGAMIENTO DE NUEVO PODER

Que por medio del presente instrumento público confiere/n poder, tan amplio como fuere necesario en Derecho, a favor de:

A) Procuradores de los Tribunales de [LOCALIDAD]:

— Don/Doña [NOMBRE Y APELLIDOS DEL PROCURADOR].

— Don/Doña [NOMBRE Y APELLIDOS DEL PROCURADOR].

B) Letrados, en cuanto lo permita su estatuto profesional:

— Don/Doña [NOMBRE Y APELLIDOS DEL LETRADO].

— Don/Doña [NOMBRE Y APELLIDOS DEL LETRADO].

FACULTADES

Facultades de representación procesal

Comparecer como actor, demandado, litisconsorte, tercero interviniente, sustituto o sucesor procesal, cualquiera que sea la causa u origen de su intervención como sujeto o parte procesal, en nombre de Don/Doña [NOMBRE Y APELLIDOS] [ELEGIR: / como representante legal de la mercantil [DENOMINACIÓN SOCIAL]], ante los Jueces, Tribunales, Fiscalías, Juntas, Jurados, Sindicatos, Corporaciones, Administración y demás organismos, autoridades y funcionarios ordinarios o extraordinarios, especiales, excepcionales o únicos, de cualquier grado y competencia, incluidos los distintos ámbitos territoriales dentro del territorio nacional o supranacionales, y cualquiera que sea la jurisdicción, ya civil, penal, contencioso-administrativa, incluidas las vías previas administrativas, económico-administrativas o tributarias, social o laboral, eclesiástica, constitucional u otra cualquiera, común, especial o única, y al efecto poder intervenir y actuar en toda clase de expedientes, procedimientos y procesos, ya ordinarios, ordinarios con especialidades o especiales, y al efecto poder seguirlos por todos sus trámites desde el acto inicial o iniciador del mismo, incluida la demanda, ya ordinaria, ya sucinta, en ejercicio de todo tipo de petición de tutela jurisdiccional, incluidas las declarativas, constitutivas, de condena, ejecutivas o cautelares, y cualesquiera otras permitidas por las leyes, o la defensa frente a dichas peticiones de tutela, siguiéndolos por todos los trámites, fases o instancias, incidentes y recursos, incluidos los de casación, revisión, recurso extraordinario por infracción procesal, incidente excepcional de nulidad de actuaciones, amparo constitucional, demanda ante el Tribunal Europeo de Derechos Humanos y ante el Comité de Derechos Humanos de las Naciones Unidas, y solicitud de planteamiento de cuestión de inconstitucionalidad o de cuestión prejudicial ante el Tribunal de Justicia de la Unión Europea, y cualquier otro medio de impugnación o rescisión de resoluciones, incluida la audiencia al demandado rebelde, y terminarlos mediante la obtención de la resolución firme que corresponda y, en su caso, su ejecución y cumplimiento hasta la total satisfacción de la tutela jurisdiccional solicitada o interesada.

Por lo tanto, podrán celebrar antejuicios y cualesquiera actos preparatorios del proceso, ya potestativos o preceptivos, incluidos el acto de conciliación y las diligencias preliminares, cualquiera que sea el resultado, pudiendo solicitar copias y testimonios de las actas y resoluciones que se dictasen; presentar, ratificar, reiterar y retirar cualesquiera escritos y documentos; instar u oponerse a la abstención o recusación de jueces y magistrados, miembros del Ministerio Fiscal, Letrados de la Administración de Justicia, oficiales, auxiliares y agentes de la Administración de Justicia y peritos, y demás personal o autoridades en general; solicitar o practicar cualesquiera diligencias, incluso de carácter personal; recibir, realizar, intervenir o ejecutar, en la forma y con los medios previstos legalmente, cualesquiera actos de comunicación y de auxilio judicial; intervenir en cuantas comparecencias prevean las leyes, con denuncia o impugnación u oposición a la denuncia de óbices o presupuestos procesales de todo tipo, incluidos la jurisdicción, la competencia, la capacidad procesal, la acumulación de acciones de todo tipo, la acumulación de autos, los intentos de transacción o conciliación previstos legalmente, la subsanación de defectos procesales y la integración de la litis; someterse a competencias o acordar la sumisión a arbitraje; oponerse a la demanda o a las alegaciones con cualquiera de las conductas posibles y admitidas en Derecho, incluida la reconvención; proponer y practicar pruebas, incluso con carácter anticipado; tachar testigos y peritos; formular resúmenes de prueba o conclusiones; instar, promover e intervenir en diligencias finales; solicitar suspensiones procesales y, en particular, la suspensión del curso de los autos, del procedimiento o de la vista; solicitar, promover o pedir cualesquiera medidas cautelares y, en particular, pedir, prestar, cancelar y retirar embargos, anotaciones preventivas, depósitos y fianzas, mandamientos de pago; cobrar, consignar y pagar créditos en metálico o por cualquier otro medio admitido en Derecho las cantidades que procedan procesal o procedimentalmente y por el uso de este poder; asistir a juntas con voz y voto; tomar parte en subastas; solicitar, conceder y aceptar quitas y esperas; nombrar síndicos, administradores, interventores y auditores; promover y continuar por todos sus trámites cualesquiera incidentes o crisis procesales.

ACTOS DE DISPOSICIÓN PROCESAL

Especialmente faculta para que puedan realizar en su nombre cualesquiera actos de disposición o terminación anormal del proceso, dentro de los límites legalmente fijados, incluidos la transacción, suspensión, desistimiento, renuncia, allanamiento y sometimiento a arbitraje, con petición, en su caso, de homologación al órgano jurisdiccional de cualquier otra fase o instancia del proceso, así como las manifestaciones o actos que impliquen satisfacción extraprocesal de la pretensión o carencia sobrevenida de objeto, según lo dispuesto en el artículo 25 de la Ley de Enjuiciamiento Civil.

COPIAS DE PODER

Pedir y retirar copias de este poder.

FACULTADES DE APODERAMIENTO

Especialmente se faculta al Letrado o Letrados (o al Procurador o Procuradores) designados por el poderdante para que puedan elegir libremente al Procurador (o al Letrado) que haya de intervenir, otorgando a tal fin los apoderamientos que sean precisos.

FACULTAD PARA FORMULAR DECLARACIONES

Especialmente se les faculta para que puedan formular declaraciones en nombre de [NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL DEL PODERDANTE].

Así lo dice y otorga el/la compareciente (o los comparecientes), quien/es, enterado/s de su derecho a leer por sí este documento, procedo por su elección a la lectura del mismo, en cuyo contenido se ratifica/n y firma/n.

Y yo, el Notario, DOY FE de identificar a los comparecientes por medio de sus documentos nacionales de identidad y de todo lo demás contenido en este instrumento público, extendido en [Nº DE FOLIOS] folios de papel timbrado de uso exclusivamente notarial, de la serie [SERIE], números [NÚMEROS].

Firmas de los comparecientes y firma y signo del Notario.
