---
name: demanda-alteracion-no-consentida-elementos-privativos-civ-0654
description: "Demanda por alteración no consentida de elementos privativos que afecta a elementos comunes. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda por alteración no consentida de elementos privativos que afecta a elementos comunes

> Formulario **CIV-0654** del plugin **Comunidades de propietarios** (`formularios-comunidades-de-propietarios`) · Civil › Propiedad horizontal · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario por la que se ejercita por el copropietario de una vivienda una acción de propiedad horizontal frente a otros condóminos por la alteración inconsentida de elementos privativos que afecta a elementos comunes como es la instalación, sin autorización de la Comunidad, en una terraza privativa de un horno o parrilla con su correspondiente chimenea anclada al paramento de la pared zaguera de la casa cegando la bajante de aguas pluviales.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda por alteración no consentida de elementos privativos que afecta a elementos comunes» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda por alteración no consentida de elementos privativos que afecta a elementos comunes” para mi caso». También puedes invocarla directamente con `/formularios-comunidades-de-propietarios:demanda-alteracion-no-consentida-elementos-privativos-civ-0654`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-comunidades-de-propietarios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Comunidades de propietarios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] NÚMERO (6 veces)
- [ ] CALLE (2 veces)
- [ ] LETRA (2 veces)
- [ ] MES (2 veces)
- [ ] PISO (2 veces)
- [ ] AÑO
- [ ] COLEGIO
- [ ] FECHA
- [ ] IMPORTE
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] Nº
- [ ] SEDE

## Normas que cita el formulario

- art. 9.2 LOPJ
- art. 36 LEC
- art. 44 LEC
- art. 85.1 LOPJ
- art. 52.1.8.º LEC
- art. 54.1 LEC
- art. 58 LEC
- art. 129 Ley 5/2015
- art. 253.1 LEC
- art. 394.3 LEC
- art. 251.11.ª LEC
- art. 25 LEC
- art. 23 LEC
- art. 5 Ley Orgánica 1/2025
- art. 7.1 LPH
- art. 706 LEC
- art. 394 LEC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a. de los Tribunales, y de D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño a este escrito, y con asistencia del Letrado en ejercicio del Iltre. Colegio de Abogados de [COLEGIO], D./Dña. [NOMBRE Y APELLIDOS], con despacho abierto en esta localidad, calle [CALLE], ante el Tribunal comparezco y como mejor proceda en derecho, DIGO:

Que mediante el presente escrito y siguiendo instrucciones de mi mandante formulo demanda de juicio ordinario sobre acción de propiedad horizontal contra D./Dña. [NOMBRE Y APELLIDOS], y su esposa D./Dña. [NOMBRE Y APELLIDOS]), acción que se ejercita en interés de la Comunidad de Propietarios.

HECHOS

PRIMERO.- Mi mandante es propietario de la vivienda sita en el edificio de la calle [CALLE] n.º [NÚMERO] planta [PISO] letra [LETRA] con un coeficiente de participación en los elementos comunes del [Nº] por ciento, cuya descripción y lindes constan en la escritura que se acompaña como documento n.º [NÚMERO].

SEGUNDO.- Los codemandados son a su vez propietarios del piso sito en el mismo edificio, planta [PISO] letra [LETRA], cuyas demás circunstancias descriptivas constan en la certificación del Registro de la Propiedad correspondiente a la finca, que se acompaña como documento n.º [NÚMERO].

TERCERO.- Por ambos citados pisos se accede a una terraza, que es elemento privativo como así se deduce de los títulos acompañados, y aproximadamente entre los meses de [MES] y de [MES] del año [AÑO] la parte demandada por su cuenta, y sin autorización del resto de la Comunidad, efectuó una obra en dicha terraza consistente en la instalación de un horno o parrilla con su correspondiente chimenea anclada al paramento de la pared zaguera de la casa, precisamente cegando la bajante de aguas pluviales, lo que figura en acta notarial que acompañamos como documento n.º [NÚMERO], al que se adjunta reportaje fotográfico.

CUARTO.- Por mi mandante se intentó una solución amistosa requiriendo al demandado al derribo de la construcción, no teniendo efecto el acto de conciliación presentado, a los efectos de cumplir el requisito de procedibilidad para la iniciación de la vía jurisdiccional, según acredita el documento n.º [NÚMERO].

A los anteriores hechos son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA

A) JURISDICCIÓN.

POTESTAD JURISDICCIONAL. La potestad jurisdiccional se ejerce por los Jueces y Tribunales determinados por las leyes, según las normas de competencia y procedimiento que las mismas establezcan (art. 117.3 CE).

JURISDICCIÓN CIVIL. Los Tribunales del orden civil conocerán, además de las materias que les son propias, de todas aquellas que no estén atribuidas a otro orden jurisdiccional (art. 9.2 LOPJ).

ÁMBITO DE LA JURISDICCIÓN. La extensión y límites de la jurisdicción de los Tribunales civiles españoles se determinará por lo dispuesto en la LOPJ y en los tratados y convenios internacionales en los que España sea parte (art. 36 LEC), no existiendo en el presente asunto elemento ninguno de extranjería.

B) COMPETENCIA

PREDETERMINACIÓN LEGAL DE LA COMPETENCIA. Para que los Tribunales civiles tengan competencia en cada caso se requiere que el conocimiento del pleito les esté atribuido por normas con rango de ley y anteriores a la incoación de las actuaciones de que se trate (art. 44 LEC).

COMPETENCIA OBJETIVA.

