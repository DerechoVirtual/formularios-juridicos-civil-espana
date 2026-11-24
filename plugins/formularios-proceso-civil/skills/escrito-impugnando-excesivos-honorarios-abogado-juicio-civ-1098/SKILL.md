---
name: escrito-impugnando-excesivos-honorarios-abogado-juicio-civ-1098
description: "Escrito impugnando por excesivos los honorarios de abogado en un juicio de desahucio. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito impugnando por excesivos los honorarios de abogado en un juicio de desahucio

> Formulario **CIV-1098** del plugin **Proceso civil: demandas, contestaciones, prueba y vista** (`formularios-proceso-civil`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 24-11-2026.

## Qué es

Escrito impugnando los honorarios reclamados por abogado, por excesivos, de conformidad con el art. 245 LEC.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito impugnando por excesivos los honorarios de abogado en un juicio de desahucio» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito impugnando por excesivos los honorarios de abogado en un juicio de desahucio” para mi caso». También puedes invocarla directamente con `/formularios-proceso-civil:escrito-impugnando-excesivos-honorarios-abogado-juicio-civ-1098`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-proceso-civil:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso civil: demandas, contestaciones, prueba y vista) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] NÚMERO (4 veces)
- [ ] AÑO (2 veces)
- [ ] FECHA (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] IMPORTE EN CIFRA (2 veces)
- [ ] ACTO O RESOLUCIÓN
- [ ] CALLE
- [ ] COLEGIO
- [ ] IMPORTE EN LETRA
- [ ] LUGAR
- [ ] SEDE

## Normas que cita el formulario

- art. 245 LEC
- art. 253.1 LEC
- art. 251.9.ª LEC

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

D./Dña. [NOMBRE Y APELLIDOS], demandante en autos de Juicio Verbal n.º [NÚMERO]/[AÑO], asistida de la Letrada en ejercicio D./Dña. [NOMBRE Y APELLIDOS], colegiada n.º [NÚMERO], con despacho abierto en calle [CALLE], n.º [NÚMERO], en la Pieza Separada de Honorarios de Abogado comparezco y como mejor en Derecho proceda, DIGO:

Que con fecha [FECHA] se ha notificado y requerido a mi patrocinada de pago, dándosele vista de la minuta del Letrado D./Dña. [NOMBRE Y APELLIDOS], que me dirigió en el juicio de desahucio seguido contra [ACTO O RESOLUCIÓN], y dentro del plazo conferido, vengo a impugnar los honorarios reclamados por excesivos, de conformidad con el art. 245 LEC, por lo que se mencionan las partidas concretas de discrepancia:

PRIMERO

En la minuta en cuestión se fija que la dirección técnica, con redacción de la demanda y alegaciones, proposición y práctica de prueba, y emisión de conclusiones en el acto de la vista, hasta sentencia definitiva en el Juicio Verbal n.º [NÚMERO]/[AÑO], importa la cantidad de [IMPORTE] euros ([IMPORTE EN CIFRA] €), sirviendo de base para el cálculo, según la minuta, el precio del inmueble arrendado, de [IMPORTE] euros.

SEGUNDO

Ciertamente la demanda consignó tal cuantía, cumpliendo el mandato del art. 253.1 LEC, aportándose certificado de A.P.I. como documento anexo, y sin que se discutiera en el proceso.

Ello porque el art. 251.9.ª LEC, hasta la reforma de la Ley 19/2009, de 23 de noviembre, de medidas de fomento y agilización procesal del alquiler y de la eficiencia energética de los edificios, disponía para la demanda de juicio sobre arrendamiento de bienes, cuando se reclamaba la posesión del bien arrendado, el reenvío a la regla 3.ª, que debía entenderse a su punto 5.º, porque no había otra regla específica y se reclamaba la recuperación posesoria, con lo que venía a resultar de aplicación el cálculo de la regla 2.ª, en que hay que estar al valor de los bienes al tiempo de interponer la demanda, conforme a los precios corrientes en el mercado.

TERCERO

Por aplicación de la Norma 137 de las orientativas de honorarios del Iltre. Colegio de Abogados de [COLEGIO], se devengan, en caso de oposición de adverso, como es el presente, los honorarios de las normas del declarativo que por cuantía corresponda, siendo la base minutable la de la Norma 138, que es el importe de la renta anual multiplicado por el tiempo de duración del contrato, con un mínimo de una anualidad y un máximo de diez.

CUARTO

Las Normas de juicios declarativos estipulan en dichas orientaciones una escala gradual-tipo en la Disposición General 20.ª. La renta probada de la finca arrendada asciende a los 1.052 euros mensuales, por lo que el máximo de diez anualidades para servir de base a la minuta, según las normas orientativas, es de 1.126.240, y el mínimo de una anualidad de 112.624 euros.

QUINTO

Conforme a la minuta que se me trasladó la cantidad reclamada por honorarios asciende a 20.205 euros, que cualquiera que sea el creciente valor de los inmuebles urbanos, resulta a todas luces exagerada, dado que las orientaciones colegiales arrojan un devengo de honorarios de 1.530 euros, sobre la base de la renta de un año, y a falta de ninguna especialidad demostrable, y no revistiendo el juicio de una dificultad de hecho (se trataba de una interpretación del Derecho Transitorio de la LAU 1994), se postula la reducción de los honorarios a dicha cantidad.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito, se digne admitirlo, teniendo por impugnados por excesivos los honorarios de la minuta del Abogado D./Dña. [NOMBRE Y APELLIDOS], seguido que sea el trámite oportuno, se dicte Decreto por el que se determine que, con estimación de esta oposición, la cantidad de la minuta que debe pagarse es de [IMPORTE EN LETRA] ([IMPORTE EN CIFRA] €), con imposición expresa de las costas al promotor del procedimiento.

Es justicia de hacerse en [LUGAR], a [FECHA].

Firma del Abogado	Firma del Procurador/a

========================================================================
