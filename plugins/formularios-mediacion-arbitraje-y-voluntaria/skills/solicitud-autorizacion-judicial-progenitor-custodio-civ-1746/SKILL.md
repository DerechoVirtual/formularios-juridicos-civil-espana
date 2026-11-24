---
name: solicitud-autorizacion-judicial-progenitor-custodio-civ-1746
description: "Solicitud de autorización judicial para que el progenitor custodio cambie de domicilio. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de autorización judicial para que el progenitor custodio cambie de domicilio

> Formulario **CIV-1746** del plugin **Mediación, MASC, arbitraje y jurisdicción voluntaria** (`formularios-mediacion-arbitraje-y-voluntaria`) · Civil › Jurisdicción voluntaria, MASC, mediación y arbitraje · normativa revisada el 24-11-2026.

## Qué es

Todas las referencias a Juzgados contenidas en este documento se entenderán sustituidas por Tribunales de Instancia cuando estos se constituyan, conforme al régimen transitorio que prevé la DT 1ª LO 1/2025

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de autorización judicial para que el progenitor custodio cambie de domicilio» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de autorización judicial para que el progenitor custodio cambie de domicilio” para mi caso». También puedes invocarla directamente con `/formularios-mediacion-arbitraje-y-voluntaria:solicitud-autorizacion-judicial-progenitor-custodio-civ-1746`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-mediacion-arbitraje-y-voluntaria:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Mediación, MASC, arbitraje y jurisdicción voluntaria) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] AÑO (5 veces)
- [ ] DÍA (5 veces)
- [ ] MES (5 veces)
- [ ] Nº DE DOCUMENTO (5 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] COLEGIO
- [ ] NOMBRE DEL MENOR
- [ ] Nº

## Normas que cita el formulario

- art. 6 LEC
- art. 17 LJV
- art. 85 LJV
- art. 154.I CC
- art. 154 CC

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

Todas las referencias a Juzgados contenidas en este documento se entenderán sustituidas por Tribunales de Instancia cuando estos se constituyan, conforme al régimen transitorio que prevé la DT 1ª LO 1/2025


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

AL TRIBUNAL DE FAMILIA/PRIMERA INSTANCIA NUM DE [LOCALIDAD]

