---
name: otrosi-demanda-impugnacion-acuerdos-comunitarios-pide-civ-1249
description: "Otrosí de la demanda de impugnación de acuerdos comunitarios que pide su suspensión cautelar. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Otrosí de la demanda de impugnación de acuerdos comunitarios que pide su suspensión cautelar

> Formulario **CIV-1249** del plugin **Medidas cautelares y diligencias preliminares** (`formularios-medidas-cautelares-civiles`) · Civil › Medidas cautelares y diligencias preliminares · normativa revisada el 24-11-2026.

## Qué es

Otrosí de demanda de impugnación de acuerdos de la Junta de Propietarios solicitando la suspensión cautelar de los mismos en régimen de propiedad horizontal.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Otrosí de la demanda de impugnación de acuerdos comunitarios que pide su suspensión cautelar» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Otrosí de la demanda de impugnación de acuerdos comunitarios que pide su suspensión cautelar” para mi caso». También puedes invocarla directamente con `/formularios-medidas-cautelares-civiles:otrosi-demanda-impugnacion-acuerdos-comunitarios-pide-civ-1249`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-medidas-cautelares-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Medidas cautelares y diligencias preliminares) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] CALLE
- [ ] LOCALIDAD
- [ ] LUGAR

## Normas que cita el formulario

- art. 723.1 LEC
- art. 733 LEC
- art. 727.11.ª LEC
- art. 728 LEC
- art. 18 LPH
- art. 18.4 LPH
- art. 728.3 LEC
- art. 728.2 LEC

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

OTROSÍ DIGO que considerándose necesaria para asegurar la efectividad de la tutela judicial que se quiere se otorgue en la sentencia estimatoria que se dicte en este proceso, esta parte solicita la adopción de la MEDIDA CAUTELAR consistente en la SUSPENSIÓN CAUTELAR DEL ACUERDO IMPUGNADO, con fundamento en los siguientes:

HECHOS

ÚNICO-

Se reproducen los hechos y las valoraciones sobre los mismos que se han dejado expresados en el cuerpo de la demanda principal; si bien conviene tener presente, a fin de resolver sobre la adopción de la medida cautelar solicitada, que la instante de dicha medida es propietaria del local de oficinas sito en la Comunidad de Propietarios de la casa señalada con el número [NÚMERO] de la calle [CALLE] de [LOCALIDAD], estando dotada dicha finca de diversos ascensores y un montacargas, este último con parada en todas las plantas del edificio, salvo en la segunda, en la que está ubicada la finca de la actora; e igualmente, que el acuerdo que es objeto de impugnación en el pleito principal prohíbe el uso de los ascensores comunitarios para carga de bultos y servicios de mensajería y reparaciones de las personas que accedían al edificio a cumplir dichos cometidos, por lo que las personas que acceden a la planta segunda, en la que está ubicada la oficina de la actora, no pueden hacer uso de los ascensores cuando van a realizar tales cometidos, debiendo acceder bien por la escalera o bien subir al piso tercero de la finca y luego bajar por las escaleras comunitarias.

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA.

Conforme al art. 723.1 LEC corresponde resolver esta petición al Tribunal de Instancia al que me dirijo, puesto que el proceso cautelar que se inicia con la demanda del proceso del que resulta instrumental es competencia funcional del órgano competente para conocer del proceso principal, como se ha razonado lo es.

II.- PROCEDIMIENTO.

La solicitud de medida cautelar se sustancia, tratándose de procedimiento ordinario con audiencia del adverso, conforme a los arts. 733 a 738 LEC.

III.- MEDIDA SOLICITADA.

Se solicita una medida cautelar, resultado de la relación de los arts. 727.11.ª LEC y 18.4 LPH, de suspensión cautelar del acuerdo impugnado.

Los arts. 721 y ss. LEC establecen los presupuestos y requisitos que con carácter general deben concurrir para la adopción de medidas cautelares, siendo necesario, como de forma expresa señala el art. 728 LEC, la apariencia de buen derecho, un peligro por la mora procesal y la prestación de fianza o caución.

Ahora bien, ha de destacarse que al lado de las reglas generales que se establecen en los preceptos citados en cuanto al tipo de medidas a adoptar, así como los requisitos generales para ello, el propio art. 727.11.ª LEC viene a establecer la posibilidad de adoptar otra serie de medidas que para la protección de ciertos derechos establezcan determinadas leyes.

Así, el art. 18 LPH reconoce a los copropietarios la facultad de impugnar los acuerdos adoptados por la junta general de la comunidad de propietarios cuando se den alguno de los supuestos que establece dicho precepto, señalando el apartado 4 de dicho precepto que tales acuerdos serán ejecutivos, aunque sean impugnados, salvo que el Juez acuerde la suspensión, a petición del impugnante.

