---
name: solicitud-medidas-cautelares-previas-demanda-parejas-civ-1222
description: "Solicitud de medidas cautelares previas a la demanda en parejas de hecho. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de medidas cautelares previas a la demanda en parejas de hecho

> Formulario **CIV-1222** del plugin **Medidas cautelares y diligencias preliminares** (`formularios-medidas-cautelares-civiles`) · Civil › Medidas cautelares y diligencias preliminares · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de medidas cautelares previas a la demanda en parejas de hecho» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de medidas cautelares previas a la demanda en parejas de hecho” para mi caso». También puedes invocarla directamente con `/formularios-medidas-cautelares-civiles:solicitud-medidas-cautelares-previas-demanda-parejas-civ-1222`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-medidas-cautelares-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Medidas cautelares y diligencias preliminares) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (10 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] IMPORTE (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] AÑO (2 veces)
- [ ] CALLE (2 veces)
- [ ] DIRECCIÓN (2 veces)
- [ ] FECHA (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] DÍA
- [ ] LUGAR
- [ ] MES
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] NOMBRE Y APELLIDOS DEL ABOGADO
- [ ] Nº DE FAX
- [ ] OTROS DATOS
- [ ] SEDE

## Normas que cita el formulario

- art. 727 LEC
- art. 732.2 LEC
- art. 723.1 LEC
- art. 721 LEC
- art. 730.2 LEC
- art. 733.2 LEC
- art. 728.2 LEC
- art. 728.1 LEC
- art. 732 LEC

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

D. [NOMBRE Y APELLIDOS] Procurador de los Tribunales, actuando en representación de [NOMBRE DEL REPRESENTADO/A], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], por medio de la presente solicito la adopción de MEDIDAS CAUTELARES PREVIAS A LA DEMANDA que pretendo deducir contra D. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], calle [CALLE] en base a los siguientes:

HECHOS

Mi mandante ha estado conviviendo de forma estable con el demandado D. desde el año [AÑO], teniendo como domicilio común la vivienda sita en [LOCALIDAD] calle [CALLE] (a efectos acreditativos acompaño como documentos [Nº DE DOCUMENTO]) (en cada caso se relacionarían los documentos que acreditan la convivencia [OTROS DATOS]) certificado de inscripción en el Registro de Uniones Estables del Ayuntamiento de [LOCALIDAD], certificado de empadronamiento, recibos de luz, agua o teléfono a nombre de mi mandante correspondiente a dicho domicilio, etc.), sin haber tenido descendencia común.

Por razones que no es el caso de exponer mi mandante y su pareja dieron por finalizada su relación el pasado día [FECHA], sin que llegaran a un acuerdo en relación a los bienes comunes, motivo por el cual se ve obligada a instar la adopción de medidas cautelares conforme a lo que se expone en el siguiente hecho.

La demanda que pretende interponer mi mandante se refiere concretamente a la vivienda familiar sita en [LOCALIDAD], finca registral número [NÚMERO] del Registro de la Propiedad [LOCALIDAD], la cual fue adquirida por mi mandante y su pareja de hecho a D. según consta en el contrato privado de compraventa de fecha [FECHA] que se acompaña como documento número

Pese a que la vivienda fue adquirida por la pareja, por razones fiscales la misma fue inscrita en el Registro de la Propiedad exclusivamente a nombre del demandado D. [NOMBRE Y APELLIDOS], si bien mi mandante ostenta la titularidad de una cuota indivisa de la mitad de la referida vivienda, según consta claramente en el contrato, motivo por el cual pretende ejercitar la correspondiente acción en el proceso subsiguiente a la pretensión cautelar.

En aras a la tutela efectiva de los intereses de esta parte, mi representada se ve en la obligación de instar urgentemente la adopción de la medida cautelar de prohibición de disponer y su anotación en el Registro de la Propiedad de [LOCALIDAD], conforme a los apartados 6 y 11 del art. 727 de la LEC, puesto que concurren razones de urgencia en tanto que el demandado D. [NOMBRE Y APELLIDOS], ignorando los derechos de mi mandante, ha puesto en venta la vivienda ofertándola en diversos medios de comunicación y en varias inmobiliarias de la localidad (acompaño como documentos copias de anuncios de prensa de venta de la vivienda y de anuncios de las inmobiliarias ofertando la enajenación de dicha vivienda).