D./Dª [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en nombre y representación de D./Dª [NOMBRE Y APELLIDOS],cuya representación acreditaré mediante comparecencia apud acta cuando sea requerido para ello, comparezco en este JUZGADO con la asistencia del Letrado D./Dª [NOMBRE Y APELLIDOS], del Ilustre Colegio de Abogados de [COLEGIO], y DIGO:

Que por medio del presente escrito y en la representación que ostento, insto procedimiento de JURISDICCIÓN VOLUNTARIA en solicitud de INTERVENCIÓN JUDICIAL POR DESACUERDO EN EL EJERCICIO DE LA PATRIA POTESTAD relativo al cambio de domicilio del/de la menor [NOMBRE DEL MENOR] cuya guarda y custodia tiene atribuida mi mandante, de conformidad con los siguientes

HECHOS

PRIMERO Por sentencia núm. [Nº], de [DÍA] de [MES] de [AÑO], dictada por el Tribunal al que tengo el honor de dirigirme, puede tratarse también de un procedimiento contencioso, en cuyo caso, las referencias que se hacen a continuación al convenio regulador judicialmente homologado, lo serían a las medidas adoptadas por el Juez, en la que se procedió a homologar el Convenio regulador de fecha [DÍA] de [MES] de [AÑO], presentado por las partes, se atribuyó a mi representado/a la guarda y custodia del hijo/a menor de los cónyuges [NOMBRE Y APELLIDOS], sin que ello obste a la titularidad conjunta de la patria potestad que ambos ostentan sobre el mismo.

Se acompaña testimonio de la citada sentencia, en el que consta su firmeza, así como del convenio regulador que la misma homologaba, como DOCUMENTO Nº [Nº DE DOCUMENTO] con remisión, a efectos probatorios, a los archivos de este Tribunal.

SEGUNDO Como consecuencia del ERE que ha afectado a la empresa en que trabaja mi mandante, y en cumplimiento de los criterios sobre movilidad geográfica adoptados en el Convenio regulador del ERE, mi representado/a se ve abocada, por decisión de la empresa, a trasladarse a la ciudad de [LOCALIDAD], quedándole como única alternativa posible el despido indemnizado. Por tanto, el cambio de domicilio deriva de una situación de necesidad por motivos laborales, que no es imputable a mi mandante.

Se acompañan, como DOCUMENTOS Nº [Nº DE DOCUMENTO] a [Nº DE DOCUMENTO], para acreditar los hechos anteriores, los siguientes:

TERCERO En fecha [DÍA] de [MES] de [AÑO], tras varias conversaciones infructuosas con este, mi representado remitió al padre/madre del/de la menor un burofax en que le comunicaba su necesidad y decisión, por los motivos expuestos, de cambiar su domicilio, en el que convive con el citado hijo común y que hasta entonces estaba fijado en:

Se acompaña como DOCUMENTO Nº [Nº DE DOCUMENTO] el citado burofax, para acreditar los hechos referidos.

En fecha [DÍA] de [MES] de [AÑO], el padre/madre del/de la menor cursó, a su vez, un burofax a mi mandante en que expresaba su oposición frontal al cambio de domicilio.

Se acompaña como DOCUMENTO Nº [Nº DE DOCUMENTO] el citado burofax, para acreditar los hechos referidos.

CUARTO El cambio de domicilio no obsta a que sea conveniente para el interés, prevalente, del/de la menor, mantener el régimen de guarda y custodia establecido en la citada sentencia en favor de mi mandante. Dicha conveniencia se basa en las siguientes consideraciones:

QUINTO Los hechos antes expuestos justifican que se autorice a mi mandante a trasladar su domicilio al siguiente:

A los anteriores hechos les son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

JURISDICCIÓN Y COMPETENCIA. Es competente el Tribunal al que me dirijo, conforme a lo previsto en los arts. 2 y 68.2.segundo inciso de la Ley de la Jurisdicción Voluntaria.

CAPACIDAD.- Tiene mi mandante capacidad para promover este procedimiento, conforme a lo dispuesto en los artículos 6 y ss LEC.

LEGITIMACIÓN.-Ostenta mi representado/a legitimación activa en su condición de progenitor del menor, correspondiendo la pasiva al otro progenitor, titulares ambos de la patria potestad sobre el menor, de conformidad con lo dispuesto en el artículo 154, 156.II del Código civil y en el artículo 86.3 de la Ley de la Jurisdicción voluntaria.

REPRESENTACIÓN Y DEFENSA.- Aunque en virtud del art. 85.3 de la Ley de la Jurisdicción Voluntaria, en la tramitación del presente expediente no es preceptiva la intervención de Abogado ni Procurador, el art. 3.2, segundo inciso de la citada ley establece que las partes que lo deseen podrán actuar asistidas o representadas por Abogado y Procurador, respectivamente, como se hace en la presente solicitud.

PROCEDIMIENTO.- Deben seguirse en este asunto las normas sobre jurisdicción voluntaria establecidas con carácter general en los artículos 17 a 22 LJV y las específicas contenidas en los artículos 85 y siguientes LJV, dando audiencia a los hijos menores al tratarse de decisiones que les afecten directamente, conforme a lo establecido en el art. 154.III CC.

DERECHO SUSTANTIVO.- Resultan aplicables los artículos 154 y 156.II del Código civil. El art. 154 CC establece: “La patria potestad, como responsabilidad parental, se ejercerá siempre en interés de los hijos e hijas, de acuerdo con su personalidad, y con respeto a sus derechos, su integridad física y mental. Esta función comprende los siguientes deberes y facultades: 1.º Velar por ellos, tenerlos en su compañía, alimentarlos, educarlos y procurarles una formación integral. 2.º Representarlos y administrar sus bienes. 3.º Decidir el lugar de residencia habitual de la persona menor de edad, que solo podrá ser modificado con el consentimiento de ambos progenitores o, en su defecto, por autorización judicial”.

Iura novit curia y cuantas normas resulten procedentes.

GASTOS.-Se rigen por lo dispuesto en el artículo 7 de la Ley de la Jurisdicción Voluntaria.

Por lo expuesto:

SUPLICO AL TRIBUNAL

Que teniendo por presentado este escrito con los documentos que se acompañan y copia de todo ello, lo admita, y tenga por promovida por el Procurador que suscribe, con quien habrán de entenderse las sucesivas diligencias en nombre y representación de D.Dª [NOMBRE Y APELLIDOS], EXPEDIENTE DE JURISDICCIÓN VOLUNTARIA en solicitud de INTERVENCIÓN JUDICIAL POR DESACUERDO EN EL EJERCICIO DE LA PATRIA POTESTAD, a fin de autorizar el cambio de domicilio del menor D.Dª [NOMBRE Y APELLIDOS], y previos los trámites legales oportunos, con intervención del Ministerio Fiscal, se digne dictar resolución por la que, estimando lo solicitado, conceda a mi mandante la autorización solicitada para trasladar su domicilio, junto con su hijo menor [NOMBRE Y APELLIDOS], a

En [LOCALIDAD], a [DÍA], de [MES], de [AÑO]

Firma y número del Letrado	Firma del Procurador

========================================================================
