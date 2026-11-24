---
name: demanda-separacion-contenciosa-privacion-potestad-civ-0155
description: "Demanda de separación contenciosa con privación de la potestad parental (Derecho catalán). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de separación contenciosa con privación de la potestad parental (Derecho catalán)

> Formulario **CIV-0155** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de separación contenciosa con privación de la potestad parental (Derecho catalán)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de separación contenciosa con privación de la potestad parental (Derecho catalán)” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-separacion-contenciosa-privacion-potestad-civ-0155`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (8 veces)
- [ ] Nº DE DOCUMENTO (6 veces)
- [ ] NÚMERO (5 veces)
- [ ] IMPORTE (4 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] AÑO (3 veces)
- [ ] CALLE (3 veces)
- [ ] MES (3 veces)
- [ ] PISO (3 veces)
- [ ] PUERTA (3 veces)
- [ ] FECHA (2 veces)
- [ ] SEDE (2 veces)
- [ ] ACTIVIDADES FORMATIVAS
- [ ] DATOS DE LAS SENTENCIAS
- [ ] DÍA
- [ ] EMPRESA O LUGAR DE TRABAJO
- [ ] FOLIO
- [ ] LUGAR
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº
- [ ] Nº DE PROCEDIMIENTO
- [ ] PARTE DEMANDADA
- [ ] TOMO

## Normas que cita el formulario

- art. 81 Código Civil
- art. 236 Código Civil
- art. 236 CC
- art. 233 Código Civil
- art. 769 LEC
- art. 89.6.a LOPJ
- art. 15 LEC
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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Junto a «…(o A LA SECCIÓN DE VIOLENCIA SOBRE LA MUJER DEL TRIBUNAL DE INSTANCIA DE [SEDE])»: Denominación legal: Sección de Familia, Infancia y Capacidad. Si no existe en el partido, conoce la Sección Civil o la Única (art. 86.3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD DEL TRIBUNAL DE INSTANCIA (o A LA SECCIÓN DE VIOLENCIA SOBRE LA MUJER DEL TRIBUNAL DE INSTANCIA DE [SEDE])

Don [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en la representación que ostento de Doña [NOMBRE Y APELLIDOS], según acredito mediante designación apud-acta otorgada ante el Letrado de la Administración de Justicia de [LOCALIDAD], y bajo la dirección Letrada de Don [NOMBRE Y APELLIDOS] ante la Sección civil del Tribunal de Instancia de [SEDE] (o Sección de familia) comparezco y como mejor proceda en Derecho, DIGO:

Que siguiendo instrucciones de mi poderdante por medio del presente escrito interpongo, en nombre del mismo, DEMANDA DE SEPARACIÓN MATRIMONIAL, contra D. [NOMBRE Y APELLIDOS], vecino de la localidad de [LOCALIDAD], con domicilio en calle [CALLE], nº [NÚMERO], piso [PISO], puerta [PUERTA], la cual baso en los siguientes

HECHOS

Mi representada y el marido, ahora demandado, de vecindad civil catalana, contrajeron matrimonio en forma (civil o religiosa que corresponda) el día [FECHA], del mes de [MES], del año [AÑO], en [LOCALIDAD], según acredito mediante certificación literal del Registro civil de la localidad de que acompaño como documento nº [Nº DE DOCUMENTO], constando inscrito el mismo en el Tomo [TOMO], Folio [FOLIO], Sección

Del referido matrimonio nació y vive una única hija, nacida el día [FECHA], del mes de [MES] del año [AÑO], por lo que en la actualidad tiene [Nº] años de edad. En prueba de lo manifestado acompaño certificación literal del Registro civil como documento nº [Nº DE DOCUMENTO]

El que fue domicilio conyugal, que actualmente ocupan la esposa y la hija común, mayor de edad, es el ubicado en la localidad de [LOCALIDAD], calle [CALLE], nº [NÚMERO], piso [PISO], puerta [PUERTA].

El demandado actualmente tiene su domicilio en [LOCALIDAD], calle [CALLE], nº [NÚMERO], piso [PISO], puerta [PUERTA]

El régimen económico del matrimonio es el de separación de bienes por ser ambos cónyuges de vecindad civil catalana y no haber pactado otro régimen económico.

Habiendo transcurrido el período establecido en el artículo 81 del Código Civil y dados los reiterados episodios de violencia por parte del demandado, tanto en relación a mi representada como a la hija común, tal como se expondrá seguidamente, lo cierto es que la convivencia entre los cónyuges se ha vuelto insostenible, lo cual determina la concurrencia de la causa de separación que se invoca en este proceso conforme al citado artículo 81 del Código Civil.

En cuanto a las medidas a adoptar, se solicita en primer lugar la privación de la potestad parental del demandado en relación a la hija común, al amparo de lo dispuesto en el artículo 236-6 del Código Civil de Cataluña, puesto que ha incumplido de forma grave y reiterada sus deberes con relación a la hija menor, observando la más absoluta desatención y abandono, y habiendo observado una conducta continuada de malos tratos físicos y psíquicos tanto contra la madre como contra la menor, siguiéndose los siguientes procesos penales por violencia de género [Nº DE PROCEDIMIENTO] y habiendo recaído las siguientes sentencias condenatorias [DATOS DE LAS SENTENCIAS]. Como consecuencia de esta conducta de maltrato físico y psíquico el padre ha sido suspendido del ejercicio de la potestad parental en el proceso número [NÚMERO] seguido ante la Sección de Violencia sobre la Mujer del Tribunal de Instancia número [NÚMERO].

Por tanto, concurre la causa de privación de la potestad parental establecida en el apartado 1 del artículo 236-6 del CC de Cataluña, puesto que la hija menor es víctima de violencia familiar, aportándose a efectos acreditativos como documento [Nº DE DOCUMENTO] informe del Equipo Técnico de [LOCALIDAD], donde se reflejan detalladamente la sucesión de episodios de violencia familiar contra la madre e hija y las consecuencias negativas para la menor derivadas de esta situación, dictaminándose que debe excluirse cualquier tipo de comunicación entre padre e hija en interés de la menor, solicitándose que se prive asimismo al demandado del derecho a visitas con la hija para evitar a ésta cualquier perjuicio personal.

Por lo que se refiere al resto de las medidas que deben fijarse como consecuencia de la separación, por medio de la presente demanda se reclama una pensión por alimentos para la hija por importe de [IMPORTE] euros y la atribución de la vivienda familiar a mi representada e hija.

A) En relación a los alimentos de la hija, el demandado resulta obligado no obstante ser privado de la potestad parental de acuerdo a lo dispuesto en el apartado 6 del artículo 236-6 del Código Civil de Cataluña, solicitándose que se fije la cantidad de [IMPORTE] euros mensuales a cargo del demandado en concepto de alimentos para la hija común, tomando en consideración la capacidad económica del demandado, quien está trabajando en [EMPRESA O LUGAR DE TRABAJO] y percibe unas rentas mensuales de [IMPORTE] euros (se acompaña como documentos [Nº DE DOCUMENTO] declaraciones tributarias conjuntas de los dos últimos ejercicios acreditativas de los ingresos del demandado) y las necesidades de la hija común, que está cursando estudios en el colegio de [LOCALIDAD], además de las siguientes actividades formativas [ACTIVIDADES FORMATIVAS] (se acompaña como documentos [Nº DE DOCUMENTO] justificantes de gastos por estudios de la hija común).

B) En cuanto a la vivienda familiar, se solicita que se atribuya a mi representada, por ser el interés más necesitado de protección, conforme a lo dispuesto en el apartado 2 del artículo 233-20 del Código Civil de Cataluña, habiéndose ponderado esta circunstancia a la hora de reclamar la pensión alimenticia por cuanto que la vivienda es titularidad pro indivisa de ambos cónyuges.

Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

A los anteriores Hechos les son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

Competencia y procedimiento

Es competente este Tribunal al que tengo el honor de dirigirme, de conformidad con lo previsto en el artículo 769 de la LEC [o artículo 89.6.a) de la LOPJ en relación con el artículo 15 de la LECrim.], debiendo seguirse el procedimiento regulado en el artículo 770 de la LEC.

Legitimación activa y pasiva

La ostentan ambas partes por su condición de cónyuges del matrimonio cuya separación se solicita, en relación con la causa legal invocada, estando legitimada mi representada para solicitar la privación de la potestad parental del otro cónyuge conforme al artículo 236-3.2 del CC de Cataluña.

Cumplimiento de los requisitos de procedibilidad

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

Separación

Artículo 81 del Código Civil.

Privación de la potestad parental y del régimen de comunicación y visitas

Artículo 236-6 en relación con los artículos 236-3 y siguientes del CC de Cataluña.

Efectos derivados y medidas

Artículo 233-4 del Código Civil de Cataluña en relación con los artículos 233-2 y 236-6.6 (alimentos) y artículo 233-20 (vivienda conyugal).

Costas. Artículo 394 de la LEC

En su virtud

SUPLICO AL TRIBUNAL: Que tenga por presentado este escrito con los documentos acompañados y sus copias; admita todo ello; por interpuesta por el Procurador que suscribe, con quien se entiendan las sucesivas diligencias, en nombre y representación de [NOMBRE DEL REPRESENTADO/A], DEMANDA DE SEPARACIÓN contra [PARTE DEMANDADA]; y previa notificación y emplazamiento, y por los trámites procesales pertinentes, dicte sentencia por la que, dando lugar a dicha separación del matrimonio, determine como medidas o efectos derivadas de la misma, los siguientes:

1º) Que se prive de la potestad parental de la hija menor al demandado, así como de cualquier comunicación y visita respecto de la hija, atribuyendo de forma exclusiva la potestad parental a mi representada.

2º) En concepto de pensión alimenticia a favor de la hija común, el demandado abonará a la madre la suma de [IMPORTE] euros mensuales. Dicha cantidad deberá ser ingresada en la cuenta que al efecto se designe, dentro de los cinco días primeros de cada mes, cantidad que se actualizará anualmente conforme a las variaciones que experimente el IPC que publique el Instituto Nacional de Estadística u Organismo que lo sustituya, siendo la primera actualización en el mes de Enero de

3º) Que se atribuya el uso del domicilio familiar sito en [LOCALIDAD], a mi representada.

4º) Y con condena en costas a la parte demandada, si concurrieren las circunstancias previstas en el artículo 394 de la Ley de Enjuiciamiento Civil.

Es justicia que insto en [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma de Abogado y Procurador

========================================================================
