---
name: apelacion-contra-auto-estima-declinatoria-sumision-civ-1304
description: "Apelación contra el auto que estima la declinatoria por sumisión a arbitraje. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Apelación contra el auto que estima la declinatoria por sumisión a arbitraje

> Formulario **CIV-1304** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **recursos**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Apelación contra el auto que estima la declinatoria por sumisión a arbitraje» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Apelación contra el auto que estima la declinatoria por sumisión a arbitraje” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:apelacion-contra-auto-estima-declinatoria-sumision-civ-1304`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] AÑO
- [ ] DOMICILIO
- [ ] DÍA
- [ ] LUGAR
- [ ] MES
- [ ] NOMBRE Y APELLIDOS DEL ABOGADO
- [ ] Nº DE CLÁUSULA

## Normas que cita el formulario

- art. 66 LEC

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

Proceso número [NÚMERO]

A LA AUDIENCIA PROVINCIAL DE [LOCALIDAD]

D. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en nombre y representación de D. [NOMBRE Y APELLIDOS], parte demandante en este proceso seguido con el número [NÚMERO], según tengo acreditado en autos, ante el Tribunal comparezco y como mejor proceda en derecho DIGO:

Que en fecha [FECHA] se me ha notificado el auto de fecha [FECHA] que declara la falta de jurisdicción del órgano al que me dirijo para conocer del presente proceso por haberse sometido a arbitraje y, no encontrándolo ajustado a derecho, dicho sea con los debidos respetos y en términos de defensa, por medio del presente escrito, y de conformidad a lo dispuesto en el art. 66 y 458 de la LEC, interpongo contra el mismo RECURSO DE APELACIÓN para ante la Audiencia Provincial de [LOCALIDAD], impugnando el pronunciamiento declarativo de la falta de jurisdicción, alegando los siguientes MOTIVOS:

PRIMERO.- Infracción por inaplicación de los artículos 83 y 90 de la Ley General de Defensa de Consumidores y Usuarios.

El auto apelado estima la declinatoria de jurisdicción aplicando una cláusula nula de pleno derecho en tanto que se trata de una cláusula abusiva por cuanto que implica obligar al consumidor a someterse a un arbitraje con la entidad [DENOMINACIÓN SOCIAL], lo cual es definido como una cláusula abusiva en el artículo 90.1 de la LGDCU.

El citado artículo 90.1 regula las cláusulas abusivas sobre competencia y derecho aplicable, disponiendo que es cláusula abusiva aquella que establezca "la sumisión de arbitrajes distintos del arbitraje de consumo, salvo que se trate de órganos de arbitraje institucionales", prescribiendo el artículo 83 la nulidad de pleno derecho de dichas cláusulas abusivas.

Pues bien, en el contrato aportado por esta parte en cuya clàusula [Nº DE CLÁUSULA] se recoge el convenio arbitral se pacta la sumisión a arbitraje en la entidad [DENOMINACIÓN SOCIAL], sin ninguna referencia al arbitraje de consumo, no siendo controvertida la condición de consumidor de mi representado, cuya única relación comercial con la entidad demandada es el crédito concertado para hacer frente a las obras de su vivienda, según consta expresamente en el contrato, por lo que actuó como consumidor de un producto financiero en la contratación con la entidad demandada.

SEGUNDO.- Infracción del artículo 9.2 de la Ley de Arbitraje.

El auto recurrido infringe el artículo 9.2 de la Ley de Arbitraje, el cual se remite a la legislación aplicable a los contratos de adhesión, que en este caso se encuentra recogida en los citados artículos 83 y 90 de la LGDCU y en la Ley de Condiciones Generales de la Contratación.

Como hemos alegado en los anteriores escritos, el contrato en cuestión es un contrato de adhesión elaborado unilateralmente por la entidad bancaria demandada, el cual está sujeto a las prescripciones de la Ley 7/1998, sobre condiciones generales de la contratación, puesto que está todo él prerredactado por la entidad de crédito aquí demandada, incluso el denominado "convenio arbitral" sin que contenga el mismo inciso alguno específico del caso, concertándose con una persona que tiene la condición de consumidor, como es mi mandante, por lo que la cláusula es nula según dispone el artículo 9.2 de la Ley de Arbitraje, que se remite a las normas reguladoras de este tipo de contratos, en este caso, la Ley General de Consumidores y Usuarios, y la Ley de Condiciones Generales de la Contratación, de cuya regulación se deduce indiscutiblemente la nulidad de la cláusula en cuestión.

La cláusula de arbitraje en que se funda la declinatoria de jurisdicción entraña sin duda una restricción de las facultades procesales de mi representado, principalmente porque le priva del acceso a la tutela de los órganos jurisdiccionales estatales y subsidiariamente porque el arbitraje debería desarrollarse en [LOCALIDAD], estando él domiciliado en [DOMICILIO], distante centenares de kilómetros de dicha ciudad, como es notorio, siendo que la entidad demandada, con sucursales en todo el territorio nacional, tiene el centro de negocios en dicha localidad.

En consecuencia, siendo nulo de pleno derecho el convenio arbitral, procede declarar la jurisdicción de los tribunales ordinarios, por lo que solicitamos que se revoque el auto apelado y se acuerde la continuación del proceso.

En base a lo anterior,

SUPLICO A LA SALA que tenga por presentado este escrito, teniendo por interpuesto el recurso de apelación frente al auto dictado en las presentes actuaciones de fecha [FECHA] y tras la pertinente tramitación, se dicte auto declarando la jurisdicción de los tribunales ordinarios y acordando la continuación del proceso.

OTROSÍ DIGO que, de conformidad con lo dispuesto en los apartados 3 y 6 de la disposición adicional decimoquinta de la LOPJ acompaño a este escrito resguardo de consignación en la cuenta de Depósitos y Consignaciones abierta a nombre del Tribunal del depósito exigido para interponer el recurso por importe de 50 euros.

Por lo que,

SUPLICO AL TRIBUNAL que tenga por constituido el depósito, dejando interesada desde este momento su devolución para el caso de estimación total o parcial del recurso.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma Abogado [NOMBRE Y APELLIDOS DEL ABOGADO] Firma Procurador

========================================================================
