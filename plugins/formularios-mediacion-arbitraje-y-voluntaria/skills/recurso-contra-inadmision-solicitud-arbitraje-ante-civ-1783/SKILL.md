---
name: recurso-contra-inadmision-solicitud-arbitraje-ante-civ-1783
description: "Recurso contra la inadmisión de una solicitud de arbitraje ante la Comisión de Juntas. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Recurso contra la inadmisión de una solicitud de arbitraje ante la Comisión de Juntas

> Formulario **CIV-1783** del plugin **Mediación, MASC, arbitraje y jurisdicción voluntaria** (`formularios-mediacion-arbitraje-y-voluntaria`) · Civil › Jurisdicción voluntaria, MASC, mediación y arbitraje · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **recursos**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Recurso contra la inadmisión de una solicitud de arbitraje ante la Comisión de Juntas» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Recurso contra la inadmisión de una solicitud de arbitraje ante la Comisión de Juntas” para mi caso». También puedes invocarla directamente con `/formularios-mediacion-arbitraje-y-voluntaria:recurso-contra-inadmision-solicitud-arbitraje-ante-civ-1783`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-mediacion-arbitraje-y-voluntaria:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Mediación, MASC, arbitraje y jurisdicción voluntaria) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] CALLE
- [ ] CORREO ELECTRÓNICO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DNI/NIE
- [ ] IMPORTE
- [ ] NOMBRE Y APELLIDOS
- [ ] Nº DE FAX
- [ ] Nº DE PROCEDIMIENTO
- [ ] OTROS DATOS

## Normas que cita el formulario

- art. 35.4 Real Decreto 713/2024

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

Procedimiento arbitral nº [Nº DE PROCEDIMIENTO]

Junta arbitral de Consumo de [LOCALIDAD]

A LA COMISIÓN DE JUNTAS ARBITRALES DE CONSUMO DE [OTROS DATOS]

D./Dª [NOMBRE Y APELLIDOS], con D.N.I., con domicilio en calle [CALLE] de [LOCALIDAD] (correo electrónico [CORREO ELECTRÓNICO] o fax [Nº DE FAX]), el cual se designa a efectos de notificaciones, en nombre de la persona/consumidor, D.N.I. [DNI/NIE], que representa EXPONE:

1) Que en fecha [FECHA] formulé solicitud de arbitraje contra la empresa [DENOMINACIÓN SOCIAL] en reclamación de [IMPORTE] euros ante la Junta Arbitral de Consumo de [LOCALIDAD] (acompaño copia de la solicitud).

2) Que el pasado día [FECHA] fui notificado de la resolución de la persona titular de la presidencia de la citada Junta Arbitral de fecha [FECHA] por la que no se admitía la solicitud de arbitraje (acompaño copia de la resolución).

3) Y que, entendiendo que dicha resolución no es conforme a derecho, al amparo de lo dispuesto en el art. 35.4 del Real Decreto 713/2024, de 23 de julio, por el que se aprueba el Reglamento que regula el Sistema Arbitral de Consumo, por medio del presente escrito formulo RECURSO CONTRA LA INADMISIÓN DE LA SOLICITUD DE ARBITRAJE fundado en los siguientes MOTIVOS:

PRIMERO.- Infracción del art. 57 del Texto Refundido de la Ley de Consumidores y Usuarios y del art. 2 del RD 713/2024.

La resolución que se recurre inadmite la solicitud de arbitraje por no darse los supuestos previstos en el art. 2 del RD 713/2024.

Según se indica en la citada resolución, la materia sometida a arbitraje está fuera del ámbito de la libre disposición de las partes.

Sin embargo, dicho razonamiento carece de fundamento y por ello entiendo que no es conforme a derecho, por cuanto que la reclamación se formuló en el contexto de una relación jurídico-privada entre el que suscribe, como consumidor, y la empresa reclamada, como prestadora de servicios. Por otra parte, no se da ninguna de las excepciones expresamente tasadas en el art. 57 del TR de la Ley y art. 2 del RD 713/2024, puesto que es patente que ni se está reclamando por supuestos de intoxicación, lesiones o muerte, ni tampoco existen indicios racionales de delito.

Por tanto, no se da el supuesto de inadmisión apreciado por la resolución recurrida, que con ello infringe el mandato establecido en los artículos 57 del TR de la Ley y 2 del RD 713/2024, ya citados, por lo que solicito que por la Comisión a la que me dirijo se revoque la citada resolución, ordenando la admisión de la solicitud de arbitraje.

En virtud de lo expuesto, es de justicia y por ello

SOLICITA A LA COMISIÓN DE LAS JUNTAS ARBITRALES DE CONSUMO que tenga por interpuesto recurso contra la resolución de la persona titular de la presidencia de la Junta Arbitral de Consumo de [LOCALIDAD] dictada en fecha [FECHA] y, tras los trámites correspondientes, acuerde revocar dicha resolución, ordenando la admisión de la solicitud de arbitraje formulada por el que suscribe.

Firmado:

========================================================================
