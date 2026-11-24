---
name: demanda-conviviente-superstite-pareja-estable-contra-civ-0233
description: "Demanda del conviviente supérstite de pareja estable contra el heredero (Cataluña). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda del conviviente supérstite de pareja estable contra el heredero (Cataluña)

> Formulario **CIV-0233** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda del conviviente supérstite de pareja estable contra el heredero (Cataluña)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda del conviviente supérstite de pareja estable contra el heredero (Cataluña)” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-conviviente-superstite-pareja-estable-contra-civ-0233`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (11 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] Nº DE DOCUMENTO (6 veces)
- [ ] FECHA (4 veces)
- [ ] IMPORTE (4 veces)
- [ ] AÑO (2 veces)
- [ ] Nº (2 veces)
- [ ] ACTIVIDAD
- [ ] DÍA
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] MES
- [ ] NOMBRE Y APELLIDOS DEL ABOGADO
- [ ] SEDE
- [ ] ÓRGANO

## Normas que cita el formulario

- art. 234 Código Civil
- art. 232 Código Civil
- art. 232 CC
- art. 52.1.4 LEC
- art. 85.1 LOPJ
- art. 5 Ley Orgánica 1/2025
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

- Junto a «…A, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE Q.P.T.R.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.

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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE Q.P.T.R.C.

D./Dña. [NOMBRE Y APELLIDOS] Procurador/a de los Tribunales, actuando en representación de D./Dña. [NOMBRE Y APELLIDOS], según se acredita por certificación del registro electrónico de apoderamientos judiciales que acompaño (o mediante designación apud acta ante el Letrado de la Administración de Justicia de [SEDE]), bajo la dirección letrada de D/Dª [NOMBRE Y APELLIDOS], Abogado/a del Iltre. Colegio de [LOCALIDAD], ante el Tribunal comparezco y como mejor en derecho proceda formulo demanda de juicio ordinario en reclamación de la compensación por trabajo y los derechos viduales familiares por muerte de D./Dña. [NOMBRE Y APELLIDOS], pareja estable de mi representado/a, prevista en el artículo 234-14 del Código Civil de Cataluña contra los herederos del causante D [NOMBRE Y APELLIDOS] y D [NOMBRE Y APELLIDOS], con domicilio sito en [LOCALIDAD], en base a los siguientes hechos y fundamentos de derecho:

HECHOS

PRIMERO.- El pasado día [FECHA] falleció en la localidad de [LOCALIDAD] D [NOMBRE Y APELLIDOS], pareja estable de mi representado, quien había residido en el domicilio sito en [LOCALIDAD], de la localidad de [LOCALIDAD], ostentando la vecindad foral de Navarra (acompaño como documentos números [Nº DE DOCUMENTO] certificado de defunción del finado).

En fecha [FECHA], el fallecido D [NOMBRE Y APELLIDOS] otorgó testamento en el año instituyendo como heredero al demandado D [NOMBRE Y APELLIDOS] ( acompaño como documento número certificación del Registro de Actos de Última Voluntad y copia simple del testamento de fecha [FECHA]).

SEGUNDO.- En el testamento antes citado no se hizo ninguna mención a mi representado, puesto que fue con posterioridad al otorgamiento de dicho testamento, concretamente en fecha [FECHA], que el causante D [NOMBRE Y APELLIDOS] inició una relación estable de pareja con el demandante, que se prolongó durante [Nº] años, estando conviviendo ambos miembros de la pareja hasta que se produjo el fallecimiento del causante [ÓRGANO] (acompaño como documentos número [Nº DE DOCUMENTO] escritura de constitución de pareja estable a efectos acreditativos).

TERCERO.- De acuerdo a los anteriores hechos, se dan los requisitos establecidos en el artículo 234-4 del Código Civil de Cataluña para el reconocimiento de los derechos viduales reconocidos por los artículos 231-30 y 231-31 del mismo texto legal, solicitándose que se declare el derecho de mi representado al uso del domicilio familiar durante el año siguiente al de fallecimiento y a la propiedad de la ropa, mobiliario y utensilios que forman el ajuar de la vivienda familiar y que se detallan en la escritura de inventario que se acompaña como documento

CUARTO.- Asimismo, y de conformidad con el precitado artículo 234-4 se solicita que se fije una compensación por razón de trabajo prevenida en el apartado 5 del artículo 232-5 del Código Civil de Cataluña en compensación del trabajo realizado por mi mandante en el hogar familiar, que ha impedido su propia proyección personal y ha servido de base y ayuda, liberándose su pareja estable, pudiendo ejercer éste plenamente su actividad comercial hasta el momento del fallecimiento, y sin que se le haya atribuido ningún bien en la herencia del causante.

En efecto, mi mandante se dedicó de forma exclusiva durante todos estos años al trabajo doméstico y al cuidado de su pareja, en tanto que su pareja pudo seguir dedicándose por completo a su negocio de [ACTIVIDAD], con unos ingresos anuales de [IMPORTE] euros, tal como se acredita por las liquidaciones de IRPF que se acompañan como documentos [Nº DE DOCUMENTO] correspondientes a los ejercicios [AÑO], habiendo adquirido varios inmuebles durante la convivencia tal como se acredita por los documentos [Nº DE DOCUMENTO] valorados en [IMPORTE] euros según informe pericial que se acompaña como documento número

Por su parte, mi mandante no percibía ningún tipo de retribución, dedicándose plenamente al trabajo doméstico, y sin que haya observado por tanto ningún tipo de incremento patrimonial, por lo que procede establecer la compensación del artículo 232-5 del CC de Cataluña, debiendo calcularse conforme a lo que dispone el apartado 3 de dicho precepto, proponiéndose el criterio de cuantificación en función del sueldo que cobraría por realizar el trabajo una tercera persona, de modo que se contribuye con lo que se deja de desembolsar o se ahorra por la falta de necesidad de contratar servicio doméstico ante la dedicación de uno de los cónyuges al cuidado del hogar, por lo cual se solicita la cantidad de [IMPORTE] euros, tomando en cuenta el salario mensual multiplicado por [Nº] años de convivencia.

En cumplimiento de lo dispuesto en la disposición adicional tercera del libro II del CC de Cataluña, se acompaña propuesta de inventario como documento número [Nº DE DOCUMENTO]

QUINTO.- Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

FUNDAMENTOS DE DERECHO

Competencia

Corresponde a los Tribunales de [LOCALIDAD] al ser el lugar en el que el finado tuvo su último domicilio ( artículo 52.1.4ª LEC, en relación con lo dispuesto en el art. 85.1º LOPJ).

Legitimación

Le corresponde activamente a esta parte en su condición de miembro sobreviviente de la pareja estable que formaba con el causante, y en la parte pasiva al heredero del causante.

Procedimiento

Es el juicio ordinario con fundamento en el art. 249,2 dado el importe de los bienes excede en todo caso de 15.000 € a partir de los que se deben seguir las reclamaciones por las normas del juicio ordinario.

Cumplimiento de los requisitos de procedibilidad

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

Fondo de reclamación

El artículo 234-14 del Código Civil de Cataluña establece que “en caso de extinción de la pareja por muerte de uno de los convivientes, el superviviente tiene, además de la compensación por razón de trabajo que eventualmente le corresponda de acuerdo con el artículo 232-5.5, los derechos viduales familiares reconocidos por los artículos 231-30 y 231-31”.

Costas

En materia de costas el art. 394 LEC señala que las de primera instancia se imponen a la parte que vea en primera instancia rechazadas sus pretensiones.

En base a lo anterior,

SUPLICO al Tribunal que tenga por presentada la presente demanda con los documentos a ella adjuntos y por parte en la representación que ostento y tras la pertinente tramitación se dicte por ese Tribunal sentencia por la que se declare el derecho de mi representado al usufructo de fidelidad sobre los bienes del causante D [NOMBRE Y APELLIDOS], condenando al demandado a estar y pasar por dicha declaración, rindiendo cuentas del producto obtenido de los bienes del causante desde el momento de su fallecimiento y a que indemnice a mi representado en la cantidad obtenida, con más los intereses correspondientes, todo ello con imposición de costas a la parte demandada.

OTROSÍ PRIMERO DIGO.- Se fija la cuantía del presente procedimiento en [IMPORTE] euros.

SUPLICO AL TRIBUNAL: que tenga por hecha la anterior manifestación a los efectos pertinentes y por acompañado el documento justificativo del abono de la tasa.

a [DÍA] de [MES] de [AÑO]

Firma de Abogado [NOMBRE Y APELLIDOS DEL ABOGADO] Firma de Procurador

========================================================================
