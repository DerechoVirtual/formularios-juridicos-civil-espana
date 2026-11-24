---
name: solicitud-medidas-sobre-hijos-menores-ante-seccion-civ-0084
description: "Solicitud de medidas sobre hijos menores ante la Sección de Violencia sobre la Mujer. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de medidas sobre hijos menores ante la Sección de Violencia sobre la Mujer

> Formulario **CIV-0084** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de medidas sobre hijos menores ante la Sección de Violencia sobre la Mujer» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de medidas sobre hijos menores ante la Sección de Violencia sobre la Mujer” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:solicitud-medidas-sobre-hijos-menores-ante-seccion-civ-0084`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] Nº (4 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] EDAD (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] SEDE (2 veces)
- [ ] AÑO
- [ ] COLEGIO
- [ ] DÍA
- [ ] FECHA
- [ ] IMPORTE
- [ ] LUGAR
- [ ] MES
- [ ] Nº DE COLEGIADO/A
- [ ] Nº DE CUENTA (IBAN)
- [ ] NÚMERO
- [ ] PETICIÓN

## Normas que cita el formulario

- art. 6 LEC
- art. 23 LEC
- art. 769.3 Ley 1/2000
- art. 85.1 LOPJ

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

A LA SECCIÓN DE VIOLENCIA SOBRE LA MUJER DEL TRIBUNAL DE INSTANCIA [SEDE]

D./DÑA. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en nombre y representación de Dña. [NOMBRE Y APELLIDOS], mayor de edad, con domicilio en [LOCALIDAD], núm. [Nº], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], comparezco ante el Tribunal y como mejor proceda en Derecho, bajo la dirección técnica del Letrado D./Dña. [NOMBRE Y APELLIDOS] con número de colegiado [Nº DE COLEGIADO/A] del Ilustre Colegio de Abogados de [COLEGIO] DIGO:

Que por el presente, y siguiendo las expresas instrucciones de mi representado/a formula demanda sobre guarda y custodia de hijos menores contra D. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD] en la calle, número [NÚMERO], en solicitud de la adopción de la siguientes medidas [PETICIÓN] y ello en base a los siguientes

HECHOS

PRIMERO Que ha mantenido una relación sentimental con el demandado que duró [Nº] años, fruto de la cual nacieron los hijos:

1º [NOMBRE Y APELLIDOS] de años [EDAD] de edad

2º [NOMBRE Y APELLIDOS] de años [EDAD] de edad

SEGUNDO Que a la fecha de hoy no ha pasado contribución alguna para el levantamiento de las cargas familiares.

TERCERO Que actualmente la demandada se encuentra en situación de paro laboral, por lo que está pasando dificultades económicas al sustento de los hijos, recibiendo ayuda de sus padres.

CUARTO Que actualmente, tiene orden de protección dictada por la Sección de Violencia sobre la Mujer del Tribunal de Instancia de [SEDE] en fecha [FECHA]

Acompañamos en prueba de ello los siguientes documentos [Nº DE DOCUMENTO] a [Nº DE DOCUMENTO]

A los anteriores hechos son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

Las partes están capacitadas activa y pasivamente para entablar la presente relación jurídico-procesal, según lo previsto en los artículos 6 y siguientes de la LECiv.

En cuanto a la postulación es de aplicación el artículo 23 y siguientes de la LECiv.

Respecto al procedimiento a seguir corresponde al previsto en el artículo 769.3 de la Ley 1/2000, de 7 de enero, de Enjuiciamiento Civil, en relación con lo dispuesto en el art. 85.1º LOPJ, que atribuyen a la Sección Civil del Tribunal de Instancia del lugar del último domicilio común de los progenitores la competencia para conocer de los procesos que versen exclusivamente sobre guarda y custodia de hijos menores o sobre alimentos reclamados por un progenitor contra el otro en nombre de los hijos.

El artículo 394 de la Ley de Enjuiciamiento Civil sobre costas que deberán ser impuestas a la parte demandada.

Por todo lo cual,

SUPLICO AL TRIBUNAL: Que teniendo por presentada esta demanda junto con sus documentos y copias de todo ello, se sirva admitirla y tenerme por personado y parte en la representación que ostento y por formulada demanda sobre custodia y guarda de hijos menores contra D. [NOMBRE Y APELLIDOS] y previos los trámites legales se dicte resolución por la que:

a) Que los hijos [NOMBRE Y APELLIDOS] y [NOMBRE Y APELLIDOS] han de quedar bajo la guarda y custodia de Dña. sin perjuicio de la patria potestad compartida, y fijar un régimen de visitas que el Juzgador estime más adecuado para el cónyuge no custodio.

b) Fijar como cantidad en concepto de alimentos la de [IMPORTE] euros en 12 mensualidades, la cual se deberá incrementar anualmente con arreglo al IPC, que deberá ser ingresar cada mes antes del día cinco en la cuenta bancaria [Nº DE CUENTA (IBAN)] número de cuenta.

Es de justicia que pido en [LUGAR], a [DÍA], de [MES], de [AÑO]

Firma de Letrado

Col. núm. [Nº]

Firma de Procurador

Col. núm. [Nº]

========================================================================
