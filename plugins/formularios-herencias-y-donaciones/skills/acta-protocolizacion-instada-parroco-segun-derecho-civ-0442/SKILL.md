---
name: acta-protocolizacion-instada-parroco-segun-derecho-civ-0442
description: "Acta de protocolización instada por el párroco según el Derecho catalán. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Acta de protocolización instada por el párroco según el Derecho catalán

> Formulario **CIV-0442** del plugin **Herencias, testamentos y donaciones** (`formularios-herencias-y-donaciones`) · Civil › Sucesiones y donaciones · normativa revisada el 24-11-2026.

## Qué es

Acta notarial de protocolización de un testamento otorgado ante párroco (por no haber notario en la localidad rural donde residía el testador), solicitada por el párroco ante notario dentro del plazo máximo de cuatro años que fija el Libro cuarto del Código Civil de Cataluña (Ley 10/2008, de 10 de julio).

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Acta de protocolización instada por el párroco según el Derecho catalán» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Acta de protocolización instada por el párroco según el Derecho catalán” para mi caso». También puedes invocarla directamente con `/formularios-herencias-y-donaciones:acta-protocolizacion-instada-parroco-segun-derecho-civ-0442`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-herencias-y-donaciones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Herencias, testamentos y donaciones) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] COLEGIO NOTARIAL (2 veces)
- [ ] NOMBRE DEL NOTARIO (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL PÁRROCO (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL TESTADOR (2 veces)
- [ ] Nº (2 veces)
- [ ] AÑO
- [ ] CLASE
- [ ] DÍA
- [ ] LOCALIDAD
- [ ] MES
- [ ] NOMBRE Y APELLIDOS DE LA MADRE
- [ ] NOMBRE Y APELLIDOS DEL PADRE
- [ ] NÚMEROS
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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Junto a «…amiento, de su seguridad y confidencialidad, el Notario titular de esta notaría.»: el original citaba la Orden del Ministerio de Justicia 484/2003, de 19 de febrero, sobre ficheros automatizados, hoy superada por el RGPD y la LOPDGDD; ajustar la cláusula informativa a la que use cada notaría.

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

Ante mí, [NOMBRE DEL NOTARIO], Notario/a del Ilustre Colegio Notarial de [COLEGIO NOTARIAL],

DICE

ÚNICO.– Que D./Dña. [NOMBRE Y APELLIDOS DEL TESTADOR], hijo/a de los consortes D. [NOMBRE Y APELLIDOS DEL PADRE] y D.ª [NOMBRE Y APELLIDOS DE LA MADRE], ambos fallecidos, otorgó testamento ante el Párroco D. [NOMBRE Y APELLIDOS DEL PÁRROCO], por no haber Notario en la localidad rural donde residía.

Que, habida cuenta de la obligación de protocolizar dicho testamento ante Notario en un plazo máximo de cuatro años, según la Ley 10/2008, de 10 de julio, del libro cuarto del Código Civil de Cataluña, relativo a las sucesiones, me solicita que protocolice el testamento cerrado que me entrega, en virtud del siguiente

REQUERIMIENTO

OBJETO

D./Dña. [NOMBRE Y APELLIDOS DEL PÁRROCO] me hace entrega de un testamento, escrito a máquina y extendido en [Nº] folios de papel común, firmados todos por D./Dña. [NOMBRE Y APELLIDOS DEL TESTADOR], para que lo examine, y me requiere para su protocolización.

ACEPTACIÓN

Yo, D./Dña. [NOMBRE DEL NOTARIO], Notario del Ilustre Colegio Notarial de [COLEGIO NOTARIAL], acepto el requerimiento, que cumplo con la protocolización del testamento que uno a esta matriz.

RESERVAS Y ADVERTENCIAS LEGALES

Se hacen al compareciente las advertencias legales, en especial las de carácter fiscal y registral.

Advierto también al compareciente de la incorporación de sus datos personales a los ficheros y tratamientos de esta notaría, conforme al Reglamento (UE) 2016/679 (RGPD) y a la Ley Orgánica 3/2018, de 5 de diciembre, de Protección de Datos Personales y garantía de los derechos digitales. Se entiende por consentimiento del afectado toda manifestación de voluntad libre, específica, informada e inequívoca por la que éste acepta, ya sea mediante una declaración o una clara acción afirmativa, el tratamiento de datos personales que le conciernen. Cuando se pretenda fundar el tratamiento de los datos en el consentimiento del afectado para una pluralidad de finalidades será preciso que conste de manera específica e inequívoca que dicho consentimiento se otorga para todas ellas. No podrá supeditarse la ejecución del contrato a que el afectado consienta el tratamiento de los datos personales para finalidades que no guarden relación con el mantenimiento, desarrollo o control de la relación contractual.

La finalidad de esta incorporación es facilitar la tramitación y seguimiento de esta escritura.

Es responsable del tratamiento, de su seguridad y confidencialidad, el Notario titular de esta notaría.

LECTURA

Permito al señor compareciente la lectura de esta escritura, porque así lo solicita, después de ser advertido de la opción del artículo 193 del Reglamento Notarial.

CONSENTIMIENTO

Enterado, según dice, por la lectura que ha practicado y por mis explicaciones verbales, el señor compareciente hace constar libremente su consentimiento al contenido de la escritura.

FIRMA

Y la firma.

AUTORIZACIÓN

Yo, el Notario, compruebo que este otorgamiento se adecúa a la legalidad y a la voluntad debidamente informada y expresada ante mí; y, con el contenido de esta escritura, extiendo en [Nº] folios de papel timbrado notarial de la clase [CLASE], serie [SERIE], números [NÚMEROS]. DOY FE.

Firma del compareciente y signo, firma y rúbrica del Notario autorizante.
