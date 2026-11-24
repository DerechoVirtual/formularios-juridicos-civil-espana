---
name: contrato-arrendamiento-nave-industrial-facultad-civ-0519
description: "Contrato de arrendamiento de nave industrial con facultad de subarrendar. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de arrendamiento de nave industrial con facultad de subarrendar

> Formulario **CIV-0519** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de arrendamiento de nave industrial con facultad de subarrendar» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de arrendamiento de nave industrial con facultad de subarrendar” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:contrato-arrendamiento-nave-industrial-facultad-civ-0519`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (10 veces)
- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] AÑO (5 veces)
- [ ] DÍA (5 veces)
- [ ] MES (5 veces)
- [ ] Nº (5 veces)
- [ ] NÚMERO (4 veces)
- [ ] Nº DE PROTOCOLO (3 veces)
- [ ] CALLE (2 veces)
- [ ] DNI/NIE (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] DENOMINACIÓN SOCIAL
- [ ] ENTIDAD BANCARIA
- [ ] FINCA
- [ ] FOLIO
- [ ] LIBRO
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº DE CUENTA (IBAN)
- [ ] TOMO
- [ ] TÍTULO DE ADQUISICIÓN

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

En [LOCALIDAD], mi residencia, a [DÍA] de [MES] de [AÑO]

REUNIDOS

De una parte:

D/Dª [NOMBRE Y APELLIDOS] mayor de edad, vecino de [LOCALIDAD], con domicilio en C/ [CALLE], nº [NÚMERO] y portador de DNI [DNI/NIE].

De otra:

D/Dª [NOMBRE Y APELLIDOS], mayor de edad, vecino de [LOCALIDAD], con domicilio en Avda., nº [NÚMERO], y con DNI número [DNI/NIE].

INTERVIENEN

D/Dª [NOMBRE Y APELLIDOS] en nombre y representación de la mercatil [DENOMINACIÓN SOCIAL] en lo sucesivo "EL ARRENDADOR", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD], D. [NOMBRE Y APELLIDOS] en fecha [DÍA] de [MES] de [AÑO], con el número de protocolo [Nº DE PROTOCOLO].

D/Dª [NOMBRE Y APELLIDOS] en nombre y representación de [NOMBRE DEL REPRESENTADO/A] en lo sucesivo "EL ARRENDATARIO", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D. [NOMBRE Y APELLIDOS] en fecha [DÍA] de [MES] de [AÑO] con el número de protocolo [Nº DE PROTOCOLO].

Ambas partes, en el respectivo carácter con el que intervienen, se reconocen mutuamente la capacidad legal en Derecho necesaria y suficiente para concertar el presente CONTRATO DE ARRENDAMIENTO DE NAVE INDUSTRIAL, por lo que a tal efecto y de común acuerdo,

EXPONEN

PRIMERO.- Que el ARRENDADOR es propietario en régimen de plena propiedad y dominio del inmueble sito en [LOCALIDAD], calle [CALLE] número [NÚMERO], con una superficie de [Nº] metros cuadrados.

Título: Adquirido por [TÍTULO DE ADQUISICIÓN] efectuada en virtud de escritura pública otorgada ante el Notario de [LOCALIDAD], D. el día [DÍA] de [MES] de [AÑO] número protocolo [Nº DE PROTOCOLO].

Inscripción: Está inscrita en el Registro de la Propiedad número [NÚMERO] de [LOCALIDAD] en el tomo [TOMO] libro [LIBRO] folio [FOLIO] finca [FINCA].

Referencia catastral: según consta en la referencia del último recibo del Impuestos sobre bienes Inmuebles que queda unido a este documento por copia.

Cargas: La referida finca se encuentra libre de cargas y gravámenes, según nota simple expedida por el Registro de la Propiedad el día de hoy, y que se une a este documento

Arrendamientos: La referida finca no se encuentra arrendada y está libre de ocupantes e inquilinos.

SEGUNDO.- Como quiera que ambas partes se encuentran interesadas en la suscripción del presente contrato de arrendamiento de nave industrial, acuerdan que su relación contractual se sujete a las siguientes

CLÁUSULAS

Objeto

Constituye el objeto del presente contrato el arrendamiento de la nave industrial que ha sido descrita, para su utilización por el arrendatario dentro de las actividades que conforman su objeto social, pudiendo subarrendarlo a un tercero.

El ARRENDATARIO reconoce haber recibido la nave industrial, en el momento de la suscripción del presente contrato, en perfecto estado de conservación y al corriente de gastos e Impuestos.

El ARRENDATARIO se compromete a realizar los trámites que resulten necesarios para obtener la licencia que requiera la actividad que piensa desarrollar, asumiendo el coste que conlleve la citada obtención.

Se acompaña como Anexo I del presente contrato, un inventario donde se describen los bienes que se encuentran en la nave arrendada y que deberán devolverse a la finalización del contrato.

Renta

El importe de la renta asciende a [IMPORTE] Euros ( EUROS) mensuales, a la que habrá que añadir el porcentaje que en cada momento corresponda en concepto del Impuesto Sobre el Valor Añadido (IVA), siendo en este momento el tipo aplicable el 21%.

La renta habrá de satisfacerse por mensualidades anticipadas, y se efectuará en los cinco primeros días de cada mes en la cuenta bancaria de la [ENTIDAD BANCARIA], Sucursal de [LOCALIDAD], número de cuenta [Nº DE CUENTA (IBAN)].

La renta se actualizará por el arrendador y arrendatario en la fecha en que se cumpla un año de vigencia del contrato, aplicando a la renta correspondiente que se viniera pagando en el momento de la actualización, la variación porcentual experimentada por el Índice General Nacional del Sistema de Índice de Precios de Consumo fijado por el Instituto Nacional de Estadística, en el periodo de doce meses inmediatamente anterior a la fecha de cada actualización, tomando como mes de referencia para la primera actualización la que corresponde al último índice que estuviera publicado en la fecha de celebración del contrato, y en las sucesivas el que corresponda al último aplicado.

Se tomarán siempre como bases para cada actualización, la renta acumulada por las anteriores actualizaciones.

La actualización será notificada por la parte interesada a la otra parte por escrito, y ésta tendrá un plazo de 15 días para mostrar su disconformidad, si considerara que el cálculo se encuentra mal realizado.

Duración del arrendamiento

El plazo de duración del arrendamiento será de [Nº] años desde el [DÍA] de [MES] de [AÑO], fecha en la que la arrendadora se compromete a entregar la nave industrial a la arrendataria.

Transcurrido dicho plazo, y si las partes no anunciaran su decisión de no prorrogarlo, con un periodo de antelación de [Nº] meses al vencimiento del mismo, el contrato quedará prorrogado por el plazo de [Nº] años.

El retraso en la devolución del inmueble, una vez terminada la relación contractual, supondrá el pago de una indemnización al arrendador consistente en el doble de la renta pactada, hasta que se deje el mismo libre.

Uso y mantenimiento

El arrendatario utilizará la finca arrendada exclusivamente para el uso pactado.

El arrendatario sabe, conoce y admite las condiciones en las que se encuentra el inmueble en cuestión y lo recibe en perfecto estado de uso y habitabilidad, por lo que deberá mantenerlo a su costa en idéntica situación.

Gastos

Serán de cuenta del arrendatario todos los servicios y suministros con que cuenta la nave arrendada tales como energía eléctrica, gas, calefacción, agua fría y caliente, recogida de basuras, alcantarillado, residuales, depuradora, teléfono, etc.

El ARRENDATARIO deberá facilitar sus datos a las empresas suministradoras al objeto de contratar personalmente el suministro que requiera su actividad, así como al Consistorio, con respecto a los gastos de agua y alcantarillado.

El IBI será abonado por el ARRENDADOR.

Obras del arrendatario

El arrendatario no podrá realizar, sin el consentimiento previo del arrendador expresado por escrito, ningún tipo de obra, tanto las obras que modifiquen la configuración de la finca arrendada, o que provoquen una disminución de la estabilidad o seguridad del inmueble en concreto, como cualquier otra que tuviera intención de llevar a cabo.

Las obras realizadas por el arrendatario quedarán en beneficio de la finca y no darán derecho a indemnización para el arrendatario.

Responsabilidades y seguros

El arrendatario se hace directa y exclusivamente responsable de cuantos daños puedan ocasionarse a personas o cosas y sean consecuencia del negocio instalado, eximiendo de toda responsabilidad al arrendador, incluso por daños derivados de instalaciones para servicios y suministros.

Con el fin de que quede cubierta la responsabilidad antes citada, el arrendatario se obliga a contratar una póliza de seguro que cubra adecuadamente las responsabilidades antedichas.

Desistimiento del arrendatario

Si en cualquier momento y antes del vencimiento del presente contrato, el arrendatario desistiera voluntariamente del mismo, vendrá obligado a notificar su propósito por escrito al arrendador, con [Nº] meses de antelación a la rescisión unilateral del contrato, no pudiendo oponerse el arrendador en ningún caso, no teniendo derecho a reclamación alguna frente al arrendatario en el ejercicio de este derecho de resolución anticipada.

En el supuesto de que el ARRENDATARIO no cumpliera el citado plazo de preaviso, se verá obligado a abonar al ARRENDADOR las mensualidades que resten hasta la finalización del contrato, como clausula penal por su incumplimiento.

Subarrendamiento

El ARRENDADOR permite al ARRENDATARIO subarrendar la nave industrial objeto del presente contrato, siempre que el tercero que vaya a hacer uso del subarriendo, mantenga la misma actividad desarrollada por el ARRENDATARIO.

El ARRENDATARIO se obliga a notificar al ARRENDADOR, con un mes de antelación a la firma del contrato de subarrendamiento con tercero, su voluntad de subarrendar el inmueble, al objeto de determinar la renta que operará a partir del referido subarriendo, puesto que las partes acuerdan aumentar la renta que se encuentre vigente a la firma del subarriendo en un %, en favor del ARRENDADOR.

El ARRENDATARIO no podrá subarrendar la finca por un importe superior a la renta que abone al ARRENDADOR.

El subarrendamiento quedará extinguido, en todo caso, cuando finalice el contrato de arrendamiento, sea por el motivo que sea.

Fianza

La ARRENDATARIA hace entrega en el presente acto del importe de la fianza que se establece en [IMPORTE] euros, que la ARRENDADORA deberá devolver en el plazo máximo de un mes desde la resolución contractual, una vez comprobado el estado de las instalaciones, y si éstas se encontraran en perfectas condiciones, y el ARRENDATARIO hubiera cumplido todas sus obligaciones.

Sumisión

En el supuesto de que pudiera surgir cualquier tipo de cuestión o diferencia entre las partes en cuanto a la interpretación y aplicación del presente contrato, serán competentes para su conocimiento los Tribunales de [LOCALIDAD], por ser el lugar donde se encuentra la nave arrendada.

Fdo. D/Dª [NOMBRE Y APELLIDOS]

(El ARRENDADOR)

Fdo. Dª/D [NOMBRE Y APELLIDOS]

(El ARRENDATARIO)

========================================================================