Por estos motivos, y siendo necesaria la adopción de la medida cautelar, se interesa que se decrete con la mayor urgencia, sin audiencia del demandado, ofreciendo la constitución de una caución de [IMPORTE] euros para garantizar los daños y perjuicios que puedan irrogarse.

Para acreditar los anteriores hechos, y al amparo de lo que dispone el artículo 732.2 de la LEC, se acompañan a esta solicitud los documentos en que esta parte funda su derecho, relacionados en los hechos, interesándose, además, la práctica de los siguientes medios probatorios en orden a justificar la concurrencia de los presupuestos para la adopción de la medida cautelar:

- TESTIFICAL, de D. y D. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], los cuales pueden dar razón tanto de la situación de convivencia marital de las partes, la cotitularidad de la vivienda, así como sobre la urgencia de la medida al estar intentando enajenarla el demandado.

FUNDAMENTOS DE DERECHO

Competencia

Le corresponde al Tribunal al que me dirijo ya que es el competente para conocer de la demanda principal que se formule con fundamento en el art. 723.1 LEC.

Legitimación

Le corresponde a esta parte ante su condición de copropietaria de la vivienda adquirida durante la unión de pareja con el demandado y con ello futura actora de la demanda en ejercicio de la acción que se pretende interponer (art. 721 LEC).

Procedimiento

Es el previsto en el art. 730.2 LEC al interesarse la adopción de la medida cautelar son carácter previo a la interposición de la demanda y sin audiencia del demandado (art. 733.2 LEC) pues concurren en este caso razones de urgencia ante la decisión manifiesta del demandado de vender la vivienda que fue familiar, copropiedad de mi mandante.

Apariencia de buen derecho

Se deriva de la documentación adjunta a esta solicitud y en la que consta la condición de unión estable de pareja y la copropiedad de mi mandante sobre la vivienda (art. 728.2 LEC).

Peligro de mora

Se deriva de la resuelta voluntad del demandante de enajenar la vivienda sobre cuya titularidad proindivisa se va a interponer la demanda ya que solamente con la medida cautelar solicitada se podrá garantizar la efectividad de una eventual sentencia favorable que se pudiere dictar en beneficio de mi mandante (art. 728.1 LEC).

Medida interesada

Es la de prohibición de disponer sobre la vivienda sita [DIRECCIÓN], finca número [NÚMERO] inscrita en el Registro de la Propiedad de [LOCALIDAD], y la anotación preventiva de dicha prohibición en el citado Registro.

Caución

Con fundamento en el art. 732,3 LEC se solicita sea fijada ésta en [IMPORTE] € dado el valor del inmueble y los posibles perjuicios que se le pudieren generar por ello.

En base a lo anterior,

SUPLICO AL TRIBUNAL que tenga por presentado escrito con los documentos a él anejos y copias, tenga por comparecido a esta parte y, tras la práctica de la prueba que dejo interesada en el hecho cuarto, acuerde prohibir al demandado D. disponer sobre la vivienda sita [DIRECCIÓN], finca número [NÚMERO] inscrita en el Registro de la Propiedad de [LOCALIDAD], y la anotación preventiva de dicha prohibición en el citado Registro, inmueble éste frente al que esta parte tiene intención de interponer demanda en el plazo legalmente previsto para ello desde la adopción de la medida cautelar, solicitando que se acuerde la misma con carácter previo a la presentación de la demanda y sin audiencia del demandado al concurrir motivos de urgencia. Asimismo se interesa que en caso de decretarse se acuerde la anotación en el Registro de la Propiedad de [LOCALIDAD] e interesando que se remita el mismo por fax por razones de urgencia (número de fax [Nº DE FAX]). De cara a la adopción de tal medida cautelar se solicita asimismo que se tenga por ofrecida una caución de [IMPORTE] €.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma Abogado [NOMBRE Y APELLIDOS DEL ABOGADO] Firma Procurador

========================================================================
