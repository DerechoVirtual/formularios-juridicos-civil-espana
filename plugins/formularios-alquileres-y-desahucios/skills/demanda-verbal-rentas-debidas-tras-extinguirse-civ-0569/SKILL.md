---
name: demanda-verbal-rentas-debidas-tras-extinguirse-civ-0569
description: "Demanda verbal de rentas debidas tras extinguirse el arrendamiento hasta recuperar la posesión. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda verbal de rentas debidas tras extinguirse el arrendamiento hasta recuperar la posesión

> Formulario **CIV-0569** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Modelo de demanda de juicio verbal sobre reclamación de rentas adeudadas tras la extinción del contrato de arrendamiento hasta el momento de ser recuperada la posesión del inmueble por el arrendador.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda verbal de rentas debidas tras extinguirse el arrendamiento hasta recuperar la posesión» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda verbal de rentas debidas tras extinguirse el arrendamiento hasta recuperar la posesión” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:demanda-verbal-rentas-debidas-tras-extinguirse-civ-0569`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (7 veces)
- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] Nº DE DOCUMENTO (7 veces)
- [ ] FECHA (5 veces)
- [ ] Nº (5 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] DOMICILIO (2 veces)
- [ ] FECHAS (2 veces)
- [ ] SEDE (2 veces)
- [ ] CORREO ELECTRÓNICO
- [ ] LUGAR
- [ ] Nº DE COLEGIADO/A
- [ ] NÚMERO
- [ ] PORCENTAJE
- [ ] TELÉFONO

## Normas que cita el formulario

- art. 24.1 LEC
- art. 437.1 LEC
- art. 21.1 LOPJ
- art. 36.1 LEC
- art. 68 LEC
- art. 85.1 LOPJ
- art. 45 LEC
- art. 50.1 LEC
- art. 50 LEC
- art. 52.1.7.º LEC
- art. 250.1.1.º LEC
- art. 6.1.1.º LEC
- art. 7.1 LEC
- art. 23 LEC
- art. 253.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 1.555.1.º CC
- art. 1.561 CC
- art. 394 LEC

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
- Junto a «…o sentencia la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) A la hora de su acreditación, todos los poderes deben estar inscritos en el Registro Electrónico de Apoderamientos Judiciales (REAJ). Se supone que, para su acreditación, basta con la consulta (de dicho Registro) automatizada orientada al dato. Algo que está a disposición de cualquier Letrado de la Administración de Justicia. Sin embargo, dado que el art. 24.2 LEC, configura la certificación de dicha inscripción como vía subsidiaria de acreditación, para el caso de que el sistema no permita aquella consulta automatizada; se señala en el modelo que se acompaña certificación electrónica. El sistema permite emitir dicha certificación para quien inscribe el poder.

(2) Modelo aplicable a otras demandas de reclamación de rentas con contrato extinguido, como en el caso de resolución unilateral y anticipada por parte del arrendatario (véase SAP Málaga 368/2011 de 5 de julio, Rec. 912/2010: El contrato se celebró con una duración fija y determinada, que obligaba al arrendatario a permanecer en el arrendamiento durante todo el plazo pactado, de modo que, el incumplimiento de la obligación de permanencia en el arriendo por parte del arrendatario no solo le permitía al actor-arrendador reclamar una indemnización por daños y perjuicios derivada de una cláusula penal, sino que le autorizaba a reclamar el importe de todas las rentas previstas contractualmente, que, por el desistimiento unilateral del arrendatario, se convertían en rentas vencidas y debidas, siendo preciso resaltar que, en realidad, desde la firma del contrato, las rentas eran "rentas debidas", aunque su vencimiento se produjera por meses (...) En consecuencia, no estamos en presencia solamente de una reclamación de daños y perjuicios derivada de una posible cláusula penal, sino de una reclamación de rentas debidas desde la firma del contrato, por lo que, tratándose de "rentas debidas" el cauce procesal elegido para su reclamación es el correcto, es decir, el previsto en el artículo 250.1 de la LEC, que habla de "rentas y cantidades debidas").

(3) El art. 155.3 LEC permite fijar expresar varios domicilios del demandado (el que aparezca en el padrón municipal o conste oficialmente a estos efectos; el que aparezca en Registro oficial o en publicaciones de colegios profesionales, si se trata de empresas o personas colegiadas; donde desarrolle su actividad profesional o laboral no ocasional; si es empresa mercantil, el domicilio de cualquiera de sus administradores, gerentes, o apoderados; o, si es asociación que consta en registro oficial; el domicilio del presidente, miembro o gestor de la Junta correspondiente). Cuando se señalen varios, indicará el orden a seguir para la notificación, con vistas al éxito de la misma.

(4) El art. 155.3 LEC configura una obligación adicional del demandante, consistente en aportar cuantos datos sean de utilidad para localizar al demandado: número de identificación fiscal o de extranjeros, nº [Nº] de teléfono o de fax, dirección de correo electrónico, o similares.

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], representación que acredito mediante escritura de poder otorgada a mi favor (existen tres posibilidades para otorgar el apoderamiento al Procurador de los Tribunales, conforme dispone el art. 24.1 LEC)

[OPCIONAL — opción en función de cómo se haya otorgado el poder]

[ELEGIR UNA OPCIÓN: Si el poder se otorga a través de la sede judicial electrónica / Si el poder se otorga mediante comparecencia apud acta / Si el poder se otorga ante Notario]

bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS], abogado/a en ejercicio, con despacho profesional abierto en [LOCALIDAD], colegiado nº [Nº DE COLEGIADO/A] del Ilustre Colegio de la Abogacía de [LOCALIDAD], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que mediante el presente escrito vengo a formular DEMANDA DE JUICIO VERBAL SOBRE RECLAMACIÓN DE CANTIDAD, contra D./Dña. [NOMBRE Y APELLIDOS], con domicilio, primero en [DOMICILIO]; y segundo, el domicilio laboral en [DOMICILIO]); con email [CORREO ELECTRÓNICO]; y con número de teléfono móvil [TELÉFONO].

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa, e, incluso, en una eventual fase de ejecución por medios telemáticos, en términos del art. 399.1 II en relación al art. 437.1, ambos LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y nº [Nº] de teléfono:

Todo ello de conformidad con los siguientes hechos y fundamentos de derecho:

HECHOS

PRIMERO.- Mi mandante, D./Dña. [NOMBRE Y APELLIDOS], es propietario del local sito en [LOCALIDAD] Se acompaña el título de propiedad -escritura de compraventa- como documento n.º [Nº DE DOCUMENTO].

SEGUNDO.- El mencionado local fue arrendado al hoy demandado en fecha [FECHA], concertándose un plazo de duración del arrendamiento de [Nº] años y una renta mensual de [IMPORTE] euros, a pagar en mensualidades anticipadas de [IMPORTE] euros, más IVA, revisable anualmente en función del índice general del coste de la vida publicado por el Instituto Nacional de Estadística. Además de la renta, el arrendatario se obligaba a satisfacer a la arrendadora los gastos de comunidad de propietarios en la parte que correspondiese al local arrendado en proporción a su cuota de participación en los elementos comunes del edificio, que era del [PORCENTAJE] %, estipulándose que la arrendadora comunicaría al arrendatario trimestralmente el importe de los referidos gastos, obligándose este último a hacerlos efectivos en el plazo máximo de los cinco días siguientes a dicha comunicación.

Las circunstancias mencionadas constan en el contrato de arrendamiento y condiciones anejas al mismo que se aporta como documento n.º [Nº DE DOCUMENTO].

TERCERO.- Extinguido el plazo del arrendamiento, el propietario del local arrendado, D./Dña. [NOMBRE Y APELLIDOS], promovió proceso para recuperar la posesión del inmueble, que se tramitó como autos n.º [NÚMERO] de juicio verbal de desahucio, dictando sentencia la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº] el [FECHA], declarando resuelto el contrato de arrendamiento y condenando al demandado-arrendatario a desalojar el local, dejándolo libres y expedito a disposición del actor, habiéndose verificado el lanzamiento el

Se aportan como documentos númerosy testimonio de la sentencia y de la diligencia de lanzamiento obrantes en los referenciados autos.

CUARTO.- Mi representado, propietaria del local, reclama del demandado las rentas debidas con el incremento y las cantidades pactadas hasta la fecha de la sentencia recaída en juicio de desahucio, y una indemnización por el tiempo que estuvo ocupando el local una vez extinguido el contrato de arrendamiento desde la fecha de la mencionada sentencia hasta el momento del lanzamiento, por tanto del [Nº] al [Nº], y la cuantificación de la indemnización se fija en las cantidades mensuales que venía satisfaciendo el demandado por renta y gastos de la comunidad de propietarios, a los que se añade el correspondiente IVA y se deducen [IMPORTE] euros de la fianza entregada en su día, con un resultado total objeto de reclamación de [IMPORTE] euros, según liquidación practicada que se aporta como documento n.º [Nº DE DOCUMENTO].

QUINTO.- La parte actora manifiesta que, previo a la presentación de la presente demanda, se han llevaron a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad, y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria; incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, mi representado envío un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por el demandado por el mismo medio, rechazando el acuerdo/ habiendo sido solo posible un acuerdo parcial, viéndonos en la necesidad de acudir a la presente vía judicial, respecto a los extremos de la controversia en los que se mantiene la discrepancia.

Acompaño como documento nº [Nº DE DOCUMENTO], el requerimiento efectuado y como documento nº [Nº DE DOCUMENTO], la contestación del demandado.

La parte actora manifiesta que, previo a la presentación de la presente demanda, se han llevaron a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad, y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria; incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, mi representado envío un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por el demandado por el mismo medio, rechazando el acuerdo/ habiendo sido solo posible un acuerdo parcial, viéndonos en la necesidad de acudir a la presente vía judicial, respecto a los extremos de la controversia en los que se mantiene la discrepancia.

Acompaño como documento nº [Nº DE DOCUMENTO], el requerimiento efectuado y como documento nº [Nº DE DOCUMENTO], la contestación del demandado.

A los anteriores hechos son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA.

La jurisdicción ordinaria es la única competente para el conocimiento de los juicios que se susciten en territorio español con arreglo a lo establecido en los tratados y convenios internacionales en los que España sea parte, en las normas de la Unión Europea y en las leyes españolas (art. 21.1 LOPJ y art. 36.1 LEC).

La competencia objetiva corresponde a la Sección Civil del Tribunal de Instancia que por reparto corresponda (art. 68 LEC) de los de esta ciudad, según lo dispuesto en el art. 85.1 LOPJ y art. 45 LEC, así como la territorial con arreglo al art. 50.1 LEC, por ser el lugar del domicilio del demandado, al no existir norma de carácter especial que atribuya la competencia a otro tribunal (se considera que, puesto que el contrato de arrendamiento se habrá extinguido, la regla de determinación de la competencia territorial es la contenida en el art. 50 LEC, y no la del art. 52.1.7.º LEC).

II.- PROCEDIMIENTO.

La presente demanda deberá sustanciarse por las normas del juicio verbal, a tenor de lo prevenido en el art. 250.1.1.º LEC.

III.- CAPACIDAD.

Demandante y demandado, personas físicas, tienen capacidad para ser parte (art. 6.1.1.º LEC), titular de facultades y cargas del proceso, y asimismo plena capacidad procesal, al ser mayores de edad, sin limitación de ejercicio válido de derechos civiles, o para comparecer en juicio, en términos del art. 7.1 LEC, pretendiendo el actor y siendo pretendido el demandado, en sus respectivos nombres y derechos.

IV.- LEGITIMACIÓN.

Corresponde la legitimación activa al demandante por ser parte en el contrato suscrito y haber cumplido sus obligaciones contractuales como arrendadora, y la pasiva la tiene el demandado en cuanto ocupa la posición de contraparte contractual y ha venido realizando el acto contradictorio a la esencial obligación asumida, de impago de las rentas.

V.- POSTULACIÓN Y DEFENSA.

Conforme a los arts. 23 y 31 LEC se formula esta demanda por medio de Procurador con poder notarial para pleitos, y con dirección y firma de Letrado habilitado.

VI.- CUANTIA.

Por así disponerlo el art. 253.1 LEC, se pone de manifiesto que la cuantía de esta demanda es de [IMPORTE] euros ( [IMPORTE] €), con arreglo a la regla 1.ª del art. 251 de dicha Ley, al reclamarse una cantidad de dinero determinada.

VII. CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 de la LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VIII.- FONDO DEL ASUNTO.

La reclamación de cantidad que se formula tiene su apoyo legal en el art. 1.555.1.º CCiv, en cuanto a la cantidad reclamada en concepto de rentas, por cuanto mi mandante cumplió con su obligación de poner a la demandada en posesión del bien arrendado, y no así la demandada, no satisfaciendo las rentas correspondientes

Las otras cantidades que se reclaman no integran, propiamente, rentas del contrato, sino más bien una indemnización por la ocupación indebida del local hasta el efectivo desalojo y la puesta a disposición del local al arrendador, pues el contrato ya se había extinguido como consecuencia de la resolución decretada judicialmente, de manera que tales cantidades tienen consideración de indemnización (aunque su monto se determine con referencia al importe de las rentas), más que rentas propiamente dichas del contrato extinguido.

Así, una vez que el contrato ha sido resuelto por la sentencia de desahucio, cuando es firme, desaparece el concepto "renta" al no existir arrendamiento del que pueda derivarse. Ahora bien, si el arrendatario no atiende el requerimiento que le hace la propia sentencia y continúa ocupando el local durante un tiempo más o menos prolongado hasta devolver su posesión o ser lanzado judicialmente, está obteniendo un beneficio o ganancia contraria a derecho con la detentación del inmueble, mientras que el dueño, antiguo arrendador, sufre un quebranto patrimonial y un real empobrecimiento por no tener el local o vivienda a su disposición. No cabe duda, por tanto, que el perjuicio generado por la conducta del arrendatario debe ser objeto de satisfacción.

Así lo entiende la jurisprudencia cuando declara: "Una cosa es que la sentencia del Juzgado que decretó el desahucio tuviera fecha de noviembre de 1979, resolviendo el contrato, y otra que el arrendatario o subarrendatario deba abonar las rentas devengadas por la arrendadora hasta la efectiva entrega del local, momento hasta el cual el subarrendatario usó y disfrutó del mismo, que no fue sino la fecha de enero de 1980, según terminante apreciación de la sentencia ahora recurrida y que por ello condenó al pago incluso de esa mensualidad, ya que la opinión o tesis contraria llevaría a la conclusión de un claro enriquecimiento injusto (uso sin contraprestación), enmarcada también en un manifiesto abuso de derecho procesal en el caso por ejemplo de una entrega tardía necesitada de un lanzamiento judicial" [STS 30 de noviembre 1984]. "El pago de las rentas es la simple consecuencia de la posesión, aun prolongada tras la extinción del arriendo, como ha tenido múltiples ocasiones de declarar esta Sala y como incluso se desprende de los preceptos de la Ley de enjuiciamiento civil, cuyos arts. 1566 y 1567 obligan a los recurrentes a acreditar que ha satisfecho las rentas vencidas so pena de tener por firme la sentencia y en parecidos términos el art. 148 de la Ley de arrendamientos urbanos. El pago, pues, es contraprestación a la tenencia de la cosa y no prueba de la subsistencia del término de vigencia" [STS 17 de marzo 1992].

Es también la postura mayoritaria asumida por la doctrina de apelación, entre otras, SAP Granada 267/2000 de 5 de abril, Rec. 917/1999, o la más reciente, SAP Cádiz 189/2011 de 29 de septiembre, Rec. 237/2011, razonándose en esta última resolución "la obligación del arrendatario de abonar el precio correspondiente a las rentas del tiempo durante el que ocupó el local arrendado, y ello porque el art. 1.561 CCiv le exige devolver la cosa arrendada al concluir el arriendo. Esto significa que será de su cargo el pago de las rentas devengadas hasta el instante de la devolución y ello aun en el caso de que se haya extinguido legalmente el contrato locatorio. Y dicho pago se debe producir bien por el concepto de indemnización, pues está privando al propietario del uso y disfrute de la misma y por la posesión que está disfrutando, bien en concepto de renta como contrapartida a esa posesión que sigue manteniendo como consecuencia del extinguido contrato de arrendamiento".

IX.- INTERESES.

Deben reconocerse a mi patrocinada los intereses moratorios de los arts. 1.100, 1.101 y 1.108 CCiv en que el deudor que incurra en mora deberá pagar los intereses que correspondan y que la indemnización de daños y perjuicios no habiendo pacto de contrario consistirá en el interés legal.

X.- COSTAS.

Conforme al art. 394 LEC las costas del procedimiento habrán de imponerse al demandado.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que, habiendo por presentado este escrito de demanda, con los documentos y las copias que se acompañan, se sirva admitirlos, y me tenga por comparecido en la representación que ostento, entendiéndose conmigo las sucesivas diligencias, y por promovido juicio verbal contra D./Dña. [NOMBRE Y APELLIDOS], acuerde darle traslado para que comparezca y la conteste en su interés, y seguido que sea por sus legales trámites, se venga a dictar sentencia por la que se condene a la parte demandada a abonar a mi representado la cantidad de [IMPORTE] euros, más sus intereses legales desde la interposición de la demanda, así como al pago de las costas causadas.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a
