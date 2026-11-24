---
name: demanda-juicio-cambiario-accion-directa-contra-civ-1151
description: "Demanda de juicio cambiario por acción directa contra la sociedad aceptante y sus avalistas. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio cambiario por acción directa contra la sociedad aceptante y sus avalistas

> Formulario **CIV-1151** del plugin **Cobrar deudas: monitorio y cambiario** (`formularios-reclamar-deudas-monitorio`) · Civil › Monitorio y cambiario · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio cambiario: acción directa contra varios ejecutados (mercantil librada aceptante y 4 avalistas solidarios), basadas en 2 letras de cambio con protesto notarial tras falta de pago llegado el vencimiento. Se solicita seguir el orden indicado para los requerimientos de pago y, en su caso, para las diligencias de embargo preventivo.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio cambiario por acción directa contra la sociedad aceptante y sus avalistas» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio cambiario por acción directa contra la sociedad aceptante y sus avalistas” para mi caso». También puedes invocarla directamente con `/formularios-reclamar-deudas-monitorio:demanda-juicio-cambiario-accion-directa-contra-civ-1151`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-reclamar-deudas-monitorio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Cobrar deudas: monitorio y cambiario) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (28 veces)
- [ ] NÚMERO (20 veces)
- [ ] IMPORTE (12 veces)
- [ ] FECHA (10 veces)
- [ ] IMPORTE EN CIFRA (10 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] DENOMINACIÓN SOCIAL (5 veces)
- [ ] CALLE (4 veces)
- [ ] DOMICILIO (4 veces)
- [ ] Nº DE DOCUMENTO (4 veces)
- [ ] LUGAR (2 veces)
- [ ] CLASE
- [ ] DIRECCIÓN
- [ ] ENTIDAD BANCARIA
- [ ] OTROS DATOS
- [ ] SEDE

## Normas que cita el formulario

- art. 85.1 LOPJ
- art. 819 LEC
- art. 822 LEC

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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: Un solo TI por partido judicial (art. 84.1 LOPJ): sobra «de los de». Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.C.

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales que actúa en la representación de D./Dña. [NOMBRE Y APELLIDOS], con D.N.I. n.º [NÚMERO] y D./Dña. [NOMBRE Y APELLIDOS], con D.N.I. n.º [NÚMERO] como acredito mediante escritura de poder inscrito en el Registro Electrónico de Apoderamientos Judiciales, a cuya justificación aporto certificación de dicho Registro como documento nº [Nº DE DOCUMENTO], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que en la representación que ostento formulo DEMANDA DE JUICIO CAMBIARIO contra

D./Dña. [NOMBRE Y APELLIDOS], D.N.I. n.º [NÚMERO], domiciliado en [DOMICILIO], calle [CALLE], n.º [NÚMERO];

D./Dña. [NOMBRE Y APELLIDOS], D.N.I. n.º [NÚMERO], domiciliado en [DOMICILIO], calle [CALLE], n.º [NÚMERO];

D./Dña. [NOMBRE Y APELLIDOS], D.N.I. n.º [NÚMERO], domiciliado en [DOMICILIO], calle [CALLE], n.º [NÚMERO];

D./Dña. [NOMBRE Y APELLIDOS], D.N.I. n.º [NÚMERO], domiciliado en [DOMICILIO], calle [CALLE], n.º [NÚMERO];

y contra la mercantil " [DENOMINACIÓN SOCIAL], S.A.", con domicilio social en [LOCALIDAD], Avenida de [DIRECCIÓN], n.º [NÚMERO],

reclamándoles conjuntamente, a los cuatro primeros en su calidad de avalistas, y a la última en la de aceptante, la suma impagada de las letras de cambio que se adjuntan y las demás responsabilidades que se dirán.

La demanda se funda en los siguientes:

HECHOS

