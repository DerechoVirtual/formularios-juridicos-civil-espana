---
name: demanda-extinguir-arrendamiento-local-negocio-lau-1964-civ-0530
description: "Demanda para extinguir el arrendamiento de local de negocio (LAU 1964) por necesidad del hijo. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda para extinguir el arrendamiento de local de negocio (LAU 1964) por necesidad del hijo

> Formulario **CIV-0530** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda para extinguir el arrendamiento de local de negocio (LAU 1964) por necesidad del hijo» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda para extinguir el arrendamiento de local de negocio (LAU 1964) por necesidad del hijo” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:demanda-extinguir-arrendamiento-local-negocio-lau-1964-civ-0530`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (11 veces)
- [ ] LOCALIDAD (7 veces)
- [ ] Nº DE DOCUMENTO (7 veces)
- [ ] AÑO (5 veces)
- [ ] MES (5 veces)
- [ ] DÍA (4 veces)
- [ ] NÚMERO (3 veces)
- [ ] CALLE (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] COLEGIO
- [ ] DNI/NIE
- [ ] FECHA
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] Nº
- [ ] SEDE

## Normas que cita el formulario

- art. 65 LAU
- art. 52.7 LEC
- art. 85.1 LOPJ
- art. 249.1.6 LEC
- art. 5 Ley Orgánica 1/2025
- art. 114 LAU
- art. 394 LEC
- art. 253 LEC
- art. 251.9 LEC

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

D./Dª [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en nombre y representación de D./Dª [NOMBRE Y APELLIDOS], cuya representación acreditaré mediante comparecencia apud acta cuando sea requerido para ello o bien: “según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº ”, comparezco ante el TRIBUNAL que corresponda por turno de reparto, con la asistencia del Letrado D./Dª [NOMBRE Y APELLIDOS], del Ilustre Colegio de Abogados de [COLEGIO], y DIGO:

Que por medio del presente escrito y en la representación que ostento, interpongo demanda de JUICIO ORDINARIO contra D./Dª [NOMBRE Y APELLIDOS], mayor de edad, con domicilio en [LOCALIDAD], calle [CALLE], nº [NÚMERO], pta., y DNI [DNI/NIE], en ejercicio de acción de RESOLUCIÓN DE CONTRATO DE ARRENDAMIENTO DE LOCAL DE NEGOCIO. La presente demanda se basa en los siguientes.

HECHOS

PRIMERO.- Mi representado formalizó en fecha [FECHA] de [MES], contrato de arrendamiento de local de negocio sito en [LOCALIDAD], calle [CALLE], nº [NÚMERO], pta., con el demandado D./Dª [NOMBRE Y APELLIDOS], con destino a la instalación de una consulta médica, con una duración de [Nº] años, formalizado en escritura pública otorgada en fecha [DÍA] de [MES] de [AÑO], ante el Notario de [LOCALIDAD], D./Dª [NOMBRE Y APELLIDOS], con número [NÚMERO] de protocolo. Se acompaña copia del citado contrato como DOCUMENTO Nº [Nº DE DOCUMENTO]

SEGUNDO.- Mi representado necesita el referido local para que lo ocupe su hijo D./Dª [NOMBRE Y APELLIDOS] Este tiene instalado, desde hace varios años, un negocio de gestoría y asesoría jurídica en el local contiguo al que ocupa el demandado, en virtud de un contrato de arrendamiento con su propietario, D./Dª [NOMBRE Y APELLIDOS] que finaliza el día [DÍA] de [MES] de [AÑO] sin posibilidad de prórroga. Dado que ni mi representado ni su hijo disponen de otro local en esta localidad, en el que pueda seguir ejerciendo su negocio, necesita, a tal efecto, el que ocupa en la actualidad el demandado. Se acompaña como DOCUMENTO Nº [Nº DE DOCUMENTO], el contrato de arrendamiento del local en el que el hijo de mi representado tiene instalada actualmente su gestoría, y como DOCUMENTOS Nos los siguientes: destinados a acreditar el ejercicio de la actividad referida por parte del hijo de mi representado/a desde el año [AÑO] hasta el momento actual y, por tanto, con más de un año de antelación a la fecha del requerimiento al que se refiere el Hecho Cuarto de esta demanda se puede aportar, entre otros, certificado del alta en el Impuesto de Actividades Económicas. Se acompaña, igualmente, como DOCUMENTO Nº [Nº DE DOCUMENTO], certificado literal de la inscripción de nacimiento del hijo de mi representado expedida por el Encargado del Registro Civil de [LOCALIDAD], en fecha [DÍA] de [MES] de [AÑO], para acreditar su relación de parentesco.

TERCERO.- Como ya hemos expresado, ni mi representado ni su hijo disponen de otros locales de su propiedad, en la misma localidad, donde se pueda instalar el referido negocio de gestoría-asesoría. Se presenta como DOCUMENTOS Nos y [Nº DE DOCUMENTO] notas simples informativas expedidas por el Registro de la Propiedad de [LOCALIDAD], acreditativas de no contar ni mi representado ni su citado hijo con inmuebles a su nombre que puedan destinarse al uso indicado, en la citada localidad. Si en la localidad de que se trata hay varias Oficinas del Registro de la Propiedad, pueden acompañarse notas simples expedidas por cada una de ellas.

CUARTO.- Cumpliendo con lo preceptuado en el art. 65 LAU/1964, ley a la que se encuentra sujeto el contrato de arrendamiento litigioso, por razón de su fecha, mi representado requirió fehacientemente al demandado, D./Dª [NOMBRE Y APELLIDOS] en denegación de la prórroga del contrato de arrendamiento. A tal efecto le comunicó el nombre de la persona que necesita la vivienda y la causa de la necesidad en que se funda la denegación de la prórroga contractual, así como la inexistencia de otros locales de su propiedad en la misma localidad. Así mismo, le ofreció una indemnización de [IMPORTE] euros ( €). Se acompaña como DOCUMENTO Nº [Nº DE DOCUMENTO], copia del citado requerimiento.

QUINTO.- El arrendatario, contra quien se dirige esta demanda, respondió, de modo fehaciente, al citado requerimiento dentro del plazo legal de treinta días, oponiéndose a la denegación de la prórroga y rechazando la indemnización ofrecida. Se acompaña como DOCUMENTO Nº [Nº DE DOCUMENTO], copia de la respuesta del arrendatario.

Resultan aplicables a los citados hechos los siguientes

SEXTO.- Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

FUNDAMENTOS DE DERECHO

I. JURISDICCIÓN.- Es competente la jurisdicción civil, de acuerdo con lo establecido en el art. 22.1º de la Ley Orgánica del Poder Judicial.

II. COMPETENCIA.- Son competentes las secciones civiles de los Tribunales de Instancia de [LOCALIDAD], lugar en que se halla situada la finca, de acuerdo con el artículo 52.7º LEC, en relación con lo dispuesto en el art. 85.1º LOPJ.

III. PROCEDIMIENTO.- La presente demanda debe sustanciarse por los trámites del juicio ordinario, en virtud de lo dispuesto en el artículo 249.1.6º LEC, según el cual se decidirán en juicio ordinario, cualquiera que sea su cuantía, las demandas que versen sobre cualesquiera asuntos relativos a arrendamientos urbanos o rústicos de bienes inmuebles, salvo que se trate de desahucio por falta de pago o por extinción del plazo de la relación arrendaticia, o salvo que sea posible hacer una valoración de la cuantía del objeto del procedimiento, en cuyo caso el proceso será el que corresponda a tenor de las reglas generales de esta Ley.

IV. CAPACIDAD.- Ambas partes tienen capacidad para serlo, conforme a lo dispuesto en los artículos 6 y ss. LEC.

V. LEGITIMACIÓN.- Están legitimados activa y pasivamente, el/la demandante y el/la demandada. El primero, como propietario y arrendador del local y, el segundo, como arrendatario del mismo.

VI. REPRESENTACIÓN Y DEFENSA.- El/La demandante comparece representado y defendido, respectivamente, por el Procurador y el Letrado que constan en el encabezamiento de este escrito, de acuerdo con lo dispuesto en los artículos 23.1 y 31.1 LEC.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VII. DERECHO SUSTANTIVO.- En atención a la fecha del contrato, el mismo se halla sujeto a la Ley de Arrendamientos Urbanos de 24 de diciembre de 1964, en virtud de la Disposición Transitoria 3ª LAU/1994.

En concreto, resulta de aplicación el art. 114 LAU/1964 y, por remisión de éste, los artículos 62.1º y 70 y ss. de la misma Ley. De acuerdo con ellos procede denegar la prórroga legal del contrato por necesitarlo el arrendador para que lo ocupen sus descendientes, en este caso, su hijo, para ejercer en él la actividad económica antes referida, y hallarse el hijo establecido en actividad de comercio o industria con más de un año de antelación a la fecha del requerimiento.

VIII. COSTAS.-Procede imponer al/a la demandado/a el pago de las costas, en virtud de lo dispuesto en los arts. 394 y 395 LEC, en la medida en que se oponga a la presente demanda.

Por lo expuesto

SUPLICO AL TRIBUNAL:

Que tras admitir este escrito con los documentos que lo acompañan y sus copias, tenga por interpuesta demanda, que habrá de sustanciarse por los trámites del juicio ordinario, en nombre de D./Dª [NOMBRE Y APELLIDOS], en ejercicio de la acción de extinción de contrato de arrendamiento de local de negocio por denegación de prórroga, contra D./Dª [NOMBRE Y APELLIDOS], dándole traslado de la misma; y, previos los trámites legales que procedan, dicte sentencia en la que, estimando íntegramente la demanda, declare extinguido el contrato de arrendamiento por concurrir causa de denegación de prórroga forzosa, por necesitar mi representado el local para que lo ocupe su hijo, y condene al demandado/a a dejarlo libre y a disposición del demandante, apercibiéndole de su lanzamiento si no lo realiza en el plazo legal, con expresa imposición de costas a aquél.

OTROSÍ DIGO.- En cumplimiento de lo dispuesto en el art. 253 LEC, esta parte fija la cuantía del procedimiento, calculada de acuerdo con lo dispuesto en el art. 251.9 LEC en [IMPORTE] euros.

En [LOCALIDAD], a [DÍA], de [MES], de [AÑO]

Firma y número del Letrado	Firma del Procurador

========================================================================
