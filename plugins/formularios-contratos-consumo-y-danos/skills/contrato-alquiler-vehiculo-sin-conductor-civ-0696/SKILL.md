---
name: contrato-alquiler-vehiculo-sin-conductor-civ-0696
description: "Contrato de alquiler de vehículo sin conductor. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de alquiler de vehículo sin conductor

> Formulario **CIV-0696** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de alquiler de vehículo sin conductor» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de alquiler de vehículo sin conductor” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:contrato-alquiler-vehiculo-sin-conductor-civ-0696`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (8 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] FECHA (4 veces)
- [ ] IMPORTE (3 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] NIF (2 veces)
- [ ] Nº (2 veces)
- [ ] AÑO
- [ ] DOMICILIO
- [ ] DÍA
- [ ] ENTIDAD BANCARIA
- [ ] INSCRIPCIÓN
- [ ] MES
- [ ] NÚMERO
- [ ] PÁGINA WEB

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

- Junto a «…UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD)»: La LO 15/1999 y su Reglamento (RD 1720/2007) fueron sustituidos por el Reglamento (UE) 2016/679 (RGPD) y la LO 3/2018, de 5 de diciembre (LOPDGDD). Fuente: LO 3/2018, disposición derogatoria única.

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

en el establecimiento comercial de la mercantil arrendadora sito en [LOCALIDAD]

De una parte, D [NOMBRE Y APELLIDOS], mayor de edad, con domicilio en [LOCALIDAD] y titular del NIF -

Interviene en nombre y representación de la mercantil de [DENOMINACIÓN SOCIAL], CIF [NIF], domiciliada en [DOMICILIO] y constituida en [LOCALIDAD] ante el Notario de [LOCALIDAD] D. [NOMBRE Y APELLIDOS], en fecha [FECHA] e inscrita en el Registro Mercantil de [LOCALIDAD] inscripción [INSCRIPCIÓN], en condición de ARRENDADORA

Y de otra, D [NOMBRE Y APELLIDOS], mayor de edad, con domicilio en [LOCALIDAD] y titular del NIF [NIF],;interviene en su propio nombre y derecho, en condición de ARRENDATARIO.

MANIFIESTAN

Que reconociéndose mutuamente las partes la capacidad legal necesaria a los efectos de este CONTRATO DE ARRENDAMIENTO DE BIENES MUEBLES- ALQUILER DE VEHÍCULO SIN CONDUCTOR-, interviniendo en la representación expresada, siendo responsables de la veracidad de sus manifestaciones, y de forma libre, espontánea y de mutuo acuerdo

EXPONEN

I. Que la ARRENDADORA es una entidad mercantil cuyo objeto es el arrendamiento de vehículos sin conductor, número de autorización otorgada por y es propietaria del siguiente vehículo:

Marca:

Modelo:

Matrícula:

Número de bastidor:

Kilómetros realizados:

Antigüedad:

Dicho vehículo está asegurado a todo riesgo en la entidad [DENOMINACIÓN SOCIAL] con póliza número con vigencia hasta el día [FECHA]

II. Que estando interesadas ambas en formalizar el arrendamiento del vehículo indicado es por lo que celebran el presente CONTRATO DE ARRENDAMIENTO DE VEHÍCULO SIN CONDUCTOR de acuerdo con las siguientes

CLÁUSULAS

Objeto y destino

La ARRENDADORA alquila al ARRENDATARIO el vehículo descrito en el expositivo I de este contrato.

El vehículo arrendado se destinará única y exclusivamente al transporte del ARRENDATARIO y sus acompañantes, y dicho vehículo sólo podrá ser conducido por éste o bajo responsabilidad absoluta del mismo, por el conductor o conductores que él señale, siempre que queden cubiertos por el seguro del vehículo, de conformidad con la cobertura que el mismo establece que el ARRENDATARIO declara conocer.

Entrega del vehículo

El vehículo es entregado en este acto al ARRENDATARIO, recibiendo de la dos juegos de las llaves del mismo, así como su documentación completa y el original del último recibo del pago de la prima del seguro contratado.

El vehículo se encuentra en perfecto estado de conservación y funcionamiento según descripción que se recoge en el Anexo que se incorpora a este contrato firmado por ambas partes, donde consta que el depósito de combustible se encuentra lleno, comprometiéndose el ARRENDATARIO a devolverlo en idéntico estado.

Duración del contrato

El periodo de alquiler es el día [FECHA] a las [Nº] horas y el día [FECHA] Hasta las [Nº] horas.

Por tanto, la entrega del vehículo con anterioridad a la finalización del periodo no da derecho al arrendatario a la devolución o deducción de importe alguno del precio a abonar o abonado.

En cualquier caso, el periodo de alquiler podrá ser prorrogado de mutuo acuerdo por las partes, antes del vencimiento del mismo.

Precio convenido

El precio del contrato se ajusta a las tarifas vigentes que se encuentran expuestas a disposición en el local del arrendador y la pagina web [PÁGINA WEB], y que en este caso son las siguientes:

-Precio por día de utilización euros.

-Precio por kilómetro [IMPORTE] euros.

El precio no incluye combustible.

El primer pago se realiza en este acto por importe de [IMPORTE] euros, sirviendo el presente documento de eficaz carta de pago, debiendo abonar el ARRENDATARIO el resto a la devolución del vehículo.

Uso del vehículo

El ARRENDATARIO recibe el vehículo en perfectas condiciones de utilización, tal como consta en el Anexo, y se compromete y obliga a utilizarlo diligentemente y en especial a:

1. Utilizarlo exclusivamente para los fines de transporte privado sin poder destinarlo a otros fines, en especial transporte remunerado de pasajeros o mercancías, pruebas deportivas o entrenamientos de cualquier modalidad y prueba de resistencia de materiales, accesorios o productos para automóviles.

2. No usarlo bajo influencia de alcohol, drogas y en condiciones de inferioridad

física, ni hacer un uso negligente del vehículo del que se derive un menoscabo en la seguridad y funcionamiento, como golpes en bajos, repostaje erróneo y otros análogos.

3. No realizar ninguna alteración o modificación en el vehículo y no llevar a cabo ni encargar ninguna reparación del coche sin consentimiento de la ARRENDADORA..

4.No conducir el vehículo por caminos, superficies no pavimentadas o vías en mal estado.

5. Proteger el vehículo de agentes meteorológicos que pudieran causarle daños.

6. En caso de incidencia grave, accidente o acto delictivo cometido contra el vehículo se obliga a formalizar la correspondiente denuncia, parte de accidente o actuación correspondiente y a informar inmediatamente de la incidencia al ARRENDADOR, transmitiéndole todas las notificaciones y prestando la colaboración necesaria.

7. Llevar la documentación del vehículo, incluido este contrato o una copia del mismo.

Seguros

El precio de alquiler incluyen las coberturas del seguro a todo riesgo concertado con la entidad reseñado en el Expositivo I.

El ARRENDATARIO, mediante la firma de este contrato, se adhiere como asegurado a la mencionada póliza.

Infracciones de tráfico

El ARRENDATARIO será responsable del pago inmediato de las multas ocasionadas por cualquier infracción de la ley durante el período de alquiler.

Deberá informar a la ARRENDADORA sobre cualquier multa impuesta sobre el vehículo o el conductor durante el período de alquiler.

En caso de que las autoridades retengan el vehículo por un acto u omisión por parte del ARRENDATARIO, sea cual fuera la causa, éste será responsable e indemnizará a la ARRENDADORA en todos los gastos incurridos por tal motivo.

Devolución del vehículo

El vehículo debe ser devuelto antes de la finalización del periodo en el establecimiento de la ARRENDADORA sito en [LOCALIDAD], o en alguna de sus sucursales dentro del horario de apertura al público..

El uso del vehículo una vez finalizado el periodo de arrendamiento o su prórroga se entenderá como uso no permitido y facultará a la ARRENDADORA a ejercitar las correspondientes acciones, incluso interponer denuncia por apropiación indebida.

Fianza

El ARRENDATARIO garantiza al ARRENDADOR en concepto de fianza, el pago de la cantidad de [IMPORTE] euros con cargo a la tarjeta de crédito de su cuenta en la entidad emisora [ENTIDAD BANCARIA] número [NÚMERO], para hacer frente a sus responsabilidades y en especial:

Cargos adeudados por tiempo y kilometraje.

Importe o la diferencia de valor de toda rueda de repuesto, neumático, herramienta, accesorio o equipo de radio, que al término del alquiler falte en el vehículo.

Cantidades por reabastecimiento de combustible si devuelve el vehículo con menos cantidad que la que se entregó.

Gastos de traslado y reparación del vehículo, motivados por la utilización de combustible inadecuado.

Pagos de multas, infracciones o responsabilidades derivadas de la indebida utilización del vehículo.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Y en prueba de conformidad con cuanto antecede, ambas partes firman este contrato por duplicado en el que se integra el Anexo expresado, y a un solo efecto en el lugar y fecha indicados en el encabezamiento.

Fdo.: Don [NOMBRE Y APELLIDOS]

-Arrendador

Fdo.: Don [NOMBRE Y APELLIDOS]

-Arrendatario-
