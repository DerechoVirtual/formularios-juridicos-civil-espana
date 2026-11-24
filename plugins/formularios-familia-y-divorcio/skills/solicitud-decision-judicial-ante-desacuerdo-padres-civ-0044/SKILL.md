---
name: solicitud-decision-judicial-ante-desacuerdo-padres-civ-0044
description: "Solicitud de decisión judicial ante el desacuerdo de los padres sobre patria potestad (art 156 CC). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de decisión judicial ante el desacuerdo de los padres sobre patria potestad (art 156 CC)

> Formulario **CIV-0044** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de decisión judicial ante el desacuerdo de los padres sobre patria potestad (art 156 CC)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de decisión judicial ante el desacuerdo de los padres sobre patria potestad (art 156 CC)” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:solicitud-decision-judicial-ante-desacuerdo-padres-civ-0044`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (10 veces)
- [ ] AÑO (4 veces)
- [ ] Nº DE DOCUMENTO (4 veces)
- [ ] DÍA (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] MES (3 veces)
- [ ] NOMBRE DEL MENOR (2 veces)
- [ ] Nº (2 veces)
- [ ] CALLE
- [ ] COLEGIO
- [ ] DNI/NIE
- [ ] FECHA
- [ ] LUGAR
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] NÚMERO
- [ ] SEDE

## Normas que cita el formulario

- art. 156 Código Civil
- art. 6 LEC

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

- Junto a «…MILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Denominación legal: Sección de Familia, Infancia y Capacidad. Si no existe en el partido, conoce la Sección Civil o la Única (art. 86.3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).

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

D./Dª [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en nombre y representación de D./Dª [NOMBRE Y APELLIDOS], mayor de edad, con domicilio en [LOCALIDAD], calle [CALLE], nº [NÚMERO], pta., y DNI [DNI/NIE], cuya representación acreditaré mediante comparecencia apud acta cuando sea requerido para ello, comparezco en este TRIBUNAL con la asistencia del Letrado D./Dª [NOMBRE Y APELLIDOS], del Ilustre Colegio de Abogados de [COLEGIO], y

DIGO

Que por medio del presente escrito promuevo EXPEDIENTE DE JURISDICCIÓN VOLUNTARIA PARA QUE SE ATRIBUYA A MI REPRESENTADO/A LA FACULTAD DE DECIDIR en el asunto que se expondrá, relativo al ejercicio de la patria potestad, por desacuerdo con el otro progenitor del/de la menor [NOMBRE DEL MENOR], D./Dª [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], conforme a lo dispuesto en el párrafo segundo del artículo 156 del Código Civil y art. 86 de la Ley de Jurisdicción Voluntaria en la nueva redacción dada por la Ley 8/2021 de 2 de junio.

La pretensión anterior se formula con base en los siguientes

HECHOS

Mi mandante D./Dª [NOMBRE Y APELLIDOS] y D./Dª [NOMBRE Y APELLIDOS], son padres del/de la menor [NOMBRE DEL MENOR], nacido en fecha [DÍA] de [MES] de [AÑO]

Se acredita esta circunstancia mediante certificación literal de nacimiento expedida por el Encargado del registro Civil de [LOCALIDAD], que se acompaña como DOCUMENTO Nº [Nº DE DOCUMENTO]

Por sentencia núm. [Nº], de de [FECHA] de dictada por el Tribunal al que tengo el honor de dirigirme, en el procedimiento de divorcio o de separación de mutuo acuerdo núm. [Nº]/[AÑO], en la que se procedió a homologar el Convenio regulador de fecha [DÍA] de [MES] de [AÑO], presentado por las partes, se atribuyó a mi representado/a la guarda y custodia del hijo/a menor de los cónyuges [NOMBRE Y APELLIDOS], sin que ello obste a la titularidad conjunta de la patria potestad que ambos ostentan sobre el mismo.

Se acompaña testimonio de la citada sentencia, en el que consta su firmeza, así como del convenio regulador que la misma homologaba, como DOCUMENTO Nº [Nº DE DOCUMENTO] con remisión, a efectos probatorios, a los archivos de este Tribunal.

Entre ambos progenitores ha surgido un desacuerdo irresoluble acerca de la conveniencia o no de que el/la menor, que cuenta en la actualidad con dieciséis años de edad, siga sus estudios, durante el próximo curso, en el siguiente Centro educativo norteamericano:

El/la padre/madre del menor se opone a ello por el distanciamiento espacial que supone del ámbito familiar y la dificultad -dice- de velar convenientemente por el/la menor en tales circunstancias.

Por el contrario, mi representado/a está convencido/a de la conveniencia para el/la hijo/a de seguir sus estudios, durante el próximo curso, en el lugar indicado. Se trata de un prestigioso centro educativo, con el que el colegio del/de la menor tiene un concierto que facilita este tipo de desplazamientos temporales, así como el alojamiento adecuado en el mismo centro, en régimen de internado. Por otra parte, el coste económico estaría cubierto gracias a la Beca obtenido por el/la menor debido a sus calificaciones sobresalientes. Esta estancia permitiría al/a la menor, consolidar sus conocimientos de inglés con la clara repercusión favorable que esto puede tener en su futuro profesional. Por último, el/la menor, que, dada su edad -dieciséis años-, cuenta con madurez suficiente para que su opinión sea tenida en cuenta, es favorable a cursar estudios en el citado centro extranjero. Todo lo anterior nos lleva a concluir que la opción de mi representado/a es la más conveniente para los intereses del/de la hijo/a.

Se acompaña, como DOCUMENTO Nº [Nº DE DOCUMENTO], certificado acreditativo de la Beca obtenida por el/la menor.

Ha sido imposible llegar a un acuerdo entre los progenitores, por lo que se solicita la intervención de la autoridad judicial, en el sentido de atribuir a uno de ellos, mi mandante, la capacidad de decidir en este asunto.

Así, previamente a la interposición de la presente solicitud se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

Resultan aplicables a los anteriores hechos, los siguientes

FUNDAMENTOS DE DERECHO

COMPETENCIA

Es competente el Tribunal al que me dirijo, conforme a lo previsto en los arts. 2 y 86.2.segundo inciso de la Ley de la Jurisdicción Voluntaria.

PROCEDIMIENTO

Debe seguirse el procedimiento de jurisdicción voluntaria regulado en los artículos 85 y siguientes de la Ley de Jurisdicción Voluntaria.

CAPACIDAD

Tiene mi mandante capacidad para promover este procedimiento, conforme a lo dispuesto en los artículos 6 y ss LEC.

LEGITIMACIÓN

Esta parte está legitimada conforme a lo dispuesto en el art. 156 del Código Civil y art. 86.3 de la Ley de Jurisdicción Voluntaria.

REPRESENTACIÓN Y DEFENSA

Aunque en virtud del art. 85.3 de la Ley de la Jurisdicción Voluntaria, en la tramitación del presente expediente no es preceptiva la intervención de Abogado ni Procurador, el art. 3.2, segundo inciso de la citada ley establece que las partes que lo deseen podrán actuar asistidas o representadas por Abogado y Procurador, respectivamente, como se hace en la presente solicitud.

DERECHO SUSTANTIVO

Resultan aplicables los artículos 154 y siguientes del Código civil, en especial el artículo 156.II.

GASTOS

Se rigen por lo dispuesto en el artículo 7 de la Ley de la Jurisdicción Voluntaria.

Por lo expuesto

SOLICITO AL TRIBUNAL:

Que tras admitir este escrito con las copias y documentos que lo acompañan, se sirva incoar expediente de jurisdicción voluntaria y, previos los trámites legales oportunos, incluida la audiencia de ambos progenitores y del/de la menor, dicte Auto en que se atribuya a mi representado/a, D./Dª [NOMBRE Y APELLIDOS], la facultad de decidir si el próximo curso, el/la hijo/a cursará estudios en el Centro educativo

Que teniendo por presentado este escrito con los documentos que se acompañan y copia de todo ello, lo admita, y tenga por promovida por el Procurador que suscribe, con quien habrán de entenderse las sucesivas diligencias en nombre y representación de D.Dª [NOMBRE Y APELLIDOS],

EXPEDIENTE DE JURISDICCIÓN VOLUNTARIA en solicitud de INTERVENCIÓN JUDICIAL POR DESACUERDO EN EL EJERCICIO DE LA PATRIA POTESTAD y, previos los trámites legales oportunos, incluida la audiencia de ambos progenitores y del/de la menor, con intervención del Ministerio Fiscal, dicte resolución en que se atribuya a mi representado/a, D./Dª [NOMBRE Y APELLIDOS], la facultad de decidir si el próximo curso, el/la hijo/a cursará estudios en el Centro educativo

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma del Procurador	Firma y número del Letrado

Téngase en cuenta que, en este tipo de procedimientos, no es preceptiva sino voluntaria, la intervención por medio de Procurador y la Asistencia Letrada.

========================================================================
