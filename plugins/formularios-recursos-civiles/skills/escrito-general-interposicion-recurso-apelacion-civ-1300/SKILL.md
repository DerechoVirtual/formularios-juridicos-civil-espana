---
name: escrito-general-interposicion-recurso-apelacion-civ-1300
description: "Escrito general de interposición del recurso de apelación. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito general de interposición del recurso de apelación

> Formulario **CIV-1300** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 24-11-2026.

## Qué es

Escrito por el que se interpone recurso de apelación con aportación de documentos o solicitud de pruebas Adaptado a la reforma del RDL 6/2023, aplicable a los procesos incoados desde el 20-3-2024.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito general de interposición del recurso de apelación» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito general de interposición del recurso de apelación” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:escrito-general-interposicion-recurso-apelacion-civ-1300`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (5 veces)
- [ ] MEDIO DE PRUEBA (4 veces)
- [ ] IMPORTE (3 veces)
- [ ] DESCRIBIR (2 veces)
- [ ] EXPONER LOS HECHOS (2 veces)
- [ ] LUGAR (2 veces)
- [ ] ACTO O RESOLUCIÓN
- [ ] CONTENIDO DE LA RESOLUCIÓN RECURRIDA
- [ ] FUNDAMENTOS
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] NOMBRE Y APELLIDOS
- [ ] NORMAS PROCESALES INFRINGIDAS
- [ ] Nº DE PROCEDIMIENTO
- [ ] ÓRGANO

## Normas que cita el formulario

- art. 458.1 LEC
- art. 448.1 LEC
- art. 276 LEC
- art. 449.1 LEC
- art. 449.3 LEC
- art. 449.4 LEC
- art. 460 LEC
- art. 464 LEC
- art. 460.1 LEC
- art. 270.1 LEC

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

- Junto a «…os incoados desde el 20-3-2024. A LA SECCION CIVIL DE LA AUDIENCIA PROVINCIAL DE»: La AP no tiene «Sección Civil» como denominación legal: se cita la Sección por su número. Fuente: LOPJ arts. 80 y 82 (Audiencia Provincial, sin cambio de denominación).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Escrito por el que se interpone recurso de apelación con aportación de documentos o solicitud de pruebas

Adaptado a la reforma del RDL 6/2023, aplicable a los procesos incoados desde el 20-3-2024.

Notas al pie del formulario original:
(1) No cabe apelación en sentencias dictadas en los juicios verbales por razón de la cuantía cuando ésta no supere los 3.000 euros.

(2) Cuando se pretenda alegar infracción de normas o garantías procesales en la primera instancia deberá expresarse: 1.º la norma infringida, 2.º la indefensión causada y 3.º la denuncia de la infracción formulada por medio del recurso u oportuna protesta.

========================================================================


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

A LA SECCION CIVIL DE LA AUDIENCIA PROVINCIAL DE

D/Doña [NOMBRE Y APELLIDOS], Procurador de los Tribunales, actuando en nombre de [NOMBRE DEL REPRESENTADO/A], cuya representación tengo acreditada en los autos de juicio [Nº DE PROCEDIMIENTO], seguido contra [ACTO O RESOLUCIÓN], ante la Sala comparezco y como mejor proceda en derecho DIGO:

Que el pasado día [FECHA] se me ha notificado la resolución de fecha [FECHA], recaída en las presentes actuaciones, por la que se acuerda [CONTENIDO DE LA RESOLUCIÓN RECURRIDA], y estimando la misma gravosa para los intereses de mi mandante, dicho sea en términos de defensa, dentro del plazo de veinte días legalmente establecido en el art. 458.1 LEC, INTERPONGO RECURSO DE APELACIÓN contra dicha resolución.

Que, conforme a lo estipulado en el apartado 2 del citado art. 458, impugno concretamente el pronunciamiento relativo a [DESCRIBIR], estando conforme con los demás pronunciamientos de la resolución recurrida, lo que hago por medio del presente escrito en el que expongo los siguientes:

REQUISITOS PROCESALES

I.- Se presenta este escrito de interposición ante ese Tribunal, que es el competente para conocer del recurso, con arreglo al art. 458.1 LEC.

II.- Se presenta este escrito de interposición dentro del plazo de veinte días contados desde el día siguiente a la notificación de la resolución impugnada (art. 458.1 y 3 LEC).

III.- Esta parte se halla legitimada por afectarle desfavorablemente la resolución impugnada, conforme exige el art. 448.1 LEC.

IV.- Las exigencias de postulación se llenan para este escrito de interposición, ya que está comparecida esta parte mediante Procurador de los Tribunales, y asistida de abogado en ejercicio, ambos colegiados y habilitados para ejercer ante el Tribunal (arts. 23.1 y 31.1 LEC).

FUNDAMENTOS DEL RECURSO

PRIMERO

En primer lugar y tal como denuncié en su momento, se han infringido las normas y garantías procesales siguientes [NORMAS PROCESALES INFRINGIDAS]

Como consecuencia de las mencionadas infracciones se ha sufrido indefensión consistente en [DESCRIBIR], ya que [EXPONER LOS HECHOS]

Tales circunstancias fueron denunciadas mediante [ÓRGANO]

SEGUNDO

Por otro lado, la resolución recurrida no ha tenido en cuenta que, según la prueba practicada en las actuaciones, [EXPONER LOS HECHOS]

TERCERO

A todo ello se suma la incorrecta aplicación de las normas de derecho sustantivo puesto que [FUNDAMENTOS]

Por lo expuesto,

SUPLICO A LA AUDIENCIA PROVINCIAL

Que, teniendo por presentado este escrito con su copia, y documento/s acompañado/s, de lo que se ha dado traslado al Procurador de la parte contraria en la forma que previene el art. 276 LEC, se sirva tener por INTERPUESTO RECURSO DE APELACIÓN contra la resolución de fecha [FECHA], y

SUPLICO AL TRIBUNAL

Que, seguido que sea el legal procedimiento, dicte sentencia que revoque la de instancia, y resolviendo sobre la cuestión que es objeto de proceso, desestime en su integridad la demanda, absolviendo de sus pedimentos a mi mandante.

Es de Justicia que pido en [LUGAR], a [FECHA].

OTROSÍ PRIMERO DIGO

Que se acompaña a este escrito resguardo acreditativo del pago del depósito de 50 euros en la Cuenta de Depósitos y Consignaciones del Tribunal al que se dirige, conforme exige la disposición adicional 15.ª LOPJ, por lo que,

SUPLICO AL TRIBUNAL

Que tenga por causada la manifestación anterior a los efectos oportunos.

[OPCIONAL — incluir si procede]

OTROSÍ SEGUNDO DIGO: Que de acuerdo con lo prescrito en el artículo 449.1 LEC, al encontrarnos ante un proceso que lleva aparejado el lanzamiento, se acredita mediante la aportación del correspondiente resguardo de ingreso en la Cuenta de Depósitos y Consignaciones judiciales, tener satisfechas las rentas vencidas y las que con arreglo al contrato deben pagarse por adelantado.

SUPLICO AL TRIBUNAL que tenga por hecha la anterior manifestación a los oportunos efectos.

[OPCIONAL — incluir si procede]

OTROSÍ SEGUNDO DIGO: Que de acuerdo con lo prescrito en el artículo 449.3 LEC, al encontrarnos ante un proceso en que se pretende la condena a indemnizar daños y perjuicios derivados de la circulación de vehículos de motor, se acredita mediante la aportación del correspondiente resguardo de ingreso en la Cuenta de Depósitos y Consignaciones judiciales, haber constituido depósito del importe de la condena, que asciende a la suma de [IMPORTE] euros, más los intereses y recargos exigibles, que se calculan en [IMPORTE] euros.

SUPLICO AL TRIBUNAL que tenga por hecha la anterior manifestación a los oportunos efectos.

[OPCIONAL — incluir si procede]

OTROSÍ SEGUNDO DIGO: Que de acuerdo con lo prescrito en el artículo 449.4 LEC, al encontrarnos ante un proceso en que se pretende la condena al pago de las cantidades debidas por un propietario a la comunidad de vecinos, se acredita mediante la aportación del correspondiente resguardo de ingreso en la Cuenta de Depósitos y Consignaciones judiciales, haber consignado la cantidad líquida de [IMPORTE] euros a que se contrae la sentencia condenatoria.

SUPLICO AL TRIBUNAL que tenga por hecha la anterior manifestación a los oportunos efectos.

[OPCIONAL — incluir si procede]

OTROSÍ TERCERO DIGO que conforme a lo regulado en el art. 460 LEC, se interesa la práctica en segunda instancia de las siguientes PRUEBAS:

- [MEDIO DE PRUEBA], que fue propuesta y admitida en la primera instancia pero, por causa no imputable a mi representación, no pudo practicarse ni siquiera como diligencia final.
- [MEDIO DE PRUEBA], que fue indebidamente denegada en la primera instancia, habiéndose formulado la oportuna protesta en la vista.
- [MEDIO DE PRUEBA], ya que se refiere a hechos de relevancia para la decisión del pleito ocurridos después del comienzo del plazo para dictar sentencia en la primera instancia.
- [MEDIO DE PRUEBA], puesto que se refiere a hechos de relevancia para la decisión del pleito ocurridos antes del plazo para dictar sentencia, y de los que esta parte ha tenido conocimiento con posterioridad, como ha quedado justificado en las alegaciones formuladas en este escrito.

En virtud de lo expuesto, A LA SALA SUPLICO que se tenga por solicitada la práctica de las pruebas señaladas en la segunda instancia.

[OPCIONAL — incluir si procede]

OTROSÍ CUARTO DIGO que de conformidad con lo dispuesto en el art. 464 LEC solicito que se acuerde la celebración de vista pública.

SUPLICO A LA AUDIENCIA PROVINCIAL que teniendo por causada la manifestación anterior a los efectos oportunos, se sirva acordar de conformidad, como es procedente en Justicia que reitero.

[OPCIONAL — incluir si procede]

OTROSÍ QUINTO DIGO: Que esta parte acompaña al presente escrito, al amparo de lo dispuesto en el art. 460.1 LEC, los siguientes documentos que no pudieron aportarse en la primera instancia, por encontrarse en los supuestos del art. 270.1 LEC:

Por ello nuevamente,

SUPLICO AL TRIBUNAL

Tenga por hecha la anterior manifestación a los oportunos efectos, y se admitan los documentos aportados, por lo que reitero nuevamente justicia en el lugar y fecha antes indicado.

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a
