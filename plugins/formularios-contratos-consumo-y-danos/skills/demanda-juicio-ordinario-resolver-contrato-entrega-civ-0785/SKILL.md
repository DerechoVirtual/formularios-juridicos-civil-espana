---
name: demanda-juicio-ordinario-resolver-contrato-entrega-civ-0785
description: "Demanda de juicio ordinario para resolver el contrato por entrega de cosa distinta (aliud pro alio). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio ordinario para resolver el contrato por entrega de cosa distinta (aliud pro alio)

> Formulario **CIV-0785** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario en la que el comprador, normalmente consumidor, ejercita la acción de resolución del contrato de compraventa por entrega de cosa distinta de la pactada (aliud pro alio), por inhabilidad del bien entregado, con restitución del precio e indemnización de daños y perjuicios. El modelo se redacta sobre la venta de un vehículo con defecto de fabricación y es adaptable a otros bienes.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio ordinario para resolver el contrato por entrega de cosa distinta (aliud pro alio)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio ordinario para resolver el contrato por entrega de cosa distinta (aliud pro alio)” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-juicio-ordinario-resolver-contrato-entrega-civ-0785`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (9 veces)
- [ ] FECHA (8 veces)
- [ ] Nº (7 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL DEMANDANTE (2 veces)
- [ ] SEDE (2 veces)
- [ ] ASEGURADORA
- [ ] AÑO
- [ ] COLEGIO DE ABOGADOS
- [ ] CONCLUSIÓN PERICIAL SOBRE EL ORIGEN DEL DEFECTO
- [ ] CUERPO POLICIAL
- [ ] DOMICILIO
- [ ] DÍA
- [ ] LOCALIDAD
- [ ] MARCA
- [ ] MATRÍCULA
- [ ] MES
- [ ] NIF
- [ ] NOMBRE Y APELLIDOS DEL LETRADO
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR
- [ ] PERIODO
- [ ] PLAZO
- [ ] TIPO
- [ ] VÍA

## Normas que cita el formulario

- art. 1101 Código Civil
- art. 1108 Código Civil
- art. 5 Ley Orgánica 1/2025
- art. 1100 Código Civil
- art. 1484 Código Civil
- art. 7.2 Ley 10/2012

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

### Avisos de actualización (3) — se aplican en el texto, nunca se copian en el documento

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…odas, sentencia del Tribunal Supremo de 17 de julio de 2000, recurso 2835/1995).»: las sentencias del Tribunal Supremo de 12 de abril de 1993 y de 17 de febrero de 1994 constaban en el original solo con referencia editorial; completar con el número de recurso o el ECLI antes de citarlas.
- Junto a «…al y nula por la sentencia del Tribunal Constitucional 140/2016, de 21 de julio.»: comprobar la exención o el importe de la tasa aplicable en la fecha de presentación, por si hubiera variado la normativa de tasas judiciales.

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

Don/Doña [NOMBRE Y APELLIDOS DEL PROCURADOR], Procurador/a de los Tribunales, actuando en representación de Don/Doña [NOMBRE Y APELLIDOS DEL DEMANDANTE], según se acredita por [ELEGIR: certificación del registro electrónico de apoderamientos judiciales que acompaño / apoderamiento apud acta otorgado ante el/la Letrado/a de la Administración de Justicia del Tribunal], bajo la dirección letrada de Don/Doña [NOMBRE Y APELLIDOS DEL LETRADO], Abogado/a del Ilustre Colegio de [COLEGIO DE ABOGADOS], ante el Tribunal comparezco y, como mejor proceda en Derecho, formulo demanda de juicio ordinario en ejercicio de la acción de resolución del contrato de compraventa de fecha [FECHA] por entrega de cosa distinta, «aliud pro alio», frente a la mercantil [DENOMINACIÓN SOCIAL], con NIF [NIF], domiciliada en [DOMICILIO], en base a los siguientes hechos y fundamentos de Derecho:

HECHOS

PRIMERO.– En fecha [FECHA], mi representado/a Don/Doña [NOMBRE Y APELLIDOS DEL DEMANDANTE] adquirió de la entidad demandada [DENOMINACIÓN SOCIAL], [ELEGIR: concesionaria de la marca [MARCA] / vendedora], un [BIEN ADQUIRIDO: por ejemplo, vehículo nuevo tipo [TIPO], matrícula [MATRÍCULA]], pactándose un precio de [IMPORTE] euros, que fue abonado [FORMA Y MOMENTO DEL PAGO: por ejemplo, en ese mismo acto] por mi representado/a (se acompaña como DOCUMENTO Nº [Nº] el contrato de fecha [FECHA] y la factura de compra por importe de [IMPORTE] euros).

SEGUNDO.– En fecha [FECHA], es decir, transcurridos [PLAZO] desde la adquisición, [DESCRIPCIÓN DEL SUCESO: por ejemplo, mi representado/a circulaba con el citado vehículo por el carril izquierdo de la autopista [VÍA] y, de repente, el coche empezó a hacer un ruido, produciéndose un desplazamiento y perdiendo en ese instante la rueda posterior izquierda, quedando sostenido solo sobre tres ruedas] (se acompaña a efectos acreditativos, como DOCUMENTOS Nº [Nº], copia del atestado elaborado por los agentes de [CUERPO POLICIAL] y reportaje fotográfico).

La causa de dicho suceso fue [CAUSA: por ejemplo, la rotura de la unión del eje de la rueda con la llanta], debido a un defecto de fabricación, tal como se desprende del informe elaborado por [ASEGURADORA], que por este motivo rechazó el siniestro (se acompaña como DOCUMENTO Nº [Nº] el informe del perito Don/Doña [NOMBRE Y APELLIDOS] de la aseguradora, a efectos acreditativos).

Ante tan grave avería, y habida cuenta de que se trataba de un defecto de fabricación que hacía inhábil el bien para su uso, mi representado/a encomendó al perito Don/Doña [NOMBRE Y APELLIDOS], [TITULACIÓN: por ejemplo, Ingeniero Industrial Superior], la elaboración de un dictamen pericial sobre los defectos, emitiéndose por este el correspondiente informe, donde se concluye que «[CONCLUSIÓN PERICIAL SOBRE EL ORIGEN DEL DEFECTO]» y que «[CONCLUSIÓN PERICIAL SOBRE LA IMPOSIBILIDAD O INVIABILIDAD DE LA REPARACIÓN]» (de conformidad con el artículo 336 de la Ley de Enjuiciamiento Civil se acompaña como DOCUMENTO Nº [Nº] el dictamen pericial elaborado por el perito Don/Doña [NOMBRE Y APELLIDOS]).

TERCERO.– De acuerdo con lo expuesto en el hecho anterior, estamos ante un incumplimiento objetivo grave y constitutivo de la entrega de una cosa por otra (aliud pro alio), dándose todos los requisitos exigidos jurisprudencialmente para el éxito de la acción de resolución por incumplimiento, puesto que, como se dice en la sentencia del Tribunal Supremo de 22 de mayo de 2008 (recurso 391/2001), uno de los supuestos de incumplimiento que abren paso a la protección que dispensan los artículos 1101 y 1124 del Código Civil, susceptible también de ser contemplado bajo el principio de identidad e integridad del pago del artículo 1166 del mismo cuerpo legal, es el de entrega de cosa distinta o aliud pro alio, que se produce cuando el objeto entregado por el vendedor es inhábil para el cumplimiento de su finalidad, como es el caso ahora contemplado, al darse las siguientes circunstancias: 1) existía un vicio oculto en el bien adquirido, desconocido y sorpresivo para el comprador, preexistente a la venta, puesto que queda acreditado por la pericial y la documental aportadas que se trata de un defecto oculto con origen en la fabricación; y 2) el vicio es de tal gravedad que hace impropio el bien para el uso a que se destina, totalmente inhábil para satisfacer el interés del comprador, por lo que existe pleno incumplimiento por inhabilidad del objeto, al haberse entregado una cosa diversa a la convenida, lo que permite a mi representado/a acudir a la protección dispensada en los artículos 1101 y 1124 del Código Civil, pues la inaptitud del objeto para el uso a que debía ser destinado significa incumplimiento del contrato.

Por otra parte, tratándose de una venta a mi representado/a en condición de consumidor, no puede perderse de vista que rige, como señala la jurisprudencia del Tribunal Supremo (sentencia de 22 de julio de 1994, recurso 2377/1991, entre otras), una inversión de la carga de la prueba, de manera que, denunciado y advertido el defecto del objeto adquirido, corresponde a los vendedores acreditar el perfecto estado del objeto, la inexistencia del defecto o problema alegado, o bien la reparación plenamente satisfactoria del mismo que revele su condición óptima para el uso a que se destina.

CUARTO.– Al amparo de los preceptos mencionados, se reclama la devolución de la cantidad satisfecha por mi representado/a como precio del bien, que asciende a [IMPORTE] euros, y, como indemnización de daños y perjuicios, la cantidad de [IMPORTE] euros, por los perjuicios derivados del incumplimiento contractual, concretados en [CONCEPTOS: por ejemplo, el pago del impuesto de matriculación para la adquisición de un nuevo vehículo, los gastos de alquiler de vehículo soportados durante el periodo posterior al accidente y la peritación de daños] (a efectos acreditativos se acompañan como DOCUMENTOS Nº [Nº] la factura de compra de fecha [FECHA] y la factura de alquiler correspondiente al periodo [PERIODO]), solicitando que estas cantidades se incrementen con el interés legal desde la fecha de esta demanda conforme al artículo 1108 del Código Civil.

QUINTO.– Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO: negociación directa, mediación, conciliación, etc.], con fecha [FECHA], no habiendo sido posible alcanzar un acuerdo definitivo. Se acompaña como DOCUMENTO Nº [Nº] la documentación que lo acredita.

FUNDAMENTOS DE DERECHO

Competencia

Corresponde a los Tribunales de [SEDE] al ser el lugar en el que tiene su domicilio la mercantil demandada (artículo 51 de la Ley de Enjuiciamiento Civil).

Legitimación

Le corresponde a esta parte su condición de compradora lesionada por el incumplimiento del demandado, en ejercicio de la acción de resolución contractual.

Procedimiento

Es el juicio ordinario con fundamento en el artículo 249.2 de la Ley de Enjuiciamiento Civil, dado el importe reclamado de [IMPORTE] euros, que excede de los 15.000 euros a partir de los cuales deben seguirse las reclamaciones por las normas del juicio ordinario.

Cumplimiento de los requisitos de procedibilidad

La presente demanda cumple con los requisitos de procedibilidad exigidos por los artículos 264.4.º y 399.3 de la Ley de Enjuiciamiento Civil, así como con lo dispuesto en el artículo 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

Acción ejercitada

Se ejercita la acción resolutoria por entrega de cosa diversa o «aliud pro alio», amparada en los artículos 1101 y 1124 del Código Civil. La acción es compatible con las establecidas en el Real Decreto Legislativo 1/2007, de 16 de noviembre, por el que se aprueba el texto refundido de la Ley General para la Defensa de los Consumidores y Usuarios, pudiendo ejercitar el consumidor la acción de resolución o la de saneamiento prevista en la legislación de consumo si se dan los requisitos establecidos en cada una de ellas, incluso articulándolas de forma subsidiaria.

Fondo de la reclamación

Los artículos 1100, 1101 y 1124 del Código Civil y la jurisprudencia que los interpreta: entre otras, sentencias del Tribunal Supremo de 12 de abril de 1993, de 17 de febrero de 1994, de 25 de octubre de 1994 (recurso 2154/1991) y de 9 de julio de 2007 (recurso 2863/2000), que expresan que se está en presencia de entrega de cosa diversa o «aliud pro alio» cuando existe pleno incumplimiento por inhabilidad del objeto y consiguiente insatisfacción total del contratante, lo que le permite acudir a la protección dispensada en los artículos 1101 y 1124 del Código Civil, sin que, en ese supuesto, sea aplicable el plazo semestral que señala el artículo 1490 para el ejercicio de las acciones edilicias, porque los artículos 1484 y 1490 del Código Civil, como reguladores de las acciones redhibitoria y «quanti minoris», integradas en el artículo 1486, resultan inaplicables en aquellos supuestos en que la demanda no se dirige a obtener las reparaciones provenientes de los vicios ocultos, sino las derivadas del defectuoso cumplimiento al haber sido hecha la entrega de cosa distinta o con vicios que hagan impropio el objeto de la compraventa para el fin a que se destina, por integrar el «aliud pro alio» un incumplimiento absoluto y total de la prestación, sustancialmente distinto a la mera presencia de vicios (por todas, sentencia del Tribunal Supremo de 17 de julio de 2000, recurso 2835/1995).

Fondo de la reclamación: resolución del contrato e indemnización de daños y perjuicios

De conformidad con lo dispuesto en los artículos 1101 y 1124 del Código Civil, ante un incumplimiento por inhabilidad del objeto, con la consiguiente insatisfacción del comprador y el resultado de objeto totalmente inhábil, procede la resolución contractual con la consiguiente devolución del precio pagado y, a su vez, la correspondiente indemnización por los daños y perjuicios causados derivados del contrato de compraventa (sentencias del Tribunal Supremo de 2 de marzo de 1982, 23 de marzo de 1982, 20 de octubre de 1984, 6 de marzo de 1985, 6 de abril de 1989, 14 de mayo de 1992 y 15 de noviembre de 2005, recurso 1189/1999).

En materia de costas, el artículo 394 de la Ley de Enjuiciamiento Civil señala que las de primera instancia se imponen a la parte que vea rechazadas sus pretensiones.

En base a lo anterior,

SUPLICO AL TRIBUNAL: que tenga por presentada la presente demanda, con el dictamen pericial y los documentos a ella adjuntos, por parte en la representación que ostento, y tras la pertinente tramitación dicte sentencia por la que se declare resuelto el contrato de compraventa de fecha [FECHA], condenando a la entidad demandada a la devolución del precio abonado de [IMPORTE] euros y a que indemnice a mi mandante en la cantidad de [IMPORTE] euros, con más los intereses legales desde el día [FECHA], todo ello con imposición de costas a la parte demandada.

OTROSÍ PRIMERO DIGO: que se fija la cuantía del presente procedimiento en [IMPORTE] euros.

En base a lo anterior,

SUPLICO AL TRIBUNAL: que se tenga por efectuada la anterior manifestación a los efectos pertinentes.

OTROSÍ SEGUNDO DIGO: que estando la presente demanda sujeta al abono de la tasa por el ejercicio de la potestad jurisdiccional fijada por la Ley 10/2012, de 20 de noviembre, y desarrollada por la Orden HAP/2662/2012, de 13 de diciembre, siendo mi representado/a persona [ELEGIR: jurídica / física] no exenta de su pago, se acompaña a la presente demanda como DOCUMENTO Nº [Nº] la correspondiente autoliquidación con el ejemplar para la Administración de Justicia debidamente validado y en el que consta el pago de la cantidad de [IMPORTE] euros correspondiente a la cuota fija, sin que se incluya la cuota variable prevista en el artículo 7.2 de la Ley 10/2012 al haber sido declarada inconstitucional y nula por la sentencia del Tribunal Constitucional 140/2016, de 21 de julio.

En base a lo anterior,

SUPLICO AL TRIBUNAL: que tenga por hecha la anterior manifestación a los efectos pertinentes y por acompañado el documento justificativo del abono de la tasa.

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado: Firma del Procurador:
