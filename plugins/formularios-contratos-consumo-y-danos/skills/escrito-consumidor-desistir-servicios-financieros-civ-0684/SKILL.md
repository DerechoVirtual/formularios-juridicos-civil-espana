---
name: escrito-consumidor-desistir-servicios-financieros-civ-0684
description: "Escrito del consumidor para desistir de servicios financieros contratados a distancia. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito del consumidor para desistir de servicios financieros contratados a distancia

> Formulario **CIV-0684** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito del consumidor para desistir de servicios financieros contratados a distancia» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito del consumidor para desistir de servicios financieros contratados a distancia” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:escrito-consumidor-desistir-servicios-financieros-civ-0684`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (4 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] TIPO DE SERVICIO FINANCIERO (2 veces)
- [ ] DENOMINACIÓN SOCIAL
- [ ] DNI/NIE
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] MEDIO DE CONTRATACIÓN A DISTANCIA
- [ ] OTROS DATOS
- [ ] PLAZO
- [ ] TIPO DE CONTRATO
- [ ] ÓRGANO

## Normas que cita el formulario

- art. 10 Ley 22/2007
- art. 10.3 Ley 22/2007
- art. 7.1.3.a Ley 22/2007

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

Escrito del consumidor de los servicios financieros a distancia al proveedor de dicho servicio, para el desistimiento del mismo. Las instrucciones y condiciones del derecho de desistimiento deberán constar en el contrato (art. 7.1.3) de la Ley 22/2007), además, la información de dicho apartado 1 deberá suministrarse de una forma clara y comprensible en la técnica a distancia utilizada. Conforme al art. 10 Ley 22/2007, la cláusula de desistimiento deberá recoger la duración, condiciones e información relativa al importe que el consumidor pueda tener que hacer frente conforme al art. 11 Ley 22/2007. Se considerarán servicios financieros todos los recogidos en el art. 2 de la Ley 22/2007 y, a distancia, lo recogido en el art. 4.3 Ley 22/2007. El art. 10.3 prevé que la comunicación debe hacerse en papel o sobre otro soporte duradero, disponible y accesible al destinatario. (ej. Burofax).


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

En [LUGAR], a [FECHA].

Yo, D./Dª [NOMBRE Y APELLIDOS], consumidor adquirente, del [TIPO DE SERVICIO FINANCIERO] el día [FECHA] con DNI/NIE [DNI/NIE] y con domicilio sito en [LOCALIDAD] actuando en mi propio nombre y representación, vengo a ejercitar el derecho de desistimiento en virtud de lo recogido en el art. 10 de la Ley 22/2007, sobre comercialización a distancia de servicios financieros destinados a los consumidores, antes de la finalización de los
14 días
30 días
  de plazo que se prevén en el articulado.

Por lo cual,

EXPONGO:

PRIMERO.- Datos del servicio financiero contratado

Que, el día [FECHA] Suscribí con D./Dª [NOMBRE Y APELLIDOS] un [TIPO DE SERVICIO FINANCIERO] con la compañía [DENOMINACIÓN SOCIAL] mediante introducir el [MEDIO DE CONTRATACIÓN A DISTANCIA] con número de contrato

SEGUNDO.- Cumplimiento del plazo de desistimiento

Que, tal y como queda recogido de forma clara y fehaciente en el contrato y sin haber transcurrido el plazo de [PLAZO]
14 días
30 días
  que otorga el art. 10 de la Ley 22/2007, vengo a ejercer mi derecho a desistimiento del producto contratado mediante el presente escrito, el cual se interpone, tal y como apercibe el art. 10.3 de la Ley 22/2007 en un soporte duradero, disponible y accesible antes de la expiración del plazo.

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]
— (En caso de que el contrato de servicios financieros cumpla con todos los requisitos de la norma y el proveedor no lo haya ejecutado)
— (En caso de que la información recogida en el contrato sea defectuosa conforme a los requisitos previstos en el art. 7.1.3.a) Ley 22/2007) [OTROS DATOS])
— (En caso de que el proveedor haya ejecutado el contrato de servicio financiero antes de finalizar el plazo de derecho de desistimiento sin consentimiento del consumidor)

CUARTO.- Comunicación expresa de desistimiento

Que, por consiguiente, y conforme a lo concertado en los arts. 10 y 11 de la Ley 22/2007, destinados a los consumidores, vengo a ejercer mi derecho a la resolución del contrato referido de manera unilateral y sin penalización alguna por realizarse dentro de los
14 días
30 días
  de plazo desde la firma del contrato de [TIPO DE CONTRATO].

Por lo anteriormente expuesto,

SOLICITO:

Que se proceda a la supresión de la gestión de cobro de cualquier tipo y al reembolso de la cantidad ya abonada mediante [ÓRGANO] el pasado día [FECHA] salvo aquellas partes que sí que se corresponden al servicio financiero suministrado por ustedes conforme al contrato hasta el día de recepción de la presente comunicación.

Fdo.
