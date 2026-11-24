---
name: escrito-inicio-expediente-jurisdiccion-voluntaria-civ-1708
description: "Escrito de inicio del expediente de jurisdicción voluntaria sobre depósito de mercancías. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito de inicio del expediente de jurisdicción voluntaria sobre depósito de mercancías

> Formulario **CIV-1708** del plugin **Mediación, MASC, arbitraje y jurisdicción voluntaria** (`formularios-mediacion-arbitraje-y-voluntaria`) · Civil › Jurisdicción voluntaria, MASC, mediación y arbitraje · normativa revisada el 24-11-2026.

## Qué es

Expediente en solicitud de depósito de mercancías

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito de inicio del expediente de jurisdicción voluntaria sobre depósito de mercancías» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito de inicio del expediente de jurisdicción voluntaria sobre depósito de mercancías” para mi caso». También puedes invocarla directamente con `/formularios-mediacion-arbitraje-y-voluntaria:escrito-inicio-expediente-jurisdiccion-voluntaria-civ-1708`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-mediacion-arbitraje-y-voluntaria:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Mediación, MASC, arbitraje y jurisdicción voluntaria) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] TÍTULO DEL APARTADO (5 veces)
- [ ] MATRÍCULA (4 veces)
- [ ] Nº DE BASTIDOR (4 veces)
- [ ] FECHA (3 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] Nº DE RESGUARDO (2 veces)
- [ ] CALLE
- [ ] IMPORTE
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] NÚMERO
- [ ] SEDE

## Normas que cita el formulario

- art. 132 Ley 15/2015
- art. 133.2 LJV
- art. 133.1 LJV
- art. 135 LJV

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

Notas al pie del formulario original:
(1) La exigencia de abogado y procurador para plantear expediente de jurisdicción voluntaria variará, según el art. 3.2 LJV, en función del expediente de que se trate, y la exigencia legal al respecto. En todo caso, aun cuando no sea necesario, las partes que lo deseen podrán actuar asistidas o representadas por Abogado y Procurador, respectivamente. En el supuesto específico del presente escrito, el art. 133.3 LJV establece como preceptiva la intervención de Abogado y Procurador para la solicitud en análisis.


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

A LA SECCIÓN DE LO MERCANTIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño a este escrito, como mejor proceda en derecho comparezco y DIGO:

Que por medio del presente escrito, y de conformidad con el art. 132 de la Ley 15/2015, de 2 de julio, de la Jurisdicción Voluntaria (en lo sucesivo, LJV), promuevo expediente en solicitud de depósito de mercancías. Todo ello, en base a los siguientes

Hechos y consideraciones jurídicas:

1.ª [TÍTULO DEL APARTADO])

Mi mandante era poseedor de dos resguardos de depósito, numerados como [Nº DE RESGUARDO] y [Nº DE RESGUARDO]; relativos a dos vehículos tractores, con placas de matrícula [MATRÍCULA] y [MATRÍCULA], y número de bastidor [Nº DE BASTIDOR] y [Nº DE BASTIDOR]; adquiridos de la entidad [DENOMINACIÓN SOCIAL] SL, el pasado [FECHA], depositados en las instalaciones de la vendedora, preparados para su transporte, y por cuyo compra había abonado la cantidad de [IMPORTE] euros

2.ª [TÍTULO DEL APARTADO])

El pasado [FECHA], el domicilio social donde se encontraban los referidos resguardos, sito en [LOCALIDAD], calle [CALLE], nº [NÚMERO], fue objeto de robo, denunciado ante el Cuerpo Nacional de Policía, y como consecuencia del cual se sustrajeron diversos bienes y enseres, incluidos los referidos títulos de depósito. Hasta la fecha las investigaciones policiales no han dado sus frutos, y los títulos no han podido ser recuperados.

3.ª [TÍTULO DEL APARTADO])

Por ello, es interés de mi cliente que se proceda al depósito judicial de los dos vehículos indicados, y que se le dé a tal hecho la publicidad legalmente procedente. Se acude, en consecuencia, al procedimiento previsto en los arts. 132 y ss. LJV, que permite solicitar aquel, a los efectos de que no se pierdan las mercancías reflejadas en los títulos sustraídos. En este sentido, mi mandante se encuentra legitimado para la solicitud que se plantea, al haber sido el legítimo comprador de los bienes representados en los títulos indicados, en virtud de lo dispuesto en el art. 133.2 LJV. Asimismo, procederá el anuncio del expediente en el Boletín Oficial del Estado, en un periódico de gran circulación en la Comunidad de Madrid, y la convocatoria de una comparecencia con citación de los interesados.

4.ª [TÍTULO DEL APARTADO])

Que es competente la Sección de lo Mercantil del Tribunal de Instancia al que me dirijo conforme al artículo 133.1 LJV, al encontrarse en su partido judicial el lugar donde los vehículos tractores en cuestión se encuentran depositados.

5.ª [TÍTULO DEL APARTADO])

Se acompañan a esta solicitud copia de la denuncia, del atestado policial, y del contrato de compraventa.

Por todo lo expuesto, al amparo de los arts. 132 y ss. LJV,

SUPLICO AL TRIBUNAL

Que teniendo por presentado este escrito y documentos que lo acompañan y por promovido expediente de jurisdicción voluntaria; previa publicación en el Boletín Oficial del Estado y en un periódico de gran circulación en la Comunidad de Madrid, y previa convocatoria de comparecencia ante el Letrado de la Administración de Justicia prevista en el art. 135 LJV, con citación de la entidad vendedora [DENOMINACIÓN SOCIAL] SL, y de quien se estime oportuno, se dicte decreto acordando constituir el depósito judicial de los vehículos tractores con placas de matrícula [MATRÍCULA] y [MATRÍCULA], y número de bastidor [Nº DE BASTIDOR] y [Nº DE BASTIDOR].

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a
