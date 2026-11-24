---
name: demanda-separacion-presentada-medidas-provisionales-civ-0167
description: "Demanda de separación presentada con medidas provisionales previas vigentes. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de separación presentada con medidas provisionales previas vigentes

> Formulario **CIV-0167** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Traslado de copia procurador contrario Tribunal y número de procedimiento de medidas provisionales previas Procurador, representación Asistencia letrada y acción que se ejercita (separación contenciosa) HECHOS FUNDAMENTOS DE DERECHO Suplico Primer Otrosí digo: Subsistencia medidas provisionales Segundo Otrosí digo: prueba anticipada Firmas

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de separación presentada con medidas provisionales previas vigentes» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de separación presentada con medidas provisionales previas vigentes” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-separacion-presentada-medidas-provisionales-civ-0167`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (10 veces)
- [ ] AÑO (7 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] DÍA (5 veces)
- [ ] MES (5 veces)
- [ ] Nº (5 veces)
- [ ] NÚMERO (3 veces)
- [ ] SEDE (3 veces)
- [ ] LIBRO (2 veces)
- [ ] TOMO (2 veces)
- [ ] CALLE
- [ ] COLEGIO
- [ ] LUGAR
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] Nº DE DOCUMENTO

## Normas que cita el formulario

- art. 772 LEC
- art. 770 LEC
- art. 749 LEC
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 81 Código Civil

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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…AMILIA, INFANCIA Y CAPACIDAD DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Denominación legal: Sección de Familia, Infancia y Capacidad. Si no existe en el partido, conoce la Sección Civil o la Única (art. 86.3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «….3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

Traslado al Procurador Don [NOMBRE Y APELLIDOS]

Antecedentes

Tribunal de Instancia de [SEDE], plaza n.º [NÚMERO]

Medidas provisionales previas: /

A LA SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D./Dª [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en nombre de DON, representación que acredito mediante primera copia de escritura de poder que acompaño, ante el Tribunal comparezco y DIGO:

Que mediante el presente escrito, bajo la dirección del/la Letrado/a del Ilustre Colegio de Abogados de [COLEGIO], D./Dª [NOMBRE Y APELLIDOS], formulo demanda de separación contenciosa frente a DOÑA [NOMBRE Y APELLIDOS], vecina de [LOCALIDAD], con domicilio en [LOCALIDAD], nº [NÚMERO], pta.

Basamos la demanda en los siguientes:

HECHOS

Demandante y demandada contrajeron entre sí matrimonio canónico en [LOCALIDAD], el día [DÍA] de [MES] de [AÑO] Consta el matrimonio inscrito en el Registro civil de [LOCALIDAD], al Tomo [TOMO], libro [LIBRO], página

Adjunto aportamos como DOCUMENTO NÚM. UNO certificado literal de matrimonio.

De dicho matrimonio nació en [LOCALIDAD] un hijo, el día [DÍA] de [MES] de [AÑO], que actualmente cuenta con la edad de [Nº] años. Consta el nacimiento inscrito en el Registro civil de [LOCALIDAD], al Tomo [TOMO], libro [LIBRO], página

Adjunto aportamos como DOCUMENTO NÚM. DOS certificado literal de nacimiento.

El domicilio familiar estaba fijado en la calle [CALLE], nº [NÚMERO], pta., de la ciudad de [LOCALIDAD], tal y como acreditamos mediante certificado de empadronamiento que adjunto acompañamos como DOCUMENTO NÚM. TRES.

El matrimonio se regía por el régimen económico de separación de bienes, habiendo otorgado capitulaciones matrimoniales el día [DÍA] de [MES] de [AÑO], ante el Notario del Ilustre Colegio de Notarios de [LOCALIDAD], Don [NOMBRE Y APELLIDOS], obrante al núm. [Nº] de su protocolo.

Aportamos como DOCUMENTO NÚM. CUATRO escritura de capitulaciones matrimoniales.

Mi mandante, con carácter previo a esta demanda formuló solicitud de medidas provisionales previas que se siguieron ante este Tribunal bajo el núm. [Nº]/[AÑO] de procedimiento.

En dicha pieza de medidas se dicto auto en fecha [DÍA] de [MES] de [AÑO], por el que se acordaba:

1.- Otorgar la guarda y custodia del menor al padre.

2.- Conceder un derecho de visitas a favor de la madre consistente en fines de semana alternos, desde la salida del colegio hasta la vuelta al centro escolar el lunes, y la mitad de todos los periodos vacacionales del menor.

3.- Se fijaba como pensión alimenticia a cargo de la madre la suma mensual de 450 €, así como la mitad de los gastos extraordinarios, debiendo abonar la mitad de la cuota mensual del préstamo hipotecario que grava la vivienda familiar.

4.- Adjudicar el uso del domicilio familiar al padre y al menor.

Adjunto acompañamos como DOCUMENTO NÚM. CINCO copia testimoniada del auto recaído en el procedimiento de referencia.

Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

A los anteriores hechos les son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

Competencia

Es competente la sección de familia, infancia y capacidad del Tribunal de Instancia de [SEDE] al que se dirige la presente demanda, por ser aquel en el que se tramitaron las medidas provisionales previas, al amparo del artículo 772 LEC.

Procedimiento

Deberá seguirse la demanda por los cauces procedimentales previstos para el divorcio contencioso en el artículo 770 de la LEC.

Legitimación

Está legitimado para instar la disolución de su matrimonio, por divorcio, cualquiera de los cónyuges.

Deberá ser parte el Ministerio Fiscal al haber hijos menores de edad (art. 749 LEC).

Cumplimiento de los requisitos de procedibilidad

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

Acción que se ejercita

Ejercitamos en la presente demanda acción declarativa de la separación del matrimonio, al amparo del artículo 81 del Código Civil.

El artículo 81 del Código Civil dispone que se decretará judicialmente la separación cualquiera que sea la forma de celebración del matrimonio: A petición de uno solo de los cónyuges, una vez transcurrido tres meses desde la celebración del matrimonio.

Costas

Deberán imponerse al demandado si se opone a la demanda.

Medidas

Proponemos se acuerden como definitivas las medidas adoptadas en la pieza de medidas provisionales previas núm. [Nº]/[AÑO] seguidas ante este Tribunal, y en concreto:

1.- Se otorgue la guarda y custodia del menor al padre.

2.- Se conceda un derecho de visitas a favor de la madre consistente en fines de semana alternos, desde la salida del colegio hasta la vuelta al centro escolar el lunes, y la mitad de todos los periodos vacacionales del menor.

3.- Se fije como pensión alimenticia a cargo de la madre la suma mensual de 450 €, así como la mitad de los gastos extraordinarios, debiendo abonar la mitad de la cuota mensual del préstamo hipotecario que grava la vivienda familiar.

4.- Se adjudique el uso del domicilio familiar al padre.

Por lo expuesto:

SUPLICO AL TRIBUNAL tenga por presentado este escrito junto con los documentos que se acompañan, me tenga por parte en la representación que otorgada por Don [NOMBRE Y APELLIDOS], asumo, entendiéndose conmigo las sucesivas actuaciones, por formulada demanda de separación contra Dª., y una vez emplazada, contestada la demanda, y celebrado el juicio, se dicte sentencia por la que se decrete la separación del matrimonio contraído entre sí por demandante y demandada, acordándose las siguientes medidas definitivas:

1.- Se otorgue la guarda y custodia del menor al padre.

2.- Se conceda un derecho de visitas a favor de la madre consistente en fines de semana alternos, desde la salida del colegio hasta la vuelta al centro escolar el lunes, y la mitad de todos los periodos vacacionales del menor.

3.- Se fije como pensión alimenticia a cargo de la madre la suma mensual de 450 €, así como la mitad de los gastos extraordinarios, debiendo abonar la mitad de la cuota mensual del préstamo hipotecario que grava la vivienda familiar.

4.- Se adjudique el uso del domicilio familiar al padre.

Y en su día se libre los oficios correspondientes al Registro civil de [LOCALIDAD]

PRIMER OTROSÍ DIGO que habiéndose formulado la demanda antes de haber transcurrido treinta días desde la adopción de las medidas provisionales previas, SUPLICO AL TRIBUNAL acuerde el testimonio de dicha pieza de medidas en los presentes autos, y se declare que las mismas permanecerán vigentes hasta que se dicte sentencia.

SEGUNDO OTROSÍ DIGO que en concepto de prueba anticipada se acuerde la práctica de las siguientes:

1.- Informe del gabinete psicosocial del Tribunal sobre la conveniencia de que la guarda y custodia se otorgue al padre dada la patología psicológica que padece la madre del menor.

2.- Se requiera a la demanda para que aporte antes del Juicio las nóminas que percibe como trabajadora del Ayuntamiento de [LOCALIDAD], así como la declaración del IRPF de las tres últimas anualidades.

Por lo que, SUPLICO AL TRIBUNAL que acuerde lo necesario para la práctica anticipada de dichos medios de prueba.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma y número Abogado	Firma Procurador

========================================================================
