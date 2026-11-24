---
name: demanda-recuperacion-finca-rustica-adquirida-civ-0608
description: "Demanda de recuperación de finca rústica adquirida por el arrendatario histórico (LAR 1980). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de recuperación de finca rústica adquirida por el arrendatario histórico (LAR 1980)

> Formulario **CIV-0608** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Modelo de demanda de juicio ordinario en ejercicio de la acción civil de recuperación de la propiedad rústica adquirida forzosamente al causante de la herencia yacente actora por arrendamiento histórico, solicitando se declare su derecho a resolver la transmisión operada de la propiedad con carácter forzoso de la finca litigiosa y se condene a la demandada a que otorgue a los herederos del causante la correspondiente escritura pública de transmisión de la propiedad de la misma.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de recuperación de finca rústica adquirida por el arrendatario histórico (LAR 1980)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de recuperación de finca rústica adquirida por el arrendatario histórico (LAR 1980)” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:demanda-recuperacion-finca-rustica-adquirida-civ-0608`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (37 veces)
- [ ] LOCALIDAD (12 veces)
- [ ] Nº DE DOCUMENTO (12 veces)
- [ ] FECHA (9 veces)
- [ ] IMPORTE (8 veces)
- [ ] NÚMERO (5 veces)
- [ ] DENOMINACIÓN SOCIAL (4 veces)
- [ ] NOMBRE DEL CASERÍO (4 veces)
- [ ] NOMBRE DEL CASERÍO (SEGUNDO NOMBRE) (4 veces)
- [ ] Nº DE PARCELA (4 veces)
- [ ] CALLE (3 veces)
- [ ] IMPORTE EN PESETAS (2 veces)
- [ ] Nº (2 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] BARRIO O LOCALIDAD
- [ ] DIRECCIÓN
- [ ] FECHAS
- [ ] FINCA
- [ ] FOLIO
- [ ] LIBRO
- [ ] LUGAR
- [ ] MUNICIPIO
- [ ] Nº DE POLÍGONO
- [ ] PROVINCIA
- [ ] SECCIÓN
- [ ] SEDE
- [ ] TOMO

## Normas que cita el formulario

- art. 156 LEC
- art. 164 LEC
- art. 85 LOPJ
- art. 45 LEC
- art. 52.1.7 LEC
- art. 6.1.4 LEC
- art. 7.5 LEC
- art. 6.1.1 LEC
- art. 7.1 LEC
- art. 10.1 LEC
- art. 23.1 LEC
- art. 31.1 LEC
- art. 399.3 LEC
- art. 5 Ley Orgánica 1/2025
- art. 249.1.6 LEC
- art. 399 LEC
- art. 251.2 LEC
- art. 252.2 LEC
- art. 394.1 LEC
- art. 219 LEC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE Q.P.T.R.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…a en sentencia de [FECHA] del Tribunal de Instancia, plaza n.º [NÚMERO], de esta»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) La Ley 83/1980, de 31 de diciembre, ha sido derogada por la vigente Ley 49/2003, de 26 de noviembre, la actual de Arrendamientos Rústicos, aunque debe advertirse que los contratos de arrendamiento y aparcería en vigor se rigen por la normativa aplicable al tiempo de su celebración (L 49/03, arrendamientos rústicos: DT1)

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE Q.P.T.R.C.

D./Dña. [NOMBRE Y APELLIDOS], Procuradora de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS], como acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS], abogado ejerciente, nº [NÚMERO] del Iltre. Colegio de [LOCALIDAD], con despacho abierto en [LOCALIDAD], calle [CALLE], ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que por medio del presente escrito paso a interponer demanda de Juicio Ordinario, en representación y beneficio de la HERENCIA DE D./DÑA. [NOMBRE Y APELLIDOS], contra D./Dña. [NOMBRE Y APELLIDOS], para ser emplazada en el domicilio sito en calle [CALLE], de [LOCALIDAD], con solicitud expresa de que, resultando negativo la comunicación, se proceda por el Letrado de la Administración de Justicia a utilizar los medios oportunos de averiguación conforme art. 156 LEC, manifestando desconocer otro, aparte de designado, y no tener la demandada la profesión u oficio que le vincule a una manifestación domiciliaria, o lugar de trabajo, procediéndose en el extremo al emplazamiento edictal en términos del art. 164 LEC, ejercitando contra los herederos inidentificados acción civil de recuperación de la propiedad rústica adquirida forzosamente a mi causante por arrendamiento histórico, y todo ello de acuerdo con los siguientes hechos y consideraciones de derecho,

HECHOS

PRIMERO.- D./Dña. [NOMBRE Y APELLIDOS] es titular poseedora del caserío [NOMBRE DEL CASERÍO] YY [NOMBRE DEL CASERÍO (SEGUNDO NOMBRE)] de [BARRIO O LOCALIDAD], municipio de [MUNICIPIO], y sus pertenecidos, que conforma la finca registral [FINCA], inscrita al folio [FOLIO], tomo [TOMO], del libro [LIBRO] del Registro de la Propiedad de [LOCALIDAD], y se corresponde con las parcelas [Nº DE PARCELA], [Nº DE PARCELA] y [Nº DE PARCELA], y [Nº DE PARCELA] del Polígono [Nº DE POLÍGONO] del Catastro de rústica del Ayuntamiento de

Se acompañan para la identidad de la casa y predios, certificados del Registro de la Propiedad, y de la Oficina Catastral de [LOCALIDAD], como documentos nos. y [Nº DE DOCUMENTO].

SEGUNDO.- D./Dña. [NOMBRE Y APELLIDOS] era arrendataria, sujeta a legislación locativa especial rústica, que pagaba una renta de [IMPORTE] euros, equivalente de [IMPORTE EN PESETAS] pesetas, mensualmente, por la cesión temporal de la finca indicada para su aprovechamiento agrícola y pecuario.

Se acompaña testimonio de los expedientes de consignación de rentas ante el Juez de Paz de [LOCALIDAD], de nos. /, [Nº] / y [Nº] / (documentos nos [Nº DE DOCUMENTO] a [Nº DE DOCUMENTO]), y nota del Registro Especial de Arrendamientos Rústicos de la Comunidad Autónoma de [LOCALIDAD] (documento nº [Nº DE DOCUMENTO]).

TERCERO.- La propiedad de la finca correspondía a D./Dña. [NOMBRE Y APELLIDOS], conforme aparece en la certificación registral aportada, el cual murió el [FECHA], no habiendo otorgado testamento, siendo viudo, sin ascendientes, y dejando cuatro hermanos, mi representado, y D./Dña. [NOMBRE Y APELLIDOS], D./Dña. [NOMBRE Y APELLIDOS], D./Dña. [NOMBRE Y APELLIDOS], y D./Dña. [NOMBRE Y APELLIDOS], a cuya demostración se acompaña testimonio del auto de declaración de herederos dictado por el Tribunal de Instancia de [SEDE], plaza n.º [NÚMERO] (documento nº [Nº DE DOCUMENTO]).

CUARTO.- La demandada, como continuadora en el arriendo de su padre y de su abuelo, alegando que residía en el caserío [NOMBRE DEL CASERÍO] YY [NOMBRE DEL CASERÍO (SEGUNDO NOMBRE)] con su hijo D./Dña. [NOMBRE Y APELLIDOS], así como que destinaba los predios citados al aprovechamiento de ganadería, vacuna y lanar, de pasto a diente, así como a la cría de gallinas y conejos, y al cultivo de hortalizas en el huerto familiar para autoconsumo, formuló el [FECHA] demanda en reclamación de acceso a la propiedad de la finca identificada, que le fue estimada en sentencia de [FECHA] del Tribunal de Instancia, plaza n.º [NÚMERO], de esta ciudad, autos de Juicio de Menor Cuantía nº [Nº DE PROCEDIMIENTO] /, confirmada por la de apelación dictada por la Sección [SECCIÓN] de la Audiencia provincial de fecha [FECHA] (Rollo civil nº [Nº DE PROCEDIMIENTO] /).

Se adjuntan testimonios de la demanda, sentencia de instancia, y de apelación, como documentos nos. a [Nº DE DOCUMENTO].

QUINTO.- Con independencia de que la demandada no residía en el caserío, ni explotaba las fincas, cuando pretendió con éxito la propiedad del causante de mi poderdante, D./Dña. [NOMBRE Y APELLIDOS], lo cual no tiene sentido aquí ya plantear, el caso es que después de declarada a favor de D./Dña. [NOMBRE Y APELLIDOS] la propiedad, y fijado el precio en ejecución de sentencia, conforme a resolución de la Junta Arbitral provincial de [PROVINCIA], que ascendía a [IMPORTE EN PESETAS] pesetas —ya cuando D./Dña. [NOMBRE Y APELLIDOS] había fallecido—, no ha cumplido con el deber de cultivar personalmente los pertenecidos del caserío, en que no reside.

Se acompaña testimonio de la ejecución forzosa en los precitados autos de Menor Cuantía, en que se consignó por D./Dña. [NOMBRE Y APELLIDOS] la cantidad señalada, y la cual no ha sido posible que se entregue por la Secretaría a ninguno de los coherederos (documento nº [Nº DE DOCUMENTO]).

SEXTO.- D./Dña. [NOMBRE Y APELLIDOS] vive con su hijo D./Dña. [NOMBRE Y APELLIDOS], soltero, por lo menos hasta estos momentos y desde [FECHA], en [DIRECCIÓN], sin hacerlo en el caserío [NOMBRE DEL CASERÍO] YY [NOMBRE DEL CASERÍO (SEGUNDO NOMBRE)], y es pensionista, mientras que su hijo presta servicios como asalariado en la empresa Fundiciones [DENOMINACIÓN SOCIAL] OO [DENOMINACIÓN SOCIAL], ignorándose cuál pueda ser el ganado que resta en el caserío, o las labores de labranza, que desde luego, no son aparentes, según se demostrará cumplidamente, y a pesar de que pueda perseverar la demandada en el censo de ganaderos de la Diputación provincial de [LOCALIDAD] (que documentó en el Menor Cuantía).

SÉPTIMO.- Mi mandante, simultáneamente a instar la declaración de herederos de su difunto hermano D./Dña. [NOMBRE Y APELLIDOS], dirigió en beneficio de la comunidad hereditaria a D./Dña. [NOMBRE Y APELLIDOS], requerimiento notarial en exigencia de la recuperación del caserío [NOMBRE DEL CASERÍO] YY [NOMBRE DEL CASERÍO (SEGUNDO NOMBRE)] y sus pertenecidos, por incumplimiento del precitado deber dentro de los seis años posteriores al acceso forzado a la propiedad, el cual se practicó en el domicilio de la calle [CALLE] en [LOCALIDAD], donde lo recibió su hijo D./Dña. [NOMBRE Y APELLIDOS], sin que nada contestara.

Se adjunta acta del Notario de [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS], de fecha [FECHA], con nº [NÚMERO] del protocolo general corriente, como documento nº [Nº DE DOCUMENTO], la cual hace fe, tanto de la precisión para esta parte de deducir demanda, como la constancia de que la demandada reside en el domicilio en que se pide sea emplazada, con protesta de no haberle otro, y si en éste no se le pudiera emplazar, activarse averiguaciones o citación edictal.

OCTAVO.- La parte actora manifiesta que, previo a la presentación de la presente demanda, se han llevaron a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad, y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria; incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, mi representado envío un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por el demandado por el mismo medio, rechazando el acuerdo/ habiendo sido solo posible un acuerdo parcial, viéndonos en la necesidad de acudir a la presente vía judicial, respecto a los extremos de la controversia en los que se mantiene la discrepancia.

Acompaño como documento nº [Nº DE DOCUMENTO], el requerimiento efectuado y como documento nº [Nº DE DOCUMENTO], la contestación del demandado.

A los hechos resultan de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

JURÍDICO PROCESALES

I.- COMPETENCIA.

Sin duda de la competencia genérica del orden civil de la jurisdicción, la competencia específica se atribuye el conocimiento de este asunto al Tribunal a quien tengo el honor de dirigirme por ser la Sección Civil del Tribunal de Instancia (art. 85 LOPJ y art. 45 LEC), que detenta competencia objetiva, y la funcional de la instancia, y que ostenta competencia territorial, por cuanto en los juicios sobre arrendamiento de inmuebles es competente el tribunal del lugar en que esté sita la finca, según el art. 52.1.7º LEC.

II.- PARTES

CAPACIDAD. No es nueva la consideración como parte de las masas patrimoniales o los patrimonios separados que carezcan transitoriamente de titular o cuyo titular haya sido privado de sus facultades de disposición y administración (art. 6.1.4º LEC), con lo que se alude —además de a la masa del concurso— al anciano ejemplo de masa de bienes que actúan en juicios, como la herencia yacente [SSTS de 20 de setiembre de 1982, 12 de marzo de 1987, o 21 de mayo de 1991 ], la cual estará representada por su administrador, albacea, o a falta de tales, el heredero, conforme al art. 7.5 LEC, condición que acredita el actor, mi patrocinado, D./Dña. [NOMBRE Y APELLIDOS]

La demandada es persona física, a la que el reconocimiento por el Derecho de personalidad implica su capacidad para ser parte (art. 6.1.1º LEC), y su mayor edad, sin discapacidad que se conozca, la capacidad procesal, o de obrar en juicio, compareciendo en su propio nombre y derecho (art. 7.1 LEC).

LEGITIMACIÓN. Conforme al art. 2.4 Ley 1/92 de 10 de febrero, de Arrendamientos Rústicos Históricos (en adelante LARH), cuenta el arrendador frente al que se ha ejercido el derecho a adquirir la propiedad de la finca cultivada en base arrendamiento anterior al 1 de agosto de 1942, con el derecho a recobrar la propiedad del arrendatario, lo que legitima activamente al demandante, en representación de la herencia del arrendador, con la legitimación activa ordinaria derivada ‘mortis causa’ (art. 10.1 LEC), y ostenta la demandada la legitimación pasiva correlativa de la misma naturaleza, directa, por pertenecer a la misma la propiedad de la finca, como adquirida forzosamente de D./Dña. [NOMBRE Y APELLIDOS]

POSTULACIÓN. Esta parte, como será debido para la personación que convenga a la contraria, comparece por medio de Procurador de los Tribunales habilitado ante el tribunal (art. 23.1 LEC), y bajo la dirección del Letrado en ejercicio (art. 31.1 LEC).

IIII.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por el art. 264.4º y art. 399.3 de la LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

PROCEDIMIENTO

TRÁMITE. El procedimiento a través del cual se ha de sustanciar la pretensión es el correspondiente al JUICIO ORDINARIO, conforme arts. 248 y 249.2 LEC, que indica aplicable el criterio prioritario de la materia, estando las pretensiones que versen sobre cualesquiera asuntos relativos a arrendamientos rústicos de bienes inmuebles, salvo desahucio o mera reclamación de cantidad, entre las listadas en art. 249.1.6º LEC, por lo que se seguirán los trámites de los arts. 399 a 436 LEC, teniendo en cuenta que la Disposiciones derogatoria única.2.7.º LEC ha derogado los arts. 123 a 137 LAR 1980.

CUANTÍA. Se señala como cuantía de la demanda la de [IMPORTE] euros (€), que se corresponde con la suma de dos factores: a) el precio de la finca descrita en el ordinal primero del cuerpo de la demanda, fijada legalmente para la consumación del derecho a adquirir la propiedad de tal finca, a pesar de que el fundamento del mismo sea el arrendamiento de bienes —que tiene otra regla de cuantificación— conforme art. 251.3ª.4º LECen relación con art. 251.2ª LEC, toda vez que tal precio que se pide fijar no es inferior al valor catastral; b) la cantidad de [IMPORTE] euros ( [IMPORTE] €), que se solicita como daños y perjuicios irrogados, que al provenir del mismo título, y ser líquida, se suma conforme art. 252.2ª LEC.

IV.- COSTAS

Serán de cuenta de la demandada, como previene el art. 394.1 LEC, consagrando el principio de vencimiento cuasiobjetivo para declarativos en primera instancia.

JURÍDICO SUSTANTIVOS

Previamente, debe destacarse que el inquilino rústico tiene derecho de acceso a la propiedad cuando la explotación de las fincas arrendadas se ejerce mediante un cultivo agrícola o ganadero siquiera de mínima entidad, según la misma dicción del art. 16 Ley 83/80 de 31 de diciembre, de Arrendamientos Rústicos, para caracterizar al cultivador personal, y nunca se podrá demostrar que D./Dña. [NOMBRE Y APELLIDOS] disponga de un conjunto de elementos destinados a una explotación ganadera, ni que haya llegado a obtenerse algún beneficio o rendimiento económico derivado.

Para el ejercicio de la facultad expropiatoria que llevó a cabo D./Dña. [NOMBRE Y APELLIDOS] era imprescindible que ostentase la condición de cultivador personal, no siendo suficiente la de profesional de la agricultura, cuando ni siquiera es esto último.

Pero la cosa juzgada material negativa impide volver sobre tal cosa, y sin embargo, el art. 2.4 LARH, al que ya se ha hecho mención, obliga a la arrendataria que ha accedido a la propiedad de la finca rústica conforme al dicho precepto, que derogó el régimen de arts. 98 y 99 LAR 1980, y estuvo viabilizado hasta 31 de diciembre de 1997, a cultivar personalmente las fincas adquiridas durante seis años como mínimo.

El caso es que la actora es pensionista, que puede estar censada como ganadera en la Diputación provincial de [LOCALIDAD], pero reside con su hijo D./Dña. [NOMBRE Y APELLIDOS] en [LOCALIDAD], y éste tiene condición de trabajador por cuenta ajena, que obtiene la totalidad de sus ingresos por trabajo personal en la empresa Fundiciones [DENOMINACIÓN SOCIAL] OO [DENOMINACIÓN SOCIAL], —según se demostrará en periodo probatorio, si hubiera resistencia y se negare de contrario—. Y por lo que esta parte ha podido comprobar, a lo sumo, D./Dña. [NOMBRE Y APELLIDOS], o más bien su hijo, dedica los ratos libres o perdidos, así como los días festivos al cuidado de un huerto, o la cría de algunos animales en un caserío abandonado. En estas fechas invernales, ni está cultivado el huerto, ni se sabe de animales, quedando el monte inculto, al crecimiento de arbustos nacedizos salvajes.

La actora en absoluto es profesional de la ganadería, ni del pastizal, ni de la horticultura, ya que de ninguna manera se ha dedicado preferentemente a dichas actividades en estos años desde 1999, cuando consiguió la propiedad, ni se atisba que vaya a dedicarse en un futuro a las mismas, por su predicha edad, ni su hijo, que es asalariado y tiene vivienda en otra población alejada del campo.

Pero es que el art. 2.4 LARH exige, no la condición de profesional de la agricultura, sino la condición de cultivador personal y no ninguna otra, la única que puede legitimar a la demandada para mantenerse en la propiedad, y oponerse con éxito al ejercicio de la pretensión que deduce esta demanda.

La doctrina de la Sala I TS exige como nota esencial al concepto de cultivador personal del art. 16 LAR 1980 la dedicación exclusiva del mismo a su actividad como arrendatario rústico, no admitiendo a tal efecto la simple dedicación preferente que para ser profesional de la agricultura considera suficiente el art. 15 de dicha norma [SSTS de 28 de abril de 1989 ) y 3 de Julio de 1992 ].

Es cierto que LARH, atiende al problema de los jubilados y que el R. Decreto 1147/1992, de 25 de septiembre, estableció una línea especial de ayudas para facilitar el acceso a la propiedad a dichos arrendatarios, pero ha de tenerse en cuenta que el art. 3 LARH exige que los mayores de 55 años que pretendan disfrutar de la prórroga complementaria que el precepto les concede han de ser cultivadores personales y continuar ostentando esta condición hasta cumplir los 65 años de edad.

A su vez, si bien la Ley 19/95 de 4 de julio, de Modernización de las Explotaciones Agrarias, modificó el art. 15 LAR 1980, relativo al profesional de la agricultura, dejó intacto el contenido del art. 16, que se refiere al cultivador personal, que es a quien, corresponde en exclusiva el ejercicio del derecho de acceso a la propiedad.

En definitiva, esta condición y la dedicación personal al cultivo de las fincas y a la obtención de todos los aprovechamientos de que las mismas son susceptibles, son los factores que según el legislador influyen de manera importante en el valor actual alcanzado por los predios, lo que le ha impulsado a reconocer a determinados arrendatarios rústicos el derecho a convertirse en propietarios, participando así en la riqueza que han contribuido a crear.

No puede olvidarse que la legislación arrendaticia rústica ha sido de carácter eminentemente social, con miras a lograr la protección del cultivador en cuanto a temas para el mismo trascendentales, como son la justeza de la renta y la estabilidad en su situación a los que se añade la posibilidad de acceso a la propiedad de los predios a cuyo cultivo él mismo y sus causantes han dedicado durante largos años su personal esfuerzo. Este derecho de acceso a la propiedad que en la Ley de 15 de Julio de 1954 se hallaba fuertemente condicionado por cuanto se concedía al arrendador la posibilidad de enervarlo mediante el abono de una determinada cantidad, se amplió en la Ley 83/1980, de 31 de diciembre, en que se suprimió dicha facultad del propietario, sin duda teniendo en cuenta el principio de que al valor actual de las fincas arrendadas habían contribuido la forma notable el arrendatario y sus ascendientes, mediante su cultivo a lo largo de varias generaciones. Si el arrendatario adquirente no se dedica al cultivo defrauda este sistema.

Justiprecio e indemnización.

En relación con el precio que debe pagarse como contraprestación al derecho de recuperación, conforme al art. 2.4 LARH, es el precio de la adquisición forzosa, que el art. 2.2 LARH confió a la fijación por las Juntas Arbitrales de Arrendamiento Rústicos (sustituyendo el criterio del art. 98.1 LAR 1980, que reenviaba a los criterios de la Ley de Expropiación Forzosa, que era la de 16 de diciembre de 1954, lo que suponía acudir al justiprecio del art. 39 LEF 1954, con reajuste al valor real de su art. 43).

Puesto que está predeterminado en resolución firme de la vía ejecutiva del Menor Cuantía, en la cual se hizo consignación para pago de D./Dña. [NOMBRE Y APELLIDOS], corresponderá, al estimarse el derecho de esta parte, que se pida al Tribunal de Instancia nº [NÚMERO], el mandamiento de devolución a la misma.

Como el art. 2.4 LARH prevé la indemnidad del arrendador al que se ha ‘expropiado’ sin razón de justicia, como se demuestra con ulterioridad, cumplimentando la orden de no dejar la sentencia a reserva de liquidación ejecutiva del art. 219 LEC, se calcula en [IMPORTE] euros ( [IMPORTE] €) la suma del concepto de renta que se hubiera devengado desde [FECHA], fecha de adquisición forzosa hasta el presente año agrícola, incluida casa de labor, según lo usual en el lugar para fincas análogas, ascendente a [IMPORTE] euros ( [IMPORTE] €), y el concepto de daño moral, por la preocupación y riesgo de irreivindicabilidad que gravitaba sobre los herederos de D./Dña. [NOMBRE Y APELLIDOS]

Respecto del valor en renta de la finca, se aporta dictamen pericial del Agente de la Propiedad Inmobiliaria D./Dña. [NOMBRE Y APELLIDOS], como documento nº [Nº DE DOCUMENTO] de la demanda.

Con relación al daño moral resarcible, se manifiesta:

Por lo expuesto,

AL TRIBUNAL SUPLICO

que tenga por presentado este escrito, lo admita, y por deducida DEMANDA de JUICIO ORDINARIO en la representación que ostento de la HERENCIA YACENTE DE D./Dña. [NOMBRE Y APELLIDOS], entendiéndose conmigo las sucesivas diligencias, frente a D./Dña. [NOMBRE Y APELLIDOS], le confiera traslado de la demanda para que la conteste, si fuera de su interés, reciba el pleito a prueba, y dicte en su día Sentencia por la que, estimando la presente demanda:

1.- Se declare el derecho de la HERENCIA YACENTE DE D./DÑA. [NOMBRE Y APELLIDOS] a resolver la transmisión operada de la propiedad con carácter forzoso el caserío ‘YY‘ descrito en el ordinal primero de los hechos, mediante el pago en metálico y al contado de la suma que se fijó como precio de la misma deeuros (€).
2.- Se condene a D./Dña. [NOMBRE Y APELLIDOS] a que otorgue con los herederos de D./Dña. [NOMBRE Y APELLIDOS] la correspondiente escritura pública de transmisión de la propiedad del caserío con el precio fijado, libre de arrendamientos y ocupantes.
3.- Se fije la suma deeuros (€) como daños y perjuicios efectivamente causados por la privación de propiedad.
4.- Se condene a la parte demandada al reintegro de todas las costas procesales.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a
