---
name: escrito-inicio-expediente-jurisdiccion-voluntaria-civ-1711
description: "Escrito de inicio del expediente de jurisdicción voluntaria sobre valores mobiliarios sustraídos. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito de inicio del expediente de jurisdicción voluntaria sobre valores mobiliarios sustraídos

> Formulario **CIV-1711** del plugin **Mediación, MASC, arbitraje y jurisdicción voluntaria** (`formularios-mediacion-arbitraje-y-voluntaria`) · Civil › Jurisdicción voluntaria, MASC, mediación y arbitraje · normativa revisada el 24-11-2026.

## Qué es

Expediente en solicitud de prohibición de negociar o transmitir valores mobiliarios y de suspensión del pago de capital, intereses o dividendos.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito de inicio del expediente de jurisdicción voluntaria sobre valores mobiliarios sustraídos» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito de inicio del expediente de jurisdicción voluntaria sobre valores mobiliarios sustraídos” para mi caso». También puedes invocarla directamente con `/formularios-mediacion-arbitraje-y-voluntaria:escrito-inicio-expediente-jurisdiccion-voluntaria-civ-1711`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-mediacion-arbitraje-y-voluntaria:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Mediación, MASC, arbitraje y jurisdicción voluntaria) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] DENOMINACIÓN SOCIAL (6 veces)
- [ ] FECHA (6 veces)
- [ ] TÍTULO DEL APARTADO (6 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] Nº (4 veces)
- [ ] CALLE (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] COMUNIDAD AUTÓNOMA (2 veces)
- [ ] MODALIDAD DE LOS VALORES (2 veces)
- [ ] Nº DE VALORES (2 veces)
- [ ] SERIE (2 veces)
- [ ] ENTIDAD BANCARIA
- [ ] IMPORTE
- [ ] LUGAR
- [ ] SEDE

## Normas que cita el formulario

- art. 132 Ley 15/2015
- art. 134.3 LJV
- art. 548 Código de Comercio
- art. 133.2 LJV
- art. 135.6 LJV
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

Que por medio del presente escrito, y de conformidad con el art. 132 Ley 15/2015, de 2 de julio, de la Jurisdicción Voluntaria (en lo sucesivo, LJV), promuevo expediente en solicitud de prohibición de negociar o transmitir valores mobiliarios y de suspensión del pago de capital, intereses o dividendos. Todo ello, en base a los siguientes

Hechos y consideraciones jurídicas:

1.ª [TÍTULO DEL APARTADO])

Mi mandante es propietario de [Nº DE VALORES] valores admitidos a cotización oficial en el mercado de renta fija, en su modalidad de [MODALIDAD DE LOS VALORES], emitidos por la entidad emisora [DENOMINACIÓN SOCIAL], con domicilio social en [LOCALIDAD], calle [CALLE], nº [NÚMERO]. Los valores disponen de número de serie [SERIE], y se encuentran numerados del [Nº] al [Nº]. Fueron adquiridos mediante escritura de adjudicación de herencia de fecha [FECHA], tras legado específico otorgado por sui padre D. [NOMBRE Y APELLIDOS], quien falleció el [FECHA]. Suponen un valor global de [IMPORTE] euros, y se encontraban depositados en la entidad financiera [ENTIDAD BANCARIA] SA.

2.ª [TÍTULO DEL APARTADO])

El pasado [FECHA], la sucursal de la citada entidad sita en [LOCALIDAD], calle [CALLE], nº [NÚMERO] fue objeto de robo, denunciado ante el Cuerpo Nacional de Policía, y como consecuencia del cual se sustrajeron diversos títulos de clientes de aquella, entre ellos los indicados que eran de propiedad de mi representado en su totalidad. Hasta la fecha las investigaciones policiales no han dado sus frutos, y los títulos no han podido ser recuperados.

3.ª [TÍTULO DEL APARTADO])

