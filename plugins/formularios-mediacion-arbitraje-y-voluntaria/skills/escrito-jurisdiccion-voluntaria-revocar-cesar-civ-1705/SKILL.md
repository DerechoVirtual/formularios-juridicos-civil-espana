---
name: escrito-jurisdiccion-voluntaria-revocar-cesar-civ-1705
description: "Escrito de jurisdicción voluntaria para revocar o cesar nombramientos de auditor. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito de jurisdicción voluntaria para revocar o cesar nombramientos de auditor

> Formulario **CIV-1705** del plugin **Mediación, MASC, arbitraje y jurisdicción voluntaria** (`formularios-mediacion-arbitraje-y-voluntaria`) · Civil › Jurisdicción voluntaria, MASC, mediación y arbitraje · normativa revisada el 24-11-2026.

## Qué es

Por medio del presente escrito, y de conformidad con el art. 120 de la Ley de Jurisdicción Voluntaria, se promueve expediente en solicitud de cese de auditor nombrado.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito de jurisdicción voluntaria para revocar o cesar nombramientos de auditor» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito de jurisdicción voluntaria para revocar o cesar nombramientos de auditor” para mi caso». También puedes invocarla directamente con `/formularios-mediacion-arbitraje-y-voluntaria:escrito-jurisdiccion-voluntaria-revocar-cesar-civ-1705`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-mediacion-arbitraje-y-voluntaria:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Mediación, MASC, arbitraje y jurisdicción voluntaria) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (10 veces)
- [ ] TÍTULO DEL APARTADO (6 veces)
- [ ] FECHA (5 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] NÚMERO (4 veces)
- [ ] CALLE (3 veces)
- [ ] SEDE (3 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] Nº (2 veces)
- [ ] FOLIO
- [ ] HOJA
- [ ] IMPORTE
- [ ] LUGAR
- [ ] NIF
- [ ] TOMO

## Normas que cita el formulario

- art. 266.1 Real Decreto Legislativo 1/2010
- art. 265 TRLSC
- art. 122 LJV
- art. 121.1 LJV
- art. 266 TRLSC
- art. 120 LJV
- art. 122.2 LJV

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

- Junto a «…e la Sección de lo Mercantil del Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) La exigencia de abogado y procurador para plantear expediente de jurisdicción voluntaria variará, según el art. 3.2 LJV, en función del expediente de que se trate, y la exigencia legal al respecto. En todo caso, aun cuando no sea necesario, las partes que lo deseen podrán actuar asistidas o representadas por Abogado y Procurador, respectivamente. En el supuesto específico del presente escrito, el art. 121.3 LJV, considera preceptiva la intervención de Abogado y Procurador para la solicitud en análisis.


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

Que por medio del presente escrito, y de conformidad con el art. 120 de la Ley de Jurisdicción Voluntaria, promuevo expediente en solicitud de cese de auditor nombrado. Todo ello, en base a los siguientes

Hechos y consideraciones jurídicas:

1.ª [TÍTULO DEL APARTADO])

Que mi mandante es socio de la entidad [DENOMINACIÓN SOCIAL] SL constituida el [FECHA], según consta en la escritura autorizada el [FECHA] por D./Dña. [NOMBRE Y APELLIDOS], Notario de [LOCALIDAD], su domicilio social se halla sito en [LOCALIDAD], calle [CALLE], nº [NÚMERO], y fue inscrita en el Registro Mercantil nº [NÚMERO] de los de [SEDE] el [FECHA], Tomo [TOMO], Folio [FOLIO], Hoja [HOJA], con CIF [NIF]. Es titular de [Nº] particiones, de [IMPORTE] euros, de valor nominal, lo que supone un 12,22% del capital social. Los administradores sociales son [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], calle [CALLE], nº [NÚMERO]. Se aporta también listado de socios y sus direcciones.

2.ª [TÍTULO DEL APARTADO])

Que el pasado [FECHA], mediante decreto dictado por el Letrado de la Administración de Justicia de la Sección de lo Mercantil del Tribunal de Instancia de [SEDE], plaza n.º [Nº] , se nombró auditor de la referida entidad a D./Dña. [NOMBRE Y APELLIDOS], con despacho profesional en [LOCALIDAD], calle [CALLE], nº [NÚMERO], tras petición al respecto planteada por los socios D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS]. La citada resolución no fue recurrida.

3.ª [TÍTULO DEL APARTADO])

Que las labores de auditoría se encuentran paralizadas desde hace más de tres meses, porque el auditor nombrado no es capaz de llevarlas a cabo, a causa de la complejidad del sector al que se dedica la mercantil en cuestión, lo que influye decisivamente en las labores auditoras. En este sentido, D./Dña. [NOMBRE Y APELLIDOS] carece de medios, experiencia y conocimientos específicos al respecto, y, por lo que parece, y a pesar de que mi mandante se lo ha aconsejado, no acaba de dar el paso para renunciar al cargo, sin que se cumpla, por ello, la necesidad de auditoría que determinó su nombramiento.

4.ª [TÍTULO DEL APARTADO])

Concurre, en consecuencia, la justa causa para revocar el nombramiento de auditor a la que hace referencia el art. 266.1 del Real Decreto Legislativo 1/2010, de 2 de julio, por el que se aprueba el texto refundido de la Ley de Sociedades de Capital (en lo sucesivo, TRLSC), atendiendo a su incapacidad para realizar una auditoría en condiciones. Asimismo, mi representado se encuentra legitimado para ello, al disponer de más de un 5% del capital social, tal y como establece el referido precepto legal, en relación con el art. 265 TRLSC. Por ello, deberán seguirse los trámites previstos en los arts. 122 y 123 LJV, convocándose a una comparecencia ante el Letrado de la Administración de Justicia, al auditor en cuestión, los administradores sociales, los socios de la entidad, y quien se estime conveniente

5.ª [TÍTULO DEL APARTADO])

Que es competente la Sección de lo Mercantil del Tribunal de Instancia al que me dirijo conforme al artículo 121.1 LJV, al encontrarse en su partido judicial el domicilio social de la entidad que designó al auditor cuyo cese se pretende.

6.ª [TÍTULO DEL APARTADO])

Se acompañan a esta solicitud copia simple de la escritura de constitución mencionada, certificación del Registro Mercantil donde constan los datos mencionados, certificación expedida por el Secretario del Consejo de Administración de [DENOMINACIÓN SOCIAL] SL del Libro Registro donde constan titularidades sociales, copia testimoniada del decreto en el que se designaba a D./Dña. [NOMBRE Y APELLIDOS] como auditor, y listado de socios y sus direcciones.

Por todo lo expuesto, al amparo del art. 266 TRLSC y del art. 120 LJV,

SOLICITO AL TRIBUNAL

Que teniendo por presentado este escrito y documentos que lo acompañan y por promovido expediente de jurisdicción voluntaria para el cese de auditor; y previa convocatoria de comparecencia ante el Letrado de la Administración de Justicia prevista en el art. 122.2 LJV, con citación del propio D./Dña. [NOMBRE Y APELLIDOS], los administradores sociales, los socios, y a quien se estime oportuno, se dicte decreto cesando en su cargo al primero, con remisión del correspondiente testimonio al Registro Mercantil.

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a
