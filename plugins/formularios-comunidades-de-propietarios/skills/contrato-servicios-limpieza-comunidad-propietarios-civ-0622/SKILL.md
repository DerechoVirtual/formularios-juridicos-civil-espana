---
name: contrato-servicios-limpieza-comunidad-propietarios-civ-0622
description: "Contrato de servicios de limpieza para una comunidad de propietarios. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de servicios de limpieza para una comunidad de propietarios

> Formulario **CIV-0622** del plugin **Comunidades de propietarios** (`formularios-comunidades-de-propietarios`) · Civil › Propiedad horizontal · normativa revisada el 24-11-2026.

## Qué es

Contrato por el que una comunidad de propietarios encarga a una empresa de limpieza el servicio de limpieza y mantenimiento de las zonas comunes del edificio, con regulación de duración, precio, obligaciones laborales de la empresa y resolución de conflictos.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de servicios de limpieza para una comunidad de propietarios» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de servicios de limpieza para una comunidad de propietarios” para mi caso». También puedes invocarla directamente con `/formularios-comunidades-de-propietarios:contrato-servicios-limpieza-comunidad-propietarios-civ-0622`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-comunidades-de-propietarios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Comunidades de propietarios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (7 veces)
- [ ] DENOMINACIÓN SOCIAL (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] AÑO (3 veces)
- [ ] DÍA (3 veces)
- [ ] MES (3 veces)
- [ ] CALLE (2 veces)
- [ ] DNI/NIE (2 veces)
- [ ] HORA (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] NIF (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] DOMICILIO SOCIAL
- [ ] FECHA
- [ ] INSTITUCIÓN ARBITRAL O ÁRBITRO
- [ ] NOMBRE Y APELLIDOS DEL PRESIDENTE
- [ ] NOMBRE Y APELLIDOS DEL REPRESENTANTE DE LA EMPRESA
- [ ] Nº DE FOLIO

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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Junto a «…como de los ingresos a cuenta de las retenciones practicadas a los trabajadores.»: el original aludía a los modelos «TC1 y TC2»; la cotización se justifica hoy mediante los documentos de cotización del Sistema RED/Sistema de Liquidación Directa de la Tesorería General de la Seguridad Social; adaptar la referencia.

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

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

INTERVIENEN

De una parte, D./Dª [NOMBRE Y APELLIDOS DEL PRESIDENTE], mayor de edad, con DNI/NIE [DNI/NIE], en nombre y representación de la Comunidad de Propietarios del edificio de la calle [CALLE], n.º [Nº], de la localidad de [LOCALIDAD], provista de NIF n.º [NIF], de la cual es presidente, nombrado en la Junta de Propietarios de fecha [FECHA], según consta en el folio n.º [Nº DE FOLIO] del libro de actas de la Comunidad.

De otra parte, D./Dª [NOMBRE Y APELLIDOS DEL REPRESENTANTE DE LA EMPRESA], mayor de edad, con DNI/NIE [DNI/NIE], en nombre y representación de la mercantil [DENOMINACIÓN SOCIAL], con domicilio social sito en [DOMICILIO SOCIAL] y provista de CIF n.º [NIF], en adelante LA EMPRESA.

Ambas partes, en la condición en la que intervienen, se reconocen capacidad necesaria y suficiente para el otorgamiento del presente CONTRATO DE PRESTACIÓN DE SERVICIOS DE LIMPIEZA y, a tal efecto,

EXPONEN

I.- Que la Comunidad de Propietarios del edificio de la calle [CALLE], n.º [Nº], de la localidad de [LOCALIDAD], está integrada por [Nº] viviendas, [Nº] plazas de garaje, [Nº] escaleras y ascensores y [OTRAS ZONAS COMUNES: p. ej., una plazoleta privada que da acceso al portal].

II.- Que la Comunidad está interesada en contratar los servicios de la EMPRESA [DENOMINACIÓN SOCIAL], a fin de que ésta se ocupe de realizar las labores de limpieza de las zonas comunes del edificio.

Ambas partes lo llevan a efecto y formalizan, mediante el presente CONTRATO DE PRESTACIÓN DE SERVICIOS, conforme a las siguientes

CLÁUSULAS

PRIMERA.- OBJETO.

Constituye el objeto del presente contrato la prestación por la EMPRESA [DENOMINACIÓN SOCIAL] a la COMUNIDAD de los servicios de limpieza y mantenimiento de las zonas comunes a las viviendas y plazas de garaje que integran la COMUNIDAD.

