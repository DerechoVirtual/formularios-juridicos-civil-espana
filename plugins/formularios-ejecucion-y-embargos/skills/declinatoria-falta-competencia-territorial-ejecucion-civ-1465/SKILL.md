---
name: declinatoria-falta-competencia-territorial-ejecucion-civ-1465
description: "Declinatoria por falta de competencia territorial en la ejecución de un acuerdo de media - variante 2. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Declinatoria por falta de competencia territorial en la ejecución de un acuerdo de media - variante 2

> Formulario **CIV-1465** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Escrito en el que el ejecutado reconduce la competencia territorial aplicable en ejecución forzosa de acuerdo de mediación iniciada sin previo procedimiento judicial abierto

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Declinatoria por falta de competencia territorial en la ejecución de un acuerdo de media - variante 2» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Declinatoria por falta de competencia territorial en la ejecución de un acuerdo de media - variante 2” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:declinatoria-falta-competencia-territorial-ejecucion-civ-1465`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (5 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] Nº (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] AÑO (2 veces)
- [ ] NOMBRE DE LA INSTITUCIÓN DE MEDIACIÓN (2 veces)
- [ ] SEDE (2 veces)
- [ ] CALLE
- [ ] COLEGIO
- [ ] DENOMINACIÓN SOCIAL
- [ ] FECHA
- [ ] LUGAR
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] NOMBRE DEL SOLICITANTE
- [ ] Nº DE PROCEDIMIENTO

## Normas que cita el formulario

- art. 63.2 LEC
- art. 63.1 LEC
- art. 65.5 LEC
- art. 545.2 LEC
- art. 59 LEC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a. de los Tribunales y de la entidad [DENOMINACIÓN SOCIAL], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño a este escrito, bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS], colegiado n.º [NÚMERO] del Iltre. Colegio de Abogados de [COLEGIO], con despacho abierto en [LOCALIDAD], calle [CALLE], en calidad de ejecutado en los autos de ejecución n.º [Nº DE PROCEDIMIENTO]/[AÑO] seguidos a instancia de [NOMBRE DEL SOLICITANTE]; comparezco y como mejor en Derecho proceda, DIGO

Que por medio del presente escrito, formulo declinatoria por falta de competencia territorial en el plazo legal de cinco días posteriores a aquél en que ha recibido la primera notificación del proceso de ejecución, y ello conforme a los siguientes:

HECHOS

PRIMERO.- Que mi principal ha sido notificado del auto que despachaba ejecución en el procedimiento de referencia y el correlativo decreto del Letrado/a de la Administración de Justicia en el que se embargaba el saldo contenido en la cuenta corriente n.º [NÚMERO], junto con copia de la demanda ejecutiva de la representación de [NOMBRE DEL REPRESENTADO/A], para que en cualquier momento pueda personarse en la ejecución, y oponerse a la misma, si lo estimara oportuno, en el plazo de diez días.

SEGUNDO.- Que dicha ejecución deriva de acuerdo alcanzado por las partes en el proceso de mediación con nº [Nº]/[AÑO] desarrollado ante la Institución [NOMBRE DE LA INSTITUCIÓN DE MEDIACIÓN], con sede en la localidad de [LOCALIDAD] y dirigida por el mediador D./Dña. [NOMBRE Y APELLIDOS]; habiéndose desarrollado todo el procedimiento y firmado el acuerdo en las dependencias de aquella. Se aportan como documentos n.º [NÚMERO] y [Nº] copias del acta constitutiva y del acta final, en los que se comprueban tales circunstancias.

A dichos hechos son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

PRIMERO.- El presente escrito se presenta ante el Tribunal a quien tengo el honor de dirigirme, el cual está conociendo del asunto, conforme a lo dispuesto en los arts. 63.2 y 547 LEC, puesto que se ha despachado ejecución y se le considera competente por la parte ejecutante.

SEGUNDO.- Conforme a lo dispuesto en los arts. 63.1 y 547 LEC, mi mandante tiene personalidad jurídica propia y actúa por medio de sus representantes legales, con plena capacidad para ser parte y comparecer en juicio, estando legitimada para proponer esta cuestión de competencia, al haberse dirigido frente a ella la presente ejecución.

TERCERO.- Tratándose de una ejecución en la que se reclama una cantidad superior a 2.000 euros, se comparece con Procurador de los Tribunales habilitado ante el tribunal, y con dirección de Letrado en ejercicio que redacta y suscribe (art. 539.1 párrafo 3.º LEC).

CUARTO.- La declinatoria constituye el cauce común para plantear cualquier defecto de jurisdicción y competencia (art. 63.1 LEC), siendo su trámite el del art. 65, al cual se remite, en la presente sede de ejecución, el art. 547 párrafo 2.º del mismo texto legal, y que en este supuesto abocará inhibir la competencia a favor de los Tribunales de Instancia de la localidad de [LOCALIDAD], con emplazamiento de las partes ante el mismo (art. 65.5 LEC), y surtirá el efecto de suspender, hasta que sea resuelta y mediante resolución del Letrado de la Administración de Justicia, el cómputo para oponerse a la ejecución, así como el desarrollo del procedimiento.

QUINTO.- De conformidad con lo dispuesto en los arts. 545.2 LEC y 26 de la Ley 5/2012, de 6 de julio, de mediación en asuntos civiles y mercantiles, la ejecución de los acuerdos alcanzados en un procedimiento de mediación distingue entre dos tipos de competencias. La primera, que se sitúa en el ámbito funcional, remite al Tribunal que haya homologado el acuerdo, y, por ende, haya dictado el título ejecutivo, en los supuestos en los que la mediación, en cuyo seno se alcanza el acuerdo, se haya iniciado tras la apertura de un procedimiento judicial, lógicamente suspendido, el cual debe cerrarse de dicha forma.

La segunda, lo que acontece en el presente caso, situada en el ámbito territorial, parte de las mediaciones iniciadas sin previo procedimiento judicial abierto, determinando el legislador que la competencia corresponde al órgano judicial en cuyo partido judicial se haya firmado el acuerdo de mediación. Y así, la ejecución que nos ocupa se ha instado ante este Tribunal de Instancia en cuyo partido judicial tiene mi mandante su domicilio social, que es diferente del partido judicial donde se firmó el acuerdo, y se desarrolló todo el procedimiento de mediación; el cual fue, en concreto, el de la localidad de [LOCALIDAD] donde tiene su sede y dependencias habilitadas para ello, la Institución Mediadora [NOMBRE DE LA INSTITUCIÓN DE MEDIACIÓN].

En consecuencia, de acuerdo con el art. 59 LEC, mi mandante puede denunciar mediante declinatoria la falta de competencia territorial del tribunal a quien tengo el honor de dirigirme, por haberse firmado el acuerdo en diferente partido judicial, procediendo que, tras la tramitación del presente incidente, se dicte auto por el cual el tribunal se inhiba a favor de la Sección Civil del Tribunal de Instancia de [SEDE] que por turno corresponda, con emplazamiento de las partes.

Por lo expuesto,

En virtud de todo lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito con sus copias, se sirva admitir uno y otras, tenerme por comparecido y parte en la representación que ostento, a los solos efectos de plantear la presente declinatoria, ordenando se extiendan conmigo las sucesivas diligencias y notificaciones; y por promovida en tiempo y forma DECLINATORIA por FALTA DE COMPETENCIA TERRITORIAL, y conforme a lo interesado en el cuerpo de este escrito, con suspensión del cómputo para formular la oposición a la ejecución, se de traslado a la parte contraria, y seguido que sea todo el pertinente procedimiento, venga a dictarse resolución que inhiba la competencia a favor de las secciones civiles de los tribunales de instancia de [LOCALIDAD], con emplazamiento de las partes ante el mismo, con expresa imposición a la parte actora de las costas hasta entonces devengadas.

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a

========================================================================
