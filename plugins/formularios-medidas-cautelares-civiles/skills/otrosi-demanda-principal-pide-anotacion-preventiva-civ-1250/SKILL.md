---
name: otrosi-demanda-principal-pide-anotacion-preventiva-civ-1250
description: "Otrosí de la demanda principal que pide anotación preventiva de demanda con audiencia del demandado. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Otrosí de la demanda principal que pide anotación preventiva de demanda con audiencia del demandado

> Formulario **CIV-1250** del plugin **Medidas cautelares y diligencias preliminares** (`formularios-medidas-cautelares-civiles`) · Civil › Medidas cautelares y diligencias preliminares · normativa revisada el 24-11-2026.

## Qué es

Otrosí de la demanda principal por el que se solicita, con audiencia del demandado, la medida cautelar de anotación preventiva de demanda en el Registro de la Propiedad (arts. 727.5.ª y 733 a 738 LEC y art. 42 de la Ley Hipotecaria), para evitar que la transmisión del inmueble litigioso a un tercero protegido registralmente frustre la sentencia.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Otrosí de la demanda principal que pide anotación preventiva de demanda con audiencia del demandado» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Otrosí de la demanda principal que pide anotación preventiva de demanda con audiencia del demandado” para mi caso». También puedes invocarla directamente con `/formularios-medidas-cautelares-civiles:otrosi-demanda-principal-pide-anotacion-preventiva-civ-1250`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-medidas-cautelares-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Medidas cautelares y diligencias preliminares) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FIRMA (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] AÑO
- [ ] DESCRIBIR LAS GESTIONES Y SU PRUEBA
- [ ] DÍA
- [ ] IMPORTE
- [ ] MES

## Normas que cita el formulario

- art. 723.1 LEC
- art. 733 LEC
- art. 727.5.ª LEC
- art. 42 LH
- art. 73 LH
- art. 721.1 LEC
- art. 726.1.1.ª LEC
- art. 731 LEC
- art. 726.1.2.ª LEC
- art. 728.2 LEC
- art. 728.1 LEC
- art. 32 LH
- art. 728.3 LEC
- art. 732.2 LEC

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

OTROSÍ DIGO. Esta parte solicita la adopción de la MEDIDA CAUTELAR DE ANOTACIÓN PREVENTIVA DE DEMANDA, con fundamento en los siguientes:

HECHOS

ÚNICO

Se reproducen los hechos y las valoraciones sobre los mismos que se han dejado expresados en el cuerpo de la demanda principal, si bien conviene tener presente, a los efectos de la presente solicitud de medida cautelar de anotación preventiva de demanda, que [ELEGIR: los demandados / el demandado] han comenzado a realizar gestiones para transmitir de nuevo el inmueble sobre el que versa el proceso [DESCRIBIR LAS GESTIONES Y SU PRUEBA], y la adquisición con carácter de irreivindicable por un tercero protegido registralmente haría imposible la tutela efectiva de la sentencia que pudiera recaer.

FUNDAMENTOS DE DERECHO

I.– COMPETENCIA

Conforme al art. 723.1 LEC, corresponde resolver esta petición al Tribunal de Instancia al que me dirijo, puesto que el proceso cautelar que se inicia con la demanda del proceso del que resulta instrumental es competencia funcional del órgano competente para conocer del proceso principal, como se ha razonado que lo es.

II.– PROCEDIMIENTO

La solicitud de medida cautelar se sustancia, tratándose de procedimiento ordinario con audiencia del adverso, conforme a los arts. 733 a 738 LEC.

III.– MEDIDA SOLICITADA

Se solicita una medida cautelar resultado de la relación de los arts. 727.5.ª LEC y 42.1.º de la Ley Hipotecaria (LH), de anotación preventiva de demanda.

Conforme al art. 727.5.ª LEC, podrá acordarse la medida cautelar de anotación preventiva de demanda cuando esta se refiera a bienes o derechos susceptibles de inscripción en Registros públicos; y el art. 42 LH faculta para pedir anotación preventiva de sus derechos en el Registro de la Propiedad al que demandare en juicio la propiedad de bienes inmuebles o la constitución, declaración, modificación o extinción de cualquier derecho real.

Haciendo uso de la facultad expresada, se solicita la anotación preventiva de esta demanda, debiendo el mandamiento judicial para esta anotación expresar las circunstancias que deba esta contener, según resulten de los títulos y documentos aportados al pleito, a tenor de lo dispuesto en el art. 73 LH.

Justificación: Con objeto de asegurar la efectividad de la tutela judicial que pudiera otorgarse en la sentencia estimatoria que se dictare (art. 721.1 LEC), de modo que no pueda verse impedida o dificultada por situaciones producidas durante la pendencia del proceso correspondiente (art. 726.1.1.ª LEC), hay posibilidad de acordar, respecto de los bienes y derechos de la parte demandada, medidas cautelares, que serán provisionales, instrumentales al proceso iniciado (art. 731 LEC), variables conforme al principio rebus sic stantibus y siempre proporcionadas (art. 726.1.2.ª LEC).

