---
name: demanda-reclamacion-legado-especifico-cosa-propia-civ-0466
description: "Demanda de reclamación de un legado específico de cosa propia del testador. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de reclamación de un legado específico de cosa propia del testador

> Formulario **CIV-0466** del plugin **Herencias, testamentos y donaciones** (`formularios-herencias-y-donaciones`) · Civil › Sucesiones y donaciones · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario por la que el legatario ejercita la acción personal ex testamento (actio legati) para reclamar a los herederos la entrega de un legado de cosa específica y determinada, propia del testador (en el modelo, una vivienda), mediante el otorgamiento de la escritura pública de entrega de legados, más los frutos y rentas producidos desde el fallecimiento del causante.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de reclamación de un legado específico de cosa propia del testador» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de reclamación de un legado específico de cosa propia del testador” para mi caso». También puedes invocarla directamente con `/formularios-herencias-y-donaciones:demanda-reclamacion-legado-especifico-cosa-propia-civ-0466`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-herencias-y-donaciones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Herencias, testamentos y donaciones) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (14 veces)
- [ ] Nº (14 veces)
- [ ] FECHA (6 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] NOMBRE Y APELLIDOS DEL CAUSANTE (6 veces)
- [ ] CORREO ELECTRÓNICO (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] DOMICILIO DEL INMUEBLE (2 veces)
- [ ] DOMICILIO PROFESIONAL (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] NOMBRE DEL NOTARIO (2 veces)
- [ ] Nº DE PROTOCOLO (2 veces)
- [ ] SEDE (2 veces)
- [ ] TELÉFONO (2 veces)
- [ ] AÑO
- [ ] CALLE
- [ ] DEMANDA / PAPELETA
- [ ] DÍA
- [ ] EDAD
- [ ] FECHAS
- [ ] IMPORTE EN LETRA
- [ ] MES
- [ ] NOMBRE Y APELLIDOS DEL ABOGADO/A
- [ ] NOMBRE Y APELLIDOS DEL HEREDERO 1
- [ ] NOMBRE Y APELLIDOS DEL HEREDERO 2
- [ ] NOMBRE Y APELLIDOS DEL LEGATARIO
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] NOMBRE Y APELLIDOS, Nº DE COLEGIADO
- [ ] Nº DE COLEGIADO
- [ ] Nº DE FINCA

## Normas que cita el formulario

- art. 399.1 LEC
- art. 85.1 LOPJ
- art. 52.1 LEC
- art. 253.1 LEC
- art. 251 LEC
- art. 23 LEC
- art. 399 LEC
- art. 5 Ley Orgánica 1/2025
- art. 885 Código Civil
- art. 882 Código Civil
- art. 1.025 Código Civil
- art. 394.1 LEC
- art. 24.2 LEC
- art. 609 Código Civil
- art. 155.3 LEC
- art. 52.1.4.º LEC
- art. 887 Código Civil
- art. 817 Código Civil
- art. 1.027 Código Civil
- art. 1.911 Código Civil

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…entro de la cuota de que puede disponer el testador y no perjudican la legítima.»: el original se refería al Registro Central de Actos de Última Voluntad (hoy Registro General de Actos de Última Voluntad) y a la DGRN; los preceptos del Código Civil citados deben contrastarse con la redacción vigente por si hubieran sido modificados por la Ley 8/2021 u otras reformas.

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

Q.P.T.R.C.

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS DEL LEGATARIO], con domicilio en [DOMICILIO], representación que acredito mediante [ELEGIR LA OPCIÓN QUE CORRESPONDA SEGÚN CÓMO SE HAYA OTORGADO EL PODER; ver nota (1)]:

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— poder otorgado a través de la sede judicial electrónica, inscrito en el Registro Electrónico de Apoderamientos Judiciales, cuya certificación acompaño a este escrito.

— poder otorgado mediante comparecencia apud acta, inscrito en el Registro Electrónico de Apoderamientos Judiciales, cuya certificación acompaño a este escrito.

— escritura de poder otorgada a mi favor ante el Notario D./Dña. [NOMBRE DEL NOTARIO], con el número [Nº DE PROTOCOLO] de su protocolo, inscrita en el Registro Electrónico de Apoderamientos Judiciales, cuya certificación acompaño a este escrito.

bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS DEL ABOGADO/A], abogado/a en ejercicio, con despacho profesional abierto en [DOMICILIO PROFESIONAL], colegiado n.º [Nº DE COLEGIADO] del Ilustre Colegio de la Abogacía de [LOCALIDAD], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que mediante el presente escrito vengo a ejercitar ACCIÓN PERSONAL EX TESTAMENTO DE RECLAMACIÓN DE LEGADO (ver nota (2)) que le corresponde en la herencia de D./Dña. [NOMBRE Y APELLIDOS DEL CAUSANTE] a mi mandante, debiendo ser citados como parte demandada D./Dña. [NOMBRE Y APELLIDOS DEL HEREDERO 1], con domicilio (ver nota (3)), primero en [DOMICILIO]; y segundo, el domicilio laboral en [DOMICILIO PROFESIONAL]; con (ver nota (4)) correo electrónico [CORREO ELECTRÓNICO] y con número de teléfono móvil [TELÉFONO]; y D./Dña. [NOMBRE Y APELLIDOS DEL HEREDERO 2]; todo ello de conformidad con los hechos y fundamentos de derecho que se especificarán.

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa e, incluso, en una eventual fase de ejecución, por medios telemáticos, en los términos del art. 399.1, párrafo segundo, LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y número de teléfono: [CORREO ELECTRÓNICO] / [TELÉFONO].

HECHOS

PRIMERO.– El causante D./Dña. [NOMBRE Y APELLIDOS DEL CAUSANTE] falleció en [LOCALIDAD], de la que era vecino, domiciliado en la calle [CALLE], n.º [Nº], en estado de [ELEGIR: viudo / viuda / soltero / soltera / otro estado civil] [ELEGIR: sin descendencia alguna / con descendencia], el día [FECHA], a la edad de [EDAD] años.

Se acredita con aportación de certificación literal de la inscripción de defunción en el Registro Civil de [LOCALIDAD] (DOCUMENTO NÚMERO [Nº]).

SEGUNDO.– El finado había otorgado testamento en fecha [FECHA], ante el Notario de [LOCALIDAD], D./Dña. [NOMBRE DEL NOTARIO], al número [Nº DE PROTOCOLO] de su protocolo general corriente, que no ha sido revocado por otro posterior, en el que lega a favor de mi mandante la vivienda sita en [DOMICILIO DEL INMUEBLE] y se instituye como herederos testamentarios universales en el remanente de todos sus bienes, derechos y acciones a [IDENTIFICACIÓN DE LOS HEREDEROS, p. ej. los hijos de su cónyuge fallecido/a], D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS], que aceptaron la herencia en escritura notarial de fecha [FECHA].

Se acompañan como DOCUMENTOS NÚMEROS [Nº] y [Nº] copia auténtica del dicho testamento y certificado del Registro General de Actos de Última Voluntad.

Asimismo, se acompaña como DOCUMENTO NÚMERO [Nº] copia de la escritura de aceptación de herencia realizada por los demandados, así como del inventario de los bienes que constituyen el caudal relicto, del que se infiere que el valor catastral de la finca objeto del legado asciende a [IMPORTE] euros, de lo que se deja constancia a los efectos de determinar la cuantía del pleito e, indirectamente, el procedimiento a seguir.

TERCERO.– Como D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS], en su condición de herederos no legitimarios de D./Dña. [NOMBRE Y APELLIDOS DEL CAUSANTE], no han dado cumplimiento al legado que éste constituyó a favor de mi mandante, [ésta / éste] presentó [DEMANDA / PAPELETA] de conciliación que fue desatendida, como revela el acta levantada el [FECHA], que se adjunta como DOCUMENTO NÚMERO [Nº].

CUARTO.– La finca objeto del legado referido y cuya entrega se reclama en la presente demanda pertenecía en el momento del fallecimiento al causante y, por consiguiente, la misma formaba parte de su caudal hereditario.