PRIMERO.- Mis representados son tenedores legítimos de dos letras de cambio expedidas ambas en [LOCALIDAD] el [FECHA] y con vencimiento en fecha [FECHA], de timbre clase [CLASE], la n.º [NÚMERO] por importe de [IMPORTE] euros ([IMPORTE EN CIFRA] €) y la n.º [NÚMERO] por importe de [IMPORTE] euros ([IMPORTE EN CIFRA] €), a cargo de la demandada " [DENOMINACIÓN SOCIAL] " que las aceptó pura y simplemente.

Como consta en el dorso de las propias letras, fueron avaladas solidariamente, por los cuatro codemandados D./Dña. [NOMBRE Y APELLIDOS], D./Dña. [NOMBRE Y APELLIDOS], D./Dña. [NOMBRE Y APELLIDOS], y D./Dña. [NOMBRE Y APELLIDOS]

Se acompañan los dos cambiales como documentos nos. y [Nº DE DOCUMENTO].

SEGUNDO.- Llegada la fecha de vencimiento, dichas letras resultaron impagadas. Esta falta de pago consta mediante protesto notarial levantado en tiempo y forma, el cual fue comunicado fehacientemente a la librada dentro del plazo legal prevenido de ocho días, sin que con ocasión del protesto " [DENOMINACIÓN SOCIAL] " o los demás interesados que debieran ser puestos en antecedentes por la avalada, hicieran manifestación alguna.

Los gastos notariales devengados por el protesto y la comunicación subsiguiente ascienden a la cantidad de [IMPORTE] euros ([IMPORTE EN CIFRA] €), según notas de las actas de protesto, que se adjuntan como documentos nos. y [Nº DE DOCUMENTO].

TERCERO.- El fundamento de las letras de cambio impagadas es un contrato de compraventa de sesenta y seis acciones de la mercantil demandada " ", articulado ante la sociedad [DENOMINACIÓN SOCIAL], el [OTROS DATOS] el [FECHA], por precio de [IMPORTE] euros ([IMPORTE EN CIFRA] €), y diferido en seis cambiales, de las que han vencido las dos que se ejecutan, otras dos vencerán el [FECHA] y las dos restantes el [FECHA], lo que se manifiesta al objeto de apreciar la extensión del eventual embargo de bienes de los ejecutados avalistas, de no producirse el pago según es lo coherente con la actitud rebelde demostrada por ellos, pues habrá de servir de garantía al apremio inminente por el incumplimiento de las venideras letras aceptadas.

Se adjunta fotocopia del contrato como documento n.º [NÚMERO].

CUARTO.- La antedicha actitud definitivamente rebelde al pago de las cambiales vencidas y que hace presumir razonablemente el impago de las demás restantes hasta el precio total, resulta evidente para esta parte porque, ante los requerimientos notariales cursados por mis patrocinados a los cuatro avalistas, a través de su Abogado y a su costa, indagando con éxito dispar su domicilio particular, no ha existido contestación alguna.

A su acreditación se aporta Acta autorizada por el Notario de [LOCALIDAD] D./Dña. [NOMBRE Y APELLIDOS], de fecha [FECHA], n.º [NÚMERO] de su protocolo, como documento nº [Nº DE DOCUMENTO], con diligencia de la notificación al Sr./a. [NOMBRE Y APELLIDOS], del Notario de [LOCALIDAD] D./Dña. [NOMBRE Y APELLIDOS], de [FECHA], n.º [NÚMERO], como documento n.º [NÚMERO], con comunicación al Sr./a. [NOMBRE Y APELLIDOS], y de la Notario de [LOCALIDAD] D./Dña. [NOMBRE Y APELLIDOS], de [FECHA], n.º [NÚMERO], como documento n.º [NÚMERO], con notificación al Sr./a. [NOMBRE Y APELLIDOS], e intento fallido al Sr./a. [NOMBRE Y APELLIDOS], cuyo paradero se ignora.

Además de haber desoído los ejecutantes el intento de solución amistosa por vía telefónica y correo privado, no han contestado nada a los requerimientos fehacientes, por lo que fuerzan esta vía jurisdiccional, quedando enterados de la presentación al cobro y del protesto, no ya sólo por el deber legal de la sociedad avalada, que como accionistas e incluso administradores les tiene ubicados con perfección, de hacérselo saber, sino por el intento calificable de excesiva buena fe de mis representados de comunicárselo mediante Notario en los domicilios que, con mejor o peor suerte, han podido privadamente averiguar.

