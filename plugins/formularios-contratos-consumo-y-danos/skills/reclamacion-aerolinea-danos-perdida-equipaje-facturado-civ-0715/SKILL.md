---
name: reclamacion-aerolinea-danos-perdida-equipaje-facturado-civ-0715
description: "Reclamación a la aerolínea por daños o pérdida del equipaje facturado. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Reclamación a la aerolínea por daños o pérdida del equipaje facturado

> Formulario **CIV-0715** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Reclamación a la aerolínea por daños o pérdida del equipaje facturado» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Reclamación a la aerolínea por daños o pérdida del equipaje facturado” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:reclamacion-aerolinea-danos-perdida-equipaje-facturado-civ-0715`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] DESCRIPCIÓN DE LOS OBJETOS (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] MARCA/MODELO (2 veces)
- [ ] AÑO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DOMICILIO
- [ ] DÍA
- [ ] FECHA
- [ ] LUGAR
- [ ] MES
- [ ] NÚMERO

## Normas que cita el formulario

- art. 118 Ley 48/1960

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

Nombre/razón social de la compañía transportista [DENOMINACIÓN SOCIAL]

Domicilio social [DOMICILIO]

Att. Servicio de Atención al Cliente

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Muy señores míos,

Por medio de la presente me dirijo a Ustedes en mi condición de pasajero del vuelo celebrado con su compañía en fecha de [FECHA] e identificado con el número [NÚMERO] (a efectos de prueba aporto copia del correspondiente billete). En dicho vuelo facturé dos maletas (aporto copia de los dos justificantes de facturación), una de las cuales no me fue entregada en el lugar de destino y otra lo fue, pero abierta y rota, y sin parte de su contenido (aporto copia fotográfica de los desperfectos de la maleta, así como copia del documento que el Servicio de Atención al Cliente de su compañía en el aeropuerto me entregó tras personarme en el mismo para hacer constar todas esas circunstancias).

La maleta extraviada, marca [MARCA/MODELO], contenía los siguientes objetos que paso a relacionar:

[DESCRIPCIÓN DE LOS OBJETOS]

De la maleta entregada en mal estado, marca [MARCA/MODELO], habían desaparecido los siguientes objetos, que paso a relacionar: [DESCRIPCIÓN DE LOS OBJETOS].

Teniendo en cuenta que según la Ley 48/1960, de 21 de julio, sobre navegación aérea (BOE del 23), en su artículo 97, “El transportista estará obligado a transportar juntamente con los viajeros y dentro del precio del billete, el equipaje, con los límites de peso y volumen que fijen los Reglamentos. El exceso será objeto de estipulación especial.”

Que su artículo 98 establece que “El transportista responderá únicamente de la pérdida, sustracción o deterioro del equipaje que se le haya entregado para su custodia.”

Que en el artículo 116 se dice, además, que “El transportista es responsable del daño o perjuicio causado durante el transporte:

1.º Por muerte, lesiones o cualquier otro daño corporal sufrido por el viajero.

2.º Por destrucción, pérdida, avería o retraso de las mercancías y de los equipajes, facturadas o de mano.”

Que en el artículo 118, se fijan las indemnizaciones, respecto a la carga o equipaje facturado, o de mano, actualizadas por el Real Decreto 37/2001, de 19 de enero (BOE de 2 de febrero):

«Artículo 3.º Indemnizaciones relativas a equipajes y mercancías.—A los efectos previstos en el artículo 118 de la Ley 48/1960, las indemnizaciones respecto a la carga o equipaje facturado o de mano serán, en su equivalencia en [IMPORTE] euros, las siguientes:

1.ª Por pérdida o avería de la carga, hasta el límite de 17 derechos especiales de giro por kilogramo de peso bruto.

2.ª Por pérdida o avería de equipajes, facturados o de mano, hasta el límite de 500 derechos especiales de giro por unidad.

3.ª Por retraso en la entrega de la carga o equipaje facturado, hasta el límite de una cantidad equivalente al precio del transporte.

Si la carga o equipaje facturado o de mano se transporta bajo manifestación de valor declarado, aceptado por el transportista, el límite de responsabilidad corresponde a ese valor».

Que en el artículo 120 se prevé que “La razón de indemnizar tiene su base objetiva en el accidente o daño y procederá, hasta los límites de responsabilidad que en este capítulo se establecen, en cualquier supuesto, incluso en el de accidente fortuito y aun cuando el transportista, operador o sus empleados justifiquen que obraron con la debida diligencia.”

Y que en el artículo 124 se establece que “La acción para exigir el pago de las indemnizaciones a que se refiere este capítulo prescribirá a los seis meses a contar desde la fecha en que se produjo el daño.

Las reclamaciones por avería o retraso de la carga o equipaje facturado deberán formalizarse por escrito ante el transportista u obligado, dentro de los diez días siguientes al de la entrega, o a la fecha en que debió entregarse, conforme a lo dispuesto en esta Ley sobre el contrato de transporte. La falta de esta reclamación previa impedirá el ejercicio de las acciones correspondientes.”

En consecuencia, y dentro del plazo de diez días de los que dispongo a tenor de artículo reproducido en último lugar, formulo ante Ustedes reclamación al objeto de que me sea abonada indemnización de los daños y perjuicios que cuantifico en [IMPORTE] euros, equivalentes al valor de la maleta y los objetos personales desaparecidos y al importe de sustitución de la maleta dañada. De no proceder en ese sentido, me veré obligado a ejercitar judicialmente la pertinente acción en defensa de mis intereses patrimoniales.

Sin otro particular, se despide atentamente

Fdo.

(Firma del pasajero perjudicado)
