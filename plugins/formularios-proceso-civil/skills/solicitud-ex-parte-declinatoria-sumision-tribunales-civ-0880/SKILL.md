---
name: solicitud-ex-parte-declinatoria-sumision-tribunales-civ-0880
description: "Solicitud ex parte de declinatoria por sumisión a tribunales extranjeros (DIPr autónomo). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud ex parte de declinatoria por sumisión a tribunales extranjeros (DIPr autónomo)

> Formulario **CIV-0880** del plugin **Proceso civil: demandas, contestaciones, prueba y vista** (`formularios-proceso-civil`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 24-11-2026.

## Qué es

ESCRITO DE SOLICITUD (EX PARTE) DE DECLINATORIA DE JURISDICCIÓN POR SUMISIÓN A TRIBUNALES EXTRANJEROS (DERECHO INTERNACIONAL PRIVADO AUTÓNOMO)

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud ex parte de declinatoria por sumisión a tribunales extranjeros (DIPr autónomo)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud ex parte de declinatoria por sumisión a tribunales extranjeros (DIPr autónomo)” para mi caso». También puedes invocarla directamente con `/formularios-proceso-civil:solicitud-ex-parte-declinatoria-sumision-tribunales-civ-0880`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-proceso-civil:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso civil: demandas, contestaciones, prueba y vista) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] Nº DE PROCEDIMIENTO (4 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] SEDE (2 veces)
- [ ] ÓRGANO JUDICIAL (2 veces)
- [ ] AÑO
- [ ] COLEGIO
- [ ] DÍA
- [ ] FECHA
- [ ] LUGAR
- [ ] MES
- [ ] Nº DE COLEGIADO
- [ ] Nº DE COLEGIADO/A
- [ ] NÚMERO
- [ ] TIPO Y Nº DE PROCEDIMIENTO

## Normas que cita el formulario

- art. 39 LEC
- art. 64 LEC
- art. 23.1 LEC
- art. 24.1 LEC
- art. 63.1 LEC
- art. 64.1 LEC
- art. 63.2 LEC
- art. 65 LEC
- art. 36.1 LEC
- art. 57 LEC
- art. 1255 CC
- art. 1255 Código Civil

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

- Junto a «…dimiento ….. n.º [NÚMERO] A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

Tribunal de Instancia de [SEDE]

Autos de Procedimiento ….. n.º [NÚMERO]

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./D.ª [NOMBRE Y APELLIDOS] Procurador/a de los Tribunales, en nombre y representación de D./D.ª [NOMBRE Y APELLIDOS], en virtud de apoderamiento apud acta/poder notarial según tengo acreditado en autos de juicio [Nº DE PROCEDIMIENTO] seguidos ante el Tribunal [ÓRGANO JUDICIAL] y asistido de la intervención del Letrado/a D./D.ª [NOMBRE Y APELLIDOS], Abogado del Ilustre Colegio de [COLEGIO], con número de colegiado [Nº DE COLEGIADO/A].

Comparezco ante el Tribunal [ÓRGANO JUDICIAL] en sede de Autos [TIPO Y Nº DE PROCEDIMIENTO] a los únicos efectos del presente escrito, y como mejor proceda en Derecho,

DIGO

Que por el presente escrito, y al amparo de los artículos 39 y 63 LEC, interpongo EXCEPCIÓN DE DECLINATORIA DE JURISDICCIÓN, en plazo legal y con los efectos de suspensión del presente procedimiento, hasta resolución del presente incidente, conforme dispone el artículo 64 LEC: “La declinatoria se habrá de proponer dentro de los diez primeros días del plazo para contestar a la demanda, y surtirá el efecto de suspender, hasta que sea resuelta, el plazo para contestar y el curso del procedimiento principal”.

Esta excepción de declinatoria de jurisdicción es procedente con base en los siguientes

HECHOS

Único.—Esta parte demandada ha sido notificada en fecha [FECHA] de la demanda de Juicio [Nº DE PROCEDIMIENTO] contra mi representada, Sociedad [DENOMINACIÓN SOCIAL], cuya sede social está en [DOMICILIO] promovido por la Sociedad [DENOMINACIÓN SOCIAL], con sede social en [DOMICILIO]. La causa de dicho procedimiento es (según el demandante), la falta de pago de un contrato de compraventa internacional de mercancías. Dicho contrato contiene una cláusula de sumisión expresa a los Tribunales del Estado de [LOCALIDAD].

