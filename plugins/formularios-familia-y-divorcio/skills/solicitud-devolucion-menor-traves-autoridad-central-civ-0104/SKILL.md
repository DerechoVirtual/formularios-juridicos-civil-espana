---
name: solicitud-devolucion-menor-traves-autoridad-central-civ-0104
description: "Solicitud de devolución de un menor a través de la Autoridad Central. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de devolución de un menor a través de la Autoridad Central

> Formulario **CIV-0104** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de devolución de un menor a través de la Autoridad Central» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de devolución de un menor a través de la Autoridad Central” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:solicitud-devolucion-menor-traves-autoridad-central-civ-0104`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS DEL MENOR (6 veces)
- [ ] Nº (6 veces)
- [ ] APELLIDOS DEL MENOR (4 veces)
- [ ] FECHA (4 veces)
- [ ] FECHA Y LUGAR DE NACIMIENTO (4 veces)
- [ ] NACIONALIDAD (4 veces)
- [ ] NOMBRE DEL MENOR (4 veces)
- [ ] Nº DE DOCUMENTO (4 veces)
- [ ] RESIDENCIA HABITUAL (4 veces)
- [ ] SEXO (4 veces)
- [ ] SEÑAS PERSONALES (3 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] AÑO
- [ ] DOMICILIO
- [ ] PAÍS
- [ ] PROFESIÓN

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

SOLICITUD DE DEVOLUCIÓN

AUTORIDAD CENTRAL REQUIRENTE

AUTORIDAD CENTRAL REQUERIDA O SOLICITANTE

SOLICITUD (Naturaleza y artículos relevantes del Convenio)

referente al menor.

1º) [NOMBRE Y APELLIDOS DEL MENOR]

2º) [NOMBRE Y APELLIDOS DEL MENOR]

3º) [NOMBRE Y APELLIDOS DEL MENOR]

4º) [NOMBRE Y APELLIDOS DEL MENOR]

cumplirá la edad de 16 años el:

1º) [FECHA] 2º) [FECHA]

3º) [FECHA] 4º) [NOMBRE Y APELLIDOS DEL MENOR]

A.INFORMACIÓN GENERAL./INFORMATIONS GENERALES./GENERAL INFORMATION.

Datos personales del menor/es y de sus padres.

Menor:

Nombre:

1º) [NOMBRE DEL MENOR] 2º) [NOMBRE DEL MENOR]

3º) [NOMBRE DEL MENOR] 4º) [NOMBRE DEL MENOR]

Apellidos:

1º) [APELLIDOS DEL MENOR] 2º) [APELLIDOS DEL MENOR]

3º) [APELLIDOS DEL MENOR] 4º) [APELLIDOS DEL MENOR]

Fecha y lugar de nacimiento:

Date et lieu de naissance:

Date and place of birth:

1º) [FECHA Y LUGAR DE NACIMIENTO] 2º) [FECHA Y LUGAR DE NACIMIENTO]

3º) [FECHA Y LUGAR DE NACIMIENTO] 4º) [FECHA Y LUGAR DE NACIMIENTO]

Nacionalidad:

Nationalité:

Nationality or nationalities:

1º) [NACIONALIDAD] 2º) [NACIONALIDAD]

3º) [NACIONALIDAD] 4º) [NACIONALIDAD]

Sexo/Sexe/Sex:

1º) [SEXO] 2º) [SEXO] 3º) [SEXO] 4º) [SEXO]

Residencia habitual:

1º) [RESIDENCIA HABITUAL] 2º) [RESIDENCIA HABITUAL]

3º) [RESIDENCIA HABITUAL] 4º) [RESIDENCIA HABITUAL]

Pasaporte o documento de identidad núm. [Nº]:

1º) [Nº DE DOCUMENTO] 2º) [Nº DE DOCUMENTO]

3º) [Nº DE DOCUMENTO] 4º) [Nº DE DOCUMENTO]

Señas personales y fotografía (Véanse anexos)

1º) [SEÑAS PERSONALES]

2º) [SEÑAS PERSONALES]

3º) [NOMBRE Y APELLIDOS DEL MENOR]

4º) [SEÑAS PERSONALES]

Padres.

2.1. Madre:

Nombre:

Apellidos:

Fecha y lugar de nacimiento:

Nacionalidad o nacionalidades:

Profesión:

Residencia habitual:

Pasaporte o Documento de Identidad núm. [Nº]:

Padre:

Nombre:

Apellidos:

Fecha y lugar de nacimiento:

Nacionalidad o nacionalidades:

Profesión:

Residencia habitual:

Pasaporte o Documento de Identidad núm. [Nº]:

Fecha y lugar de celebración del matrimonio:

Fecha y lugar de la sentencia de divorcio si la hubiere:

II.-DATOS PERSONALES DEL INDIVIDUO O INSTITUCION DEL SOLICITANTE:

Nombre:

Apellidos:

Nacionalidad (si es persona física):

Profesión (del individuo):

Dirección:

Pasaporte o Documento de Identidad núm. [Nº]:

Relación con el menor:

Nombre y dirección del Abogado o Asesor Jurídico, si lo hubiera:

III.-BASES DE HECHO O LEGALES QUE JUSTIFICAN LA SOLICITUD (por ejemplo: la resolución de un Tribunal):

IV. Procedimientos civiles en curso o que serán iniciados:

B. INFORMACIÓN ADICIONAL EN SUPUESTOS DE SOLICITUDES PARA EL RESTABLECIMIENTO DE LA CUSTODIA:

Lugar donde se supone que se encuentra el menor:

Datos de la persona que supuestamente haya sustraído o retenido ilícitamente al menor o a los menores:

Nombre:

Apellidos:

Fecha y lugar de nacimiento:

Nacionalidad:

Profesión:

Relación con el menor:

Último domicilio conocido:

Pasaporte o Documento de Identidad núm. [Nº]:

Señas personales y fotografía (véanse anexos):

Dirección del menor o de los menores:

Otras personas que pudieran proporcionar información complementaria en relación con el paradero del menor o de los menores:

Lugar, fecha y circunstancias en que tuvo lugar la sustracción o retención indebida:

El menor debe ser devuelto a:

a) Nombre:

Apellidos:

Fecha y lugar de nacimiento:

Dirección:

Número de Teléfono:

Propuesta en cuanto a las condiciones en que deberá llevarse a cabo la devolución del menor:

C. OTRAS CUESTIONES. AUTRES QUESTIONS. OTHER QUESTIONS.

Otras observaciones:

Relación de los documentos que se acompañan:

Fecha [FECHA]

Lugar/ [LOCALIDAD]

Firma y/o sello de la Autoridad Central Requirente o del solicitante

D./Dña. [NOMBRE Y APELLIDOS]

con profesión [PROFESIÓN] y domiciliada en [DOMICILIO]

AUTORIZA, según lo exigido en el artículo 28 del Convenio sobre los Aspectos Civiles de la Sustracción Internacional de Menores y artículo 13 párrafo 1 (a) del Convenio Europeo de Reconocimiento y Ejecución de decisiones en Materia de Custodia de Menores y Restablecimiento de dicha Custodia, a la AUTORIDAD CENTRAL DEL ESTADO [PAÍS] o a la persona designada por esta Autoridad Central para actuar en mi nombre.

Lugar, [LOCALIDAD] Día, [Nº] mes, [AÑO] año, [NOMBRE Y APELLIDOS]

FIRMADO:

========================================================================
