---
name: demanda-ordinaria-danos-materiales-accidente-trafico-civ-0820
description: "Demanda ordinaria por daños materiales en accidente de tráfico contra concesionaria y aseguradora. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda ordinaria por daños materiales en accidente de tráfico contra concesionaria y aseguradora

> Formulario **CIV-0820** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario del propietario de un vehículo contra la entidad concesionaria de una autopista y su aseguradora (acción directa del art. 76 LCS) para reclamar la indemnización de los daños en los bienes sufridos en un accidente de tráfico ocurrido en la autopista, por incumplimiento de las obligaciones de conservación y seguridad de la concesionaria.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda ordinaria por daños materiales en accidente de tráfico contra concesionaria y aseguradora» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda ordinaria por daños materiales en accidente de tráfico contra concesionaria y aseguradora” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-ordinaria-danos-materiales-accidente-trafico-civ-0820`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (5 veces)
- [ ] DENOMINACIÓN SOCIAL DE LA ASEGURADORA (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] Nº (3 veces)
- [ ] AÑO (2 veces)
- [ ] DENOMINACIÓN SOCIAL DE LA CONCESIONARIA (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] FIRMA (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] CIRCUNSTANCIAS
- [ ] DENOMINACIÓN SOCIAL DE LA CONCESIONARIA DE LA AUTOPISTA
- [ ] DOMICILIO PROFESIONAL
- [ ] DÍA
- [ ] MES
- [ ] NOMBRE Y APELLIDOS DEL ABOGADO/A
- [ ] NOMBRE Y APELLIDOS DEL DEMANDANTE
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº DE DOCUMENTO
- [ ] Nº DE INSCRIPCIÓN
- [ ] PUNTOS KILOMÉTRICOS
- [ ] SEDE
- [ ] VEHÍCULO

## Normas que cita el formulario

- art. 85 LOPJ
- art. 51 LEC
- art. 6.1.1.º LEC
- art. 7.1 LEC
- art. 6.1.3.º LEC
- art. 7.4 LEC
- art. 10 LEC
- art. 76 Ley 50/1980
- art. 253.1 LEC
- art. 251 LEC
- art. 5 Ley Orgánica 1/2025
- art. 3 TRLGDCU
- art. 147 TRLGDCU
- art. 128 TRLGDCU
- art. 148 TRLGDCU
- art. 1101 CC
- art. 1902 CC
- art. 76 LCS
- art. 20.4.º LCS
- art. 394.1 LEC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDANTE], y a cuya justificación aporto escritura de poder inscrita en el Registro Electrónico de Apoderamientos Judiciales con el n.º [Nº DE INSCRIPCIÓN] y que se puede acreditar mediante consulta automatizada orientada al dato, por parte del órgano judicial al cual tengo el honor de dirigirme, acompañándose certificación electrónica del Registro Electrónico de Apoderamientos Judiciales como Documento n.º [Nº DE DOCUMENTO], por si no es posible la consulta automatizada, y con la asistencia del/de la Letrado/a D./Dña. [NOMBRE Y APELLIDOS DEL ABOGADO/A], del Ilustre Colegio de la Abogacía de [LOCALIDAD], cuyo despacho está abierto en esta población, calle [DOMICILIO PROFESIONAL], ante la Sección Civil del Tribunal de Instancia que por turno de reparto corresponda, comparezco y, como mejor proceda en Derecho, DIGO:

Que, siguiendo expresas instrucciones de quien ostento representación, por medio del presente escrito formulo demanda de JUICIO ORDINARIO, que dirijo contra:

— [DENOMINACIÓN SOCIAL DE LA CONCESIONARIA DE LA AUTOPISTA], con domicilio en [LOCALIDAD], calle [DOMICILIO].

— La aseguradora [DENOMINACIÓN SOCIAL DE LA ASEGURADORA], para ser citada en su oficina de [LOCALIDAD], calle [DOMICILIO].

HECHOS

PRIMERO.– [EXPONER LOS HECHOS: fecha, hora y lugar del accidente (autopista y punto kilométrico), circunstancias (por ejemplo, calzada en mal estado, aquaplaning, objetos en la vía), atestado levantado por la autoridad, daños sufridos por el vehículo y reclamación previa a la concesionaria y a la aseguradora].

SEGUNDO.– [CONTINUAR LA EXPOSICIÓN DE LOS HECHOS, con referencia a los documentos que se aportan: DOCUMENTO N.º [Nº]].

FUNDAMENTOS DE DERECHO

I.– JURISDICCIÓN Y COMPETENCIA

Los arts. 85 LOPJ y 45 LEC designan a las secciones civiles de los tribunales de instancia como los órganos con la competencia específica, objetiva y funcional para resolver estos pleitos, y es asimismo competente el Tribunal desde el punto de vista territorial, al ser en esta población donde la demandada tiene su domicilio, a tenor de los principios de los arts. 51 y 53 LEC, no estando la materia regida por fuero imperativo, por cuanto se reclama frente a la entidad concesionaria por su condición de prestadora del servicio de mantenimiento de la autopista.

II.– PROCEDIMIENTO

En aplicación de los arts. 248.3 y 249.2 LEC, y en atención a la cuantía del objeto litigioso, que supera los 15.000 euros, este pleito se tramitará por las normas del proceso declarativo llamado juicio ordinario.

III.– CAPACIDAD

Conforme al art. 6.1.1.º LEC, tienen capacidad para ser parte las personas físicas, y a tenor del art. 7.1 LEC detentan capacidad de obrar procesal, en tanto que mayores de edad en pleno ejercicio de sus derechos civiles, siendo el caso del actor.

La capacidad para ser parte de las personas jurídicas se reconoce en el art. 6.1.3.º LEC, cuya personalidad deriva de su constitución en escritura pública inscrita en el Registro Mercantil, debiendo comparecer en juicio por medio de sus representantes legales (art. 7.4 LEC).

IV.– LEGITIMACIÓN

El art. 10 LEC legitima para comparecer y actuar en juicio a los titulares de la relación jurídica o del objeto litigioso, lo cual es legitimación ordinaria, que en el caso de autos detenta, la activa originaria, el demandante, en cuanto titular del derecho subjetivo patrimonial a la reparación de los daños inferidos a su patrimonio, así como, la pasiva originaria, los demandados: [DENOMINACIÓN SOCIAL DE LA CONCESIONARIA], en su condición de entidad concesionaria responsable de la conservación y mantenimiento de la autopista, y [DENOMINACIÓN SOCIAL DE LA ASEGURADORA], al tratarse de la entidad que, por virtud del contrato de seguro, cubría el riesgo de responsabilidad civil derivado de la actividad desarrollada por la citada concesionaria, en lo que es la acción directa recogida en el art. 76 de la Ley 50/1980, de Contrato de Seguro (LCS).

V.– POSTULACIÓN

En aplicación de los arts. 23.1 y 31.1 LEC, las partes comparecerán representadas por Procurador/a de los Tribunales y asistidas por Letrado en ejercicio, ambos habilitados ante el Tribunal.

VI.– CUANTÍA

Cumpliendo la exigencia del art. 253.1 LEC, se cifra la cuantía de la demanda en la cantidad de [IMPORTE] euros, conforme a la regla 1.ª del art. 251 LEC.

VII.– CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4.º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia. [OPCIONAL — incluir si procede: describir en los hechos el medio adecuado de solución de controversias intentado y aportar el documento que lo acredite.]

VIII.– FONDO DEL ASUNTO

VIII.1

Son de aplicación los arts. 3 y 147 del texto refundido de la Ley General para la Defensa de los Consumidores y Usuarios, aprobado por Real Decreto Legislativo 1/2007, de 16 de noviembre (TRLGDCU), dado que el conductor del vehículo que resultó dañado es usuario (art. 3 TRLGDCU) y ha utilizado unos servicios mediante el pago del oportuno peaje (art. 147 TRLGDCU), y la producción de un daño genera responsabilidad objetiva según establecen los arts. 128 y siguientes TRLGDCU (STS de 1 de julio de 1997, rec. 2092/1993), debiéndose tener en cuenta que dicha responsabilidad «cubre los daños originados en el correcto uso de los servicios, cuando por su propia naturaleza, o por estar así reglamentariamente establecido, incluyan necesariamente la garantía de niveles determinados de eficacia o seguridad, en condiciones objetivas de determinación, y supongan controles técnicos, profesionales o sistemáticos de calidad, hasta llegar en debidas condiciones al consumidor y usuario» (art. 148 TRLGDCU), y justamente el art. 27.1 y 2.a) de la Ley 8/1972, de 10 de mayo, de construcción, conservación y explotación de autopistas en régimen de concesión, dispone que «el concesionario deberá conservar la vía, sus accesos, señalización y servicios reglamentarios en perfectas condiciones de utilización. La continuidad en la prestación del servicio le obligará, especialmente, a facilitarlo en condiciones de absoluta normalidad, suprimiendo las causas que originen molestias, incomodidades, inconvenientes o peligrosidad a los usuarios de la vía, salvo que la adopción de medidas obedezca a razones de seguridad o de urgente reparación», de forma que, mediante el pago de un peaje a cargo del usuario, la empresa concesionaria viene obligada a garantizar a este una circulación fluida, rápida y sin riesgo de ningún tipo, y ha de afirmarse que la entidad demandada tiene responsabilidad directa del hecho por el art. 1101 CC (en cuanto que la concesionaria dejó de cumplir aquel servicio que ofreció como contrapartida al pago de peaje) y por el art. 1902 CC, ya que, como indica la STS de 6 de junio de 1997, rec. 165/1993, «la responsabilidad de la empresa es directa ya que se establece por incumplimiento de los deberes que imponen las relaciones de convivencia social de vigilar a las personas y a las cosas que están bajo la dependencia de determinadas personas y de emplear la debida cautela en la elección de servidores y en la vigilancia de sus actos», y es responsabilidad objetiva por aplicación de la normativa de consumidores y usuarios, que lleva a una inversión de la carga de la prueba; por lo que, no acreditando la entidad concesionaria demandada la adopción de todas las medidas adecuadas o convenientes para evitar [CAUSA DEL ACCIDENTE, por ejemplo, que los días de lluvia se produjeran hechos de tráfico por aquaplaning] en el tramo de la autopista donde ocurrió el accidente, cuando se trataba de hechos previsibles, como lo demuestran los diversos accidentes y consecuentes atestados levantados en [CIRCUNSTANCIAS] en el tramo de los p.k. [PUNTOS KILOMÉTRICOS], procede declarar la responsabilidad de la concesionaria demandada y, por ende, condenar a la misma, con la aseguradora codemandada, ex art. 76 LCS, a las cantidades que se dirán.

VIII.2

En el plano de los daños en los bienes, para la fijación del quantum indemnizatorio rige el principio de indemnidad o restitutio in integrum, por lo que la reparación viene fijada por los daños efectivamente sufridos.

Como consecuencia de lo anteriormente expuesto, se reclaman las siguientes cantidades:

— Valor de mercado de segunda mano del [VEHÍCULO], matriculado en el año [AÑO], con arreglo al dictamen pericial del tasador D./Dña. [NOMBRE Y APELLIDOS], que se aporta como documento número [Nº]. Subtotal: [IMPORTE] euros.

— Gastos de servicio de grúa, con arreglo a la factura que se acompaña como documento número [Nº]. Subtotal: [IMPORTE] euros.

Total: [IMPORTE] euros.

VIII.3

Resulta aplicable el régimen especial de mora del asegurador del art. 20.4.º LCS, habida cuenta de que [DENOMINACIÓN SOCIAL DE LA ASEGURADORA] no procedió a remitir, dentro de los tres meses siguientes a la reclamación verificada por la víctima a la aseguradora, una oferta motivada de indemnización, sino que se produjo respuesta motivada del art. 7.2 del texto refundido de la Ley sobre responsabilidad civil y seguro en la circulación de vehículos a motor (RDLeg 8/2004), rechazando la responsabilidad en el siniestro.

IX.– COSTAS

El empleo del principio cuasiobjetivo del vencimiento del art. 394.1 LEC conlleva el deber de reintegro de las costas procesales por la parte demandada, sin que existan dudas de hecho o derecho, ni vacilaciones jurisprudenciales sobre el objeto del proceso.

Por todo lo anteriormente expuesto,

AL TRIBUNAL SUPLICO,

que, habiendo por presentado este escrito, con el poder que acredita la representación procesal y los documentos acompañados, y copias de todo ello, se sirva admitir uno y otros, tener por formulada demanda de juicio ordinario, en nombre de quien comparezco, contra [DENOMINACIÓN SOCIAL DE LA CONCESIONARIA] y [DENOMINACIÓN SOCIAL DE LA ASEGURADORA] y, seguidos que sean los trámites legales, dicte sentencia por la que, estimando íntegramente esta demanda, se condene a los demandados a que indemnicen conjunta y solidariamente en la suma de [IMPORTE] euros a mi representado/a D./Dña. [NOMBRE Y APELLIDOS], incrementadas en lo que representen los intereses de mora al tipo diario consistente en el legal vigente en la fecha de ocurrencia del siniestro incrementado en un cincuenta por ciento desde la fecha de ocurrencia del accidente o, en su caso, del veinte por ciento, respecto de la aseguradora codemandada, y los intereses legales desde la interpelación judicial respecto del otro codemandado, con expresa imposición de las costas a los demandados.

Es justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a: [FIRMA] Firma del Procurador/a: [FIRMA]