El costo de los requerimientos, que consta en las facturas cosidas a las Actas hace un total de [IMPORTE] euros ([IMPORTE EN CIFRA] €).

QUINTO.- La cantidad objeto de reclamación en esta demanda es la de [IMPORTE] euros ( [IMPORTE] €), importe de las expresadas letras de cambio, más los réditos de la cantidad anterior devengados desde la fecha del vencimiento de la letra calculados al tipo del interés legal del dinero incrementado en dos puntos, además de los gastos de protesto y los derivados de la devolución bancaria de los efectos que ascienden a [IMPORTE] euros ([IMPORTE EN CIFRA] €), a cuya demostración se acompaña como documento n.º [NÚMERO], certificado expedido por la entidad domiciliataria CAJA DE AHORRROS [ENTIDAD BANCARIA], y las costas del juicio que, prudencialmente por ahora, han de fijarse en [IMPORTE] euros ([IMPORTE EN CIFRA] €).

A los anteriores hechos son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

I. Ejercitándose en esta demanda la acción dimanante de una letra de cambio, se interpone ante el Tribunal de Instancia que ha de conocer de ella, conforme a la regla sobre competencia territorial imperativa establecida en el art. 820, párrafo 2.º de la Ley 1/2000, de 7 de enero, de Enjuiciamiento Civil (LEC) en relación con lo dispuesto en el art. 85.1º LOPJ, dado que siendo varios los deudores por obligación derivada de los mismos títulos, es el del partido de los Tribunales a que me dirijo domicilio de dos de ellos.

II. La acción cambiaria puede ejercitarse, tanto en la vía ordinaria, como a través del proceso especial cambiario, conforme al art. 49, párrafo 2.º de la Ley 19/1985, de 16 de julio, Cambiaria y del Cheque (LCCH), reformado por la Disposición Final 10.ª.2 LEC.

III.- Arts. 23 y 31 LEC, según los cuales no se excepciona para el juicio cambiario que la comparecencia en juicio se efectúe por medio de Procurador, y bajo dirección y firma de Letrado.

IV. El proceso especial cambiario de los arts. 819-27 LEC es un juicio especial documental en que la legitimación se acredita preliminarmente mediante aportación de un título formal (art. 821.1 y 2 párrafo 1.º LEC), que en el caso son dos letras de cambio, cuya corrección dimana de la concurrencia en las mismas de todas y cada una de las menciones que exige el art. 1 LCCH.

V. Los que hubieren librado, aceptado, endosado o avalado una letra de cambio responden solidariamente frente al tenedor, que tendrá derecho a proceder contra todas estas personas individual y conjuntamente, sin que sea indispensable observar el orden en que se hayan obligado (art. 57 LCCH).

VI. La acción cambiaria puede ser directa contra el aceptante y sus avalistas o de regreso contra cualquier otro obligado, y el tenedor podrá reclamar a la persona contra la quien ejercite la acción directa —como es caso, contra aceptante y avalistas—, sin necesidad de protesto —aunque en el caso lo ha habido—, el importe de la letra de cambio no pagada, los réditos de la cantidad anterior devengados desde la fecha de vencimiento de la letra calculados al tipo de interés legal del dinero incrementado en dos puntos, y los demás gastos, incluidos los del protesto y los de comunicaciones (art. 58 en relación con el art. 49 párrafo 1.º LCCH).

VII. La letra de cambio tendrá aparejada ejecución a través del juicio cambiario que regula la Ley de Enjuiciamiento Civil en el Capítulo II, Título III, del Libro IV, por la suma determinada en el título y por las demás cantidades, conforme a los arts. 58, 59 y 62 LCCH, sin necesidad de reconocimiento judicial de las firmas.

