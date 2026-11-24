---
name: demanda-juicio-ordinario-danos-trafico-contra-civ-0825
description: "Demanda de juicio ordinario por daños de tráfico contra conductor, propietario y aseguradora. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio ordinario por daños de tráfico contra conductor, propietario y aseguradora

> Formulario **CIV-0825** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario en reclamación de indemnización por daños en las personas y en los bienes derivados de la circulación de vehículos de motor, interpuesta por el conductor y por el propietario del vehículo perjudicado frente al otro conductor, el propietario de su vehículo y la aseguradora (acción directa del art. 76 LCS), con reclamación de intereses del art. 20 LCS.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio ordinario por daños de tráfico contra conductor, propietario y aseguradora» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio ordinario por daños de tráfico contra conductor, propietario y aseguradora” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-juicio-ordinario-danos-trafico-contra-civ-0825`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (16 veces)
- [ ] Nº (15 veces)
- [ ] Nº DE DOCUMENTO (14 veces)
- [ ] NOMBRE Y APELLIDOS DEL CONDUCTOR DEMANDANTE (12 veces)
- [ ] DENOMINACIÓN SOCIAL DE LA EMPRESA PROPIETARIA DEL VEHÍCULO (10 veces)
- [ ] AÑO (8 veces)
- [ ] LOCALIDAD (8 veces)
- [ ] NOMBRE Y APELLIDOS DEL CONDUCTOR DEMANDADO (7 veces)
- [ ] DÍA (6 veces)
- [ ] MES (6 veces)
- [ ] DENOMINACIÓN SOCIAL DE LA ASEGURADORA (5 veces)
- [ ] DENOMINACIÓN SOCIAL DE LA EMPRESA PROPIETARIA DEL VEHÍCULO CAUSANTE (5 veces)
- [ ] CALLE Y NÚMERO (4 veces)
- [ ] MARCA Y MODELO (4 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] Nº/AÑO (3 veces)
- [ ] MATRÍCULA (2 veces)
- [ ] SEDE (2 veces)
- [ ] CONCESIONARIO
- [ ] CUERPO POLICIAL QUE INSTRUYÓ EL ATESTADO
- [ ] DENOMINACIÓN
- [ ] DIRECCIÓN
- [ ] FECHA
- [ ] FECHAS
- [ ] MARCA
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] NOMBRES
- [ ] Nº DE INSCRIPCIÓN
- [ ] Nº DE PÓLIZA
- [ ] PORCENTAJE
- [ ] PUNTO KILOMÉTRICO
- [ ] TIPO DE VEHÍCULO
- [ ] VÍA

## Normas que cita el formulario

- art. 85 LOPJ
- art. 52.1.9.º LEC
- art. 6.1.1.º LEC
- art. 7.1 LEC
- art. 6.1.3.º LEC
- art. 7.4 LEC
- art. 10 LEC
- art. 76 Ley 50/1980
- art. 253.1 LEC
- art. 251 LEC
- art. 5 Ley Orgánica 1/2025
- art. 1.089 Código Civil
- art. 1.902 Código Civil
- art. 1.903 Código Civil
- art. 76 LCS
- art. 1.100 Código Civil
- art. 20.4.ª LCS
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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…amente contra el conductor y el propietario del vehículo causante del accidente.»: el apartado VIII.2 (cuantificación de las lesiones) sigue la estructura del antiguo baremo de la Ley 30/1995 (tablas III, IV, V y VI). Para accidentes ocurridos desde el 1 de enero de 2016 debe adaptarse al sistema de valoración vigente tras la Ley 35/2015 (texto refundido de la Ley sobre responsabilidad civil y seguro en la circulación de vehículos a motor, RDLeg 8/2004: comprobar los artículos y tablas aplicables, así como la numeración actual de los preceptos citados sobre intereses de demora y oferta motivada).
- Junto a «…mora y oferta motivada).] A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

NOTAS DE USO: Si la cuantía de la demanda supera los 15.000 euros se sigue el cauce del juicio ordinario y si es inferior el del juicio verbal. Presentada la demanda se examinará por el Letrado de la Administración de Justicia, que dictará decreto admitiéndola a trámite y dando traslado a los demandados para que contesten en veinte días. No obstante, el LAJ dará cuenta al Tribunal para que resuelva por auto sobre la admisión cuando estime falta de jurisdicción o competencia o que la demanda adolece de defectos formales y no se hubiesen subsanado por el actor en el plazo que se le concediera. La reclamación de cuantía superior a 2.000 euros requiere la intervención de Abogado y Procurador. Los documentos a los que tenga acceso el actor y, en su caso, el informe pericial, deben presentarse con la demanda. Es imprescindible que en el informe pericial se recojan los requisitos incluidos en el artículo 335.2 de la LEC.

La Ley de Contrato de Seguro regula la reclamación de intereses de la siguiente manera. Se entiende que el asegurador incurre en mora cuando no hubiere cumplido su prestación en el plazo de tres meses desde la producción del siniestro o no hubiere procedido al pago del importe mínimo de lo que pueda deber dentro de los cuarenta días a partir de la recepción de la declaración del siniestro. La indemnización por mora se impondrá de oficio por el juzgador y consistirá en el pago de un interés anual igual al del interés legal del dinero vigente en el momento en que se devengue incrementado en el 50 por 100. Transcurridos dos años desde la producción del siniestro el interés anual no podrá ser inferior al 20 por 100. Hay que tener en cuenta que la STS, Sala Primera, 251/2007, de 1 de marzo, ha interpretado este polémico precepto sentando la doctrina jurisprudencial de que el interés de demora debe calcularse durante los dos primeros años siguientes al siniestro al tipo legal más el 50%, y a partir de ese momento, al tipo del 20%, si aquél no resulta superior. El término inicial del cómputo de los intereses es la fecha del siniestro y el final, en los casos de falta de pago del importe mínimo de lo que el asegurador pueda deber, el día en que comiencen a devengarse intereses por el importe total de la indemnización, salvo que con anterioridad sea pagado por el asegurador el importe mínimo, en cuyo caso será término final la fecha de este pago. Será término final del plazo de la obligación de abono de intereses de demora por la aseguradora en los restantes supuestos el día en que efectivamente satisfaga la indemnización mediante pago, reparación o reposición al asegurado, beneficiario o perjudicado. No habrá lugar a la indemnización por mora del asegurador si la falta de satisfacción de la indemnización o pago del importe mínimo está fundada en una causa justificada o que no le fuere imputable.

La Ley 18/2011, de 5 de julio, regula el expediente judicial electrónico, el documento judicial electrónico, las copias y archivos de documentos electrónicos y el registro electrónico. La Ley 35/2015 modificó el texto refundido de la Ley sobre responsabilidad civil y seguro en la circulación de vehículos a motor dando una nueva redacción al artículo 7. Tras su entrada en vigor se exige con carácter previo a la interposición de la demanda que se dirija reclamación extrajudicial a la aseguradora, suponiendo la no aportación de los documentos que acrediten la presentación de la reclamación al asegurador y la oferta o respuesta motivada, si se hubiere emitido por el asegurador, causa de inadmisión de la demanda. Este requisito se aplica a los accidentes acaecidos con posterioridad al 1 de enero de 2016, fecha de entrada en vigor de la reforma, como vienen declarando varias Audiencias, de las que a título de ejemplo se cita el Auto de la AP de Madrid, Sección 9.ª, n.º 199/2017. Sin embargo, no está claro que este requisito previo sea exigible cuando la demanda en reclamación de daños materiales se dirija acumuladamente contra el conductor y el propietario del vehículo causante del accidente.


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

Q.P.T.C.

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS DEL CONDUCTOR DEMANDANTE] y de [DENOMINACIÓN SOCIAL DE LA EMPRESA PROPIETARIA DEL VEHÍCULO], y a cuya justificación aporto escritura de poder inscrito en el Registro Electrónico de Apoderamientos Judiciales con el n.º [Nº DE INSCRIPCIÓN] y que se puede acreditar mediante consulta automatizada orientada al dato, por parte del órgano judicial al cual tengo el honor de dirigirme, acompañándose certificación electrónica del Registro Electrónico de Apoderamientos Judiciales como documento n.º [Nº DE DOCUMENTO] por si no es posible la consulta automatizada, y con la asistencia del/de la Letrado/a D./Dña. [NOMBRE Y APELLIDOS], del Ilustre Colegio de Abogados de [LOCALIDAD], cuyo despacho está abierto en esta población, calle [CALLE Y NÚMERO], ante la Sección Civil del Tribunal de Instancia que por turno de reparto corresponda, comparezco y, como mejor proceda en Derecho, DIGO:

Que siguiendo expresas instrucciones de quienes ostento representación, por medio del presente escrito formulo demanda de

JUICIO ORDINARIO

que dirijo contra:

- D./Dña. [NOMBRE Y APELLIDOS DEL CONDUCTOR DEMANDADO], mayor de edad, vecino de [LOCALIDAD], domiciliado en la calle [CALLE Y NÚMERO], cuyas demás circunstancias personales nos son desconocidas.

- [DENOMINACIÓN SOCIAL DE LA EMPRESA PROPIETARIA DEL VEHÍCULO CAUSANTE], con domicilio en [LOCALIDAD], calle [CALLE Y NÚMERO].

- La aseguradora [DENOMINACIÓN SOCIAL DE LA ASEGURADORA], para ser citada en su oficina de [LOCALIDAD], calle [CALLE Y NÚMERO].

La demanda se basa en los siguientes

HECHOS

PRIMERO.- En fecha [DÍA] de [MES] de [AÑO], mi representada [DENOMINACIÓN SOCIAL DE LA EMPRESA PROPIETARIA DEL VEHÍCULO] era titular de un vehículo [TIPO DE VEHÍCULO] marca [MARCA Y MODELO], matrícula [MATRÍCULA], conforme acredito mediante fotocopia del permiso de circulación que aportamos (documento número [Nº DE DOCUMENTO]), designando los Libros del Registro de Bienes Muebles y archivo de la Jefatura Provincial de Tráfico.

SEGUNDO.- [DENOMINACIÓN SOCIAL DE LA EMPRESA PROPIETARIA DEL VEHÍCULO] es titular de una empresa de arrendamiento de vehículos industriales, y mi otro poderdante, D./Dña. [NOMBRE Y APELLIDOS DEL CONDUCTOR DEMANDANTE], conducía el vehículo de la misma que resultó siniestrado. Se acompaña a su demostración el contrato de arrendamiento de cosas como documento número [Nº DE DOCUMENTO].

TERCERO.- El citado día [DÍA] de [MES] de [AÑO], y expresamente autorizado para ello mediante el referido contrato, conducía el vehículo antes reseñado D./Dña. [NOMBRE Y APELLIDOS DEL CONDUCTOR DEMANDANTE] por la [VÍA] y en dirección a [LOCALIDAD], por el carril de la derecha, cuando a la altura del p.k. [PUNTO KILOMÉTRICO], en paralelo, por el carril de su izquierda, conducía el vehículo marca [MARCA Y MODELO], matrícula [MATRÍCULA], el codemandado D./Dña. [NOMBRE Y APELLIDOS DEL CONDUCTOR DEMANDADO], cuando inició el adelantamiento del vehículo de mi patrocinado D./Dña. [NOMBRE Y APELLIDOS DEL CONDUCTOR DEMANDANTE] y, haciéndolo de forma distraída y a excesiva velocidad, se aproximó en exceso, colisionando por alcance en la furgoneta con tal intensidad que provocaron al conductor de ésta, mi mandante, la pérdida de control, dando una vuelta de campana, para posteriormente quedar detenido a unos [Nº] metros, volcado sobre su lateral izquierdo, transversalmente al eje de la calzada y con los neumáticos orientados hacia [DIRECCIÓN].

CUARTO.- El turismo [MARCA Y MODELO], que conducía D./Dña. [NOMBRE Y APELLIDOS DEL CONDUCTOR DEMANDADO], es propiedad de [DENOMINACIÓN SOCIAL DE LA EMPRESA PROPIETARIA DEL VEHÍCULO CAUSANTE], para la que prestaba sus servicios el primero como trabajador por cuenta ajena, y se encontraba asegurado en la fecha del siniestro en la aseguradora también demandada [DENOMINACIÓN SOCIAL DE LA ASEGURADORA], con póliza número [Nº DE PÓLIZA]. A la acreditación de estos extremos se aporta el testimonio del resultado de las diligencias preliminares n.º [Nº/AÑO] llevadas a efecto en la Sección Civil del Tribunal de Instancia n.º [Nº] de esta ciudad (documento número [Nº DE DOCUMENTO]).

QUINTO.- D./Dña. [NOMBRE Y APELLIDOS DEL CONDUCTOR DEMANDANTE] fue evacuado de urgencia del lugar del accidente al Hospital de [LOCALIDAD], donde fue intervenido de herida abierta en cabeza, y permaneció ingresado, causando posteriormente baja laboral.

Presenta en definitiva las siguientes lesiones a la fecha en que es dado de alta, [DÍA] de [MES] de [AÑO]:

- Esguince cervical.

- Traumatismo en mano izquierda.

- Heridas en la lengua.

- Traumatismo cráneo-encefálico de grado II.

[Sustituir las lesiones por las que correspondan al caso.]

Para su sanidad, además de la asistencia hospitalaria de [Nº] días, precisó D./Dña. [NOMBRE Y APELLIDOS DEL CONDUCTOR DEMANDANTE] tratamiento médico posterior consistente en collarín cervical, férula y cabestrillo en mano izquierda, sutura de las heridas, y tratamiento rehabilitador, curando en [Nº] días, incapacitado para sus ocupaciones habituales.

Permanecen como secuelas cervicalgia irradiada a brazo derecho, cefaleas y mareos y lumbalgia, ambos estables en el tiempo a la vista de la persistencia en su sintomatología; zonas de insensibilidad linguales, y síndrome depresivo susceptible de desaparecer con el paso del tiempo.

A efectos probatorios se acompañan como documentos números [Nº] a [Nº], el informe de asistencia en el Servicio de Urgencias del Hospital [DENOMINACIÓN] y el informe de alta del mismo, partes de baja y alta de Incapacidad Temporal, certificados expedidos por los Doctores [NOMBRES], que le han venido asistiendo periódicamente a D./Dña. [NOMBRE Y APELLIDOS DEL CONDUCTOR DEMANDANTE]; e igualmente se acompaña dictamen de valoración de daño corporal emitido por perito designado por esta parte y que justifica la reclamación pecuniaria que se formula.

Para el supuesto de que fueren impugnados los documentos aportados por esta parte relativos a asistencia prestada por Centros Sanitarios Públicos, se solicita se remita oficio a fin de que se proceda al cotejo o comprobación de los aportados con los que obren en los correspondientes archivos.

SEXTO.- El vehículo de [DENOMINACIÓN SOCIAL DE LA EMPRESA PROPIETARIA DEL VEHÍCULO], que tuvo que ser retirado de la calzada mediante grúa, sufrió graves daños, siendo considerado como siniestro total, según informe pericial, el cual calcula el precio medio del mercado a la fecha del siniestro, y que se acompaña como documento número [Nº DE DOCUMENTO], causando posteriormente la furgoneta baja total según la nota informativa de la Jefatura Provincial de Tráfico que se acompaña como documento número [Nº DE DOCUMENTO].

A los oportunos efectos probatorios se acompaña la factura de los servicios de grúa (documento número [Nº DE DOCUMENTO]).

Además, ante la pérdida total del vehículo, mi representado hubo de adquirir otro, faltándole desde la fecha del accidente y hasta el día [DÍA] de [MES] de [AÑO], como se acredita con factura que hace documento número [Nº DE DOCUMENTO] de los adjuntados a este escrito.

SÉPTIMO.- Después de la ocurrencia del siniestro fue instruido atestado por [CUERPO POLICIAL QUE INSTRUYÓ EL ATESTADO], registrado como n.º [Nº/AÑO], y cuyos archivos designamos, con citación contraria, dado que no se ha facilitado a esta parte copia del mismo, siendo preciso a tal fin remisión de oficio por el Tribunal, el que se interesa se entregue al Procurador/a suscrito, a fin de cuidar de su cumplimentación, en la cual intervendrá.

Igualmente se incoaron, en virtud de parte facultativo de lesiones, las Diligencias Previas n.º [Nº/AÑO] por la Sección de Instrucción del Tribunal de Instancia de [SEDE], las que fueron sobreseídas por no constar la formulación de denuncia en el plazo legalmente establecido. Se acompaña como documento número [Nº DE DOCUMENTO] testimonio de las referidas actuaciones.

OCTAVO.- La parte actora manifiesta que, previo a la presentación de la presente demanda, se han llevado a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad, y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria; incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución. Finalmente, mi representado envió un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito. Mis patrocinados han tenido que acudir a la presente vía judicial civil, por no haber sido atendida su reclamación amistosa, a cuya prueba se acompaña el burofax enviado a los codemandados (documento número [Nº DE DOCUMENTO]) reclamando las cantidades que en esta demanda se solicitan, con especificación de partidas de indemnización y su cuantificación, sin que en momento alguno hayan atendido al pago o recibido respuesta motivada de [DENOMINACIÓN SOCIAL DE LA ASEGURADORA], y habiendo transcurrido en exceso el plazo de tres meses desde la indicada reclamación, sin que se haya pagado o consignado cantidad alguna.

FUNDAMENTOS DE DERECHO

I JURISDICCIÓN Y COMPETENCIA

Los arts. 85 LOPJ y 45 LEC designan a las secciones civiles de los tribunales de instancia como los órganos con la competencia específica, objetiva y funcional, para resolver estos pleitos, y el art. 52.1.9.º LEC fija la competencia territorial para juicio en que se pida indemnización de los daños y perjuicios derivados de la circulación de vehículos de motor en el tribunal del lugar en que se causaron los daños.

II PROCEDIMIENTO

En aplicación de los arts. 248.3 y 249.2 LEC, y en atención a la cuantía del objeto litigioso, que supera los 15.000 euros, este pleito se tramitará por las normas del proceso declarativo llamado juicio ordinario.

III CAPACIDAD

Conforme al art. 6.1.1.º LEC tienen capacidad para ser parte las personas físicas, y a tenor del art. 7.1 LEC detentan capacidad de obrar procesal, en tanto que mayores de edad y en pleno ejercicio de sus derechos civiles.

La capacidad para ser parte de las personas jurídicas se reconoce en el art. 6.1.3.º LEC, cuya personalidad deriva de su constitución en escritura pública inscrita en el Registro Mercantil, debiendo comparecer en juicio por medio de sus representantes legales (art. 7.4 LEC).

IV LEGITIMACIÓN

El art. 10 LEC legitima para comparecer y actuar en juicio a los titulares de la relación jurídica o del objeto litigioso, lo cual es legitimación ordinaria, que en el caso de autos detentan la activa originaria los demandantes, en cuanto titulares del derecho subjetivo patrimonial a la reparación de los daños inferidos a la persona de D./Dña. [NOMBRE Y APELLIDOS DEL CONDUCTOR DEMANDANTE], y al patrimonio de [DENOMINACIÓN SOCIAL DE LA EMPRESA PROPIETARIA DEL VEHÍCULO], así como la pasiva originaria, los demandados, incumplidores de la correlativa obligación resarcitoria, D./Dña. [NOMBRE Y APELLIDOS DEL CONDUCTOR DEMANDADO] como agente del daño, [DENOMINACIÓN SOCIAL DE LA EMPRESA PROPIETARIA DEL VEHÍCULO CAUSANTE], en cuanto propietaria del vehículo y empleadora de ese conductor, y [DENOMINACIÓN SOCIAL DE LA ASEGURADORA], por virtud del contrato de seguro, en lo que es la acción directa recogida en el art. 76 de la Ley 50/1980, de Contrato de Seguro (LCS).

V POSTULACIÓN

En aplicación de los arts. 23.1 y 31.1 LEC, las partes comparecerán representadas por Procurador/a de los Tribunales y asistidas por Letrado en ejercicio, ambos habilitados ante el Tribunal.

VI CUANTÍA

Cumpliendo la exigencia del art. 253.1 LEC, se cifra la cuantía de la demanda en la cantidad de [IMPORTE] euros, conforme a la regla 1.ª del art. 251 LEC.

VII CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4.º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VIII FONDO DEL ASUNTO

VIII.1

Mis mandantes ejercen una acción que nace de reconocer el art. 1.089 del Código Civil entre las fuentes de las obligaciones las acciones y omisiones ilícitas o en que intervenga cualquier género de culpa o negligencia, y para estas últimas, prevenir el art. 1.093 la regulación contenida en el capítulo II del título XVI del libro IV del mismo, es decir, en los arts. 1.902 y ss., siendo que este art. 1.902 del Código Civil establece que el que por acción u omisión causa un daño a otro interviniendo culpa o negligencia, está obligado a reparar el daño causado, trasunto normativo de la antigua regla jurídica del «alterum non laedere», en su vertiente clásica de la responsabilidad civil por actos propios.

La acción se dirige contra:

a) El conductor imprudente, D./Dña. [NOMBRE Y APELLIDOS DEL CONDUCTOR DEMANDADO].

b) La sociedad dueña del vehículo, [DENOMINACIÓN SOCIAL DE LA EMPRESA PROPIETARIA DEL VEHÍCULO CAUSANTE], por la vinculación con aquél por la relación de trabajo en la que es empleador, en términos que regula el art. 1.903 del Código Civil.

c) La compañía aseguradora de la conducción de éste, deudora solidaria de la indemnidad, como autoriza el art. 76 LCS.

En el plano de los daños en las personas, la normativa del seguro de responsabilidad civil del automóvil de suscripción obligatoria, modificada y rebautizada como Ley sobre Responsabilidad Civil y Seguro en la Circulación de Vehículos a Motor por la Ley 30/1995, de 8 de noviembre, y actualmente recogida en el texto refundido aprobado por Real Decreto Legislativo 8/2004, de 29 de octubre (TRLRCSCVM), aísla un campo de relaciones sociales, la circulación de vehículos de motor, en que la responsabilidad civil no sigue un régimen subjetivo, como la tradición de la precitada batería normativa, y aunque no llega a suplantarse absolutamente la culpabilidad por causalidad, el elemento que atribuye la obligación de responder es la creación del riesgo (art. 1.1, párrafo 1.º TRLRCSCVM), y las causas de exoneración se ciñen a la culpa exclusiva de la víctima o la fuerza mayor ajena a la conducción o al funcionamiento del vehículo (art. 1.1, párrafo 2.º TRLRCSCVM). Por otro lado, la Ley predetermina la tasa adecuada o fijación de un «quantum» máximo para la reparación, conforme a las reglas del sistema de valoración que contiene el TRLRCSCVM, que establece un sistema con baremos.

En el plano de los daños en los bienes, se mantiene el principio de la responsabilidad por culpa (art. 1.1, párrafo 3.º TRLRCSCVM), y el de la «restitutio in integrum» del art. 1.902 del Código Civil, por la regla del art. 1.2 TRLRCSCVM, en relación con la inaplicabilidad del sistema de valoración de daños corporales.

En el caso presente, se afirma la acción indiligente en la conducción de D./Dña. [NOMBRE Y APELLIDOS DEL CONDUCTOR DEMANDADO], y el evidente nexo causal con los daños y perjuicios cuya reparación se pide, en la persona de D./Dña. [NOMBRE Y APELLIDOS DEL CONDUCTOR DEMANDANTE], y en el vehículo de [DENOMINACIÓN SOCIAL DE LA EMPRESA PROPIETARIA DEL VEHÍCULO].

VIII.2

Por parte de D./Dña. [NOMBRE Y APELLIDOS DEL CONDUCTOR DEMANDANTE], conforme al régimen con baremos del TRLRCSCVM, se reclaman las siguientes cantidades para restañar los daños y perjuicios:

Lesiones temporales

- [Nº] días de asistencia hospitalaria por la cantidad de [IMPORTE] euros/día. Subtotal [IMPORTE] euros.

- [Nº] días impeditivos por la cantidad de [IMPORTE] euros/día. Subtotal [IMPORTE] euros.

- [Nº] días no impeditivos por la cantidad de [IMPORTE] euros/día. Subtotal [IMPORTE] euros.

Lesiones permanentes

- Cervicalgia irradiada a brazo derecho: [Nº] puntos.

- Cefaleas y mareos: [Nº] puntos.

- Lumbalgia: [Nº] puntos.

- Insensibilidad lingual: [Nº] puntos.

- Síndrome depresivo susceptible de desaparecer con el paso del tiempo: [Nº] puntos.

El subtotal asciende a [IMPORTE] euros, aplicando la fórmula legal para caso de indemnizaciones concurrentes, con arreglo al valor del punto para su número y edad del demandante conforme al baremo.

Sobre estos subtotales, que se aquilatan, ha de aplicarse el factor de corrección del [PORCENTAJE] %, con arreglo a las tablas del baremo, por los ingresos netos de trabajo personal de D./Dña. [NOMBRE Y APELLIDOS DEL CONDUCTOR DEMANDANTE], de [IMPORTE] euros anuales.

A efectos probatorios se acompaña copia de la declaración sobre el Impuesto sobre la Renta de las Personas Físicas del ejercicio fiscal [AÑO] (documento número [Nº DE DOCUMENTO]), y se designan, con citación contraria, los archivos de la Administración Estatal de la Agencia Tributaria en [LOCALIDAD].

Total de [IMPORTE] euros.

Por parte de [DENOMINACIÓN SOCIAL DE LA EMPRESA PROPIETARIA DEL VEHÍCULO] se reclaman:

- Valor de mercado de segunda mano de la furgoneta [MARCA Y MODELO], matriculada en el año [AÑO], con arreglo al dictamen pericial del tasador D./Dña. [NOMBRE Y APELLIDOS], que se aporta como documento número [Nº DE DOCUMENTO]. Subtotal [IMPORTE] euros.

- Gastos de servicio de grúa, con arreglo a la factura que se acompaña como documento número [Nº DE DOCUMENTO]. Subtotal [IMPORTE] euros.

- Lucro cesante por inactividad durante [Nº] días del vehículo siniestrado, que se cifra también atenidos al dictamen pericial del precitado documento número [Nº DE DOCUMENTO], sin perjuicio de, al tiempo, designar los libros de [CONCESIONARIO], concesionario de la marca [MARCA], quien vendió el vehículo de sustitución en cuanto estuvo a disposición, y los propios de [DENOMINACIÓN SOCIAL DE LA EMPRESA PROPIETARIA DEL VEHÍCULO], sobre su flota de vehículos, y nivel de negocio. Subtotal [IMPORTE] euros.

El lucro cesante no debe ser objeto de una prueba más rigurosa que cualquiera otra, desde esa torcida lectura de la jurisprudencia, cuando se habla de la incertidumbre de los «sueños de ganancia». Cuando se dice que la prueba del «lucrum cesans» debe ser categórica no se quiere decir que se construya en datos de hecho que hayan de probarse de una manera diferente en el proceso que los demás, sino que por tratarse de hechos futuribles —ganancias esperadas— la prueba no deja de ser tan rigurosa como la de cualquier hecho y no son puros datos conjeturales. Y precisamente el cálculo que se propone es conjetural en esencia. El objeto de este tipo de prueba es imposible captarlo como hecho histórico, al tratarse de sopesar algo que no ocurrirá sino que se impidió que ocurriera, pero es siempre preciso captarlo como algo seguro que habría ocurrido. Los hechos necesitados de prueba son aquí de dos naturalezas, el histórico, consistente en unos días de ausencia de rendimiento derivados de un bien productivo, como la furgoneta en cuestión, y el condicional, consistente en el rendimiento medio de un período de tiempo precedente similar de comparación, teniendo en cuenta los ingresos de [DENOMINACIÓN SOCIAL DE LA EMPRESA PROPIETARIA DEL VEHÍCULO] y efectuando el descuento de los gastos fijos de la estructura empresarial.

Total de [IMPORTE] euros.

VIII.3

La exoneración de los intereses por mora sólo se produce cuando el asegurador acredite haber presentado al perjudicado la oferta motivada de indemnización a que se refieren los arts. 7.2 y 22.1 TRLRCSCVM. El art. 7.2 TRLRCSCVM, introducido por Ley 21/2007, de 11 de julio, recoge la regulación del art. 22.1, sobre la reclamación de los perjudicados no residentes en España ante las entidades aseguradoras autorizadas en España o los representantes para tramitación y liquidación de siniestros por éstas designados en el resto de los Estados del Espacio Económico Europeo. Conforme a este sistema, en el plazo de tres meses desde la recepción de la reclamación del perjudicado, el asegurador debe seguir una de dos conductas:

A) Presentar una oferta motivada de indemnización, cuando entienda acreditada la responsabilidad y cuantificado el daño.

B) Dar una respuesta motivada, porque entienda la aseguradora que no es probada responsable, resulta incuantificado el daño, o porque la reclamación haya sido rechazada.

Tal oferta o respuesta cuenta con un contenido legal mínimo, aunque reglamentariamente puede precisarse (art. 7.3, 4 y 5 TRLRCSCVM).

Por consiguiente, en el caso presente se han devengado los intereses de demora, por cuanto ha transcurrido el plazo de tres meses desde la reclamación de esta parte el [DÍA] de [MES] de [AÑO], sin que haya presentado una oferta motivada de indemnización, «por una causa no justificada o que le fuera imputable al asegurador».

La indemnización de todos los daños en este ámbito devenga intereses moratorios especiales, con ribete penitencial indiscutido, que se agrega al carácter de reparación adicional por el retraso culpable en el pago, al ser la obligada compañía de seguros, conforme a un sistema que representa excepción legal expresa a un principio jurisprudencial tradicional —de suyo, no es requisito de la común «mora debitoris» del art. 1.100 del Código Civil—, y que sin carácter absoluto, en general rechaza la aplicación de intereses moratorios a los créditos de suma ilíquida, dentro de los que se hallan el derecho a las indemnizaciones de daños y perjuicios.

Sin negar que en alguna ocasión muy especial puedan percibirse circunstancias que indiquen justificado en estos casos no hacer pago o hacerlo en cantidad inferior a la debida, o que el impago pueda ser imputable a conducta del acreedor, el art. 9.b) TRLRCSCVM instaura un único mecanismo de conciliar iliquidez y ese acicate para el resarcimiento temprano de los damnificados, consistente en la declaración judicial de suficiencia de la consignación o pago verificado dentro de los tres meses desde la reclamación del perjudicado. Tal es el mecanismo de enervar estos intereses disuasorios, el cual no se ha utilizado en el asunto.

Por consiguiente, en modo alguno se ha enervado el devengo de intereses de mora para la aseguradora que establece el art. 20.4.ª LCS, con los dos tipos o réditos del interés de mora, con carácter de mínimos, uno del legal del dinero incrementado en el 50% y otro exacerbado del 20% anual, que procede para cuando el retraso culpable en el pago supere los dos años.

IX COSTAS

El empleo del principio cuasiobjetivo del vencimiento del art. 394.1 LEC conlleva el deber de reintegro de las costas procesales por la parte demandada, sin que existan dudas de hecho o derecho, ni vacilaciones jurisprudenciales sobre el objeto del proceso.

Por todo lo anteriormente expuesto,

AL TRIBUNAL SUPLICO,

que habiendo por presentado este escrito, con el poder que acredita la representación procesal, y los documentos acompañados, y copias de todo ello, se sirva admitir uno y otros, tener por formulada demanda de juicio ordinario, en nombre de quien comparezco, contra D./Dña. [NOMBRE Y APELLIDOS DEL CONDUCTOR DEMANDADO], y las sociedades [DENOMINACIÓN SOCIAL DE LA EMPRESA PROPIETARIA DEL VEHÍCULO CAUSANTE] y [DENOMINACIÓN SOCIAL DE LA ASEGURADORA], y seguidos que sean los trámites legales, dicte sentencia por la que estimando íntegramente esta demanda, se condene a los demandados a que indemnicen conjunta y solidariamente en la suma de [IMPORTE] euros a mi representado D./Dña. [NOMBRE Y APELLIDOS DEL CONDUCTOR DEMANDANTE], y a la suma de [IMPORTE] euros a mi también representada [DENOMINACIÓN SOCIAL DE LA EMPRESA PROPIETARIA DEL VEHÍCULO], incrementadas en lo que representen los intereses de mora al tipo diario consistente en el legal vigente en la fecha de ocurrencia del siniestro incrementado en un cincuenta por ciento desde la fecha de ocurrencia del accidente o, en su caso, del veinte por ciento, respecto de la aseguradora codemandada, y los intereses legales desde la interpelación judicial respecto de los otros codemandados.

Es justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a: [NOMBRE Y APELLIDOS] | Firma del Procurador/a: [NOMBRE Y APELLIDOS]
