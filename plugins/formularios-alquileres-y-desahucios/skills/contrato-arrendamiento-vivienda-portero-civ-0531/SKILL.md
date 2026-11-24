---
name: contrato-arrendamiento-vivienda-portero-civ-0531
description: "Contrato de arrendamiento de la vivienda del portero. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de arrendamiento de la vivienda del portero

> Formulario **CIV-0531** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Contrato por el que una comunidad de propietarios arrienda, como vivienda, un elemento común del edificio que antes era la vivienda del portero y hoy está en desuso. Se rige por la Ley de Arrendamientos Urbanos (arrendamiento de vivienda) y se usa cuando la comunidad decide rentabilizar esa vivienda.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de arrendamiento de la vivienda del portero» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de arrendamiento de la vivienda del portero” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:contrato-arrendamiento-vivienda-portero-civ-0531`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (6 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] AÑO (4 veces)
- [ ] DÍA (4 veces)
- [ ] MES (4 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] DENOMINACIÓN O DOMICILIO DE LA COMUNIDAD (2 veces)
- [ ] DNI/NIE (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] FECHA (2 veces)
- [ ] IMPORTE EN LETRA (2 veces)
- [ ] Nº (2 veces)
- [ ] Nº DE FOLIO (2 veces)
- [ ] ENTIDAD BANCARIA
- [ ] FOLIO
- [ ] INSTITUCIÓN ARBITRAL O ÁRBITRO
- [ ] LETRA
- [ ] LIBRO
- [ ] NIF
- [ ] NOMBRE Y APELLIDOS DEL ARRENDATARIO
- [ ] Nº DE FINCA
- [ ] PLANTA
- [ ] TOMO

## Normas que cita el formulario

- No cita artículos concretos; Claude localizará las normas aplicables con Jurisprudenciator si el documento las necesita.

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

- Junto a «…ebración del contrato, y en las sucesivas el que corresponda al último aplicado.»: comprobar el índice de referencia y el límite a la actualización de la renta de vivienda vigentes en la fecha de firma (art. 18 LAU, en su redacción actual).
- Junto a «… vivienda se establece en la Ley de Arrendamientos Urbanos y en el Código Civil.»: el original remitía, por error evidente, a lo previsto para el arrendamiento de «uso distinto del de vivienda»; se ha corregido al tratarse de un arrendamiento de vivienda sujeto al art. 9 LAU.

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

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO]

INTERVIENEN

De una parte, D./Dña. [NOMBRE Y APELLIDOS], con DNI/NIE [DNI/NIE], en nombre y representación de la Comunidad de Propietarios del edificio sito en la calle [DOMICILIO], nº [Nº], de la localidad de [LOCALIDAD], con NIF [NIF], de la cual es Presidente/a, nombrado/a en la Junta de Propietarios de fecha [FECHA], según consta en el folio nº [Nº DE FOLIO] del libro de actas de la Comunidad.

De otra parte, D./Dña. [NOMBRE Y APELLIDOS], con DNI/NIE [DNI/NIE], y domicilio en [DOMICILIO], en su propio nombre y derecho.

Ambas partes, en el respectivo carácter con el que intervienen, se reconocen mutuamente la capacidad legal en Derecho necesaria para concertar el presente CONTRATO DE ARRENDAMIENTO DE VIVIENDA DE PORTERÍA y, a tal efecto, libremente y de común acuerdo,

EXPONEN

I.- Que la Comunidad de Propietarios [DENOMINACIÓN O DOMICILIO DE LA COMUNIDAD], en su reunión de fecha [FECHA], según consta en el folio nº [Nº DE FOLIO] del libro de actas de la comunidad, acordó arrendar la vivienda sita en la planta [PLANTA] letra [LETRA], inscrita en el Registro de la Propiedad número [Nº] de [LOCALIDAD], al Tomo [TOMO], Libro [LIBRO], Folio [FOLIO] y con número de finca [Nº DE FINCA]. Se trata de un elemento común del edificio, actualmente en desuso y que antiguamente era la vivienda destinada a portería.

II.- Que D./Dña. [NOMBRE Y APELLIDOS DEL ARRENDATARIO] manifiesta su intención de celebrar contrato de arrendamiento sobre la vivienda descrita en el expositivo anterior, por cuya razón pacta con la Comunidad de Propietarios [DENOMINACIÓN O DOMICILIO DE LA COMUNIDAD], de [LOCALIDAD], el presente CONTRATO DE ARRENDAMIENTO en base a las siguientes

CLÁUSULAS

PRIMERA.– Destino del arrendamiento.

El arrendatario usará el piso arrendado única y exclusivamente para vivienda y no podrá subarrendar, ceder o traspasar, total o parcialmente, la vivienda objeto de este arrendamiento.

El arrendatario renuncia expresamente a los derechos de tanteo y retracto, en caso de aportación o cualquier tipo de transmisión de la vivienda arrendada a terceros.

SEGUNDA.– Duración del contrato.

De conformidad con lo dispuesto en la Ley 29/1994, de 24 de noviembre, de Arrendamientos Urbanos, y en concreto en su artículo 9, la duración del contrato será de un año, prorrogable anualmente hasta una duración máxima de cinco años, o de siete años si el arrendador fuese persona jurídica, a contar desde el [DÍA] de [MES] de [AÑO], salvo que el arrendatario manifieste su voluntad de no renovarlo con treinta días de antelación como mínimo a la fecha de terminación del contrato o de cualquiera de las prórrogas.

Se acuerda por ambas partes que el arrendatario podrá desistir libremente del presente contrato y darlo por finalizado siempre que avise con sesenta días de antelación al arrendador, sin penalización alguna.

Llegado el [DÍA] de [MES] de [AÑO], cumplidos cinco años desde el inicio de vigencia del presente contrato, o siete años si el arrendador fuese persona jurídica, no existirá posibilidad de prórroga y, sin necesidad de denuncia por parte del arrendador, el presente contrato quedará automáticamente resuelto, quedando obligado el arrendatario a desalojar la vivienda y sometido, en el caso de que no lo hiciera, a la obligación de indemnizar al arrendador con [IMPORTE] euros (cantidad que se acuerde) por cada uno de los días que dure la ilegítima ocupación.

TERCERA.– Renta.

La renta inicial será de [IMPORTE] euros mensuales, pagaderos por meses adelantados en los cinco primeros días de cada mes.

La forma de pago será mediante transferencia bancaria en la cuenta corriente que la Comunidad de Propietarios designe a tal efecto.

La renta se actualizará en la fecha en que se cumpla cada año de vigencia del contrato, aplicando a la renta correspondiente a la anualidad anterior la variación porcentual experimentada por el Índice General Nacional del Sistema de Índices de Precios de Consumo en un período de doce meses inmediatamente anteriores a la fecha de cada actualización, tomando como mes de referencia para la primera actualización el que corresponda al último índice que estuviera publicado en la fecha de celebración del contrato, y en las sucesivas el que corresponda al último aplicado.

CUARTA.– Estado de la vivienda.

El arrendatario declara recibir la vivienda objeto de arriendo y los diversos muebles, objetos y enseres en ella existentes en perfecto estado, y en las mismas condiciones debe entregarlos a la propiedad al término del arriendo, siendo de cuenta y cargo del arrendatario todas las reparaciones que hayan de realizarse por daños causados, así como las reposiciones de cuantas pérdidas o deterioros le sean imputables.

Se anexa al presente contrato inventario de muebles y enseres.

QUINTA.– Gastos de servicios individuales.

Los servicios y suministros de electricidad, agua, gas y aquellos otros de que pudiera estar dotado el inmueble serán de cuenta y cargo del arrendatario y no quedan incluidos en el importe de la renta.

Si el arrendatario quisiera darse de alta en otros servicios, tales como televisión digital, teléfono, internet o cualquier otro, serán asimismo de su cuenta los gastos de alta en tales servicios y los consumos que realizara.

SEXTA.– Fianza.

El arrendatario deposita la cantidad de [IMPORTE EN LETRA] ([IMPORTE] €), en concepto de fianza, que servirá como anticipo de servicios como electricidad, gas, agua, etc., y/o para responder de daños causados a la vivienda, y que le será devuelta al término del contrato, previas las deducciones que procedan por incumplimiento de lo estipulado en este contrato.

Sirve el presente contrato como eficaz carta de pago y consignación de la cuantía de [IMPORTE] € correspondiente a la fianza.

SÉPTIMA.– Aval bancario.

[OPCIONAL — incluir si procede]

Igualmente entrega aval bancario por importe de [IMPORTE EN LETRA] euros ([IMPORTE] euros) a fin de responder del pago de los alquileres mensuales durante la vigencia del contrato, siendo los gastos de constitución y mantenimiento del aval por cuenta del arrendatario. El aval será renovado cada 12 meses, contando desde el día [DÍA] de [MES] de [AÑO], entregando el correspondiente documento bancario en donde conste el siguiente período, siendo causa suficiente para resolver el contrato la falta de presentación del aval.

El arrendatario entrega en este acto aval bancario de la entidad [ENTIDAD BANCARIA] por importe de [IMPORTE] euros.

OCTAVA.– Obras.

I.- El arrendatario acepta la vivienda arrendada en el estado que mantiene en el momento de celebrarse este contrato, renunciando a formular reclamación alguna al arrendador.

II.- El arrendatario no podrá realizar obra alguna de las que modifiquen la configuración de la vivienda o debiliten la naturaleza y resistencia de los materiales empleados en la construcción, sin autorización escrita del arrendador, bajo pena de resolución contractual.

III.- Será de cuenta del arrendatario, sin posibilidad de repercusión al arrendador, las reparaciones necesarias a fin de conservar la vivienda arrendada en estado de servir al uso convenido, así como las responsabilidades derivadas del incumplimiento de esta obligación.

IV.- Las obras autorizadas quedarán en beneficio de la finca, sin derecho alguno de reintegro a favor del arrendatario; respecto de las obras no autorizadas, y sin perjuicio de la facultad de resolución de la relación arrendaticia, la propiedad podrá optar entre exigir la demolición de lo ilegalmente realizado, reteniendo, en cuanto cubra, el importe de la fianza, o aceptar el nuevo estado de la vivienda arrendada, sin obligación alguna de reintegro en favor del arrendatario.

NOVENA.– Resolución del contrato.

El arrendador podrá resolver la relación arrendaticia, además de por las causas legalmente establecidas, por las siguientes:

a) El cambio de destino de la vivienda arrendada.

b) La realización de actividades comerciales, industriales y/o empresariales en la vivienda arrendada, o de cualquier actividad que pudiera estar sujeta a contribución.

c) La realización de obras sin contar con el consentimiento escrito de la propiedad.

d) La comisión de cualquier delito o falta en el interior de la vivienda arrendada.

e) La realización de actividades no permitidas en los Estatutos de la finca, dañosas para la misma, moralmente peligrosas, incómodas o insalubres.

DÉCIMA.– Sometimiento a tribunales o a arbitraje.

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— Sumisión a tribunales con renuncia al fuero propio: Para cualquier cuestión derivada de la interpretación o aplicación de lo aquí dispuesto, las partes se someten expresamente a la jurisdicción de los Tribunales de [LOCALIDAD], con renuncia a cualquier otro fuero que, en su caso, pudiera corresponderles.

— Sin renuncia al fuero propio: Para cualquier cuestión relacionada con la interpretación y el cumplimiento del presente contrato, ambas partes acuerdan someterse expresamente a los Tribunales competentes en virtud de la Ley de Enjuiciamiento Civil vigente.

— Sumisión a arbitraje: Para dirimir cualquier controversia o reclamación derivada del cumplimiento y aplicación de este contrato, las partes se someten, con renuncia a su fuero propio si fuera otro, al arbitraje de [INSTITUCIÓN ARBITRAL O ÁRBITRO].

UNDÉCIMA.– Normativa aplicable.

En todo lo no expresamente previsto en este contrato será de aplicación cuanto sobre el arrendamiento de vivienda se establece en la Ley de Arrendamientos Urbanos y en el Código Civil.

Y en prueba de conformidad con cuanto antecede, firman ambas partes el presente documento, por duplicado ejemplar y a un solo efecto, en el lugar y fecha indicados en el encabezamiento.

Fdo.: [NOMBRE Y APELLIDOS], EL ARRENDADOR (Presidente/a de la Comunidad de Propietarios)

Fdo.: [NOMBRE Y APELLIDOS], EL ARRENDATARIO
