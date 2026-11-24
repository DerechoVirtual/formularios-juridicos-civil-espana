---
name: certificado-sustitutivo-titulo-ejecutivo-europeo-civ-1598
description: "Certificado sustitutivo de título ejecutivo europeo emitido tras un recurso (art. 6.3). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Certificado sustitutivo de título ejecutivo europeo emitido tras un recurso (art. 6.3)

> Formulario **CIV-1598** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Modelo de certificado sustitutorio de título ejecutivo europeo emitido a raíz de un recurso.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Certificado sustitutivo de título ejecutivo europeo emitido tras un recurso (art. 6.3)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Certificado sustitutivo de título ejecutivo europeo emitido tras un recurso (art. 6.3)” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:certificado-sustitutivo-titulo-ejecutivo-europeo-civ-1598`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (2 veces)
- [ ] ESTADO MIEMBRO DE ORIGEN
- [ ] FECHA
- [ ] LUGAR
- [ ] OTRA DIVISA
- [ ] OTRO TIPO DE INTERÉS

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

Modelo de certificado sustitutorio de título ejecutivo europeo emitido a raíz de un recurso.


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

El Reglamento (CE) 44/2001 ha sido sustituido por el Reglamento (UE) nº 1215/2012 (Bruselas I bis) para acciones judiciales iniciadas a partir del 10 de enero de 2015, aunque el 44/2001 sigue vigente para procedimientos anteriores a esa fecha.

A. Se interpuso recurso contra la siguiente resolución/transacción judicial/instrumento auténtico (Táchese lo que no proceda) certificada/o como título ejecutivo europeo

1. Estado miembro de origen:

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

□ Bélgica

□ República Checa

□ Alemania

□ Estonia

□ Grecia

□ España

□ Francia

□ Irlanda

□ Italia

□ Chipre

□ Letonia

□ Lituania

□ Luxemburgo

□ Hungría

□ Malta

□ Países Bajos

□ Austria

□ Polonia

□ Portugal

□ Eslovenia

□ Eslovaquia

□ Finlandia

□ Suecia

□ Reino Unido

2. Órgano jurisdiccional/autoridad que expide el certificado

2.1. Denominación:
2.2. Dirección:
2.3. Tel./fax/correo electrónico:

3. Si es diferente, órgano jurisdiccional/autoridad que expide la resolución/transacción judicial/instrumento auténtico (Táchese lo que no proceda).

3.1. Denominación:
3.2. Dirección:
3.3. Tel./fax/correo electrónico:

4. Resolución/transacción judicial/instrumento auténtico (Táchese lo que no proceda)

4.1. Fecha:
4.2. Nº [Nº] de referencia:
4.3. Las partes
4.3.1. Nombre y dirección del [ELEGIR: acreedor / acreedores]:
4.3.2. Nombre y dirección del [ELEGIR: deudor / deudores]:

B. A raíz del recurso se dictó la siguiente decisión que se certifica por la presente como título ejecutivo europeo en sustitución del título ejecutivo europeo original.

1. Órgano jurisdiccional emisor

1.1. Denominación:
1.2. Dirección:
1.3. Tel./fax/correo electrónico.

2. Decisión

2.1. Fecha:
2.2. Nº [Nº] de referencia:

3. Crédito pecuniario certificado

3.1. Capital principal

3.1.1. Divisas:

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

□ Euro

□ Libra chipriota

□ Corona checa

□ Corona estonia

□ Libra esterlina

□ Forint húngaro

□ Litas lituanas

□ Lats letón

□ Lira maltesa

□ Zloty polaco

□ Corona sueca

□ Corona eslovaca

□ Tolar esloveno

□ Otra [OTRA DIVISA]

3.1.2. Si el crédito es por un pago periódico

3.1.2.1. Importe de cada plazo:

3.1.2.2. Fecha de vencimiento del primer plazo:

3.1.2.3. Fecha de vencimiento de los plazos sucesivos

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

□ semanal

□ mensual

□ otra (precisar)

3.1.2.4. Duración del crédito

3.1.2.4.1.

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

□ Actualmente indefinida

□

3.1.2.4.2. Fecha de vencimiento del último plazo:

3.2. Intereses

3.2.1. Tipo de interés

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

3.2.1.1. % o

3.2.1.2. % por encima del tipo base del BCE (Tipo de interés aplicado por el Banco Central Europeo a sus principales operaciones de refinanciación).

3.2.1.3. Otros [OTRO TIPO DE INTERÉS]:

3.2.2. Intereses que deberán percibirse a partir de:

3.3. Importe de costes reembolsables si está especificado en la decisión:

4.

□ La decisión es ejecutiva en el Estado miembro de origen

5. Contra la decisión cabe interponer nuevo recurso

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

□ Sí

□ No

6.

□ La decisión se ajusta al artículo 6, apartado 1, letra b)

7. La decisión se ha dictado en causas relativas a contratos celebrados con consumidores

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

□ Sí

□ No

7.1. En caso afirmativo:

el deudor es el consumidor

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

□ Sí

□ No

7.2. En caso afirmativo:

□ El deudor está domiciliado en el Estado miembro de origen [ESTADO MIEMBRO DE ORIGEN]

8. En el momento de la decisión adoptada a raíz del recurso, el crédito no está impugnado en el sentido del artículo 3, apartado 1, letras b) o c)

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

□ Sí

□ No

En caso afirmativo:

8.1. Notificación del escrito de incoación del recurso.

¿El acreedor presentó el recurso?

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

□ Sí

□ No

En caso afirmativo:

8.1.1.

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

□ La notificación se efectuó con arreglo al artículo 13

□ o la notificación se efectuó con arreglo al artículo 14

□ o está probado de acuerdo con el artículo 18, apartado 2, que el deudor recibió el documento

8.1.2. Información debida

□ El deudor ha sido informado con arreglo a los artículos 16 y 17

8.2. Notificación de la citación, en su caso

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

□ Sí

□ No

En caso afirmativo:

8.2.1.

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

□ La notificación se efectuó con arreglo al artículo 13

□ o la notificación se efectuó con arreglo al artículo 14

□ o está probado de acuerdo con el artículo 18, apartado 2, que el deudor recibió la notificación

8.2.2. Información debida

□ El deudor ha sido informado con arreglo al artículo 17

8.3. Subsanación del incumplimiento de las normas mínimas procesales según el artículo 18, apartado 1

8.3.1.

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

□ La notificación de la decisión se efectuó con arreglo al artículo 13

□ o la notificación de la decisión se efectuó con arreglo al artículo 14

□ o está probado de acuerdo con el artículo 18, apartado 2, que el deudor recibió la decisión

8.3.2. Información debida

□ El deudor ha sido informado con arreglo al artículo 18, apartado 1, letra b)

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma

========================================================================
