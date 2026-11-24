---
name: contrato-compraventa-finca-comunidad-bienes-renuncia-civ-0671
description: "Contrato de compraventa de finca de una comunidad de bienes con renuncia solo al retracto legal. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de compraventa de finca de una comunidad de bienes con renuncia solo al retracto legal

> Formulario **CIV-0671** del plugin **Propiedad, posesión, servidumbres e hipotecas** (`formularios-propiedad-y-derechos-reales`) · Civil › Propiedad y derechos reales · normativa revisada el 24-11-2026.

## Qué es

Contrato de compraventa de una finca titularidad de una comunidad de bienes, renunciando los comuneros al retracto legal pero no al convencional, en relación a su porción respectiva. Se concretan las condiciones, pactos y requisitos necesarios para llevar a cabo la compraventa, así como los derechos y obligaciones de comprador y vendedor.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de compraventa de finca de una comunidad de bienes con renuncia solo al retracto legal» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de compraventa de finca de una comunidad de bienes con renuncia solo al retracto legal” para mi caso». También puedes invocarla directamente con `/formularios-propiedad-y-derechos-reales:contrato-compraventa-finca-comunidad-bienes-renuncia-civ-0671`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-propiedad-y-derechos-reales:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Propiedad, posesión, servidumbres e hipotecas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (10 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] IMPORTE (3 veces)
- [ ] Nº (3 veces)
- [ ] FECHA (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] LUGAR
- [ ] MUNICIPIO
- [ ] Nº DE PROTOCOLO
- [ ] PROVINCIA
- [ ] REFERENCIA CATASTRAL
- [ ] TÍTULO DE ADQUISICIÓN

## Normas que cita el formulario

- art. 1522 Código Civil

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

En [LUGAR], a [FECHA].

REUNIDOS

DE UNA PARTE,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con domicilio en [LOCALIDAD], provisto de N.I.F. número [NÚMERO].

Todos ellos como parte vendedora.

Y DE OTRA PARTE

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con domicilio en [LOCALIDAD], provisto de N.I.F. número [NÚMERO], como parte compradora.

Ambas partes recíprocamente se reconocen la suficiente capacidad legal y legitimación, para llevar a efecto el presente contrato de compraventa, acreditando su identidad por los documentos indicados, actuando en nombre y representación propia, y que de común acuerdo se regirán por todo lo establecido libre y voluntariamente en el contenido de las siguientes:

ESTIPULACIONES

Primera.- Que la parte vendedora es propietaria, de forma proindivisa, de la finca sita en el término municipal de [MUNICIPIO] provincia de [PROVINCIA], con una superficie de [Nº] metros cuadrados, lindando a la izquierda con la finca propiedad de D./Dña. [NOMBRE Y APELLIDOS], a la derecha con la finca propiedad de D./Dña. [NOMBRE Y APELLIDOS] constando inscrita en el Registro de la Propiedad de [LOCALIDAD], adquirida por título de [TÍTULO DE ADQUISICIÓN] y formalizada en escritura autorizada por el Notario de [LOCALIDAD] D./Dña. [NOMBRE Y APELLIDOS] en fecha [FECHA] y con número de protocolo [Nº DE PROTOCOLO], estando interesado en venderla.

Referencia catastral: [REFERENCIA CATASTRAL].

Segunda.- Que D./Dña. [NOMBRE Y APELLIDOS], quien de ahora en adelante se le denominará comprador, está interesado en la compra de la finca descrita en la primera estipulación.

Tercera.- A tal efecto, los comuneros venden la finca urbana ya referenciada en la primera estipulación a D./Dña. [NOMBRE Y APELLIDOS], quien a su vez compra, en la cantidad de [IMPORTE] euros ( €).

Cuarta.- En este acto los vendedores reciben la suma indicada, en proporción a sus cuotas de participación y a su entera satisfacción, sirviendo la firma del presente contrato de la más eficaz carta de pago. Vendiendo y transmitiendo la finca libre de cargas, gravámenes, arrendatarios, ocupantes y al corriente de pagos de impuestos, arbitrios y contribuciones.

Quinta.- Los comuneros renuncian en este acto a ejercitar el derecho de retracto legal que les corresponde en virtud del artículo 1522 del Código Civil, quedando no obstante fijado un derecho de retracto convencional para cada uno de los copropietarios de la finca, a ejercitar, exclusivamente respecto de su porción respectiva, en el plazo improrrogable de [Nº] años, no pudiendo el comprador obligarle a redimir la totalidad de la finca.

Sexta.- En caso de ejercicio individual de dicho retracto, el comunero accionante deberá abonar al comprador la cantidad de [IMPORTE] euros ( €), y a su vez, el comprador entregará la porción de finca que le corresponda a aquél comunero, realizando al respecto la preceptiva división.

Séptima.- Igualmente se podrá ejercer el derecho de retracto, comúnmente por todos los integrantes de la parte vendedora, y en el plazo mencionando, estableciéndose un precio de recompra global de [IMPORTE] euros ( €), más la suma consistente en los gastos sufragados por el adquirente por el contrato o cualquier otro relacionado con la compraventa, así como los gastos necesarios y útiles hechos en la finca vendida.

Octava.- Los gastos notariales y registrales que ocasione la división de la finca para el ejercicio de retracto serán sufragados por los comuneros retractantes.

Novena.- Ambas partes se comprometen a elevar a escritura pública el presente contrato en el plazo de [Nº] días.

Décima.- Todos los gastos de la formalización de la escritura pública del presente contrato, así como los posteriores derivados de su inscripción registral e impuestos que pudieran derivarse del mismo, serán a cargo exclusivamente del comprador, a cuyo fin se compromete a comparecer en la Notaría del D./Dña. [NOMBRE Y APELLIDOS] el día y hora que se señale al efecto.

Undécima.- El derecho de retracto podrá ser ejercitado igualmente, aunque sólo durante el tiempo estipulado, por cualquiera de los causahabientes del vendedor, en la proporción que le corresponda, o por uno sólo si se ha adjudicado a un sólo heredero, en caso de fallecimiento de aquél.

Duodécima.- No obstante, en el momento de formalización de la escritura, se transmitirá el dominio de la finca al comprador, el cual deberá conservarla y cuidarla con la diligencia de un buen padre de familia.

Decimotercera.- Ambas partes, con renuncia de su fuero propio si lo tuvieren, se someten expresamente a los Tribunales de [LOCALIDAD] para la interpretación o cualquier cuestión litigiosa que derive de este contrato.

Y para que conste, firman por duplicado y a un solo efecto en el lugar y fecha ‘ut supra’.

VENDEDOR

COMPRADOR

D./Dña. [NOMBRE Y APELLIDOS] D./Dña. [NOMBRE Y APELLIDOS]

========================================================================