Presupuestos: La cuestión objeto del proceso principal se corresponde con el ejercicio de una acción [ELEGIR: personal / real], por la que se pretende en esencia que se decrete que [DESCRIBIR LA PRETENSIÓN PRINCIPAL, por ejemplo, el contrato de compraventa en escritura pública otorgada ante notario por ambos demandados es nulo de pleno derecho por simulación absoluta o inexistencia de causa, o por ampararse en causa ilícita].

Ahora bien, resulta evidente su trascendencia registral, de manera que, según entiende esta parte, nada impide, acreditada más que indiciariamente la apariencia de buen derecho a que se refiere el art. 728.2 LEC, la adopción de esta medida.

En este sentido, el AAP Baleares, Secc. 3.ª, de 10 de enero de 2003, rec. 658/2002, declara que «la anotación preventiva de demanda, contemplada como medida cautelar específica en el artículo 727.5.ª de la Ley de Enjuiciamiento Civil cuando se refiera a bienes o derechos susceptibles de inscripción en Registros públicos, tiene, según la jurisprudencia, un doble contenido: el procesal, conforme al cual se asegura que la sentencia que en su día recaiga tendrá la misma eficacia que si hubiera dictado ya en el día en que la anotación se practica, y el contenido sustantivo, a través del cual se consigue la ventaja que proporciona el principio de prioridad registral si el actor obtiene sentencia favorable (STS de 18 de noviembre de 1993, rec. 916/1991). Ahora bien, al venir regulada en la Ley Hipotecaria (artículo 42), las condiciones y procedimiento para poder ser solicitada, acordada e inscrita en el Registro de la Propiedad vienen reguladas en dicha Ley, al decir el artículo citado que "podrán pedir anotación preventiva de sus respectivos derechos en el Registro correspondiente […] el que demandare en juicio la propiedad de bienes inmuebles, o la constitución, declaración, modificación o extinción de cualquier derecho real", dicción literal que limita la anotación preventiva de demanda al ejercicio de una acción real pero, actualmente, superada por la doctrina de la Dirección General de los Registros y del Notariado en el sentido de permitir la anotación preventiva de demanda en ejercicio de acciones de crédito o personales con trascendencia real (RRDGRN de 6 de julio y 29 de septiembre de 1962 y 24 y 25 de junio de 1991, por todas), pero siempre que la sentencia que se dicte sea capaz de producir una inscripción en el Registro público que modifique su contenido, precisamente porque, como señala la doctrina científica, su función es evitar que, mientras se sustancia el proceso, se causen en el propio Registro inscripción o inscripciones contrarias o irreversibles que hagan imposible la inscripción o inscripciones que causaría la ejecución de sentencia».

El periculum in mora (art. 728.1 LEC) viene específicamente propiciado por los efectos de la fe pública registral que ampara a quien asiente el dominio o derecho real sobre el inmueble litigioso que puede haber adquirido durante la pendencia del proceso principal (arts. 32 y 34 LH).

Presupuesto de la ejecución de la medida cautelar (art. 728.3 LEC): se ofrece prestar la caución que al efecto prudencialmente se señale para indemnizar los perjuicios que de la anotación puedan seguirse a los demandados caso de ser absueltos, y que se considera puede ascender a [IMPORTE] euros (teniendo en cuenta el alcance limitado de la anotación preventiva de demanda, alcance que, entre otras, se recoge en la STS de 18 de noviembre de 1993, rec. 916/1991, en la que se señala que la anotación «no produce cierre registral, como ya destacó la Dirección General de los Registros en su resolución de 4-7-1919, puesto que los derechos a que se refiere pueden ser objeto de transmisiones aunque, como se ha dicho, subordinadas al resultado del proceso y efectos de la anotación pendiente»), prefiriéndose la fórmula de aval bancario a primer requerimiento por tiempo indefinido, con las condiciones que fije S.S.ª, oídas las partes.

Prueba: De conformidad con el art. 732.2, párrafo tercero, LEC, se propone la práctica de prueba documental y de interrogatorio de la parte contraria para la acreditación de los presupuestos de la medida cautelar, señalándose como documentos los que acompañan la demanda principal.

En su virtud,

SUPLICO AL TRIBUNAL

que, teniendo por recibida solicitud de medida cautelar, se digne admitirla y, convocándose por el Letrado de la Administración de Justicia a las partes para la vista, seguido que sea el oportuno trámite, practicándose la prueba que se propone, dicte Auto por el que se disponga, previa la prestación de la caución por la actora en la cuantía y forma que se señale, la anotación preventiva de la presente demanda, librándose al efecto el correspondiente mandamiento al Registro de la Propiedad de [LOCALIDAD], con entrega a esta parte para su diligenciado, todo ello con imposición de las costas del proceso cautelar a la parte contraria, si se resistiere a la adopción de la medida.

Es justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a: [FIRMA] Firma del Procurador/a: [FIRMA]