El pasado [FECHA] tal hecho se denunció ante la Sociedad Rectora del Mercado Oficial de Renta Fija, con solicitud de prohibición de la negociación o transmisión de los valores indicados y el pago de capital, intereses o dividendos. Lo que se materializó mediante acuerdo de fecha [FECHA], que, además, comunicaba tal decisión a las restantes sociedades rectoras, con publicación en el tablón de anuncios, en el Boletín Oficial del Estado, y en un periódico de gran circulación en la Comunidad Autónoma de [LOCALIDAD].

4.ª [TÍTULO DEL APARTADO])

Que cumpliendo con lo dispuesto en el art. 134.3 LJV, y dentro del plazo legal de nueve días se acude al procedimiento previsto en los arts. 132 y ss. LJV, a fin de mantener la interdicción acordada, y que permite llevar a la práctica el derecho previsto en el art. 548 del Código de Comercio. En este sentido, mi mandante se encuentra legitimado para la solicitud que se plantea, al ser el legítimo propietario de los valores mobiliarios indicados, en virtud de lo dispuesto en el art. 133.2 LJV. Asimismo, procederá el anuncio del expediente en el Boletín Oficial del Estado, en un periódico de gran circulación en la Comunidad de [COMUNIDAD AUTÓNOMA] y la convocatoria de una comparecencia con citación de los interesados. Finalmente, y dado que los valores mobiliarios en cuestión ofrecen el derecho de asistencia y de voto en las juntas generales y especiales de la entidad emisora, se solicita, al amparo del art. 135.6 LJV, que se nombre un administrador para el ejercicio de los derechos referidos, y, en su caso, para la eventual impugnación de acuerdos sociales de la misma.

5.ª [TÍTULO DEL APARTADO])

Que es competente la Sección de lo Mercantil del Tribunal de Instancia al que me dirijo conforme al artículo 133.1 LJV, al encontrarse en su partido judicial el domicilio de la entidad emisora de los valores sustraídos.

6.ª [TÍTULO DEL APARTADO])

Se acompañan a este escrito copia del atestado elaborado por el Cuerpo Nacional de Policía, copia de la escritura pública de adjudicación de herencia, copia de la denuncia planteada ante la Sociedad Rectora del Mercado de Renta Fija, copia del acuerdo adoptado por la misma, certificación expedida por la entidad emisora [DENOMINACIÓN SOCIAL], y por la entidad depositaria [DENOMINACIÓN SOCIAL] SA.

Por todo lo expuesto, al amparo de los arts. 132 y ss. LJV, y del art. 548 del Código de Comercio,

SUPLICO AL TRIBUNAL

Que teniendo por presentado este escrito y documentos que lo acompañan y por promovido expediente de jurisdicción voluntaria; previa publicación en el Boletín Oficial del Estado y en un periódico de gran circulación en la Comunidad de [COMUNIDAD AUTÓNOMA], y previa convocatoria de comparecencia ante el Letrado de la Administración de Justicia prevista en el art. 135 LJV, con citación de la entidad [DENOMINACIÓN SOCIAL] SA, y de quien se estime oportuno, se dicte decreto:

1.- Manteniendo la prohibición de negociación o transmisión de los [Nº DE VALORES] valores admitidos a cotización oficial en el mercado de renta fija, en su modalidad de [MODALIDAD DE LOS VALORES], emitidos por la entidad emisora [DENOMINACIÓN SOCIAL], con domicilio social en [LOCALIDAD], calle [CALLE], nº [NÚMERO], con número de serie [SERIE], y numerados del [Nº] al [Nº]; así como el pago de capital, intereses o dividendos
2.- Se nombre administrador para el ejercicio de los derechos derecho de asistencia y de voto en las juntas generales y especiales de la entidad emisora [DENOMINACIÓN SOCIAL] SA, y, en su caso, para la eventual impugnación de acuerdos sociales de la misma.

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a
