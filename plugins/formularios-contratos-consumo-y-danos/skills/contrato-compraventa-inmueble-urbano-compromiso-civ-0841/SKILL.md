---
name: contrato-compraventa-inmueble-urbano-compromiso-civ-0841
description: "Contrato de compraventa de inmueble urbano con compromiso de elevarlo a escritura pública. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de compraventa de inmueble urbano con compromiso de elevarlo a escritura pública

> Formulario **CIV-0841** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Contrato de compraventa de bien inmueble urbano con compromiso de las partes de elevar el contrato a escritura pública, corriendo el comprador con los gastos, incluyendo como opción pacto de reserva de dominio y cláusula penal.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de compraventa de inmueble urbano con compromiso de elevarlo a escritura pública» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de compraventa de inmueble urbano con compromiso de elevarlo a escritura pública” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:contrato-compraventa-inmueble-urbano-compromiso-civ-0841`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (11 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] IMPORTE (4 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] FECHA (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] PROFESIÓN (2 veces)
- [ ] IMPORTE EN CIFRA
- [ ] LUGAR
- [ ] Nº
- [ ] Nº DE PROTOCOLO
- [ ] PROVINCIA

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

Notas al pie del formulario original:
(1) El presente contrato es un contrato privado, siendo aconsejable en estos casos de compraventa de bien inmueble su elevación a escritura pública para que el negocio jurídico pueda acceder al Registro de la Propiedad, y así el nuevo titular pueda quedar amparado por la protección que dicho Registro otorga.

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

En [LUGAR], a [FECHA]
REUNIDOS

DE UNA PARTE, D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, [ESTADO CIVIL] (estado civil) [PROFESIÓN], con domicilio en [LOCALIDAD], provisto de N.I.F. número [NÚMERO]

Y DE OTRA PARTE, D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, [ESTADO CIVIL] (estado civil) [PROFESIÓN], con domicilio en [LOCALIDAD], provisto de N.I.F. número [NÚMERO]

Ambas partes recíprocamente se reconocen la suficiente capacidad legal y legitimación para llevar a efecto el presente contrato de compraventa, acreditando su identidad por los documentos indicados, actuando en nombre y representación propia, y que de común acuerdo se regirá por todo lo establecido libre y voluntariamente en el contenido de las siguientes:

ESTIPULACIONES

PRIMERA.- Que D./Dña. [NOMBRE Y APELLIDOS], a quien de ahora en adelante se denominará vendedor, es propietario de la finca sita en el término municipal de [LOCALIDAD], provincia de [PROVINCIA], con una superficie de [Nº] metros cuadrados, lindando a la izquierda con la finca propiedad de D./Dña. [NOMBRE Y APELLIDOS], a la derecha con la finca propiedad de D. [NOMBRE Y APELLIDOS], constando inscrita a su nombre y libre de cargas en el Registro de la Propiedad de [LOCALIDAD], mediante título de compraventa en escritura autorizada por el Notario de [LOCALIDAD] D. [NOMBRE Y APELLIDOS] en fecha [FECHA] y con número de protocolo [Nº DE PROTOCOLO], estando interesado en venderla.

Referencia catastral:

SEGUNDA.- Que D./Dña. [NOMBRE Y APELLIDOS], a quien de ahora en adelante se denominará comprador, está interesado en la compra de la finca descrita en la primera estipulación.

TERCERA.- D./Dña. [NOMBRE Y APELLIDOS], vende la finca urbana ya referenciada en la primera estipulación a D./Dña. [NOMBRE Y APELLIDOS], quien a su vez compra, en la cantidad de [IMPORTE] euros ([IMPORTE EN CIFRA] €).

[OPCIONAL — si se trata de una compraventa con entrega del precio y transmisión civil del dominio]

CUARTA.- En este acto el vendedor recibe la suma indicada, a su entera satisfacción, sirviendo la firma del presente contrato de la más eficaz carta de pago, vendiendo y transmitiendo la finca libre de cargas, gravámenes, arrendatarios, ocupantes y al corriente de pagos de impuestos, arbitrios y contribuciones.

[OPCIONAL — si se trata de una compraventa con pacto de reserva de dominio y cláusula penal]

CUARTA.- En este acto el vendedor recibe la suma de [IMPORTE] euros, a su entera satisfacción, sirviendo la firma del presente contrato de la más eficaz carta de pago, quedando pendiente la cantidad de [IMPORTE] euros que se harán efectivas a la parte vendedora en pagos trimestrales a razón de [IMPORTE] euros cada uno de ellos, con vencimiento en los días uno de los meses de abril, julio, octubre y enero de cada año.

QUINTA.- La venta de la finca descrita en la primera estipulación queda condicionada al total pago del precio estipulado y en los plazos fijados, no perfeccionándose hasta que dicho precio haya sido pagado en su totalidad.

SEXTA.- En caso de impago de dos plazos consecutivos o alternos, quedará el contrato sin efecto alguno, quedando en poder del vendedor lo percibido hasta ese momento, en concepto de daños y perjuicios, si las cantidades satisfechas fuesen inferiores al treinta por ciento del precio total de venta; si la cantidad percibida hubiese sido mayor, se devolverá al comprador la diferencia.

SÉPTIMA.- La parte vendedora transmite la finca libre de cargas, gravámenes, arrendatarios, ocupantes y al corriente de pagos de impuestos, arbitrios y contribuciones, declarando la parte compradora que recibe la finca en perfecto estado de conservación y habitabilidad y a su entera satisfacción.

QUINTA.- Ambas partes se comprometen a elevar a escritura pública el presente contrato en el plazo de días, corriendo con todos los gastos que de ello se derive la parte compradora, obligándose a comparecer ante el Notario el vendedor en el día y a la hora que se le indique.

SEXTA.- Ambas partes, con renuncia de su fuero propio si lo tuvieren, se someten expresamente a los Tribunales de [LOCALIDAD] para la interpretación o cualquier cuestión litigiosa que derive de este contrato.

En prueba de aceptación y conformidad, y para que así conste, las partes suscriben el presente documento, por duplicado ejemplar y a un solo efecto, en el lugar y fecha arriba indicados.

LA VENDEDORA

EL ADQUIRIENTE

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]
