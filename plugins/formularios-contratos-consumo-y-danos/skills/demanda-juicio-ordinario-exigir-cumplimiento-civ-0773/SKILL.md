---
name: demanda-juicio-ordinario-exigir-cumplimiento-civ-0773
description: "Demanda de juicio ordinario para exigir el cumplimiento de una compraventa de bien mueble. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio ordinario para exigir el cumplimiento de una compraventa de bien mueble

> Formulario **CIV-0773** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio declarativo ejercitando acción para instar el cumplimiento del contrato de compraventa para que el comprador proceda a la recepción de la cosa en los términos pactados

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio ordinario para exigir el cumplimiento de una compraventa de bien mueble» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio ordinario para exigir el cumplimiento de una compraventa de bien mueble” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-juicio-ordinario-exigir-cumplimiento-civ-0773`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] IMPORTE (8 veces)
- [ ] FECHA (5 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] CALLE (2 veces)
- [ ] COLEGIO
- [ ] DESCRIPCIÓN DE LOS DAÑOS
- [ ] LUGAR
- [ ] MARCA/MODELO
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] NÚMERO
- [ ] SEDE

## Normas que cita el formulario

- art. 21 LOPJ
- art. 85 LOPJ
- art. 50.1 LEC
- art. 10 LEC
- art. 23 LEC
- art. 5 Ley Orgánica 1/2025
- art. 1124 CC
- art. 394.1 LEC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…rador/a ========================================================================»: requisito de procedibilidad del art. 5 LO 1/2025 — antes de presentar la demanda hay que intentar un medio adecuado de solución de controversias (MASC) y acreditarlo con la demanda (arts. 264.4.º y 399.3 LEC), salvo las materias excluidas del art. 5.2. Fuente: LO 1/2025, arts. 5 a 7 (BOE-A-2025-76).

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

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en nombre y representación de [NOMBRE DEL REPRESENTADO/A], con domicilio en [LOCALIDAD], calle [CALLE], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño a este escrito, ante el Tribunal comparezco, bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS], Abogado del Ilustre Colegio de Abogados de [COLEGIO], con despacho profesional en [LOCALIDAD], y como mejor proceda en Derecho DIGO:

Que por medio del presente escrito, formulo demanda de JUICIO

ORDINARIO

verbal [IMPORTE] en ejercicio de acción de cumplimiento de obligación de hacer contra D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], calle [CALLE], y ello en base a los siguientes:

HECHOS

PRIMERO.- En fecha [FECHA] mi representada, en calidad de vendedora, suscribió un contrato de compraventa con la compradora D./Dña. [NOMBRE Y APELLIDOS]

El contrato tenía por objeto una cocina, de instalación y puesta en funcionamiento que recoge el presupuesto n.º [NÚMERO], de fecha [FECHA]

Se aportan copia simple del contrato de compraventa y presupuesto previamente aceptado por el demandado como documentos [Nº DE DOCUMENTO]

SEGUNDO.- El precio de la compraventa quedó fijado en la cantidad de [IMPORTE] euros, y para el pago del mismo se fijó un sistema que consistía en la entrega en ese acto de [IMPORTE] euros en efectivo, tal como consta en el propio contrato, y respecto al resto, [IMPORTE] euros, quedó diferido hasta el momento en que se verificase la entrega de la cocina.

De los términos del contrato, aceptado expresamente por el demandado, se deducen claramente los términos concretos de su cumplimiento: bien concreto objeto del contrato, plazo máximo de entrega, obligación de recepción del comprador, plazo de recepción, y precio convenido.

TERCERO.- Con fecha [FECHA], una semana antes del vencimiento del plazo de entrega, mi representada se puso en contacto con D./Dña. [NOMBRE Y APELLIDOS], comunicando al comprador tener a su disposición la cocina objeto del contrato para proceder a su instalación en el domicilio del demandado, previa entrega del precio que quedaba pendiente de pago, en los términos convenidos, obteniendo la negativa de D./Dña. [NOMBRE Y APELLIDOS] a su recepción, y resultando infructuosas todas las gestiones realizadas por mi representada para intentar la entrega durante las semanas posteriores, pese a las insistentes peticiones de mi representada.

Es por ello que esta parte se ve en la necesidad de interponer la presente demanda.

Se aportan como documentos números [Nº DE DOCUMENTO] telegrama y burofax de fechas [FECHA] así como certificado de Correos de su recepción.

Se adjuntan asimismo como prueba copias de las comunicaciones enviadas y recibidas durante el proceso de negociación, incluidas cartas, correos electrónicos y/o actas de reuniones como documentos números [Nº DE DOCUMENTO].

[OPCIONAL — incluir si procede]

CUARTO.- Como consecuencia del incumplimiento de lo estipulado por parte de la vendedora, los daños sufridos por mi representada, son los que a continuación se relacionan [DESCRIPCIÓN DE LOS DAÑOS] (indicar, justificar y cuantificar económicamente tales gastos; por ejemplo gastos de espera, traslados de mercancía y almacenamiento en concepto de indemnización de daños y perjuicios)

A los anteriores Hechos, son aplicables los siguientes

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA

Los arts. 21 y 22 LOPJ y 36 LEC atribuyen con carácter general a la jurisdicción de nuestro Estado y al orden civil, el conocimiento de una materia como la presente.

Los arts. 85 LOPJ y 45 LEC, designan a los Tribunales de Instancia, como los órganos con la competencia específica objetiva y funcional para resolver estos pleitos.

Finalmente, el art. 50.1 LEC fija que la competencia territorial general, en el caso de personas físicas, corresponderá al tribunal del domicilio del demandado.

II.- TRAMITACIÓN

En aplicación de los arts. 248.3, 249.2 y 251.11.ª LEC, y en atención al valor de lo reclamado, se fija la cuantía en [IMPORTE] euros ( [IMPORTE] €), debiéndose tramitarse este pleito por las normas de proceso declarativo llamado Juicio Ordinario.

III.- LEGITIMACIÓN Y POSTULACIÓN

El art. 10 LEC legitima para comparecer y actuar en juicio a los titulares de la relación jurídica o del objeto litigioso. En el caso de autos, la ostenta el actor, en su calidad de vendedor, como parte perjudicada por el incumplimiento del comprador, sobre quien recae la legitimación pasiva para el ejercicio de esta acción.

En aplicación de los arts. 23 y 31 LEC, las partes comparecerán representadas por Procurador/a de los Tribunales y asistidas por Letrado en ejercicio, ambos habilitados ante el Tribunal.

IV.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

V.- FONDO DEL ASUNTO

De conformidad con lo dispuesto en los arts. 1.089 y 1.091 CCiv, las obligaciones nacen, entre otros supuestos, de los contratos, teniendo estos fuerza de ley entre las partes, es decir, los pactos de los contratos son vinculantes para ambas partes, debiendo cada una de ellas cumplir a lo que se obligó en los términos previstos en el propio contrato y mucho más en supuestos de contratos, como el de compraventa, que es por su propia naturaleza un contrato bilateral, silanagmático y oneroso, surgiendo obligaciones reciprocas comprador-vendedor de forma que, cada uno deberá cumplir las obligaciones que le son propias.

A tenor de los hechos expuestos, se ejercita aquí una acción para instar el cumplimiento del contrato suscrito por mi representada con el comprador para que éste proceda a la recepción de la cosa en los términos pactados, de conformidad con lo establecido en el art. 1124 CCiv.

Ciertamente el segundo párrafo de dicho precepto otorga al perjudicado por el incumplimiento de cualquier contrato bilateral la facultad de optar entre exigir el cumplimiento o la resolución de la obligación, con el resarcimiento de daños y abono de intereses en ambos casos, optando mi representada por la primera opción citada

VI.- COSTAS

En aplicación del art. 394.1 LEC deberán imponerse las costas a la parte demandada.

Por lo expuesto

SUPLICO AL TRIBUNAL,

que teniendo por presentado este escrito, documentos que acompañan y copias preceptivas, se sirva admitir todo ello, y, en su virtud, de conformidad con las manifestaciones que contiene, tenga por interpuesta en la representación ostento, demanda de juicio declarativo ordinario, en ejercicio de acción de cumplimiento de contrato, contra D./Dña. [NOMBRE Y APELLIDOS], y previos los trámites legales pertinentes, y previo recibimiento del juicio a prueba, dicte sentencia con los siguientes pronunciamientos:

1.- Se declare que D./Dña. [NOMBRE Y APELLIDOS] ha incurrido en mora tanto en la recepción de la cocina modelo [MARCA/MODELO], como en el pago de su precio.
2.- Se condene a D./Dña. [NOMBRE Y APELLIDOS] a recibir la cocina contratada descrita en el cuerpo de este escrito, por el precio pactado de [IMPORTE] euros, cantidad que restaba por pagar del precio de la mercancía encargada, así como (en su caso) al pago de la cantidad de [IMPORTE] euros, en concepto de indemnización de daños y perjuicios, conforme a lo indicado en el ordinal cuarto de los Hechos de la demanda.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