Se aportan los documentos [Nº DE DOCUMENTO] acreditativos del domicilio de mi representado así como del citado contrato que contiene la cláusula de sumisión expresa.

Sobre los hechos manifestados, así como de la excepción de incompetencia de jurisdicción que se denuncia por medio del presente escrito, son de aplicación los subsiguientes,

FUNDAMENTOS DE DERECHO

Primero. De orden procesal.

I. Legitimación, capacidad para ser parte y postulación procesal.

Debe tenerse por comparecida a la demandada en el presente procedimiento a los únicos efectos de oponer la excepción de declinatoria de jurisdicción, encontrándose debidamente postulada de conformidad con el artículo 23.1 LEC en la representación del Procurador/a de los Tribunales, D./D.ª [NOMBRE Y APELLIDOS], legalmente habilitado, y bajo la preceptiva intervención letrada del colegiado/a D./D.ª [NOMBRE Y APELLIDOS] todo ello conforme a los artículos 24.1 y 31 de la LEC.

La legitimación de la parte a la que represento, a los presentes efectos, deviene por ser la demandada en Autos de Juicio [Nº DE PROCEDIMIENTO] y de conformidad con lo dispuesto en el artículo 63.1 LEC y, paralelamente, en el artículo 39 de la LEC.

La comparecencia ante el presente Tribunal, se realiza en plazo legal de diez días del artículo 64.1 LEC.

II. Competencia.

De conformidad con el artículo 63.2 LEC la competencia para resolver sobre la excepción de declinatoria de Jurisdicción corresponde al “mismo tribunal que esté conociendo del pleito y al que se considere carente de jurisdicción o de competencia (...)”. Siendo que en este Tribunal se siguen los autos de procedimiento [Nº DE PROCEDIMIENTO] contra mi representado, es por lo que resulta competente para resolver el presente incidente.

III. Tramitación.

Se denuncia la falta de jurisdicción del Tribunal que conoce de los presentes Autos, en legal plazo del artículo 64.1 LEC por lo que ha de admitirse la excepción de Declinatoria internacional, debiendo seguirse los demás trámites legales regulados en el artículo 65 LEC.

IV. Efectos inmediatos.

Procede la inmediata suspensión de los Autos del procedimiento principal hasta la resolución de la presente excepción de declinatoria internacional, según dispone el artículo 64.1 LEC. Procede igualmente la suspensión del cómputo de los plazos producidos por la notificación de la demanda a mi representado.

Segundo. Sobre la falta de competencia judicial internacional.

La acción que ejerce la sociedad demandante contra mi representado/a deviene por supuesto incumplimiento y falta de ejecución del contrato de compraventa aportado a los presentes Autos, [Nº DE DOCUMENTO]. Consta en el mismo contrato una cláusula de sumisión expresa a favor de los Tribunales de [LOCALIDAD], para someter toda contienda que en cumplimiento del contrato se pudiese producir entre las partes presentes. Esta cláusula de sumisión expresa tiene pleno efecto en la presente litis y para las partes.

Para decidir sobre su procedencia y efecto inhibitorio de la jurisdicción de este Tribunal es de aplicación, en primer lugar, el artículo 36.1 LEC, que establece que para resolver sobre la extensión y límites de la jurisdicción de los tribunales españoles, serán de aplicación los Tratados y Convenios Internacionales de los que España sea parte y, en su defecto, la normativa española.

En la materia sobre la que versa la acción de la actora principal, no existe Convenio Internacional aplicable. Tampoco cabe sustentar la Jurisdicción de España al amparo del Reglamento (UE) nº 1215/2012 del Parlamento Europeo y del Consejo, de 12 de diciembre de 2012, relativo a la competencia judicial, el reconocimiento y la ejecución de resoluciones judiciales en materia civil y mercantil, pues no es aplicación a la presente litis ya que la parte actora ha suscrito un acuerdo de sumisión expresa a favor de Tribunales no comunitarios, cuestión que excluye la aplicación del Reglamento de conformidad con el artículo 25.1.