El ejercicio de la acción cambiaria, a través del proceso especial cambiario, se someterá al procedimiento establecido en la Ley de Enjuiciamiento Civil, con las particularidades previstas en los artículos anteriores y las que a continuación se expresan (arts. 66 y 68 LCCH).

VIII. El avalista responde de igual manera que el avalado, y no podrá oponer las excepciones personales de éste. Será válido el aval aunque la obligación garantizada fuere nula por cualquier causa que no sea la de vicio de forma (art. 37 párrafo 1.º LCCH).

Los avalistas de las letras presentadas se ha intentado queden notificados fehacientemente del impago de la entidad avalada, son administradores de ésta, y no hay exigencia legal de reclamación en la acción directa más allá de la derivada de su firma en las letras afianzando el crédito para su vencimiento.

IX. Aunque el deudor atienda en el plazo legal del requerimiento al pago, y poniéndose a disposición de mis mandantes la suma de dinero pagado, y entregándose las letras a aquél, se ponga término al proceso, serán de cargo conjunto de los deudores las costas procesales (art. 822 en relación con 583 LEC).

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito de demanda con la copia de poderes y originales de las letras de cambio acompañadas, así como de las actas de protesto y demás documentos, se sirva admitirlo, tenerme por comparecido y parte en la representación de D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS], y por formulada conjuntamente demanda de juicio cambiario contra D./Dña. [NOMBRE Y APELLIDOS], D./Dña. [NOMBRE Y APELLIDOS], D./Dña. [NOMBRE Y APELLIDOS], D./Dña. [NOMBRE Y APELLIDOS], y la mercantil ‘[DENOMINACIÓN SOCIAL]’, procediéndose a:

A) Requerir a los deudores a fin de que paguen la cantidad de [IMPORTE] euros ([IMPORTE EN CIFRA] €) importe de las dos letras de cambio base de la demanda, más los réditos desde la fecha del vencimiento calculados al tipo de interés legal del dinero incrementado en dos puntos, así como los gastos de protesto, devolución bancaria y comunicaciones, que ascienden a [IMPORTE] euros ([IMPORTE EN CIFRA] €), y las costas del juicio que, prudencialmente y por ahora, han de fijarse en [IMPORTE] euros ([IMPORTE EN CIFRA] €), así como a
B) Ordenar el inmediato embargo preventivo de bienes de los deudores por la citada suma total, por si no se atendiera el requerimiento de pago en el plazo legal de diez días, expidiéndose mandamiento al Servicio Común de Notificaciones y Embargos, a fin de que asistida la comisión judicial del Sr. Letrado de la Administración de Justicia u Oficial Habilitado, se personen en el domicilio de los deudores y diligencien el embargo, y
C) Para el caso de que no satisfagan las dichas cantidades, ni tampoco formulen oposición, se despache la ejecución contra los bienes de los expresados deudores, y
D) Para el caso de que formulen oposición en tiempo y forma, por el Letrado de la Administración de Justicia judicial se me traslade y convoque a juicio verbal, que seguido que sea por sus demás trámites, lleve a dictar Sentencia que condene al pago solidario de los demandados a mis representados de cuanto se acredita a razón de las letras, con lo demás que sea de Justicia que pido en [LUGAR], a [FECHA].

OTROSI DIGO: A los efectos del art. 57 LCCH, en relación con el art. 822 y 581 LEC, sobre orden de los requerimientos de pago y en su caso de los subsiguientes embargos, interesa que las expresadas diligencias se entiendan en primer lugar con los avalistas D./Dña. [NOMBRE Y APELLIDOS], con D./Dña. [NOMBRE Y APELLIDOS], con D./Dña. [NOMBRE Y APELLIDOS], y con D./Dña. [NOMBRE Y APELLIDOS], y sólo posteriormente, en quinto lugar, con la mercantil " ", por lo que

SUPLICO AL TRIBUNAL, se sirva acordar por dicho orden de la práctica de las mencionadas diligencias de embargo preventivo, como es Justicia de hacerse en [LOCALIDAD] en lugar y fecha "ut supra".

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a
