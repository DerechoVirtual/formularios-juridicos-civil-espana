---
name: contrato-opcion-compra-sin-precio-civ-0705
description: "Contrato de opción de compra con o sin precio. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de opción de compra con o sin precio

> Formulario **CIV-0705** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Contrato por el que una parte (concedente, promitente u optatario) concede a otra (optante) la facultad exclusiva de decidir sobre la celebración o no de otro contrato, que ha de realizarse en un plazo cierto y en unas determinadas condiciones mediante precio o gratuitamente.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de opción de compra con o sin precio» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de opción de compra con o sin precio” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:contrato-opcion-compra-sin-precio-civ-0705`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] DNI/NIE (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] FECHA (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] PLAZO (2 veces)
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] IMPORTE
- [ ] LUGAR
- [ ] NOMBRE O DENOMINACIÓN
- [ ] Nº
- [ ] Nº DE CLÁUSULA

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

Contrato por el que una parte (concedente, promitente u optatario) concede a otra (optante) la facultad exclusiva de decidir sobre la celebración o no de otro contrato, que ha de realizarse en un plazo cierto y en unas determinadas condiciones mediante precio o gratuitamente.


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

En [LUGAR], a [FECHA]
REUNIDOS

DE UNA PARTE,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Datos de CONCEDENTE)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, CONCEDENTE.

Y DE OTRA,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Datos del OPTANTE)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, OPTANTE.

INTERVIENEN

[ELEGIR UNA OPCIÓN: en caso de que todas las partes actúen en nombre y representación propia / si alguna de las partes actúa en su propio nombre y representación]

[OPCIONAL — si alguna de las partes actúa en nombre y representación de persona física o jurídica]
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[ELEGIR UNA OPCIÓN: Si se trata de persona física / Si se trata de una persona jurídica]

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato de OPCIÓN DE COMPRA y, a tal fin,

EXPONEN

[ELEGIR UNA OPCIÓN: Muebles / Inmuebles]

II. Que le pertenecen por compra en virtud de escritura pública autorizada por el notario de [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS], el [FECHA] con el número «[NOMBRE O DENOMINACIÓN]» de su protocolo.

[ELEGIR UNA OPCIÓN: Muebles / Inmuebles]

IV. Que ambas partes han convenido el otorgamiento de un contrato de opción de compra sobre los bienes descritos en el expositivo I anterior, conforme a los pactos y cláusulas que se determinan a continuación

CLÁUSULAS

Primera.- Objeto

El CONCEDENTE concede al OPTANTE, que la acepta, la facultad en exclusiva (derecho de opción) de decidir sobre la celebración o no de un contrato de COMPRAVENTA entre ambos cuyo objeto sea [DESCRIPCIÓN DEL BIEN], facultad que podrá ser ejercitada en el plazo de [PLAZO]. contados a partir de la fecha del otorgamiento del presente contrato.

Segunda.- Precio

[ELEGIR UNA OPCIÓN: Con precio / Sin precio]

Tercera.- Duración

El derecho de opción que se otorga en el presente contrato se concede por el plazo de [PLAZO] a contar desde la fecha de su firma. Durante dicho plazo el concedente de la opción no podrá enajenar o gravar por ningún título los bienes objeto del derecho de opción.

Hasta el momento en que se lleve a cabo la eventual compraventa con el OPTANTE, el CEDENTE continuará siendo propietario de dicho objeto, ostentando todos los derechos sobre el mismo en su calidad de propietario, salvo la prohibición de vender a persona distinta del OPTANTE descrita en el párrafo precedente.

Cuarta.- Ejercicio de la Opción

[ELEGIR UNA OPCIÓN: Muebles / Inmuebles]

En dicho caso el Concedente se obliga a entregar la posesión de los bienes en el plazo máximo de [Nº] días a contar desde la notificación por cualquier medio que deje constancia de su recepción, del ejercicio de la opción en el domicilio que se fija en la cláusula [Nº DE CLÁUSULA] En el caso de retraso en la entrega, el Optante tendrá derecho a percibir del Concedente una cantidad igual a [IMPORTE] euros ( €) por cada día de retraso, como sanción que no excluye la posible reclamación por los daños y perjuicios que se causen.

Quinta.- Conservación

En el caso de que el OPTANTE decida ejercer su derecho de opción, el objeto del contrato de compraventa descrito deberá hallarse en ese momento en igual estado que a la fecha de la celebración del presente contrato en que, habiendo sido examinado por el OPTANTE, lo encuentra de su conformidad.

Igualmente, el CEDENTE se obliga al saneamiento y evicción de los referidos bienes en el caso de que se perfeccione la compraventa.

Si, mientras el bien objeto del contrato de compraventa estuviere en poder del CONCEDENTE éste se perdiera o deteriorara de modo que lo haga inservible, quedará nulo el presente contrato y sin efecto y el OPTANTE tendrá derecho a la devolución de la cantidad entregada en concepto de prima por la opción de compra.

Sexta.- No ejercicio

En el caso de que el adquirente del derecho de opción decida no ejercitar el mismo, u opte por dejar caducar el plazo de la opción, podrá el Concedente de la opción disponer de los bienes objeto de la misma con total libertad.

Séptima.- Gastos e Impuestos

Todos los gastos e impuestos que se deriven del presente contrato de opción de compra serán a cargo del/la OPTANTE.

[OPCIONAL — incluir si procede]

(Inmuebles)

Octava.- Formalización

El presente contrato se elevará a escritura pública y podrá ser inscrito en el Registro de la Propiedad a petición de cualquiera de las partes, siendo los gastos que se deriven a costa de la parte que así lo solicite.

.- Notificaciones

Las partes convienen los siguientes domicilios para la práctica de las notificaciones necesarias para la ejecución del presente contrato:

.- Ley aplicable

Las partes, en la representación en que intervienen, manifiestan que el presente contrato tiene carácter de mercantil y se regirá en primer término por las estipulaciones contenidas en el mismo y en lo que en ellas no estuviere previsto por las disposiciones del Código de Comercio, leyes especiales, los usos y costumbres mercantiles.

.- Tribunales

Las partes para cualquier cuestión que pudiera suscitarse en el interpretación y ejecución del presente contrato, se someten expresamente a los Tribunales de [LOCALIDAD].

Y para que conste lo firman por duplicado ejemplar y a un solo efecto en el lugar y fecha arriba indicados.

CONCEDENTE

OPTANTE

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]
