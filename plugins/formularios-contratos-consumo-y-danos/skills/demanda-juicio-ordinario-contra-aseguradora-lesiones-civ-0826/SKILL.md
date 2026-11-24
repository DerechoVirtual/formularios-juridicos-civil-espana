---
name: demanda-juicio-ordinario-contra-aseguradora-lesiones-civ-0826
description: "Demanda de juicio ordinario contra la aseguradora por lesiones derivadas de accidente de tráfico. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio ordinario contra la aseguradora por lesiones derivadas de accidente de tráfico

> Formulario **CIV-0826** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario en reclamación de indemnización por daños en las personas derivados de la circulación de vehículos de motor, frente a la compañía aseguradora.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio ordinario contra la aseguradora por lesiones derivadas de accidente de tráfico» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio ordinario contra la aseguradora por lesiones derivadas de accidente de tráfico” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-juicio-ordinario-contra-aseguradora-lesiones-civ-0826`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (12 veces)
- [ ] IMPORTE (9 veces)
- [ ] Nº (8 veces)
- [ ] FECHA (5 veces)
- [ ] Nº DE DOCUMENTO (5 veces)
- [ ] NÚMERO (4 veces)
- [ ] AÑO (2 veces)
- [ ] CITA JURISPRUDENCIAL (2 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] MARCA/MODELO (2 veces)
- [ ] SEDE (2 veces)
- [ ] ASEGURADORA
- [ ] CALLE
- [ ] COLEGIO
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] MATRÍCULA
- [ ] MUNICIPIO
- [ ] NOMBRE DEL HOSPITAL
- [ ] Nº DE CARRETERA
- [ ] PARTE DEMANDADA
- [ ] SUCURSAL

## Normas que cita el formulario

- art. 85 LOPJ
- art. 45 LEC
- art. 52.1.9.º LEC
- art. 6.1.1.º LEC
- art. 7.1 LEC
- art. 6.1.3.º LEC
- art. 7.4 LEC
- art. 10 LEC
- art. 76 LCS
- art. 253.1 LEC
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 73 Ley 50/1980
- art. 73 LCS
- art. 1144 CC
- art. 1137 CC
- art. 1145.I CC
- art. 20 LCS
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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…rador/a ========================================================================»: requisito de procedibilidad del art. 5 LO 1/2025 — antes de presentar la demanda hay que intentar un medio adecuado de solución de controversias (MASC) y acreditarlo con la demanda (arts. 264.4.º y 399.3 LEC), salvo las materias excluidas del art. 5.2. Fuente: LO 1/2025, arts. 5 a 7 (BOE-A-2025-76).

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

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], y a cuya justificación aporto escritura de poder inscrito en el Registro Electrónico de Apoderamientos Judiciales con el nº [NÚMERO] y que se puede acreditar mediante consulta automatizada orientada al dato, por parte del órgano judicial al cual tengo el honor de dirigirme, acompañándose certificación electrónica del Registro Electrónico de Apoderamientos Judiciales como Documento nº [Nº DE DOCUMENTO] por si no es posible la consulta automatizada, y con la asistencia de el/la Letrado/a D./Dña. [NOMBRE Y APELLIDOS], del Ilustre Colegio de Abogados de [COLEGIO], cuyo despacho está abierto en esta población, calle [CALLE], ante la Sección Civil del Tribunal de Instancia que por turno de reparto corresponda, comparezco y, como mejor proceda en Derecho, DIGO:

Que siguiendo expresas instrucciones de quien ostento representación, por medio del presente escrito formulo demanda deJUICIO ORDINARIO, que dirijo contra la aseguradora SEGUROS DEL NORTE [DENOMINACIÓN SOCIAL], para ser citada en su oficina de [SUCURSAL], calle

HECHOS

PRIMERO.- El día [FECHA], mi representado D./Dña. [NOMBRE Y APELLIDOS] viajaba como ocupante en el vehículo turismo marca [MARCA/MODELO], modelo [MARCA/MODELO], matrícula [MATRÍCULA], conducido por su propietario D./Dña. [NOMBRE Y APELLIDOS], con póliza de seguro n.º [NÚMERO] en

SEGUNDO.- El citado vehículo, al llegar a una curva existente en el km. de la carretera [Nº DE CARRETERA], en el término de [MUNICIPIO], haciéndolo de forma distraída y a excesiva velocidad, se salió de la calzada, provocando la pérdida de control del vehículo, dando una vuelta de campana, para posteriormente quedar detenido a unos [Nº] metros, volcado sobre su lateral izquierdo, transversalmente al eje de la calzada y con los neumáticos orientados hacia

TERCERO.- Como consecuencia de ello D./Dña. [NOMBRE Y APELLIDOS] fue evacuado de urgencia del lugar del accidente al Hospital de [LOCALIDAD], donde fue intervenido de herida abierta en cabeza, y permaneció ingresado, causando posteriormente baja laboral.

Presenta en definitiva las siguientes lesiones a la fecha en que es dado de alta, [FECHA]:

— Esguince cervical.
— Traumatismo en mano izquierda.
— Heridas en la lengua.
— Traumatismo cráneo-encefálico de grado II.

Para su sanidad, además de la asistencia hospitalaria de [Nº] días, precisó D./Dña. [NOMBRE Y APELLIDOS] tratamiento médico posterior consistente en collarín cervical, férula y cabestrillo en mano izquierda, sutura de las heridas, y tratamiento rehabilitador, curando en [Nº] días incapacitado para sus ocupaciones habituales.

Permanecen como secuelas cervicalgia irradiada a brazo derecho, cefaleas y mareos y lumbalgia, ambos estables en el tiempo a la vista de la persistencia en su sintomatología; zonas de insensibilidad linguales, y síndrome depresivo susceptible de desaparecer con el paso del tiempo.

A efectos probatorios se acompañan como documentos números [Nº DE DOCUMENTO], el informe de asistencia en el Servicio de Urgencias del Hospital [NOMBRE DEL HOSPITAL] y el informe de alta del mismo, partes de baja y alta de Incapacidad Temporal, certificados expedidos por los Doctores [NOMBRE Y APELLIDOS] y [NOMBRE Y APELLIDOS], que le han venido asistiendo periódicamente a D./Dña. [NOMBRE Y APELLIDOS]; e igualmente se acompaña dictamen de valoración de daño corporal emitido por perito designado por esta parte y que justifica la reclamación pecuniaria que se formula.

Para el supuesto de que fueren impugnados los documentos aportados por esta parte relativos a asistencia prestada por Centros Sanitarios Públicos, se solicita se remita oficio a fin de que se proceda al cotejo o comprobación de los aportados con los que obren en los correspondientes archivos.

CUARTO.- Después de la ocurrencia del siniestro fue instruido atestado por la Policía Autonómica, registrado como n.º [NÚMERO]/[AÑO], y cuyos archivos designamos, con citación contraria, dado que no se ha facilitado a esta parte copia del mismo, siendo preciso a tal fin remisión de oficio por el Tribunal, el que se interesa se entregue al Procurador/a suscrito, a fin de cuidar de su cumplimentación, en la cual intervendrá.

Igualmente se incoaron las Diligencias Previas n.º [NÚMERO]/[AÑO] por la Sección de Instrucción del Tribunal de Instancia de [SEDE], en virtud de parte facultativo, las que fueron sobreseídas por no constar la formulación de denuncia en el plazo legalmente establecido. Se acompaña como documento número [Nº DE DOCUMENTO] testimonio de las referidas actuaciones.

QUINTO.- Mi patrocinado ha tenido que acudir a la presente vía judicial civil, por no haber sido atendidas sus reclamaciones amistosas. Habiéndose formulado el día [FECHA] reclamación circunstanciada, con petición precisa de indemnizaciones, a [ASEGURADORA], esta compañía contestó mediante una oferta que no se atiene al contenido legal necesario, y sin que haya sido seguida de pago o consignación de ningún tipo, a cuya prueba se acompañan el burofax enviado a dicha demandada, y la carta recibida el [FECHA] (documentos números [Nº DE DOCUMENTO]).

FUNDAMENTOS DE DERECHO

I JURISDICCION Y COMPETENCIA

Los art. 85 LOPJ y art. 45 LEC, designan a las secciones civiles de los tribunales de instancia, como los órganos con la competencia específica, objetiva y funcional, para resolver estos pleitos, y el art 52.1.9.º LEC fija la competencia territorial para juicio en que se pida indemnización de los daños y perjuicios derivados de la circulación de vehículos de motor en el tribunal del lugar en que se causaron los daños.

II PROCEDIMIENTO

En aplicación de los arts. 248.3 y 249.2 LEC, y en atención a la cuantía del objeto litigioso, que supera los 15.000 euros, este pleito se tramitará por las normas del proceso declarativo llamado juicio ordinario.

III CAPACIDAD

Conforme al art. 6.1.1.º LEC tienen capacidad para ser parte las personas físicas, y a tenor del art. 7.1 LEC detentan capacidad de obrar procesal, en tanto que mayores de edad no incapacitadas, siendo el caso del actor.

La capacidad para ser parte de las personas jurídicas se reconoce en el art. 6.1.3.º LEC, cuya personalidad deriva de su constitución en escritura pública inscrita en el Registro Mercantil, debiendo comparecer en juicio a medio de sus representantes legales (art. 7.4 LEC).

IV LEGITIMACIÓN

El art. 10 LEC legitima para comparecer y actuar en juicio, a los titulares de la relación jurídica o del objeto litigioso, lo cual es legitimación ordinaria, que en el caso de autos detenta la activa originaria el demandante, en cuanto titular del derecho subjetivo patrimonial a la reparación de los daños inferidos a su persona, así como la pasiva originaria, el demandado, incumplidor de la correlativa obligación resarcitoria, SEGUROS DEL NORTE [DENOMINACIÓN SOCIAL], por virtud del contrato de seguro, en lo que es la acción directa recogida en el art. 76 LCS 50/80.

V POSTULACIÓN

En aplicación de los arts. 23.1 y 31.1 LEC, las partes comparecerán representadas por Procurador/a de los Tribunales y asistidas por Letrado en ejercicio, ambos habilitados ante el Tribunal.

VI CUANTÍA

Cumpliendo la exigencia del art. 253.1 LEC, se cifra la cuantía de la demanda en la cantidad de [IMPORTE] euros, conforme a la regla 1.ª delart. 251 LEC.

VII CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VIII FONDO DEL ASUNTO

VIII 1

Mi mandante ejerce, frente a la aseguradora demandada, la acción prevista en el art. 1 del Texto Refundido de la Ley sobre Responsabilidad Civil y Seguro en la Circulación de Vehículos a Motor (TRLRCSCVM), aprobado por Real Decreto Legislativo 8/2004, de 29 de octubre, y en los arts. 73 y 76 de la Ley 50/1980, de 8 de octubre, de Contrato de Seguro (LCS 50/80).

En el art. 1 TRLRCSCVM se dispone que "el conductor de vehículos a motor es responsable, en virtud del riesgo creado por la conducción de estos, de los daños causados a las personas o en los bienes con motivo de la circulación. En el caso de daños a las personas, de esta responsabilidad sólo quedará exonerado cuando pruebe que los daños fueron debidos únicamente a la conducta o la negligencia del perjudicado o a fuerza mayor extraña a la conducción o al funcionamiento del vehículo; no se considerarán casos de fuerza mayor los defectos del vehículo ni la rotura o fallo de alguna de sus piezas o mecanismos".

A su vez dispone el art. 73 LCS 50/80 que "por el seguro de responsabilidad civil el asegurador se obliga, dentro de los límites establecidos en la Ley y en el contrato, a cubrir el riesgo del nacimiento a cargo del asegurado de la obligación de indemnizar a un tercero los daños y perjuicios causados por un hecho previsto en el contrato de cuyas consecuencias sea civilmente responsable el asegurado conforme a derecho", estableciendo el art. 76 de la misma Ley que "el perjudicado o sus herederos tendrán acción directa contra el asegurador para exigirle el cumplimiento de la obligación de indemnizar".

Así pues, mediante el seguro de responsabilidad civil la entidad aseguradora asume el riesgo del asegurado de ver comprometido su patrimonio por la obligación de resarcir los daños y perjuicios derivados de una eventual responsabilidad de aquella índole; asunción contractual que si, de una parte, desplaza sobre la aseguradora la deuda indemnizatoria a cargo del asegurado, de otra, confiere al tercero perjudicado acción para instar directamente de aquella entidad la satisfacción de la obligación asumida mediante el pago de la indemnización debida por su asegurado. La confluencia de estas dos responsabilidades directas en relación a un mismo objeto, el resarcimiento de la víctima, se traduce, conforme a reiterada jurisprudencia (Tribunal Supremo, Sala Primera, de lo Civil, Sentencia de 7 May. 1993, [CITA JURISPRUDENCIAL]) en la solidaridad de asegurador y asegurado respecto al abono de la indemnización consecuente a la responsabilidad civil de este último, que puede ser exigida conjunta o indistintamente de uno y otro, según lo prevenido por el art. 1144 CCiv; siendo de recordar, en lo que al vínculo solidario se refiere, que aunque la solidaridad no se presume según el art. 1137 CCiv, puede venir determinada no sólo por el pacto entre acreedores y deudores, sino también por la Ley e incluso por la propia naturaleza o circunstancias de la obligación.

La responsabilidad directa y solidaria de la aseguradora faculta pues al perjudicado para instar de aquélla la satisfacción de la deuda indemnizatoria a cargo del asegurado.

Siendo solidaria la responsabilidad exigible, la aseguradora no podrá dejar de hacer frente, a instancia del perjudicado, a la totalidad de la deuda indemnizatoria de que asimismo habría de responder su asegurado; naturalmente sin perjuicio de repetir contra los demás responsables solidarios la parte o porción que a cada uno corresponda con los intereses del anticipo, según lo dispuesto en el art. 1145.II CCiv, aplicable al asegurador que por virtud de la acción directa satisface la deuda en lugar o por el codeudor asegurado (Tribunal Supremo, Sala Primera, de lo Civil, Sentencia de 31 Oct. 1991, [CITA JURISPRUDENCIAL].

VIII. 2

Conforme al régimen con baremos del Anexo al TRLRCSCVM, se reclaman las siguientes cantidades para restañar los daños y perjuicios:

Lesiones temporales (Tabla V baremo)

— días de asistencia hospitalaria por la cantidad de [IMPORTE] euros/día

Subtotal [IMPORTE] euros

— días impeditivos por la cantidad de [IMPORTE] euros/día.

Subtotal [IMPORTE] euros.

— días no impeditivos la cantidad de [IMPORTE] euros/día.

Subtotal [IMPORTE] euros.

Lesiones permanentes (Tabla VI baremo)

— Cervicalgia irradiada a brazo derecho [Nº] puntos

— Cefaleas y mareos [Nº] puntos

— Lumbalgia [Nº] puntos

— Insensibilidad lingual [Nº] puntos

— Síndrome depresivo susceptible de desaparecer con el paso del tiempo [Nº] puntos

El subtotal asciende a [IMPORTE] euros, aplicando la fórmula legal de apartado 2 del Anexo, para caso de indemnizaciones concurrentes, con arreglo al valor del punto para su número y edad del demandante de la Tabla III del baremo.

Sobre estos subtotales, que se aquilatan, ha de aplicarse el factor de corrección del%, con arreglo a las tablas IV y V baremo, por los ingresos netos de trabajo personal de D./Dña. [NOMBRE Y APELLIDOS], de [IMPORTE] euros anuales.

A efectos probatorios se acompaña copia de la declaración sobre el Impuesto de Renta de las Personas Físicas del ejercicio fiscal (documento número [Nº DE DOCUMENTO]), y se designan, con citación contraria, los archivos de la Administración Estatal de la Agencia Tributaria en

Total deeuros

VIII 3

La exoneración de los intereses por mora especial del asegurador impone acreditar haber presentado al perjudicado la oferta motivadade indemnización a que se refiere elart 7.2 TRLRCSCVM, introducido por Ley 21/2007, de 11 de julio, conforme al que, en el plazo de tres meses desde la recepción de la reclamación del perjudicado, el asegurador debe una de dos conductas:

A) Presentar una oferta motivada de indemnización, cuando entienda acreditada la responsabilidad y cuantificado el daño.
B) Dar una respuesta motivada, porque entienda la aseguradora que no es probada responsable, resulta incuantificado el daño, o porque la reclamación haya sido rechazada.

Tal oferta o respuesta cuenta con un contenido legal mínimo, aunque reglamentariamente puede precisarse (art. 7.3, 4 y 5 TRLRCSCVM).

Ahora bien, la oferta motivada debe cumplir los siguientes requisitos (art. 7.3 TRLRCSCVM):

a) Contendrá una propuesta de indemnización por los daños en las personas y en los bienes que pudieran haberse derivado del siniestro. En caso de que concurran daños a las personas y en los bienes figurará de forma separada la valoración y la indemnización ofertada para unos y otros.
b) Los daños y perjuicios causados a las personas se calcularán según los criterios e importes que se recogen en el anexo de este TRLRCSCVM.
c) Contendrá, de forma desglosada y detallada, los documentos, informes o cualquier otra información de que se disponga para la valoración de los daños, identificándose aquellos en que se ha basado para cuantificar de forma precisa la indemnización ofertada, de manera que el perjudicado tenga los elementos de juicio necesarios para decidir su aceptación o rechazo.
d) Se hará constar que el pago del importe que se ofrece no se condiciona a la renuncia por el perjudicado del ejercicio de futuras acciones en el caso de que la indemnización percibida fuera inferior a la que en derecho pueda corresponderle.
e) Podrá consignarse para pago la cantidad ofrecida.

Además, en el art. 7.2, párrafo 4.º TRLRCSCVM se incide en que el asegurador debe observar desde el momento en que conozca por cualquier medio la existencia del siniestro una conducta diligente en la cuantificación del daño y la liquidación de la indemnización, lo cual sin duda, sirve de canon para calibrar la causa justificada o inimputable al asegurador para no emitir su oferta.

Pues bien, aunque la demandada no responde negando responsabilidad, o rechazando la reclamación, alega la inviabilidad de cuantificar la indemnización en cuanto a las lesiones permanentes, y entonces, no se pone a disposición de esta parte cifra alguna.

Debió la aseguradora, al tenor del art. 9.b) TRLRCSCVM, por excepción al plazo y condiciones de la predicha oferta motivada, cuando los daños causados a las personas hubiesen de sufrirse por estas durante más de tres meses, o su exacta valoración no pudiera ser determinada a efectos de tal oferta, recabar del órgano judicial competente que resolviera, en auto frente a la que no cabría recurso alguno, acerca de la suficiencia o ampliación de la cantidad consignada por el asegurador ‘a la vista de las circunstancias del caso y de los dictámenes e informes que precise’, siempre atendiendo a los criterios, y respetando los límites cuantitativos fijados en el baremo del Anexo del TRLRCSCVM.

No ha procedido así, y no existe mitigación de las consecuencias del régimen de la mora del asegurador, ahorrándole los intereses del art. 20 LCS 50/80 cuando su conducta no es demostrativa de la voluntad de cumplir, mediante la oferta motivada de una determinada indemnización, siempre que, aceptada por el perjudicado, se pagara efectivamente. La oferta motivada debe atenerse al contenido preceptivo de la Ley, y en su día, desarrollado reglamentariamente, y en otro caso, no tiene eficacia.

No cumple la aseguradora con aventurar al derechohabiente de una suma, sino con la consignación que resulte al tiempo de efectuarla, adecuada, pero ello si es cabal cuantificarla y el perjudicado acepta. En otro caso, no habrá cantidad cierta ofertada, y no se sabe, según los informes y dictámenes que obren en autos, y atenido al Baremo del Anexo al TRLRCSCVM, cuál es la misión en concreto del órgano judicial para fijar la suficiencia.

Por consiguiente, en modo alguno se ha enervado el devengo de intereses de mora para la aseguradora que establece el art. 20.4.ª LCS 50/80, con los dos tipos o réditos del interés de mora, con carácter de mínimos, uno del legal del dinero incrementado en el 50% y otro exacerbado del 20% anual, que procede para cuando el retraso culpable en el pago supere los dos años.

IX COSTAS

El empleo del principio cuasiobjetivo del vencimiento del art. 394.1 LEC, conlleva el deber de reintegro de las costas procesales por la parte demandada, sin que existan dudas de hecho o derecho, ni vacilaciones jurisprudenciales sobre el objeto del proceso.

Por todo lo anteriormente expuesto,

AL TRIBUNAL SUPLICO,

que habiendo por presentado este escrito, con el poder que acredita la representación procesal, y los documentos acompañados, y copias de todo ello, se sirva admitir uno y otros, tener por formulada demanda de juicio ordinario, en nombre de quien comparezco, contra [PARTE DEMANDADA], y seguidos que sean los trámites legales, dicte sentencia por la que estimando íntegramente esta demanda, se condene al demandado a que indemnice en la suma deeuros a mi representado D./Dña. [NOMBRE Y APELLIDOS], incrementadas en lo que representen los intereses de mora al tipo diario consistente en el legal vigente en la fecha de ocurrencia del siniestro incrementado en un cincuenta por ciento desde la fecha de ocurrencia del accidente o, en su caso, del veinte por ciento,

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
