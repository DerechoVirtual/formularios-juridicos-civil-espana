---
name: demanda-contra-declaracion-desamparo-razones-fondo-civ-0174
description: "Demanda contra la declaración de desamparo por razones de fondo. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda contra la declaración de desamparo por razones de fondo

> Formulario **CIV-0174** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Al Tribunal Comparecencia, representación y asistencia letrada Interposición de demanda de oposición a la declaración de desamparo HECHOS FUNDAMENTOS DE DERECHO Suplico Otrosí digo Firmas

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda contra la declaración de desamparo por razones de fondo» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda contra la declaración de desamparo por razones de fondo” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-contra-declaracion-desamparo-razones-fondo-civ-0174`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] AÑO (10 veces)
- [ ] MES (10 veces)
- [ ] LOCALIDAD (9 veces)
- [ ] DÍA (8 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] NOMBRE DEL MENOR (4 veces)
- [ ] Nº (3 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] CALLE
- [ ] COLEGIO
- [ ] SEDE
- [ ] ÓRGANO ADMINISTRATIVO

## Normas que cita el formulario

- art. 779 LEC
- art. 780.2 LEC
- art. 780.4 LEC
- art. 85.1 LOPJ
- art. 749.2 LEC
- art. 750.1 LEC
- art. 780.1 LEC
- art. 780 LEC
- art. 753 LEC
- art. 3.2 LO 1/2025
- art. 172.1.I CC
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

### Avisos de actualización (3) — se aplican en el texto, nunca se copian en el documento

- Junto a «…Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).
- Junto a «…2666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.

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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D./Dª [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en nombre y representación de D./Dª [NOMBRE Y APELLIDOS] y D./Dª [NOMBRE Y APELLIDOS], cuya representación acreditará cuando sea requerido para ello mediante comparecencia apud acta (o bien: representación que acredito mediante copia de poder especial para pleitos que presento, la cual solicito me sea devuelta tras su testimonio inicial en autos, por necesitarla para otros usos), bajo la dirección técnica de D./Dª [NOMBRE Y APELLIDOS], Letrado del Ilustre Colegio de [COLEGIO], con despacho profesional en calle [CALLE], ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que por medio del presente escrito, siguiendo instrucciones expresas de mis representados y dentro del plazo de veinte días concedido mediante diligencia de ordenación de fecha [DÍA] de [MES] de [AÑO], interpongo, con base en lo dispuesto en los arts. 779 y 780 LEC, DEMANDA DE OPOSICIÓN A LA RESOLUCIÓN ADMINISTRATIVA dictada en fecha [DÍA] de [MES] de [AÑO] por la Delegación Territorial de [LOCALIDAD] de la Consejería de Bienestar Social (u organismo que corresponda según la Comunidad Autónoma de que se trate) de la Comunidad Autónoma de [LOCALIDAD] por la que se declara en situación de desamparo al/a los menor/es [NOMBRE DEL MENOR], conforme a los siguientes

HECHOS

PRIMERO.- D./Dª [NOMBRE Y APELLIDOS] y D./Dª [NOMBRE Y APELLIDOS] son los padres de [NOMBRE DEL MENOR], nacido en [LOCALIDAD], el día [DÍA] de [MES] de [AÑO] -- y, por tanto, menor/es de edad.

Se acompaña certificación/es de la inscripción/es de nacimiento del/de los menor/es emitida/as por el encargado del Registro Civil de [LOCALIDAD] como Documento/s nº [Nº DE DOCUMENTO] para acreditar este extremo.

SEGUNDO.- La Delegación Territorial de [LOCALIDAD] de la Consejería de Bienestar Social (u organismo que corresponda según la Comunidad Autónoma de que se trate) de la Comunidad Autónoma de [LOCALIDAD], dictó resolución de fecha [DÍA] de [MES] de [AÑO], por la que declaró la situación legal de desamparo del hijo de mis representados, antes citado, y asumió de modo automático su tutela legal, estableciendo un acogimiento familiar (o residencial) para la guarda del menor. La citada resolución fue notificada a mis mandantes en fecha [DÍA] de [MES] de [AÑO].

Se acompaña como Documento nº [Nº DE DOCUMENTO] testimonio de la citada resolución.

TERCERO.- En fecha [DÍA] de [MES] de [AÑO], conforme al art. 780.2 LEC, mis representados presentaron ante este Tribunal un escrito inicial en el que sucintamente expresaban su pretensión de oponerse a la declaración de desamparo de su hijo/s efectuada por la resolución antes citada, con las menciones y manifestaciones establecidas en el mismo precepto.

CUARTO.- Recibido, conforme a lo preceptuado en el art. 780.4 LEC, testimonio completo del expediente administrativo, del que se dio traslado a mis representados, el Letrado de la Administración del Estado les emplazó para que en el plazo de veinte días presentaran la correspondiente demanda, lo que efectúan mediante el presente escrito.

QUINTO.- Mis representados se oponen a la referida declaración de desamparo por no ser ciertos los hechos sobre los que se fundamenta, como acreditarán mediante la prueba oportuna. La resolución que declara el desamparo del menor alega la drogodependencia de mis mandantes y sus antecedentes penales que, en opinión de la Administración competente, les inhabilita para el adecuado cuidado de su hijo. Sin embargo, lo cierto es que desde el mes de [MES] del año [AÑO], después de diversos tratamientos, ambos han dejado las drogas y no ha cometido más delitos, por lo que llevan una vida ordenada y adecuada para atender a su/s hijo/s, el/los menor/es [NOMBRE DEL MENOR] Se insiste, con detalle, en estas circunstancias.

Se acompañan para acreditar estos hechos, como documentos nº [Nº DE DOCUMENTO], informes médicos relativos a cada uno de mis representados, acreditativos de su desintoxicación y certificados de antecedentes penales (y cualesquiera otros documentos que sirvan para acreditar los hechos, por ejemplo, los demostrativos de hallarse trabajando y percibiendo un sueldo los demandantes).

Resultan aplicables a los anteriores hechos, los siguientes

FUNDAMENTOS DE DERECHO

I. COMPETENCIA.- La competencia corresponde a este Tribunal, conforme al art. 779 LEC, en relación con lo dispuesto en el art. 85.1º LOPJ, que la atribuye al Tribunal del domicilio de la entidad protectora del menor.

II. LEGITIMACIÓN.- Ostentan legitimación activa mis representados, como padres del menor/es declarados en desamparo según dispone el art. 780.1.II y legitimación pasiva, la entidad pública que dictó la resolución en que se contiene dicha declaración, siendo preceptiva la intervención del Ministerio Fiscal, de acuerdo con el art. 749.2 LEC, por estar interesados en el procedimiento uno o varios menores de edad.

III. REPRESENTACIÓN Y DEFENSA.- Los demandantes se hallan debidamente representados y asistidos por el Procurador y Letrado señalados al inicio, tal y como exige el art. 750.1 LEC.

IV. PROCEDIMIENTO. La presente oposición se formula sin haber tenido lugar, previamente, reclamación en vía administrativa, por así permitirlo el art. 780.1 de la LEC, dentro de los tres meses de la notificación de la resolución que declaró el desamparo del menor. Deberá tramitarse conforme a lo establecido en el citado precepto.

Dispone el art. 780 LEC: “1. No será necesaria la reclamación previa en vía administrativa para formular oposición, ante los tribunales civiles, a las resoluciones administrativas en materia de protección de menores.

La oposición a la resolución administrativa por la que se declare el desamparo de un menor podrá formularse en el plazo de tres meses desde su notificación, y en el plazo de dos meses la oposición a las restantes resoluciones administrativas que se dicten en materia de protección de menores.

2. Quien pretenda oponerse a una resolución administrativa en materia de protección de menores presentará un escrito inicial en el que sucintamente expresará su pretensión y la resolución a que se opone.

3. El Letrado de la Administración de Justicia reclamará a la entidad administrativa un testimonio completo del expediente, que deberá ser aportado en el plazo de veinte días.

4. Recibido el testimonio del expediente administrativo, el Letrado de la Administración de Justicia emplazará al actor por veinte días para que presente la demanda, que se tramitará con arreglo a lo previsto en el artículo 753.

5. Si el Ministerio Fiscal, las partes o el Juez competente tuvieren conocimiento de la existencia de más de un procedimiento de oposición a resoluciones administrativas relativas a la protección de un mismo menor, pedirán los primeros y dispondrá el segundo, incluso de oficio, la acumulación ante el Tribunal que estuviera conociendo del procedimiento más antiguo.

Acordada la acumulación, se procederá según dispone el artículo 84, con la especialidad de que no se suspenderá la vista que ya estuviera señalada si fuera posible tramitar el resto de procesos acumulados dentro del plazo determinado por el señalamiento. En caso contrario, el Letrado de la Administración de Justicia acordará la suspensión del que tuviera la vista ya fijada, hasta que los otros se hallen en el mismo estado, procediendo a realizar el nuevo señalamiento para todos con carácter preferente y, en todo caso, dentro de los diez días siguientes.

Contra el auto que deniegue la acumulación podrán interponerse los recursos de reposición y apelación sin efectos suspensivos. Contra el auto que acuerde la acumulación no se dará recurso alguno.”

El art. 753 LEC, se remite a los trámites del juicio verbal, con las especialidades que el mismo precepto establece.

Por otra parte, de conformidad con lo dispuesto en el art. 779 de la LEC 1/2000, el procedimiento que se insta deberá tener carácter preferente.

Conforme a lo dispuesto en el art. 3.2 LO 1/2025, la presente demanda no está sujeta al requisito de MASC, en cuanto se dirige contra una entidad pública como lo es en este caso [ÓRGANO ADMINISTRATIVO].

VI. DERECHO SUSTANTIVO.- La conciencia social y la legislación vigente consideran, en principio, a la propia familia como el entorno más adecuado para el desarrollo personal y social del menor. Sólo cuando la atención prestada por la propia familia presente carencias graves puede llegar a declararse en desamparo el menor, con todo lo que esto implica. La valoración de la situación y la decisión que se adopte al respecto, puede afectar al bienestar del menor y a su futura relación con su familia de origen.

El art. 172.1.II CC establece que se considera como situación de desamparo la que se produce como consecuencia del incumplimiento, o del imposible o inadecuado ejercicio de los deberes de protección establecidos por las leyes para la guarda de los menores, cuando estos queden privados de la adecuada asistencia moral o material. Pero nada de esto se da en el caso presente, careciendo la medida adoptada de fundamento, o en el mejor de los casos, resultando claramente desproporcionada, pues el menor puede ser perfectamente atendido en su propio entorno familiar, con las oportunas medidas de ayuda o apoyo familiar si se consideran necesarias.

La resolución impugnada, que declara el desamparo del/de los menor/es se basa, fundamentalmente, en la dependencia de las drogas de mis representados y en llevar estos una vida desordenado y ser autores de diversos actos delictivos.

Pero como se deduce de la documentación que acompaña a esta demanda y podrá corroborarse con la práctica de las pruebas que se realicen en el momento oportuno, esta situación, que pudo existir en tiempos pasados, no se corresponde con las circunstancias actuales de mis representados que, desde el mes de [MES] del año [AÑO], después de diversos tratamientos, han dejado las drogas y no ha cometido más delitos, por lo que llevan una vida ordenada y adecuada para atender a su/s hijo/s, el/los menor/es

No existe base por tanto, para alejar al/a los menor/es de su entorno familiar, lo que podría tener consecuencias irreversibles.

Subsidiariamente, para el caso de no considerarse así, solicitan mis representados que se les conceda un régimen de visitas más amplio que el fijado en la resolución impugnada y se programe una nueva evaluación de la situación dentro de [Nº] meses.

-VII. COSTAS.- Procede imponer las costas a la entidad pública demandada, conforme al art. 394 LEC, de cuya aplicación no está exenta.

VIII. Iura novit curia y los demás que en Derecho procedan.

En su virtud:

SUPLICO AL TRIBUNAL: Que teniendo por presentado este escrito, en tiempo y forma, con los documentos que se acompañan, se sirva admitirlo, tenga por interpuesta DEMANDA DE OPOSICIÓN A LA DECLARACIÓN DE DESAMPARO DEL MENOR [NOMBRE DEL MENOR] efectuada por resolución de fecha [DÍA] de [MES] de [AÑO] de la Delegación Territorial de [LOCALIDAD], Consejería de Bienestar Social (u organismo que corresponda según la Comunidad Autónoma de que se trate) de la Comunidad Autónoma de [LOCALIDAD] y, estimando lo que en él se solicita y previos los trámites legales oportunos, declare nula y sin efecto la citada resolución, por no darse los presupuestos necesarios para la declaración de desamparo, y acuerde la entrega inmediata de los menores a sus padres; o subsidiariamente, de no estimarse esta pretensión, se amplíe el régimen de visitas concedido a mis representados por la resolución impugnada, programándose una nueva evaluación de la situación dentro de [Nº] meses.

OTROSÍ DIGO: La cuantía del procedimiento resulta inestimable, por carecer su objeto de interés económico.

En [LOCALIDAD], [DÍA] de [MES] de [AÑO]

Firma y número del Letrado	Firma del Procurador

========================================================================
