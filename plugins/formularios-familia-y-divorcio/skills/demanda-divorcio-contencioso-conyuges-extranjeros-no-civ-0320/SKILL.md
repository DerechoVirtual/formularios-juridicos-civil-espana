---
name: demanda-divorcio-contencioso-conyuges-extranjeros-no-civ-0320
description: "Demanda de divorcio contencioso de cónyuges extranjeros no comunitarios por fuero de los demandantes. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de divorcio contencioso de cónyuges extranjeros no comunitarios por fuero de los demandantes

> Formulario **CIV-0320** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda de divorcio contencioso presentada ante un tribunal español por cónyuges extranjeros no comunitarios (en el modelo, de nacionalidad colombiana y sin hijos menores), con aplicación del Derecho extranjero común y fuero de la residencia de la parte demandante. Se usa cuando el último domicilio conyugal estuvo en España, la parte demandada reside en el extranjero y debe acreditarse el Derecho aplicable.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de divorcio contencioso de cónyuges extranjeros no comunitarios por fuero de los demandantes» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de divorcio contencioso de cónyuges extranjeros no comunitarios por fuero de los demandantes” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-divorcio-contencioso-conyuges-extranjeros-no-civ-0320`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] AÑO (7 veces)
- [ ] MES (7 veces)
- [ ] DÍA (5 veces)
- [ ] Nº DE DOCUMENTO (5 veces)
- [ ] DOMICILIO (3 veces)
- [ ] EDAD (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] NOMBRE DEL HIJO/A (3 veces)
- [ ] NOMBRE Y APELLIDOS DEL DEMANDADO/A (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] PAÍS (3 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] NOMBRE Y APELLIDOS DE LA DEMANDANTE (2 veces)
- [ ] AUTORIDAD CENTRAL DEL ESTADO EXTRANJERO
- [ ] AUTORIDAD EXTRANJERA QUE EXPIDE LA CERTIFICACIÓN
- [ ] COLEGIO
- [ ] CÓDIGO DE INSCRIPCIÓN
- [ ] DENOMINACIÓN SOCIAL
- [ ] DEPARTAMENTO/PROVINCIA
- [ ] DIRECCIÓN ELECTRÓNICA
- [ ] LOCALIDAD Y PAÍS DE INSCRIPCIÓN DEL MATRIMONIO
- [ ] LOCALIDAD Y PAÍS DE ORIGEN
- [ ] LOCALIDAD, DEPARTAMENTO/PROVINCIA Y PAÍS
- [ ] MARCA
- [ ] MATRÍCULA
- [ ] MUNICIPIO
- [ ] NIE
- [ ] NOMBRE Y APELLIDOS DEL LETRADO/A
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº DE COLEGIADO
- [ ] Nº DE DOCUMENTOS
- [ ] PAÍS DE LA NACIONALIDAD COMÚN
- [ ] PRECEPTO EXTRANJERO SOBRE EL RÉGIMEN ECONÓMICO MATRIMONIAL
- [ ] SEDE

## Normas que cita el formulario

- art. 36.1 LEC
- art. 9.2 LOPJ
- art. 96 LOPJ
- art. 769 LEC
- art. 10 LEC
- art. 23 LEC
- art. 770 LEC
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 9.2 CC
- art. 164 Código Civil
- art. 281 LEC
- art. 152 Código Civil
- art. 156 Código Civil
- art. 160 Código Civil
- art. 162.1 Código Civil
- art. 394 LEC
- art. 154 Código Civil

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

- Junto a «… de Justicia y, en el país de origen, [AUTORIDAD CENTRAL DEL ESTADO EXTRANJERO].»: adaptar este párrafo al convenio aplicable según el Estado cuyo Derecho se invoque.
- Junto a «…, a falta de mejor acuerdo, pueda tener que decidirse en ejecución de sentencia.»: los fundamentos de Derecho material de este apartado corresponden al Derecho colombiano del modelo original; si el Derecho aplicable es el de otro Estado, sustitúyanse por los preceptos y la doctrina del ordenamiento extranjero que corresponda y acredítense conforme al art. 281 LEC.
- Junto a «…OCALIDAD], a [DÍA] de [MES] de [AÑO]. Firma del Abogado/a Firma del Procurador/a»: requisito de procedibilidad (art. 5 LO 1/2025): antes de demandar hay que intentar un medio adecuado de solución de controversias y acreditarlo con la demanda, salvo las materias excluidas del art. 5.2. Los procesos de divorcio, al versar sobre materias de Derecho de familia indisponibles en parte, deben contrastarse con las exclusiones del art. 5.2 antes de exigir o acreditar el intento negociador.

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

A LA SECCIÓN CIVIL (SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD) DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, [ELEGIR: en virtud de designación de oficio / en nombre y representación] de D./Dña. [NOMBRE Y APELLIDOS DE LA DEMANDANTE], de nacionalidad [NACIONALIDAD], bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS DEL LETRADO/A], colegiado/a n.º [Nº DE COLEGIADO] del Ilustre Colegio de Abogados de [COLEGIO], [ELEGIR: igualmente en virtud de designación de oficio / de libre designación], ante el Tribunal comparezco y, como mejor proceda en Derecho, DIGO:

Que por medio del presente escrito interpongo DEMANDA DE DIVORCIO contra D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO/A], de nacionalidad [NACIONALIDAD], residente en [PAÍS], con domicilio en [DOMICILIO], en base a los siguientes:

HECHOS

PRIMERO.– Matrimonio.

Mi representada y D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO/A] contrajeron matrimonio civil en [PAÍS], [DEPARTAMENTO/PROVINCIA], [MUNICIPIO], inscrito en el Registro Civil de dicha localidad, con código [CÓDIGO DE INSCRIPCIÓN], según se acredita mediante la certificación de dicho Registro Civil que se aporta como documento número [Nº DE DOCUMENTO] de la presente demanda.

SEGUNDO.– Hijos.

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]
— De dicho matrimonio nacieron [NÚMERO] hijos: [NOMBRE DEL HIJO/A], en fecha [DÍA] de [MES] de [AÑO], que en la actualidad cuenta con [EDAD] años de edad; [NOMBRE DEL HIJO/A], en fecha [DÍA] de [MES] de [AÑO], que en la actualidad cuenta con [EDAD] años de edad; y [NOMBRE DEL HIJO/A], en fecha [DÍA] de [MES] de [AÑO], que en la actualidad cuenta con [EDAD] años de edad. Por tanto, los hijos habidos del matrimonio son mayores de edad.
— De dicho matrimonio no han nacido hijos.

Se acompañan los certificados de nacimiento como documentos números [Nº DE DOCUMENTOS].

TERCERO.– Domicilio conyugal.

El domicilio conyugal ha venido trasladándose según las circunstancias familiares. Hasta el año [AÑO] el matrimonio residió en [LOCALIDAD Y PAÍS DE ORIGEN], país de origen de ambos; después ambos pasaron a residir en España, fijando el domicilio conyugal en la calle [DOMICILIO] de [LOCALIDAD], donde continúa residiendo la demandante.

Se acompaña como documento número [Nº DE DOCUMENTO] el volante de empadronamiento.

CUARTO.– Causas de la separación.

[EXPOSICIÓN DE LAS CAUSAS DE LA RUPTURA CONFORME AL DERECHO EXTRANJERO APLICABLE. En el modelo original: durante aproximadamente cinco años los cónyuges estuvieron separados de hecho en el país de origen, debido a las continuas infidelidades del demandado y a la situación económica, al no contribuir prácticamente al sostenimiento de la familia; la demandante emigró a España, comenzó a trabajar y trajo posteriormente a sus hijos; hace año y medio el esposo solicitó una nueva oportunidad y se reanudó la convivencia en común hacia mediados del mes de [MES] de [AÑO]; en el mes de [MES] siguiente la demandante tuvo conocimiento de que el esposo seguía manteniendo una relación con otra persona en el país de origen, a la que enviaba dinero todos los meses y que estaba embarazada de un hijo de aquel; tras dichos acontecimientos, el demandado se marchó del domicilio familiar y volvió a su país de origen, fijando su residencia en la localidad de [LOCALIDAD], donde también residen sus padres, llevando ambos cónyuges vidas perfectamente separadas.]

QUINTO.– Régimen económico matrimonial.

El régimen económico del matrimonio es el de [RÉGIMEN ECONÓMICO MATRIMONIAL, p. ej. sociedad de bienes gananciales], por lo que con el divorcio queda finalizado dicho régimen.

El matrimonio posee los siguientes bienes en común:

El inmueble sito en calle [DOMICILIO], n.º [NÚMERO], [LOCALIDAD, DEPARTAMENTO/PROVINCIA Y PAÍS], que constituía el domicilio conyugal en un principio.

El vehículo marca [MARCA], matrícula [MATRÍCULA], cuya titularidad en la DGT corresponde al demandado. El pago de dicho vehículo, aunque se efectuó a la financiera [DENOMINACIÓN SOCIAL], estando casados actora y demandado, y precisamente cuando el segundo había vuelto, reconciliado, a España, fue dinero de exclusiva propiedad de la actora, de manera que ello tiene que considerarse donación reintegrable a la liquidación de la comunidad conyugal.

En el momento procesal oportuno se solicitará por esta parte la liquidación del régimen económico matrimonial.

SEXTO.– Proceso de negociación previo y medios de solución de controversias de manera amistosa y extrajudicial.

Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO: mediación, conciliación privada, opinión neutral de persona experta independiente, oferta vinculante confidencial, negociación directa con o sin abogado, proceso de Derecho colaborativo u otra actividad negociadora reconocida en ésta u otras leyes, estatales o autonómicas], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento n.º [Nº DE DOCUMENTO] [DOCUMENTO QUE ACREDITA QUE SE HA ACUDIDO A UN MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS].

FUNDAMENTOS DE DERECHO

I. Jurisdicción y competencia.

Competencia internacional. La resolución de la pretensión de divorcio pertenece a la jurisdicción española y, a tenor del art. 36.1 LEC, la extensión y límites de la jurisdicción de los tribunales civiles españoles se determinará por lo dispuesto en la Ley Orgánica del Poder Judicial y en los tratados y convenios internacionales en los que España sea parte.

Dicha normativa viene constituida por el Reglamento (UE) 2019/1111 del Consejo, de 25 de junio de 2019, relativo a la competencia, el reconocimiento y la ejecución de resoluciones en materia matrimonial y de responsabilidad parental, y sobre la sustracción internacional de menores, cuyo art. 3.a), segundo guion, atribuye competencia a los tribunales españoles, al ser los órganos jurisdiccionales correspondientes al último lugar de residencia habitual de los cónyuges, teniendo aún la demandante su residencia en España.

Competencia genérica. Está atribuida al orden civil de jurisdicción, conforme al art. 9.2 LOPJ.

Competencia objetiva. Corresponde a los Tribunales de Instancia y, con arreglo a la especialización ex art. 96 LOPJ, a las Secciones de Familia, Infancia y Capacidad que haya en esta ciudad.

Competencia territorial. Se asigna desde el art. 769 LEC a los tribunales del último domicilio del matrimonio.

II. Partes.

Capacidad. Las partes poseen capacidad para ser parte y capacidad procesal, en cuanto que personas físicas mayores de edad en pleno ejercicio de sus derechos civiles (arts. 6.1.1.º y 7.1 LEC).

Legitimación. Ostentan las partes legitimación ordinaria por ocupar la posición de cónyuges en la situación jurídica de relación matrimonial (art. 10 LEC), siendo el objeto de la pretensión la disolución del vínculo por divorcio.

Postulación. El mandato procesal de la actora mediante procurador de los tribunales, y la correlativa dirección de abogado para su defensa, cumple los presupuestos de postulación conforme a lo establecido en los arts. 23 y 31 LEC.

III. Procedimiento.

El procedimiento a través del que ha de sustanciarse la pretensión es el recogido en el art. 770 LEC.

IV. Cumplimiento de los requisitos de procedibilidad.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4.º y 399.3 en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

V. Fondo del asunto.

Derecho aplicable. Se invoca la aplicación de la legislación de [PAÍS DE LA NACIONALIDAD COMÚN], al concurrir las circunstancias previstas en el art. 8.c) del Reglamento (UE) n.º 1259/2010 del Consejo, de 20 de diciembre de 2010, por el que se establece una cooperación reforzada en el ámbito de la ley aplicable al divorcio y a la separación judicial, ostentar ambos cónyuges dicha nacionalidad extranjera común, y haber transcurrido más de un año desde la ruptura convivencial.

A tal efecto se aporta la copia del certificado de residencia y trabajo de la mandante, con número de identificación de extranjería [NIE] (documento número [Nº DE DOCUMENTO]).

Lo cual resulta coherente tanto con la cláusula general del Derecho internacional privado español del art. 9.2 CCiv, conforme a la que los efectos del matrimonio se rigen por la ley personal común de los cónyuges al tiempo de contraerlo, como con el Derecho internacional privado del país de origen, [NORMA DE DERECHO INTERNACIONAL PRIVADO EXTRANJERO APLICABLE, p. ej. en el modelo, el art. 164 del Código Civil colombiano, que para el divorcio decretado en el exterior respecto del matrimonio civil celebrado en dicho país impone que se rija por la ley del domicilio conyugal].

Acreditación. De conformidad con el art. 281 LEC, además de los hechos relativos a la tutela judicial solicitada en el proceso, es objeto de prueba la costumbre y el derecho extranjero, el cual deberá ser probado en lo que respecta a su contenido y vigencia, pudiendo valerse el tribunal de cuantos medios de averiguación estime necesarios para su aplicación.

Se aporta certificación de la legislación [PAÍS] realizada a través de la Subdirección General de Cooperación Jurídica Internacional del Ministerio de Justicia, de fecha [DÍA] de [MES] de [AÑO], por [AUTORIDAD EXTRANJERA QUE EXPIDE LA CERTIFICACIÓN] (documento número [Nº DE DOCUMENTO]).

El procedimiento para acreditar cualquier aspecto de la legislación extranjera ante las autoridades judiciales españolas es el previsto, en el modelo, por la Convención Interamericana sobre Prueba e Información acerca del Derecho Extranjero, hecha en Montevideo el 8 de mayo de 1979 (BOE n.º 11, de 13 de enero de 1988), por conducto de la Autoridad Central que a los efectos del citado Convenio sea designada en el Estado parte de que se trate, que en el Reino de España es la Subdirección General de Cooperación Jurídica Internacional del Ministerio de Justicia y, en el país de origen, [AUTORIDAD CENTRAL DEL ESTADO EXTRANJERO].

De acuerdo con dicha certificación, el régimen del divorcio está consagrado en [NORMA EXTRANJERA, p. ej. Título VII, Libro Primero del Código Civil del país (arts. 153 a 164 en el modelo)], cuyo tenor se reproduce en la certificación en [NÚMERO] páginas, que además incorpora los preceptos del título correspondiente a la separación de cuerpos. La primera parte de la certificación establece la tabla de vigencias.

De conformidad con [PRECEPTO EXTRANJERO SOBRE EL RÉGIMEN ECONÓMICO MATRIMONIAL], por el hecho del matrimonio se contrae sociedad de bienes entre los cónyuges, según las reglas del título correspondiente de dicho Código Civil.

Para que el juzgador pueda acceder con facilidad a otras disposiciones de la legislación extranjera, puede serle de utilidad el empleo de Internet, a través de la dirección electrónica oficial de la base de datos de legislación del Estado de que se trate: [DIRECCIÓN ELECTRÓNICA].

Pretensiones ejercibles.

Disolución del vínculo por causa legal. De acuerdo con el art. 152 del Código Civil del país de origen [en el modelo, Colombia], el matrimonio civil se disuelve por la muerte real o presunta de uno de los cónyuges o por divorcio judicialmente decretado.

Causas. Son causales de divorcio según el art. 154, entre otras: 1.ª) La relación sexual extramatrimonial de uno de los cónyuges. La última versión del precepto procede del art. 6 de la Ley 25 de 1992, habiéndose declarado inexequible el párrafo «salvo que el demandante las haya consentido, facilitado o perdonado» en la Sentencia de la Corte Constitucional C-660-00, de 8 de junio de 2000, mientras que la propia causal ha sido declarada exequible en la Sentencia de la Corte Constitucional C-821-05, de 9 de agosto de 2005. 2.ª) El grave e injustificado incumplimiento por parte de alguno de los cónyuges de sus deberes de marido o de padre y de esposa o de madre.

En este juicio se ejerce pretensión de disolución del vínculo por las causas invocadas, recogidas en ese art. 154, causales 1.ª y 2.ª. Debe tenerse en cuenta que el art. 164 del Código Civil colombiano dispone que este divorcio, que se declarará fuera de Colombia respecto del matrimonio civil celebrado en Colombia, no producirá los efectos de disolución sino a condición de que la causal respectiva sea admitida por la ley colombiana.

Derecho de acción. Con arreglo al art. 156 del Código Civil colombiano, el divorcio solo podrá ser demandado por el cónyuge que no haya dado lugar a los hechos que lo motivan y dentro del término de un año, contado desde cuando tuvo conocimiento de ellos respecto de la causal 1.ª, y en todo caso dentro de los dos años siguientes a su ocurrencia, mientras que el «dies ad quem» de la pretensión de divorcio por causal 2.ª es el de los dos años desde cuando sucedieron los hechos.

Efectos. El art. 160 del Código Civil colombiano establece los efectos legales al admitirse la demanda de divorcio, que estimamos es una norma procesal, debiéndose aplicar la «lex fori», pero hay dos efectos materiales del divorcio que interesa destacar a esta parte:

A) Conforme al art. 160, firme la sentencia que decreta el divorcio, además de quedar disuelto el vínculo del matrimonio civil y disuelta la sociedad conyugal, y no habiendo en este asunto hijos comunes menores sujetos a potestad, subsisten, según el caso, los derechos y deberes alimentarios de los cónyuges entre sí.

B) En armonía con el art. 162.1 del Código Civil colombiano, en los casos de las causales 1.ª y 2.ª del art. 154, que aquí se invocan, el cónyuge inocente puede revocar las donaciones que por causa de matrimonio hubiere hecho al cónyuge culpable, sin que este pueda invocar derechos o concesiones estipulados exclusivamente en su favor en capitulaciones matrimoniales.

Lo segundo se deja manifiesto de cara a las condiciones de la división de bienes gananciales de la liquidación que, a falta de mejor acuerdo, pueda tener que decidirse en ejecución de sentencia.

VI. Costas.

Deberá ser impuesto a la contraparte el reembolso de las costas del proceso, en virtud de lo establecido en el art. 394 LEC.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito de demanda junto con sus documentos y copias, se sirva admitirlo, y habiéndome por personado y parte por quien comparezco, y por formulada demanda de divorcio matrimonial de D./Dña. [NOMBRE Y APELLIDOS DE LA DEMANDANTE] respecto de D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO/A], y seguido que sea el trámite legal oportuno, con emplazamiento de la parte demandada a través de la correspondiente comisión rogatoria por el Tribunal, en atención a su lugar de residencia, dicte sentencia por la que:

1.– Se declare la disolución del matrimonio entre las partes por divorcio, fundado en las causales 1.ª y 2.ª del artículo 154 del Código Civil [del Estado cuyo Derecho se aplica] en vigor.

2.– Se declare la disolución del régimen económico matrimonial.

3.– Se ordene el asiento de la sentencia firme de divorcio en el Registro Civil de [LOCALIDAD Y PAÍS DE INSCRIPCIÓN DEL MATRIMONIO].

Todo ello con expresa condena en costas a la parte contraria, si se opusiera.

Es justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a Firma del Procurador/a