Fue adquirida por el causante en fecha [FECHA], a virtud de contrato de compraventa, y se halla inscrita a nombre de éste con el número de finca registral [Nº DE FINCA] en el Registro de la Propiedad de [LOCALIDAD], en el Libro [Nº], Tomo [Nº], Folio [Nº], inscripción [Nº], según queda acreditado con la correspondiente certificación literal expedida por dicho Registro y que se acompaña a la presente como DOCUMENTO NÚMERO [Nº].

QUINTO.– En razón a todo lo expuesto debe darse exacto cumplimiento a la voluntad del testador, que en este caso sin duda alguna aparece movido por un más que comprensible agradecimiento a mi mandante, [quien le cuidó y sirvió al menos durante los últimos [Nº] años de su vida, supliendo la obligación moral de los familiares y de los más próximos allegados — SUPRIMIR O ADAPTAR SEGÚN LOS HECHOS REALES], y por ello también íntegra acogida a la demanda que, ante la falta del voluntario cumplimiento de dicha disposición, se deduce judicialmente.

SEXTO.– La parte actora manifiesta que, previamente a la presentación de la presente demanda, se han llevado a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria; incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, mi representado envió un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por el demandado por el mismo medio, [ELEGIR: rechazando el acuerdo / habiendo sido solo posible un acuerdo parcial], viéndonos en la necesidad de acudir a la presente vía judicial respecto a los extremos de la controversia en los que se mantiene la discrepancia.

Acompaño como documento n.º [Nº] el requerimiento efectuado y como documento n.º [Nº] la contestación del demandado.

A los anteriores hechos les son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA.

Radicando la competencia genérica en el orden civil de la jurisdicción, detenta la competencia objetiva y funcional el Tribunal de Instancia, por aplicación de lo dispuesto en los arts. 85.1 LOPJ y 45 LEC.

Conforme a lo dispuesto en el ordinal 4.º del art. 52.1 LEC, es territorialmente competente el Tribunal de [SEDE] por ser el del lugar donde el finado D./Dña. [NOMBRE Y APELLIDOS DEL CAUSANTE] tuvo su último domicilio (ver nota (5)).

II.- CAPACIDAD Y LEGITIMACIÓN.

Tanto mi mandante D./Dña. [NOMBRE Y APELLIDOS] como los demandados, D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS], son personas físicas, mayores de edad, en pleno ejercicio de sus derechos civiles, por lo que tienen capacidad para ser parte y capacidad procesal ex arts. 6.1.1.º y 7.1 LEC.

Está legitimada activamente mi mandante, en base al testamento otorgado por D./Dña. [NOMBRE Y APELLIDOS DEL CAUSANTE], siendo pues titular del derecho subjetivo legítimo a la entrega del legado, y deberán ser tenidos como parte legítima pasiva los herederos y sucesores del testador, los demandados D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS].

III.- PROCEDIMIENTO.

La presente demanda deberá sustanciarse por las normas del juicio ordinario, a tenor de lo prevenido en los arts. 248 y 249.2 LEC, toda vez que el criterio de atribución preferente de la materia objeto del proceso resulta inaplicable, al carecer de especialidad típica la de éste, y cumplir entonces el criterio de cuantía, que rebasa con creces los quince mil euros.

IV.- CUANTÍA.

Levantando la carga prevenida en el art. 253.1 LEC, hacemos constar que la cuantía de esta demanda es de [IMPORTE EN LETRA] euros ([IMPORTE] €), que resulta del valor catastral de los bienes legados que se reclaman, por la utilización del criterio subsidiario de la regla 2.ª del art. 251 LEC.

V.- POSTULACIÓN Y DEFENSA.

Conforme a los arts. 23 y 31 LEC se formula esta demanda por medio de representación de Procurador/a de los Tribunales con poder para pleitos, y bajo dirección y firma de Letrado habilitado ante el Tribunal.

VI.- REQUISITOS FORMALES.

No aparecen, aparte de los requisitos genéricos de la demanda en juicio ordinario del art. 399 LEC, otros de carácter formal cuya falta, por el tipo de acción, invalidarían el proceso para pronunciarse sobre el fondo del asunto.

VII.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4.º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VIII.- FONDO DE LA CUESTIÓN CONTROVERTIDA.

