---
name: demanda-guarda-custodia-alimentos-hijos-menores-civ-0240
description: "Demanda de guarda y custodia y alimentos de hijos menores (Derecho civil catalán). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de guarda y custodia y alimentos de hijos menores (Derecho civil catalán)

> Formulario **CIV-0240** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda de un progenitor, de vecindad civil catalana, contra el otro progenitor tras la ruptura de la pareja estable, para fijar la guarda y custodia, el régimen de visitas, los alimentos de los hijos menores y la atribución del uso de la vivienda familiar (arts. 234-7 a 234-10 del Código Civil de Cataluña), tramitada por las normas de los procesos matrimoniales y de menores (arts. 769 y 770 LEC).

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de guarda y custodia y alimentos de hijos menores (Derecho civil catalán)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de guarda y custodia y alimentos de hijos menores (Derecho civil catalán)” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-guarda-custodia-alimentos-hijos-menores-civ-0240`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (10 veces)
- [ ] HORA (4 veces)
- [ ] IMPORTE (4 veces)
- [ ] PADRE/MADRE (4 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] AÑO (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] DURACIÓN (2 veces)
- [ ] EDAD (2 veces)
- [ ] EL/LA DEMANDANTE (2 veces)
- [ ] ENTIDAD (2 veces)
- [ ] FECHA (2 veces)
- [ ] IBAN (2 veces)
- [ ] NOMBRE (2 veces)
- [ ] NOMBRE DE LOS HIJOS (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL DEMANDADO (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL DEMANDANTE (2 veces)
- [ ] SEDE (2 veces)
- [ ] CALLE
- [ ] DÍA
- [ ] EMPRESA O ACTIVIDAD
- [ ] MES
- [ ] NOMBRE Y APELLIDOS
- [ ] NOMBRE Y APELLIDOS DEL ABOGADO/A
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] NOMBRE Y APELLIDOS, Nº DE COLEGIADO
- [ ] PISO
- [ ] PROFESIÓN
- [ ] PUERTA

## Normas que cita el formulario

- art. 234 Código Civil
- art. 770.1.ª LEC
- art. 769 LEC
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 770.4 LEC
- art. 749.2.º LEC

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

- Junto a «…MILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
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

[OPCIONAL — si ha lugar: pueden solicitarse además otras medidas derivadas de la ruptura de la pareja estable, según se indica en la disposición adicional sexta del libro segundo del Código Civil de Cataluña.]

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]

[ELEGIR: Q.P.T.R.C. — SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD (si en la sede se ha constituido), o Sección Civil que por turno de reparto corresponda]

Don/Doña [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, en la representación que ostento de Doña/Don [NOMBRE Y APELLIDOS DEL DEMANDANTE], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento n.º [Nº], y bajo la dirección letrada de Don/Doña [NOMBRE Y APELLIDOS DEL ABOGADO/A], ante la Sección Civil del Tribunal de Instancia de [SEDE] que por turno de reparto corresponda [OPCIONAL — si ha lugar: o ante la Sección de Familia, Infancia y Capacidad], comparezco y, como mejor proceda en Derecho, DIGO:

Que, siguiendo instrucciones de mi poderdante, por medio del presente escrito interpongo, en nombre del mismo/de la misma y de sus hijos menores, DEMANDA SOBRE GUARDA Y CUSTODIA Y RECLAMACIÓN DE ALIMENTOS EN NOMBRE DE LOS HIJOS MENORES [NOMBRE DE LOS HIJOS] y [NOMBRE DE LOS HIJOS] de los litigantes, contra Don/Doña [NOMBRE Y APELLIDOS DEL DEMANDADO], vecino/a de la localidad de [LOCALIDAD], con domicilio en calle [CALLE], núm. [Nº], piso [PISO], puerta [PUERTA], la cual baso en los siguientes

HECHOS

PRIMERO.– Mi representado/a y el/la demandado/a, ambos de vecindad civil catalana, han venido manteniendo una relación de convivencia estable, fruto de la cual nacieron y viven en la actualidad dos hijos menores de edad llamados [NOMBRE] y [NOMBRE], nacidos los días [FECHA] y [FECHA], por consiguiente, de [EDAD] y [EDAD] años de edad respectivamente, según acredito mediante certificación literal del Registro Civil de la localidad de [LOCALIDAD] que acompaño como documento número [Nº].

SEGUNDO.– Mi representado/a y el/la demandado/a han venido residiendo desde el año [AÑO] en el domicilio familiar sito en [DOMICILIO], propiedad exclusiva del/de la demandado/a, en compañía de sus hijos desde el nacimiento de éstos.

TERCERO.– Como consecuencia de desavenencias personales que se han producido entre mi representado/a y el/la demandado/a, ambos han decidido poner fin a la convivencia, habiéndose trasladado el/la demandado/a a otro domicilio, motivo por el cual se formula la presente demanda a fin de regularizar la situación y fijar los efectos de la extinción de la relación ante la imposibilidad de llegar a un acuerdo con el/la demandado/a.

De acuerdo con lo anterior, debemos instar las siguientes medidas en relación con la guarda y custodia, visitas y comunicación, y alimentos de los hijos comunes:

a) En cuanto a las medidas personales respecto a los hijos comunes, se interesa que se atribuya la custodia de los hijos menores a mi representado/a, con responsabilidad parental compartida, por ser de interés de los menores, y que se establezca un régimen de visitas de los hijos menores a favor del [PADRE/MADRE], proponiéndose que pueda visitarlos y tenerlos en su compañía los fines de semana alternos, desde el viernes a las [HORA] horas hasta el domingo a las [HORA] horas; la mitad de las vacaciones escolares de Navidad, la mitad de las vacaciones escolares de Semana Santa y [DURACIÓN] en verano, eligiendo las fechas alternativamente la madre o el padre según sean años impares o pares en el caso de no llegar a un acuerdo; en todos los casos, el [PADRE/MADRE] deberá recoger y reintegrar a los menores en el domicilio del otro progenitor.

b) En cuanto a los alimentos para los menores, se solicita que se fije una pensión alimenticia en la cantidad de [IMPORTE] euros mensuales que deberá abonarse por el/la demandado/a dentro de los cinco primeros días de cada mes, en la cuenta bancaria n.º [IBAN] que [EL/LA DEMANDANTE] tiene abierta en la entidad financiera [ENTIDAD], oficina n.º [Nº]. Dicha pensión se actualizará automáticamente cada doce meses, incrementándose o disminuyéndose según el IPC que publique el Instituto Nacional de Estadística u otro organismo oficial que pudiera sustituirle. Los gastos extraordinarios que se puedan originar mientras subsista la contribución de alimentos para los hijos deben ser sufragados por mitad entre ambos progenitores.

Se solicita esta cantidad en concepto de pensión teniendo en cuenta los ingresos de cada una de las partes, tomando en consideración, conforme al artículo 234-8, apartado 3, del Código Civil de Cataluña, que se solicita el uso de la vivienda familiar, titularidad del/de la demandado/a, de forma proporcionada en función de las necesidades de los hijos comunes. Así, mi representado/a trabaja en [EMPRESA O ACTIVIDAD] y percibe unos ingresos mensuales aproximados de [IMPORTE] euros, en tanto que el/la demandado/a trabaja como [PROFESIÓN] y percibe unos ingresos mensuales aproximados de [IMPORTE] euros. A los efectos prevenidos en el art. 770.1.ª de la LEC acompaño los documentos de que dispone esta parte acreditativos de los ingresos de uno y otro litigante y que son los siguientes: declaraciones tributarias (documentos n.º [Nº]), nóminas (documentos n.º [Nº]), certificaciones bancarias (documentos n.º [Nº]), certificaciones registrales (documentos n.º [Nº]).

c) En cuanto a la atribución del uso de la vivienda: debe atribuirse el uso de la vivienda familiar a mi representado/a y a los hijos comunes por aplicación del artículo 234-8, apartado 2, del Código Civil de Cataluña, que establece que, en defecto de acuerdo, debe atribuirse preferentemente al miembro de la pareja a quien corresponda la custodia de los hijos y mientras dure ésta, habiéndose tomado en consideración este extremo a la hora de reclamar la pensión alimenticia, tal como se ha indicado anteriormente por aplicación del mismo artículo 234-8, apartado 3.

CUARTO.– Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [INDICAR EL MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS AL QUE LAS PARTES SE HAN SOMETIDO EN CUMPLIMIENTO DEL REQUISITO DE PROCEDIBILIDAD QUE EXIGE LA LO 1/2025], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento n.º [Nº] [ESPECIFICAR EL DOCUMENTO QUE ACREDITA QUE SE HA ACUDIDO A UN MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS].

A los anteriores hechos les son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

Legitimación activa y pasiva

La ostentan ambas partes por su condición de miembros de la pareja estable extinguida y progenitores de los hijos comunes.

Competencia

Es competente este Tribunal, de conformidad con lo previsto en el artículo 769 de la LEC.

Cumplimiento de los requisitos de procedibilidad

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4.º y 399.3 LEC, en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

Efectos derivados o medidas

Artículos 234-7 a 234-10 del Código Civil de Cataluña.

Audiencia de los menores

La audiencia del menor es preceptiva, conforme a lo previsto en el artículo 770.4 de la LEC.

Procedimiento

Son de aplicación las normas contenidas en el Libro IV, Título Primero, Capítulo Primero de la LEC y las normas del juicio verbal, con sujeción, además, a las reglas establecidas en el artículo 770 de la misma ley, conforme se previene en el párrafo preliminar de dicho artículo.

Intervención del Ministerio Fiscal

Procede la intervención del Ministerio Fiscal, por existir dos hijos menores de edad, conforme a lo previsto en el artículo 749.2.º de la LEC.

Costas

Artículo 394 de la LEC.

Demás normas concordantes y de aplicación

Iura novit curia.

En su virtud,

SUPLICO AL TRIBUNAL: Que tenga por presentado este escrito con los documentos acompañados y sus copias; admita todo ello; por interpuesta por el Procurador/a que suscribe, con quien se entiendan las sucesivas diligencias, en nombre y representación de Don/Doña [NOMBRE Y APELLIDOS DEL DEMANDANTE], con devolución de la escritura de poderes una vez quede testimonio en autos, DEMANDA DE GUARDA Y CUSTODIA Y ALIMENTOS EN NOMBRE DE LOS HIJOS MENORES contra Don/Doña [NOMBRE Y APELLIDOS DEL DEMANDADO]; y previa notificación y emplazamiento, y por los trámites procesales pertinentes, con intervención del Ministerio Fiscal y audiencia de los menores, dicte sentencia por la que, dando lugar a las medidas solicitadas, determine las siguientes, condenando al demandado a su cumplimiento:

a) En cuanto a las medidas personales respecto a los hijos comunes: que se atribuya la custodia de los hijos menores a mi representado/a, con responsabilidad parental compartida, por ser de interés de los menores, y que se establezca un régimen de visitas de los hijos menores a favor del [PADRE/MADRE], proponiéndose que pueda visitarlos y tenerlos en su compañía los fines de semana alternos, desde el viernes a las [HORA] horas hasta el domingo a las [HORA] horas; la mitad de las vacaciones escolares de Navidad, la mitad de las vacaciones escolares de Semana Santa y [DURACIÓN] en verano, eligiendo las fechas alternativamente la madre o el padre según sean años impares o pares en el caso de no llegar a un acuerdo; en todos los casos, el [PADRE/MADRE] deberá recoger y reintegrar a los menores en el domicilio del otro progenitor.

b) En cuanto a los alimentos para los menores: que se fije una pensión alimenticia en la cantidad de [IMPORTE] euros mensuales que deberá abonarse por el/la demandado/a dentro de los cinco primeros días de cada mes, en la cuenta bancaria n.º [IBAN] que [EL/LA DEMANDANTE] tiene abierta en la entidad financiera [ENTIDAD], oficina n.º [Nº]. Dicha pensión se actualizará automáticamente cada doce meses, incrementándose o disminuyéndose según el IPC que publique el Instituto Nacional de Estadística u otro organismo oficial que pudiera sustituirle. Los gastos extraordinarios que se puedan originar mientras subsista la contribución de alimentos para los hijos deben ser sufragados por mitad entre ambos progenitores.

c) En cuanto a la atribución del uso de la vivienda familiar sita en [DOMICILIO]: que se atribuya su uso a mi representado/a y a los hijos comunes.

Y con condena en costas a la parte demandada, si concurrieren las circunstancias previstas en el artículo 394 de la Ley de Enjuiciamiento Civil.

Es justicia que insto en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma de Abogado: [NOMBRE Y APELLIDOS, Nº DE COLEGIADO]

Firma de Procurador: [NOMBRE Y APELLIDOS]
