---
name: demanda-juicio-ordinario-danos-trafico-tras-juicio-civ-0763
description: "Demanda de juicio ordinario por daños de tráfico tras juicio por delito leve y reserva de acciones. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio ordinario por daños de tráfico tras juicio por delito leve y reserva de acciones

> Formulario **CIV-0763** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Demanda declarativa ante la jurisdicción civil, en solicitud de indemnización derivada de hecho de la circulación que fue objeto de previo juicio por delitos leves en el que hubo reserva de acciones.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio ordinario por daños de tráfico tras juicio por delito leve y reserva de acciones» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio ordinario por daños de tráfico tras juicio por delito leve y reserva de acciones” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-juicio-ordinario-danos-trafico-tras-juicio-civ-0763`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (22 veces)
- [ ] IMPORTE (12 veces)
- [ ] Nº DE DOCUMENTO (11 veces)
- [ ] Nº (9 veces)
- [ ] LOCALIDAD (7 veces)
- [ ] FECHA (6 veces)
- [ ] ASEGURADORA (5 veces)
- [ ] NÚMERO (3 veces)
- [ ] MARCA/MODELO (2 veces)
- [ ] MATRÍCULA (2 veces)
- [ ] AÑO
- [ ] CALLE
- [ ] CORREO ELECTRÓNICO
- [ ] DOMICILIO
- [ ] LUGAR
- [ ] MARCA Y MATRÍCULA DEL VEHÍCULO
- [ ] NOMBRE DE LA PARTE
- [ ] NOMBRE DE LA VÍA
- [ ] NOMBRE DEL HOSPITAL
- [ ] Nº DE COLEGIADO/A
- [ ] Nº DE PROCEDIMIENTO
- [ ] SEDE
- [ ] SUCURSAL
- [ ] TELÉFONO

## Normas que cita el formulario

- art. 24.1 LEC
- art. 399.1 LEC
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
- art. 251 LEC
- art. 5 Ley Orgánica 1/2025
- art. 1.092 CC
- art. 1.902 CC
- art. 1.100 CC
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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) A la hora de su acreditación, todos los poderes deben estar inscritos en el Registro Electrónico de Apoderamientos Judiciales (REAJ). Se supone que, para su acreditación, basta con la consulta (de dicho Registro) automatizada orientada al dato. Algo que está a disposición de cualquier Letrado de la Administración de Justicia. Sin embargo, dado que el art. 24.2 LEC, configura la certificación de dicha inscripción como vía subsidiaria de acreditación, para el caso de que el sistema no permita aquella consulta automatizada; se señala en el modelo que se acompaña certificación electrónica. El sistema permite emitir dicha certificación para quien inscribe el poder.

(2) El art. 155.3 LEC permite fijar expresar varios domicilios del demandado (el que aparezca en el padrón municipal o conste oficialmente a estos efectos; el que aparezca en Registro oficial o en publicaciones de colegios profesionales, si se trata de empresas o personas colegiadas; donde desarrolle su actividad profesional o laboral no ocasional; si es empresa mercantil, el domicilio de cualquiera de sus administradores, gerentes, o apoderados; o, si es asociación que consta en registro oficial; el domicilio del presidente, miembro o gestor de la Junta correspondiente). Cuando se señalen varios, indicará el orden a seguir para la notificación, con vistas al éxito de la misma.

(3) El art. 155.3 LEC configura una obligación adicional del demandante, consistente en aportar cuantos datos sean de utilidad para localizar al demandado: número de identificación fiscal o de extranjeros, nº [Nº] de teléfono o de fax, dirección de correo electrónico, o similares.

========================================================================

[NOTA DE REVISIÓN: requisito de procedibilidad del art. 5 LO 1/2025 — antes de presentar la demanda hay que intentar un medio adecuado de solución de controversias (MASC) y acreditarlo con la demanda (arts. 264.4.º y 399.3 LEC), salvo las materias excluidas del art. 5.2. Fuente: LO 1/2025, arts. 5 a 7 (BOE-A-2025-76).]


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

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], representación que acredito mediante escritura de poder otorgada a mi favor (existen tres posibilidades para otorgar el apoderamiento al Procurador de los Tribunales, conforme dispone el art. 24.1 LEC)

[OPCIONAL — opción en función de cómo se haya otorgado el poder]

[ELEGIR UNA OPCIÓN: Si el poder se otorga a través de la sede judicial electrónica / Si el poder se otorga mediante comparecencia apud acta / Si el poder se otorga ante Notario]

bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS], abogado/a en ejercicio, con despacho profesional abierto en [LOCALIDAD], colegiado nº [Nº DE COLEGIADO/A] del Ilustre Colegio de la Abogacía de [LOCALIDAD], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que mediante el presente escrito vengo a formular DEMANDA DE JUICIO ORDINARIO, contra:

— D./Dña. [NOMBRE Y APELLIDOS], con domicilio, primero en [DOMICILIO]); con email [CORREO ELECTRÓNICO]; y con número de teléfono móvil [TELÉFONO]
— La aseguradora [ASEGURADORA], para ser citada en su oficina de [SUCURSAL], calle [CALLE]

; en ejercicio de la acción que se concretará en el cuerpo del escrito y en el suplico, y todo ello de conformidad con los hechos y fundamentos de derecho que se desarrollarán a continuación.

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa, e, incluso, en una eventual fase de ejecución por medios telemáticos, en términos del art. 399.1 II LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y nº [Nº] de teléfono:

HECHOS

PRIMERO.- En fecha [FECHA], mi representado D./Dña. [NOMBRE Y APELLIDOS] era titular de un vehículo marca [MARCA/MODELO], matrícula [MATRÍCULA], conforme acredito mediante fotocopia del permiso de circulación que aportamos (documento número [Nº DE DOCUMENTO]), designando los Libros del Registro de Bienes Muebles y archivo de la Jefatura Provincial de Tráfico.

SEGUNDO.- El citado día [FECHA], conducía el vehículo antes reseñado D./Dña. [NOMBRE Y APELLIDOS], haciéndolo de forma correcta y a velocidad moderada por [NOMBRE DE LA VÍA] cuando al llegar a la altura del cruce con la carretera de San Tomás fue colisionado por el vehículo marca [MARCA/MODELO], matrícula [MATRÍCULA], conducido por el demandado D./Dña. [NOMBRE Y APELLIDOS], que no respetó la señal de preferencia ("Stop") que le afectaba, provocando así la colisión.

TERCERO.- El turismo [MARCA Y MATRÍCULA DEL VEHÍCULO], que conducía D./Dña. [NOMBRE Y APELLIDOS]. se encontraba asegurado en la fecha del siniestro en la aseguradora también demandada [ASEGURADORA], con póliza número

A la acreditación de estos extremos se aporta copia de las Diligencias a Prevención n.º [Nº]/[AÑO] de la Policía Local de [LOCALIDAD], dejando designados los archivos de dicha autoridad a efectos probatorios (documento número [Nº DE DOCUMENTO]).

CUARTO.- D./Dña. [NOMBRE Y APELLIDOS] fue evacuado de urgencia del lugar del accidente al Hospital de [LOCALIDAD], donde fue intervenido de herida abierta en cabeza, y permaneció ingresado, causando posteriormente baja laboral.

Presenta en definitiva las siguientes lesiones a la fecha en que es dado de alta, [FECHA]:

- Esguince cervical.
- Traumatismo en mano izquierda.
- Heridas en la lengua.
- Traumatismo cráneo-encefálico de grado II.

Para su sanidad, además de la asistencia hospitalaria de [Nº] días, precisó D./Dña. [NOMBRE Y APELLIDOS] tratamiento médico posterior consistente en collarín cervical, férula y cabestrillo en mano izquierda, sutura de las heridas, y tratamiento rehabilitador, curando en [Nº] días incapacitado para sus ocupaciones habituales.

Permanecen como secuelas cervicalgia irradiada a brazo derecho, cefaleas y mareos y lumbalgia, ambos estables en el tiempo a la vista de la persistencia en su sintomatología; zonas de insensibilidad linguales, y síndrome depresivo susceptible de desaparecer con el paso del tiempo.

A efectos probatorios se acompañan como documentos números [Nº DE DOCUMENTO] a [Nº DE DOCUMENTO], el informe de asistencia en el Servicio de Urgencias del Hospital [NOMBRE DEL HOSPITAL] y el informe de alta del mismo, partes de baja y alta de Incapacidad Temporal, certificados expedidos por los Doctores [NOMBRE Y APELLIDOS] y [NOMBRE Y APELLIDOS], que le han venido asistiendo periódicamente a D./Dña. [NOMBRE Y APELLIDOS]; e igualmente se acompaña dictamen de valoración de daño corporal emitido por perito designado por esta parte y que justifica la reclamación pecuniaria que se formula.

Para el supuesto de que fueren impugnados los documentos aportados por esta parte relativos a asistencia prestada por Centros Sanitarios Públicos, se solicita se remita oficio a fin de que se proceda al cotejo o comprobación de los aportados con los que obren en los correspondientes archivos.

QUINTO.- El vehículo de mi patrocinado, que tuvo que ser retirado de la calzada mediante grúa, sufrió graves daños, siendo considerado como siniestro total, según informe pericial, el cual calcula el precio medio del mercado a la fecha del siniestro, y que se acompaña como documento número [Nº DE DOCUMENTO], causando posteriormente el vehículo baja total según la nota informativa de la Jefatura Provincial de Tráfico de que se acompaña como documento número [Nº DE DOCUMENTO].

A los oportunos efectos probatorios se acompaña la factura de los servicios de grúa (documento número [Nº DE DOCUMENTO]).

SEXTO.- Consecuencia de tales hechos esta parte interpuso denuncia penal, siguiéndose ante la Sección de Instrucción del TI n.º [NÚMERO] de [LOCALIDAD] el Juicio por delitos leves / [Nº DE PROCEDIMIENTO] que finalizó con la sentencia condenatoria contra el conductor hoy demandado, asegurado en [ASEGURADORA], con reserva de acciones civiles al perjudicado, las cuáles se ejercitan a través de la presente demanda.

Se acompaña como documento número [Nº DE DOCUMENTO] copia de la Sentencia n.º [NÚMERO], de fecha [FECHA], dictada por la Sección de Instrucción del TI n.º [NÚMERO] de [LOCALIDAD], dejando designados los archivos de dicho tribunal a efectos de prueba.

SÉPTIMO.- Mis patrocinados han tenido que acudir a la presente vía judicial civil, por no haber sido atendida su reclamación amistosa, a cuya prueba se acompaña el burofax enviado a los codemandados (documento número [Nº DE DOCUMENTO]) reclamando las cantidades que en esta demanda se solicitan, con especificación de partidas de indemnización y su cuantificación, sin que en momento alguno hayan atendido al pago o recibido respuesta motivada de [ASEGURADORA], y habiendo transcurrido en exceso el plazo de tres meses desde la indicada reclamación, sin que se haya pagado o consignado cantidad alguna.

FUNDAMENTOS DE DERECHO

I. JURISDICCIÓN Y COMPETENCIA

Los art. 85 LOPJ y art. 45 LEC, designan a las secciones civiles de los tribunales de instancia, como los órganos con la competencia específica, objetiva y funcional, para resolver estos pleitos, y el art 52.1.9.º LEC fija la competencia territorial para juicio en que se pida indemnización de los daños y perjuicios derivados de la circulación de vehículos de motor en el tribunal del lugar en que se causaron los daños.

II. PROCEDIMIENTO

En aplicación de los arts. 248.3 y 249.2 LEC, y en atención a la cuantía del objeto litigioso, que supera los 15.000 euros, este pleito se tramitará por las normas del proceso declarativo llamado juicio ordinario.

III. CAPACIDAD

Conforme al art. 6.1.1.º LEC tienen capacidad para ser parte las personas físicas, y a tenor del art. 7.1 LEC detentan capacidad de obrar procesal, en tanto que mayores de edad no incapacitadas.

La capacidad para ser parte de las personas jurídicas se reconoce en el art. 6.1.3.º LEC, cuya personalidad deriva de su constitución en escritura pública inscrita en el Registro Mercantil, debiendo comparecer en juicio por medio de sus representantes legales (art. 7.4 LEC).

IV. LEGITIMACIÓN

El art. 10 LEC legitima para comparecer y actuar en juicio, a los titulares de la relación jurídica o del objeto litigioso, lo cual es legitimación ordinaria, que en el caso de autos detenta la activa originaria el demandante, en cuanto titular del derecho subjetivo patrimonial a la reparación de los daños inferidos a la persona y al patrimonio de D./Dña. [NOMBRE Y APELLIDOS], así como la pasiva originaria, los demandados, incumplidores de la correlativa obligación resarcitoria, D./Dña. [NOMBRE Y APELLIDOS] como agente del daño, y [ASEGURADORA], por virtud del contrato de seguro, en lo que es la acción directa recogida en el art. 76 LCS 50/80.

V. POSTULACIÓN

En aplicación de los arts. 23.1 y 31.1 LEC, las partes comparecerán representadas por Procurador/a de los Tribunales y asistidas por Letrado en ejercicio, ambos habilitados ante el Tribunal.

VI. CUANTÍA

Cumpliendo la exigencia del art. 253.1 LEC, se cifra la cuantía de la demanda en la cantidad de [IMPORTE] euros, conforme a la regla 1.ª del art. 251 LEC.

VII. CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VIII. FONDO DEL ASUNTO

1. Mi mandante ejercita la acción civil "ex delicto" derivada de la existencia de un ilícito penal, con fundamento en el art. 1.092 CCiv.

2. La acción se dirige contra:

a) El conductor imprudente, D./Dña. [NOMBRE Y APELLIDOS]
b) La compañía aseguradora de la conducción de éste, deudora solidaria de la indemnidad, como autoriza el art. 76 LCS 50/80.

En el plano de los daños en las personas, la normativa del seguro de responsabilidad civil del automóvil de suscripción obligatoria, modificada y rebautizada como Ley sobre Responsabilidad Civil y Seguro en la Circulación de Vehículos a Motor, por la Ley 30/1995 de 8 de noviembre, y actualmente recogida en el Texto Refundido aprobado por Real Decreto Legislativo 8/2004 de 29 de octubre (TRLRCSCVM), aísla un campo de relaciones sociales, la circulación de vehículos de motor, en que la responsabilidad civil no sigue un régimen subjetivo, como la tradición de la precitada batería normativa, y aunque no llega a suplantarse absolutamente la culpabilidad por causalidad, el elemento que atribuye la obligación de responder es la creación del riesgo —art. 1.1, párrafo 1.º TRLRCSCVM—, y las causas de exoneración se ciñen a la culpa exclusiva de la víctima o la fuerza mayor ajena a la conducción o al funcionamiento del vehículo —art. 1.1, párrafo 2.º TRLRCSCVM—. Por otro lado, la Ley predetermina la tasa adecuada o fijación de un "quantum" máximo para la reparación, conforme a las reglas del Anexo al TRLRCSCVM, que establece un sistema con baremos.

En el plano de los daños en los bienes, se mantiene el principio de la responsabilidad por culpa (art. 1.1, párrafo 3.º TRLRCSCVM), y el de la ’restitutio in integrum‘ del art. 1.902 CCiv, por la regla del art. 1.2 TRLRCSCVM, en relación con la inaplicabilidad del sistema del Anexo al TRLRCSCVM.

En el caso presente, se afirma la acción indiligente en la conducción de D./Dña. [NOMBRE Y APELLIDOS], y el evidente nexo causal con los daños y perjuicios cuya reparación se pide, en la persona y en el automóvil de D./Dña. [NOMBRE Y APELLIDOS]

3. Cuantificación de los daños.

3.1. Daños corporales. Conforme al régimen con baremos del Anexo al TRLRCSCVM, se reclaman las siguientes cantidades para restañar los daños y perjuicios:

Lesiones temporales (Tabla V baremo)

- días de asistencia hospitalaria por la cantidad de [IMPORTE] euros/día.

Subtotal [IMPORTE] euros

- días impeditivos por la cantidad de [IMPORTE] euros/día.

Subtotal [IMPORTE] euros.

- días no impeditivos la cantidad de [IMPORTE] euros/día.

Subtotal [IMPORTE] euros.

Lesiones permanentes (Tabla VI baremo)

- Cervicalgia irradiada a brazo derecho [Nº] puntos

- Cefaleas y mareos [Nº] puntos

- Lumbalgia [Nº] puntos

- Insensibilidad lingual [Nº] puntos

- Síndrome depresivo susceptible de desaparecer con el paso del tiempo [Nº] puntos

El subtotal asciende a [IMPORTE] euros, aplicando la fórmula legal del apartado 2 del Anexo, para caso de indemnizaciones concurrentes, con arreglo al valor del punto para su número y edad del demandante de la Tabla III del baremo.

Sobre estos subtotales, que se aquilatan, ha de aplicarse el factor de corrección del%, con arreglo a las tablas IV y V del baremo, por los ingresos netos de trabajo personal de D./Dña. [NOMBRE Y APELLIDOS], de [IMPORTE] euros anuales.

A efectos probatorios se acompaña copia de la declaración sobre el Impuesto de Renta de las Personas Físicas del ejercicio fiscal (documento número [Nº DE DOCUMENTO]), y se designan, con citación contraria, los archivos de la Administración Estatal de la Agencia Tributaria en

Total deeuros

3.2. Daños materiales. Se reclaman:

- Valor de mercado de segunda mano del vehículo, matriculado en el año, con arreglo al dictamen pericial del tasador D./Dña. [NOMBRE Y APELLIDOS], que se aporta como documento número [Nº DE DOCUMENTO].

Subtotal [IMPORTE] euros

- Gastos de servicio de grúa, con arreglo a la factura que se acompaña como documento número 13.

Subtotal [IMPORTE] euros.

Total de [IMPORTE] euros

4. La exoneración de los intereses por mora sólo se produce cuando el asegurador acredite haber presentado al perjudicado la oferta motivada de indemnización a que se refieren los arts 7.2 y 22.1 TRLRCSCVM. El art. 7.2 TRLRCSCVM introducido por Ley 21/2007, de 11 de julio, recoge la regulación del art. 22.1, sobre la reclamación de los perjudicados no residentes en España ante las entidades aseguradoras autorizadas en España o los representantes para tramitación y liquidación de siniestros por éstas designados en el resto de los Estados del Espacio Económico Europeo. Conforme a este sistema, en el plazo de tres meses desde la recepción de la reclamación del perjudicado, el asegurador debe una de dos conductas:

A) Presentar una oferta motivada de indemnización, cuando entienda acreditada la responsabilidad y cuantificado el daño.
B) Dar una respuesta motivada, porque entienda la aseguradora que no es probada responsable, resulta incuantificado el daño, o porque la reclamación haya sido rechazada.

Tal oferta o respuesta cuenta con un contenido legal mínimo, aunque reglamentariamente puede precisarse (art. 7.3, 4 y 5 TRLRCSCVM).

Por consiguiente, en el caso presente se han devengado los intereses de demora, por cuanto ha trascurrido el plazo de tres meses desde la reclamación de esta parte el [FECHA], sin que haya presentado una oferta motivada de indemnización ’por una causa no justificada o que le fuera imputable al asegurador‘.

La indemnización de todos los daños en este ámbito devenga intereses moratorios especiales, con ribete penitencial indiscutido, que se agrega al carácter de reparación adicional por el retraso culpable en el pago, al ser la obligada compañía de seguros, conforme a un sistema que representa excepción legal expresa a un principio jurisprudencial tradicional —de suyo, no es requisito de la común ’mora debitoris‘ del art. 1.100 CCiv—, y que sin carácter absoluto, en general rechaza la aplicación de intereses moratorios a los créditos de suma ilíquida, dentro de los que se hallan el derecho a las indemnizaciones de daños y perjuicios.

Sin negar que en alguna ocasión muy especial puedan percibirse circunstancias que indiquen justificado en estos casos no hacer pago o hacerlo en cantidad inferior a la debida, o que el impago pueda ser imputable a conducta del acreedor, el art. 9.b) TRLRCSCVM instaura un único mecanismo de conciliar iliquidez y ese acicate para el resarcimiento temprano de los damnificados, consistente en la declaración judicial de suficiencia de la consignación o pago verificado dentro de los tres meses desde la reclamación del perjudicado. Tal es el mecanismo de enervar estos intereses disuasorios, el cual no se ha utilizado en el asunto.

Por consiguiente, en modo alguno se ha enervado el devengo de intereses de mora para la aseguradora que establece el art. 20.4.ª LCS 50/80, con los dos tipos o réditos del interés de mora, con carácter de mínimos, uno del legal del dinero incrementado en el 50% y otro exacerbado del 20% anual, que procede para cuando el retraso culpable en el pago supere los dos años.

IX. COSTAS

El empleo del principio cuasiobjetivo del vencimiento del art. 394.1 LEC, conlleva el deber de reintegro de las costas procesales por la parte demandada, sin que existan dudas de hecho o derecho, ni vacilaciones jurisprudenciales sobre el objeto del proceso.

Por todo lo anteriormente expuesto,

AL TRIBUNAL SUPLICO,

que habiendo por presentado este escrito, con el poder que acredita la representación procesal, y los documentos acompañados, y copias de todo ello, se sirva admitir uno y otros, tener por formulada demanda de juicio ordinario, en nombre de quien comparezco, contra D./Dña. [NOMBRE Y APELLIDOS] y [NOMBRE DE LA PARTE], y seguidos que sean los trámites legales, dicte sentencia por la que estimando íntegramente esta demanda, se condene a los demandados a que indemnicen conjunta y solidariamente en la suma deeuros a mi representado D./Dña. [NOMBRE Y APELLIDOS], incrementadas en lo que representen los intereses de mora al tipo diario consistente en el legal vigente en la fecha de ocurrencia del siniestro incrementado en un cincuenta por ciento desde la fecha de ocurrencia del accidente o, en su caso, del veinte por ciento, respecto de la aseguradora codemandada, y los intereses legales desde la interpelación judicial respecto del otro codemandado, con lo demás que proceda en Justicia que pido en

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a