Corresponde a las secciones civiles de los tribunales de instancia, puesto que no viene atribuida por Ley esta causa civil a otros Tribunales (art. 85.1 LOPJ y 45 LEC).

COMPETENCIA TERRITORIAL.

Resulta competente el Tribunal a que me honro en dirigirme por ser del partido del lugar donde está sita la finca, conforme al mandato del art. 52.1.8.º LEC, que es fuero necesario (art. 54.1 LEC), controlable ‘ex officio iudicis’, a instancia del Letrado de la Administración de Justicia, en trámite de admisión de la demanda (art. 58 LEC).

II.- PROCEDIMIENTO

Conforme al número 8.º del art. 249.1 de la Ley de Enjuiciamiento Civil el procedimiento ajustado a derecho, por tratarse de acción que otorga a los propietarios la Ley de propiedad Horizontal, será el del juicio declarativo ordinario regulado en los arts. 399 a 436 de la misma Ley.

III.- LEGITIMACIÓN ACTIVA Y PASIVA

Les corresponde al demandante la legitimación activa, por el derecho y acción que tiene para reclamar, como señala la Ley de Propiedad Horizontal, ya que cualquier alteración de un elemento común hace necesario el consentimiento unánime de la Junta de Propietarios, siendo uno de ellos mi mandante, siendo jurisprudencia que la legitimación legal del Presidente de la comunidad no excluye la de cualquiera de los comuneros, ante la pasividad del representante orgánico del ente, y siempre que se actúe, como se hace, en beneficio del común, con base en las reglas supletorias de la comunidad de bienes de los arts. 392 y ss. CCiv [SSTS de 17 de abril de 1990 y 22 de octubre de 1993, rec. 3089/1990].

La legitimación pasiva corresponde a los codemandados, puesto que son matrimonio en régimen de bienes supletorio legal, que es el de comunicación foral, por vecindad en Tierra Llana de Bizkaia, de modo que el inmueble es común por mitad, según el art. 129 de la Ley 5/2015, de 25 de junio, de Derecho Civil Vasco, figurando inscrita la finca que es su participación en la comunidad y lugar de la obra inconsentida como presuntivamente ganancial, y precaverse el eventual embargo en términos del art. 144 RH, ambos que han realizado en su patrimonio las obras que han alterado un elemento común sin consentimiento del resto de comuneros.

IV.- CUANTÍA

En cumplimiento del art. 253.1 LEC, puesto que la cuantía litigiosa resulta estimable, y tiene su importancia a efectos de una eventual limitación de la condena en costas a tenor del art. 394.3 LEC, se hace constar que la cuantía de esta demanda es la de [IMPORTE] euros ( €), conforme al art. 251.11.ª LEC, ya que se pretende una prestación de hacer (demolición de la obra inconsentida), fungible, cuyo costo es el indicado, y a tal acreditación se aporta presupuesto de ‘Construcciones ’ como documento n.º [NÚMERO].

V.- POSTULACIÓN Y DEFENSA

El actor ha otorgado poder notarial al Procurador/a. de los Tribunales que encabeza este escrito, habilitado en el partido del Tribunal, cuya copia auténtica se ha aportado, general para pleitos (art. 25 LEC), siendo redactada y firmada la demanda por abogado ejerciente colegiada que redacta y firma, según resulta preceptivo conforme a los arts. 23 y 31 LEC.

VI.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VII.- FONDO DEL ASUNTO

La obra realizada lo ha sido en una terraza que es elemento privativo, y su alteración no precisaba el acuerdo unánime de la Junta de propietarios, mas dicha obra altera la estructura general del edificio y su configuración exterior y daña gravemente su seguridad. Y ello tanto por la factura de la chimenea, como su uso para hacer fuego, según resulta evidente, dado que se adosa a la pared de la casa, y además obstruye la bajante de pluviales que se hallaba inmediatamente detrás de lo que ahora oculta la obra, por lo que perjudica los derechos de otros propietarios e inutiliza elementos comunes (art. 7.1 LPH).

La jurisprudencia de la Sala Primera Tribunal Supremo [SS de 20 de marzo de 1984, 17 de julio de 1987 y 23 de mayo de 1989 ] previenen en casos como el presente, en que no se cuenta con el permiso de la Comunidad, y la obra afectante a lo común ha sido clandestina, que se está en la obligación de dejar el elemento común en su primitivo estado, lo cual se ha negado a verificar el demandado, a pesar de ser requerido fehacientemente para ello, y que tendrá lugar, en su caso, a través de la ejecución en términos del art. 706 LEC.

VIII.- COSTAS.

Conforme al art. 394 LEC las costas han de imponerse a la parte demandada, por principio objetivo del vencimiento

Por lo expuesto,

SUPLICO AL TRIBUNAL:

Que teniendo por presentado este escrito y documentos que le acompañan, con sus copias, lo admita a trámite, me tenga por comparecido y parte, y admita a trámite la demanda que se formula, acordando conferir traslado de la misma a los demandados D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS] emplazándoles para que, si es sus interés, comparezcan y la contesten, y seguido el juicio por sus trámites, se dicte en definitiva sentencia por la que estimando íntegramente la demanda, se declare la ilicitud de la obra realizado por los demandados y descrita en el cuerpo de esta demanda, condenándoles a su inmediata demolición a fin de restablecer en su primitivo estado los elementos comunes inutilizados, con el apercibimiento de ejecutarse a su costa. Todo ello con imposición de costas a dichos demandados.

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a

========================================================================
