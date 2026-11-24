---
name: contrato-cesion-bienes-acreedores-pago-deudas-civ-0704
description: "Contrato de cesión de bienes a los acreedores en pago de deudas. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de cesión de bienes a los acreedores en pago de deudas

> Formulario **CIV-0704** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Contrato por el que un deudor (Cedente) pone a disposición de sus acreedores (Cesionarios) todos o parte de sus bienes con la finalidad de que los propios acreedores administren esos bienes y los liquiden para satisfacer sus respectivos derechos de crédito con el precio que se haya obtenido de esa liquidación.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de cesión de bienes a los acreedores en pago de deudas» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de cesión de bienes a los acreedores en pago de deudas” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:contrato-cesion-bienes-acreedores-pago-deudas-civ-0704`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] IMPORTE (6 veces)
- [ ] DNI/NIE (4 veces)
- [ ] CALLE (3 veces)
- [ ] Nº (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] DÍA (2 veces)
- [ ] FECHAS (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] AÑO
- [ ] CAUSA
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] FECHA
- [ ] LUGAR
- [ ] MES
- [ ] NOMBRE DE LA PARTE
- [ ] PORCENTAJE
- [ ] SEDE
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

Contrato por el que un deudor (Cedente) pone a disposición de sus acreedores (Cesionarios) todos o parte de sus bienes con la finalidad de que los propios acreedores administren esos bienes y los liquiden para satisfacer sus respectivos derechos de crédito con el precio que se haya obtenido de esa liquidación.


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
(Datos del CEDENTE)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, CEDENTE.

Y DE OTRA,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Datos del CESIONARIO)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, CESIONARIO.

INTERVIENEN

[ELEGIR UNA OPCIÓN: en caso de que todas las partes actúen en nombre y representación propia / si alguna de las partes actúa en su propio nombre y representación]

[OPCIONAL — si alguna de las partes actúa en nombre y representación de persona física o jurídica]
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[ELEGIR UNA OPCIÓN: Si se trata de persona física / Si se trata de una persona jurídica]

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato de CESIÓN DE BIENES EN PAGO y, a tal fin,

MANIFIESTAN

I. Que EL CEDENTE es propietario en régimen de plena propiedad y dominio de [DESCRIPCIÓN DEL BIEN], por título de [TÍTULO DE ADQUISICIÓN]

Que el producto se encuentra libre de toda carga o gravamen y no existe sobre el mismo contienda judicial o de cualquier otra índole.

[OPCIONAL — incluir si procede]

(Inmueble)

I. Que EL CEDENTE es propietario en régimen de plena propiedad y dominio del departamento número [NÚMERO], que está dotado de acceso independiente por la calle [CALLE], y linda, tomando como frente la calle [CALLE]: frente o este, dicha calle, zaguán, cuartos de instalaciones y escalera de acceso a las plantas altas; derecha o norte, calle [CALLE]; izquierda o sur, patio y zaguán de acceso a la planta baja; y fondo u oeste,

El local está integrado en la comunidad de propietarios del edificio como uno de sus inmuebles horizontales, rigiéndose por las normas de la Ley 49/1960, de 21 de julio, de Propiedad Horizontal y disposiciones complementarias. Su cuota es de [PORCENTAJE] ( %). Está inscrito en el Registro de la Propiedad Número [NÚMERO] de los de [SEDE], finca registral número [NÚMERO]. Referencia catastral:

Que el inmueble se encuentra libre de toda carga o gravamen y no existe sobre el mismo contienda judicial o de cualquier otra índole.

II. Que EL CEDENTE le debe a [NOMBRE Y APELLIDOS] la cantidad de [IMPORTE] euros ( [IMPORTE] €), como consecuencia de [CAUSA]:

III. Que no disfrutando el deudor de liquidez, ambas partes convienen en otorgar el presente contrato de CESIÓN DE BIENES EN PAGO, que se regirá por las siguientes:

CLÁUSULAS

Primera.- Objeto

Por el presente contrato, EL CEDENTE transmite al CESIONARIO, que acepta, el bien descrito en la manifestación [Nº] del apartado precedente, con cuanto le sea anejo, inherente o accesorio, y libre de cargas, gravámenes, sin arrendar y al corriente en el pago de todo tipo de gastos, impuestos y arbitrios.

Segunda.- Apoderamiento

EL CEDENTE apodera irrevocablemente al CESIONARIO tan ampliamente como sea preciso en derecho, para la enajenación y administración del bien cedido, siendo el valor de la presente cesión el de [IMPORTE] euros ( [IMPORTE] €) y, en su caso, el que resulte de la venta del mismo.

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

Tercera.- Exención de deuda

EL CEDENTE queda liberado de las responsabilidades patrimoniales descritas con el importe obtenido de la venta indicada en la cláusula anterior, aunque lo obtenido por la enajenación del bien cedido fuera inferior al importe de la deuda a que alude este contrato.

Tercera.- Reconocimiento de deuda

EL CEDENTE reconoce expresamente que queda pendiente de pago y, por lo tanto adeuda al CESIONARIO, la cantidad líquida y vencida de [IMPORTE] euros.

Reconocida la deuda anterior, EL CEDENTE se compromete a pagar el importe adeudado en [Nº] mensualidades sucesivas de [IMPORTE] euros cada una.

El pago de las mensualidades establecidas se hará efectivo entre los días [FECHAS] y [DÍA] de cada mes en la cuenta bancaria núm. [Nº] que EL CESIONARIO tiene abierta en

El primer pago deberá realizarse entre los días [FECHAS] y [DÍA] del mes de [MES] de [AÑO]

Cuarta.- Seguro

EL CEDENTE contratará un seguro que resulte satisfactorio para EL CESIONARIO que cubra el riesgo de daños o pérdida que pueda sufrir el bien cedido durante todo el período de vigencia del presente contrato y hasta el momento en que la transmisión del bien se efectúe.

EL CEDENTE proporcionará al CESIONARIO, a su solicitud, pruebas de la existencia de dicho seguro. La cobertura incluirá, entre otros aspectos, los daños provocados por incendios, agua, fenómenos naturales y robo.

Quinta.- Formalización

Este Contrato podrá ser elevado a escritura pública, a petición de cualquiera de las Partes corriendo a su cargo los gastos producidos por esta formalización

Sexta.- Notificaciones

Las partes señalan como domicilios para la práctica de las notificaciones necesarias en la ejecución del presente contrato:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

Séptima.- Protección de datos personales

Las partes reconocen que la legislación sobre protección de datos personales (Ley Orgánica 3/2018, de 5 de diciembre, de protección de datos personales y garantía de derechos digitales) establece una serie de obligaciones en el tratamiento de datos de carácter personal, entre las que destaca la prohibición de realizar cesiones de datos de carácter personal sin la correspondiente autorización del titular de los datos personales.

Octava.- Impuestos

Todos los impuestos, gastos judiciales o extrajudiciales originados a consecuencia de la celebración del presente contrato serán de cuenta de [NOMBRE DE LA PARTE].

Novena.- Naturaleza del contrato y normativa aplicable

El presente contrato tiene naturaleza mercantil, rigiéndose por lo dispuesto en sus propias cláusulas y en lo en ellas no previsto por el Código de Comercio, leyes especiales y usos mercantiles que le sean aplicables, o en lo no previsto, por las disposiciones del Código Civil.

Décima.- Fuero competente

[ELEGIR UNA OPCIÓN: Sometimiento a tribunales / Sometimiento a arbitraje]

Y en prueba de conformidad con todo ello firman el presente documento por duplicado ejemplar y a un solo efecto en el lugar y fecha expresados en el encabezamiento.

CEDENTE	CESIONARIO

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]
