---
name: demanda-revision-renta-finca-rustica-arrendamiento-civ-0603
description: "Demanda de revisión de renta de finca rústica (arrendamiento sujeto a la LAR 1980). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de revisión de renta de finca rústica (arrendamiento sujeto a la LAR 1980)

> Formulario **CIV-0603** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario por la que el arrendador de una finca rústica, transcurrido el primer año de vigencia del contrato, pide la revisión judicial de la renta por ser inferior a la usual en el lugar para fincas análogas (contrato sometido a la Ley 83/1980, de Arrendamientos Rústicos, aplicable por razón de la fecha de su celebración).

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de revisión de renta de finca rústica (arrendamiento sujeto a la LAR 1980)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de revisión de renta de finca rústica (arrendamiento sujeto a la LAR 1980)” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:demanda-revision-renta-finca-rustica-arrendamiento-civ-0603`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (12 veces)
- [ ] LOCALIDAD (8 veces)
- [ ] IMPORTE (4 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] DOMICILIO (3 veces)
- [ ] FECHA (3 veces)
- [ ] DENOMINACIÓN DE LA FINCA (2 veces)
- [ ] FIRMA (2 veces)
- [ ] NOMBRE DEL NOTARIO (2 veces)
- [ ] Nº DE PROTOCOLO (2 veces)
- [ ] SUPERFICIE (2 veces)
- [ ] AÑO
- [ ] CULTIVO
- [ ] CÁMARA AGRARIA LOCAL U ORGANISMO COMPETENTE
- [ ] DATOS REGISTRALES
- [ ] DNI/NIE
- [ ] DURACIÓN
- [ ] DÍA
- [ ] FECHAS
- [ ] IMPORTE EN LETRA
- [ ] LINDERO ESTE
- [ ] LINDERO NORTE
- [ ] LINDERO OESTE
- [ ] LINDERO SUR
- [ ] MES
- [ ] NOMBRE Y APELLIDOS DEL CAUSANTE
- [ ] NOMBRE Y APELLIDOS DEL DEMANDANTE
- [ ] Nº DE COLEGIADO
- [ ] PARTIDA
- [ ] SE EXPRESARÁN LAS CAUSAS
- [ ] SEDE

## Normas que cita el formulario

- art. 85 LOPJ
- art. 45 LEC
- art. 52.1.7.º LEC
- art. 249.1.6.º LEC
- art. 6.1.1.º LEC
- art. 7.1 LEC
- art. 253.1 LEC
- art. 251 LEC
- art. 23 LEC
- art. 399 LEC
- art. 399.3 LEC
- art. 5 Ley Orgánica 1/2025
- art. 40 Ley 83/1980
- art. 42 Ley 83/1980
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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en nombre y representación de [NOMBRE Y APELLIDOS DEL DEMANDANTE], con domicilio en [DOMICILIO], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento n.º [Nº], con asistencia del Letrado/a suscribiente D./Dña. [NOMBRE Y APELLIDOS], abogado/a ejerciente n.º [Nº DE COLEGIADO] del Ilustre Colegio de Abogados de [LOCALIDAD], que tiene abierto despacho en [LOCALIDAD], calle [DOMICILIO], ante el Tribunal comparezco y, como mejor proceda en Derecho, DIGO:

Que por medio del presente escrito deduzco demanda de juicio ordinario, ejercitando acción de revisión de renta de finca rústica, contra D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con D.N.I. n.º [DNI/NIE], y con domicilio en [LOCALIDAD], calle [DOMICILIO], basándola en los siguientes hechos y fundamentos de derecho:

HECHOS

PRIMERO.- Mi mandante es legítimo propietario del inmueble que luego se mencionará en su condición de heredero de su padre D./Dña. [NOMBRE Y APELLIDOS DEL CAUSANTE], en virtud de testamento abierto otorgado ante el Notario de [LOCALIDAD] D./Dña. [NOMBRE DEL NOTARIO] con el n.º [Nº DE PROTOCOLO] de su protocolo, según se acredita mediante copia del expresado testamento, que se acompaña como documento n.º [Nº] a la presente demanda, y copia auténtica de la escritura de aceptación y adjudicación de herencia autorizada por el mismo notario D./Dña. [NOMBRE DEL NOTARIO], obrante en su protocolo con el n.º [Nº DE PROTOCOLO]. En el referido documento se constata el carácter de sucesor a título universal y único de mi mandante respecto de la finca "[DENOMINACIÓN DE LA FINCA]", cuya descripción consta en la misma. La finca de referencia forma parte del caudal relicto del causante y testador dicho, y su descripción es la que sigue: finca de regadío plantada de [CULTIVO], situada en la partida de [PARTIDA] del término municipal de [LOCALIDAD], con una extensión superficial de [SUPERFICIE] hectáreas, lindante al Este con [LINDERO ESTE], al Sur con [LINDERO SUR], al Oeste con [LINDERO OESTE] y al Norte con [LINDERO NORTE]. Se halla inscrita en el Registro de la Propiedad de [LOCALIDAD], Libro [Nº], Tomo [Nº], Folio [Nº], inscripción [Nº], con el n.º [Nº] de finca registral [DATOS REGISTRALES]. Dicha finca carece de gravámenes de todo género, según consta de la certificación expedida por el/la Registrador/a de la Propiedad, que se acompaña como documento n.º [Nº], en la que se acredita la titularidad dominical de mi mandante.

SEGUNDO.- Entre el demandante D./Dña. [NOMBRE Y APELLIDOS] y el demandado, el primero en concepto de arrendador y el segundo en concepto de arrendatario, se concertó con fecha [FECHA] un contrato de arrendamiento para aprovechamiento agrícola en virtud del cual el demandante cedía al demandado la posesión útil de la finca descrita, sita en este término municipal y conocida como "[DENOMINACIÓN DE LA FINCA]", con una extensión superficial de [SUPERFICIE] hectáreas, por un plazo de duración de [DURACIÓN] y por una renta anual de [IMPORTE] euros, habiendo transcurrido un año de vigencia del contrato el día [FECHA].

Se acompaña como documento n.º [Nº] el original del contrato de arrendamiento.

TERCERO.- La simple observancia de las cláusulas de dicho contrato permite apreciar que la actual renta es inferior a la usual en la zona para fincas análogas y no está conforme con los precios que rigen el mercado para los productos que las fincas producen, ya que [SE EXPRESARÁN LAS CAUSAS]; por ello se pide la revisión de la renta contractual inicialmente fijada, al cumplirse una anualidad de vigencia del contrato.

CUARTO.- La parte actora manifiesta que, previo a la presentación de la presente demanda, se han llevado a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria, incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, mi representado envió un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por el demandado por el mismo medio, [ELEGIR: rechazando el acuerdo / habiendo sido solo posible un acuerdo parcial], viéndonos en la necesidad de acudir a la presente vía judicial, respecto a los extremos de la controversia en los que se mantiene la discrepancia.

Acompaño como documento n.º [Nº] el requerimiento efectuado y como documento n.º [Nº] la contestación del demandado.

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA.

Sin duda de la competencia genérica del orden civil de la jurisdicción, la competencia específica atribuye el conocimiento de este asunto al Tribunal a quien tengo el honor de dirigirme, por ser el de Instancia (art. 85 LOPJ y art. 45 LEC), que detenta competencia objetiva y la funcional de la instancia, y que ostenta competencia territorial, por cuanto en los juicios sobre arrendamiento de inmuebles es competente el tribunal del lugar en que esté sita la finca, según el art. 52.1.7.º LEC.

II.- PROCEDIMIENTO.

La demanda deberá sustanciarse por las normas del juicio ordinario del Título II del Libro II LEC, a tenor de lo expresamente prevenido en el art. 249.1.6.º LEC, al tener por objeto pretensiones relativas a contrato de arrendamiento de finca rústica, sin que opere la exclusión material de la acción de desahucio o de mera reclamación de cantidad.

III.- CAPACIDAD.

Demandante y demandado, personas físicas, tienen capacidad para ser parte (art. 6.1.1.º LEC), titular de facultades y cargas del proceso, y asimismo plena capacidad procesal, al ser mayores de edad, sin limitación de ejercicio válido de derechos civiles, o para comparecer en juicio, en términos del art. 7.1 LEC, pretendiendo el actor y siendo pretendido el demandado, en sus respectivos nombres y derechos.

IV.- LEGITIMACIÓN.

La legitimación activa corresponde al demandante por ser el propietario de la finca, y la pasiva la tiene el demandado en cuanto obligado a lo que se pide como arrendatario de la finca, por haber concertado el contrato.

V.- CUANTÍA.

Conforme al art. 253.1 LEC cifro la cuantía de la presente demanda en [IMPORTE EN LETRA] euros ([IMPORTE] €), importe de una anualidad de renta, según resulta de la regla 9.ª del art. 251 LEC.

VI.- POSTULACIÓN Y DEFENSA.

Conforme a los arts. 23 y 31 LEC se formula esta demanda por medio de Procurador con poder para pleitos, y con dirección y firma de Letrado habilitado. Asimismo se cumplen los requisitos formales del art. 399 LEC.

VII.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por el art. 264.4.º y el art. 399.3 de la LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VIII.- FONDO DEL ASUNTO.

Se ejercita acción de revisión de la renta, por transcurso del primer año de vigencia, solicitando al órgano jurisdiccional que se determine la renta justa sometida a revisión por ser la actual inferior a la usual en la zona, revisión que encuentra apoyo legal en el art. 40 de la Ley 83/1980, de 31 de diciembre, de Arrendamientos Rústicos, derogada por la vigente Ley 49/2003, pero que resulta aplicable al contrato vigente, puesto que era la del momento de su celebración (disposición transitoria primera de la Ley 49/2003, de 26 de noviembre, de Arrendamientos Rústicos).

Aunque la inicial fijación de la renta contractual se funda en la libre determinación de las partes, procede su revisión en favor de cualquiera de las partes, transcurrido el plazo de un año, si fuera superior o inferior a la usual en el lugar para fincas análogas.

El precepto citado, al establecer el derecho de revisión de la renta, no lo hace a favor de una u otra parte, sino que lo otorga a los dos, de suerte que ese juicio de revisión tanto sirve para aumentar como para reducir la renta pactada, puesto que el fundamento de este artículo, el móvil que lo inspira, no es otro que hallar y declarar la renta justa que en cada caso particular deba regir. El Tribunal Supremo tiene declarado que, al conceder la Ley a los que contratan arrendamientos rústicos la facultad de fijar libremente la renta, les otorga también el derecho a solicitar, luego de que transcurra un año desde la entrada en vigor del arrendamiento, que se revise la renta pactada y se fije la que en lo sucesivo haya de ser satisfecha, estableciendo a favor de los mismos un derecho eminentemente social, encaminado a lograr la equidad en las rentas de dichos contratos en beneficio público, de carácter necesario y, por tanto, como todos los de su clase, irrenunciable, a menos que lo sea después de incorporado al patrimonio del renunciante.

El artículo 40 de la Ley 83/1980 permite que, transcurrido el primer año de vigencia del contrato, el arrendador en este caso pueda pedir la elevación de la renta por ser ésta inferior a lo usual del lugar para fincas análogas. El Tribunal Supremo, interpretando dicho precepto (sentencias de 23 de octubre de 1991 y de 25 de mayo de 1992), declara que la revisión de la renta debe tender a que ésta sea justa como equitativa contrapartida de la posesión y disfrute de la finca, teniendo en cuenta los usos y costumbres del lugar, y que los únicos criterios a que ha de atenderse por el Tribunal son de índole estrictamente objetiva y económica: a la renta usual en el lugar para fincas análogas.

Son, pues, los requisitos legales para el ejercicio de esta acción, que concurren en el caso: a) la existencia de un contrato de arrendamiento rústico; b) el transcurso del primer año de vigencia del mismo; c) que la renta sea superior o inferior a la usual en el lugar para fincas análogas; y d) que únicamente tendrá efecto respecto de los vencimientos posteriores a la demanda (artículo 42 de la Ley 83/1980).

La jurisprudencia recoge los perfiles de esta institución en las citadas sentencias de la Sala Primera del Tribunal Supremo de 23 de octubre de 1991 y de 25 de mayo de 1992, así como se ha tratado por la doctrina de las Audiencias Provinciales, como la de Valladolid, sentencia de 3 de abril de 1989; Soria, sentencia de 1 de junio de 1995; o Ávila, sentencia de 29 de junio de 1997.

Para la determinación de la renta justa de revisión esta parte entiende que deberá fijarse, de acuerdo al criterio de la renta usual en el lugar para fincas análogas, en [IMPORTE] euros por hectárea de regadío, aportándose como documento n.º [Nº] de la demanda certificación de [CÁMARA AGRARIA LOCAL U ORGANISMO COMPETENTE] de [LOCALIDAD], que acredita el precio medio de las fincas de regadío sitas en su término municipal.

IX.- COSTAS.

Conforme al art. 394 LEC, las costas procesales han de imponerse a la parte demandada, con la estimación de la demanda.

En virtud de lo anteriormente expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito con sus copias, se digne admitir uno y otras, formar juicio ordinario especial arrendaticio, en el que se tenga a quien comparece a través de mandatario procesal como parte legítima, entendiéndose con el dicho mandatario todas las actuaciones, y, en mérito a lo alegado, seguido que sea todo el pertinente procedimiento, se venga a dictar en su día definitiva sentencia que declare que la renta justa respecto al contrato de arrendamiento de fincas rústicas que une al actor, como arrendador, y al demandado, como arrendatario, es la renta de [IMPORTE] euros por hectárea de regadío, condenando al demandado a pasar por esta declaración y al pago de esta renta en lo sucesivo, con imposición de las costas.

Por ser de justicia, lo pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a: [FIRMA]	Firma del Procurador/a: [FIRMA]