[OPCIONAL — incluir si procede: detalle de las labores de limpieza]

Concretamente, el servicio de limpieza consistirá en [DETALLE DE LAS LABORES: p. ej., limpieza diaria de portales, escaleras, cabinas de ascensores, patios, limpieza de cuartos de contadores, accesos a garaje y garaje y plazoleta privada].

El horario de limpieza será de [DÍAS DE LA SEMANA: p. ej., lunes a viernes], con exclusión de los festivos; se trabajarán [Nº] horas, en el horario de [HORA] a [HORA] horas.

SEGUNDA.- DURACIÓN DEL CONTRATO.

El plazo de duración del presente contrato se extenderá desde el día [DÍA] de [MES] de [AÑO] hasta el día [DÍA] de [MES] de [AÑO], prorrogándose tácitamente por anualidades sucesivas si ninguna de las partes lo resolviera con un mes de antelación a la finalización de cada anualidad de vigencia.

Si se incumpliere el referido plazo de preaviso, la parte que no observare dicho plazo deberá indemnizar a la otra parte contratante, si lleva a efecto la resolución unilateral del contrato antes de su vencimiento, con una indemnización equivalente a dos mensualidades del precio del servicio.

Sin perjuicio de lo establecido en el párrafo anterior, las partes pactan un periodo de prueba de [Nº] meses, durante el cual ambas partes podrán resolver el presente contrato unilateralmente.

TERCERA.- PRECIO.

El precio que se pacta por la prestación de los servicios contratados asciende a la cantidad de [IMPORTE] euros anuales, a los que habrá que aplicar los impuestos correspondientes (IVA y retención de IRPF, en su caso), pagaderos por mensualidades anticipadas de [IMPORTE] euros mensuales dentro de los cinco primeros días de cada mes (mediante transferencia bancaria en la cuenta corriente señalada por la Comunidad a tal efecto).

En caso de tácita reconducción del presente contrato, se pacta que el precio estipulado se incrementará o disminuirá de acuerdo con la variación que experimente el Índice de Precios al Consumo que fije para el Estado el Instituto Nacional de Estadística u organismo que lo sustituya.

CUARTA.- CUMPLIMIENTO DE OBLIGACIONES DE LA EMPRESA.

La EMPRESA [DENOMINACIÓN SOCIAL], que manifiesta estar a la fecha al corriente de sus obligaciones fiscales, con la Seguridad Social y con sus propios trabajadores, asume la responsabilidad plena para el pago de cuantas obligaciones se deriven de las relaciones de trabajo que tenga establecidas con el personal que desempeñe los servicios contratados, obligándose, en todo caso, a proporcionar mensualmente a la Comunidad, a través de su Secretario-Administrador, justificación documental de haber satisfecho tanto las nóminas de los trabajadores como el pago de los seguros sociales (boletines de cotización a la Seguridad Social), así como de los ingresos a cuenta de las retenciones practicadas a los trabajadores.

QUINTA.- NORMATIVA APLICABLE.

En lo no pactado expresamente en este contrato, las partes se someten a las reglas generales de las obligaciones y contratos contenidas en el Código Civil vigente.

SEXTA.- RESOLUCIÓN DE CONTROVERSIAS.

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— Sumisión a tribunales con renuncia al fuero propio: Para cualquier cuestión derivada de la interpretación o aplicación de lo aquí dispuesto, las partes se someten expresamente a la jurisdicción de los Tribunales de [LOCALIDAD], con renuncia a cualquier otro fuero que, en su caso, pudiera corresponderles.

— Sin renuncia al fuero propio: Para cualquier cuestión relacionada con la interpretación y el cumplimiento del presente contrato, ambas partes acuerdan someterse expresamente a los Jueces y Tribunales competentes en virtud de la Ley de Enjuiciamiento Civil vigente.

— Sumisión a arbitraje: Para dirimir cualquier controversia o reclamación derivada del cumplimiento y aplicación de este contrato, las partes se someten, con renuncia a su fuero propio si fuera otro, al arbitraje de [INSTITUCIÓN ARBITRAL O ÁRBITRO].

Y en prueba de conformidad con cuanto antecede, firman ambas partes el presente documento, por duplicado ejemplar y a un solo efecto, en el lugar y fecha indicados en el encabezamiento.

Fdo.: [NOMBRE Y APELLIDOS], LA EMPRESA Fdo.: [NOMBRE Y APELLIDOS], LA COMUNIDAD
