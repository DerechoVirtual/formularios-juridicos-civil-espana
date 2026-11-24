---
name: demanda-extincion-pareja-estable-segun-derecho-civil-civ-0235
description: "Demanda de extinción de pareja estable según el Derecho civil catalán. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de extinción de pareja estable según el Derecho civil catalán

> Formulario **CIV-0235** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de extinción de pareja estable según el Derecho civil catalán» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de extinción de pareja estable según el Derecho civil catalán” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-extincion-pareja-estable-segun-derecho-civil-civ-0235`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (11 veces)
- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] AÑO (7 veces)
- [ ] Nº DE DOCUMENTO (6 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] FECHA (2 veces)
- [ ] SEDE (2 veces)
- [ ] DÍA
- [ ] LETRA O Nº DE APARTADO
- [ ] LUGAR
- [ ] MARCA/MODELO
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] MES
- [ ] NOMBRE Y APELLIDOS DEL ABOGADO
- [ ] NOMBRE Y APELLIDOS DEL NOTARIO
- [ ] Nº
- [ ] TELÉFONO

## Normas que cita el formulario

- art. 234.1 Código Civil
- art. 234.4 Código Civil
- art. 234.7 Código Civil
- art. 234 Código Civil
- art. 234.9 Código Civil
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

### Avisos de actualización (3) — se aplican en el texto, nunca se copian en el documento

- Junto a «…NCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.R.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.
- Junto a «…ción Letrada de Don [NOMBRE Y APELLIDOS] ante el Tribunal de Instancia de [SEDE]»: Un solo TI por partido judicial (art. 84.1 LOPJ): sobra «de los de». Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

Don/Dª [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en la representación que ostento de Doña [NOMBRE Y APELLIDOS], según acredito mediante escritura de poderes que acompaño para su unión a los autos mediante testimonio, previo cotejo y devolución del original, y bajo la dirección Letrada de Don [NOMBRE Y APELLIDOS] ante el Tribunal de Instancia de [SEDE] que por turno de reparto corresponda comparezco y, como mejor proceda en Derecho, DIGO:

Que por medio del presente escrito formulo demanda en ejercicio de los derechos derivados de la extinción de la relación de pareja estable frente al demandado D. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], fundado mi pretensión en los siguientes:

HECHOS

Mi representado y el demandado D. [NOMBRE Y APELLIDOS], ambos de vecindad civil catalana, han mantenido una relación de pareja estable desde el año [AÑO], conforme al art. 234.1 del Código Civil de Cataluña lo cual acredito mediante (escritura pública de fecha [FECHA] otorgada ante el Notario [NOMBRE Y APELLIDOS DEL NOTARIO] de constitución de pareja establece que acompaño como documento [Nº DE DOCUMENTO]) (o por la convivencia marital ininterrumpida por un periodo superior a dos años, concretamente de [Nº] años, según se acreditará oportunamente, aportándose los siguientes documentos: acta de notoriedad, certificado de empadronamiento, título de propiedad del inmueble, recibos de agua, luz, gas y teléfono [TELÉFONO],) (o por libro de familia o certificado de nacimiento de los hijos comunes [Nº DE DOCUMENTO])

En fecha [FECHA] y por motivos personales, se produjo la extinción de la convivencia por la causa [LETRA O Nº DE APARTADO] del artículo 234.4 del Código Civil de Cataluña ( en su caso, según acredito mediante comunicación fehaciente recibida por mi mandante, certificación del Registro Civil de matrimonio del demandado con un tercero, etc.)

No habiendo convenido nada las partes para el cese de la convivencia, son de aplicación las normas recogidas en los artículos 234.7 y siguientes del Código Civil de Cataluña, solicitándose por mi representado que se le conceda la compensación establecida en el artículo 234-9 del Código Civil de Cataluña por importe de [IMPORTE] euros, cuya procedencia se funda en que mi mandante ha trabajado para el negocio de su esposa durante todo el periodo de convivencia marital, con plena dedicación y sin compensación económica, de manera que todo el trabajo de mi representado ha revertido en el patrimonio del demandado como seguidamente paso a exponer.

1) Circunstancias de dedicación y trabajo: Mi representado y el demandado conviven desde el año [AÑO] trabajando mi representado desde esa fecha en el negocio de panadería propiedad del demandado, haciéndose cargo de todo el negocio durante todo este tiempo.

En el momento actual de ruptura de la convivencia, el saldo de la cuenta es de [IMPORTE] euros más [IMPORTE] euros en caja (aporto como documentos [Nº DE DOCUMENTO] resúmenes contables del negocio desde el año [AÑO] al año [AÑO]), donde se acreditan dichas ganancias.

Durante todo este tiempo, mi representado no cobró sueldo alguno y trabajaba a tiempo completo en el negocio, haciéndose cargo del mismo de forma exclusiva, como contable, atendiendo la tienda y dirigiendo a los otros tres empleados del negocio.

2) Determinación de la compensación. Incrementos de patrimonio: Tal como consta en el inventario que se acompaña a esta demanda como documento número [Nº DE DOCUMENTO] en cumplimiento de lo dispuesto en la disposición adicional cuarta del Libro II del Código Civil de Cataluña, en todo este periodo de convivencia, mi mandante no ha incrementado su patrimonio, siendo titular únicamente de un vehículo marca [MARCA/MODELO] adquirido en el año [AÑO] por importe de [IMPORTE] euros; antes del matrimonio, ya poseía una vivienda en [LOCALIDAD] como donación de su madre. Por tanto, el único bien que constituye un incremento patrimonial de mi representado es el vehículo, el cual tiene actualmente un valor de [IMPORTE] euros.

Por su parte, el demandado ha adquirido varios inmuebles en todo este tiempo, actualmente sin cargas, teniendo arrendados varios de ellos, habiendo aumentado su patrimonio en un valor total de [IMPORTE] euros y percibiendo actualmente unas rentas arrendaticias de [IMPORTE] euros mensuales (acompaño como documentos [Nº DE DOCUMENTO] declaraciones de IRPF correspondientes a los años [AÑO] y certificación de los Registros de la Propiedad de [LOCALIDAD] acreditativos de estos extremos). Con arreglo a ello, el incremento patrimonial del demandado, calculado conforme a las reglas del art. 232.6, se estima en [IMPORTE] euros.

3) Solicitud de compensación por razón de trabajo: El artículo 234.9 del Código Civil de Cataluña se remite al artículo 232.5, el cual, en su apartado 3, establece que para determinar la cuantía de la compensación económica por razón de trabajo, debe tenerse en cuenta la duración e intensidad de la dedicación, teniendo en cuenta los años de convivencia, con el límite establecido en el apartado 4 concretado en la cuarta parte de la diferencia entre los incrementos de los patrimonios de los convivientes, calculada de acuerdo con las reglas establecidas por el artículo 232.6; sin embargo, si el acreedor prueba que su contribución ha sido notablemente superior, la autoridad judicial puede incrementar esta cuantía. En este caso, atendidas las circunstancias anteriores, solicitamos una compensación por razón de trabajo de [IMPORTE] euros como efecto derivado de la extinción de la relación estable de pareja.

A los anteriores Hechos le son de aplicación los siguientes

Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

FUNDAMENTOS DE DERECHO

Legitimación activa y pasiva

La ostentan ambas partes por su condición de miembros de la pareja de hecho.

Competencia

Es competente este Tribunal, de conformidad con lo previsto en los artículos 49 y siguientes, y artículo 769 LEC, en relación con lo dispuesto en el art. 85.1º LOPJ.

Procedimiento

Debe seguirse el procedimiento del art. 770 de la LEC por establecerlo así la disposición adicional sexta del Libro II del Código Civil de Cataluña.

Cumplimiento de los requisitos de procedibilidad

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

Extinción

Artículo 234.4 del Código Civil de Cataluña.

Efectos derivados

Son de aplicación las normas del Código Civil de Cataluña, en especial el artículo 234-9 en relación con los artículos 232.5 y siguientes, a los cuales se remite en relación a la compensación por razón de trabajo.

En relación a las reglas de cálculo citamos la STSJ Cataluña de 9 de mayo de 2005, rec. 122/2004 y de 29 de mayo de 2007, rec. 75/2006 que indica que pueden incluirse los bienes adquiridos mediante la inversión de rentas generadas, especialmente las procedentes del trabajo o de la actividad mercantil o industrial, el aumento y la conservación del valor experimentados por los bienes privativos de los convivientes en razón a las inversiones realizadas con las antedichas rentas o merced a la actuación directa de los propios convivientes.

Costas

Artículo 394 de la LEC.

Demás normas concordantes y de aplicación

Iura novit Curia.

En su virtud,

SUPLICO AL TRIBUNAL: Que tenga por presentado este escrito con los documentos acompañados y sus copias; admita todo ello; por interpuesta por el Procurador que suscribe, con quien se entiendan las sucesivas diligencias, en nombre y representación de Don [NOMBRE Y APELLIDOS], con devolución de la escritura de poderes una vez quede testimonio en autos, demanda para determinar los efectos de la extinción de la relación de pareja estable contra D [NOMBRE Y APELLIDOS]; y previa notificación y emplazamiento, y por los trámites procesales pertinentes, se dicte sentencia por la que se estime la demanda y se condene al demandado [NOMBRE Y APELLIDOS] a indemnizar a mi representado en la cantidad de [IMPORTE] euros, más los intereses correspondientes, en concepto de compensación económica por extinción de la relación de pareja estable, todo ello con expresa imposición de costas a la parte demandada.

OTROSÍ PRIMERO DIGO: Que fijo la cuantía del proceso en la cantidad de [IMPORTE] euros.

En virtud de lo anterior,

SUPLICO AL TRIBUNAL: que tenga por hecha la anterior manifestación a los efectos pertinentes y por acompañado el documento justificativo de la tasa.

Es justicia que insto en [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma de Abogado [NOMBRE Y APELLIDOS DEL ABOGADO] Firma de Procurador

========================================================================