Ejercita mi patrocinado/a acción personal ex testamento de reclamación de legado o actio legati, siendo de empleo el art. 885 del Código Civil, el cual dispone que el legatario no puede ocupar por su propia autoridad la cosa legada, sino que debe pedir su entrega y posesión al heredero o al albacea, cuando éste se halle autorizado para darla.

Acreditado que el objeto del legado es una cosa específica y determinada, propia del testador, en virtud del art. 882 del Código Civil el legatario adquiere la propiedad y los frutos de la cosa legada por el causante desde que el testador muere (ver nota (6)). Por todo ello corresponde a D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS] la entrega del legado sobre la finca en cuestión a favor de mi mandante, efectuando dicha entrega mediante la suscripción de la escritura pública de tradición de la finca legada; y la de sus frutos, resultando la atribución de frutos al legatario desde el fallecimiento del testador una consecuencia legal y necesaria de la reclamación de la cosa.

De dichos preceptos se desprende que, aunque el legatario tenga derecho al legado desde el momento de la muerte del testador y adquiera la propiedad de la cosa legada cuando es específica, determinada y propia del testador, ello no significa que no tenga que pedir su entrega al heredero o albacea autorizado, ya que su adquisición no se verifica de forma inmediata como en la herencia, sino de forma mediata a través del heredero. Como tiene declarado la jurisprudencia, en el legado que recae sobre cosa determinada, el legatario adquiere la propiedad de la cosa desde la muerte del testador y puede pedir a los herederos que se la entreguen, una vez formado el inventario y transcurrido el término para deliberar (cfr. art. 1.025 del Código Civil) (ver nota (7)).

IX.- COSTAS.

Se deben imponer a la parte demandada, por el criterio del vencimiento que establece para los declarativos en la instancia el art. 394.1 LEC.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito, con sus copias y documentos que se acompañan, se sirva admitir uno y otros; en su virtud, tener por interpuesta, en la representación que ostento, la presente demanda de juicio declarativo ordinario contra D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS], quienes deberán ser emplazados a fin de que puedan contestar, si a su derecho les conviene, y previos los oportunos trámites legales, en su día dicte sentencia por la que condene a dichos demandados a que entreguen a la parte actora la posesión de la finca de la que es propietaria en virtud de legado específico constituido a su favor por D./Dña. [NOMBRE Y APELLIDOS DEL CAUSANTE], consistente en la vivienda sita en [DOMICILIO DEL INMUEBLE], otorgando la correspondiente escritura pública de entrega de legados, bajo apercibimiento de que de no hacerlo se otorgará de oficio y a su costa; más los frutos y rentas que la misma haya producido desde el fallecimiento del testador, todo ello con expresa imposición de las costas procesales a la parte demandada.

Es justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a: [NOMBRE Y APELLIDOS, Nº DE COLEGIADO]

Firma del Procurador/a: [NOMBRE Y APELLIDOS]

NOTAS EXPLICATIVAS

(1) Para su acreditación, todos los poderes deben estar inscritos en el Registro Electrónico de Apoderamientos Judiciales (REAJ). Basta, para su acreditación, con la consulta automatizada de dicho Registro, que está a disposición de cualquier Letrado de la Administración de Justicia. No obstante, dado que el art. 24.2 LEC configura la certificación de dicha inscripción como vía subsidiaria de acreditación, para el caso de que el sistema no permita aquella consulta automatizada, se señala en el modelo que se acompaña certificación electrónica. El sistema permite emitir dicha certificación a quien inscribe el poder.

(2) En el régimen de Derecho civil común español el legatario tiene acción personal para reclamar su cumplimiento en toda clase de legados, solicitando la entrega y posesión de la cosa legada al heredero o albacea autorizado para darla (art. 885 del Código Civil), asegurable erga omnes mediante su anotación preventiva al amparo de los arts. 42.7.º y 47 y ss. de la Ley Hipotecaria, o la constitución forzosa de hipoteca si el legado es de rentas o pensiones periódicas.

