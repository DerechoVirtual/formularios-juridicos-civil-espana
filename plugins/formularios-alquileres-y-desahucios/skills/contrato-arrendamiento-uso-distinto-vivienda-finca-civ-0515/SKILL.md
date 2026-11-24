---
name: contrato-arrendamiento-uso-distinto-vivienda-finca-civ-0515
description: "Contrato de arrendamiento para uso distinto de vivienda de una finca destinada a actividad docente. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de arrendamiento para uso distinto de vivienda de una finca destinada a actividad docente

> Formulario **CIV-0515** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de arrendamiento para uso distinto de vivienda de una finca destinada a actividad docente» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de arrendamiento para uso distinto de vivienda de una finca destinada a actividad docente” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:contrato-arrendamiento-uso-distinto-vivienda-finca-civ-0515`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (9 veces)
- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] Nº (5 veces)
- [ ] IMPORTE (3 veces)
- [ ] CALLE (2 veces)
- [ ] NIF (2 veces)
- [ ] PISO (2 veces)
- [ ] PUERTA (2 veces)
- [ ] ÓRGANO (2 veces)
- [ ] ACTIVIDAD
- [ ] AÑO
- [ ] DATOS REGISTRALES
- [ ] DÍA
- [ ] FOLIO
- [ ] FORMA DE PAGO
- [ ] INSTITUCIÓN DE MEDIACIÓN
- [ ] MES
- [ ] OTROS DATOS
- [ ] PROVINCIA
- [ ] TOMO

## Normas que cita el formulario

- art. 36 LAU
- art. 32 LAU

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

En la localidad/ciudad de [LOCALIDAD], a [DÍA] de [MES] de [AÑO]

REUNIDOS

De una parte, D [NOMBRE Y APELLIDOS], mayor de edad, con domicilio en [LOCALIDAD] y titular del NIF [NIF], en calidad de ARRENDADOR;

Y de otra, D [NOMBRE Y APELLIDOS], mayor de edad, con domicilio en [LOCALIDAD] y titular del NIF [NIF], en calidad de ARRENDATARIA;

MANIFIESTAN

Que reconociéndose mutuamente las partes, según intervienen, la capacidad legal necesaria a los efectos de este CONTRATO DE ARRENDAMIENTO DE FINCA PARA ACTIVIDAD DOCENTE, interviniendo en nombre y derecho propio, siendo responsables de la veracidad de sus manifestaciones, y de forma libre, espontánea y de mutuo acuerdo

EXPONEN

I. Que [NOMBRE Y APELLIDOS] es dueño en pleno dominio, por el título que se dirá, del inmueble sito en [LOCALIDAD] cuya descripción registral es la siguiente: [DATOS REGISTRALES]. El local se encuentra inscrito en el Registro de la Propiedad núm. [Nº] de [LOCALIDAD], siendo la finca registral núm. [Nº], inscrita al tomo [TOMO], folio [FOLIO], inscripción

Al Local le corresponde una cuota de contribución a los gastos de comunidad del edificio en el que se ubica del %.

II. Que estando interesados D. [NOMBRE Y APELLIDOS] como parte arrendadora, y D. [NOMBRE Y APELLIDOS]. Como parte arrendataria en formalizar el arrendamiento de la finca indicada, es por lo que celebran el presente CONTRATO DE ARRENDAMIENTO DE FINCA PARA ACTIVIDAD DOCENTE de acuerdo con las siguientes

CLÁUSULAS

Objeto y destino

El Arrendador, por medio de este Contrato arrienda el inmueble descrito en el Expositivo I, al Arrendatario, que declara conocer dicho local y lo encuentra apto para el fin a que va a destinarlo. El inmueble se destinará por el Arrendatario a [ACTIVIDAD], quedando expresamente prohibido el cambio de destino sin contar con el previo consentimiento, por escrito, del Arrendador.

El Arrendatario declara conocer la calificación urbanística del local y los usos autorizados, y en consecuencia exime al Arrendador de responsabilidad en caso de que el Local no fuera apto, desde el punto de vista administrativo, para el ejercicio de la actividad. El Arrendatario deberá proveerse de todas las autorizaciones y licencias que se requieran para el ejercicio de su actividad y la apertura del local conforme al destino aquí señalado, y se obliga a mantenerlas en vigor. No será causa de resolución del arriendo el hecho de que se denegaran, suspendieran o revocaran dichos permisos.

Duración

El contrato tendrá una duración de [Nº] años, a contar desde la fecha de este contrato, en que el Local se pone a disposición del Arrendatario mediante la entrega de las llaves de acceso al mismo.

Regimen jurídico

Este Contrato regula un arrendamiento para uso distinto del de vivienda que se regirá, conforme a lo establecido en el artículo 4 de la Ley de Arrendamientos Urbanos, por la voluntad de las partes recogida en este Contrato y, en su defecto, respecto de lo no previsto en el mismo y siempre que no se oponga a los acuerdos en él consignados, por lo dispuesto en el Título III de la citada Ley y, supletoriamente, por el Código Civil.

Renta y actualización

La renta de este contrato se fija en la cantidad de [IMPORTE] euros anuales (- €), pagaderos por mensualidades anticipadas de [IMPORTE] euros (- €) cada una. Dicho importe se verá incrementado en factura con los impuestos aplicables vigentes en cada momento, y minorado con la retención fiscal que, en su caso, legalmente esté establecida.

Se verificarán los pagos por meses anticipados y dentro de los cinco primeros días de cada mes, mediante [ÓRGANO].

La Renta se revisará anualmente a partir de la fecha de este documento por aplicación de las variaciones que experimente el Índice General de Precios al Consumo, Conjunto Nacional, que elabore el Instituto Nacional de Estadística u Organismo que, en su caso, lo sustituya, en los doce meses anteriores a la fecha de efectos de cada actualización, y se aplicará sobre la Renta vigente que corresponda al mes anterior a aquél en que se deba realizar la actualización.

Servicios, suministros y comunidad

El inmueble se arrienda en el actual estado de acometidas, servicios y suministros.

Los gastos por servicios y suministros del Local correrán por cuenta del Arrendatario, que los abonará [FORMA DE PAGO].

Los gastos de comunidad serán de cuenta del [ELEGIR: arrendador / arrendatario].

Fianza

El Arrendatario entrega en este acto al Arrendador en concepto de fianza a los efectos previstos en la LAU, la cantidad de [IMPORTE] euros (.-€) mediante [ÓRGANO] efectivo, talón conformado, etc. La fianza se actualizará de conformidad con lo previsto en el art. 36 LAU 1994 y será devuelta a la extinción de la relación contractual si no hubiera responsabilidades pendientes a cargo del primero.

Conservación y obras del local

Derechos de adquisición preferente

Cesión del contrato y subarriendo

.Se incluirá lo pactado en materia de cesión del contrato y subarriendo, si fuera distinto a lo que establece el artículo 32 la LAU 1994

Fallecimiento del arrendatario

Designación de domicilio

A efectos de notificaciones o emplazamientos judiciales, y en general, toda comunicación o requerimiento que hayan de oír las partes en relación con el presente contrato, se tomará como domicilio del arrendador el señalado al inicio del presente contrato, es decir, calle [CALLE], núm. [Nº], piso [PISO], puerta [PUERTA], de la localidad/ciudad de [LOCALIDAD], provincia de [PROVINCIA], y como domicilio del arrendatario el de la calle [CALLE], núm. [Nº], piso [PISO], puerta [PUERTA], de la localidad/ciudad de [LOCALIDAD], provincia de

De conformidad a lo dispuesto en el artículo 4.6 de la Ley de Arrendamientos Urbanos, las partes designan las siguientes direcciones electrónicas para realizar las notificaciones:

- Por el arrendador

- Por el arrendatario

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata, y por un medio que garantice la recepción del mensaje.

Sumisión a mediación y/o arbitraje

Las partes contratantes acuerdan libre y voluntariamente que todas las desavenencias, divergencias o cuestiones litigiosas que deriven de este contrato, salvo lo estipulado en la cláusula novena de este contrato, se resolverán a través de la Mediación [INSTITUCIÓN DE MEDIACIÓN] de [LOCALIDAD], antes de acudir a la jurisdicción o a otra solución extrajudicial de conflictos, sometiéndose a la regulación establecida en la Ley 5/2012, de 6 de julio, y [OTROS DATOS] fijando un plazo máximo de duración del procedimiento de sesenta días desde la solicitud de iniciación por cualquiera de las partes.

A falta de resolución de la controversia en el procedimiento de mediación, la misma será definitivamente resuelta mediante Arbitraje de la Corte de [LOCALIDAD], a la que se encomienda la administración del arbitraje y la designación de los árbitros, de acuerdo con su reglamento.

Y en prueba de conformidad con cuanto antecede, ambas partes firman este contrato por duplicado y a un solo efecto en el lugar y fecha indicados en el encabezamiento.

Fdo.: Don [NOMBRE Y APELLIDOS] Fdo.: Don [NOMBRE Y APELLIDOS]

-Arrendador- -Arrendatario-

========================================================================
