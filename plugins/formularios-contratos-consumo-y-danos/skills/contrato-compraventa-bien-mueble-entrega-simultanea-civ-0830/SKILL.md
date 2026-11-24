---
name: contrato-compraventa-bien-mueble-entrega-simultanea-civ-0830
description: "Contrato de compraventa de bien mueble con entrega simultánea al pago o diferida. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de compraventa de bien mueble con entrega simultánea al pago o diferida

> Formulario **CIV-0830** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Contrato de compraventa de un bien mueble, con tres modalidades alternativas: entrega simultánea de la cosa y del precio; precio aplazado sin entrega de la cosa hasta el pago íntegro; o venta condicionada a que no se ejercite un compromiso de venta anterior a favor de un tercero, con pago aplazado.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de compraventa de bien mueble con entrega simultánea al pago o diferida» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de compraventa de bien mueble con entrega simultánea al pago o diferida” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:contrato-compraventa-bien-mueble-entrega-simultanea-civ-0830`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (5 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] NOMBRE Y APELLIDOS DEL COMPRADOR (3 veces)
- [ ] NOMBRE Y APELLIDOS DEL VENDEDOR (3 veces)
- [ ] AÑO (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] MES (2 veces)
- [ ] NIF (2 veces)
- [ ] DESCRIPCIÓN DEL BIEN MUEBLE OBJETO DE ESTE CONTRATO
- [ ] DÍA
- [ ] FECHA
- [ ] IMPORTE EN LETRA
- [ ] NOMBRE Y APELLIDOS DEL BENEFICIARIO DEL COMPROMISO DE VENTA
- [ ] PORCENTAJE

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

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO]

REUNIDOS

DE UNA PARTE, D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, [ESTADO CIVIL], con domicilio en [DOMICILIO], provisto de N.I.F. número [NIF].

Y DE OTRA PARTE, D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, [ESTADO CIVIL], con domicilio en [DOMICILIO], provisto de N.I.F. número [NIF].

Ambas partes recíprocamente se reconocen la suficiente capacidad legal y legitimación para llevar a efecto el presente contrato de compraventa, actuando en nombre y representación propia, y que se regirá por todo lo establecido libre y voluntariamente en el contenido de las siguientes:

ESTIPULACIONES

PRIMERA.- Que D./Dña. [NOMBRE Y APELLIDOS DEL VENDEDOR], a quien de ahora en adelante se denominará vendedor, es propietario del bien mueble [DESCRIPCIÓN DEL BIEN MUEBLE OBJETO DE ESTE CONTRATO], que se encuentra en perfecto estado de conservación y uso, estando interesado en venderlo.

SEGUNDA.- Que D./Dña. [NOMBRE Y APELLIDOS DEL COMPRADOR], a quien de ahora en adelante se denominará comprador, está interesado en la compra del bien mueble descrito en la primera estipulación.

TERCERA.- D./Dña. [NOMBRE Y APELLIDOS DEL VENDEDOR] vende el bien mueble referenciado en la primera estipulación a D./Dña. [NOMBRE Y APELLIDOS DEL COMPRADOR], quien a su vez compra, en la cantidad de [IMPORTE EN LETRA] euros ([IMPORTE] €).

[ELEGIR UNA DE ESTAS TRES MODALIDADES Y SUPRIMIR LAS DEMÁS:]

— MODALIDAD A (compraventa con entrega simultánea de cosa y precio):

CUARTA.- En este acto el vendedor recibe la suma indicada, a su entera satisfacción, sirviendo la firma del presente contrato de la más eficaz carta de pago.

QUINTA.- El comprador recibe igualmente en el mismo acto, a su entera satisfacción, el bien mueble objeto de este contrato, sin que nada tenga que pedir ni reclamar al vendedor una vez haya dado la conformidad del mismo.

— MODALIDAD B (compraventa sin entrega de la cosa hasta la satisfacción íntegra por el comprador del precio aplazado):

CUARTA.- En este acto el vendedor recibe la cantidad de [IMPORTE] euros correspondientes al [PORCENTAJE] por ciento de la suma indicada objeto de esta compra referenciada en la anterior estipulación, quedando pendiente la cantidad de [IMPORTE] euros, que serán satisfechas por el comprador al vendedor del uno al cinco de cada mes en el domicilio del vendedor o en una cuenta bancaria que éste designe, a razón de [IMPORTE] euros cada mes, hasta su total liquidación, correspondiendo la última mensualidad al mes de [MES] del año [AÑO], sirviendo la firma del presente contrato de la más eficaz carta de pago.

QUINTA.- El comprador acepta no entrar en posesión inmediata del bien mueble, quedando éste en poder del vendedor hasta la total liquidación de la cantidad acordada en esta venta, quien cuidará con la diligencia debida de un buen padre de familia hasta la entrega del mismo, una vez cumplidas las condiciones de pago.

SEXTA.- El impago de dos mensualidades consecutivas o alternas dejará sin efecto ni valor alguno el presente contrato, quedando facultado el vendedor para iniciar las acciones legales para que se le hagan efectivos los importes pendientes de pago, corriendo el comprador con todos los gastos que esto ocasionase, o devolver al comprador el cincuenta por ciento de las cantidades percibidas hasta dicho momento, quedando el resto en su poder en concepto de indemnización por daños y perjuicios, perdiendo el comprador dichas cantidades así como cualquier derecho que le hubiese correspondido sobre el bien mueble.

— MODALIDAD C (compraventa condicionada, por existir un compromiso de venta anterior, de un bien mueble con pago aplazado):

CUARTA.- D./Dña. [NOMBRE Y APELLIDOS DEL VENDEDOR] vende el bien mueble referenciado en la primera estipulación a D./Dña. [NOMBRE Y APELLIDOS DEL COMPRADOR], quien a su vez compra, en la cantidad de [IMPORTE] euros, condicionado a que sólo podrá adquirirlo en el supuesto caso de que D./Dña. [NOMBRE Y APELLIDOS DEL BENEFICIARIO DEL COMPROMISO DE VENTA] no ejercite el derecho que tiene, por existir el compromiso de venta a su favor, y que dicha transmisión no podrá realizarse hasta el día [FECHA], fecha en que concluye el plazo existente del compromiso de venta.

QUINTA.- En este acto el vendedor recibe la mitad de la suma indicada en la anterior estipulación objeto de la compra, a su entera satisfacción, sirviendo la firma del presente contrato de la más eficaz carta de pago, y en cuanto a la cantidad restante, la pagará el comprador el primer día en que se produzca la entrega del bien aquí adquirido.

SEXTA.- Si no se llegase a la transmisión del bien porque se ejerciera y llevase a efecto el compromiso de venta ya conocido, el vendedor devolverá la cantidad recibida en este acto al día siguiente después del cual sea imposible el cumplimiento de la compraventa objeto de este contrato.

SÉPTIMA.- Ambas partes, con renuncia de su fuero propio si lo tuvieren, se someten expresamente a los Tribunales de [LOCALIDAD] para la discusión litigiosa de cualquier cuestión dimanante del presente contrato.

[NOTA: en las modalidades A y B esta cláusula de sumisión se numerará como SEXTA o SÉPTIMA según corresponda, ajustando la numeración.]

En prueba de aceptación y conformidad, y para que así conste, las partes suscriben el presente documento, por duplicado ejemplar y a un solo efecto, en el lugar y fecha arriba indicados.

EL VENDEDOR: Firmado: D./Dña. [NOMBRE Y APELLIDOS]

EL COMPRADOR: Firmado: D./Dña. [NOMBRE Y APELLIDOS]
