---
name: demanda-divorcio-contencioso-extranjeros-no-civ-0310
description: "Demanda de divorcio contencioso de extranjeros no comunitarios residentes en España. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de divorcio contencioso de extranjeros no comunitarios residentes en España

> Formulario **CIV-0310** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda de divorcio contencioso de cónyuges extranjeros no comunitarios, residentes en España y con hijos menores, con aplicación del fuero de residencia.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de divorcio contencioso de extranjeros no comunitarios residentes en España» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de divorcio contencioso de extranjeros no comunitarios residentes en España” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-divorcio-contencioso-extranjeros-no-civ-0310`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (14 veces)
- [ ] LOCALIDAD (12 veces)
- [ ] NÚMERO (8 veces)
- [ ] NOMBRE DEL HIJO/A (6 veces)
- [ ] CALLE (5 veces)
- [ ] Nº DE DOCUMENTO (5 veces)
- [ ] FECHA DE NACIMIENTO (4 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] DENOMINACIÓN SOCIAL (3 veces)
- [ ] AÑO (2 veces)
- [ ] FECHA (2 veces)
- [ ] MES (2 veces)
- [ ] BENEFICIARIO
- [ ] COLEGIO
- [ ] LUGAR
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] NOMBRE DE LA MANDANTE
- [ ] NOMBRE DEL DEMANDADO
- [ ] NOMBRE DEL ESPOSO
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] PLAZO
- [ ] PÁGINA
- [ ] ÓRGANO

## Normas que cita el formulario

- art. 36.1 LEC
- art. 96 LOPJ
- art. 769 LEC
- art. 770 LEC
- art. 253 LEC
- art. 251 LEC
- art. 86 CC
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 9.4 CC
- art. 81.2.º CC
- art. 97 CC
- art. 97.4.º CC
- art. 160 CC
- art. 149 CC
- art. 91 CC
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

- Junto a «…IR: (SECCIÓN CIVIL) / (SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD)] DE [LOCALIDAD]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.
- Junto a «…zación ex art. 96 LOPJ, a las Secciones de Familia, Infancia y Capacidad que hay»: Denominación legal: Sección de Familia, Infancia y Capacidad. Si no existe en el partido, conoce la Sección Civil o la Única (art. 86.3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).

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

AL TRIBUNAL DE INSTANCIA [ELEGIR: (SECCIÓN CIVIL) / (SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD)] DE [LOCALIDAD]

D./Dña. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, que actúa en nombre y representación de [NOMBRE DEL REPRESENTADO/A], provista de documento de identidad n.º [NÚMERO], con domicilio en [LOCALIDAD], calle [CALLE], a virtud de poder para pleitos cuya copia acompaño para su unión a los autos mediante testimonio bastante, con ruego de devolución de la copia autorizada por necesitarla a otros usos, bajo dirección del Letrado D./Dña. [NOMBRE Y APELLIDOS], colegiada n.º [NÚMERO] del Iltre. Colegio de Abogados de [COLEGIO], cuyo despacho está abierto en [LOCALIDAD], calle [CALLE], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que por medio del presente escrito, siguiendo las instrucciones de mi mandante, vengo a formular demanda de DIVORCIO frente a su esposo [NOMBRE Y APELLIDOS], con domicilio actual en [LOCALIDAD], calle [CALLE], con base a los siguientes datos y argumentos:

HECHOS

PRIMERO.- Mi mandante contrajo matrimonio conforme a la ley islámica con [NOMBRE Y APELLIDOS] en [LOCALIDAD], el día [FECHA]

Se acompaña la correspondiente certificación de matrimonio expedida por el Registro Civil de [LOCALIDAD] (DOCUMENTO n.º [NÚMERO]).

De dicha unión nacieron dos hijos que son menores de edad, de nombre [NOMBRE DEL HIJO/A] y [NOMBRE DEL HIJO/A], nacidos el [FECHA DE NACIMIENTO], y el [FECHA DE NACIMIENTO], así pues, de ocho y cinco años de edad.

Se adjuntan las correspondientes certificaciones de nacimiento que ha emitido el Registro Civil de [LOCALIDAD] (DOCUMENTOS nos. y [Nº DE DOCUMENTO]).

SEGUNDO.- Tanto mi mandante como su esposo nacieron en Fez (Reino de Marruecos), [NOMBRE DE LA MANDANTE] el [FECHA DE NACIMIENTO], y [NOMBRE DEL ESPOSO] el [FECHA DE NACIMIENTO], siendo su nacionalidad común marroquí, pero habiendo inmigrado a España hace once años, y fijando su primera residencia común en [LOCALIDAD], de donde pasaron a [LOCALIDAD], calle [CALLE], n.º [NÚMERO], hasta que hace un año y ocho meses el demandado abandonara a su mujer e hijos.

Se acompañan el libro de familia, certificado de empadronamiento, y pasaporte de la actora como DOCUMENTOS nos. [Nº DE DOCUMENTO], [Nº DE DOCUMENTO] y [Nº DE DOCUMENTO].

TERCERO.- Los casados cesaron efectivamente su convivencia conyugal desde hace un año y ocho meses, sin que haya existido ulterior reanudación de la convivencia.

El demandado reside desde entonces en [LOCALIDAD], calle [CALLE], conforme acredito con certificado de empadronamiento que se acompaña como DOCUMENTO n.º [NÚMERO].

CUARTO.- El régimen económico que rige los aspectos económicos del matrimonio desde su comienzo es de plena separación de bienes, vigente como ley personal del marido -también la común de los cónyuges- al momento de contraer matrimonio, por lo que no es menester medida alguna en lo que se refiere al régimen económico matrimonial.

QUINTO.- Mi patrocinada se incorporó legalmente al mercado laboral ya el año [AÑO], en actividades de limpieza de edificios, pero nunca ha dejado hasta la actualidad de prestar servicios con trabajos a tiempo parcial y con contratos temporales, careciendo de estabilidad, habiendo percibido [IMPORTE] euros líquidos el pasado año, y [IMPORTE] euros líquidos en los cuatro primeros meses del año corriente, en labores de media jornada. Se adjunta certificación de haberes como DOCUMENTO n.º [NÚMERO].

SEXTO.- Para determinar los ingresos del demandado, de un lado, están los ingresos oficiales que percibe [NOMBRE DEL DEMANDADO] mediante nómina laboral, como gerente del Restaurante [ÓRGANO], propiedad de la mercantil [DENOMINACIÓN SOCIAL], de la que es socio fundador, titular del 20% del capital social, y administrador social único, y de otro lado, los beneficios que recibe por esta condición de socio y administrador.

En cuanto a los primeros, ingresos "oficiales", a mi representada le consta que el salario del demandado asciende aproximadamente a [IMPORTE] euros líquidos anuales, lo cual en caso de ser negado, podrá demostrarse por conducto de obtener de la Tesorería General de la Seguridad Social las bases de cotización, pero que resulta indiciariamente de: 1.º) La cifra que aparece en la página [PÁGINA] de las cuentas anuales de [DENOMINACIÓN SOCIAL] depositadas en el Registro Mercantil de [LOCALIDAD], donde se comprueba la partida de "retribución gerencia", y que se aporta subrayada en la certificación que hace el DOCUMENTO n.º [NÚMERO]; 2.º) La cantidad que aparece como abonos de nómina en favor de [BENEFICIARIO] en el último extracto de cuenta corriente de la Caja de Ahorros de [LOCALIDAD], del que tiene posesión mi mandante, de los meses [MES] y [MES] del año [AÑO] (DOCUMENTO n.º [NÚMERO]), cuando la familia convivía unida.

Por lo que toca a lo segundo, los beneficios sociales "clandestinos" por su participación en la sociedad del negocio ya referido, son de mucha más difícil captación, aunque se estiman en no menos de [IMPORTE] euros, lo que cabe inducir de gastos lujosos adverados, como es la adquisición del vehículo 4x4 marca "Lexus" matrícula 1124-DSH, cuyo valor de mercado asciende a [IMPORTE] euros (se acompaña certificación de la Delegación Provincial de Tráfico en tanto que DOCUMENTO n.º 11. Asimismo puede inferirse mediante presunciones "ad hominem" de que, según en periodo probatorio, por requerimiento documental a la contraparte, resultará de la diferencia entre los beneficios declarados en la cuentas anuales depositadas en el Registro Mercantil, y lo que se reflejaba en los denominados "Informes de resultados de gestión" en las Juntas de socios de [DENOMINACIÓN SOCIAL].

SÉPTIMO.- Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA.

La resolución de la pretensión de divorcio pertenece a la jurisdicción, y a tenor del art. 36.1 LEC, la extensión y límites de la jurisdicción de los tribunales civiles españoles se determinará por lo dispuesto en la Ley Orgánica del Poder Judicial y en los tratados y convenios internacionales en los que España sea parte.

Dicha normativa viene constituida por el Reglamento (UE) 2019/1111 del Consejo, de 25 de junio de 2019, relativo a la competencia, el reconocimiento y la ejecución de resoluciones en materia matrimonial y de responsabilidad parental, y sobre la sustracción internacional de menores.

En materia de matrimonio, el art.3.a) del Reglamento atribuye competencia para resolver las cuestiones relativas al divorcio, la separación judicial o la nulidad del matrimonio de los cónyuges, a los órganos jurisdiccionales del Estado miembro en cuyo territorio se encuentre la residencia habitual de los cónyuges.

Por su parte, el art. 7.1 del Reglamento, específicamente referido a la responsabilidad parental, establece como fuero de competencia general el Estado miembro el de residencia habitual del menor en el momento en que se presenta el asunto ante el órgano jurisdiccional.

Por lo tocante a la competencia objetiva corresponde a los Tribunales de Instancia, y con arreglo a la especialización ex art. 96 LOPJ, a las Secciones de Familia, Infancia y Capacidad que hay en esta ciudad.

La competencia territorial para conocer del proceso viene fijada por el art. 769 LEC, a los Tribunales a que me honro en dirigirme, que son los del último domicilio del matrimonio.

II.- PROCEDIMIENTO.

El procedimiento adecuado es el del art. 770 LEC para conocer de las demandas de divorcio contenciosas.

Se fija la cuantía de la demanda, en lo que tiene de estimable, desde el imperativo del art. 253 LEC, en base a la pretensión de medidas que incluye reclamaciones de pensiones periódicas, acumulada a la disolución del matrimonio, en [IMPORTE] euros, en armonía con la regla 7.ª del art. 251 LEC.

III.- PARTES.

Tienen capacidad para ser parte y procesal la actora y quien viene demandado, en cuanto que personas físicas mayores de edad en pleno ejercicio de sus derechos civiles (arts. 6.1.1.º y 7.1 LEC)

Ostentan legitimación ordinaria por hallarse en la situación jurídica de relación matrimonial ambos cónyuges (arts. 86 CCiviv y 10 LEC), siendo el objeto de la pretensión la disolución vincular por divorcio.

IV.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

V.- FUNDAMENTOS MATERIALES.

1) Derecho aplicable

AL DIVORCIO

En virtud de lo dispuesto en el art. 8.a) del Reglamento (UE) 1259/2010, será la del lugar donde los cónyuges tengan su residencia habitual en el momento de la interposición de la demanda. Por tanto, demostrado que ambos cónyuges siguen en España, no cabe duda de que es de aplicación la ley española.

A LAS RELACIONES PATERNO-FILIALES

Deberá aplicarse el derecho del foro según el art. 15 del Convenio de La Haya de 19 de octubre de 1996 relativo a la competencia, la ley aplicable, el reconocimiento, la ejecución y la cooperación en materia de responsabilidad parental y de medidas de protección de los niños.

El citado precepto incorpora la máxima lex fori in foro propio, estableciendo que las autoridades de los Estados contratantes aplicarán su propia ley cuando resulten internacionalmente competentes de conformidad con las disposiciones del Capítulo II del Convenio.

Ahora bien, dado que los menores respecto de los cuales se interesan las medidas residen habitualmente en España, la competencia judicial internacional viene determinada, no por los foros de competencia judicial internacional del dicho Capítulo II del Convenio de la Haya de 1996, sino por las disposiciones del Reglamento (CE) nº 2201/2003, de 27 de noviembre de 2003, relativo a la competencia, el reconocimiento y la ejecución de resoluciones judiciales en materia matrimonial y de responsabilidad parental, de conformidad con lo previsto en el art. 61.a) del propio Reglamento, que en materia de responsabilidad parental (cfr.: art. 8), otorga competencia a los órganos jurisdiccionales del Estado miembro de la residencia habitual del menor en el momento en el que se presenta el asunto ante dicho órgano jurisdiccional.

De este modo, una interpretación estricta del art. 15.1 del Convenio de La Haya de 1996 podría inducir a pensar que en supuestos como el que nos ocupa no resultaría de aplicación la norma de conflicto convencional, debiendo, entonces, tener que acudir a la norma de conflicto de producción interna, es decir, al art. 9.4 CCiv. No obstante lo dicho, de conformidad con acreditada doctrina científica (CALVO, CARRASCOSA), debe entenderse que si, como es el caso, el foro del Reglamento 2201/2003 en el cual el órgano jurisdiccional fundamenta su competencia judicial internacional, en tanto que incorpora idéntico criterio de atribución de competencia, es equivalente a uno de los que contempla el Convenio de la Haya de 1996, nada impide al Tribunal aplicar las normas de conflicto previstas en el citado Convenio. Dicha solución resulta conforme con el "espíritu conflictual" del Convenio, puesto que lleva a aplicar el Derecho material del Estado contratante cuyas autoridades resultan competentes en virtud de uno de los foros previstos en la propia norma convencional, cual es el de la residencia habitual del menor, incorporado en el art. 5.1 del Convenio de La Haya de 1996 (en este sentido, SAP Zaragoza de 20 de abril de 2012, rec. 146/2012).

A LOS ALIMENTOS A MENORES

Resulta de aplicación la ley española, por disposición del art. 15 del Reglamento (CE) nº 4/2009 del Consejo, de 18 de diciembre de 2008, relativo a la competencia, la ley aplicable, el reconocimiento y la ejecución de las resoluciones y la cooperación en materia de obligaciones de alimentos, que establece que se determinará de acuerdo con el Protocolo de La Haya de 23 de noviembre de 2007, cuyo art. 3 también fija el criterio de la residencia del menor, como ya hacía el art. 4 del Convenio de La Haya de 2 de octubre de 1973, al que ha venido a sustituir, como expresamente se establece en su art. 18.

2) Petición de divorcio

El fondo de la pretensión consiste en la declaración de divorcio, a fin de la disolución del matrimonio, a instancia de uno de los cónyuges, de conformidad con el art. 81.2.º CCiv, por remisión del art. 86 CCiv, después de transcurridos tres meses desde la celebración del matrimonio sin que puedan oponerse por el otro cónyuge, no expresamente conforme ninguna causa de oposición material, al fundarse en la voluntad de no permanecer casado, como corolario legal del derecho del art. 32 CE a contraer matrimonio.

VI.- MEDIDAS

VI.1.- PENSIÓN COMPENSATORIA. Para establecer una pensión compensatoria que se pide es de aplicación el art. 97 CCiv.

La finalidad de esta obligación de tracto sucesivo y cumplimiento periódico es evitar que la ruptura del vínculo matrimonial suponga para uno de los casados un descenso en el nivel de vida efectivamente gozado durante el matrimonio, que no debe confundirse con una aportación al levantamiento de las cargas del matrimonio, que viene a extinguirse con el divorcio, ni tampoco con los alimentos entre parientes.

El presupuesto básico para que nazca este derecho a pensión compensatoria es que el cónyuge solicitante sufra a causa de la ruptura matrimonial un desequilibrio económico, tomando como punto de referencia la posición del otro cónyuge, no sólo en una faceta patrimonial estricta, sino también teniendo en cuenta el déficit de beneficios, influencias, amistades o cualquier otra circunstancia, de forma que su consecuencia haya sido un empeoramiento de su situación anterior al matrimonio.

Un criterio jurisprudencial consolidado es que, si como aquí sucede, ambos cónyuges trabajan, deben compararse los ingresos respectivos.

También tiene relevancia, si a pesar de dedicarse cada cónyuge a su respectiva actividad remunerada, el cuidado del hogar o la atención a la familia recae en su mayor parte sobre uno de ellos, como acontece con mi representada en este asunto.

Teniendo en cuenta los criterios legales, ha de resaltarse unos datos acreditados en el plano objetivo, de dedicación pasada y futura a la familia (art. 97.4.º CCiv), duración del matrimonio y de la convivencia matrimonial de doce años (art. 97.6.º), y sobre todo, el caudal y medios económicos muy superiores del marido, al lado de una desproporción en las necesidades de uno y otro cónyuge, mayores en una madre con dos hijos pequeños (art. 97.8.º), a lo que deben agregarse otros datos en el plano subjetivo.

Porque el antedicho precepto no es una enumeración cerrada de criterios, como resulta de su propio tenor literal ("cualquier otra circunstancia relevante"), sin que la doctrina descarte tomar en consideración otras líneas de ponderación, como puede ser, sin duda, la culpabilidad en la crisis conyugal.

En consecuencia al desequilibrio económico objetivo, la dedicación a la familia de la esposa, la duración de la convivencia matrimonial, si se suma el grave daño moral causado a mi representada, justifican, teniendo en cuenta los medios económicos del demandado, una pensión compensatoria mensual de [IMPORTE] EUROS ( [IMPORTE] euros).

VI.2.- GUARDA Y CUSTODIA DE LOS HIJOS. Habida cuenta la edad de los dos hijos menores, y considerando su interés como el criterio rector de cualquier medida en relación con los mismos, carece de sentido que se posibilite la vivencia con el padre demandado, sin que haya ámbito por el momento a respetar inviables decisiones personales de los menores.

Es lo oportuno, por naturaleza, que la madre actora, hasta el momento quien ha vivido con los hijos comunes, desde el abandono del marido, retenga la guarda y custodia de éstos, sin perjuicio de que la patria potestad siga compartida por ambos progenitores.

VI.3.- DERECHO DE VISITA. Se postula, apercibida mi patrocinada de la desavenencia grave entre los cónyuges de cara a que pueda existir el consentimiento de ambos para la relación fluida con los hijos comunes, el siguiente régimen de visitas, de amplitud:

Fines de semana alternos, desde las 20.00 horas del sábado a las 21.00 horas del domingo; siete días durante las vacaciones escolares de Navidad, dos días durante las de Carnavales, y cuatro durante las de Semana Santa, y un mes durante las de verano; correspondiendo escoger dichos periodos vacacionales, en caso de desacuerdo, los años pares al padre y los impares a la madre.

Resulta de utilidad para regular el derecho de comunicación y visita del padre no custodio de los hijos menores en potestad lo prevenido en el art. 160 CCiv.

VI.4.- ALIMENTOS DE LOS MENORES. La prestación alimenticia para los hijos comunes, en tanto no se modifiquen las actuales circunstancias, de los escasos ingresos salariales de la madre demandante y de la pensión compensatoria que intente equilibrar su situación patrimonial en relación con la que gozaba casada, puesto que ésta prestará alimentos de forma directa, a través de la atención directa y proporcionando vivienda, ex art. 149 CCiv, sin asignación de cuota, desde el dinero de su salario y de la pensión compensatoria, supone que al otro progenitor, el padre demandado, le corresponde a través de una pensión en metálico, que se sumará a la compensatoria, con arreglo a los arts. 91, 92 y 93 CCiv, que calculamos en [IMPORTE] EUROS ( [IMPORTE] euros), estándose en cuanto a la fecha en que debe abonarse, a lo dispuesto en el art. 148, párrafo 2.º CCiv.

VII.- COSTAS.

Corresponde emplear el principio del vencimiento en punto a las costas procesales consagrado en el art. 394 LEC, debiéndose condenar al demandado que se oponga, dado que el obtener la razón precisando de un proceso no ha de suponer una merma patrimonial del que tiene razón, de acuerdo con la Ley.

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito con los documentos que se acompañan y sus copias, se digne admitirlos, tenerme por comparecido y parte en la representación que ostento, entendiéndose conmigo las sucesivas diligencias y por formulada demanda de disolución del matrimonio por divorcio, de modo que seguido que sea el pertinente procedimiento, se dicte en su día sentencia por la que:

SE DECLARE EL DIVORCIO de los espososy

SE OFICIE a su firmeza al Registro Civil depara la anotación de su parte dispositiva en la inscripción del matrimonio.

SE ACUERDEN LAS SIGUIENTES MEDIDAS DEFINITIVAS, que se podrán modificar si se alteraren sustancialmente las circunstancias:

1.- Atribución de la guarda y custodia de los hijos menores [NOMBRE DEL HIJO/A] y [NOMBRE DEL HIJO/A] a la demandante, en cuya compañía conviven, conservándose la patria potestad compartida por ambos progenitores.
2.- Derecho de comunicación y visita con dichos hijos menores de su padre conforme a lo expuesto en el fundamento de derecho V.3.
3.- Establecimiento de sendas pensiones alimenticias a favor de los hijos comunes menores de edad, [NOMBRE DEL HIJO/A] y [NOMBRE DEL HIJO/A], de [IMPORTE] EUROS ( [IMPORTE] euros) cada una y en doce mensualidades al año, a cargo del demandado, con efectos desde la fecha de interposición de esta demanda, pagaderas dentro de [PLAZO], mediante el sistema que se establezca en ejecución, si fuere menester.
4.- Concesión a la esposa de una pensión compensatoria de [IMPORTE] EUROS ( [IMPORTE] euros) mensuales y en doce mensualidades al año, a cargo del demandado, con efectos desde la fecha de la sentencia, pagaderas por meses anticipados, mediante el sistema que se establezca en ejecución, si fuere menester.
5.- Las anteriores pensiones serán actualizables anualmente, a partir del primero de enero del año siguiente a la fecha de la sentencia, conforme a los incrementos que experimente el Índice de Precios al Consumo que publique el Instituto Nacional de Estadística, u organismo oficial que lo sustituya.

Todo ello con condena en costas al demandado, si se opusiera a la presente demanda.

Es Justicia de hacerse en [LUGAR], a [FECHA].

OTROSÍ DIGO: Que por necesitar para otros usos la copia de escritura de poder acreditativa de la representación del suscrito Procurador, intereso y

SUPLICO AL TRIBUNAL que, por causada la antecedente manifestación, se sirva acordar el desglose y devolución del poder a esta parte, dejando en autos testimonio del mismo.

Reitero Justicia en lugar y fecha "ut supra ".

Firma del Abogado/a	Firma del Procurador/a

========================================================================