Sólo en el caso de legado de cosa específica y determinada, propiedad del testador, o de derecho real en cosa de su herencia, al ser transmitidos desde la muerte del testador, a no ser que éste hubiere ordenado otra cosa, goza además el legatario de acción real reivindicatoria, sin perjuicio de las excepciones que el heredero pueda oponer al legatario, por deber reducirse el legado, en los casos de aceptación a beneficio de inventario, inoficiosidad, etc.; y puede igualmente, en el caso de que no haya herederos ni legatarios y nadie posea la cosa como dueño, inscribir su legado y pedir la posesión judicial del mismo por el procedimiento de la LEC o por el interdicto de adquirir; incluso algunos autores han señalado que la entrega de la cosa legada es una mera puesta en posesión, incluso realizable tácitamente, ya que no tiene el alcance de la tradición a que se refiere el art. 609 del Código Civil.

Por lo tanto, en materia de acciones es preciso distinguir el tipo de legado, ya sea la única acción ejercitable la acción personal ex testamento, como ocurre en los legados de cosa ajena o del heredero, o bien como acción complementaria, en los legados de cosa o derecho real del testador o constituido por éste sobre algún bien de la herencia a favor del legatario, con el fin de obtener la transferencia de la posesión, su formalización y la entrega de los frutos producidos por el bien legado desde la muerte del testador, si el testador no hubiera dispuesto otra cosa; pero no hay obstáculo a que se ejercite la acción reivindicatoria contra el heredero sólo en el caso de cosa específica y determinada, propiedad del testador, aunque la utilidad de la misma es muy inferior a la de la acción personal, pues para el ejercicio de ésta basta alegar el título sucesorio y la posesión del heredero por título que procede del causante, mientras que, prescrita la acción personal, el ejercicio de la acción reivindicatoria exige probar el dominio del causante.

También podrá el legatario de cosa específica ejercitar la acción reivindicatoria contra un tercero poseedor, pero el legado puede todavía ser objeto de reducción si infringe derechos legitimarios o de los acreedores hereditarios que no hubieran prescrito.

Respecto a los legatarios que no lo sean de cuota, es decir, los legatarios de cosa específica y determinada, al no ser titulares de una cuota abstracta de la herencia, de necesaria individualización, lo que sí carecen es de legitimación para pedir judicialmente la división de la herencia. Sólo cuando el heredero o el legatario adquieren un derecho abstracto que es preciso determinar pueden pedir judicialmente la división de la herencia, quedando equiparados en este aspecto por el mismo interés jurídico. Por el contrario, cuando el legatario no es titular de una cuota abstracta, sino que lo es de cosa determinada porque así aparece en la herencia, no está legitimado para promover la partición —naturalmente salvo que sea además heredero—, sin perjuicio de su derecho a solicitar la entrega y posesión de la cosa legada al heredero o al albacea autorizado para darla, o ejercitando al respecto la acción judicial que corresponda.

(3) El art. 155.3 LEC permite expresar varios domicilios del demandado (el que aparezca en el padrón municipal o conste oficialmente a estos efectos; el que aparezca en registro oficial o en publicaciones de colegios profesionales, si se trata de empresas o personas colegiadas; donde desarrolle su actividad profesional o laboral no ocasional; si es empresa mercantil, el domicilio de cualquiera de sus administradores, gerentes o apoderados; o, si es asociación que consta en registro oficial, el domicilio del presidente, miembro o gestor de la junta correspondiente). Cuando se señalen varios, se indicará el orden a seguir para la notificación, con vistas al éxito de la misma.

(4) El art. 155.3 LEC configura una obligación adicional del demandante, consistente en aportar cuantos datos sean de utilidad para localizar al demandado: número de identificación fiscal o de extranjeros, número de teléfono o de fax, dirección de correo electrónico o similares.

(5) Si se ejercitara acción reivindicatoria sobre bienes inmuebles, en el caso del legado de bienes determinados propiedad del testador, la competencia territorial se determinaría por la regla 1.ª del art. 52.1 LEC.

Si se tratara de reclamar la entrega de bienes muebles, o de ejercitar la acción personal para reclamar legados obligacionales, vendría en aplicación el art. 52.1.4.º LEC, que establece como regla general que en las cuestiones hereditarias será competente el tribunal del lugar en que el causante tuvo su último domicilio y, si lo hubiere tenido en país extranjero, el del lugar de su último domicilio en España, o donde tuviere la mayor parte de sus bienes, a elección del demandante.