De la regulación concreta y específica de dicha medida cautelar, se pone de relieve sus peculiaridades, dado que, si bien mantiene esa finalidad general de toda medida cautelar, cual es que puedan producirse situaciones durante la pendencia del proceso que impidieran o dificultaran la tutela que pudiera ser otorgada en virtud de una sentencia firme, la suspensión cautelar de los acuerdos adoptados por parte de la comunidad de propietarios, aparte de dicha finalidad general, tiene a su vez una función específica, cual es evitar que, ante un acuerdo impugnado y que aparentemente pueda ser nulo o anulable, durante la tramitación del proceso, pueda desplegar sus efectos y, en consecuencia, causar una situación de hecho y unos perjuicios que serán de difícil o imposible reparación, aun cuando se proceda a la anulación del acuerdo.

El citado art. 18.4 LPH dispone que la impugnación de los acuerdos de la junta no suspenderá su ejecución, salvo que el juez así lo disponga con carácter cautelar, de manera que la suspensión del acuerdo requiere la concurrencia de los requisitos antes referidos contenidos en el art. 728 LEC.

Concurre la apariencia de buen derecho, acreditada más que indiciariamente, en cuanto se pone de relieve que los ascensores cuyo uso parcialmente se ha limitado por el acuerdo de la comunidad, es un elemento común del inmueble, del que pueden o deben poder hacer uso, con arreglo a su destino, todos los miembros de la comunidad, sin que en los estatutos de la comunidad, ni en el título constitutivo de la misma se recoja alguna limitación al uso de los ascensores, y de forma muy especial para dar el servicio correspondiente a la oficina de la actora que no está dotada del servicio de montacargas.

En cuanto al segundo de los requisitos, ha de ponerse de relieve que, en este caso, la medida cautelar tiene como finalidad no sólo posibilitar que en el futuro pueda ejecutarse la sentencia que pudiera dictarse, sino impedir que, en virtud del carácter ejecutivo de los acuerdos de la comunidad, aunque hayan sido impugnados, en base a lo establecido en el art. 18.4 LPH, puedan desplegar la totalidad de sus efectos y, por lo tanto, como ya se ha expuesto, causar unos daños, como es la limitación del uso de los ascensores comunitarios para dar servicio a la oficina de la actora, lo que indudablemente causa, o puede entenderse de modo razonable, que ha de causar una serie de molestias, incomodidades y perjuicios en el uso y explotación de la oficina de la actora, si no de imposible, sí de difícil reparación.

El art. 728.3 LEC, por su parte, viene a establecer la necesidad de que por parte del instante de la medida cautelar se preste la caución que se considere suficiente para responder de una forma directa e inmediata de los daños y perjuicios que la medida cautelar pudiera causar en el patrimonio del demandado.

Con relación a estos requisitos ha de ponerse de relieve que tanto la exigencia o no de la caución, como de la cuantía de la misma, el art. 728.2 LEC exige por parte del Juez un juicio indiciario sobre el fundamento de la pretensión del solicitante de la medida cautelar sin que ello suponga prejuzgar el fallo, debiendo ser tal juicio provisorio uno de los elementos esenciales que debe tener en cuenta el órgano judicial a la hora de valorar tanto la exigencia de la caución como de fijar el importe de dicha caución, así como los daños que dicha medida cautelar pudiera ocasionar.

En base a todos los criterios, en cumplimiento de este tercer presupuesto, esta parte se ofrece a prestar aval bancario a primer requerimiento, por importe de [IMPORTE] EUROS ( [IMPORTE] €) cantidad que entendemos más que suficiente para responder de los eventuales perjuicios que la medida cautelar pudiera causar al demandado en el improbable caso de que sean desestimadas nuestras pretensiones; en cualquier caso, esta parte ofrece prestar la caución que se fije por el Tribunal, de ser ésta superior a la ofrecida anteriormente, y en la forma que se determine.

De conformidad con el art. 732.2, párrafo 3.º LEC, se propone la práctica de prueba documental y de interrogatorio de la parte contraria para la acreditación de los presupuestos de la medida cautelar, señalándose como documentos los que acompañan la demanda principal.

En su virtud,

SUPLICO AL TRIBUNAL

que, teniendo por presentada la presente solicitud, se sirva admitirla y previos los trámites legales oportunos, se dicte auto por el que se acuerde la suspensión cautelar del acuerdo adoptado en la Junta de Propietarios de la Comunidad demandada de fecha [FECHA], señalado en su apartado de número [NÚMERO] del orden del día, por el cual se prohíbe el uso de ascensores comunitarios para la carga de bultos, y su uso al personal de mensajería, o de reparación o mantenimiento; acuerdo cuyo contenido se consigna en el cuerpo de este escrito.

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a

========================================================================
