---
name: demanda-guarda-custodia-alimentos-hijos-menores-civ-0257
description: "Demanda de guarda y custodia y alimentos de hijos menores. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de guarda y custodia y alimentos de hijos menores

> Formulario **CIV-0257** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de guarda y custodia y alimentos de hijos menores» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de guarda y custodia y alimentos de hijos menores” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-guarda-custodia-alimentos-hijos-menores-civ-0257`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE DEL HIJO/A 1 (2 veces)
- [ ] NOMBRE DEL HIJO/A 2 (2 veces)
- [ ] Nº (2 veces)
- [ ] CALLE
- [ ] EDAD
- [ ] FECHA
- [ ] FECHAS
- [ ] LUGAR Y FECHA
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] Nº DE DOCUMENTO
- [ ] PETICIÓN
- [ ] PISO
- [ ] PUERTA
- [ ] SEDE

## Normas que cita el formulario

- art. 770 LEC
- art. 769 LEC
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 770.4 Código Civil
- art. 749.2 LEC

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

- Junto a «…NCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.R.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.R.C.

-SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD-

Don [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en la representación que ostento de Doña [NOMBRE Y APELLIDOS], según acredito mediante escritura de poderes que acompaño para su unión a los autos mediante testimonio, previo cotejo y devolución del original, y bajo la dirección letrada de Don [NOMBRE Y APELLIDOS] ante el Tribunal que por turno de reparto corresponda comparezco y, como mejor proceda en Derecho, DIGO:

Que siguiendo instrucciones de mi poderdante por medio del presente escrito interpongo, en nombre del mismo y de sus hijos menores, DEMANDA SOBRE GUARDA Y CUSTODIA Y RECLAMACIÓN DE ALIMENTOS EN NOMBRE LOS HIJOS MENORES de filiación extramatrimonial [NOMBRE DEL HIJO/A 1] y [NOMBRE DEL HIJO/A 2] de los litigantes, contra Don [NOMBRE Y APELLIDOS], vecino de la localidad de [LOCALIDAD], con domicilio en calle [CALLE], núm. [Nº], piso [PISO], puerta [PUERTA], la cual baso en los siguientes

HECHOS

PRIMERO.- Mi representada y el demandado han venido manteniendo una relación sentimental con períodos de convivencia esporádica, fruto de la cual nacieron y viven en la actualidad dos hijos llamados [NOMBRE DEL HIJO/A 1] y [NOMBRE DEL HIJO/A 2], nacidos los días [FECHAS] y [FECHA], por consiguiente, de [EDAD] y [Nº] años de edad respectivamente, según acredito mediante certificación literal del Registro Civil de la localidad de [LOCALIDAD] que acompaño como documento número dos.

SEGUNDO.- Mi representada reside en su domicilio en compañía de sus hijos desde el nacimiento de éstos, relacionándose en algunas ocasiones con el padre, quien ha venido visitándolos en fines de semana alternos. No obstante, desde hace dos años, el padre está desatendiendo a los hijos comunes, dejando de satisfacer prestación económica alguna para su manutención, realizando las visitas en los días que arbitrariamente considera oportunos, con el consecuente transtorno para mi representada y sus hijos, motivo por el cual se inicia el presente procedimiento a fin de regularizar la situación y fijar la cantidad que debe satisfacer el demandado en concepto de alimentos de los hijos menores.

TERCERO.- De acuerdo a lo anterior, debemos instar las siguientes medidas en relación a la guarda y custodia, visitas y comunicación, y alimentos de los hijos comunes:

a) En cuanto a las medidas personales respecto a los hijos comunes: [PETICIÓN].

b) En cuanto a los alimentos para los menores: (fundamentar las medidas relativas a estos extremos, con la cláusula de actualización de la pensión que en su caso se solicite, incluyendo la documental a que se refiere el art. 770 regla 1ª de la LEC).

CUARTO.- Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

FUNDAMENTOS DE DERECHO

I. Legitimación activa y pasiva. La ostentan ambas partes por su condición de progenitores de los hijos comunes.

II. Competencia. Es competente este Tribunal, de conformidad con lo previsto en el artículo 769 de la LEC.

III. Cumplimiento de los requisitos de procedibilidad. La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

IV. Efectos derivados o medidas. Artículos 154 y ss. del Código Civil en relación con los arts. 90 y ss. del Código Civil, en su nueva redacción dada por la Ley 8/2021 de 2 de junio y la Ley 17/2021 de 15 diciembre

V. Audiencia de los menores. La audiencia del menor es preceptiva, conforme a lo previsto en el artículo 770.4 del Código Civil y los nuevos criterios de la Ley 8/2021.

VI. Procedimiento. Son de aplicación las normas contenidas en el Libro IV, Título Primero, Capítulo Primero de la LEC, y las normas del juicio verbal, con sujeción, además, a las reglas establecidas en el artículo 770 de la misma ley, conforme se previene en el párrafo preliminar de dicho artículo.

VII. Intervención del Ministerio Fiscal. Procede la intervención del Ministerio Fiscal, por existir dos hijos menores de edad, conforme a lo previsto en el artículo 749.2º de la LEC.

VIII. Medidas Propuestas:

a) Custodia:

b) Régimen de comunicación y visitas con el progenitor no custodio:

c) Pensión de alimentos a favor de los hijos menores de edad:

IX. Costas. Artículo 394 de la LEC.

X. Demás normas concordantes y de aplicación: Iura novit Curia.

En su virtud,

SUPLICO AL TRIBUNAL: Que tenga por presentado este escrito con los documentos acompañados y sus copias; admita todo ello; por interpuesta por el Procurador que suscribe, con quien se entiendan las sucesivas diligencias, en nombre y representación de Don [NOMBRE Y APELLIDOS], con devolución de la escritura de poderes una vez quede testimonio en autos, DEMANDA DE GUARDA Y CUSTODIA Y ALIMENTOS EN NOMBRE DE LOS HIJOS MENORES contra Don [NOMBRE Y APELLIDOS]; y previa notificación y emplazamiento, y tras los trámites procesales pertinentes, con intervención del Ministerio Fiscal y audiencia de los menores, dicte sentencia por la que con estimación de nuestra demanda, establezca las medidas propuestas en el Fundamento de Derecho VII que se dan por reproducidas a fin de evitar reiteraciones innecesarias. Y con condena en costas a la parte demandada, si concurrieren las circunstancias previstas en el artículo 394 de la Ley de Enjuiciamiento Civil.

Es justicia que insto en [LUGAR Y FECHA]

========================================================================
