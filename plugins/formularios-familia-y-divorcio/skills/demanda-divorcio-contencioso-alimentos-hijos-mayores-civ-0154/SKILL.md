---
name: demanda-divorcio-contencioso-alimentos-hijos-mayores-civ-0154
description: "Demanda de divorcio contencioso con alimentos para hijos mayores de edad (Derecho catalán). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de divorcio contencioso con alimentos para hijos mayores de edad (Derecho catalán)

> Formulario **CIV-0154** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de divorcio contencioso con alimentos para hijos mayores de edad (Derecho catalán)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de divorcio contencioso con alimentos para hijos mayores de edad (Derecho catalán)” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-divorcio-contencioso-alimentos-hijos-mayores-civ-0154`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (7 veces)
- [ ] Nº DE DOCUMENTO (7 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] AÑO (3 veces)
- [ ] CALLE (3 veces)
- [ ] MES (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] PISO (3 veces)
- [ ] FECHA (2 veces)
- [ ] Nº (2 veces)
- [ ] PUERTA (2 veces)
- [ ] SEDE (2 veces)
- [ ] ACTIVIDADES FORMATIVAS
- [ ] AÑOS (EJERCICIOS)
- [ ] CARGO
- [ ] DÍA
- [ ] EMPRESA O LUGAR DE TRABAJO
- [ ] FOLIO
- [ ] LUGAR
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº DE CURSO
- [ ] PARTE DEMANDADA
- [ ] TOMO

## Normas que cita el formulario

- art. 86 Código Civil
- art. 237 Código Civil
- art. 233 Código Civil
- art. 232 Código Civil
- art. 232 CC
- art. 769 LEC
- art. 85.1 LOPJ
- art. 770 LEC
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025

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

### Avisos de actualización (4) — se aplican en el texto, nunca se copian en el documento

- Junto a «…NCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.R.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.
- Junto a «…n [NOMBRE Y APELLIDOS] ante la Sección Civil del Tribunal de Instancia de [SEDE]»: Un solo TI por partido judicial (art. 84.1 LOPJ): sobra «de los de». Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).
- Junto a «…ue por turno de reparto corresponda (o Sección de Familia, Infancia y Capacidad)»: Denominación legal: Sección de Familia, Infancia y Capacidad. Si no existe en el partido, conoce la Sección Civil o la Única (art. 86.3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.R.C.

Don [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en la representación que ostento de Doña [NOMBRE Y APELLIDOS], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], y bajo la dirección Letrada de Don [NOMBRE Y APELLIDOS] ante la Sección Civil del Tribunal de Instancia de [SEDE] que por turno de reparto corresponda (o Sección de Familia, Infancia y Capacidad) comparezco y como mejor proceda en Derecho, DIGO:

Que siguiendo instrucciones de mi poderdante por medio del presente escrito interpongo, en nombre del mismo, DEMANDA DE DISOLUCIÓN MATRIMONIAL POR DIVORCIO, contra D. [NOMBRE Y APELLIDOS], vecino de la localidad de [LOCALIDAD], con domicilio en calle [CALLE], nº [NÚMERO], piso [PISO], puerta [PUERTA], la cual baso en los siguientes

PRIMERO.- HECHOS

Mi representada y el marido, ahora demandado, de vecindad civil catalana, contrajeron matrimonio en forma (civil o religiosa que corresponda) el día [FECHA], del mes de [MES], del año, en [LOCALIDAD], según acredito mediante certificación literal del Registro civil de la localidad de que acompaño como documento nº [Nº DE DOCUMENTO], constando inscrito el mismo en el Tomo [TOMO], Folio [FOLIO], Sección

SEGUNDO.- Del referido matrimonio nació y vive una única hija, nacida el día [FECHA], del mes de [MES] del año [AÑO], por lo que en la actualidad tiene [Nº] años de edad. En prueba de lo manifestado acompaño certificación literal del Registro civil como documento nº [Nº DE DOCUMENTO]

La hija, mayor de edad, convive habitualmente con mi representada en el domicilio familiar como se expondrá seguidamente.

TERCERO.- El que fue domicilio conyugal, que actualmente ocupan la esposa y la hija común, mayor de edad, es el ubicado en la localidad de [LOCALIDAD], calle [CALLE], nº [NÚMERO], piso [PISO], puerta

El demandado actualmente tiene su domicilio en [LOCALIDAD], calle [CALLE], nº [NÚMERO], piso [PISO], puerta [PUERTA]

CUARTO.- El régimen económico del matrimonio es el de separación de bienes por ser ambos cónyuges de vecindad civil catalana y no haber pactado otro régimen económico.

QUINTO.- Habiendo transcurrido el período establecido en el artículo 86 del Código Civil y por razones que no son del caso exponer, lo cierto es que la convivencia entre los cónyuges se ha deteriorado, con la consiguiente pérdida de la «affectio maritalis», lo cual determina la concurrencia de la causa de disolución del matrimonio por divorcio que se invoca en este proceso conforme al citado artículo 86 del Código Civil.

SEXTO.- Por lo que se refiere a las medidas que deben fijarse como consecuencia del divorcio, por medio de la presente demanda se reclama una pensión por alimentos para la hija común y la atribución de la vivienda familiar a mi representada e hija.

A) En relación a los alimentos de la hija común, mayor de edad, debe subrayarse que la hija está conviviendo habitualmente con mi representada, quien está costeando todos sus gastos de mantenimiento, vestido y educación, puesto que está cursando estudios en la Universidad de [LOCALIDAD], hallándose en la actualidad en el [Nº DE CURSO] curso de la carrera universitaria de

Por este motivo, y de acuerdo a lo dispuesto en el artículo 233-4 en relación con el artículo 237-1 y 237-9 del Código Civil de Cataluña se solicita que se fije la cantidad de [IMPORTE] euros mensuales a cargo del demandado en concepto de alimentos para la hija común, tomando en consideración la capacidad económica del demandado, quien está trabajando en [EMPRESA O LUGAR DE TRABAJO] y percibe unas rentas mensuales de [IMPORTE] euros (se acompaña como documentos [Nº DE DOCUMENTO] declaraciones tributarias conjuntas de los dos últimos ejercicios acreditativas de los ingresos del demandado) y las necesidades de la hija común, con unos gastos fijos por estudios en concepto de matrícula y material por importe de …. euros anuales, estando además cursando las siguientes actividades formativas [ACTIVIDADES FORMATIVAS] se acompaña como documentos [Nº DE DOCUMENTO] justificantes de gastos por estudios de la hija común). Se solicita que esta cantidad se abone por el demandado hasta tanto la hija común tenga ingresos propios o esté en disposición de obtenerlos.

B) En cuanto a la vivienda familiar, se solicita que se atribuya a mi representada, por ser el interés más necesitado de protección al estar conviviendo la hija común en el domicilio y hasta tanto se independice la hija, conforme a lo dispuesto en el artículo 233-20 del Código Civil de Cataluña, habiéndose ponderado esta circunstancia a la hora de reclamar la pensión alimenticia por cuanto que la vivienda es titularidad pro indivisa de ambos cónyuges.

SEPTIMO.- Además de las medidas solicitadas y rigiendo el régimen económico-matrimonial de separación de bienes, se está en el caso de solicitar la compensación prevenida en el artículo 232-5 del Código Civil de Cataluña en compensación del trabajo realizado por mi mandante en el hogar familiar, que ha impedido su propia proyección personal y ha servido de base y ayuda, liberándose al otro cónyuge, para que puede ejercer éste su carrera profesional.

En efecto, mi mandante se ha dedicado de forma exclusiva durante todos estos años al trabajo doméstico y al cuidado del esposo e hija común, en tanto que el demandado ha podido continuar su carrera profesional, ostentado el cargo de [CARGO] en la empresa y percibiendo una retribución mensual de [IMPORTE] euros, tal como se acredita por las liquidaciones de IRPF que se acompañan como documentos [Nº DE DOCUMENTO] correspondientes a los ejercicios [AÑOS (EJERCICIOS)], de donde se aprecia que el demandante ha adquirido varios inmuebles constante matrimonio, con un valor de [IMPORTE] euros. Por su parte, mi mandante no ha percibido ningún tipo de retribución ni ha podido adquirir ningún bien al dedicarse plenamente al trabajo doméstico, por lo que procede establecer la compensación del artículo 232-5 del CC de Cataluña, debiendo calcularse conforme a lo que dispone el apartado 3 de dicho precepto, proponiéndose el criterio de cuantificación en función del sueldo que cobraría por realizar el trabajo una tercera persona, de modo que se contribuye con lo que se deja de desembolsar o se ahorra por la falta de necesidad de contratar servicio doméstico ante la dedicación de uno de los cónyuges al cuidado del hogar, por lo cual se solicita la cantidad de [IMPORTE] euros, tomando en cuenta el salario mensual multiplicado por [Nº] años de matrimonio.

OCTAVO.- Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

A los anteriores Hechos les son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

Competencia y procedimiento

Es competente este Tribunal al que tengo el honor de dirigirme, de conformidad con lo previsto en el artículo 769 de la LEC, en relación con lo dispuesto en el art. 85.1º LOPJ, debiendo seguirse el procedimiento regulado en el artículo 770 de la LEC.

Legitimación activa y pasiva

La ostentan ambas partes por su condición de cónyuges del matrimonio cuya disolución por divorcio se solicita, en relación con la causa legal invocada, estando legitimada mi representada para reclamar los alimentos para la hija común según dispone el apartado 1 del artículo 233-4 del Código Civil de Cataluña.

Cumplimiento de los requisitos de procedibilidad

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

Disolución por divorcio

Artículo 86 del Código Civil en relación con el artículo 81.

Efectos derivados o medidas

Artículo 233-4 del Código Civil de Cataluña en relación con los artículos 237-1 y siguientes (alimentos en nombre de la hija mayor), artículo 233-20 (vivienda conyugal) y 232-5 (compensación económica por razón de trabajo).

Costas. Artículo 394 de la LEC

En su virtud

SUPLICO AL TRIBUNAL: Que tenga por presentado este escrito con los documentos acompañados y sus copias; admita todo ello; por interpuesta por el Procurador que suscribe, con quien se entiendan las sucesivas diligencias, en nombre y representación de [NOMBRE DEL REPRESENTADO/A], DEMANDA DE DISOLUCIÓN MATRIMONIAL POR DIVORCIO contra [PARTE DEMANDADA]; y previa notificación y emplazamiento, y por los trámites procesales pertinentes, dicte sentencia por la que, dando lugar a dicha disolución, del matrimonio, determine como medidas o efectos derivadas de la misma, los siguientes:

1º) Que se atribuya el uso del domicilio familiar sito en [LOCALIDAD], a mi representada hasta tanto la hija común se independice.

2º) En concepto de pensión alimenticia a favor de la hija común, el demandado abonará a la madre la suma de [IMPORTE] euros mensuales. Dicha cantidad deberá ser ingresada en la cuenta que al efecto se designe, dentro de los cinco días primeros de cada mes, cantidad que se actualizará anualmente conforme a las variaciones que experimente el IPC que publique el Instituto Nacional de Estadística u Organismo que lo sustituya, siendo la primera actualización en el mes de Enero de [AÑO].

3º) Que en concepto de indemnización ex-artículo 232-5 del Código Civil de Cataluña a favor de la demandante con cargo al demandado se establezca la suma total de [IMPORTE] euros que deberá ser abonada en el plazo de veinte días a contar desde la fecha de la Sentencia, momento a partir del cual, si no ha sido abonada devengará el interés legal.

4º) Y con condena en costas a la parte demandada, si concurrieren las circunstancias previstas en el artículo 394 de la Ley de Enjuiciamiento Civil.

En virtud de lo anterior,

SUPLICO AL TRIBUNAL: que tenga por hecha la anterior manifestación a los efectos pertinentes.

Es justicia que insto en [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma de Abogado y Procurador

========================================================================