(6) La jurisprudencia ha tratado de armonizar la aparente contradicción entre lo previsto en el art. 882 del Código Civil sobre la atribución de la propiedad al legatario, con las reglas sobre el pago de las deudas hereditarias, sobre el respeto a las legítimas y el orden de preferencia entre legados, estableciendo que el derecho que se concede al legatario en el art. 882 está subordinado a la liquidación de la masa hereditaria, a la circunstancia de que quepa en la parte de bienes de que el testador pueda disponer libremente o al orden que establece el art. 887 del Código Civil; y que la necesidad de pedir la entrega y posesión al heredero o albacea constituye un requisito complementario para la efectividad del legado.

En la doctrina científica, Albaladejo interpreta la subordinación de que habla la jurisprudencia en el sentido de que no alcanza a impedir que se produzca el efecto de la adquisición de la propiedad por el legatario, sino a facultar a los interesados a que después obtengan que se borren los efectos producidos, ya que el derecho del legitimario lesionado (la reductibilidad del legado por inoficioso cuando su atribución ponga en peligro la legítima, de lo que resulta la supeditación de la adquisición de la propiedad a que el legado quepa en la parte de bienes de que el testador pudo disponer libremente, art. 817 del Código Civil), o del acreedor hereditario (la eventual reducción o incluso ineficacia del legado por no alcanzar los restantes bienes de la herencia para pagar a los acreedores, dada la inequívoca supeditación de los legados a la liquidación de la herencia, que determinará si quedan bienes suficientes para aplicar a su pago, art. 1.027 del Código Civil), o del legatario preferente (por las reglas de prelación en el pago de los legados, art. 887 del Código Civil), sólo permitirían deshacer el traspaso de la propiedad de la cosa legada que recibió el legatario, o impedir la entrega del legado al legatario.

(7) Hay que tener en cuenta que, si bien, como matiza la STS de 25 de mayo de 1992, el legado de cosa específica no forma parte del caudal hereditario sobre el que han de versar las operaciones particionales, la situación cambia cuando en la herencia concurren, junto con el legatario o legatarios, herederos forzosos o legitimarios, con independencia de que ellos mismos tengan, también, esta misma consideración, porque en este caso el legado mismo está subordinado, o puede estarlo, al pago de las deudas y abono de las legítimas, y la dispersión de los bienes, si se permitiese sin más la entrega de las cosas específicas y determinadas legadas, perjudicaría la integridad de la masa hereditaria, pudiendo con ello impedir el pago de las deudas y la satisfacción de las legítimas que, como ocurría en vida del causante, supone especial garantía, conforme a lo previsto en el art. 1.911 del Código Civil, de los acreedores y de los legitimarios, y por esta razón tanto la jurisprudencia como —de forma prácticamente constante— la doctrina de la Dirección General de los Registros y del Notariado (hoy Dirección General de Seguridad Jurídica y Fe Pública) sostiene que debe preceder a la entrega del legado, de cualquier clase que sea, la liquidación y partición de herencia, pues ésa es la única forma de saber si se encuentran dentro de la cuota de la que puede disponer el testador por no perjudicar la legítima de los herederos forzosos, aunque la salvaguarda de los derechos de los acreedores y legitimarios no suponga la protección de un interés propio y específico de los herederos en general, razón por la cual el derecho conferido por el art. 882 del Código Civil está subordinado a la liquidación de la masa hereditaria, pues su vigencia depende de que quepa en la parte de bienes de que el testador puede disponer libremente.

Siguiendo dicha pauta, la doctrina de apelación no exige la previa partición de la herencia cuando haya un único heredero (SAP Tenerife, Sección 3.ª, de 24 de febrero de 2006, rec. 817/2005).

Por lo tanto, en su caso deberá acreditarse que se ha llevado a cabo la liquidación de la herencia, se han pagado las deudas y se han satisfecho las legítimas, pues es requisito para la válida y efectiva entrega del legado y puede ser motivo de oposición. La previa liquidación y adjudicación de la herencia en su totalidad, esto es, la determinación del haber hereditario, es necesaria pues sólo de este modo se puede saber si dichos legados se encuentran dentro de la cuota de que puede disponer el testador y no perjudican la legítima.
