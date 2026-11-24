---
name: solicitud-aprobacion-judicial-acuerdo-mediacion-sobre-civ-0009
description: "Solicitud de aprobación judicial de un acuerdo de mediación sobre visitas de los abuelos. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de aprobación judicial de un acuerdo de mediación sobre visitas de los abuelos

> Formulario **CIV-0009** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de aprobación judicial de un acuerdo de mediación sobre visitas de los abuelos» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de aprobación judicial de un acuerdo de mediación sobre visitas de los abuelos” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:solicitud-aprobacion-judicial-acuerdo-mediacion-sobre-civ-0009`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] AÑO (5 veces)
- [ ] DÍA (5 veces)
- [ ] MES (5 veces)
- [ ] Nº DE DOCUMENTO (4 veces)
- [ ] NOMBRE DEL MENOR (2 veces)
- [ ] SEDE (2 veces)
- [ ] CORREO ELECTRÓNICO
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] NOMBRE DE LA INSTITUCIÓN DE MEDIACIÓN
- [ ] Nº
- [ ] Nº DE COLEGIADO
- [ ] Nº DE FAX

## Normas que cita el formulario

- art. 160 Código Civil
- art. 1811 LEC

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

### Avisos de actualización (4) — se aplican en el texto, nunca se copian en el documento

- Junto a «…MILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.
- Junto a «… 160 del Código Civil, ante la Sección Civil del Tribunal de Instancia de [SEDE]»: Un solo TI por partido judicial (art. 84.1 LOPJ): sobra «de los de». Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).
- Junto a «…dicción voluntaria regulado en los artículos 1811 y siguientes de la LEC de 1881»: La jurisdicción voluntaria de la LEC de 1881 está derogada; hoy rige la Ley 15/2015, de 2 de julio, de la Jurisdicción Voluntaria. Hay que citar el artículo equivalente.

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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D. [NOMBRE Y APELLIDOS] y Dª [NOMBRE Y APELLIDOS] actuando en su nombre y representación, y bajo la dirección Letrada de Don [NOMBRE Y APELLIDOS], [Nº DE COLEGIADO] al amparo de lo dispuesto en el artículo 160 del Código Civil, ante la Sección Civil del Tribunal de Instancia de [SEDE] que por turno de reparto corresponda comparezco y, como mejor proceda en Derecho,

DIGO:

Que mediante el presente escrito promueven expediente de jurisdicción voluntaria para la homologación del acuerdo de mediación de fecha [DÍA] de [MES] de [AÑO] que se acompaña como documento número [Nº DE DOCUMENTO] alcanzado con Dª [NOMBRE Y APELLIDOS], madre del menor [NOMBRE DEL MENOR] y nieto de los solicitantes, en base a los siguientes

HECHOS

Los promotores de este expediente son los abuelos del menor [NOMBRE DEL MENOR], actualmente de [Nº] años de edad.

El padre del menor, hijo de los solicitantes, era D. [NOMBRE Y APELLIDOS], quien falleció en fecha [DÍA] de [MES] de [AÑO] (acompaño como documentos [Nº DE DOCUMENTO] y [Nº DE DOCUMENTO] certificado de nacimiento del menor y de defunción del hijo de los solicitantes).

Al fallecer, el menor quedó bajo la guarda y custodia de su madre Dª [NOMBRE Y APELLIDOS], con quien se fue deteriorando la relación, al punto que no era posible una comunicación fluida, lo cual, durante un tiempo, afectó a la relación personal con el menor, al no ser posible comunicarse con él y visitarlo regularmente por parte de sus abuelos.

Ante esta situación, los solicitantes y la madre del menor decidieron de mutuo acuerdo acudir a un procedimiento de mediación ante la institución [NOMBRE DE LA INSTITUCIÓN DE MEDIACIÓN], en el cual intervino el mediador D. [NOMBRE Y APELLIDOS], habiendo alcanzado el acuerdo de mediación de fecha [DÍA] de [MES] de [AÑO] que se acompaña como documento [Nº DE DOCUMENTO], en virtud del cual fijan un régimen de comunicación y visitas de los abuelos con el menor en los siguientes términos: " Las partes pactan el siguiente régimen de relación y comunicación a favor de los abuelos con el nieto

A) El primer fin de semana de cada mes, desde el viernes a la salida del colegio, hasta el domingo a las 20:00 horas, así como dos miércoles por la tarde durante cada mes, desde la salida del colegio hasta las 20 horas. La recogida y entrega dela menor se hará en todo caso por los abuelos en el domicilio materno.

B) Durante las vacaciones de Navidad y Semana Santa, el menor estará un fin de semana con los abuelos, y una quincena en las vacaciones de verano, a elección de la madre.

C) La madre se compromete a que los abuelos puedan contactar con el menor vía telefónica, respetando las actividades y horario de descanso del menor".

Existiendo acuerdo de las partes en la regulación de la comunicación y visitas con el nieto, por medio del presente escrito se solicita que, tras la preceptiva audiencia de la madre, del menor y del Ministerio Fiscal, se apruebe el precedente acuerdo, fijando el régimen de visitas convenido teniendo en consideración especialmente el interés del menor.

FUNDAMENTOS DE DERECHO

COMPETENCIA. Son competentes los Tribunales de Instancia de esta ciudad, por ser el del domicilio del menor.

PROCEDIMIENTO. Debe seguirse el procedimiento de jurisdicción voluntaria regulado en los artículos 1811 y siguientes de la LEC de 1881 con relación al art. 160 del Código Civil.

LEGITIMACIÓN. Esta parte está legitimada conforme a lo dispuesto en el art. 160 del Código Civil.

FUNDAMENTOS DE FONDO. El art. 160 del Código Civil y la Ley de Mediación 5/2012 debiendo aprobarse el acuerdo teniendo en cuenta el prevalente interés del menor.

Por lo expuesto,

AL TRIBUNAL SUPLICO: Que tenga por presentado este escrito, lo admita, y por promovido expediente de jurisdicción voluntaria de aprobación del acuerdo de mediación de fecha [DÍA] de [MES] de [AÑO] en relación al régimen de comunicación y visitas de los abuelos solicitantes con su nieto menor., y practicadas las diligencias oportunas, con audiencia de la madre, del menor, y con intervención del Ministerio Fiscal, y previos los demás trámites con arreglo a Derecho dicte resolución en forma de auto en la que se acuerde la aprobación del régimen de comunicación y visitas convenido por las partes en el acuerdo de mediación antes citado, tal como se expresa en el hecho tercero de este escrito.

OTROSÍ PRIMERO DIGO que a efectos de comunicaciones designo el domicilio del letrado firmante de este escrito sito en [LOCALIDAD], así como la dirección de correo electrónico del mismo [CORREO ELECTRÓNICO] y el número de fax [Nº DE FAX].

SUPLICO AL TRIBUNAL: tenga por hecha la citada designación de domicilio.

Es Justicia que insto en [LUGAR], a [DÍA] de [MES] de [AÑO].

Firmas de los Solicitantes y Letrado.

========================================================================