Únicamente procede, para resolver sobre la presente Excepción de jurisdicción de declinatoria, la aplicación del Derecho Internacional Privado autónomo. Es en su aplicación por la que se debe proceder a la inhibición de la Jurisdicción de los Tribunales españoles por efecto DEROGATIO FORI del acuerdo de sumisión contenido en la cláusula del contrato de compraventa mercantil internacional. La vigencia y prueba de que existe un pacto de sumisión entre las partes, necesariamente conlleva la declaración de inhibición jurisdiccional de este Tribunal para conocer de la cuestión principal.

Entiende así la parte demandada a la que represento, que la existencia de un acuerdo de sumisión a un Tribunal extranjero supone “corresponder el conocimiento de ésta a tribunales extranjeros”, aceptado en nuestra Ley procesal el efecto derogatio fori generado por el acuerdo de sumisión (artículo 57 LEC).

La Jurisprudencia reciente ha evolucionado hacia la admisibilidad de la declinatoria de jurisdicción internacional, por efecto de pacto de sumisión expresa de las partes. Así, mientras que en los años 90 se consideraba (Sentencia del Tribunal Supremo de 18 de junio de 1990, entre otras) que un pacto de tal naturaleza “provocaría el riesgo de que por una supuesta sumisión de los interesados se pudiera eludir el conocimiento de litigios que vengan atribuidos a Jueces y Tribunales españoles con la consiguiente sustracción de los imperativos que ligan la Jurisdicción a la Soberanía nacional”, hoy, las líneas jurisprudenciales establecen el respeto a dichos pactos entre las partes, pues los pactos de sumisión no tienen un fin en fraude de Ley como han venido sosteniendo en algunas de las Audiencias Provinciales que no son jurisprudencia vinculante (Sentencia de la Audiencia Provincial de Badajoz de 23 marzo de 2001, rec. 177/2000 o Auto de la Audiencia Provincial de Zaragoza de 3 de abril de 2001).

Bien al contrario, la Jurisprudencia española actualmente desvincula los acuerdos de sumisión del fraude procesal y los considera plenamente válidos, puesto que el objeto de estos pactos pertenece al ámbito de la autonomía negocial de las partes, lo que está permitido por el artículo 1255 CC. Éste es el tenor de la actual Jurisprudencia contenida en la Sentencia del Tribunal Supremo de 31 de octubre de 2007, rec. 3219/2000 (“no cabe hablar de fraude de Ley cuando la que se señala como norma de cobertura —esto es, la que permite a las partes someterse a un Tribunal extranjero: artículo 1255 del Código Civil— es la que debe regular el supuesto fáctico definitivamente, atribuyéndole una protección suficiente o no claudicante”). Esta línea jurisprudencial es también seguida en criterio de las Audiencias Provinciales, siendo ejemplo de ello: Sentencia de la Audiencia Provincial de Madrid de 10 de julio de 2000, rec. 1407/1998; Sentencia de la Audiencia Provincial de Valencia de 17 de julio de 2001, rec. 278/2001 o Auto de la Audiencia Provincial de Santa Cruz de Tenerife de 29 de octubre de 2004)

No existiendo, así, obstáculo alguno para apreciar que, por efecto de la derogatio fori que implica la validez y eficacia del acuerdo de sumisión expresa acreditado en los presentes Autos, procede la declaración de inhibición de jurisdicción de este Tribunal, por estimar la excepción de declinatoria, que en Derecho ejerce la representación legal de la demandada.

En su virtud, por todo lo expuesto,

SUPLICO AL TRIBUNAL: Que tenga por presentado este escrito dentro del legal plazo, y, en su virtud, tenga por interpuesta la excepción de declinatoria de jurisdicción, acordando su admisión y dando el legal trámite a la misma, resuelva finalmente sobre la ausencia de jurisdicción denunciada por la representación del demandado, acogiendo sus pretensiones, dictando en su día Auto por el cual este Tribunal se inhiba de conocer y seguir los autos del procedimiento principal contra mi representado, siendo condenada con ello en costas a la parte actora.

OTROSÍ DIGO: que de conformidad con el artículo 64.1 LEC, se acuerde de forma inmediata, la automática la suspensión de los Autos de procedimiento principal, así como del cómputo de los plazos en el curso del mismo.

SUPLICO II, acuerde conforme se interesa, la suspensión de los Autos de procedimiento principal.

Es Justicia que pido en [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma y número del/de la Letrado/a [Nº DE COLEGIADO] Firma del/de la Procurador/a

========================================================================
